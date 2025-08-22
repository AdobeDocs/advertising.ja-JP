---
title: Adobe AdvertisingとAdobe Customer Journey Analytics間の統合の概要
description: Adobe AdvertisingとAdobe Customer Journey Analyticsを統合するためのオプションについて説明します。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: ed3c3b4331b743d0c40f04fb8543c535d80ca1d5
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe AdvertisingとCustomer Journey Analyticsの統合の概要

<!-- title? If I change, change refs throughout -->

*Advertising DSP[!DNL Advertising Search, Social, & Commerce]* の広告主

Adobe AdvertisingはAdobe Customer Journey Analyticsと統合されており、双方向のデータ共有が可能です。 統合を設定するには、次の 2 つの方法があります。

* [!DNL Analytics for Advertising] とCustomer Journey Analyticsの両方を持つ広告主は、[!DNL Analytics for Advertising] を通じて持っているのと同じ機能を持っており、Customer Journey Analyticsにビジュアライゼーションが追加されています。

  引き続き、Adobe Experience Platform Web SDK（`alloy.js`）またはAdobe Experience Cloud ID サービス（`visitorAPI.js`）を使用してクリックスルーイベントをトラッキングします。 Advertising DSPを使用する広告主は、引き続きJavaScript スニペットを使用してビュースルーイベントをトラッキングします。 Customer Journey Analyticsで使用できるデータは次のとおりです。

   * Adobe Advertisingからの Campaign パフォーマンスデータ

     **メモ：** [!DNL Apple] および [!DNL Tiktok] のデータは使用できません。

   * [!DNL Google Ads]、[!DNL Microsoft Advertising] および [!DNL Meta] で追跡されるサイトアクティビティとコンバージョン

   * [!DNL Analytics] のアトリビューションデータ（Adobe Advertisingでの最適化とレポートに使用できます）

  このユースケースでは、オプションで [Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データを収集 ](/help/integrations/analytics/rvars-to-evars.md) する以外に、追加の手順を実行する必要はありません。

* （今後リリース予定のベータ版機能）Customer Journey Analyticsを使用してい [!DNL Analytics for Advertising] 広告主は、Adobe Experience Platform web SDK（`alloy.js`）を使用してクリックスルーおよびビュースルーイベントをトラッキングすることにより、Adobe AdvertisingとCustomer Journey Analyticsの間で次のデータをネイティブに交換できます。 データは、キャンペーンレベル、広告グループレベル、パッケージレベル、プレースメント レベル、キーワードレベルで使用できます。

   * Adobe Advertisingからの Campaign パフォーマンスデータ

     **メモ：** [!DNL Apple] および [!DNL Tiktok] のデータは使用できません。

   * [!DNL Google Ads]、[!DNL Microsoft Advertising] および [!DNL Meta] で追跡されるサイトアクティビティとコンバージョン

   * Customer Journey Analyticsのアトリビューションデータ（Adobe Advertisingでの最適化とレポートに使用できます）

  **メモ：** まだオーガニックデータはありません。<!-- Does that belong somewhere up above? -->

  この使用例では、Web SDKを使用してサイトイベントを追跡し（Cookie、ハッシュ化された IP アドレス、ユニバーサル ID を使用）、サイトイベントを [!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Meta] およびAdobe DSPの有料メディアアクティビティに関連付けます。 また、データ収集にもAdobe Experience Platformを使用します。

## Adobe AdvertisingとCustomer Journey Analytics間のネイティブ統合を開始する方法

Adobe アカウントチームに連絡してください。アカウントチームは、開始するために必要な初期設定を行い、組織のニーズに基づいて実装とデータ使用の計画を立てるのに役立ちます。

>[!MORELIKETHIS]
>
>* [ 前提条件 ](prerequisites.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データを収集します ](/help/integrations/analytics/rvars-to-evars.md)。
