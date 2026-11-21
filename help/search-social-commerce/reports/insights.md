---
title: （新しいUI）Advertising インサイト
description: モデルの精度、パフォーマンス、シミュレーション、予算上限、コンバージョンに関するAdvertising insight ダッシュボードの設定および表示方法について説明します。
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# （新しいUI）Advertising インサイト

Advertisingのインサイトにより、視覚的かつ実用的なデータを取得して、ポートフォリオのパフォーマンスを評価したり、最適化の課題を特定したり、コンバージョンデータを比較したりできます。 各insightはオンデマンドで生成され、画面上のダッシュボードとして表示されます。

**[!UICONTROL Reports]>[!UICONTROL Insights]** ビューには、**[!UICONTROL Dashboards]**&#x200B;の下に使用可能なインサイトが表示されます。 ページ見出しは&#x200B;**[!UICONTROL Advertising Insights]**&#x200B;です。

>[!NOTE]
>
>このページでは、ベータ版の新しいユーザーインターフェイスにおけるinsight ダッシュボードについて説明します。 可用性は、アクセス権と、選択した広告主が利用できるインサイトによって異なります。 [従来のAdvertising インサイト &#x200B;](/help/search-social-commerce/legacy-ui/advertising-insights/insight-about.md)には、生成されたファイルの分析と手順の異なるセットが含まれています。

## インサイトの種類 {#insight-types}

| Insight | 説明 |
| --- | --- |
| [!UICONTROL Model Accuracy] | Search, Social, &amp; Commerceが、ポートフォリオのコストと売上をどの程度予測するかを特定します。 モデルの精度は、ポートフォリオ、広告ネットワーク、キャンペーンの各レベルで確認できます。 |
| [!UICONTROL Performance Insights] | 最適化ステータスの変更、目的の変更、または指定された日付の前後のポートフォリオパフォーマンスを比較します。 ダッシュボードには、パフォーマンスの概要、最適化に影響を与える変更の監査、キャンペーンの比較、トレンド、客観的な価値分析が含まれます。 |
| [!UICONTROL Portfolio Simulation Analysis] | 既存のカスタムシミュレーションと実際のパフォーマンスを比較します。 ポートフォリオと施策のデータを確認し、シミュレーションの精度を分析し、さまざまなターゲット支出レベルで予測されるパフォーマンスを調査することができます。 |
| [!UICONTROL Campaign Budget Cap Analysis] | ポートフォリオの支出がキャンペーン予算上限によって制限されたかどうかを示します。 このダッシュボードには、上限を設定した費用、影響を受けるキャンペーン、失われたインプレッション数の予測、日々のトレンドや週のトレンド、ポートフォリオ設定に関するレコメンデーションなどが含まれています。 |
| [!UICONTROL Modeled Conversions] | Adobeのコンバージョン値と、モデルデータを含むアドネットワークによって報告された値を比較します。 アカウント、ポートフォリオ、またはキャンペーンを分析し、Adobeで測定された値とAdobeで測定およびモデル化された値の両方を、パブリッシャーが報告した値と比較できます。 |
| [!UICONTROL Delayed Revenue Analysis] | コンバージョンの遅延（広告のクリックやビュースルーから、その後のコンバージョンに至るまでの時間）を測定し、それが目標値、投資収益率（ROI）、モデルの精度に与える影響を示します。 分析は、クリックベースまたはビュースルーの収益アトリビューションを持つポートフォリオでのみ使用できます。 |

## Insightの生成 {#insight-generate}

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Insights]**&#x200B;をクリックします。

1. 生成するinsightをクリックします。

