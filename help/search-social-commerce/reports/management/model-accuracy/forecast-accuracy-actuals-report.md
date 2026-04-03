---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: データ列を含む[!UICONTROL Forecast Accuracy (Actuals) Report]について説明します。
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
TQID: https://experienceleague.adobe.com/wQyO42Dt5McqK23z-adEP-BAxxTrBk9RJi0I-4noP0I
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 321
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
| [!UICONTROL Device] | Default | （Google Ads、Microsoft Advertising、Yahoo! Yahoo！ディスプレイネットワーク Japan Ads、およびYahoo Native campaigns）広告が表示されたデバイスタイプ：<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i>、または<i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値は<i>[!UICONTROL N/A]</i>です。<br><br>検索キャンペーンで、キーワード、広告、および/または広告拡張機能のトラッキングテンプレートまたは宛先URLに、デバイス （<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}）でデータを追跡するパラメーターが含まれている場合</code>）広告がクリックされた時点で、コンバージョンデータも各デバイスタイプの行に含まれます。 それ以外の場合、コンバージョンデータをデバイスタイプに関連付けられない場合は、「[!UICONTROL Device]」値が<i>[!UICONTROL N/A]</i>の別の行に集計されます。 |
| [!UICONTROL Revenue] | Default | 総収入。 |
| [!UICONTROL Impressions] | Default | 全体的なインプレッション。 |
| [!UICONTROL Clicks] | Default | 合計クリック数： |
| [!UICONTROL Cost] | Default | 総コスト。 |

>[!MORELIKETHIS]
>
>* [ モデル精度レポートについて](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [ モデル精度レポートを生成](model-accuracy-report-generate.md)
>* [ モデル精度レポート設定](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
