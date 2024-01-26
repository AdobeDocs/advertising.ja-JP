---
title: キャンペーンデータビューの管理
description: キャンペーン、パッケージ、プレースメントおよび広告のデータビューをカスタマイズする方法について説明します。
feature: DSP Campaign Data Views
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# キャンペーンデータビューの管理

キャンペーン管理ビュー ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]) をクリックします。

## データビジュアライゼーションの管理 {#data-visualizations-manage}

キャンペーン全体または単一のキャンペーンのすべてのデータビジュアライゼーションに対して、指標とグラフモードを変更できます。 単一のキャンペーンに対する変更は、そのキャンペーンのすべてのデータビジュアライゼーション ( [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads] ビュー。

### データのビジュアライゼーションの指標の変更

1. データビジュアライゼーションの右上で、 ![設定](/help/dsp/assets/settings-chart.png).

1. 指標を選択します。

   同じ指標を 2 回選択することはできません。

1. クリック **[!UICONTROL Apply]**.

### データビジュアライゼーションの表示モードの変更

* データビジュアライゼーションの右上で、 [!UICONTROL Overlay] スイッチ (![オーバーレイスイッチ](/help/dsp/assets/overlay.png)) をクリックして、オーバーレイモード（すべてのグラフが一緒にオーバーレイ表示）とトレリスグラフモード（3 つの異なるグラフ）を切り替えます。

## データテーブルを管理 {#data-tables-manage}

すべてのキャンペーン管理ビュー ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]を参照 )、データテーブル内に表示されるデータをカスタマイズできます。

### 列表示の管理 {#column-views-manage}

各キャンペーン管理レベル ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]) には、組み込み [!UICONTROL Pacing] および [!UICONTROL Performance] ビューに含まれているエンティティの関連指標が表示されます。 デフォルトでは、 [!UICONTROL Pacing] ビューが表示され、パフォーマンスの低いキャンペーンとキャンペーンのコンポーネントを一目で特定できます。 オプションで、カスタム列セットを作成および編集できます。

![列表示セレクター](/help/dsp/assets/column-view-selector.png)

DSPでは、最新のビューがデフォルトのビューとして保存されるので、ページに戻るたびに、自分に関連する指標を常に表示できます。

#### 列表示の変更 {#column-view-change}

* 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、目的の列表示の名前をクリックします。

#### カスタム列表示の作成 {#column-view-create}

1. 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、 **[!UICONTROL Create View]**.

1. ビューに含める指標を指定します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスを選択します。

      すべての指標は、カテゴリ別にアルファベット順に表示されます。 [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (DSPが追跡する標準指標 ) [!UICONTROL Viewability]、および [!UICONTROL Conversions]. 指標に「([!UICONTROL Lifetime])」の戻り値を検索すると、ページで選択した日付範囲に関係なく、キャンペーンの開始時点からの戻り値が返されます。

   1. 必要に応じて、右側のパネルの列名をクリックし、必要な位置までドラッグして、列の順序を編集します。

   一部の列には固定位置があり、移動または削除できません。

1. 設定を適用または保存します。

   * 設定をビューに保存せずに一時的に適用するには、 **[!UICONTROL Apply].**

   * 設定を新しいカスタム列表示に保存するには、 **[!UICONTROL Save As]**. Adobe Analytics の [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、 **[!UICONTROL Save]**.

#### 列表示の編集 {#column-view-edit}

>[!NOTE]
>
>標準（定義済み）の列表示には変更を保存できませんが、変更を一時的に適用したり、新しいカスタム表示に保存したりできます。

1. 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、既存の列ビュー名をクリックします。

1. 表示セレクターで、 ![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、 **[!UICONTROL Edit View]**.

1. 表示に含める指標を編集します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスを選択し、除外する各指標の横にあるチェックボックスをオフにします。

      すべての指標は、カテゴリ別にアルファベット順に表示されます。 [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (DSPが追跡する標準指標 ) [!UICONTROL Viewability]、および [!UICONTROL Conversions]. 指標に「([!UICONTROL Lifetime])」の戻り値を検索すると、ページで選択した日付範囲に関係なく、キャンペーンの開始時点からの戻り値が返されます。

   1. 必要に応じて、右側のパネルの列名をクリックし、必要な位置までドラッグして、列の順序を編集します。

   一部の列には固定位置があり、移動または削除できません。

1. 設定を適用または保存します。

   * （カスタムビューのみ）設定を保存するには、 **[!UICONTROL Save]**.

   * 設定をビューに保存せずに一時的に適用するには、 **[!UICONTROL Apply].**

   * 設定を新しいカスタム列表示に保存するには、 **[!UICONTROL Save As]**. Adobe Analytics の [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、 **[!UICONTROL Save]**.

### キャンペーンデータをフィルタ {#filter-data-tables}

フィルターは、現在のタブに表示されるデータを変更します。 使用可能なフィルターは、エンティティのタイプによって異なりますが、エンティティ名、ステータス、追加のプロパティ列などが含まれる場合があります。

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


### 日付範囲の変更

任意のデータテーブルの上にある日付範囲セレクターを使用して、すべての標準ビューとカスタムビューで使用される日付範囲を変更します。

![日付範囲セレクター](/help/dsp/assets/date-range-selector.png "日付範囲セレクター")

* プリセット範囲の場合：共通の時間増分のリストから選択します。 デフォルトはです。 [!UICONTROL Last 30 days]*.

* 特定の範囲に対して、次のいずれかの操作を行います。

   * クリック ![カレンダー](/help/dsp/assets/calendar.png "カレンダー")をクリックし、カレンダー内の開始日と終了日をクリックします。

   * 日付範囲内をクリックし、開始日と終了日を入力するか、カレンダー内で選択します。

     数値（M-D-YY から MM-DD-YYYY まで）や月の名前や略語（1 月や 1 月など）を入力できます。

### データ列の並べ替え

任意のデータ列を昇順 (A ～ Z、1 ～ 10) または降順 (Z ～ A、10 ～ 1) で並べ替えることができます。

* 列ヘッダーをクリックして、昇順と降順を切り替えます。


### データ行数の指定

任意のページの右下、の横 **[!UICONTROL Items per page]** を選択します。 *[!UICONTROL 25]*, *[!UICONTROL 50]*&#x200B;または *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Campaign Management Views のパフォーマンスレポートについて](campaign-reports-about.md)
>* [プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [配置予測レポートの表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [配置診断レポートの表示](placement-diagnostics.md)
>* [Campaign Managementビューからのデータの書き出し](campaign-export-data.md)
>* [ビデオ：DSPアカウントの構造とユーザーインターフェイス](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
