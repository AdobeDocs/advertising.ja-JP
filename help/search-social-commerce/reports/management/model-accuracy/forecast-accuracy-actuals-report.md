---
title: "[!UICONTROL Forecast Accuracy (Actuals) Report]"
description: 詳しくは、 [!UICONTROL Forecast Accuracy (Actuals) Report]（データ列を含む）
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# この [!UICONTROL Forecast Accuracy (Actuals) Report]

このレポートは、各ポートフォリオの広告ネットワークからの実際のインプレッション、クリック数、コスト、売上高のデータを日別に表示します。

## 使用可能な列

次に、各レポートに自動的に含まれる列を示します。 列を追加することはできません。

| 列 | デフォルト？ | 説明 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | デフォルト | ポートフォリオが属するポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | デフォルト | 数値のポートフォリオ ID。 |
| [!UICONTROL EF Portfolio Group ID] | デフォルト | ポートフォリオが属するポートフォリオグループの数値 ID。 |
| [!UICONTROL Portfolio] | デフォルト | ポートフォリオ。 |
| [!UICONTROL Portfolio Status] | デフォルト | ポートフォリオのステータス：<ul><li><i>[!UICONTROL Optimize]:</i> 最適化機能は、関連するキャンペーンのクリックおよび売上高データを収集し、入札を最適化するデータをモデリングし、入札およびキャンペーン予算（最適化タイプおよびキャンペーン入札戦略に応じて）を最適化します。</li><li><i>[!UICONTROL Active]:</i> 最適化機能は、関連するキャンペーンのクリック数および売上高データを収集し、データをモデリングしていますが、入札やキャンペーン予算は最適化されていません。</li><li><i>[!UICONTROL Inactive]:</i> 最適化機能は、レポートを作成する目的で、関連するキャンペーンのクリックデータを収集しますが、データのモデリングや入札やキャンペーン予算の最適化はおこないません。 |
| [!UICONTROL Day of Week] | デフォルト | 報告される曜日： <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>または <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | デフォルト | 報告された日付。 |
| [!UICONTROL Device] | デフォルト | (Google Ads、Microsoft® Advertising、Yahoo! ディスプレイネットワーク、Yahoo! Japan Ads および Yahoo ネイティブキャンペーン ) 広告が表示されたデバイスタイプ。 <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>または <i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行には、 <i>[!UICONTROL N/A]</i>.<br><br>検索キャンペーンで、キーワード、広告および広告拡張のトラッキングテンプレートまたはリンク先 URL に、デバイス (&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}) 別にデータを追跡するためのパラメーターが含まれていた場合</code>) をクリックした時点で、コンバージョンデータも各デバイスタイプの行に含まれます。 それ以外の場合、コンバージョンデータをデバイスタイプに関連付けることができない場合は、別の行で「[!UICONTROL Device]」の値 <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | デフォルト | 合計売上高。 |
| [!UICONTROL Impressions] | デフォルト | 合計インプレッション数。 |
| [!UICONTROL Clicks] | デフォルト | クリック総数。 |
| [!UICONTROL Cost] | デフォルト | 合計コスト。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [モデル精度レポートについて](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [この [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [モデル精度レポートの生成](model-accuracy-report-generate.md)
>* [モデル精度レポート設定](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)

