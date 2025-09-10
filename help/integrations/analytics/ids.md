---
title: 使用するAdobe Advertising ID [!DNL Analytics]
description: 使用するAdobe Advertising ID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 1d7f66dd2d4775231fb21e3d79a2e337f375679b
workflow-type: tm+mt
source-wordcount: '1531'
ht-degree: 0%

---

# [!DNL Analytics] が使用するAdobe Advertising ID

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]* に適用

Adobe Advertisingは、オンサイトのパフォーマンストラッキングに *EF ID* と *AMO ID* の 2 つの ID を使用します。

広告インプレッションが発生すると、Adobe Advertisingは AMO ID と EF ID の値を作成して保存します。 広告を見た訪問者が広告をクリックせずにサイトに入ると、[!DNL Analytics] ではこれらの値をAdobe Advertisingから [!DNL Analytics for Advertising] JavaScript コードを通じて呼び出します。 ビュースルートラフィックの場合、[!DNL Analytics] は追加の ID （`SDID`）を生成します。これは、EF ID と AMO ID を [!DNL Analytics] にステッチするために使用されます。 クリックスルートラフィックの場合、これらの ID は、`ef_id` および `s_kwcid` （AMO ID の）クエリ文字列パラメーターを使用して、ランディングページ URL に含まれます。

Adobe Advertisingは、次の条件を使用して、web サイトに対するクリックスルーまたはビュースルーエントリを区別します。

