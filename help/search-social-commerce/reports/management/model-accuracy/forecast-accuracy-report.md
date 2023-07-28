---
title: '[!UICONTROL Forecast Accuracy Report]'
description: データ列を含む予測精度レポートの詳細を説明します。
exl-id: 2bb36728-ae14-441b-bcda-fa457f5cf664
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# The [!UICONTROL Forecast Accuracy Report]

このレポートは、指定したポートフォリオのコストと売上高のモデルの精度を日別に表示します。 デフォルトでは、各ポートフォリオに対する日別の予測および実際の売上高、コスト、クリック数、および予測の精度が含まれます。 ポートフォリオに現在マッピングされているキャンペーンのデータが含まれます。

過去 18 ヶ月のデータを表示できます。

>[!NOTE]
>
>* このレポートは、ポートフォリオレベルと同じデータを提供します [!UICONTROL Model Accuracy Report] ただし、複数のポートフォリオにまたがって実行でき、アトリビューションルールを変更できる点が異なります。 また、カスタムパラメーターを使用してレポートを実行し、スケジュールを設定したり、それを使用してスプレッドシートフィードを作成したりすることもできます。
>
>* ベストプラクティスは、 [!UICONTROL Forecast Accuracy Report] 少なくとも過去 7 日間は、ポートフォリオの支出戦略に関係なく、ほとんどのポートフォリオには本来の曜日トレンドが表示されるからです。 最適化機能は、この傾向を考慮に入れ、それに応じて支出を割り当てます。
>
>* コスト予測の場合、過去 7 日間の 10%の偏差は許容可能と見なされるので、予測支出の 90%～110%の実際の支出は適切です。 売上高予測の場合、過去 7 日間の 15%の偏差が許容可能と見なされるので、実際の売上高（予測支出の 85%～115%）は適切です。 偏差が大きい予測は、調査する必要があります。
>
>* ポートフォリオ内のキーワードが入札シフト制約に関連付けられている場合、ポートフォリオは入札シフトに起因する合計金額で過剰または過少使用します。 その結果、予測されたコスト列は、支出の増減によって目標支出から外れます。

## 使用可能な列

次に、各レポートで使用できる列を示します。 デフォルトの列は、デフォルトで自動的に含まれます。 使用可能なカスタム列を [!UICONTROL Columns] 」セクションに表示されます。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio] | デフォルト | ポートフォリオ。 |
| [!UICONTROL Day of Week] | デフォルト | 報告される曜日： <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>または <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | デフォルト | 最初の日が報告されました。 |
| [!UICONTROL End Date] | デフォルト | 最終日が報告されました。 |
| [!UICONTROL Predicted Revenue] | デフォルト | ポートフォリオの予測売上高。 |
| [!UICONTROL Revenue] | デフォルト | ポートフォリオの実際の売上高。 |
| [!UICONTROL Revenue Accuracy] | デフォルト | 売上高予測の精度をパーセンテージで表します。 |
| [!UICONTROL Predicted Cost] | デフォルト | ポートフォリオに対して予測されるコスト。 |
| [!UICONTROL Cost] | デフォルト | ポートフォリオの実際のコスト。 |
| [!UICONTROL Cost Accuracy] | デフォルト | コスト予測の精度（パーセンテージで表されます）。 |
| [!UICONTROL Predicted Clicks] | デフォルト | ポートフォリオに対して予測されたクリック数。 |
| [!UICONTROL Clicks] | デフォルト | ポートフォリオの実際のクリック数。 |
| [!UICONTROL Click Accuracy] | デフォルト | クリック予測の精度（パーセンテージで表される）。 |
| [!UICONTROL EF Portfolio Group ID] | デフォルト | ポートフォリオが属するポートフォリオグループの数値 ID。 |
| [!UICONTROL Portfolio Group Name] | デフォルト | ポートフォリオが属するポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | デフォルト | 数値のポートフォリオ ID。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [モデル精度レポートについて](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [モデル精度レポートの生成](model-accuracy-report-generate.md)
>* [モデル精度レポート設定](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
