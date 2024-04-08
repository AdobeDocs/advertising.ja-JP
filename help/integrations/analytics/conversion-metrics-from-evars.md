---
title: Adobe Analyticsからのコンバージョン指標の作成 [!DNL eVars] および prop
description: を使用したカスタム成功イベント指標の設定 [!DNL eVar] – および [!DNL prop]のレベルのデータ。
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: a0d5bc1791f5d05e2cbdeab58e1943f4d494b53f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Adobe Analyticsからのコンバージョン指標の作成 [!DNL eVars] および [!DNL props]

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

成功イベント指標を使用して、ブランドの目標に最適なAdobe Analytics サイトデータに基づいて、DSP パッケージと検索、ソーシャル、コマースキャンペーンを最適化できます。 既存の指標に基づいてカスタム成功イベント指標を設定できます [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) および [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) ファネルによって [!DNL eVar] – および [!DNL prop]イベントに対するレベルのデータ。 その他 [!DNL Analytics] 標準、カスタム、予約済みのコンバージョン指標やトラフィック指標を含む指標は、DSPと検索、ソーシャル、コマースで自動的に使用できます。

![使用例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用例")

次のタスクのほとんどは、で実行する必要があります。 [!DNL Analytics] 管理者またはその他のユーザー。 サポートが必要な場合は、（DSP ユーザー）DSP テクニカルサポートチーム（）にお問い合わせください。 `adcloud_support@adobe.com` または（検索、ソーシャル、コマースユーザー） Adobeアカウントチーム。

1. 対象： [!DNL Analytics], [プレースホルダー成功イベントの作成](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   以下の追加パラメーターを使用します。

   **タイプ：** `Counter`

   **極性：**  次のいずれか `Up is Good` または `Up is Bad`

   **可視性：** `Visible Everywhere`

   **ユニークイベントの録画：** `Always Record Event`

   **参加：** `Enabled`

   既に取り込まれた既存のデータが使用されるので、ブランドの web サイトに新しいイベントを実装する必要はありません。

1. での処理ルールの作成と検証 [!DNL Analytics]:

   >[!NOTE]
   >
   >のみ [!DNL Analytics] アカウント管理者は、管理者以外のユーザーに権限を付与していない限り、処理ルールを作成できます。

   1. [処理ルールの作成](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)。次の設定を使用します。

      * 満たす必要がある条件で、必須のを指定します [!DNL eVars] または [!DNL props].

        必要に応じて追加の精度レベルを設定し、最も正確なイベントを作成できます。

        >[!TIP]
        >
        >ベストプラクティスは、1 つのみを使用することです [!DNL eVar] または [!DNL prop].

      * アクションの場合は、 **イベントを設定** プレースホルダーイベントを選択します。

   1. 対象： [!DNL Analytics] [!DNL Analysis Workspace], [プロジェクトの作成](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) および新しいイベントをフリーフォームテーブルに取り込んで、にデータが確実に入力されるようにします [!DNL eVar] または [!DNL prop] 指標。

1. Adobeアカウントチームに連絡して、新しい指標をAdobe Advertisingに同期します。

指標が使用可能になったら、それを使用して目的を作成し、検索、ソーシャル、コマースのポートフォリオに割り当てたり、として使用したりできます [カスタム目標](/help/dsp/optimization/custom-goal.md) （DSP パッケージ用）。

目標の作成について詳しくは、「目標」に関する最適化ガイドの章を参照してください。この章は、Search、Social、Commerce 内から入手できます。

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Adobe Advertising内のデータ](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [広告主について追跡されたコンバージョン指標の表示](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
