---
title: キャンペーンデータビューの管理
description: キャンペーン、パッケージ、プレースメント、広告のデータビューをカスタマイズする方法について説明します。
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 5b07096e5f07c60a3efcbf4213b3bc2f061f36a4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# キャンペーンデータビューの管理

キャンペーン管理ビューに表示されるデータ（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads]）をカスタマイズできます。

## データビジュアライゼーションの管理 {#data-visualizations-manage}

キャンペーン全体または単一のキャンペーンのすべてのデータビジュアライゼーションについて、指標とグラフモードを変更できます。 1 つのキャンペーンに対する変更は、[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads] の各ビューの変更を含む、キャンペーンのすべてのデータビジュアライゼーションに適用されます。

### データビジュアライゼーションの指標の変更

1. データビジュアライゼーションの右上にある ![ 設定 ](/help/dsp/assets/settings-chart.png) をクリックします。

1. 指標を選択します。

   同じ指標を 2 回選択することはできません。

1. 「**[!UICONTROL Apply]**」をクリックします。

### データビジュアライゼーションの表示モードの変更

* データビジュアライゼーションの右上にある [!UICONTROL Overlay] スイッチ（![ オーバーレイスイッチ ](/help/dsp/assets/overlay.png)）をクリックして、オーバーレイモード（すべてのグラフが重ねて表示される）とトレリスグラフモード（3 つの異なるグラフ）を変更します。

## データテーブルの管理 {#data-tables-manage}

すべてのキャンペーン管理ビュー（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements] および [!UICONTROL Ads]）で、データテーブル内に表示されるデータをカスタマイズできます。

### 列表示の管理 {#column-views-manage}

各キャンペーン管理レベル（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements] および [!UICONTROL Ads]）には、そのエンティティの関連指標を含む組み込みの [!UICONTROL Pacing] ビューと [!UICONTROL Performance] ビューが含まれています。 デフォルトでは [!UICONTROL Pacing] ビューが表示されるので、パフォーマンスの低いキャンペーンやキャンペーンコンポーネントを一目で特定できます。 オプションで、カスタム列セットを作成および編集できます。

![ 列表示セレクター ](/help/dsp/assets/column-view-selector.png)

DSPでは最新のビューをデフォルトビューとして保存するので、ページに戻るたびに、常に自分に関連する指標を表示できます。

#### 列表示の変更 {#column-view-change}

* 表示セレクターで ![ 下矢印 ](/help/dsp/assets/chevron-down.png) をクリックし、目的の列表示の名前をクリックします。

#### カスタム列ビューの作成 {#column-view-create}

1. 表示セレクターで ![ 下矢印 ](/help/dsp/assets/chevron-down.png) をクリックし、「**[!UICONTROL Create View]**」をクリックします。

1. ビューに含める指標を指定：

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスを選択します。

      すべての指標は、カテゴリ（[!UICONTROL Settings]、[!UICONTROL Spend]、[!UICONTROL Pacing]、[!UICONTROL Reporting] （DSPが追跡する標準指標）、[!UICONTROL Viewability]、[!UICONTROL Conversions] のアルファベット順になります。 「（[!UICONTROL Lifetime]）」が追加された指標では、ページで選択した日付範囲に関係なく、キャンペーンの開始時から値が返されます。

   1. 必要に応じて、右側のパネルで列名をクリックして必要な位置にドラッグすることで、列の順序を編集します。

   一部の列は、固定された位置を持ち、移動または削除できません。

