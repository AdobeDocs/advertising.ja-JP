---
title: エクスペリエンスレベルのパフォーマンスレポート
description: エクスペリエンスレベルのパフォーマンスレポートを表示する方法について説明します。
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# エクスペリエンスレベルのパフォーマンスレポート

任意のエクスペリエンスの詳細なパフォーマンスデータを表示できます。

## エクスペリエンスレベルのパフォーマンスレポートのデータ

レポート表示には、次のデータが含まれます。

* **概要** タブ：以下を含む、エクスペリエンス全体のすべてのコンバージョン指標に関するパフォーマンスの概要 <!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." -->

   * **全体的なパフォーマンス** セクション：

      * **全体的なパフォーマンス**：合計インプレッション数、クリック数、クリックスルー率（CTR）、ビュースルーコンバージョンおよびクリックスルーコンバージョン。

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **デフォルト率**: （決定ツリーのターゲット設定を使用したエクスペリエンスのみ）ターゲットクリエイティブ、ターゲットを設定していない汎用クリエイティブまたは「その他すべてのユーザー」をターゲットにした汎用クリエイティブおよびエクスペリエンスのデフォルトクリエイティブによるインプレッション数。

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **パフォーマンスの分類** セクション：

      * **地域パフォーマンス：*：地理的な場所ごとの個々の指標。

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **デバイスのパフォーマンス：** デバイスタイプ、オペレーティングシステムおよびブラウザー別の個々の指標。 必要に応じて、任意のデバイスカテゴリの値をクリックして、その条件を満たす上位 10 件のクリエイティブのリストを表示します。

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Creativeのパフォーマンス** タブ*: クリエイティブ、バンドルまたは広告タグ別のパフォーマンスの概要。以下に例を示します。

   * **クリエイティブ** サブタブ：エクスペリエンス内の各クリエイティブのインプレッション数、クリック数および CTR の合計 <!-- No breakdown yet for the individual ad elements and/or the served ads. -->。

   * **バンドル/タグ** サブタブ：エクスペリエンス内の個々のバンドル（デシジョンツリーターゲティングを使用したエクスペリエンス）または広告タグ（デシジョンツリーターゲティングを使用しないエクスペリエンス）のインプレッション数、クリック数および CTR の合計数。

## エクスペリエンスのパフォーマンスレポートの表示

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. （任意） [&#x200B; ビューをカスタマイズ &#x200B;](/help/creative/introduction/customize-data-views.md) して、特定のエクスペリエンスを含めます。

1. エクスペリエンスを選択します。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Reports]**」をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Reports]** をクリックします。

   「[!UICONTROL Overview]」タブが開きます。

