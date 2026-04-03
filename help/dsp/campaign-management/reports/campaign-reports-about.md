---
title: キャンペーン管理ビューのパフォーマンスレポートの種類
description: キャンペーン管理ビューに含まれるレポートデータについて説明します。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
TQID: https://experienceleague.adobe.com/-3WGjX1rQOEKSO9aSdLxBxfDOIyPUMHLbZg-3bFxMd0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: f784309e-91ce-4bb5-ade4-5cbbceabecc0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 648
ht-degree: 0%

---

# キャンペーン管理ビューのパフォーマンスレポートの種類

キャンペーン管理ビューには、包括的なレポートデータが含まれます。 利用可能なレポートは、パフォーマンスが高いパッケージとプレースメント、および注意が必要なパッケージとプレースメントを特定するのに役立ちます。 クイックアクションボタンも生産性を向上させます。

## 全キャンペーン表示

[!UICONTROL Campaigns] ビューが開き、一連のパフォーマンスデータチャートと、アカウント内のすべてのキャンペーンのリストが表示されます。

### チャートビュー {#chart-view}

3つの指標を使用して、すべてのキャンペーンをまたいで[時系列トレンドチャート &#x200B;](campaign-data-views-manage.md#data-visualizations-manage)をカスタマイズできます。 デフォルトでは、[!UICONTROL Net Spend]、[!UICONTROL Impressions]および[!UICONTROL Net CPM]のデータは別々のグラフ（トレリス グラフ）に含まれます。 オプションで指標を変更できます。 時系列トレンド チャートで時間別データを有効にするには、日付の選択を1日（[!UICONTROL Today]、[!UICONTROL Yesterday]、または特定の日）に変更します。

![3つの指標に対する個別の傾向チャート &#x200B;](/help/dsp/assets/trend-chart-separate.png)

また、オプションで3つの指標をオーバーレイして、異常値を簡単に検出し、スケールやパフォーマンスを向上させる領域を検出することもできます。

![&#x200B; オーバーレイ付きトレンドチャート &#x200B;](/help/dsp/assets/trend-chart.png)

### テーブルビュー

![&#x200B; キャンペーンリスト &#x200B;](/help/dsp/assets/campaigns-list.png)

デフォルトでは、各キャンペーン行にはペーシングと配信の指標が含まれています。 ペーシング指標には[!UICONTROL Gross Spend (Lifetime)]が含まれます。これには、キャンペーン内のすべてのパッケージの実際のターゲット内支出と予想されるターゲット内支出のゲージが含まれます。これにより、パフォーマンスの低いキャンペーンを一目で特定できます。 オプションで[列ビュー](campaign-data-views-manage.md#column-view-change)を変更するか、[&#x200B; カスタム列ビュー](campaign-data-views-manage.md#column-view-create)を作成することもできます。

さらに[追加の方法でデータテーブル &#x200B;](campaign-data-views-manage.md#data-tables-manage)をカスタマイズし、[表示データをフィルタリング &#x200B;](campaign-data-views-manage.md#filter-data-tables)できます。

キャンペーンをより詳細に表示するには、キャンペーン名をクリックします。

#### アラート指標

「[!UICONTROL Alerts]」列は、キャンペーンまたはその下の子エンティティに問題がある場合を示します。 ツールバーの右側にある[!UICONTROL Pulse Panel] アイコンは、リストされているエンティティに対してアラートが使用可能かどうかを示します。 詳しくは、「[&#x200B; アラートを表示](campaign-alerts.md)」を参照してください。

## 単一キャンペーンレポート {#single-campaign-reporting}

キャンペーン内で、キャンペーンエンティティ [!UICONTROL Packages]、[!UICONTROL Placements]および[!UICONTROL Ads]に基づいてデータをフィルタリングできます。 さらに[表示データをフィルタリングして、表示するパッケージ、プレースメント、または広告のみを含めることができます](campaign-data-views-manage.md#filter-data-tables)。

![&#x200B; キャンペーンエンティティのタブ &#x200B;](/help/dsp/assets/campaign-subtabs.png)

### チャートビュー

各キャンペーンについて、3つの指標を含む時系列トレンドチャート [を](campaign-data-views-manage.md#data-visualizations-manage) カスタマイズできます。これらの指標は、各エンティティビューで利用できます。 キャンペーンのすべてのトレンドチャートで、同じ指標が保持されます。

詳しくは、クロスキャンペーン指標[に関する「](#chart-view) 「チャートビュー」の節を参照してください。

### テーブルビュー

各エンティティタブでは、デフォルトで各行にペーシングと配信の指標が含まれますが、[列ビュー](campaign-data-views-manage.md#column-view-change)を変更するか、[&#x200B; カスタム列ビュー](campaign-data-views-manage.md#column-view-create)を作成して、キャンペーンのすべてのサブタブに適用できます。 さらに[&#x200B; データテーブル &#x200B;](campaign-data-views-manage.md#data-tables-manage)を追加の方法でカスタマイズできます。 各データテーブルには[!UICONTROL Subtotals]行が含まれており、表示されているすべての行に対する各指標の合計または平均値が表示されます。

#### アラート指標

「[!UICONTROL Alerts]」列は、パッケージ、プレースメント、または広告（またはパッケージまたはプレースメントの下にあるすべての子エンティティ）に問題がある場合を示します。 「[!UICONTROL Alerts]」列は、キャンペーンまたはその下の子エンティティに問題がある場合を示します。 ツールバーの右側にある[!UICONTROL Pulse Panel] アイコンは、リストされているエンティティに対してアラートが使用可能かどうかを示します。 詳しくは、「[&#x200B; アラートを表示](campaign-alerts.md)」を参照してください。

### その他の種類のキャンペーンレベルのレポート

その他のデータの分類については、[&#x200B; キャンペーンレベルのレポートページ &#x200B;](/help/dsp/campaign-management/campaigns/campaign-view-report.md)を参照してください。 レポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]のデータに関するセクションが含まれています。

### その他の種類のプレースメントレベルのレポート

その他のデータ分類については、[&#x200B; プレースメントレベルのレポートページ &#x200B;](/help/dsp/campaign-management/placements/placement-view-report.md)を参照してください。 レポートには、[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]、[!UICONTROL Notifications]および[!UICONTROL Ads]のデータに関するセクションが含まれています。

さらに、プレースメント設定内で次のデータを表示できます。

* [A （詳細ビュー[!UICONTROL Inspector]） &#x200B;](placement-details-view.md)。プレースメントのターゲットサイト、広告、頻度データ、お得な情報をすべて表示します。

* [&#x200B; プレースメント予測レポート &#x200B;](/help/dsp/campaign-management/reports/placement-forecast.md)。

* [配置診断レポート &#x200B;](/help/dsp/campaign-management/reports/placement-diagnostics.md)。


### その他の種類の広告レベルのレポート

その他のデータの分類については、[広告レベルのレポートページ &#x200B;](/help/dsp/campaign-management/ads/ad-view-report.md)を参照してください。 レポートには、[!UICONTROL Overview]、[!UICONTROL Geography]および[!UICONTROL Viewability]のデータが含まれています。

>[!MORELIKETHIS]
>
>* [&#x200B; プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [&#x200B; キャンペーンデータビューの管理](campaign-data-views-manage.md)
>* [&#x200B; キャンペーン管理ビューからデータをエクスポート &#x200B;](campaign-export-data.md)
>* [&#x200B; キャンペーンの詳細レポートを表示](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [&#x200B; アラートの表示](campaign-alerts.md)
