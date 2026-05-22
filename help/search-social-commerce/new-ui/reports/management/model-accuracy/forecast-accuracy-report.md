---
title: '[!UICONTROL Forecast Accuracy Report]'
description: データ列を含む予測精度レポートについて説明します。
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# ザ [!UICONTROL Forecast Accuracy Report]

このレポートは、指定されたポートフォリオの日別のコストと収益モデルの精度を示します。 デフォルトでは、各ポートフォリオの1日の予測収益と実際の収益、コスト、クリック数、予測の精度が含まれます。 現在ポートフォリオにマッピングされているキャンペーンのデータが含まれます。

過去18か月間のデータを表示できます。

>[!NOTE]
>
>* このレポートは、ポートフォリオレベル [!UICONTROL Model Accuracy Report]と同じデータを提供しますが、複数のポートフォリオをまたいで実行でき、アトリビューションルールを変更できます。 また、カスタムパラメーターを使用してレポートを実行およびスケジュールし、それを使用してスプレッドシートのフィードを作成することもできます。
>
>* ベストプラクティスは、ポートフォリオの支出戦略に関係なく、ほとんどのポートフォリオで固有の曜日の傾向が見られるため、少なくとも過去7日間は[!UICONTROL Forecast Accuracy Report]を表示することです。 最適化機能では、このトレンドを考慮して、それに応じて支出を配分しています。
>
>* コスト予測の場合、過去7日間で10%の偏差は許容できると考えられるため、予測された支出の90%から110%の実際の支出は問題ありません。 売上予測については、過去7日間で15%の偏差が許容できると見なされるので、実際の売上は予測された支出の85%から115%の間です。 より大きな偏差を持つ予測を調査する必要があります。
>
>* ポートフォリオ内のキーワードが入札シフトの制約に関連付けられている場合、入札シフトによって引き起こされる合計金額だけポートフォリオが過小支出または過小支出になります。 その結果、予測コスト列は、目標支出から増減した支出で逸脱する。

## 使用可能な列

以下は、各レポートで使用できる列です。 デフォルトの列は、デフォルトで自動的に含まれます。 使用可能なカスタム列は、レポート設定の[!UICONTROL Columns] セクションから追加できます。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio] | Default | ポートフォリオ。 |
| [!UICONTROL Day of Week] | Default | 報告された曜日：<i>[!UICONTROL Sunday]</i>、<i>[!UICONTROL Monday]</i>、<i>[!UICONTROL Tuesday]</i>、<i>[!UICONTROL Wednesday]</i>、<i>[!UICONTROL Thursday]</i>、<i>[!UICONTROL Friday]</i>、または<i>[!UICONTROL Saturday]</i>。 |
| [!UICONTROL Start Date] | Default | 最初の日が報告されました。 |
| [!UICONTROL End Date] | Default | 最終日が報告されました。 |
| [!UICONTROL Predicted Revenue] | Default | ポートフォリオの予測収益。 |
| [!UICONTROL Revenue] | Default | ポートフォリオの実際の収益。 |
| [!UICONTROL Revenue Accuracy] | Default | 売上予測の精度（パーセントで表されます）。 |
| [!UICONTROL Predicted Cost] | Default | ポートフォリオの予測コスト。 |
| [!UICONTROL Cost] | Default | ポートフォリオの実際のコスト。 |
| [!UICONTROL Cost Accuracy] | Default | コスト予測の精度（パーセントで表されます）。 |
| [!UICONTROL Predicted Clicks] | Default | ポートフォリオに対して予測されるクリック数。 |
| [!UICONTROL Clicks] | Default | ポートフォリオの実際のクリック数。 |
| [!UICONTROL Click Accuracy] | Default | クリック予測の精度。パーセントで表されます。 |
| [!UICONTROL EF Portfolio Group ID] | Default | ポートフォリオが属するポートフォリオグループの数値ID。 |
| [!UICONTROL Portfolio Group Name] | Default | ポートフォリオが属するポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | Default | 数値ポートフォリオ ID。 |

>[!MORELIKETHIS]
>
>* [&#x200B; モデル精度レポートについて](model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [&#x200B; スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [&#x200B; モデル精度レポート設定](model-accuracy-report-settings.md)
