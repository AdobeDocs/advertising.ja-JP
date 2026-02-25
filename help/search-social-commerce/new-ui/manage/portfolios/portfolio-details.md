---
title: （新しい UI） ポートフォリオ パフォーマンスの詳細の表示
description: ポートフォリオレベルおよび割り当てられた各キャンペーンでの実際の指標と予測された指標を含め、ポートフォリオパフォーマンスの詳細を表示する方法を説明します。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: e786ffc8c9e331fffcc8b0f7cce4cb082baea6ac
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# （新しい UI）ポートフォリオのパフォーマンスの詳細を表示

*Beta機能*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

ポートフォリオ詳細表示には、ポートフォリオに関する次の情報が含まれます。

* 最大 3 つのパフォーマンス指標の実際の値と予測値。 レポートには、ポートフォリオの合計指標値と日付別の指標の分類が含まれます。<!-- Not for active portfolios only?  -->

* モデルが予測からどれだけ乖離したかを示す、アクティブなポートフォリオのモデル精度データ。 このレポートには、1 日または 7 日周期の全体的なコスト精度、クリック精度および目標値の精度が表示されます。

  データは、クリック日（デフォルト）またはトランザクション日で表示できます。   また、トレンドグラフ（デフォルト）またはテーブルとしてデータを表示することもできます。

* アクティブなポートフォリオのターゲット支出と実際の支出の比較。 オプションで、ポートフォリオのキャンペーン予算合計を含めることもできます。

