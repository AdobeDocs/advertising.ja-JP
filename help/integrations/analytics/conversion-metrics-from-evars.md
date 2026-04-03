---
title: Adobe Analytics [!DNL eVars] およびpropからコンバージョン指標を作成します
description: ' [!DNL eVar] レベルおよび [!DNL prop] レベルのデータを使用して、カスタム成功イベント指標を設定します。'
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
TQID: https://experienceleague.adobe.com/DRwNcYJ4-tv6CWhaIHc-qZ-xNsM8sSqoSNkG8AaYI2c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# Adobe Analytics [!DNL eVars]および[!DNL props]からコンバージョン指標を作成

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

サクセスイベント指標を使用すると、ブランドの目標に最適なAdobe Analytics サイトデータに基づいて、DSP パッケージとSearch, Social, &amp; Commerce キャンペーンを最適化できます。 [[!DNL Analytics] [!DNL eVars] レベルおよび](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) レベルのデータをイベントにファネリングすることで、既存の[[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html)および[!DNL eVar]&#x200B;[!DNL prop]に基づいてカスタム成功イベント指標を設定できます。 標準、カスタム、予約済みのコンバージョン指標およびトラフィック指標を含むその他の[!DNL Analytics]指標は、DSPおよびSearch, Social, &amp; Commerceで自動的に利用できます。

![使用例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用例")

次のタスクのほとんどは、[!DNL Analytics]管理者または他のユーザーが実行する必要があります。 サポートが必要な場合は、Adobe アカウントチームにお問い合わせください。

1. [!DNL Analytics]で、[&#x200B; プレースホルダー成功イベントを作成](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event)します。

   次の追加パラメーターを使用します。

   **種類：** `Counter`

   **極性：** （`Up is Good`または`Up is Bad`）

   **表示：** `Visible Everywhere`

   **ユニーク イベント記録：** `Always Record Event`

   **参加：** `Enabled`

   既に取得された既存のデータを使用するため、新しいイベントをweb サイトに実装する必要はありません。

1. [!DNL Analytics]で処理ルールを作成して検証します。

   >[!NOTE]
   >
   >管理者以外のユーザーに権限を付与していない限り、[!DNL Analytics]人のアカウント管理者のみが処理ルールを作成できます。

   1. [次の設定を使用して、処理ルール &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)を作成します。

      * 条件を満たす必要がある場合は、必須の[!DNL eVars]または[!DNL props]を指定します。

        必要に応じてさらに詳細レベルを設定することで、最も正確なイベントを作成できます。

        >[!TIP]
        >
        >ベストプラクティスは、[!DNL eVar]または[!DNL prop]を1つだけ使用することです。

      * アクションの場合は、**イベントを設定**&#x200B;を選択し、プレースホルダーイベントを選択します。

   1. [!DNL Analytics] [!DNL Analysis Workspace]で、[&#x200B; プロジェクト &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html)を作成し、新しいイベントをフリーフォームテーブルに取り込んで、[!DNL eVar]または[!DNL prop]指標にデータが入力されていることを確認します。

1. 新しい指標をAdobe Advertisingに同期するには、Adobe アカウントチームにお問い合わせください。

この指標を使用して目的を作成し、Search, Social, &amp; Commerce ポートフォリオに割り当てるか、DSP パッケージの[&#x200B; カスタム目標](/help/dsp/optimization/custom-goal.md)として使用できます。

目的の作成について詳しくは、Search, Social, &amp; Commerce内から入手できる「目的」に関する最適化ガイドの章を参照してください

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Adobe Advertisingのデータ &#x200B;](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [広告主に対して追跡されたコンバージョン指標を表示](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
