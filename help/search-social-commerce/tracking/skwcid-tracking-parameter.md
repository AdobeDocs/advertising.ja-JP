---
title: AMO ID(s_kwcid) トラッキングパラメーター
description: Adobe AnalyticsとAdobe Advertisingデータを共有するために使用されるトラッキングパラメーターについて説明します。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 47cb00bc456601ef943c37de14a2047220f756f1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# AMO ID(s_kwcid) トラッキングパラメーター

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertisingは、AMO ID 追加パラメーター ( `s_kwcid` パラメーター。広告チャネルと広告ネットワーク固有の要素で構成されます。

<!-- add everything below to IDs page -->

パラメーターは、次のいずれかの方法でトラッキング URL に追加されます。

* （推奨）サーバー側挿入機能が実装されています。

  の場合 [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントの [!UICONTROL Auto Upload] アカウントまたはキャンペーンに対してを有効にすると、エンドユーザーが広告をクリックすると、ピクセルサーバーによって AMO ID パラメーターがランディングページのサフィックスに自動的に追加されます <!-- click a search ad or views a display ad --> をAdobe Advertisingピクセル

  他の広告ネットワークの場合、または [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントの [!UICONTROL Auto Upload] 設定を無効にした場合、AMO ID パラメーターをアカウントレベルの追加パラメーターに手動で追加し、ベース URL に追加します。

* <!-- (Search, Social, & Commerce only) -->サーバー側挿入機能が実装されていないので、AMO ID パラメーターを ([!DNL Google Ads] および [!DNL Microsoft Advertising]) ランディングページのサフィックスや（その他の広告ネットワーク）アカウントレベルの追加パラメーターを追加できます。

サーバー側挿入機能を実装する場合や、ビジネスに最適なオプションを決定する場合は、Adobeアカウントチームにお問い合わせください。

## Advertising DSP広告用の AMO ID フォーマット

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

場所：

* `AC` ディスプレイチャネルを示します。

* `{TM_AD_ID}` は英数字の広告キーです。

* `{TM_PLACEMENT_ID}` は、英数字の配置キーです。

## 検索、ソーシャル、コマース広告の AMO ID 形式

パラメーターは広告ネットワークによって異なりますが、次のパラメーターはすべてに共通です。

* `AL` は、検索チャネルを示します。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` は、広告主に割り当てられる一意のユーザー ID です。

* `{sid}` は、広告主の広告ネットワークアカウントの数値 ID に置き換えられます。 *3* 対象： [!DNL Google Ads], *10* 対象： [!DNL Microsoft Advertising], *45* 対象： [!DNL Meta], *86* 対象： [!DNL Yahoo! Display Network], *87* 対象： [!DNL Naver], *88* 対象： [!DNL Baidu], *90* 対象： [!DNL Yandex], *94* 対象： [!DNL Yahoo! Japan Ads], *105* 対象： [!DNL Yahoo Native] （非推奨）、または *106* 対象： [!DNL Pinterest] （非推奨）。

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

これには、 [!DNL Google Merchant Center].

* 最新の AMO ID 形式を使用するアカウント。パフォーマンスの最大キャンペーンとドラフト&amp;実験キャンペーンのキャンペーンレベルおよび広告グループレベルのレポートをサポートします。

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* その他すべてのアカウント：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* 動的検索広告の場合、 {keyword} が自動ターゲットに設定されている。
>* のトラッキングを生成する際 [!DNL Google] 買い物広告、製品 ID パラメーター `{adwords_producttargetid}`の前に、が挿入されます。 製品 ID パラメーターが [!DNL Google Ads] アカウントレベルおよびキャンペーンレベルのトラッキングパラメーター。
>* 最新の AMO ID トラッキングコードを使用するには、[の AMO ID トラッキングコードを更新します。 [!DNL Google Ads] アカウント](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* キャンペーンの検索：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 買い物キャンペーン ( [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* オーディエンスネットワークキャンペーン：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [広告ネットワークアカウントの管理](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Baidu キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising キャンペーンの設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Japan Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
