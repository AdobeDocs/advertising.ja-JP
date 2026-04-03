---
title: Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集する
description: Adobe Customer Journey Analyticsで今後の使用のためにAdobe Analyticsで予約変数の履歴データを収集する方法について説明します
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
TQID: https://experienceleague.adobe.com/sOUivMvQxpfRmBYsrC3vdFC2UUxwQO0cl5BUdsQ2-u0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 607
ht-degree: 0%

---

# Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集する

*広告主、[!DNL Analytics for Advertising]およびAdobe Customer Journey Analyticsのみ*&#x200B;を使用

<!-- Solution built but not tested. Move to the CJA chapter once it's available?  If so, then create a redirect. -->

予約済み変数を使用して[統合の](ids.md)AMO IDとEF ID[!DNL Analytics for Advertising]を取得する場合は、できるだけ早くAMO IDとEF IDの予約済み変数を[標準](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-overview) [!DNL analytics]にコピーすることで、Adobe Advertisingと[Adobe Customer Journey Analytics [!DNL eVars]の間で統合するためのデータを準備できます。これはAdobeの次世代型](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) ソリューションです。 これにより、タスクを完了するとすぐに、AMO IDとEF IDの履歴データの収集が可能になります。 予約済み変数を使用しており、このタスクを完了する必要がある場合は、Adobe アカウントチームから通知されます。

<!-- 
You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation.

This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task.
-->

## Customer Journey Analyticsの履歴データを収集する必要があるのはなぜですか？

Customer Journey Analyticsでは、Adobe Experience Platformから[!DNL Workspace]にデータを同期できます。 現在、Experience Platformへの[!DNL Analytics Data Connector]は、[!DNL Analytics]からExperience Platformへの予約済み変数のデータを送信していません。 そのため、予約済み変数によってキャプチャされたAMO IDとEF IDのデータは、Customer Journey Analytics内では利用できません。<!-- Instead, XXXXXXXXXX what exactly? -->

<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertisingでは、Customer Journey Analyticsにデータを自動的に送信するソリューションを構築しています。 ソリューションがリリースされると、Adobe AdvertisingはCustomer Journey Analyticsで使用するためにAMO IDとEF IDのデータの送信を開始しますが、リリース日以前の履歴データは存在しません。

ただし、AMO IDとEF IDのデータの収集を開始するには、簡単な[[!DNL Analytics] 処理ルール &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)を作成してAMO IDとEF IDを[!DNL eVars]にコピーします。 処理ルールを作成すると、AMO IDとEF IDが新しいイベントを追跡するとすぐに、それらのIDのデータの取得が開始されます。 過去のデータは、ソリューションが利用可能になるとCustomer Journey Analytics内で利用できるようになります。

>[!NOTE]
>
>* 2025年2月28日現在、このプロセスはクリックスルーデータを追跡しますが、ビュースルーデータは追跡しません。
>* 処理ルールは、受信した新しいデータにのみ適用されます。 過去のデータを収集するために過去にさかのぼって作業することはありません。

## AMO IDとEF IDの予約済み変数を[!DNL eVars]にコピーします

この手順は手作業で、今後Adobe Advertisingと統合する予定のAMO IDとEF ID <!-- [!DNL rVars] -->を追跡する各レポートスイートで完了する必要があります。

1. [次の設定で処理ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules)を作成します。

   * AMO IDおよびEF ID <!-- [!DNL rVar] --> データをCustomer Journey Analyticsで使用するためにExperience Platformに移行するレポートスイートを選択します。

   * [!UICONTROL Rule Title]には、「AMO IDとEF IDをeVarsにコピー」など、わかりやすい名前を使用します。

   * [!UICONTROL Always Execute] セクションで、新しいeVarを作成する2つのアクションを追加します。

      * `AMO ID`について：

         1. 「**値を上書き**」を選択します。
         1. *\&lt;新しい/未使用のeVar\>*&#x200B;を選択します。
         1. **クエリ文字列パラメーター**&#x200B;を選択します。
         1. `s_kwcid`と入力します。

        例：```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * `EF ID`について：

         1. 「**値を上書き**」を選択します。
         1. *\&lt;新しい/未使用のeVar\>*&#x200B;を選択します。
         1. **クエリ文字列パラメーター**&#x200B;を選択します。
         1. `ef_id`と入力します。

        例：`Overwrite the value of rVar11 with Query String Parameter ef_id`

   * [!UICONTROL Reason for rule]には、「AMO IDとEF IDはAdobe Analytics コネクタを介してAEPに転送されます」などの説明的なメモを使用します。

1. 保存した処理ルールを検証します。

   処理ルールを保存すると、`AMO ID`と`AMO EF ID` <!-- the existing reserved variables -->のデータは、コピー先の2つの新しいeVarのデータと同じになります。

   例えば、新しいeVar `eVar142`が`amo.s_kwcid(Context Data)`にマッピングされている場合、`eVar142`と`AMO ID`のデータは同じである必要があります。

処理ルールの適用方法について詳しくは、「[処理ルールの仕組み](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)」を参照してください。

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
