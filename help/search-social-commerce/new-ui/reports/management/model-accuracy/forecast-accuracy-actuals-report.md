---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: データ列を含む[!UICONTROL Forecast Accuracy (Actuals) Report]について説明します。
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# ザ [!UICONTROL Forecast Accuracy (Actuals) Report]

このレポートには、各ポートフォリオの日別の広告ネットワークの実際のインプレッション、クリック、コスト、収益データが表示されます。

## 使用可能な列

以下は、各レポートに自動的に含まれる列です。 追加の列を追加することはできません。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Default | ポートフォリオが属するポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | Default | 数値ポートフォリオ ID。 |
| [!UICONTROL EF Portfolio Group ID] | Default | ポートフォリオが属するポートフォリオグループの数値ID。 |
| [!UICONTROL Portfolio] | Default | ポートフォリオ。 |
| [!UICONTROL Portfolio Status] | Default | ポートフォリオステータス：<ul><li><i>[!UICONTROL Optimize]:</i>最適化機能では、関連するキャンペーンのクリック数と収益データを収集し、最適化に使用されたデータをモデリングして、入札、キャンペーン予算、キャンペーン入札戦略のターゲットを最適化しています（最適化の種類と入札戦略によって異なります）。</li><li><i>[!UICONTROL Active]:</i>最適化機能は、関連するキャンペーンのクリック数と収益データを収集し、データをモデリングしていますが、入札額やキャンペーン予算を最適化していません。</li><li><i>[!UICONTROL Inactive]:</i>最適化機能は、レポート用に関連するキャンペーンのクリック データを収集していますが、データのモデリングや、入札やキャンペーン予算の最適化を行っていません。 |
| [!UICONTROL Day of Week] | Default | 報告された曜日：<i>[!UICONTROL Sunday]</i>、<i>[!UICONTROL Monday]</i>、<i>[!UICONTROL Tuesday]</i>、<i>[!UICONTROL Wednesday]</i>、<i>[!UICONTROL Thursday]</i>、<i>[!UICONTROL Friday]</i>、または<i>[!UICONTROL Saturday]</i>。 |
| [!UICONTROL Event Date] | Default | 報告された日付。 |
| [!UICONTROL Device] | Default | （Google Ads、[!DNL LY Ads]、Microsoft Advertising、Yahoo! ディスプレイ ネットワーク、およびYahoo ネイティブ キャンペーン）広告が表示されたデバイス タイプ：<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i>、または<i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値は<i>[!UICONTROL N/A]</i>です。<br><br>検索キャンペーンで、キーワード、広告、および/または広告拡張機能のトラッキングテンプレートまたは宛先URLに、デバイス （<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}）でデータを追跡するパラメーターが含まれている場合</code>）広告がクリックされた時点で、コンバージョンデータも各デバイスタイプの行に含まれます。 それ以外の場合、コンバージョンデータをデバイスタイプに関連付けられない場合は、「[!UICONTROL Device]」値が<i>[!UICONTROL N/A]</i>の別の行に集計されます。 |
| [!UICONTROL Revenue] | Default | 総収入。 |
| [!UICONTROL Impressions] | Default | 全体的なインプレッション。 |
| [!UICONTROL Clicks] | Default | 合計クリック数： |
| [!UICONTROL Cost] | Default | 総コスト。 |

>[!MORELIKETHIS]
>
>* [ モデル精度レポートについて](model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [ スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [ モデル精度レポート設定](model-accuracy-report-settings.md)
