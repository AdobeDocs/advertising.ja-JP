---
title: Adobe AdvertisingID 使用者 [!DNL Analytics]
description: Adobe AdvertisingID 使用者 [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 426f6e25f0189221986cc42d186bfa60f5268ef1
workflow-type: tm+mt
source-wordcount: '1653'
ht-degree: 0%

---

# Adobe AdvertisingID 使用者 [!DNL Analytics]

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertisingでは、オンサイトパフォーマンストラッキングに 2 つの ID( *EF ID* そして *AMO ID*.

広告インプレッションが発生すると、Adobe Advertisingは AMO ID と EF ID の値を作成して保存します。 広告を閲覧した訪問者が広告をクリックせずにサイトに入ったとき、 [!DNL Analytics] は、を通じてこれらの値をAdobe Advertisingから呼び出します [!DNL Analytics for Advertising] JavaScript コード。 ビュースルートラフィックの場合、 [!DNL Analytics] は追加の ID(`SDID`) で始まり、EF ID と AMO ID をステッチするために使用されます。 [!DNL Analytics]. クリックスルートラフィックの場合、これらの ID は `ef_id` および `s_kwcid` （AMO ID の場合）クエリー文字列パラメーター。

Adobe Advertisingは、次の条件を使用して、Web サイトへのクリックスルーエントリとビュースルーエントリを区別します。

* ビュースルーエントリは、広告を表示した後、広告をクリックせずにユーザーがサイトを訪問した場合に取り込まれます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。

   * 訪問者には、 [!DNL DSP] または [!DNL Search, Social, & Commerce] 次の期間の広告 [ルックバックウィンドウをクリック](#lookback-a4adc).

   * 訪問者が少なくとも 1 つを閲覧しました [!DNL DSP] 次の期間の広告 [インプレッションのルックバックウィンドウ](#lookback-a4adc). 最後のインプレッションは、ビュースルーとして渡されます。

* クリックスルーエントリは、サイト訪問者がサイトに入る前に広告をクリックするとキャプチャされます。 [!DNL Analytics] は、次のいずれかの条件が発生した場合にクリックスルーをキャプチャします。

   * URL には、Adobe Advertising別のランディングページ URL に追加された EF ID と AMO ID が含まれます。

   * URL にトラッキングコードは含まれていませんが、Adobe Advertisingの JavaScript コードが過去 2 分以内にクリックを検出しました。

![Adobe Advertisingビューベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-view-through-process.png)

*図 1:Adobe Advertisingビューベース [!DNL Analytics] 統合*

![Adobe Advertisingクリックの URL ベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Adobe Advertisingクリックの URL ベース [!DNL Analytics] 統合*

## Adobe AdvertisingEF ID

EF ID は、アクティビティをオンラインクリックまたは広告露出に関連付けるためにAdobe Advertisingが使用する一意のトークンです。 EF ID は、に格納されます。 [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または [!DNL rVar] （予約済み） [!DNL eVar]) ディメンション (Adobe AdvertisingEF ID) を使用して、個々のブラウザーまたはデバイスレベルでの各広告のクリックまたは露出を追跡します。 EF ID は主に送信のキーとして機能します [!DNL Analytics] データをAdobe Advertisingに送信し、Adobe Advertising内でのレポートおよび入札の最適化を行います。

### EF ID 形式

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 次の場合、 [!DNL Analytics] 実装により、URL トラッキングが強制的に小文字に変換され、Adobe Advertisingは EF ID を認識しません。 これはAdobe Advertisingの入札とレポートに影響しますが、内のAdobe Advertisingレポートには影響しません。 [!DNL Analytics].

#### [!DNL Google Ads] 広告を検索

```
{gclid}:G:s
```

場所：

* `gclid` が [!DNL Google Click ID] (GCLID) を使用します。
* `s` はネットワークタイプです（「s」は検索用）。

#### Microsoft Advertising 検索広告

```
{msclkid}:G:s
```

場所：

* `msclkid` が [!DNL Microsoft Click ID] (MSCLKID)。
* `s` はネットワークタイプです（「s」は検索用）。

#### 他の検索エンジンでの広告と検索広告の表示

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

場所：

* &lt;*Adobe Advertising訪問者 ID*> は、訪問者ごとの一意の ID です（UhKVaAABCkJ0mDt など）。 また、 *サーファー ID*.

* &lt;*timestamp*> は、YYYYMMDDHHMMSS という形式の時刻です (2019 年の場合は20190821192533、08 月の場合は 21 日、19 時など )。:25:33).

* &lt;*チャネルタイプ*> は、クリックまたは露出の原因となるチャネルタイプです。

   * `d` DSPディスプレイ広告のクリック（クリックスルーを表示）
   * `i` DSPディスプレイ広告のインプレッション（表示ビュースルー）の場合
   * `s` 検索広告のクリック（検索クリックスルー）。

例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### の EF IDDimension [!DNL Analytics]

In [!DNL Analytics] レポートでは、EF ID データを検索するには、 [!UICONTROL EF ID] ディメンションと使用 [!UICONTROL EF ID Instance] 指標。

EF ID には、Analysis Workspaceでの 500,000 個の一意の ID 制限が適用されます。 500,000 個の値に達すると、すべての新しいトラッキングコードが 1 行項目のタイトル「[!UICONTROL Low Traffic].&quot; レポートの正確性が欠落する可能性があるので、EF ID は分類されず、でのセグメントやレポートに使用しないでください [!DNL Analytics].

## Adobe AdvertisingAMO ID {#amo-id}

AMO ID は、より詳細なレベルで一意の広告の組み合わせを追跡し、 [!DNL Analytics] 広告指標（インプレッション数、クリック数、コストなど）のデータ分類とAdobe Advertisingからの取り込み AMO ID は、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション (AMO ID)。でのレポートにのみ使用されます。 [!DNL Analytics].

AMO ID は、 `s_kwcid`(「[!DNL the squid].&quot;

### AMO ID の実装方法

パラメーターは、次のいずれかの方法でトラッキング URL に追加されます。

* （推奨）サーバー側挿入機能が実装されています。

   * DSPのお客様：ピクセルサーバーは、エンドユーザーがディスプレイ広告とAdobe Advertisingピクセルを表示すると、ランディングページのサフィックスに s_kwcid パラメーターを自動的に追加します。

   * 検索、ソーシャル、コマースのお客様：

      * の場合 [!DNL Google Ads] および [!DNL Microsoft® Advertising] アカウントの [!UICONTROL Auto Upload] アカウントまたはキャンペーンに対してを有効にすると、エンドユーザーがAdobe Advertisingピクセルを持つ広告をクリックすると、ピクセルサーバーによって s_kwcid パラメーターがランディングページのサフィックスに自動的に追加されます。

      * 他の広告ネットワークの場合、または [!DNL Google Ads] および [!DNL Microsoft® Advertising] アカウントの [!UICONTROL Auto Upload] を無効に設定した場合、アカウントレベルの追加パラメーターに手動でパラメーターを追加して、ベース URL に追加します。

* サーバー側挿入機能は実装されていません。

   * DSPのお客様：

      * の場合 [!DNL Flashtalking] 広告タグ、「 」ごとに追加のマクロを手動で挿入[追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * の場合 [!DNL Google Campaign Manager 360] 広告タグ、「 」ごとに追加のマクロを手動で挿入[追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * 検索、ソーシャル、コマースのお客様：

      * の場合 ([!DNL Google Ads] および [!DNL Microsoft® Advertising]) 広告の場合は、ランディングページのサフィックスに AMO ID パラメーターを手動で追加します。

      * その他すべての広告ネットワーク上の広告の場合は、AMO ID パラメーターをアカウントレベルの追加パラメーターに手動で追加し、ベース URL に追加します。

サーバー側挿入機能を実装する場合や、ビジネスに最適なオプションを決定する場合は、Adobeアカウントチームにお問い合わせください。

### AMO ID の形式 {#amo-id-formats}

#### の AMO ID フォーマット [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

場所：

* `AC` ディスプレイチャネルを示します。

* `{TM_AD_ID}` は、Adobe Advertisingで生成される英数字の広告キーです。 広告の一意の識別子として使用され、広告エンティティのメタデータを読み取り可能なAdobe Advertisingに変換するためのキーとして機能します [!DNL Analytics] ディメンション。

* `{TM_PLACEMENT_ID}` は、Adobe Advertising生成の英数字配置キーです。 配置の一意の識別子として使用され、Adobe Advertisingエンティティのメタデータを読み取り可能に変換するためのキーとして機能します [!DNL Analytics] ディメンション。

AMO ID の例： AC!iIMvXqlOa6Nia2lDvtgw!GrV6o2oV2qQLjQiXLC7

#### 検索、ソーシャル、コマース広告の AMO ID 形式

パラメーターは広告ネットワークによって異なりますが、次のパラメーターはすべてに共通です。

* `AL` は、検索チャネルを示します。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` は、広告主に割り当てられる一意のユーザー ID です。

* `{sid}` は、広告主の広告ネットワークアカウントの数値 ID に置き換えられます。 *3* 対象： [!DNL Google Ads], *10* 対象： [!DNL Microsoft Advertising], *45* 対象： [!DNL Meta], *86* 対象： [!DNL Yahoo! Display Network], *87* 対象： [!DNL Naver], *88* 対象： [!DNL Baidu], *90* 対象： [!DNL Yandex], *94* 対象： [!DNL Yahoo! Japan Ads], *105* 対象： [!DNL Yahoo Native] （非推奨）、または *106* 対象： [!DNL Pinterest] （非推奨）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

場所：

* `{creative}` は、クリエイティブに対する広告ネットワークの一意の数値 ID です。
* `{placement}` は、広告がクリックされた Web サイトです。
* `{keywordid}` は、広告をトリガーしたキーワードに関する、広告ネットワークの一意の数値 ID です。

##### [!DNL Google Ads]

これには、 [!DNL Google Merchant Center].

* 最新の AMO ID 形式を使用するアカウント。パフォーマンスの最大キャンペーンとドラフト&amp;実験キャンペーンのキャンペーンレベルおよび広告グループレベルのレポートをサポートします。

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* その他すべてのアカウント：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

場所：

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` が [!DNL Google Ads] クリエイティブの一意の数値 ID。
* `{matchtype}` は、広告をトリガーしたキーワードの一致タイプです。 `e` 正確には `p` ( フレーズの場合は、 `b` 幅の広い
* `{placement}` は、広告がクリックされた Web サイトのドメイン名です。 値は、配置ターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` クリックが発生したネットワークを示します。 `g` 対象： [!DNL Google] 検索（キーワードターゲット広告のみ） `s` 検索パートナー（キーワードターゲット広告のみ）の場合、または `d` ディスプレイネットワーク用（キーワードターゲット広告またはプレースメントターゲット広告用）。
* `{product_partition_id}` は、製品広告と共に使用される、広告ネットワークの一意の数値 ID です。
* `{keyword}` は、（検索サイトで）広告をトリガーした特定のキーワードか、（コンテンツサイトで）最適なキーワードのどちらかです。
* `{campaignid}` は、キャンペーンに関する広告ネットワークの一意の数値 ID です。
* `{adgroupid}` は、広告グループに対する広告ネットワークの一意の数値 ID です。

>[!NOTE]
>
>* 動的検索広告の場合、 {keyword} が自動ターゲットに設定されている。
>* のトラッキングを生成する際 [!DNL Google] 買い物広告、製品 ID パラメーター `{adwords_producttargetid}`の前に、が挿入されます。 製品 ID パラメーターが [!DNL Google Ads] アカウントレベルおよびキャンペーンレベルのトラッキングパラメーター。
>* 最新の AMO ID トラッキングコードを使用するには、[の AMO ID トラッキングコードを更新します。 [!DNL Google Ads] アカウント](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* キャンペーンの検索：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 買い物キャンペーン ( [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* オーディエンスネットワークキャンペーン：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

場所：

* `{AdId}` は、クリエイティブに対する広告ネットワークの一意の数値 ID です。
* `{OrderItemId}` は、キーワードに対する広告ネットワークの数値 ID です。
* `{CriterionId}` は、製品広告と共に使用される製品グループに対する広告ネットワークの数値 ID です。

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

場所：

* `{creative}` は、クリエイティブに対する広告ネットワークの一意の数値 ID です。
* `{matchtype}` は、広告をトリガーしたキーワードの一致タイプです。 `be` 正確には `bp` ( フレーズの場合は、 `bb` 幅の広い
* `{network}` クリックが発生したネットワークを示します。 `n` ネイティブまたは `s` を検索します。
* `{keyword}` は、広告をトリガーしたキーワードです。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

場所：

* `{ad_id}` は、クリエイティブに対する広告ネットワークの一意の数値 ID です。
* `{source_type}` は、広告が表示されたサイトのタイプです。 *b* 検索には *c* ( コンテキスト（コンテンツ）の場合 )、または *ct* （カテゴリ用）
* `{phrase_id}` は、キーワードに対する広告ネットワークの数値 ID です。

### AMO IDDimension（内） [!DNL Analytics]

Analytics レポートでは、 [!UICONTROL AMO ID] ディメンションと使用 [!UICONTROL AMO ID Instance] 指標。 The [!UICONTROL AMO ID] ディメンションには、取得されたすべての AMO ID 値が格納されますが、 [!UICONTROL AMO ID Instance] 指標は、AMO ID 値がサイトによってキャプチャされた頻度を示します。 例えば、同じ検索広告が 4 回クリックされたが、Analytics が 7 つのサイトエントリを追跡した場合、 [!UICONTROL AMO ID Instance] 7(7) で [!UICONTROL Clicks] は 4(4) です。

内の任意のレポートまたは監査 [!DNL Analytics]を使用する場合、ベストプラクティスは、AMO ID を対応するインスタンスと共に使用することです。 詳しくは、[のデータ検証 [!DNL Analytics for Advertising]](data-variances.md#data-validation)」(「 [!DNL Analytics] そしてAdobe Advertising」

## Analytics 分類について

In [!DNL Analytics], a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) は、アカウント、キャンペーン、広告など、特定のトラッキングコードのメタデータの一部です。 Adobe Advertisingは、レポートを生成する際に様々な方法（広告タイプやキャンペーン別など）でデータを表示できるように、分類を使用して生のAdobe Advertisingデータを分類します。 分類は、 [!DNL Analytics] とは、AMO 指標と共に使用できます。例： [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]、および [!UICONTROL AMO Clicks]、およびのようなカスタムおよび標準のオンサイトイベント [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]、および [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe Advertising](data-variances.md)
