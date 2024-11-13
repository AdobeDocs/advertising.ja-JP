---
title: Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データの収集
description: Adobe Customer Journey Analyticsで今後使用するために、Adobe Analyticsで予約済み変数の履歴データを収集する方法について説明します
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データの収集

*[!DNL Analytics for Advertising] とAdobe Customer Journey Analyticsのみを使用する広告主*

予約済みの変数を使用して [!DNL Analytics for Advertising] 統合の [AMO ID および EF ID](ids.md) を取得する場合は、AMO ID および EF ID の予約変数を可能な限り早く [ 標準  [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) にコピーすることで、Adobe AdvertisingとAdobeの次世代 [!DNL analytics] ソリューションである [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) との今後の統合に備えることができます。 これにより、タスクを完了するとすぐに、AMO ID と EF ID の履歴データを収集できます。 予約済みの変数を使用していて、このタスクを完了する必要がある場合は、Adobeアカウントチームからお知らせします。

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Customer Journey Analyticsに履歴データを収集する必要があるのはなぜですか？

Customer Journey Analyticsを使用すると、Adobe Experience PlatformのデータをAdobe Analytics Analysis Workspaceに同期できます。 現在、Experience Platformへの [!DNL Analytics Data Connector] は、[!DNL Analytics] からExperience Platformに予約変数のデータを送信しません。 その結果、予約済み変数によってキャプチャされた AMO ID および EF ID のデータは、現在、Customer Journey Analytics内では使用できません。 <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertisingは、Customer Journey Analyticsを使用して将来の実装を計画しています。 実装がリリースされると、[!DNL Analytics for Advertising] 統合では、[!DNL Analytics] トラッキングを使用してクリックスルーデータと（DSP ユーザーの）ビュースルーデータを収集する必要がありますが、両方の商品がある場合は、1\） [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> と 2\）の両方のCustomer Journey Analytics<!-- (Analysis Workspace using data from Experience Platform)--> でデータを表示できるようになります。 この機能がリリースされると、Experience Platformでは、Customer Journey Analyticsで使用する AMO ID および EF ID のデータの収集を開始しますが、リリース日前の履歴データは存在しません。

ただし、簡単な [[!DNL Analytics]  処理ルール ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)<!-- [!DNL rVars] --> を作成して、すぐに AMO ID と EF ID を [!DNL eVars] にコピーすることで、AMO ID と EF ID のデータ収集を開始で <!-- [!DNL rVars] --> ます。 処理ルールを作成すると、新しいイベントを追跡するとすぐに、AMO ID と EF ID のデータが累積され始 <!-- [!DNL rVars] --> ます。 履歴データは、実装が利用可能になったら、Customer Journey Analytics内で利用できます。

>[!NOTE]
>
>処理ルールは、受信した新しいデータにのみ適用されます。 過去のデータを収集するためにさかのぼって機能することはありません。

## AMO ID および EF ID の予約変数を [!DNL eVars] にコピー

この手順は手動で行い、今後Adobe Advertisingと連携する予定の AMO ID および EF ID をトラッキングするレポートスイート <!-- [!DNL rVars] --> とに実行する必要があります。

1. 次の設定を使用して [ 処理ルールを作成 ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) します。

   * Customer Journey Analyticsで使用するために、AMO ID および EF ID <!-- [!DNL rVar] --> データをExperience Platformに移行するレポートスイートを選択します。

   * [!UICONTROL Rule Title] には、「AMO ID と EF ID を eVar にコピー」などのわかりやすい名前を使用します。

   * 「[!UICONTROL Always Execute]」セクションで、2 つのアクションを追加して新しい eVar を作成します。

      * `AMO ID` の場合：```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * `EF ID` の場合：```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * [!UICONTROL Reason for rule] については、「AMO ID および EF ID はAdobe Analytics コネクタを介して AEP に転送されます」などといった説明的なメモを使用します。

1. 保存した処理ルールを検証します。

   処理ルールを保存したら、`AMO ID` および `AMO EF ID` <!-- the existing reserved variables --> のデータは、コピー先の 2 つの新しい eVar のデータと同一になる必要があります。

   例えば、新しいeVar`eVar142` が `amo.s_kwcid(Context Data)` にマッピングされる場合、`eVar142` と `AMO ID` のデータは同一である必要があります。

処理ルールの適用方法の詳細は、「[ 処理ルールの仕組み ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about) を参照してください。

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
