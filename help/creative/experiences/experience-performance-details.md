---
title: エクスペリエンスレベルのパフォーマンスレポート
description: エクスペリエンスレベルのパフォーマンスレポートを表示する方法について説明します。
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 137f334eec778499f263e26c125e97ffe37d6112
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# エクスペリエンスレベルのパフォーマンスレポート

*クローズドベータ版*

任意のエクスペリエンスの詳細なパフォーマンスデータを表示できます。

## エクスペリエンスレベルのパフォーマンスレポートのデータ

レポート表示には、次のデータが含まれます。

* **概要** タブ：以下を含むエクスペリエンス全体のパフォーマンスの概要

   * **全体的なパフォーマンス** セクション：

   * **全体的なパフォーマンス**：合計インプレッション数、クリック数、クリックスルー率（CTR）、単一のコンバージョン指標に対するビュースルーコンバージョンおよびクリックスルーコンバージョン。<!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

   * **デフォルト率**: （決定ツリーのターゲット設定を使用したエクスペリエンスのみ）ターゲットクリエイティブ、ターゲットを設定していない汎用クリエイティブまたは「その他すべてのユーザー」をターゲットにした汎用クリエイティブおよびエクスペリエンスのデフォルトのクリエイティブによるインプレッション数。

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **パフォーマンスの分類** セクション：

      * **地域パフォーマンス：*：地理的な場所ごとの個々の指標。

        <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **デバイスのパフォーマンス：** デバイスタイプ、オペレーティングシステムおよびブラウザー別の個々の指標。 必要に応じて、任意のデバイスカテゴリの値をクリックして、その条件を満たす上位 <!-- NN --> 件のクリエイティブのリストを表示します。

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **クリエイティブパフォーマンス** タブ*: クリエイティブ、バンドルまたは広告タグ別のパフォーマンスの概要。以下に例を示します。

   * **クリエイティブ** サブタブ：エクスペリエンス内の各クリエイティブのインプレッション数、クリック数および CTR の合計 <!-- No breakdown yet for the individual ad elements and/or the served ads. -->。

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

   * **バンドル/タグ** サブタブ：エクスペリエンス内の個々のバンドル（デシジョンツリーターゲティングを使用したエクスペリエンス）または広告タグ（デシジョンツリーターゲティングを使用しないエクスペリエンス）のインプレッション数、クリック数および CTR の合計数。

     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## エクスペリエンスのパフォーマンスレポートの表示

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のエクスペリエンスを含めます。

1. エクスペリエンスを選択します。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Reports]**」をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Reports]** をクリックします。

   「[!UICONTROL Overview]」タブが開きます。

1. （オプション）右上のツールバーで、日付範囲、コンバージョンアトリビューションルール、すべてのパフォーマンスレポート内で報告されるコンバージョンを指定します。

   * （オプション）パフォーマンスデータの日付範囲を変更するには、日付メニューでオプションを選択します。

      * プリセットの期間を指定するには、レポート（*[!UICONTROL Last Month-to-date]、* *[!UICONTROL Last 7 days]、* *[!UICONTROL Last 30 days]、* *[!UICONTROL Last 7 days]、* *[!UICONTROL Last 30 days]、* *[!UICONTROL Today]、* または *[!UICONTROL Yesterday]*）を選択します。

      * カスタムの日付範囲を指定するには、開始日と終了日の <!-- in the format MM/DD/YYYY or M/D/YYYY,--> を指定するか、フィールドの横にある ![ カレンダーアイコン ](/help/search-social-commerce/assets/calendar.png) をクリックして、日付を選択します。

   * （任意）コンバージョンにつながる一連のイベント内のコンバージョンデータを属性化するためのルールを変更するには、![ 設定 ](/help/creative/assets/settings.png) をクリックして **[!UICONTROL Attribution Rule]** を変更します。

   * （オプション）レポートされたコンバージョンを変更するには、![ 設定 ](/help/creative/assets/settings.png) をクリックし、**[!UICONTROL Conversions]** メニューでコンバージョン名を選択します。&lt;!—1 つまたは複数のどちらですか。 これらの値の表示方法を確認する – 複数のコンバージョンが既に設定されている広告主を確認する必要があります – >

     使用可能なコンバージョン列には、検索、ソーシャル、Commerceのユーザーであるかどうかに関わらず、Advertising検索、ソーシャル、Commerceで使用可能なコンバージョンが含まれます。 これには、広告主が [ 統合 ](/help/integrations/analytics/overview.md) した際にAdobe Analyticsから同期されたコンバージョン指標とサイトエンゲージメント指標が含  [!DNL Adobe Analytics for Advertising]  れます。 <!--Analytics calculated metrics and advanced calculated metrics aren't available.--> 収集したコンバージョンをレポートに含める方法について詳しくは、「検索、ソーシャル、Commerceガイド」のトピック「[ 広告主のコンバージョン指標の管理について ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) を参照してください。