* ビュースルーエントリは、ユーザーが広告を表示したがクリックしなかった後にサイトを訪問した際に取得されます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。

   * [!DNL DSP] クリックルックバックウィンドウ [!DNL Search, Social, & Commerce] の間、訪問者が [ または ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 広告のクリックスルーを行うことはありません。

   * 訪問者は、[!DNL DSP] インプレッションルックバックウィンドウ [ 中に少なくとも 1 つの ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 広告を確認しました。 最後のインプレッションがビュースルーとして渡されます。

* クリックスルーのエントリは、サイト訪問者がサイトに入る前に広告をクリックした際にキャプチャされます。 [!DNL Analytics] は、次のいずれかの状況が発生した場合にクリックスルーをキャプチャします。

   * URL には、Adobe Advertisingによってランディングページ URL に追加された EF ID と AMO ID が含まれます。

   * URL にはトラッキングコードが含まれていませんが、Adobe Advertising JavaScript コードは過去 2 分以内にクリックを検出します。

![Adobe Advertisingのビューベースの [!DNL Analytics] 統合 ](/help/integrations/assets/a4adc-view-through-process.png)

*図 1:Adobe Advertisingのビューベースの [!DNL Analytics] 統合*

![Adobe Advertisingで URL ベースの [!DNL Analytics] 統合をクリック ](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Adobe Advertisingのクリックの URL ベースの [!DNL Analytics] 統合*

<!-- ## Adobe Advertising EF IDs -->

{{$include /help/_includes/ef-id.md}}

### [!DNL Analytics] の EF ID Dimension

[!DNL Analytics] レポートでは、[!UICONTROL EF ID] ディメンションを検索して [!UICONTROL EF ID Instance] 指標を使用することで、EF ID データを見つけることができます。

EF ID は、Analysis Workspaceで 500,000 個の ID 制限の対象となります。 500,000 の値に達すると、すべての新しいトラッキングコードが、1 行項目タイトル「[!UICONTROL Low Traffic]」の下にレポートされます。 レポートの忠実性が失われる可能性があるため、EF ID は分類されず、セグメントや [!DNL Analytics] でのレポートに使用しないでください。

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID は、一意の各広告の組み合わせをそれほど詳細でないレベルで追跡し、Adobe Advertisingからのデータのクラス分けや広告指標（インプレッション数、クリック数、コストなど）の取り込みに [!DNL Analytics] 用します。 AMO ID は、[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション（AMO ID）に格納され、[!DNL Analytics] でのレポートにのみ使用されます。

AMO ID は `s_kwcid` とも呼ばれ、「[!DNL squid]」と発音されることがあります。

### AMO ID 形式 {#amo-id-formats}

#### [!DNL DSP] の AMO ID 形式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

ここで、

* `AC` はディスプレイチャネルを示します。

* `{TM_AD_ID}` は、Adobe Advertisingで生成された英数字の広告キーです。 広告の一意の ID として使用され、Adobe Advertisingのエンティティメタデータを読み取り可能な [!DNL Analytics] ディメンションに変換するためのキーとして機能します。

* `{TM_PLACEMENT_ID}` は、Adobe Advertisingで生成される英数字のプレースメントキーです。 プレースメントの一意の ID として使用され、Adobe Advertisingのエンティティメタデータを読み取り可能な [!DNL Analytics] ディメンションに変換するためのキーとして機能します。

AMO ID の例：AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### 検索、ソーシャル、Commerce広告の AMO ID 形式 {#amo-id-format-search}

パラメーターは広告ネットワークによって異なりますが、次のパラメーターはすべてのユーザーに共通です。

* `AL` は検索チャネルを示します。<!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` は、広告主に割り当てられた一意のユーザー ID です。

* `{sid}` は、広告主の広告ネットワークアカウントの数値 ID に置き換えられます。*の場合は* 3[!DNL Google Ads]、*の場合は* 10[!DNL Microsoft Advertising]、*の場合は* 45[!DNL Meta]、*の場合は* 86[!DNL Yahoo! Display Network]、*の場合は* 87[!DNL Naver]、*の場合は* 88[!DNL Baidu]、*900 の場合は*[!DNL Yandex] **&#x200B; [!DNL Yahoo! Japan Ads] &#x200B;** [!DNL Yahoo Native] ** [!DNL Pinterest] 90588885 （廃止予定）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

ここで、

* `{creative}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{placement}` は、広告がクリックされた web サイトです。
* `{keywordid}` は、広告をトリガーしたキーワードの広告ネットワークの一意の数値 ID です。

##### [!DNL Google Ads]

これには、[!DNL Google Merchant Center] を使用したショッピングキャンペーンが含まれます。

* 最新の AMO ID 形式を使用するアカウント。この形式は、Performance MAX キャンペーンおよびドラフト/実験キャンペーンに関するキャンペーンレベルおよび広告グループレベルのレポートをサポートします。

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* その他すべてのアカウント：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

ここで、

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` は、クリエイティブの [!DNL Google Ads] 一の一意の数値 ID です。
* `{matchtype}` は、広告をトリガーしたキーワードのマッチタイプです（正確は `e`、フレーズは `p`、幅広は `b`）。
* `{placement}` は、広告がクリックされた web サイトのドメイン名です。 値は、プレースメントターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` は、クリックが発生したネットワークを示します。`g` 検索の場合は [!DNL Google] （キーワードターゲット広告の場合のみ）、検索パートナーの場合は `s` （キーワードターゲット広告の場合のみ）、表示ネットワークの場合は `d` （キーワードターゲット広告またはプレースメントターゲット広告の場合）。
* `{product_partition_id}` は、製品広告で使用される製品グループの広告ネットワークの一意の数値 ID です。
* `{keyword}` は、広告をトリガーした特定のキーワード（検索サイトの場合）または最も一致したキーワード（コンテンツサイトの場合）です。
* `{campaignid}` は、広告ネットワークにおけるキャンペーンの一意の数値 ID です。
* `{adgroupid}` は、広告グループの広告ネットワークの一意の数値 ID です。

>[!NOTE]
>
>* 動的検索広告の場合は、自動ターゲット {keyword} 設定されます。
>* [!DNL Google] のショッピング広告のトラッキングを生成すると、製品 ID パラメーター `{adwords_producttargetid}` がキーワードパラメーターの前に挿入されます。 製品 ID パラメーターは、[!DNL Google Ads] アカウントレベルとキャンペーンレベルのトラッキングパラメーターには表示されません。
>* 最新の AMO ID トラッキングコードを使用するには、「[ アカウントの AMO ID トラッキングコードの更新  [!DNL Google Ads]  を参照してください。](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md) <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* すべてのキャンペーンタイプ：

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

ここで、

* `{AdId}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{OrderItemId}` は、広告ネットワークのキーワードの数値 ID です。
* `{CampaignId}` は、広告ネットワークにおけるキャンペーンの一意の数値 ID です。
* `{AdGroupId}` は、広告グループの広告ネットワークの一意の数値 ID です。

>[!NOTE]
>
> [!UICONTROL Auto Upload] トラッキングオプションのないキャンペーンで、まだ新しい形式に移行されていないアカウントの場合、上記の形式を含めるように各ランディングページのサフィックスを手動で更新します。
> &#x200B;>それまでの間、次のような従来の形式も引き続き機能します。
>* 検索キャンペーン：
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* ショッピングキャンペーン（[!DNL Microsoft Merchant Center] を使用）:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* オーディエンスネットワークキャンペーン：
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

ここで、

* `{creative}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* `{matchtype}` は、広告をトリガーしたキーワードのマッチタイプです（正確は `be`、フレーズは `bp`、幅広は `bb`）。
* `{network}` は、クリックが発生したネットワーク（ネイティブの場合は `n`、検索の場合は `s`）を示します。
* `{keyword}` は、広告をトリガーしたキーワードです。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

ここで、

* `{ad_id}` は、クリエイティブの広告ネットワークの一意の数値 ID です。
* 広告 `{source_type}` 表示されたサイトのタイプです。検索の場合は *b*、コンテキスト （コンテンツ）の場合は *c*、カテゴリの場合は *ct* です。
* `{phrase_id}` は、広告ネットワークのキーワードの数値 ID です。

### AMO ID を実装する方法 {#amo-id-implement}

パラメーターは、次のいずれかの方法でトラッキング URL に追加されます。

* （推奨） サーバーサイド挿入機能を実装する場合。

   * DSPのお客様：Pixel Server は、エンドユーザーがAdobe Advertising ピクセルを使用してディスプレイ広告を表示する際に、ランディングページサフィックスに s_kwcid パラメーターを自動的に追加します。

   * 検索、ソーシャル、Commerceのお客様：

      * アカウントまたはキャンペーンに対して [!DNL Google Ads] 設定が有効な [!DNL Microsoft Advertising] および [!UICONTROL Auto Upload] アカウントの場合、エンドユーザーがAdobe Advertising ピクセルで広告をクリックすると、ピクセルサーバーは s_kwcid パラメーターをランディングページサフィックスに自動的に追加します。

      * 他の広告ネットワーク、または [!DNL Google Ads] 設定が無効の [!DNL Microsoft Advertising] および [!UICONTROL Auto Upload] アカウントの場合は、[ アカウントレベルの追加パラメーター ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} にパラメーターを手動で追加して、ベース URL に追加します。

* サーバーサイド挿入機能が実装されていない場合：

   * DSPのお客様：[JavaScript コード ](javascript.md) は、クリックスルーとビュースルーを自動的に記録します。 ブラウザーがサードパーティ cookie をサポートしていない場合でも、次の広告タイプのクリックベースのコンバージョンを追跡できます。

      * [!DNL Flashtalking] の広告タグの場合は、「[ 追加  [!DNL Analytics for Advertising]  マクロを  [!DNL Flashtalking]  広告タグに ](/help/integrations/analytics/macros-flashtalking.md)」ごとに手動で追加マクロを挿入します。 **注意：** 組織が [!DNL Flashtalking] と直接関係があり、データパスマクロを使用して `s_kwcid` および `ef_id` のトラッキングパラメーターを追跡する場合、[!DNL Flashtalking] サポートドキュメント （[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) に記載されている必要はありません。

      * [!DNL Google Campaign Manager 360] の広告タグの場合は、「[ 追加  [!DNL Analytics for Advertising]  マクロを  [!DNL Google Campaign Manager 360]  広告タグに ](/help/integrations/analytics/macros-google-campaign-manager.md)」ごとに手動で追加マクロを挿入します。

   * 検索、ソーシャル、Commerceのお客様：

      * （[!DNL Google Ads] および [!DNL Microsoft Advertising]）広告の場合、個々のアカウントコンポーネントに異なるトラッキングが必要な場合を除き、ランディングページのサフィックスに AMO ID パラメーターを手動で（理想的には [ アカウントレベル ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} 追加します。

      * その他のすべての広告ネットワークの広告の場合は、AMO ID パラメーターを [ アカウントレベルの追加パラメーター ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} に手動で追加し、ベース URL に追加します。

サーバーサイドの挿入機能を実装する、またはビジネスに最適なオプションを判断するには、Adobe アカウントチームにお問い合わせください。

### [!DNL Analytics] での AMO ID Dimension

Analytics レポートでは、[!UICONTROL AMO ID] ディメンションを検索して [!UICONTROL AMO ID Instances] 指標を使用することで、AMO ID データを見つけることができます。 [!UICONTROL AMO ID] ディメンションには、取得したすべての AMO ID 値が格納されます。[!UICONTROL AMO ID Instances] 指標は、AMO ID 値がサイトによって取得された頻度を示します。 例えば、同じ検索広告を 4 回クリックしても、Analytics で 7 つのサイトエントリをトラッキングした場合、[!UICONTROL AMO ID Instances] は 7 回、[!UICONTROL Clicks] は 4 回になります。

[!DNL Analytics] 内のレポートや監査の場合、ベストプラクティスは AMO ID を対応するインスタンスと共に使用することです。 詳しくは、「[ とAdobe Advertisingの間で予想されるデータの相違」の  [!DNL Analytics for Advertising]](data-variances.md#data-validation) のクリックスルー [!DNL Analytics] データの検証」を参照してください。

## Analytics 分類について

[!DNL Analytics] えば、[ 分類 ](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) は、アカウント、キャンペーン、広告などの特定のトラッキングコードのメタデータの一部です。 Adobe Advertisingでは、レポートの生成時に様々な方法（広告タイプ別やキャンペーン別など）でデータを表示できるように、分類を使用して生のAdobe Advertising データを分類します。 分類は、[!DNL Analytics] でのAdobe Advertising レポートの基礎となるもので、[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]、[!UICONTROL AMO Clicks] などの AMO 指標や、[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]、[!UICONTROL Revenue] などのカスタムおよび標準のオンサイトイベントで使用できます。

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [ とAdobe Advertisingの間で予想されるデ  [!DNL Analytics]  タの相違 ](data-variances.md)
