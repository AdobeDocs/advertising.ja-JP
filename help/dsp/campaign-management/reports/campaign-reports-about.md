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

この [!UICONTROL Campaigns] 表示では、パフォーマンスデータグラフのセットと、アカウント内のすべてのキャンペーンのリストが開きます。

### グラフ ビュー {#chart-view}

次のことができます [時系列トレンドグラフのカスタマイズ](campaign-data-views-manage.md#data-visualizations-manage) 3 つの指標を使用するすべてのキャンペーンで。 デフォルトでは、 [!UICONTROL Net Spend], [!UICONTROL Impressions]、および [!UICONTROL Net CPM] は別のグラフ（トレリス グラフ）に含まれます。 オプションで、指標を変更できます。 時系列トレンドグラフで時間別データを有効にするには、日付選択を 1 日に変更します（[!UICONTROL Today], [!UICONTROL Yesterday]、または特定の日）。

![3 つの指標に対して別々のトレンドグラフ](/help/dsp/assets/trend-chart-separate.png)

また、オプションで 3 つの指標をオーバーレイし、異常値や領域を簡単に検出してスケールやパフォーマンスを向上させることもできます。

![オーバーレイ付きトレンドグラフ](/help/dsp/assets/trend-chart.png)

### テーブル表示

![キャンペーンリスト](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行にはペーシングおよび配信指標が含まれます。 ペーシング指標には次のものがあります [!UICONTROL Gross Spend (Lifetime)]には、キャンペーン内のすべてのパッケージをまたいで、実際の目標を達成した支出と期待される目標を達成した支出の比較が含まれているので、パフォーマンスの低いキャンペーンを一目で特定できます。 オプションで、次のことが可能です [列表示の変更](campaign-data-views-manage.md#column-view-change) または [カスタム列表示の作成](campaign-data-views-manage.md#column-view-create).

その他の操作 [データテーブルのカスタマイズ](campaign-data-views-manage.md#data-tables-manage) その他の方法と [表示データをフィルター](campaign-data-views-manage.md#filter-data-tables).

キャンペーンの詳細を表示するには、キャンペーン名をクリックします。

#### アラート指標

*ベータ版機能*

アン &quot;[!UICONTROL Alerts]「」列は、キャンペーンまたはその下の子エンティティに問題があることを示します。 A [!UICONTROL Pulse Panel] ツールバーの右側にあるアイコンは、リストされているエンティティでアラートが使用できるかどうかも示します。 参照先」[アラートの表示](campaign-alerts.md)」を参照してください。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内では、キャンペーンエンティティに基づいてデータをフィルタリングできます。 [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]. その他の操作 [表示データをフィルター](campaign-data-views-manage.md#filter-data-tables) 表示するパッケージ、プレースメントまたは広告のみを含める。

![Campaign エンティティタブ](/help/dsp/assets/campaign-subtabs.png)

### グラフ ビュー

キャンペーンごとに、次のことができます [時系列トレンドグラフのカスタマイズ](campaign-data-views-manage.md#data-visualizations-manage) 3 つの指標を使用できます。これらの指標は、各エンティティビューで使用できます。 キャンペーンのすべてのトレンドグラフにわたって同じ指標が保持されます。

を参照してください。 [クロスキャンペーン指標の「グラフビュー」セクション](#chart-view) を参照してください。

### テーブル表示

各エンティティタブの各行には、デフォルトでペーシングと配信の指標が含まれていますが、次のことができます [列表示の変更](campaign-data-views-manage.md#column-view-change) または [カスタム列表示の作成](campaign-data-views-manage.md#column-view-create) をキャンペーンのすべてのサブタブに適用します。 その他の操作 [データテーブルのカスタマイズ](campaign-data-views-manage.md#data-tables-manage) その他の方法でも同様です。 各データテーブルには、 [!UICONTROL Subtotals] 行：表示されているすべての行の各指標の合計または平均値を表示します。

#### アラート指標

*ベータ版機能*

アン &quot;[!UICONTROL Alerts]「」列は、パッケージ、プレースメント、広告、またはパッケージやプレースメントの下の子エンティティに問題があることを示します。 アン &quot;[!UICONTROL Alerts]「」列は、キャンペーンまたはその下の子エンティティに問題があることを示します。 A [!UICONTROL Pulse Panel] ツールバーの右側にあるアイコンは、リストされているエンティティでアラートが使用できるかどうかも示します。 参照先」[アラートの表示](campaign-alerts.md)」を参照してください。

### その他のタイプのキャンペーンレベルのレポート

その他のデータ内訳については、次を表示します。 [キャンペーンレベルのレポートページ](/help/dsp/campaign-management/campaigns/campaign-view-report.md). レポートには、次のセクションが含まれます [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]、および [!UICONTROL Audience Performance] データ。

### その他のタイプのプレースメントレベルレポート

その他のデータ内訳については、次を表示します。 [プレースメントレベルのレポートページ](/help/dsp/campaign-management/placements/placement-view-report.md). レポートには、次のセクションが含まれます [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications]、および [!UICONTROL Ads] データ。

さらに、プレースメント設定内で次のデータを表示できます。

* [A （詳細ビュー） [!UICONTROL Inspector]）](placement-details-view.md)。すべてのターゲットサイト、広告、頻度データおよびプレースメントの取引を表示します。

* A [配置予測レポート](/help/dsp/campaign-management/reports/placement-forecast.md).

* [プレースメント診断レポート](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### その他のタイプの広告レベルレポート

その他のデータ内訳については、次を表示します。 [広告レベルのレポートページ](/help/dsp/campaign-management/ads/ad-view-report.md). このレポートに含まれる [!UICONTROL Overview], [!UICONTROL Geography]、および [!UICONTROL Viewability] データ。

>[!MORELIKETHIS]
>
>* [プレースメントのサイト、広告、頻度の詳細の表示](placement-details-view.md)
>* [キャンペーンデータビューの管理](campaign-data-views-manage.md)
>* [Campaign Management ビューからのデータの書き出し](campaign-export-data.md)
>* [キャンペーンの詳細レポートの表示](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [アラートの表示](campaign-alerts.md)
