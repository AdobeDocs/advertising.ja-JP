---
title: Adobe AdvertisingとAdobe Customer Journey Analytics間の統合の概要
description: Adobe AdvertisingとAdobe Customer Journey Analyticsを統合するためのオプションについて説明します。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: fabe7312fc4d1ab899bedcf9eae1c8040a4a6532
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Adobe AdvertisingとCustomer Journey Analyticsの統合の概要

<!-- title? If I change, change refs throughout -->

*Advertising DSP[!DNL Advertising Search, Social, & Commerce]* の広告主

Adobe AdvertisingはAdobe Customer Journey Analyticsと統合されており、双方向のデータ共有とレポート作成が可能です。 統合を設定するには、次の 2 つの方法があります。

* [!DNL Analytics for Advertising] とCustomer Journey Analyticsの両方を持つ広告主は、[!DNL Analytics for Advertising] を通じて持っているのと同じ機能を持っており、Customer Journey Analyticsにビジュアライゼーションが追加されています。

  引き続き、Adobe Experience Platform Web SDK（`alloy.js`）またはAdobe Experience Cloud ID サービス（`visitorAPI.js`）を使用してクリックスルーイベントをトラッキングします。 Advertising DSPを使用する広告主は、引き続きJavaScript スニペットを使用してビュースルーイベントをトラッキングします。 Customer Journey Analyticsで使用できるデータは次のとおりです。

   * Customer Journey AnalyticsのAdobe Advertisingからの Campaign パフォーマンスデータ

   * Customer Journey Analyticsで [!DNL Google Ads] と [!DNL Microsoft Advertising] が追跡したサイトアクティビティとコンバージョン（毎日更新）

   * Adobe Advertisingの [!DNL Analytics] のアトリビューションデータ。最適化とレポートに使用できます。

  このユースケースでは、オプションで [Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データを収集 &#x200B;](/help/integrations/analytics/rvars-to-evars.md) を使用する必要があります。

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* （今後リリース予定のベータ版機能）Customer Journey Analyticsを使用してい [!DNL Analytics for Advertising] 広告主は、[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja) を使用して、Adobe AdvertisingとCustomer Journey Analyticsの間でデータをネイティブに交換できます。 Cookie、ハッシュ化された IP、ユニバーサル ID （[!DNL LiveRamp RampIDs] および ID5 ID）を使用してサイトイベントを追跡し、サイトイベントを有料メディアアクティビティに関連付けることができます。 次のデータは、キャンペーン、広告グループ、パッケージ、プレースメント、キーワードの各レベルで利用できます。

   * Customer Journey AnalyticsのAdobe Advertisingからの Campaign パフォーマンスデータ

     **メモ：** [!DNL Apple] および [!DNL Tiktok] のデータは使用できません。

   * Customer Journey Analyticsで [!DNL Google Ads] と [!DNL Microsoft Advertising] が追跡するサイトアクティビティとコンバージョン

   * 最適化やレポートに使用できる、Adobe AdvertisingのCustomer Journey Analyticsのアトリビューションデータ

  この使用例では、Web SDKを使用してサイトイベントを追跡し（Cookie、ハッシュ化された IP アドレス、ユニバーサル ID を使用）、サイトイベントを [!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Meta] およびAdobe DSPの有料メディアアクティビティに関連付けます。 また、データ収集にもAdobe Experience Platformを使用します。

## Adobe AdvertisingとCustomer Journey Analytics間のネイティブ統合を開始する方法

Adobe アカウントチームに連絡してください。アカウントチームは、開始するために必要な初期設定を行い、組織のニーズに基づいて実装とデータ使用の計画を立てるのに役立ちます。

>[!MORELIKETHIS]
>
>* [&#x200B; 前提条件 &#x200B;](prerequisites.md)
>* [&#x200B; 使用するAdobe Advertising ID [!DNL Customer Journey Analytics]](ids.md)
>* [&#x200B; データ収集、データ転送、レポートの設定 &#x200B;](set-up.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標およびディメンション &#x200B;](advertising-data-in-cja.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データを収集します &#x200B;](/help/integrations/analytics/rvars-to-evars.md)。