1. （[[!UICONTROL Overview]] タブ）:

   * （省略可能） [!UICONTROL Overall Regional Performance] セクションで、グラフ内のポイントの上にカーソルを置くと、そのポイントのデータが表示されます。

   * （オプション） [!UICONTROL Regional Performance] のセクションで、次のいずれかの操作を行います。

      * 指標名（[!UICONTROL Impressions] など）をクリックすると、その指標が表示されます。

      * [!UICONTROL Region] メニューで領域を選択します。

      * 国または州にカーソルを合わせると、その地域のデータが表示されます。

   * （オプション） [!UICONTROL Device Performance] のセクションで、次のいずれかの操作を行います。

      * 任意のデバイスカテゴリの値にカーソルを合わせると、その条件のデータが表示されます。

      * 任意のデバイスカテゴリの値をクリックすると、その条件を満たす上位 <!-- NN--> 件のクリエイティブのリストが表示されます。

1. （オプション）クリエイティブ別、バンドル別または広告タグ別にデータを表示するには、「**[!UICONTROL Creative Performance]**」タブをクリックします。

   * 「[!UICONTROL Creatives]」サブタブでは、次のいずれかの操作を実行できます。

      * （オプション）グラフ表示とグリッド表示を切り替えるには、「![ グラフ ](/help/creative/assets/chart-view-button.png " グラフ ")」および「![グリッド](/help/creative/assets/table-view-button.png "グリッド")」をそれぞれクリックします。

      * （オプション）グラフ・ビューで、グラフ内のポイントの上にカーソルを置くと、そのポイントのデータが表示されます。

      * （デシジョンツリーのターゲット設定を使用したエクスペリエンスのみ。オプション）適用された各広告ターゲットのパフォーマンスを分割するには、**[!UICONTROL Split targeting]** を有効にします。

1. バンドル（デシジョンツリーターゲティングを使用したエクスペリエンス）または広告タグ（デシジョンツリーターゲティングを使用しないエクスペリエンス）別にデータを表示するには、「**[!UICONTROL Bundles]**」サブタブをクリックします。 次のいずれかの操作を行うことができます。

   * （オプション）グラフ表示とグリッド表示を切り替えるには、「![ グラフ ](/help/creative/assets/chart-view-button.png " グラフ ")」および「![グリッド](/help/creative/assets/table-view-button.png "グリッド")」をそれぞれクリックします。

   * （オプション）グラフ・ビューで、グラフ内のポイントの上にカーソルを置くと、そのポイントのデータが表示されます。

   * （デシジョンツリーのターゲット設定を使用したエクスペリエンスのみ。オプション）適用された各広告ターゲットのパフォーマンスを分割するには、**[!UICONTROL Split targeting]** を有効にします。

1. （任意） [!DNL Microsoft Excel] ファイルのデータをスプレッドシート（XLSX）形式でダウンロードするには、ツールバーの ![ ダウンロード ](/help/creative/assets/download.png " ダウンロード ") をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

>[!MORELIKETHIS]
>
>* [ カスタムクリエイティブレポート ](/help/creative/report-custom-creative.md)
