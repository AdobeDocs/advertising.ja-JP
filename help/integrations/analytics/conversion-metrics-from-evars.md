---
title: Adobe Analytics eVar および prop からのコンバージョン指標の作成
description: データレベルと prop レベルのeVarを使用して、カスタム成功イベント指標を設定します。
feature: Integration with Adobe Analytics, Conversions
source-git-commit: d4f439ad23fc386bc85d95cc1291ec668ecf1cd2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Adobe Analytics eVar および prop からのコンバージョン指標の作成

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

成功イベント指標を使用すると、DSPの目標に最も適したAdobe Analyticsサイトデータに基づいて、Search、Social、および Commerce のパッケージとキャンペーンを最適化できます。 既存の [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) および [prop](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) eVarレベルと prop レベルのデータをイベントに送信する。 その他 [!DNL Analytics] 標準、カスタム、予約済みのコンバージョン指標およびトラフィック指標を含む指標は、DSPと Search、Social および Commerce で自動的に使用できます。

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

1. での処理ルールの作成 [!DNL Analytics]:

   >[!NOTE]
   >
   >のみ [!DNL Analytics] アカウント管理者は、管理者以外のユーザーに権限を付与していない限り、処理ルールを作成できます。

   1. [処理ルールの作成](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)（次の設定を使用）。

      * 満たす必要がある条件の場合、必要な eVar または prop を指定します。

        必要に応じて、精度を追加のレベルで設定し、最も正確なイベントを確実に作成できます。

        >[!TIP]
        >
        >ベストプラクティスは、1 つのeVarまたは prop のみを使用することです。

      * アクションに対して、「 」を選択します。 **イベントを設定** プレースホルダーイベントを選択します。

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [プロジェクトを作成する](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) をクリックし、新しいイベントをフリーフォームテーブルに取り込んで、eVarまたは prop 指標に対してデータが入力されるようにします。

1. 担当のAdobeアカウントチームに連絡して、新しい指標をAdobe Advertisingに同期させます。

指標が使用可能になったら、その指標を使用して目標を作成し、それを検索、ソーシャル、コマースのポートフォリオに割り当てたり、 [カスタム目標](/help/dsp/optimization/custom-goal-about.md) DSPパッケージ用。

目標の作成の詳細については、Search、Social、および Commerce から利用できる「目標」に関する「最適化ガイド」の章を参照してください。

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] データのAdobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->