* 広告ネットワークによるアクティブなポートフォリオのコスト、クリックまたは [ 目標値 ](/help/search-social-commerce/glossary.md#o-p) 予測の精度。<!-- Verify -->

* ポートフォリオ設定。

  オプションで、ポートフォリオ設定を開いて編集することもできます。

## ポートフォリオのパフォーマンスの詳細を開く

1. メインメニューで、**[!UICONTROL Manage]/[!UICONTROL Portfolios]** をクリックします。

1. ポートフォリオ名をクリックします。

1. （オプション） **[!UICONTROL Granularity]** のメニューから、データの精度を *[!UICONTROL Daily]、*、*[!UICONTROL Weekly]、* または *[!UICONTROL Monthly]から変更します。*

1. （オプション）ポートフォリオ詳細の日付範囲を変更するには、右上の日付範囲をクリックし、日付範囲を指定して、「**[!UICONTROL Apply]** 開」をクリックします。

## 「[!UICONTROL Portfolio Overview]」タブのカスタマイズ

* （オプション） [!UICONTROL Portfolio Performance] のレポートをカスタマイズするには、次のいずれかの操作を行います。

   * 合計指標と詳細指標の両方に使用されるパフォーマンス指標を変更するには、「**[!UICONTROL Metrics]**」をクリックし、最大 3 つの指標を選択します。

     デフォルトの指標は、*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*、*[!UICONTROL Objective Value]* です。<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * 詳細な指標については、以下を参照してください。

      * **[!UICONTROL Display predictions]** の横にあるスイッチを動かして、予測された指標値の表示/非表示を切り替えます。

      * グラフ表示（![ グラフ表示 ](/help/search-social-commerce/assets/chart-view.png " グラフ表示 ")）とテーブル表示（![テーブル表示](/help/search-social-commerce/assets/table-view.png "テーブル表示")）を切り替えます。

      * （グラフ表示）グラフ上の任意のポイントのデータを表示するには、そのポイントにカーソルを置きます。

* （オプション） [!UICONTROL Model accuracy] のトレンドグラフをカスタマイズするには、次のいずれかの操作を行います。

   * グラフ表示（![ グラフ表示 ](/help/search-social-commerce/assets/chart-view.png " グラフ表示 ")）とテーブル表示（![テーブル表示](/help/search-social-commerce/assets/table-view.png "テーブル表示")）を切り替えます。

   * *[!UICONTROL Click Date]* と *[!UICONTROL Transaction Date]* でデータ表示を切り替えます。

   * *[!UICONTROL Daily Accuracy]* と *[!UICONTROL 7 Day Rolling Accuracy]* に関するデータの表示を切り替えます。

     [!UICONTROL 7 Day Rolling Accuracy] は、過去 7 日間の予測の平均精度をパーセントで表したものです。 例えば、2025 年 5 月 8 日の値は、2025 年 5 月 1 日から 5 月 7 日までの期間の平均精度です。

   * （グラフ表示）グラフ上の任意のポイントのデータを表示するには、そのポイントにカーソルを置きます。

* （オプション） [!UICONTROL Target vs actual spend] のトレンドグラフをカスタマイズするには、次のいずれかの操作を行います。

   * **[!UICONTROL Display budget]** の横にあるスイッチを動かして、各日付のキャンペーン予算合計の表示/非表示を切り替えます。

   * グラフ上の任意のポイントのデータを表示するには、そのポイントの上にカーソルを置きます。

* （オプション） [!UICONTROL Network Accuracy] のトレンドグラフをカスタマイズするには、次のいずれかの操作を行います。

   * レポートされた指標を *[!UICONTROL Cost]*、*[!UICONTROL Clicks]* または *[!UICONTROL Objective Value]* に変更します。

   * グラフ上の任意のポイントのデータを表示するには、そのポイントの上にカーソルを置きます。

1. 「**[!UICONTROL Download report]**」をクリックします。

## ポートフォリオ内のキャンペーンのリスト

* 「**[!UICONTROL Campaigns]**」タブをクリックします。

## ポートフォリオの広告グループのリスト

* ポートフォリオ内のキャンペーンのすべての広告グループを表示するには、[**[!UICONTROL Campaigns]**] タブをクリックし、キャンペーン名をクリックします。

## ポートフォリオ内のキーワードのリスト

* ポートフォリオ内のすべてのキーワードを表示するには、「**[!UICONTROL Keywords]**」タブをクリックします。

* ポートフォリオ内の広告グループ内のすべてのキーワードを表示するには、[**[!UICONTROL Ad Groups]**] タブをクリックし、広告グループ名をクリックします。

## ポートフォリオ設定の表示と編集

* ポートフォリオ設定を表示または非表示にするには、[**[!UICONTROL Portfolio Settings]**] をクリックします。

   * 表示可能なポートフォリオ設定を編集するには、「設定」セクションの横にある ![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ") をクリックし、[ ポートフォリオ設定を編集 ](portfolio-edit.md) をクリックします。

ポートフォリオ設定について詳しくは、最適化ガイドを参照してください。このガイドは、検索、ソーシャル、Commerce内から利用できます。

## ポートフォリオ コンポーネントのポートフォリオ パフォーマンス レポートおよびリストをダウンロードします

* すべてのレポートをダウンロードするには：

   1. ツールバーの「**[!UICONTROL Download report]**」をクリックします。

   1. 組み込む各パフォーマンスレポートとポートフォリオコンポーネントタイプの横にあるチェックボックスをオンにします。

      一部のパフォーマンスレポートでは、データをグラフとテーブルのどちらでダウンロードするかを選択できます。

   1. 「**[!UICONTROL Download report]**」をクリックします。

* 特定のタイプのデータを含む [!DNL model accuracy] レポートをダウンロードするには：

   1. レポートのツールバーで、[**[!UICONTROL Download report]**] をクリックします。

   1. 含めるデータの各タイプの横にあるチェック ボックスをオンにし、データの分類方法（入札単位またはクリック量を使用）を選択します。

   1. 「**[!UICONTROL Download report]**」をクリックします。

>[!MORELIKETHIS]
>
>* ポートフォリオに関する [ （新しい UI） ](portfolio-about.md)
>* [ （新しい UI）ポートフォリオの編集 ](portfolio-edit.md)
>* [ （新しい UI） [!UICONTROL Portfolios] ビューでのデータのダウンロード ](portfolio-view-report.md)
