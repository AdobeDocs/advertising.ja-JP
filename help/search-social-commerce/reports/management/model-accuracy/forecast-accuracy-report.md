---
title: '[!UICONTROL Forecast Accuracy Report]'
description: データ列を含む予測精度レポートについて説明します。
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# [!UICONTROL Forecast Accuracy Report]

このレポートには、指定したポートフォリオの日別のコストと収益モデルの精度が表示されます。 デフォルトでは、各ポートフォリオについて、毎日の予測収益および実際の収益、コスト、クリック数、ならびに予測の精度が含まれます。 現在ポートフォリオにマッピングされているキャンペーンのデータが含まれます。

過去 18 か月のデータを表示できます。

>[!NOTE]
>
>* このレポートは、ポートフォリオレベルの [!UICONTROL Model Accuracy Report] と同じデータを提供しますが、複数のポートフォリオで実行でき、属性ルールを変更できる点が異なります。 カスタムパラメーターを使用してレポートを実行およびスケジュールしたり、スプレッドシートフィードの作成に使用したりすることもできます。
>
>* ベストプラクティスは、ポートフォリオの支出戦略に関係なく、ほとんどのポートフォリオは曜日の固有のトレンドを見ているので、少なくとも過去 7 日間は [!UICONTROL Forecast Accuracy Report] を表示することです。 最適化機能では、このトレンドを考慮に入れ、それに応じて費用を割り当てます。
>
>* コスト予測の場合、過去 7 日間に 10% の偏差は許容できると見なされるので、実際の支出は予測された支出の 90% ～ 110% の間であれば問題ありません。 収益予測の場合、過去 7 日間の 15% の偏差は許容できると見なされるので、実際の収益は、予測支出の 85% から 115% の間であれば問題ありません。 偏差が大きい予測は調査する必要があります。
>
>* ポートフォリオ内のキーワードが入札シフト制約に関連付けられている場合、ポートフォリオは入札シフトによって発生する合計金額だけ支出を超過または下回ります。 その結果、予測コスト列は、支出の増加または減少によって目標支出からずれます。

## 使用可能な列

各レポートで使用できる列は次のとおりです。 デフォルトの列は、デフォルトで自動的に含まれます。 使用可能なカスタム列は、レポート設定の「[!UICONTROL Columns]」セクションから追加できます。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio] | デフォルト | ポートフォリオ。 |
| [!UICONTROL Day of Week] | デフォルト | 報告された曜日：<i>[!UICONTROL Sunday]</i>、<i>[!UICONTROL Monday]</i>、<i>[!UICONTROL Tuesday]</i>、<i>[!UICONTROL Wednesday]</i>、<i>[!UICONTROL Thursday]</i>、<i>[!UICONTROL Friday]</i>、<i>[!UICONTROL Saturday]</i>。 |
| [!UICONTROL Start Date] | デフォルト | 報告された最初の日。 |
| [!UICONTROL End Date] | デフォルト | 最後に報告された日。 |
| [!UICONTROL Predicted Revenue] | デフォルト | ポートフォリオに対して予測される売上高。 |
| [!UICONTROL Revenue] | デフォルト | ポートフォリオの実収益。 |
| [!UICONTROL Revenue Accuracy] | デフォルト | 売上高予測の精度（パーセント単位）。 |
| [!UICONTROL Predicted Cost] | デフォルト | ポートフォリオの予測コスト。 |
| [!UICONTROL Cost] | デフォルト | ポートフォリオの実際のコスト。 |
| [!UICONTROL Cost Accuracy] | デフォルト | コスト予測の精度（パーセント単位）。 |
| [!UICONTROL Predicted Clicks] | デフォルト | ポートフォリオで予測されたクリック数。 |
| [!UICONTROL Clicks] | デフォルト | ポートフォリオの実際のクリック数。 |
| [!UICONTROL Click Accuracy] | デフォルト | クリック予測の精度（パーセントで表します）。 |
| [!UICONTROL EF Portfolio Group ID] | デフォルト | ポートフォリオが属しているポートフォリオグループの数値 ID。 |
| [!UICONTROL Portfolio Group Name] | デフォルト | ポートフォリオが属しているポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | デフォルト | 数値ポートフォリオ ID。 |

>[!MORELIKETHIS]
>
>* [&#x200B; モデル精度レポートについて &#x200B;](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [[!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [&#x200B; モデル精度レポートの生成 &#x200B;](model-accuracy-report-generate.md)
>* [&#x200B; モデル精度レポートの設定 &#x200B;](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
