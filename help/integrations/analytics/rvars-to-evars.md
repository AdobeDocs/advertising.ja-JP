---
title: Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データの収集
description: Adobe Customer Journey Analyticsで今後使用するために、Adobe Analyticsで予約済み変数の履歴データを収集する方法について説明します
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: 5b78ec0fc4c5ea4742cbb080b992bdb323fc9af3
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データの収集

*[!DNL Analytics for Advertising] とAdobe Customer Journey Analyticsのみを使用する広告主*

予約済みの変数を使用して [!DNL Analytics for Advertising] 統合の [AMO ID および EF ID](ids.md) を取得する場合は、できるだけ早く、AMO ID および EF ID の予約変数を [ 標準  [!DNL eVars]](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/evar) にコピーすることで、Adobe AdvertisingとAdobeの次世代 [!DNL analytics] ソリューションである [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-overview) との間の将来の統合に備えることができます。 これにより、タスクを完了するとすぐに、AMO ID と EF ID の履歴データを収集できます。 予約変数を使用していて、このタスクを実行する必要がある場合は、Adobe アカウントチームからお知らせします。

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Customer Journey Analyticsの履歴データを収集する必要があるのはなぜですか？

Customer Journey Analyticsを使用すると、Adobe Experience PlatformのデータをAdobe Analytics Analysis Workspaceに同期できます。 現在、Experience Platformへの [!DNL Analytics Data Connector] は、[!DNL Analytics] からExperience Platformに予約変数のデータを送信しません。 その結果、予約済み変数によってキャプチャされた AMO ID および EF ID のデータは、現在、Customer Journey Analytics内では使用できません。 <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe AdvertisingはCustomer Journey Analyticsとの将来の実装を計画しています。 実装がリリースされると、[!DNL Analytics for Advertising] の統合では、引き続き [!DNL Analytics] トラッキングを使用してクリックスルーデータを収集する必要がありますが <!-- Add back if we implement this:  and (DSP users) view-through data --> 組織に両方の製品がある場合は、1\） [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> および 2\）の両方でデータをCustomer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> 表示できるようになります。 この機能がリリースされると、Experience Platformでは、Customer Journey Analyticsで使用する AMO ID および EF ID のデータの収集を開始します。ただし、リリース日前の履歴データは存在しません。

ただし、簡単な [[!DNL Analytics]  処理ルール ](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)<!-- [!DNL rVars] --> を作成して、すぐに AMO ID と EF ID を [!DNL eVars] にコピーすることで、AMO ID と EF ID のデータ収集を開始で <!-- [!DNL rVars] --> ます。 処理ルールを作成すると、新しいイベントを追跡するとすぐに、AMO ID と EF ID のデータが累積され始 <!-- [!DNL rVars] --> ます。 履歴データは、実装が使用可能になると、Customer Journey Analytics内で使用できるようになります。

>[!NOTE]
>
>* 2025 年 2 月 28 日（PT）現在、このプロセスは、クリックスルーデータを追跡しますが、ビュースルーデータは追跡しません。
>* 処理ルールは、受信した新しいデータにのみ適用されます。 過去のデータを収集するためにさかのぼって機能することはありません。

## AMO ID および EF ID の予約変数を [!DNL eVars] にコピー

この手順は手動で行い、今後Adobe Advertisingと統合する予定の AMO ID および EF ID をトラッキングするレポートスイート <!-- [!DNL rVars] --> とに実行する必要があります。

1. 次の設定を使用して [ 処理ルールを作成 ](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) します。

   * Customer Journey Analyticsで使用するために、AMO ID および EF ID <!-- [!DNL rVar] --> データをExperience Platformに移行するレポートスイートを選択します。

   * [!UICONTROL Rule Title] には、「AMO ID と EF ID を eVar にコピー」などのわかりやすい名前を使用します。

   * 「[!UICONTROL Always Execute]」セクションで、2 つのアクションを追加して新しい eVar を作成します。

      * `AMO ID` の場合：

         1. 「**の値を上書き**」を選択します。
         1. *\&lt; 新規/未使用のeVar\>* を選択します。
         1. **クエリ文字列パラメーター** を選択します。
         1. `s_kwcid` と入力します。

        例：```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * `EF ID` の場合：

         1. 「**の値を上書き**」を選択します。
         1. *\&lt; 新規/未使用のeVar\>* を選択します。
         1. **クエリ文字列パラメーター** を選択します。
         1. `ef_id` と入力します。

        例：`Overwrite the value of rVar11 with Query String Parameter ef_id`

   * [!UICONTROL Reason for rule] の場合は、「AMO ID および EF ID はAdobe Analytics コネクタを介してAEPに転送されます」など、説明的なメモを使用します。

1. 保存した処理ルールを検証します。

   処理ルールを保存したら、`AMO ID` および `AMO EF ID` <!-- the existing reserved variables --> のデータは、コピー先の 2 つの新しい eVar のデータと同一になる必要があります。

   例えば、新しいeVar `eVar142` が `amo.s_kwcid(Context Data)` にマッピングされる場合、`eVar142` と `AMO ID` のデータは同一である必要があります。

処理ルールの適用方法の詳細は、「[ 処理ルールの仕組み ](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about) を参照してください。

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
