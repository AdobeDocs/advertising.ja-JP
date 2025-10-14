---
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID は、一意の各広告の組み合わせを細かいレベルで追跡し、[!DNL Analytics] とCustomer Journey Analyticsのデータ分類や、Adobe Advertisingからの広告指標（インプレッション数、クリック数、コストなど）の取り込みに使用されます。

[!DNL Analytics]:AMO ID は、[eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=ja) または rVar ディメンション（AMO ID）に保存されます。

Customer Journey Analyticsの場合、AMO ID は、`trackingCode` `conversionDetails` の一部である [&#x200B; オブジェクトの [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] プロパティに保存さ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) ます。

AMO ID は `s_kwcid` とも呼ばれ、「[!DNL squid]」と発音されることがあります。

### AMO ID 形式 {#amo-id-formats}

#### [!DNL DSP] の AMO ID 形式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

ここで、

* `AC` はディスプレイチャネルを示します。

* `{TM_AD_ID}` は、Adobe Advertisingで生成された英数字の広告キーです。 広告の一意の ID として使用され、Adobe Advertising エンティティメタデータを読み取り可能な [!DNL Analytics] およびCustomer Journey Analytics ディメンションに変換するためのキーとして機能します。

* `{TM_PLACEMENT_ID}` は、Adobe Advertisingで生成される英数字のプレースメントキーです。 プレースメントの一意の ID として使用され、Adobe Advertising エンティティメタデータを読み取り可能な [!DNL Analytics] およびCustomer Journey Analytics ディメンションに変換するためのキーとして機能します。

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
>* 最新の AMO ID トラッキングコードを使用するには、「[&#x200B; アカウントの AMO ID トラッキングコードの更新  [!DNL Google Ads]  を参照してください。](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md) <!-- Update terminology there too. -->

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
