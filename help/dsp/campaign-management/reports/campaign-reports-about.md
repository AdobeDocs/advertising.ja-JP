---
title: Campaign Management ビューでのパフォーマンスレポートのタイプ
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: eba8e9813f8daea58b30f7890ac2dca2498f326f
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Campaign Management ビューでのパフォーマンスレポートのタイプ

キャンペーン管理ビューには、包括的なレポートデータが含まれます。 利用可能なレポートは、パフォーマンスが高いパッケージとプレースメント、および注意が必要なパッケージとプレースメントを特定するのに役立ちます。 クイックアクションボタンを使用すると、生産性も向上します。

## すべてのキャンペーン ビュー

[!UICONTROL Campaigns] ビューが開き、パフォーマンスデータグラフのセットと、アカウント内のすべてのキャンペーンのリストが表示されます。

### グラフ ビュー {#chart-view}

3 つの指標を使用して、すべてのキャンペーンをまたいで [&#x200B; 時系列トレンドグラフをカスタマイズ &#x200B;](campaign-data-views-manage.md#data-visualizations-manage) できます。 デフォルトでは、[!UICONTROL Net Spend]、[!UICONTROL Impressions]、[!UICONTROL Net CPM] のデータは、別々のグラフ（trellis グラフ）に含まれています。 オプションで、指標を変更できます。 時系列トレンドグラフで時間別データを有効にするには、日付選択を 1 日（[!UICONTROL Today]、[!UICONTROL Yesterday] または特定の日）に変更します。

![3 つの指標についてトレンドグラフを分ける &#x200B;](/help/dsp/assets/trend-chart-separate.png)

また、オプションで 3 つの指標をオーバーレイし、異常値や領域を簡単に検出してスケールやパフォーマンスを向上させることもできます。

![&#x200B; オーバーレイ付きトレンドグラフ &#x200B;](/help/dsp/assets/trend-chart.png)

### テーブル表示

![&#x200B; キャンペーンリスト &#x200B;](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行にはペーシングおよび配信指標が含まれます。 ペーシング指標には [!UICONTROL Gross Spend (Lifetime)] が含まれます。この指標は、キャンペーン内のすべてのパッケージについて、実際の目標を達成した支出と期待される目標を達成した支出の比較を含んでいるので、パフォーマンスの低いキャンペーンを一目で特定できます。 オプションで [&#x200B; 列表示を変更 &#x200B;](campaign-data-views-manage.md#column-view-change) または [&#x200B; カスタム列表示を作成 &#x200B;](campaign-data-views-manage.md#column-view-create) することもできます。

さらに [&#x200B; データテーブルをカスタマイズ &#x200B;](campaign-data-views-manage.md#data-tables-manage) したり、表示データを [&#x200B; フィルタリング &#x200B;](campaign-data-views-manage.md#filter-data-tables) したりできます。

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

#### アラート指標

「[!UICONTROL Alerts]」列は、キャンペーンまたはその下の子エンティティに問題があることを示します。 ツールバーの右側にある [!UICONTROL Pulse Panel] アイコンは、リストされているエンティティでアラートが使用できるかどうかも示します。 詳しくは、「[&#x200B; アラートの表示 &#x200B;](campaign-alerts.md)」を参照してください。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内では、キャンペーンエンティティ（[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads]）に基づいてデータをフィルタリングできます。 さらに [&#x200B; 表示データをフィルタリング &#x200B;](campaign-data-views-manage.md#filter-data-tables) して、表示するパッケージ、プレースメントまたは広告のみを含めることができます。

![Campaign エンティティタブ &#x200B;](/help/dsp/assets/campaign-subtabs.png)

### グラフ ビュー

キャンペーンごとに、3 つの指標を使用して [&#x200B; 時系列トレンドグラフをカスタマイズ &#x200B;](campaign-data-views-manage.md#data-visualizations-manage) できます。これらの指標は、各エンティティビューで使用できます。 キャンペーンのすべてのトレンドグラフにわたって同じ指標が保持されます。

詳しくは、クロスキャンペーン指標に関する [&#x200B; 「グラフ表示」の節を参照 &#x200B;](#chart-view) てください。

### テーブル表示

各エンティティタブでは、デフォルトで各行にペーシング指標と配信指標が含まれていますが、キャンペーンのすべてのサブタブにそれらの指標を適用するには、[&#x200B; 列表示を変更 &#x200B;](campaign-data-views-manage.md#column-view-change) または [&#x200B; カスタム列表示を作成 &#x200B;](campaign-data-views-manage.md#column-view-create) を実行します。 追加の方法で [&#x200B; データテーブルをカスタマイズ &#x200B;](campaign-data-views-manage.md#data-tables-manage) することもできます。 各データテーブルには、表示可能なすべての行にわたる各指標の合計または平均値を表示する [!UICONTROL Subtotals] 行が含まれます。

#### アラート指標

「[!UICONTROL Alerts]」列は、パッケージ、プレースメント、広告、またはパッケージやプレースメントの下の子エンティティに問題があることを示します。 「[!UICONTROL Alerts]」列は、キャンペーンまたはその下の子エンティティに問題があることを示します。 ツールバーの右側にある [!UICONTROL Pulse Panel] アイコンは、リストされているエンティティでアラートが使用できるかどうかも示します。 詳しくは、「[&#x200B; アラートの表示 &#x200B;](campaign-alerts.md)」を参照してください。

### その他のタイプのキャンペーンレベルのレポート

その他のデータブレークアウトについては、[&#x200B; キャンペーンレベルのレポートページ &#x200B;](/help/dsp/campaign-management/campaigns/campaign-view-report.md) を参照してください。 このレポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、および [!UICONTROL Audience Performance] データに関するセクションが含まれています。

### その他のタイプのプレースメントレベルレポート

その他のデータブレークアウトについては、[&#x200B; プレースメントレベルのレポートページ &#x200B;](/help/dsp/campaign-management/placements/placement-view-report.md) を参照してください。 レポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]、[!UICONTROL Notifications]、および [!UICONTROL Ads] データに関するセクションが含まれています。

さらに、プレースメント設定内で次のデータを表示できます。

* [A （詳細ビュー [!UICONTROL Inspector]） &#x200B;](placement-details-view.md)：ターゲットサイト、広告、頻度データをすべて表示し、プレースメントの取引を表示します。

* [&#x200B; プレースメント予測レポート &#x200B;](/help/dsp/campaign-management/reports/placement-forecast.md)。

* [&#x200B; プレースメント診断レポート &#x200B;](/help/dsp/campaign-management/reports/placement-diagnostics.md)。


### その他のタイプの広告レベルレポート

その他のデータブレークアウトについては、[&#x200B; 広告レベルのレポートページ &#x200B;](/help/dsp/campaign-management/ads/ad-view-report.md) を参照してください。 レポートには、[!UICONTROL Overview]、[!UICONTROL Geography]、[!UICONTROL Viewability] のデータが含まれます。

>[!MORELIKETHIS]
>
>* [&#x200B; プレースメントのサイト、広告、頻度の詳細の表示 &#x200B;](placement-details-view.md)
>* [&#x200B; キャンペーンデータビューの管理 &#x200B;](campaign-data-views-manage.md)
>* [Campaign Management ビューからのデータのエクスポート &#x200B;](campaign-export-data.md)
>* [&#x200B; キャンペーンの詳細レポートの表示 &#x200B;](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [&#x200B; アラートの表示 &#x200B;](campaign-alerts.md)
