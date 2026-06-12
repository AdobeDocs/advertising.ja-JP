---
title: キャンペーンデータビューの管理
description: キャンペーン、パッケージ、プレースメント、広告のデータビューをカスタマイズする方法について説明します。
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
TQID: https://experienceleague.adobe.com/iHIvQ5-7AJxfvMb5g3VlNfWkIR7a6ZwdvQtDKczrDw8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: f784309e-91ce-4bb5-ade4-5cbbceabecc0
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 927
ht-degree: 0%

---

# キャンペーンデータビューの管理

キャンペーン管理ビュー（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads]）に表示されるデータをカスタマイズできます。

## データビジュアライゼーションの管理 {#data-visualizations-manage}

キャンペーン全体または単一のキャンペーンのすべてのデータビジュアライゼーションの指標とチャートモードを変更できます。 単一のキャンペーンへの変更は、[!UICONTROL Packages]、[!UICONTROL Placements]、[!UICONTROL Ads]のビューを含む、キャンペーンのすべてのデータビジュアライゼーションに適用されます。

### データビジュアライゼーションの指標の変更

1. データビジュアライゼーションの右上にある「![設定](/help/dsp/assets/settings-chart.png)」をクリックします。

1. 指標を選択します。

   同じ指標を2回選択することはできません。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。

### データビジュアライゼーションの表示モードの変更

* データビジュアライゼーションの右上にある[!UICONTROL Overlay] スイッチ （![ オーバーレイスイッチ ](/help/dsp/assets/overlay.png)）をクリックして、オーバーレイモード （すべてのチャートがオーバーレイされている）とトレリスチャートモード （3つの個別のチャート）を切り替えます。

## データテーブルの管理 {#data-tables-manage}

すべてのキャンペーン管理ビュー（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]、および[!UICONTROL Ads]）で、データテーブル内に表示されるデータをカスタマイズできます。

### 列ビューの管理 {#column-views-manage}

各キャンペーン管理レベル （[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements]、および[!UICONTROL Ads]）には、そのエンティティの関連指標を含む組み込みの[!UICONTROL Pacing]および[!UICONTROL Performance] ビューが含まれています。 デフォルトでは、[!UICONTROL Pacing] ビューが表示されるので、パフォーマンスの低いキャンペーンやキャンペーンコンポーネントを一目で特定できます。 必要に応じて、カスタム列セットを作成および編集できます。

![列ビューセレクター](/help/dsp/assets/column-view-selector.png)

DSPでは、最新のビューがデフォルトのビューとして保存されるため、ページに戻るたびに、自分に関連する指標を常に表示できます。

#### 列表示の変更 {#column-view-change}

