---
title: 「Adobe Analyticsからのコンバージョン指標の作成 [!DNL eVars] および props
description: 「次を使用してカスタム成功イベント指標を設定 [!DNL eVar] — および [!DNL prop] — レベルのデータ。」
feature: Integration with Adobe Analytics, Conversions
source-git-commit: 71ffd021b31154a2ed2a522049f656a13d364d00
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Adobe Analyticsでのコンバージョン指標の作成 [!DNL eVars] および [!DNL props]

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

成功イベント指標を使用すると、DSPの目標に最も適したAdobe Analyticsサイトデータに基づいて、Search、Social、および Commerce のパッケージとキャンペーンを最適化できます。 既存の [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) および [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) 集めることで [!DNL eVar] — および [!DNL prop]-level データをイベントに追加します。 その他 [!DNL Analytics] 標準、カスタム、予約済みのコンバージョン指標およびトラフィック指標を含む指標は、DSPと Search、Social および Commerce で自動的に使用できます。

![使用例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用例")

次のタスクのほとんどは、 [!DNL Analytics] 管理者またはその他のユーザー。 サポートが必要な場合は、(DSPユーザー )DSPテクニカルサポートチーム ( `adcloud_support@adobe.com` または（検索、Social、およびコマースユーザー）ユーザーアカウントチームにAdobeします。

1. In [!DNL Analytics], [プレースホルダー成功イベントの作成](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   次の追加パラメーターを使用します。

   **タイプ：** `Counter`

   **極性：**  どちらか `Up is Good` または `Up is Bad`

   **表示：** `Visible Everywhere`

   **個別イベントの記録：** `Always Record Event`

   **パーティシペーション：** `Enabled`

   ブランドの Web サイトに新しいイベントを実装する必要はありません。既に取り込まれた既存のデータを使用するからです。

1. での処理ルールの作成と検証 [!DNL Analytics]:

   >[!NOTE]
   >
   >のみ [!DNL Analytics] アカウント管理者は、管理者以外のユーザーに権限を付与していない限り、処理ルールを作成できます。

   1. [処理ルールの作成](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)（次の設定を使用）。

      * 満たす必要がある条件に対して、必要なを指定します [!DNL eVars] または [!DNL props].

        必要に応じて、精度を追加のレベルで設定し、最も正確なイベントを確実に作成できます。

        >[!TIP]
        >
        >ベストプラクティスは、1 つだけを使用することです [!DNL eVar] または [!DNL prop].

      * アクションに対して、「 」を選択します。 **イベントを設定** プレースホルダーイベントを選択します。

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [プロジェクトを作成する](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) 新しいイベントをフリーフォームテーブルに取り込み、 [!DNL eVar] または [!DNL prop] 指標。

1. 担当のAdobeアカウントチームに連絡して、新しい指標をAdobe Advertisingに同期させます。

指標が使用可能になったら、その指標を使用して目標を作成し、それを検索、ソーシャル、コマースのポートフォリオに割り当てたり、 [カスタム目標](/help/dsp/optimization/custom-goal-about.md) DSPパッケージ用。

目標の作成の詳細については、Search、Social、および Commerce から利用できる「目標」に関する「最適化ガイド」の章を参照してください。

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] データのAdobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->