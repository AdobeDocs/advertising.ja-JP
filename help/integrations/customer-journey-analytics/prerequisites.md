---
title: Adobe AdvertisingとCustomer Journey Analyticsの統合の前提条件
description: Adobe AdvertisingとCustomer Journey Analyticsの統合の前提条件
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: 194675147b64af37de6373116f246f1e61388a23
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Adobe AdvertisingとCustomer Journey Analyticsの統合の前提条件

*Advertising DSP[!DNL Advertising Search, Social, & Commerce]* の広告主

* [!DNL Analytics for Advertising] とCustomer Journey Analyticsの両方を持つ広告主：

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [ その他すべての前提条件  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)。

* Customer Journey Analyticsを持つが [!DNL Analytics for Advertising] を持たない広告主：

   * Adobe Experience Platform Web SDK ライブラリ：`alloy.js`

     Web SDKとAdobe Advertising広告主アカウントで使用する [!DNL Org ID] は同じである必要があります。 この ID は、Adobe Experience Cloud Debugger の [ 概要」タブ ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=ja) にあります。

     ![Experience Cloud Debugger の概要画面 ](/help/integrations/assets/a4adc-debugger-summary.png)

     Experience Platform データストリームおよび XDM スキーマを作成するには、Experience Platform サイト管理者のサポートが必要です。

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     データセットへの接続を設定し、レポートを設定するには、社内の Web アナリストによるサポートが必要です。

>[!TIP]
>
>データの忠実性を向上させるには、各ライブラリの最新バージョンを使用します。

>[!MORELIKETHIS]
>
>* [ 概要 ](overview.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データを収集します ](/help/integrations/analytics/rvars-to-evars.md)。
