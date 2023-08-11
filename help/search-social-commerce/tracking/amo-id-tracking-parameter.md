---
title: AMO ID(s_kwcid) トラッキングパラメーター
description: Adobe AnalyticsとAdobe Advertisingデータを共有するために使用されるトラッキングパラメーターについて説明します。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
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

DSPおよび検索、Social、およびコマースの AMO ID の形式については、[Adobe AdvertisingID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe AdvertisingID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [広告ネットワークアカウントの管理](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Baidu キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising キャンペーンの設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Japan Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
