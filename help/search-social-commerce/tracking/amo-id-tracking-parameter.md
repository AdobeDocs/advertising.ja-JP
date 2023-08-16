---
title: AMO ID(s_kwcid) トラッキングパラメーター
description: Adobe AnalyticsとAdobe Advertisingデータを共有するために使用されるトラッキングパラメーターについて説明します。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# AMO ID(s_kwcid) トラッキングパラメーター

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertisingは、AMO ID 追加パラメーター ( `s_kwcid` パラメーター。広告チャネルと広告ネットワーク固有の要素で構成されます。

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

DSPおよび検索、Social、およびコマースの AMO ID の形式については、[Adobe AdvertisingID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe AdvertisingID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* （検索、ソーシャル、コマース） [広告ネットワークアカウントの管理](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* （検索、ソーシャル、コマース） [Baidu キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* （検索、ソーシャル、コマース） [Google Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* （検索、ソーシャル、コマース） [Microsoft® Advertising campaign の設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* （検索、ソーシャル、コマース） [Yahoo! Japan Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* （検索、ソーシャル、コマース） [Yandex キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
