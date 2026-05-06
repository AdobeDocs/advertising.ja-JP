---
title: '[!UICONTROL Spend Planner]の使用'
description: ポートフォリオ全体で最適な支出配分を実現するために、ポートフォリオの予算レコメンデーションを生成、ダウンロード、適用する方法について説明します。
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: c3664a71f39c9a45fad739fdf4805c9862c69915
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 0%

---

# [!UICONTROL Spend Planner]の使用

[!UICONTROL Spend Planner] （従来のユーザーインターフェイスでは「[!UICONTROL Spend Recommendation Tool]」と呼ばれます）は、最適化されたポートフォリオとアクティブなポートフォリオ間の最適な支出配分を同じ目的と通貨で特定するため、ポートフォリオセットの収益または目標目標を最大化できます。

日別予算を持つポートフォリオの予算予算推奨レポートを表示する場合、任意のポートフォリオの予算を推奨予算に変更できます。

## [!UICONTROL Spend Planner] レポートのデータ

目標[!UICONTROL Maximize Clicks]を持つポートフォリオの場合、レポートには支出の推奨事項とクリックの予測が含まれます。 その他の目標については、このレポートには支出のレコメンデーションと売上予測が含まれています。

支出推奨レポートには、次のデータが含まれます。

* 散布線グラフは、個々の支出目標が最適に設定されている場合に、ポートフォリオセットの特定の総コストで達成できる予測される最大収益またはクリック数を示します。 各収益ポイントまたはクリックポイントの予測コストが含まれます。

* 2つのドーナツチャートは、現在の支出目標1\）と提案された支出目標2\）に対する支出と予想される収益またはポートフォリオによるクリック分布を示しています。

* 選択したすべてのポートフォリオで現在の1日の総支出目標を維持する場合、または提案された総支出目標の場合に、推奨される1日の支出（コスト）と予測される収益分布またはクリック分布を示す、各ポートフォリオの棒グラフ。 必要に応じて、選択したポートフォリオに推奨される支出目標を適用できます。これは、次の入札実行サイクルでの入札に影響します。

## 使用可能なアクション

