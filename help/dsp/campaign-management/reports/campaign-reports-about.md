---
title: Campaign Management ビューでのパフォーマンスレポートのタイプ
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 4e82caa995286635b4a181f186d6a1fabb09847d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Campaign Management ビューでのパフォーマンスレポートのタイプ

キャンペーン管理ビューには、包括的なレポートデータが含まれます。 利用可能なレポートは、パフォーマンスが高いパッケージとプレースメント、および注意が必要なパッケージとプレースメントを特定するのに役立ちます。 クイックアクションボタンを使用すると、生産性も向上します。

## すべてのキャンペーン ビュー

[!UICONTROL Campaigns] ビューが開き、パフォーマンスデータグラフのセットと、アカウント内のすべてのキャンペーンのリストが表示されます。

### グラフ ビュー {#chart-view}

3 つの指標を使用して、すべてのキャンペーンをまたいで [ 時系列トレンドグラフをカスタマイズ ](campaign-data-views-manage.md#data-visualizations-manage) できます。 デフォルトでは、[!UICONTROL Net Spend]、[!UICONTROL Impressions]、[!UICONTROL Net CPM] のデータは、別々のグラフ（trellis グラフ）に含まれています。 オプションで、指標を変更できます。 時系列トレンドグラフで時間別データを有効にするには、日付選択を 1 日（[!UICONTROL Today]、[!UICONTROL Yesterday] または特定の日）に変更します。

![3 つの指標についてトレンドグラフを分ける ](/help/dsp/assets/trend-chart-separate.png)

また、オプションで 3 つの指標をオーバーレイし、異常値や領域を簡単に検出してスケールやパフォーマンスを向上させることもできます。

![ オーバーレイ付きトレンドグラフ ](/help/dsp/assets/trend-chart.png)

### テーブル表示

![ キャンペーンリスト ](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行にはペーシングおよび配信指標が含まれます。 ペーシング指標には [!UICONTROL Gross Spend (Lifetime)] が含まれます。この指標は、キャンペーン内のすべてのパッケージについて、実際の目標を達成した支出と期待される目標を達成した支出の比較を含んでいるので、パフォーマンスの低いキャンペーンを一目で特定できます。 オプションで [ 列表示を変更 ](campaign-data-views-manage.md#column-view-change) または [ カスタム列表示を作成 ](campaign-data-views-manage.md#column-view-create) することもできます。

さらに [ データテーブルをカスタマイズ ](campaign-data-views-manage.md#data-tables-manage) したり、表示データを [ フィルタリング ](campaign-data-views-manage.md#filter-data-tables) したりできます。

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

#### アラート指標

*Beta機能*

「[!UICONTROL Alerts]」列は、キャンペーンまたはその下の子エンティティに問題があることを示します。 ツールバーの右側にある [!UICONTROL Pulse Panel] アイコンは、リストされているエンティティでアラートが使用できるかどうかも示します。 詳しくは、「[ アラートの表示 ](campaign-alerts.md)」を参照してください。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内では、キャンペーンエンティティ（[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads]）に基づいてデータをフィルタリングできます。 さらに [ 表示データをフィルタリング ](campaign-data-views-manage.md#filter-data-tables) して、表示するパッケージ、プレースメントまたは広告のみを含めることができます。

![Campaign エンティティタブ ](/help/dsp/assets/campaign-subtabs.png)

### グラフ ビュー

キャンペーンごとに、3 つの指標を使用して [ 時系列トレンドグラフをカスタマイズ ](campaign-data-views-manage.md#data-visualizations-manage) できます。これらの指標は、各エンティティビューで使用できます。 キャンペーンのすべてのトレンドグラフにわたって同じ指標が保持されます。

詳しくは、クロスキャンペーン指標に関する [ 「グラフ表示」の節を参照 ](#chart-view) てください。

### テーブル表示

各エンティティタブでは、デフォルトで各行にペーシング指標と配信指標が含まれていますが、キャンペーンのすべてのサブタブにそれらの指標を適用するには、[ 列表示を変更 ](campaign-data-views-manage.md#column-view-change) または [ カスタム列表示を作成 ](campaign-data-views-manage.md#column-view-create) を実行します。 追加の方法で [ データテーブルをカスタマイズ ](campaign-data-views-manage.md#data-tables-manage) することもできます。 各データテーブルには、表示可能なすべての行にわたる各指標の合計または平均値を表示する [!UICONTROL Subtotals] 行が含まれます。

#### アラート指標

*Beta機能*

「[!UICONTROL Alerts]」列は、パッケージ、プレースメント、広告、またはパッケージやプレースメントの下の子エンティティに問題があることを示します。 「[!UICONTROL Alerts]」列は、キャンペーンまたはその下の子エンティティに問題があることを示します。 ツールバーの右側にある [!UICONTROL Pulse Panel] アイコンは、リストされているエンティティでアラートが使用できるかどうかも示します。 詳しくは、「[ アラートの表示 ](campaign-alerts.md)」を参照してください。

### その他のタイプのキャンペーンレベルのレポート

その他のデータブレークアウトについては、[ キャンペーンレベルのレポートページ ](/help/dsp/campaign-management/campaigns/campaign-view-report.md) を参照してください。 このレポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、および [!UICONTROL Audience Performance] データに関するセクションが含まれています。

### その他のタイプのプレースメントレベルレポート

その他のデータブレークアウトについては、[ プレースメントレベルのレポートページ ](/help/dsp/campaign-management/placements/placement-view-report.md) を参照してください。 レポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]、[!UICONTROL Notifications]、および [!UICONTROL Ads] データに関するセクションが含まれています。

さらに、プレースメント設定内で次のデータを表示できます。

* [A （詳細ビュー [!UICONTROL Inspector]） ](placement-details-view.md)：ターゲットサイト、広告、頻度データをすべて表示し、プレースメントの取引を表示します。

* [ プレースメント予測レポート ](/help/dsp/campaign-management/reports/placement-forecast.md)。

* [ プレースメント診断レポート ](/help/dsp/campaign-management/reports/placement-diagnostics.md)。


### その他のタイプの広告レベルレポート

その他のデータブレークアウトについては、[ 広告レベルのレポートページ ](/help/dsp/campaign-management/ads/ad-view-report.md) を参照してください。 レポートには、[!UICONTROL Overview]、[!UICONTROL Geography]、[!UICONTROL Viewability] のデータが含まれます。

>[!MORELIKETHIS]
>
>* [ プレースメントのサイト、広告、頻度の詳細の表示 ](placement-details-view.md)
>* [ キャンペーンデータビューの管理 ](campaign-data-views-manage.md)
>* [Campaign Management ビューからのデータのエクスポート ](campaign-export-data.md)
>* [ キャンペーンの詳細レポートの表示 ](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [ アラートの表示 ](campaign-alerts.md)