1. （オプション）右上のツールバーで、日付範囲、コンバージョンアトリビューションルール、すべてのパフォーマンスレポート内で報告されるコンバージョンを指定します。

   * （オプション）パフォーマンスデータの日付範囲を変更するには、日付メニューでオプションを選択します。

      * プリセットの期間を指定するには、レポート（*[!UICONTROL Last Month-to-date]、* *[!UICONTROL Last 7 days]、* *[!UICONTROL Last 30 days]、* *[!UICONTROL Last 7 days]、* *[!UICONTROL Last 30 days]、* *[!UICONTROL Today]、* または *[!UICONTROL Yesterday]*）を選択します。

      * カスタムの日付範囲を指定するには、開始日と終了日を入力するか、フィールドの横にある ![&#x200B; カレンダーアイコン &#x200B;](/help/search-social-commerce/assets/calendar.png) をクリックして日付を選択します。

   * （任意）コンバージョンにつながる一連のイベント内のコンバージョンデータを属性化するためのルールを変更するには、![&#x200B; 設定 &#x200B;](/help/creative/assets/settings.png) をクリックして **[!UICONTROL Attribution Rule]** を変更します。

     アトリビューションルールについて詳しくは、[&#x200B; アトリビューションルールの計算方法 &#x200B;](/help/search-social-commerce/reports/attribution-rules.md) を参照してください。

   * （オプション）レポートされたコンバージョンを変更するには、![&#x200B; 設定 &#x200B;](/help/creative/assets/settings.png) をクリックし、**[!UICONTROL Conversions]** メニューでコンバージョン名を選択します。 現在、使用可能な唯一の指標は、すべてのコンバージョン指標を含める「すべてを選択」です。

     使用可能なコンバージョン列には、検索、ソーシャル、Commerceのユーザーであるかどうかに関わらず、Advertising検索、ソーシャル、Commerceで使用可能なコンバージョンが含まれます。 このリストには、広告主が [an [!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md) を実行した際にAdobe Analyticsから同期されたコンバージョン指標とサイトエンゲージメント指標を含めることができます。 [!DNL Analytics] 計算指標と高度な計算指標は使用できません。 収集したコンバージョンをレポートに含める方法について詳しくは、「検索、ソーシャル、Commerceガイド」のトピック「[&#x200B; 広告主のコンバージョン指標の管理について &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) を参照してください。

1. （[[!UICONTROL Overview]] タブ）:

   * （省略可能） [!UICONTROL Overall Regional Performance] セクションで、グラフ内のポイントの上にカーソルを置くと、そのポイントのデータが表示されます。

   * （オプション） [!UICONTROL Regional Performance] のセクションで、次のいずれかの操作を行います。

      * 指標名（[!UICONTROL Impressions] など）をクリックすると、その指標が表示されます。

      * [!UICONTROL Region] メニューで領域を選択します。

      * 国または州にカーソルを合わせると、その地域のデータが表示されます。

   * （オプション） [!UICONTROL Device Performance] のセクションで、次のいずれかの操作を行います。

      * 任意のデバイスカテゴリの値にカーソルを合わせると、その条件のデータが表示されます。

      * 任意のデバイスカテゴリの値をクリックすると、その条件を満たす上位のクリエイティブ <!-- NN--> リストが表示されます。

1. （オプション）クリエイティブ別、バンドル別または広告タグ別にデータを表示するには、「**[!UICONTROL Creative Performance]**」タブをクリックします。

   * 「[!UICONTROL Creatives]」サブタブでは、次のいずれかの操作を実行できます。

      * （オプション）グラフ表示とグリッド表示を切り替えるには、「![&#x200B; グラフ &#x200B;](/help/creative/assets/chart-view-button.png " グラフ ")」および「![グリッド](/help/creative/assets/table-view-button.png "グリッド")」をそれぞれクリックします。

      * （オプション）グラフ・ビューで、グラフ内のポイントの上にカーソルを置くと、そのポイントのデータが表示されます。

      * （デシジョンツリーのターゲット設定を使用したエクスペリエンスのみ。オプション）適用された各広告ターゲットのパフォーマンスを分割するには、**[!UICONTROL Split targeting]** を有効にします。

1. バンドル（デシジョンツリーターゲティングを使用したエクスペリエンス）または広告タグ（デシジョンツリーターゲティングを使用しないエクスペリエンス）でデータを表示するには、「**[!UICONTROL Bundles]**」サブタブをクリックします。 次のいずれかの操作を行うことができます。

   * （オプション）グラフ表示とグリッド表示を切り替えるには、「![&#x200B; グラフ &#x200B;](/help/creative/assets/chart-view-button.png " グラフ ")」および「![グリッド](/help/creative/assets/table-view-button.png "グリッド")」をそれぞれクリックします。

   * （オプション）グラフ・ビューで、グラフ内のポイントの上にカーソルを置くと、そのポイントのデータが表示されます。

   * （デシジョンツリーのターゲット設定を使用したエクスペリエンスのみ。オプション）適用された各広告ターゲットのパフォーマンスを分割するには、**[!UICONTROL Split targeting]** を有効にします。

## エクスペリエンスのパフォーマンスレポートをダウンロードする

* パフォーマンスレポートの上部にあるツールバーで、「![&#x200B; ダウンロード &#x200B;](/help/creative/assets/download.png " ダウンロード ")」をクリックします。

  ファイルは、ブラウザーの通常の手順に従って、スプレッドシート（XLSX）形式の [!DNL Microsoft Excel] ファイルとしてダウンロードされます。

>[!MORELIKETHIS]
>
>* [&#x200B; カスタムCreativeレポート &#x200B;](/help/creative/report-custom-creative.md)
>* [&#x200B; ビュー内のすべてのエクスペリエンスをダウンロード &#x200B;](/help/creative/experiences/experience-download-view.md)
>* [Advertising Creativeでのエクスペリエンスについて &#x200B;](/help/creative/experiences/experience-about.md)