1. 設定を適用または保存します。

   * 設定をビューに保存せずに一時的に適用するには、[**[!UICONTROL Apply]] をクリックします。**

   * 新しいカスタム列ビューに設定を保存するには、[**[!UICONTROL Save As]**] をクリックします。 [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、[**[!UICONTROL Save]**] をクリックします。

#### 列表示の編集 {#column-view-edit}

>[!NOTE]
>
>標準（事前定義済み）列ビューには変更を保存できませんが、変更を一時的に適用したり、新しいカスタムビューに保存したりできます。

1. 表示セレクタで ![ 下矢印 ](/help/dsp/assets/chevron-down.png) をクリックし、既存の列表示名をクリックします。

1. 表示セレクターで ![ 下矢印 ](/help/dsp/assets/chevron-down.png) をクリックし、「**[!UICONTROL Edit View]**」をクリックします。

1. ビューに含める指標を編集します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスをオンにし、除外する各指標の横にあるチェックボックスをオフにします。

      すべての指標は、カテゴリ（[!UICONTROL Settings]、[!UICONTROL Spend]、[!UICONTROL Pacing]、[!UICONTROL Reporting] （DSPが追跡する標準指標）、[!UICONTROL Viewability]、[!UICONTROL Conversions] のアルファベット順になります。 「（[!UICONTROL Lifetime]）」が追加された指標では、ページで選択した日付範囲に関係なく、キャンペーンの開始時から値が返されます。

   1. 必要に応じて、右側のパネルで列名をクリックして必要な位置にドラッグすることで、列の順序を編集します。

   一部の列は、固定された位置を持ち、移動または削除できません。

1. 設定を適用または保存します。

   * （カスタム ビューのみ）設定を保存するには、[**[!UICONTROL Save]**] をクリックします。

   * 設定をビューに保存せずに一時的に適用するには、[**[!UICONTROL Apply]] をクリックします。**

   * 新しいカスタム列ビューに設定を保存するには、[**[!UICONTROL Save As]**] をクリックします。 [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、[**[!UICONTROL Save]**] をクリックします。

### キャンペーンデータのフィルタリング {#filter-data-tables}

フィルターは、現在のタブに表示されるデータを変更します。 使用可能なフィルターは、エンティティタイプによって異なりますが、エンティティ名、ステータス、追加のプロパティ列が含まれる場合があります。

1. メインツールバーで、「![ フィルターボタン ](/help/dsp/assets/filter.png)」をクリックします。
1. 適用するフィルターごとに、左側の列でフィルター名をクリックし、フィルター値を指定します。
1. 「**[!UICONTROL Apply]**」をクリックします。

#### 使用可能なフィルター

[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements] の各ビューでは、次のフィルターを使用できます。

* [!UICONTROL Campaigns] ビューフィルター：
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] ビューフィルター：
   * [!UICONTROL Custom flights] （存在するかどうか）
   * [!UICONTROL Custom goal] （該当する場合）
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] ビューフィルター：
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] （該当する場合）
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] （[!UICONTROL less than]、[!UICONTROL greater than]、または [!UICONTROL equal to] は指定された値）
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] （[!UICONTROL impressions] または [!UICONTROL spend]）
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] ビューフィルター：
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### 日付範囲の変更

任意のデータテーブルの上にある日付範囲セレクターを使用して、すべての標準ビューとカスタムビューで使用される日付範囲を変更します。

![ 日付範囲セレクター ](/help/dsp/assets/date-range-selector.png " 日付範囲セレクター ")

* プリセット範囲の場合：一般的な時間増分のリストから選択します。 デフォルトは [!UICONTROL Last 30 days]*です。

* 特定の範囲に対して、次のいずれかの操作を行います。

   * ![ カレンダー ](/help/dsp/assets/calendar.png " カレンダー ") をクリックし、カレンダー内の開始日と終了日をクリックします。

   * 日付範囲内をクリックし、開始日と終了日を入力するか、カレンダー内で選択します。

     数値（M-D-YY から MM-DD-YYYY）や月名、略称（1 月や 1 月など）を入力できます。

### データ列の並べ替え

任意のデータ列を昇順（A から Z、または 1 から 10）または降順（Z から A、または 10 から 1）で並べ替えることができます。

* 列ヘッダーをクリックして、昇順と降順を切り替えます。


### データ行数の指定

ページの右下の「**[!UICONTROL Items per page]**」の横にある「*[!UICONTROL 25]*」、「*[!UICONTROL 50]*」、または「*[!UICONTROL 100]*」を選択します。

>[!MORELIKETHIS]
>
>* [Campaign Management ビューにおけるパフォーマンスレポートのタイプ ](campaign-reports-about.md)
>* [ プレースメントのサイト、広告、頻度の詳細の表示 ](placement-details-view.md)
>* [ 配置予測レポートの表示 ](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [ プレースメント診断レポートの表示 ](placement-diagnostics.md)
>* [Campaign Management ビューからのデータのエクスポート ](campaign-export-data.md)
>* [ ビデオ：DSP アカウント構造とユーザーインターフェイス ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
