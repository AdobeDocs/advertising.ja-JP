---
title: Campaign Managementビューでのパフォーマンスレポートのタイプ
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: c7860d98edbf44b71d97c3800edf47a409606b74
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Campaign Managementビューでのパフォーマンスレポートのタイプ

キャンペーン管理ビューには、包括的なレポートデータが含まれます。 利用可能なレポートは、パフォーマンスの高いパッケージや配置、および注意を必要とするパッケージや配置を特定するのに役立ちます。 また、クイックアクションボタンを使用すると、生産性が向上します。

## すべてのキャンペーン表示

The [!UICONTROL Campaigns] [ 表示 ] をクリックすると、一連のパフォーマンスデータグラフと、アカウント内のすべてのキャンペーンの一覧が開きます。

### グラフ表示 {#chart-view}

以下が可能です。 [時系列トレンドグラフのカスタマイズ](campaign-data-views-manage.md#data-visualizations-manage) がすべてのキャンペーンで使用され、3 つの指標が使用されます。 デフォルトでは、 [!UICONTROL Net Spend], [!UICONTROL Impressions]、および [!UICONTROL Net CPM] は別々のグラフ（トレリス図）に含まれます。 オプションで指標を変更できます。 時系列トレンドグラフの時間別データを有効にするには、日付の選択を 1 日に変更します ([!UICONTROL Today], [!UICONTROL Yesterday]、または特定の日 )。

![3 つの指標に関する個別のトレンドグラフ](/help/dsp/assets/trend-chart-separate.png)

また、オプションで 3 つの指標をオーバーレイして、異常値や、スケールやパフォーマンスを向上させる領域を容易に検出できます。

![オーバーレイを含むトレンドグラフ](/help/dsp/assets/trend-chart.png)

### テーブル表示

![キャンペーンリスト](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行には、ペーシングと配信指標が含まれます。 ペーシング指標には以下が含まれます [!UICONTROL Gross Spend (Lifetime)]：キャンペーン内のすべてのパッケージでの実際の目標上の支出に対する予想される目標上の支出のゲージを含むので、効果の低いキャンペーンを一目で特定できます。 オプションで、 [列表示を変更する](campaign-data-views-manage.md#column-view-change) または [カスタム列表示の作成](campaign-data-views-manage.md#column-view-create).

さらに詳しく [データテーブルのカスタマイズ](campaign-data-views-manage.md#data-tables-manage) 追加の方法と [表示されるデータのフィルター](campaign-data-views-manage.md#filter-data-tables).

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

#### アラート指標

*ベータ版機能*

An &quot;[!UICONTROL Alerts]「 」列は、キャンペーンまたはその下にある子エンティティがいつ問題を抱えているかを示します。 A [!UICONTROL Pulse Panel] ツールバーの右側のアイコンは、リストされているエンティティに対してアラートが使用可能かどうかも示します。 参照：[アラートの表示](campaign-alerts.md)」を参照してください。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内では、キャンペーンエンティティに基づいてデータをフィルタリングできます。 [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]. さらに詳しく [表示されるデータのフィルター](campaign-data-views-manage.md#filter-data-tables) を使用して、表示するパッケージ、プレースメントまたは広告のみを含めます。

![キャンペーンエンティティタブ](/help/dsp/assets/campaign-subtabs.png)

### グラフ表示

キャンペーンごとに、以下の操作を実行できます。 [時系列トレンドグラフのカスタマイズ](campaign-data-views-manage.md#data-visualizations-manage) と 3 つの指標を組み合わせ、各エンティティ表示で使用できます。 キャンペーンのすべてのトレンドグラフで、同じ指標が保持されます。

詳しくは、 [クロスキャンペーン指標に関する「グラフ表示」の節](#chart-view) を参照してください。

### テーブル表示

各エンティティタブでは、デフォルトで、各行にペーシングと配信指標が含まれますが、 [列表示を変更する](campaign-data-views-manage.md#column-view-change) または [カスタム列表示の作成](campaign-data-views-manage.md#column-view-create) をクリックして、キャンペーンのすべてのサブタブに適用します。 さらに詳しく [データテーブルのカスタマイズ](campaign-data-views-manage.md#data-tables-manage) その他の方法では。 各データテーブルには、 [!UICONTROL Subtotals] 行：表示されているすべての行の各指標の合計または平均値を表示します。

#### アラート指標

*ベータ版機能*

An &quot;[!UICONTROL Alerts]「 」列は、パッケージ、配置、広告、またはパッケージまたは配置下の子エンティティに問題がある場合を示します。 An &quot;[!UICONTROL Alerts]「 」列は、キャンペーンまたはその下にある子エンティティがいつ問題を抱えているかを示します。 A [!UICONTROL Pulse Panel] ツールバーの右側のアイコンは、リストされているエンティティに対してアラートが使用可能かどうかも示します。 参照：[アラートの表示](campaign-alerts.md)」を参照してください。

### その他のキャンペーンレベルのレポートタイプ

その他のデータ分類の場合は、 [キャンペーンレベルのレポートページ](/help/dsp/campaign-management/campaigns/campaign-view-report.md). このレポートには、 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]、および [!UICONTROL Audience Performance] データ。

### その他のタイプの配置レベルのレポート

その他のデータ分類の場合は、 [配置レベルのレポートページ](/help/dsp/campaign-management/placements/placement-view-report.md). このレポートには、 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications]、および [!UICONTROL Ads] データ。

また、配置設定内では、次のデータを表示できます。

* [A（詳細ビュー） [!UICONTROL Inspector])](placement-details-view.md)：プレースメントのすべてのターゲットサイト、広告、頻度データおよび取引情報を表示します。

* A [配置予測レポート](/help/dsp/campaign-management/reports/placement-forecast.md)

* [配置診断レポート](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### その他の広告レベルのレポートタイプ

その他のデータ分類の場合は、 [広告レベルのレポートページ](/help/dsp/campaign-management/ads/ad-view-report.md). レポートには以下が含まれます。 [!UICONTROL Overview], [!UICONTROL Geography]、および [!UICONTROL Viewability] データ。

>[!MORELIKETHIS]
>
>* [プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [キャンペーンデータビューの管理](campaign-data-views-manage.md)
>* [Campaign Managementビューからのデータの書き出し](campaign-export-data.md)
>* [キャンペーンの詳細レポートの表示](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [アラートの表示](campaign-alerts.md)