* [新しいUI](#spend-recommendations-generate)または[従来のUI](#spend-recommendations-generate-legacy)から[!UICONTROL Spend Planner] レポートを生成します

* [対応するポートフォリオに予算の推奨事項](#spend-recommendations-apply)を適用します。

* [予算推奨レポートデータをファイルに開くか、保存します](#spend-recommendations-download)

## （新しいUI） [!UICONTROL Spend Planner] レポートの生成 {#spend-recommendations-generate}

1. 次のいずれかの操作を行います。

   * メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Spend Planner]**&#x200B;をクリックします。

   * メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。 データテーブルの上にあるツールバーで、![費用プランナー](/help/search-social-commerce/assets/spend-planner-icon.png "費用プランナー")をクリックします。

   [!UICONTROL Spend Recommendation] ツールが従来のユーザーインターフェイスで開きます。

1. 選択したポートフォリオの現在の結合された予算を使用してデータを表示します。

   1. ポートフォリオ目標を選択します。

   1. 通貨を選択します。

   1. （オプション）ポートフォリオ支出戦略を選択して、ポートフォリオリストをさらにフィルタリングします。

   1. 含める各ポートフォリオの横にあるチェックボックスをオンにします。 すべてのポートフォリオを選択するには、[!UICONTROL Portfolios]の横にあるチェックボックスをオンにします。

      選択したパラメーターを持つ最適化されたアクティブなポートフォリオのみが一覧表示されます。

   1. **[!UICONTROL Update]**&#x200B;をクリックします。

   1. （オプション）グラフ上の任意のポイントのコストと収益を表示するには、ポイントの上にカーソルを置きます。

1. （オプション）異なる総支出目標を使用して、ポートフォリオごとに推奨される日別支出目標と予想収益を表示するには、[!UICONTROL Total Spend Target] フィールドにすべてのポートフォリオにわたって提案された日別支出目標を入力します。 次に、**Enter** キーを押します。

   予算分配のレコメンデーションツールは、毎週のシミュレーションのデータを使用するため、推奨される予算合計は、提案された予算目標と最も近い予算配分となり、理想的な予算配分の組み合わせとなります。

<!--

New UI; validate post-Update steps once I get it to generate a report:

## Generate a spend recommendation report {#spend-recommendations-generate}

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Spend Planner]**.

1. View data using the current, combined budgets for the selected portfolios:

   1. Click **[!UICONTROL Select Objective]**.

   1. Select the portfolio objective.

   1. Select the currency.

   1. (Optional) Select a portfolio spend strategy to further filter the portfolios list.

   1. Select the check box next to each portfolio to include.

      Only optimized and active portfolios with the selected parameters are listed.

   1. Click **[!UICONTROL Update]**.

   1. (Optional) To see the cost and revenue for any point on the chart, hold the cursor over the point.

1. (Optional) To download the proposed allocation and expected revenue per portfolio, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download") next to [!UICONTROL Portfolio Allocation] in the right column.

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

1. (Optional) To view the recommended daily spend and expected revenue for each of the portfolios using a different total spend target, enter a proposed total daily spend target across all portfolios in the [!UICONTROL Total Spend Target] field. Then press the **Enter** key.

   The spend recommendation tool uses data from weekly simulations, so the total recommended spend is the closest match to your proposed spend target with the ideal spend mix.

-->

## （従来のUI） [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation] ビューから[!UICONTROL Spend Recommendation] レポートを生成 {#spend-recommendations-generate-legacy}

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**&#x200B;をクリックします。

1. 選択したポートフォリオの現在の結合された予算を使用してデータを表示します。

   1. ポートフォリオ目標を選択します。

   1. 通貨を選択します。

   1. （オプション）ポートフォリオ支出戦略を選択して、ポートフォリオリストをさらにフィルタリングします。

   1. 含める各ポートフォリオの横にあるチェックボックスをオンにします。 すべてのポートフォリオを選択するには、[!UICONTROL Portfolios]の横にあるチェックボックスをオンにします。

      選択したパラメーターを持つ最適化されたアクティブなポートフォリオのみが一覧表示されます。

   1. **[!UICONTROL Update]**&#x200B;をクリックします。

   1. （オプション）グラフ上の任意のポイントのコストと収益を表示するには、ポイントの上にカーソルを置きます。

1. （オプション）新しい総支出目標を使用して、ポートフォリオごとに推奨される1日の支出額と予測収益を表示するには、[!UICONTROL Total Spend Target] フィールドにすべてのポートフォリオで提案される1日の支出合計ターゲットを入力します。 次に、**Enter** キーを押します。

   予算分配のレコメンデーションツールは、毎週のシミュレーションのデータを使用するため、推奨される予算合計は、提案された予算目標と最も近い予算配分となり、理想的な予算配分の組み合わせとなります。

<!--
## (New UI) Apply spend recommendations {#spend-recommendations-apply}

*Portfolios with daily budgets only*

>[!NOTE]
>
>* If the applied changes will increase or decrease the spend target of any portfolio by more than 20%, you must approve the change.
>* When the spend target for a portfolio changes by more than 20%, Search, Social, & Commerce takes up to 3-4 days to adjust its models and achieve the new target.

1. [Generate a spend recommendation report](#spend-recommendations-generate) for one or more portfolios with daily budgets.

1. Select the check box next to each portfolio for which you want to apply the recommended spend target. To select all portfolios, select the check box next to **[!UICONTROL Select All Recommendations]**.

1. Click **[!UICONTROL Apply Selected Recommendations]**.

1. (If any of the budgets will change by more than 20%) In the confirmation message, click **[!UICONTROL Confirm]** to approve the changes.

-->

## <!--(Legacy UI) -->予算分配の推奨事項を適用 {#spend-recommendations-apply-legacy}

日別予算のみ&#x200B;*ポートフォリオ*

>[!NOTE]
>
>* 適用された変更により、任意のポートフォリオの支出目標が20%以上増加または減少する場合は、変更を承認する必要があります。
>* ポートフォリオの支出目標が20%以上変化した場合、Search, Social, &amp; Commerceは、モデルを調整し、新しい目標を達成するのに最大3～4日かかります。

1. [1日当たりの予算を持つ1つ以上のポートフォリオの予算予算推奨レポート ](#spend-recommendations-generate-legacy)を生成します。

1. 推奨される費用ターゲットを適用する各ポートフォリオの横にあるチェックボックスをオンにします。 すべてのポートフォリオを選択するには、**[!UICONTROL Select All Recommendations]**&#x200B;の横にあるチェックボックスをオンにします。

1. **[!UICONTROL Apply Selected Recommendations]**&#x200B;をクリックします。

1. （いずれかの予算が20%以上変更される場合）確認メッセージで「**[!UICONTROL Yes]**」をクリックして変更を承認します。

<!--

## (New UI) Open or save data as a [!DNL Microsoft Excel] workbook file {#spend-recommendations-download}

You can open or save data from either a) the line chart showing cost points and the expected revenue for each cost and b) the donut charts of the current and proposed media mix. [This seems to be identical to the Portfolio Allocation report -- how should these be different?]

1. [Generate a spend recommendation report](#spend-recommendations-generate) for selected portfolios.

1. Above the report, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download").

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

-->

<!--(Legacy UI) -->

## データを[!DNL Microsoft Excel] ワークブック ファイルとして開くか保存する {#spend-recommendations-download-legacy}

1. 選択したポートフォリオの予算推奨レポートを生成します。

1. レポートの右上にある「![ ダウンロード ](/help/search-social-commerce/assets/download-spend-recommendation.png " ダウンロード ")」をクリックします。

   ブラウザーの通常の手順に従って、ファイルを開くか保存します。 詳しくは、ブラウザーのオンラインヘルプを参照してください。
