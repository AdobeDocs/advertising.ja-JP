---
title: Adobe Analyticsおよび prop からのコンバージョン指標  [!DNL eVars]  作成
description: ' [!DNL eVar] レベルおよび  [!DNL prop] レベルのデータを使用して、カスタム成功イベント指標を設定します。'
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: be78460b42e1d9622cb781a0a32b01a34464a76d
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Adobe Analytics [!DNL eVars] および [!DNL props] からのコンバージョン指標の作成

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

成功イベント指標を使用して、ブランドの目標に最適なAdobe Analytics サイトデータに基づいて、DSP パッケージや検索、ソーシャル、Commerce キャンペーンを最適化できます。 [[!DNL Analytics] [!DNL eVars] レベルおよび ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) レベルのデータをイベントにファネルすることで、既存の [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) ールおよび [!DNL eVar][!DNL prop] ークフローに基づいてカスタム成功イベント指標を設定できます。 標準、カスタム、予約済みのコンバージョン指標やトラフィック指標など、その他の [!DNL Analytics] ース指標は、DSPや、検索、ソーシャル、Commerceで自動的に使用できます。

![ 使用例 ](/help/integrations/assets/a4adc-conversion-evar-example.jpg " 使用例 ")

次のタスクのほとんどは、[!DNL Analytics] 管理者または他のユーザーが実行する必要があります。 サポートが必要な場合は、Adobe アカウントチームにお問い合わせください。

1. [!DNL Analytics] では、[ プレースホルダー成功イベントを作成 ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event) します。

   以下の追加パラメーターを使用します。

   **タイプ：** `Counter`

   **極性：** `Up is Good` または `Up is Bad`

   **表示：** `Visible Everywhere`

   **一意のイベントの記録：** `Always Record Event`

   **参加：** `Enabled`

   既に取り込まれた既存のデータが使用されるので、ブランドの web サイトに新しいイベントを実装する必要はありません。

1. [!DNL Analytics] で処理ルールを作成して検証します。

   >[!NOTE]
   >
   >管理者以外のユーザーに権限を付与していない限り、処理ルールを作成できるのは [!DNL Analytics] アカウント管理者のみです。

   1. 次の設定を使用して、[ 処理ルールを作成 ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en) します。

      * 満たす必要がある条件の場合、必要な [!DNL eVars] または [!DNL props] を指定します。

        必要に応じて追加の精度レベルを設定し、最も正確なイベントを作成できます。

        >[!TIP]
        >
        >ベストプラクティスは、1 つの [!DNL eVar] または [!DNL prop] のみを使用することです。

      * アクションの場合は、「**イベントを設定**」を選択し、プレースホルダーイベントを選択します。

   1. [!DNL Analytics] [!DNL Analysis Workspace] では、[ プロジェクトを作成 ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) して新しいイベントをフリーフォームテーブルに取り込み、[!DNL eVar] または [!DNL prop] の指標にデータが入力されていることを確認します。

1. 新しい指標をAdobeに同期する場合は、Adobe Advertising アカウントチームにお問い合わせください。

指標が使用可能になったら、それを使用して目的を作成し、検索、ソーシャル、Commerceのポートフォリオに割り当てたり、DSP パッケージの [ カスタム目標 ](/help/dsp/optimization/custom-goal.md) として使用したりできます。

目標の作成について詳しくは、「目標」に関する最適化ガイドの章を参照してください。この章は、検索、ソーシャル、Commerce内から利用できます

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Adobe Advertisingのデータ ](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [ 広告主について追跡されたコンバージョン指標の表示 ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
