---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: データ列を含む [!UICONTROL Forecast Accuracy (Actuals) Report] について説明します。
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# [!UICONTROL Forecast Accuracy (Actuals) Report]

このレポートは、広告ネットワークからの実際のインプレッション、クリック数、コスト、売上高のデータを、ポートフォリオごとに日別に表示します。

## 使用可能な列

各レポートに自動的に含まれる列は次のとおりです。 列を追加することはできません。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | デフォルト | ポートフォリオが属しているポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | デフォルト | 数値ポートフォリオ ID。 |
| [!UICONTROL EF Portfolio Group ID] | デフォルト | ポートフォリオが属しているポートフォリオグループの数値 ID。 |
| [!UICONTROL Portfolio] | デフォルト | ポートフォリオ。 |
| [!UICONTROL Portfolio Status] | デフォルト | ポートフォリオの状態：<ul><li><i>[!UICONTROL Optimize]:</i> 最適化機能は、関連するキャンペーンのクリック数および売上高データを収集し、最適化に使用されるデータをモデリングして、最適化のタイプと入札戦略に応じて、入札、キャンペーン予算およびキャンペーン入札戦略のターゲットを最適化します。</li><li><i>[!UICONTROL Active]:</i> 最適化機能は、関連するキャンペーンのクリック数と売上高のデータを収集しており、データをモデリングしていますが、入札やキャンペーン予算を最適化していません。</li><li><i>[!UICONTROL Inactive]:</i> 最適化機能は、レポート目的で関連するキャンペーンのクリックデータを収集していますが、データのモデリングや、入札またはキャンペーン予算の最適化は行っていません。 |
| [!UICONTROL Day of Week] | デフォルト | 報告された曜日：<i>[!UICONTROL Sunday]</i>、<i>[!UICONTROL Monday]</i>、<i>[!UICONTROL Tuesday]</i>、<i>[!UICONTROL Wednesday]</i>、<i>[!UICONTROL Thursday]</i>、<i>[!UICONTROL Friday]</i>、<i>[!UICONTROL Saturday]</i>。 |
| [!UICONTROL Event Date] | デフォルト | レポートされた日付。 |
| [!UICONTROL Device] | デフォルト | （Google広告、Microsoft Advertising、Yahoo! ディスプレイネットワーク，Yahoo! 日本広告、Yahoo ネイティブキャンペーン）広告が表示されたデバイスタイプ：<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i>、<i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値は <i>[!UICONTROL N/A]</i> です。<br><br> 検索キャンペーンで、キーワード、広告または広告拡張機能のトラッキングテンプレートまたは宛先 URL に、デバイス別にデータを追跡するパラメーターが含まれている場合（<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>）を選択した場合は、デバイスタイプごとの行にもコンバージョンデータが含まれます。 そうでない場合、コンバージョンデータをデバイスタイプに関連付けることができない場合は、「[!UICONTROL Device]」の値が <i>[!UICONTROL N/A]</i> の別の行に集計されます。 |
| [!UICONTROL Revenue] | デフォルト | 合計売上高。 |
| [!UICONTROL Impressions] | デフォルト | 合計インプレッション数。 |
| [!UICONTROL Clicks] | デフォルト | クリック総数。 |
| [!UICONTROL Cost] | デフォルト | 合計コスト。 |

>[!MORELIKETHIS]
>
>* [ モデル精度レポートについて ](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [[!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [ モデル精度レポートの生成 ](model-accuracy-report-generate.md)
>* [ モデル精度レポートの設定 ](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