* 表示セレクターで、![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、目的の列表示の名前をクリックします。

#### カスタム列ビューの作成 {#column-view-create}

1. 表示セレクターで、![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、**[!UICONTROL Create View]**&#x200B;をクリックします。

1. ビューに含める指標を指定します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスをオンにします。

      すべての指標は、カテゴリ別にアルファベット順です：[!UICONTROL Settings]、[!UICONTROL Spend]、[!UICONTROL Pacing]、[!UICONTROL Reporting] （DSPが追跡する標準の指標）、[!UICONTROL Viewability]、および[!UICONTROL Conversions]。 「（[!UICONTROL Lifetime]）」が付いた指標は、ページで選択した日付範囲に関係なく、キャンペーンの開始時の値を返します。

   1. 右側のパネルで列名をクリックし、必要な位置にドラッグすることで、必要に応じて列の順序を編集できます。

   一部の列は固定された位置にあり、移動または削除できません。

1. 設定を適用または保存します。

   * 設定をビューに保存せずに一時的に適用するには、**[!UICONTROL Apply]をクリックします。**

   * 設定を新しいカスタム列ビューに保存するには、**[!UICONTROL Save As]**&#x200B;をクリックします。 [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

#### 列表示の編集 {#column-view-edit}

>[!NOTE]
>
>標準（定義済み）列ビューに変更を保存することはできませんが、変更を一時的に適用したり、新しいカスタムビューに保存したりすることはできます。

1. 表示セレクターで、![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、既存の列ビュー名をクリックします。

1. 表示セレクターで、![下向き矢印](/help/dsp/assets/chevron-down.png)をクリックし、**[!UICONTROL Edit View]**&#x200B;をクリックします。

1. ビューに含める指標を編集します。

   1. 使用可能な指標のリストで、含める各指標の横にあるチェックボックスを選択し、除外する各指標の横にあるチェックボックスをオフにします。

      すべての指標は、カテゴリ別にアルファベット順です：[!UICONTROL Settings]、[!UICONTROL Spend]、[!UICONTROL Pacing]、[!UICONTROL Reporting] （DSPが追跡する標準の指標）、[!UICONTROL Viewability]、および[!UICONTROL Conversions]。 「（[!UICONTROL Lifetime]）」が付いた指標は、ページで選択した日付範囲に関係なく、キャンペーンの開始時の値を返します。

   1. 右側のパネルで列名をクリックし、必要な位置にドラッグすることで、必要に応じて列の順序を編集できます。

   一部の列は固定された位置にあり、移動または削除できません。

1. 設定を適用または保存します。

   * （カスタムビューのみ）設定を保存するには、**[!UICONTROL Save]**&#x200B;をクリックします。

   * 設定をビューに保存せずに一時的に適用するには、**[!UICONTROL Apply]をクリックします。**

   * 設定を新しいカスタム列ビューに保存するには、**[!UICONTROL Save As]**&#x200B;をクリックします。 [!UICONTROL Save View] ウィンドウで、新しいビューの名前を入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

### キャンペーンデータのフィルタリング {#filter-data-tables}

フィルターは、現在のタブに表示されるデータを変更します。 利用できるフィルターはエンティティのタイプによって異なりますが、エンティティ名、ステータス、追加のプロパティ列が含まれる場合があります。

1. メインツールバーで、![ フィルターボタン ](/help/dsp/assets/filter.png)をクリックします。
1. 適用する各フィルターについて、左側の列のフィルター名をクリックし、フィルター値を指定します。
1. **[!UICONTROL Apply]**&#x200B;をクリックします。

#### 利用可能なフィルター

次のフィルターは、[!UICONTROL Campaigns]、[!UICONTROL Packages]、および[!UICONTROL Placements] ビューで使用できます。

* [!UICONTROL Campaigns]表示フィルター：
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages]表示フィルター：
   * [!UICONTROL Custom flights] （それらが存在するかどうかに関係なく）
   * [!UICONTROL Custom goal] （該当する場合）
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements]表示フィルター：
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] （該当する場合）
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] （[!UICONTROL less than]、[!UICONTROL greater than]、または[!UICONTROL equal to]を指定した値）
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] （[!UICONTROL impressions]または[!UICONTROL spend]）
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads]表示フィルター：
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### 日付範囲の変更

任意のデータテーブルの上にある日付範囲セレクターを使用して、すべての標準ビューとカスタムビューで使用される日付範囲を変更します。

![日付範囲セレクター](/help/dsp/assets/date-range-selector.png "日付範囲セレクター")

* プリセット範囲の場合：共通の時間増分のリストから選択します。 デフォルトは[!UICONTROL Last 30 days]*です。

* 特定の範囲の場合は、次のいずれかの操作を行います。

   * ![ カレンダー](/help/dsp/assets/calendar.png " カレンダー")をクリックし、カレンダー内の開始日と終了日をクリックします。

   * 日付範囲内をクリックし、開始日と終了日を入力するか、カレンダー内で選択します。

     数値（M-D-YYからMM-DD-YYYYまで）および/または月名または省略形（1月または1月など）を入力できます。

### データ列の並べ替え

任意のデータ列を昇順（A ～ Z、または1 ～ 10）または降順（Z ～ A、または10 ～ 1）で並べ替えることができます。

* 列ヘッダーをクリックして、昇順と降順を切り替えます。


### データ行数の指定

任意のページの右下の&#x200B;**[!UICONTROL Items per page]**&#x200B;の横にある「*[!UICONTROL 25]*」、「*[!UICONTROL 50]*」または「*[!UICONTROL 100]*」を選択します。

>[!MORELIKETHIS]
>
>* [ キャンペーン管理ビューのパフォーマンスレポートの種類](campaign-reports-about.md)
>* [ プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [ プレースメント予測レポートを表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [ プレースメント診断レポートを表示](placement-diagnostics.md)
>* [ キャンペーン管理ビューからデータをエクスポート ](campaign-export-data.md)
>* [ ビデオ：DSP アカウント構造とユーザーインターフェイス ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
