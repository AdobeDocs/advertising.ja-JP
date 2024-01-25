---
title: キャンペーンデータビューの管理
description: キャンペーン、パッケージ、プレースメントおよび広告のデータビューをカスタマイズする方法について説明します。
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# キャンペーンデータビューの管理

## データビジュアライゼーションの管理

キャンペーン全体または単一のキャンペーンのすべてのデータビジュアライゼーションに対して、指標とグラフモードを変更できます。 単一のキャンペーンに対する変更は、 [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads] タブ。

### データのビジュアライゼーションの指標の変更

1. データビジュアライゼーションの右上で、 ![設定](/help/dsp/assets/settings-chart.png).
1. 指標を選択します。
同じ指標を 2 回選択することはできません。
1. クリック **[!UICONTROL Apply]**.

### データビジュアライゼーションの表示モードの変更

* データビジュアライゼーションの右上で、 [!UICONTROL Overlay] スイッチ (![オーバーレイスイッチ](/help/dsp/assets/overlay.png)) をクリックして、オーバーレイモード（すべてのグラフが一緒にオーバーレイ表示）とトレリスグラフモード（3 つの異なるグラフ）を切り替えます。

## データテーブルを管理

すべてのキャンペーン管理ビュー ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]を参照 )、データテーブル内に表示されるデータをカスタマイズできます。

### 列表示の変更

* 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、目的の列表示の名前をクリックします。

### カスタム列表示の作成

1. 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、 **[!UICONTROL Create View]**.

1. ビューに含める指標を指定します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスを選択します。

   1. 必要に応じて、右側のパネルの列名をクリックし、必要な位置までドラッグして、列の順序を編集します。

   一部の列には固定位置があり、移動または削除できません。

1. 設定を適用または保存します。

   * 設定をビューに保存せずに一時的に適用するには、 **[!UICONTROL Apply].**

   * 設定を新しいカスタム列表示に保存するには、 **[!UICONTROL Save As]**. Adobe Analytics の [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、 **[!UICONTROL Save]**.

### カスタム列表示の編集

>[!NOTE]
>
>標準（事前定義済み）の列表示は編集できません。

1. 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、既存の列ビュー名をクリックします。

1. 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、 **[!UICONTROL Edit View]**.

1. 表示に含める指標を編集します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスを選択し、除外する各指標の横にあるチェックボックスをオフにします。

   1. 必要に応じて、右側のパネルの列名をクリックし、必要な位置までドラッグして、列の順序を編集します。

   一部の列には固定位置があり、移動または削除できません。

1. 設定を適用または保存します。

   * 設定をビューに保存せずに一時的に適用するには、 **[!UICONTROL Apply].**

   * 設定を新しいカスタム列表示に保存するには、 **[!UICONTROL Save As]**. Adobe Analytics の [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、 **[!UICONTROL Save]**.

### キャンペーンデータをフィルタ

1. メインツールバーで、 ![フィルターボタン](/help/dsp/assets/filter.png).
1. 適用する各フィルターに対して、左の列のフィルター名をクリックし、フィルター値を指定します。
1. クリック **[!UICONTROL Apply]**.

#### 使用可能なフィルター

では、次のフィルターを使用できます [!UICONTROL Campaigns], [!UICONTROL Packages]、および [!UICONTROL Placements] ビュー：

* [!UICONTROL Campaigns] フィルターを表示：
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] フィルターを表示：
   * [!UICONTROL Custom flights] （存在するかどうか）
   * [!UICONTROL Custom goal] （該当する場合）
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] フィルターを表示：
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] （該当する場合）
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than]または [!UICONTROL equal to] 指定した値 )
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] または [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] フィルターを表示：
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### データ列の並べ替え

任意のデータ列を昇順 (A ～ Z、1 ～ 10) または降順 (Z ～ A、10 ～ 1) で並べ替えることができます。

* 列ヘッダーをクリックして、昇順と降順を切り替えます。

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [プラットフォーム内レポートについて](campaign-reports-about.md)
>* [データビジュアライゼーションの管理](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [列表示の変更](column-view-change.md)
>* [カスタム列表示の作成](column-view-create.md)
>* [カスタム列表示の編集](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [キャンペーンデータをフィルタ](campaign-data-filter.md)
>* [データ列の並べ替え](campaign-data-sort.md)
>* [プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [配置予測レポートの表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [配置診断レポートの表示](placement-diagnostics.md)
>* [Campaign Managementビューからのデータの書き出し](campaign-export-data.md)
>* [ビデオ：DSPアカウントの構造とユーザーインターフェイス](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