1. **[!UICONTROL Configure]** パネルで、[insight設定](#insight-settings)を指定します。

1. **[!UICONTROL Generate Insight]**&#x200B;をクリックします。

   設定パネルが閉じ、ダッシュボードに分析が表示されます。

1. [insightの結果](#insight-results)を確認します。

設定を変更するには、**[!UICONTROL Configure]**&#x200B;をクリックし、値を変更して、**[!UICONTROL Generate Insight]**&#x200B;をもう一度クリックします。 Insight リストに戻るには、パンくずリストの&#x200B;**[!UICONTROL Analysis List]**&#x200B;をクリックします。

## Insightの設定 {#insight-settings}

### モデルの精度 {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** 1つのポートフォリオを選択してください。

* **[!UICONTROL Choose Revenue Type]:** **[!UICONTROL Actual Revenue]** （デフォルト）または&#x200B;**[!UICONTROL Delayed Revenue]**&#x200B;を選択します。

* **[!UICONTROL Date Range]:**&#x200B;分析する日付を選択します。 [日付範囲設定](#date-range-settings)を参照してください。

### パフォーマンスインサイト {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** 1つのポートフォリオを選択してください。

* **[!UICONTROL Revenue Type]:** **[!UICONTROL Actual Revenue]** （デフォルト）または&#x200B;**[!UICONTROL Delayed Revenue]**&#x200B;を選択します。

* **イベント日：** パフォーマンスを比較する日付のタイプを選択します：

  * **[!UICONTROL Optimization Status Change (last 90 days)]** （デフォルト）: ポートフォリオで使用可能な最適化ステータス変更日を選択します。

  * **[!UICONTROL Objective Change Date (last 90 days)]:** ポートフォリオで使用可能な目標の変更日を選択します。

  * **[!UICONTROL Specific Date]:**&#x200B;日付選択ツールを使用して日付を指定します。

  比較期間を設定する前に、イベント日を選択します。 選択したポートフォリオにイベント日がない場合は、**[!UICONTROL Specific Date]**&#x200B;を使用できます。

* **[!UICONTROL Pre Days]:** イベント日より前の期間を指定します：

  * **[!UICONTROL 7]** （デフォルト）、**[!UICONTROL 14]**、または&#x200B;**[!UICONTROL 30]**&#x200B;を選択します。

  * **[!UICONTROL Pre Start Date]**&#x200B;を選択し、**[!UICONTROL Custom Pre Date]**&#x200B;を指定します。

  * **[!UICONTROL Custom Pre Days]**&#x200B;を選択し、正の日数を入力してください。

* **[!UICONTROL Post Days]:** イベント日の後の期間を指定します：

  * **[!UICONTROL 7]** （デフォルト）、**[!UICONTROL 14]**、または&#x200B;**[!UICONTROL 30]**&#x200B;を選択します。

  * **[!UICONTROL Post End Date]**&#x200B;を選択し、**[!UICONTROL Custom Post Date]**&#x200B;を指定します。

  * **[!UICONTROL Custom Post Days]**&#x200B;を選択し、正の日数を入力してください。

  イベント日付自体は、どちらの比較期間にも含まれていません。

* **[!UICONTROL Date Exclusion]:** （オプション）分析から日付を除外：

  1. **[!UICONTROL Select Dates]**&#x200B;をクリックします。

  1. 除外する日付を選択：

     * 個々の日付をクリックして選択または選択解除します。

     * クリック中に&#x200B;**[!UICONTROL Shift]**&#x200B;を押しながら範囲を選択します。

     * すべての除外を削除するには、**[!UICONTROL Clear All]**&#x200B;をクリックします。

  1. 完了したら、**[!UICONTROL Done]**&#x200B;をクリックします。

### Portfolio Simulation Analysis {#simulation-settings}

* **[!UICONTROL Portfolios]:**&#x200B;既存のカスタムシミュレーションを持つポートフォリオを1つ選択します。

* **[!UICONTROL Simulation Date]:**&#x200B;分析するシミュレーションの日付を選択します。 その日付に複数のシミュレーションが使用可能な場合は、名前でシミュレーションも選択します。

  使用できるカスタムシミュレーションがない場合は、このinsightを使用する前に[&#x200B; カスタムシミュレーションを生成](/help/search-social-commerce/manage/portfolios/portfolio-create-simulation.md)します。

* **[!UICONTROL Actual Days]:**&#x200B;実際のパフォーマンスデータの&#x200B;**[!UICONTROL 7]** （デフォルト）、**[!UICONTROL 14]**、または&#x200B;**[!UICONTROL 30]**&#x200B;日間を選択します。 別の数値を指定するには、**[!UICONTROL Enter Actual Days]**&#x200B;を選択し、1 ～ 90の値を入力します。

* **[!UICONTROL Type]:** コンバージョンアトリビューション用に&#x200B;**[!UICONTROL Transaction Date]** （デフォルト）または&#x200B;**[!UICONTROL Click Date]**&#x200B;を選択します。

### キャンペーン予算上限分析 {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** 1つのポートフォリオを選択してください。

* **[!UICONTROL Date Range]:**&#x200B;分析する日付を選択します。 [日付範囲設定](#date-range-settings)を参照してください。

### モデルコンバージョン {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** **[!UICONTROL Account]**、**[!UICONTROL Portfolio]** （デフォルト）、または&#x200B;**[!UICONTROL Campaign]**&#x200B;を選択します。

* **[!UICONTROL Accounts]**、**[!UICONTROL Portfolios]**、または&#x200B;**[!UICONTROL Campaigns]:**&#x200B;分析レベルに該当するエンティティを選択します。 複数のエンティティを選択できます。

* **[!UICONTROL Date Range]:**&#x200B;分析する日付を選択します。 [日付範囲設定](#date-range-settings)を参照してください。

* **[!UICONTROL Adobe Conversion]:**&#x200B;比較するAdobe コンバージョンプロパティを選択します。

* **[!UICONTROL Publisher Conversion]:**&#x200B;比較するパブリッシャー変換プロパティを選択します。

  使用可能なコンバージョンプロパティは、分析レベル、選択したエンティティ、日付範囲によって異なります。 比較には両方の変換プロパティが必要です。

### 収益分析の遅延 {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** クリックベースまたはビュースルーの収益アトリビューションを含むポートフォリオを1つ選択します。

* **[!UICONTROL Date Range]:**&#x200B;分析する日付を選択します。 [日付範囲設定](#date-range-settings)を参照してください。

### 日付範囲の設定 {#date-range-settings}

**[!UICONTROL Date Range]**&#x200B;設定のインサイトの場合は、**[!UICONTROL Last 7 days]** （デフォルト）、**[!UICONTROL Last 14 days]**、または&#x200B;**[!UICONTROL Last 30 days]**&#x200B;を選択します。

別の期間を指定するには、**[!UICONTROL Custom Date]**&#x200B;を選択し、**[!UICONTROL Start Date]**&#x200B;と&#x200B;**[!UICONTROL End Date]**&#x200B;を入力します。 現在の日付から過去90日以内の日付を選択できます。

## Insightの結果を見る {#insight-results}

### モデルの精度 {#model-accuracy-results}

ポートフォリオの詳細を確認し、次のタブを使用します。

* **[!UICONTROL Portfolio]:** ポートフォリオレベルのモデルの精度と予算比較を確認します。

* **[!UICONTROL Ad Network]:** モデルの正確性と予算の比較を広告ネットワーク別に確認します。

* **[!UICONTROL Campaigns]:** キャンペーンレベルのモデルの正確性と目標と実際のパフォーマンスの比較を確認します。

* **[!UICONTROL Playground Beta]:**&#x200B;複数のキャンペーンのモデルの精度を比較します。

キャンペーンの精度チャートの場合は、**[!UICONTROL Comparison Options]**&#x200B;と&#x200B;**[!UICONTROL Campaign]**&#x200B;を選択します。 **[!UICONTROL Playground Beta]**&#x200B;では、複数のキャンペーンを選択できます。 **[!UICONTROL Table View]**&#x200B;をクリックして、グラフとその基になるデータを切り替えます。

### パフォーマンスインサイト {#performance-insights-results}

ダッシュボードには、**[!UICONTROL Pre Period]**&#x200B;と&#x200B;**[!UICONTROL Post Period]**、両方の期間の集計パフォーマンス指標、およびポートフォリオの詳細が表示されます。

**[!UICONTROL Audit Trail]**&#x200B;は、ポートフォリオ予算、支出戦略、最小キャンペーン支出、および支出制限の複数など、最適化に影響を与える要因の変更を要約します。 変更内容の詳細が使用可能な場合は、**[!UICONTROL View Details]**&#x200B;をクリックして確認します。

**[!UICONTROL Comparative Overview]**、**[!UICONTROL Campaigns Comparison]**、**[!UICONTROL Trends & Patterns]**、**[!UICONTROL Deep Analysis]**、**[!UICONTROL Objective Value And Analysis]**&#x200B;のタブを使用して、比較を調べます。

### Portfolio Simulation Analysis {#simulation-results}

シミュレーションの詳細を確認し、次のタブを使用します。

* **[!UICONTROL Portfolio]:** ポートフォリオレベルのシミュレーションデータを確認します。 このタブ内：

  * **[!UICONTROL Simulation Data]**&#x200B;は、シミュレーション指標とターゲット支出のパフォーマンスを示しています。

  * **[!UICONTROL Simulation Vs Actual]**&#x200B;は、シミュレートされたパフォーマンスと実際のパフォーマンスを比較します。

  * **[!UICONTROL Try New Target]**&#x200B;を使用すると、**[!UICONTROL Explore Target Spend]**&#x200B;にターゲット支出を入力して、クリック数、コスト、収益の見積もりを表示できます。 これはパフォーマンスの予測を分析したものであり、ポートフォリオの支出目標は変わりません。

* **[!UICONTROL Campaigns]:** キャンペーンレベルのシミュレーション比較を確認します。

* **[!UICONTROL Accuracy Analysis]:** シミュレーションの精度を確認します。

### キャンペーン予算上限分析 {#budget-cap-results}

ポートフォリオの詳細と概要指標を確認します。

* **[!UICONTROL Total Capped Spend]:** キャンペーン予算がヒットした日の支出の割合。

* **[!UICONTROL Capped Campaigns]:**&#x200B;少なくとも1回は予算にヒットしたキャンペーンの数。

* 予算上限が原因で、**[!UICONTROL Est. Lost Impressions]:**&#x200B;推定インプレッションが欠落しました。

* **[!UICONTROL Peak Capping Day]:**&#x200B;最も上限のある支出を含む曜日。

**[!UICONTROL Spend on Capped Campaigns by Day]**&#x200B;と&#x200B;**[!UICONTROL Capped Spend by Weekday]**&#x200B;のグラフにキャッピングトレンドが表示されます。 キャンペーンの詳細については&#x200B;**[!UICONTROL Capped Campaign Performance]**&#x200B;を、提案された設定の変更については&#x200B;**[!UICONTROL Portfolio Settings Recommendations]**&#x200B;を確認してください。

### モデルコンバージョン {#modeled-conversions-results}

選択したエンティティと日付範囲について、次の表を確認します。

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** Adobeによって直接測定されたコンバージョン値と、測定データとモデル化データを含むパブリッシャーから報告された値を比較します。

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** Adobeで測定およびモデル化されたコンバージョン値と、発行者が報告した値を比較します。

両方のテーブルには、エンティティ名とID、Adobe値、発行者が報告した値、絶対差、パーセンテージ差が含まれます。

使用可能なデータがない場合は、コンバージョンプロパティと、選択したエンティティと日付範囲の両方にデータが存在することを確認します。

### 収益分析の遅延 {#delayed-revenue-results}

**[!UICONTROL Key Insights Summary]**&#x200B;には、予測される重み付けされた収益（「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれます）、ROI、およびモデルの精度に関する情報が表示されます。

**[!UICONTROL Conversion Lag Breakdown by Revenue Property]** セクションには、各収益プロパティについて、0日目、3、7、14および28日目に実現されたコンバージョンの割合が表示されます。

**[!UICONTROL Performance Over Time]**&#x200B;で、**[!UICONTROL Objective Value]**、**[!UICONTROL ROI]**&#x200B;または&#x200B;**[!UICONTROL Model Accuracy]**&#x200B;を選択して、クリック日、トランザクション日、期待されるパフォーマンスを比較します。 **[!UICONTROL Table View]**&#x200B;をクリックして、グラフとその基になるデータを切り替えます。

**[!UICONTROL Metrics Definitions]**&#x200B;で、分析で使用される日付と指標の説明については&#x200B;**[!UICONTROL Show]**&#x200B;をクリックし、それらを折りたたむには&#x200B;**[!UICONTROL Hide]**&#x200B;をクリックします。

分析が適用できない場合は、クリックベースまたはビュースルーの収益アトリビューションが設定されているポートフォリオを選択します。 使用可能なデータがない場合は、選択したポートフォリオと日付範囲にデータが存在することを確認します。
