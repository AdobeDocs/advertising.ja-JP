---
title: が使用するAdobe Advertising ID [!DNL Analytics]
description: が使用するAdobe Advertising ID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 0%

---

# が使用するAdobe Advertising ID [!DNL Analytics]

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertisingでは、オンサイトのパフォーマンストラッキングに 2 つの ID を使用します。 *EF ID* および *AMO ID*.

広告インプレッションが発生すると、Adobe Advertisingは AMO ID と EF ID の値を作成して保存します。 広告を見た訪問者が広告をクリックせずにサイトに入ると、 [!DNL Analytics] では、これらの値をAdobe Advertisingから次を使用して呼び出します [!DNL Analytics for Advertising] JavaScript コード。 ビュースルートラフィックの場合、 [!DNL Analytics] 追加の ID （`SDID`）。EF ID と AMO ID をにステッチするために使用されます。 [!DNL Analytics]. クリックスルートラフィックの場合、これらの ID は次を使用してランディングページ URL に含まれます `ef_id` および `s_kwcid` （AMO ID の場合） クエリ文字列パラメーター。

Adobe Advertisingは、次の条件を使用して、web サイトに対するクリックスルーまたはビュースルーエントリを区別します。

* ビュースルーエントリは、ユーザーが広告を表示したがクリックしなかった後にサイトを訪問した際に取得されます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。

   * 訪問者にはに対するクリックスルーがありません [!DNL DSP] または [!DNL Search, Social, & Commerce] 次の期間の広告 [クリックルックバックウィンドウ](#lookback-a4adc).

   * 訪問者に 1 人以上が表示されている [!DNL DSP] 次の期間の広告 [インプレッションルックバックウィンドウ](#lookback-a4adc). 最後のインプレッションがビュースルーとして渡されます。

* クリックスルーのエントリは、サイト訪問者がサイトに入る前に広告をクリックした際にキャプチャされます。 [!DNL Analytics] 次のいずれかの状況が発生した場合、クリックスルーをキャプチャします。

   * URL には、Adobe Advertisingによってランディングページ URL に追加された EF ID と AMO ID が含まれます。

   * URL にはトラッキングコードが含まれていませんが、Adobe Advertising JavaScript コードが過去 2 分以内にクリックを検出します。

![Adobe Advertisingビューベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-view-through-process.png)

*図 1: Adobe Advertisingビューベース [!DNL Analytics] 統合*

![Adobe Advertisingクリックの URL ベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Adobe Advertisingクリックの URL ベース [!DNL Analytics] 統合*

## Adobe Advertisingの EF ID

EF ID は、Adobe Advertisingがアクティビティをオンラインクリックまたは広告漏洩に関連付けるために使用する一意のトークンです。 EF ID は次の場所に保存されます。 [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または [!DNL rVar] （予約済み [!DNL eVar]）のディメンション（Adobe Advertisingの EF ID）を設定し、個々のブラウザーまたはデバイスレベルで各広告のクリックまたは露出をトラッキングします。 EF ID は、主に送信用のキーとして機能します [!DNL Analytics] Adobe Advertising内でのレポート作成と入札最適化のためのデータをAdobe Advertisingに送信します。

### EF ID フォーマット

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 次の場合： [!DNL Analytics] を実装すると、URL トラッキングが小文字に変換され、Adobe Advertisingで EF ID が認識されません。 これは、Adobe Advertisingの入札とレポートに影響しますが、内のAdobe Advertisingレポートには影響しません [!DNL Analytics].

#### [!DNL Google Ads] 広告を検索

```
{gclid}:G:s
```

ここで、

* `gclid` が [!DNL Google Click ID] （GCLID）。
* `s` はネットワークタイプ（検索用は「s」）です。

#### [!DNL Microsoft Advertising] 広告を検索

```
{msclkid}:G:s
```

ここで、

* `msclkid` が [!DNL Microsoft Click ID] （MSCLKID）。
* `s` はネットワークタイプ（検索用は「s」）です。

#### 他の検索エンジンでの広告および検索広告の表示

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

ここで、

* &lt;*Adobe Advertising訪問者 ID*> は、訪問者ごとの一意の ID （UhKVaAABCkJ0mDt など）。 「the」とも呼ばれる *サーファー ID*.

* &lt;*timestamp*> は、YYYYMMDDHHMMSS 形式の時間（2019 年、08 月、21 日、19 日の 20190821192533 など）:25:33）。

* &lt;*チャネルタイプ*> は、クリックまたは露出を行うチャネルのタイプです。

   * `d` DSP ディスプレイ広告をクリックした場合（表示のクリックスルー）
   * `i` DSP ディスプレイ広告のインプレッションの場合（ビュースルーの表示）
   * `s` 検索広告をクリックしてください（検索クリックスルー）。

例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### の EF IDDimension [!DNL Analytics]

対象： [!DNL Analytics] レポートを検索すると、EF ID データを見つけることができます。 [!UICONTROL EF ID] のディメンション設定と使用 [!UICONTROL EF ID Instance] 指標。

EF ID は、Analysis Workspaceで 500,000 個の ID 制限の対象となります。 500,000 個の値に達すると、すべての新しいトラッキングコードが 1 行項目のタイトルの下にレポートされます」[!UICONTROL Low Traffic].」と入力します。 レポートの忠実性が失われる可能性があるので、EF ID は分類されず、のセグメントやレポートに使用しないでください [!DNL Analytics].

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID は、一意の各広告の組み合わせをあまり詳細でないレベルでトラッキングし、次の目的に使用されます [!DNL Analytics] Adobe Advertisingからの広告指標（インプレッション数、クリック数、コストなど）のデータの分類と取り込み。 AMO ID は [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または変数ディメンション（AMO ID）で、のレポートにのみ使用されます。 [!DNL Analytics].

AMO ID は `s_kwcid`（場合によっては「」と発音されます）[!DNL the squid].」と入力します。

### AMO ID を実装する方法 {#amo-id-implement}

パラメーターは、次のいずれかの方法でトラッキング URL に追加されます。

* （推奨） サーバーサイド挿入機能を実装する場合。

   * DSPのお客様：Pixel Server は、エンドユーザーがAdobe Advertisingピクセルでディスプレイ広告を表示する際に、ランディングページサフィックスに s_kwcid パラメーターを自動的に追加します。

   * 検索、ソーシャル、Commerceのお客様：

      * の場合 [!DNL Google Ads] および [!DNL Microsoft® Advertising] のアカウント [!UICONTROL Auto Upload] アカウントまたはキャンペーンに対して有効な設定では、エンドユーザーがAdobe Advertisingピクセルで広告をクリックすると、ピクセルサーバーによってランディングページのサフィックスに s_kwcid パラメーターが自動的に追加されます。

      * その他の広告ネットワークの場合 [!DNL Google Ads] および [!DNL Microsoft® Advertising] のアカウント [!UICONTROL Auto Upload] 無効の場合、パラメーターをに手動で追加 [勘定科目レベル追加パラメータ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}：ベース URL に追加します。

* サーバーサイド挿入機能が実装されていない場合：

   * DSPのお客様： [JavaScript コード](javascript.md) は、クリックスルーとビュースルーを自動的に記録します。 ブラウザーがサードパーティ cookie をサポートしていない場合でも、次の広告タイプのクリックベースのコンバージョンを追跡できます。

      * の場合 [!DNL Flashtalking] タグを追加し、「」ごとに手動で追加マクロを挿入する[Append [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ](/help/integrations/analytics/macros-flashtalking.md).」と入力します。

      * の場合 [!DNL Google Campaign Manager 360] タグを追加し、「」ごとに手動で追加マクロを挿入する[Append [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ](/help/integrations/analytics/macros-google-campaign-manager.md).」と入力します。

   * 検索、ソーシャル、Commerceのお客様：

      * （用）[!DNL Google Ads] および [!DNL Microsoft® Advertising]）を使用する場合は、ランディングページのサフィックスに AMO ID パラメーターを手動で追加します（理想的には、 [アカウントレベル](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} 個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除きます。

      * その他のすべての広告ネットワークの広告の場合、AMO ID パラメーターを手動で [勘定科目レベル追加パラメータ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}：ベース URL に追加します。

サーバーサイドの挿入機能を実装する、またはお客様のビジネスに最適なオプションを判断するには、Adobeアカウントチームにお問い合わせください。

### AMO ID 形式 {#amo-id-formats}

#### の AMO ID 形式 [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

ここで、

* `AC` ディスプレイチャネルを示します。

* `{TM_AD_ID}` は、Adobe Advertisingで生成された英数字の広告キーです。 Adobe Advertisingの一意の ID として使用され、広告エンティティメタデータを読み取り可能に変換するためのキーとして機能します [!DNL Analytics] ディメンション。

* `{TM_PLACEMENT_ID}` は、Adobe Advertisingで生成される英数字のプレースメントキーです。 プレースメントの一意の ID として使用され、Adobe Advertisingエンティティのメタデータを読み取り可能に変換するためのキーとして機能します [!DNL Analytics] ディメンション。

AMO ID の例：AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### 検索、ソーシャル、Commerce広告の AMO ID 形式 {#amo-id-format-search}

パラメーターは広告ネットワークによって異なりますが、次のパラメーターはすべてのユーザーに共通です。

* `AL` 検索チャネルを示します。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` は、広告主に割り当てられた一意のユーザー ID です。

* `{sid}` は、広告主の広告ネットワークアカウントの数値 ID に置き換えられます。 *3* （用） [!DNL Google Ads], *10* （用） [!DNL Microsoft Advertising], *45* （用） [!DNL Meta], *86* （用） [!DNL Yahoo! Display Network], *87* （用） [!DNL Naver], *88* （用） [!DNL Baidu], *90* （用） [!DNL Yandex], *94* （用） [!DNL Yahoo! Japan Ads], *105* （用） [!DNL Yahoo Native] （非推奨）、または *106* （用） [!DNL Pinterest] （非推奨）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

ここで、

* `{creative}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{placement}` は、広告がクリックされた web サイトです。
* `{keywordid}` は、広告をトリガーしたキーワードの広告ネットワークの一意の数値 ID です。

##### [!DNL Google Ads]

これには、を使用したショッピングキャンペーンが含まれます [!DNL Google Merchant Center].

* 最新の AMO ID 形式を使用するアカウント。この形式は、Performance MAX キャンペーンおよびドラフト/実験キャンペーンに関するキャンペーンレベルおよび広告グループレベルのレポートをサポートします。

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* その他すべてのアカウント：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

ここで、

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` が [!DNL Google Ads] クリエイティブの一意の数値 ID。
* `{matchtype}` は、広告をトリガーしたキーワードのマッチタイプです。 `e` exact の場合、 `p` フレーズ用、または `b` 広い。
* `{placement}` は、広告がクリックされた web サイトのドメイン名です。 値は、プレースメントターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` クリックが発生したネットワークを示します。 `g` （用） [!DNL Google] 検索（キーワードターゲット広告のみ） `s` 検索パートナー（キーワードターゲット広告の場合のみ）または `d` ディスプレイネットワークの場合（キーワードターゲット広告またはプレースメントターゲット広告のいずれか）。
* `{product_partition_id}` は、製品広告で使用される製品グループの広告ネットワークの一意の数値 ID です。
* `{keyword}` は、広告をトリガーした特定のキーワード（検索サイトの場合）または最も一致したキーワード（コンテンツサイトの場合）です。
* `{campaignid}` は、キャンペーンにおける広告ネットワークの一意の数値 ID です。
* `{adgroupid}` は、広告グループの広告ネットワークの一意の数値 ID です。

>[!NOTE]
>
>* 動的検索広告の場合、 {keyword} には、自動ターゲットが設定されます。
>* のトラッキングを生成する場合 [!DNL Google] ショッピング広告、製品 ID パラメーター、 `{adwords_producttargetid}`、がキーワードパラメーターの前に挿入されます。 製品 ID パラメーターがに表示されません [!DNL Google Ads] アカウントレベルとキャンペーンレベルのトラッキングパラメーター。
>* 最新の AMO ID トラッキングコードを使用するには、「」を参照してください[の AMO ID トラッキングコードの更新 [!DNL Google Ads] アカウント](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).」と入力します。 <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* 検索キャンペーン：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* ショッピングキャンペーン （使用 [!DNL Microsoft Merchant Center]）:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* オーディエンスネットワークキャンペーン：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

ここで、

* `{AdId}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{OrderItemId}` は、広告ネットワークのキーワードに対する数値 ID です。
* `{CriterionId}` は、製品広告で使用される製品グループの広告ネットワークの数値 ID です。

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

ここで、

* `{creative}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{matchtype}` は、広告をトリガーしたキーワードのマッチタイプです。 `be` exact の場合、 `bp` フレーズ用、または `bb` 広い。
* `{network}` クリックが発生したネットワークを示します。 `n` ネイティブまたは `s` を検索します。
* `{keyword}` は、広告をトリガーしたキーワードです。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

ここで、

* `{ad_id}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{source_type}` は、広告が表示されたサイトのタイプです。 *b* 検索の場合、 *c* コンテキスト（コンテンツ）の場合 *ct* カテゴリの場合。
* `{phrase_id}` は、広告ネットワークのキーワードに対する数値 ID です。

### での AMO IDDimension [!DNL Analytics]

Analytics レポートでは、を検索することで AMO ID データを見つけることができます [!UICONTROL AMO ID] のディメンション設定と使用 [!UICONTROL AMO ID Instances] 指標。 この [!UICONTROL AMO ID] ディメンションには、取り込まれたすべての AMO ID 値が格納されますが、 [!UICONTROL AMO ID Instances] 指標は、AMO ID 値がサイトによってキャプチャされた頻度を示します。 例えば、同じ検索広告を 4 回クリックした後に Analytics が 7 つのサイトエントリをトラッキングした場合、次のようになります。 [!UICONTROL AMO ID Instances] は 7 で、 [!UICONTROL Clicks] は 4 になります。

内でのレポートや監査のために [!DNL Analytics]を使用する場合、ベストプラクティスは、AMO ID を対応するインスタンスと共に使用することです。 詳しくは、「」を参照してください[のクリックスルーのデータ検証 [!DNL Analytics for Advertising]](data-variances.md#data-validation)の間で予期されるデータの相違で [!DNL Analytics] とAdobe Advertising。」

## Analytics 分類について

対象： [!DNL Analytics], a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) は、アカウント、キャンペーン、広告などの特定のトラッキングコードのメタデータです。 Adobe Advertisingでは、レポートの生成時に様々な方法（広告タイプ別やキャンペーン別など）でデータを表示できるように、分類を使用して生のAdobe Advertisingデータを分類します。 分類は、のAdobe Advertisingレポートの基盤となります。 [!DNL Analytics] また、次のような AMO 指標と併用できます [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions]、および [!UICONTROL AMO Clicks]に加えて、のようなカスタムおよび標準のオンサイトイベント機能を備えています [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]、および [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [間で予期されるデータの相違 [!DNL Analytics] とAdobe Advertising](data-variances.md)
