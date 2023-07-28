---
title: s_kwcid トラッキングパラメーター
description: Adobe AnalyticsとAdobe Advertisingデータを共有するために使用されるトラッキングパラメーターについて説明します。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# s_kwcid トラッキングパラメーター

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

<!-- Where should this go? It probably belongs in the Analytics integration chapter, but I'll need to fit it in/create context around it/explain more about implementation and how this works.  SPECIFICALLY, I'll need to update the second section that explains when/where to add the code for DSP clients. -->

Adobe Advertisingは、 `s_kwcid` ad channel および ad ネットワーク固有の要素で構成される append パラメーター。 パラメーターは、次のいずれかの方法でトラッキング URL に追加されます。

* （推奨）<!--; the only option for Advertising DSP-->) サーバー側 s_kwcid 機能が実装されている。

  の場合 [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントの [!UICONTROL Auto Upload] アカウントまたはキャンペーンに対して有効に設定を指定すると、エンドユーザーが広告をクリックすると、ピクセルサーバーによってランディングページのサフィックスに s_kwcid パラメーターが自動的に追加されます <!-- click a search ad or views a display ad --> をAdobe Advertisingピクセル

  他の広告ネットワークの場合、または [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントの [!UICONTROL Auto Upload] を無効に設定した場合、アカウントレベルの追加パラメーターに手動でパラメーターを追加して、ベース URL に追加します。

* <!-- (Search, Social, & Commerce only) -->サーバー側の s_kwcid 機能が実装されていないので、s_kwcid パラメーターを ([!DNL Google Ads] および [!DNL Microsoft Advertising]) ランディングページのサフィックスや（その他の広告ネットワーク）アカウントレベルの追加パラメーターを追加できます。

サーバー側 s_kwcid 機能を実装する場合や、ビジネスに最適なオプションを決定する場合は、Adobeアカウントチームにお問い合わせください。

## Advertising DSP広告用の s_kwcid 形式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

場所：

* `AC` ディスプレイチャネルを示します。

* `{TM_AD_ID}` は英数字の広告キーです。

* `{TM_PLACEMENT_ID}` は、英数字の配置キーです。

## 検索、ソーシャル、コマースの広告の s_kwcid 形式

パラメーターは広告ネットワークによって異なりますが、次のパラメーターはすべてに共通です。

* `AL` は、検索チャネルを示します。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` は、広告主に割り当てられる一意のユーザー ID です。

* `{sid}` は、広告主の広告ネットワークアカウントの数値 ID に置き換えられます。 *3* 対象： [!DNL Google Ads], *10* 対象： [!DNL Microsoft Advertising], *45* 対象： [!DNL Meta], *86* 対象： [!DNL Yahoo! Display Network], *87* 対象： [!DNL Naver], *88* 対象： [!DNL Baidu], *90* 対象： [!DNL Yandex], *94* 対象： [!DNL Yahoo! Japan Ads], *105* 対象： [!DNL Yahoo Native] （非推奨）、または *106* 対象： [!DNL Pinterest] （非推奨）。

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

これには、 [!DNL Google Merchant Center].

* 最新の s_kwcid 形式を使用するアカウント。パフォーマンスの最大キャンペーンおよびドラフトと実験キャンペーンのキャンペーンおよび広告グループレベルのレポートをサポートします。

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* その他すべてのアカウント：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* 動的検索広告の場合、 {keyword} が自動ターゲットに設定されている。
>* のトラッキングを生成する際 [!DNL Google] 買い物広告、製品 ID パラメーター `{adwords_producttargetid}`の前に、が挿入されます。 製品 ID パラメーターが [!DNL Google Ads] アカウントレベルおよびキャンペーンレベルのトラッキングパラメーター。
>* 最新の s_kwcid トラッキングコードを使用するには、[の s_kwcid トラッキングコードを更新します。 [!DNL Google Ads] アカウント](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;

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
