---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: について説明します [!UICONTROL Forecast Accuracy (Actuals) Report]（データ列を含む）
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# この [!UICONTROL Forecast Accuracy (Actuals) Report]

このレポートは、広告ネットワークからの実際のインプレッション、クリック数、コスト、売上高のデータを、ポートフォリオごとに日別に表示します。

## 使用可能な列

各レポートに自動的に含まれる列は次のとおりです。 列を追加することはできません。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | デフォルト | ポートフォリオが属しているポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | デフォルト | 数値ポートフォリオ ID。 |
| [!UICONTROL EF Portfolio Group ID] | デフォルト | ポートフォリオが属しているポートフォリオグループの数値 ID。 |
| [!UICONTROL Portfolio] | デフォルト | ポートフォリオ。 |
| [!UICONTROL Portfolio Status] | デフォルト | ポートフォリオの状態：<ul><li><i>[!UICONTROL Optimize]:</i> 最適化機能は、関連するキャンペーンのクリック数と売上高のデータを収集し、入札を最適化するためのデータをモデリングし、（最適化タイプとキャンペーン入札戦略に応じて）入札とキャンペーン予算の最適化を行います。</li><li><i>[!UICONTROL Active]:</i> 最適化機能は、関連するキャンペーンのクリック数と売上高のデータを収集しており、データをモデリングしていますが、入札やキャンペーン予算を最適化していません。</li><li><i>[!UICONTROL Inactive]:</i> 最適化機能は、レポート目的で関連するキャンペーンのクリックデータを収集していますが、データのモデリングや、入札またはキャンペーン予算の最適化は行っていません。 |
| [!UICONTROL Day of Week] | デフォルト | レポートされる曜日： <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>、または <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | デフォルト | レポートされた日付。 |
| [!UICONTROL Device] | デフォルト | （Google広告、Microsoft広告、Yahoo! ディスプレイネットワーク，Yahoo! 日本広告、Yahoo ネイティブキャンペーン）広告が表示されたデバイスタイプ。 <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>、または <i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値は次のとおりです <i>[!UICONTROL N/A]</i>.<br><br>検索キャンペーンで、キーワード、広告または広告拡張機能のトラッキングテンプレートや宛先 URL に、デバイス別にデータを追跡するパラメーターが含まれている場合（<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>）を選択した場合は、デバイスタイプごとの行にもコンバージョンデータが含まれます。 そうでない場合、コンバージョンデータをデバイスタイプに関連付けることができない場合は、「」を使用して別の行に集計されます[!UICONTROL Device]の値 <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | デフォルト | 合計売上高。 |
| [!UICONTROL Impressions] | デフォルト | 合計インプレッション数。 |
| [!UICONTROL Clicks] | デフォルト | クリック総数。 |
| [!UICONTROL Cost] | デフォルト | 合計コスト。 |

>[!MORELIKETHIS]
>
>* [モデル精度レポートについて](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [この [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [モデル精度レポートの生成](model-accuracy-report-generate.md)
>* [モデル精度レポートの設定](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
