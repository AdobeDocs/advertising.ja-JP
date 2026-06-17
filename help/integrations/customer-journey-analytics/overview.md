---
title: Adobe AdvertisingとAdobe Customer Journey Analyticsの連携の概要
description: Adobe AdvertisingとAdobe Customer Journey Analyticsを統合するオプションについて説明します。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
TQID: https://experienceleague.adobe.com/nxn5AcKCc-xm-k5LXOcKIquNKyoXbt3soR5nhQR0w-E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a93c33ee47bd1a8df137a69598b367e985def4ee
workflow-type: tm+mt
source-wordcount: 499
ht-degree: 0%

---

# Adobe AdvertisingとCustomer Journey Analyticsの連携の概要

<!-- title? If I change, change refs throughout -->

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*&#x200B;の広告主

Adobe Advertisingは、Adobe Customer Journey Analyticsと統合されているため、双方向のデータ共有とレポート作成が可能です。 統合を設定するには、次の2つのオプションがあります。

* [!DNL Analytics for Advertising]とCustomer Journey Analyticsの両方を持つ広告主は、[!DNL Analytics for Advertising]を通じて持つ機能と同じ機能を持ち、Customer Journey Analyticsにビジュアライゼーションが追加されています。

  Adobe Experience Platform Web SDK （`alloy.js`）またはAdobe Experience Cloud Identity Service （`visitorAPI.js`）を使用して、クリックスルーを追跡できます。 Advertising DSPを導入している広告主は、引き続きJavaScriptスニペットを使用してビュースルーイベントを追跡します。 Customer Journey Analyticsでは、次のデータを利用できます。

   * Customer Journey AnalyticsのAdobe Advertisingからのキャンペーンパフォーマンスデータ

   * Customer Journey Analyticsの[!DNL Google Ads]および[!DNL Microsoft Advertising]によって追跡されたサイトアクティビティとコンバージョンが、毎日更新されます

   * Adobe Advertisingの[!DNL Analytics]からのアトリビューションデータ。最適化とレポートに使用できます

  この使用例では、Customer Journey Analytics[&#128279;](/help/integrations/analytics/rvars-to-evars.md)で使用するAMO IDとEF IDの履歴データをオプションで収集する必要があります。

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* [!DNL Analytics for Advertising]ではなく[Customer Journey Analyticsを使用している広告主は、Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja)を使用して、Adobe AdvertisingとCustomer Journey Analytics間でデータをネイティブに交換できます。 Cookie、ハッシュ化されたIP、ユニバーサル ID （[!DNL LiveRamp RampIDs]およびID5 ID）を使用してサイトイベントを追跡し、サイトイベントを有料メディアのアクティビティに関連付けることができます。 キャンペーン、広告グループ、パッケージ、プレースメント、キーワードの各レベルで、次のデータを利用できます。

   * Customer Journey AnalyticsのAdobe Advertisingからのキャンペーンパフォーマンスデータ

     **注：** [!DNL Apple]および[!DNL Tiktok]のデータは利用できません。

   * Customer Journey Analyticsで[!DNL Google Ads]および[!DNL Microsoft Advertising]によって追跡されたサイトアクティビティとコンバージョン

   * Adobe AdvertisingのCustomer Journey Analyticsからのアトリビューションデータ。最適化やレポートに使用できます

  このユースケースでは、Web SDKを使用して、サイトイベント（Cookie、ハッシュ化されたIP アドレス、ユニバーサル IDを使用）を追跡し、サイトイベントを[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Meta]およびAdobe DSPの有料メディアアクティビティに関連付けます。 また、データ収集にもAdobe Experience Platformを使用します。

## レポートデータタイプの定義

* **イベントレベルのデータ：** セッション、ページビュー、リードフォーム送信、アプリケーション送信などのタイムスタンプ付きイベント。

* **概要データ：**&#x200B;広告プラットフォーム、キャンペーン、配置、インプレッション、クリック、コストなどの集計レポートデータ。

* **分類/ディメンション データ：** レポート ディメンション（Adobe Advertising キャンペーン名、ポートフォリオ名、プレースメント IDなど）。 イベントレベルのデータと概要データを分類やディメンション別に検索（フィルター）できます。

## Adobe AdvertisingとCustomer Journey Analyticsのネイティブ統合を開始する方法 {#integration-cja-initiate}

Adobeのアカウントチームにお問い合わせください。最初に必要な設定を行い、組織のニーズに基づいて導入とデータ利用を計画するのに役立ちます。

>[!MORELIKETHIS]
>
>* [前提条件](prerequisites.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)様が使用しているAdobe Advertising ID
>* [&#x200B; データ収集、データ転送、レポートの設定](set-up.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション &#x200B;](advertising-data-in-cja.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集](/help/integrations/analytics/rvars-to-evars.md)。
>* [&#x200B; トラブルシューティング &#x200B;](troubleshooting.md)
