---
title: エクスペリエンス全体のパフォーマンスレポート
description: エクスペリエンスレベルのパフォーマンスレポートを表示する方法について説明します。
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
TQID: https://experienceleague.adobe.com/1k8mcvg9-anlNxZQ43czfxpLEweDr-TolaaEIrDz-Fg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 9376767ebde74e1e8edbc8617ecb72bfd49c8a3d
workflow-type: tm+mt
source-wordcount: 791
ht-degree: 0%

---

# エクスペリエンス全体のパフォーマンスレポート

あらゆるエクスペリエンスの詳細なパフォーマンスデータを表示できます。

## エクスペリエンスレベルのパフォーマンスレポートのデータ

レポートビューには、次のデータが含まれます。

* **概要** タブ：エクスペリエンス全体<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." -->のすべてのコンバージョン指標に関するパフォーマンスの概要（次を含む）:

   * **全体的なパフォーマンス** セクション：

      * **全体的なパフォーマンス**：合計インプレッション数、クリック数、クリックスルー率（CTR）、ビュースルーコンバージョン数およびクリックスルー率コンバージョン数。

        <!--
      ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
      -->

      * **デフォルトのレート**: （デジジョンツリーのターゲティングのみを使用したエクスペリエンス） ターゲットを絞ったクリエイティブ、ターゲットを持たない汎用的なクリエイティブ、または「他のすべてのユーザー」をターゲットにした汎用的なクリエイティブ、およびエクスペリエンスのデフォルトのクリエイティブから得られるインプレッションの数。

        <!--
      ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
      -->

   * **パフォーマンスの分類** セクション：

      * ** 地域別実績：*：地理的地域別の個別指標

        <!--
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **デバイスのパフォーマンス：** デバイスの種類、オペレーティングシステム、ブラウザーごとの個々の指標。 オプションで、任意のデバイスカテゴリの値をクリックすると、その条件で配信された上位10人のクリエイターのリストが表示されます。

        <!--
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* 「**Creative パフォーマンス**」タブ*：クリエイティブおよびバンドルまたは広告タグ別のパフォーマンスの概要（以下を含む）。

   * **Creative** サブタブ：エクスペリエンス内の各クリエイティブのインプレッション数、クリック数、CTRの合計数<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * **バンドル/タグ** サブタブ：エクスペリエンス内の個々のバンドル（デシジョンツリーターゲティングを使用したエクスペリエンス）または広告タグ（デシジョンツリーターゲティングを使用しないエクスペリエンス）のインプレッション、クリック、およびCTRの合計数。

## エクスペリエンスのパフォーマンスレポートの表示

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. （オプション） [特定のエクスペリエンスを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. エクスペリエンスを選択します。

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Reports]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Reports]**&#x200B;をクリックします。

   「[!UICONTROL Overview]」タブが開きます。

1. （オプション）右上のツールバーで、すべてのパフォーマンスレポートでレポートされる日付範囲、コンバージョン属性ルール、コンバージョンを指定します。

   * （オプション）パフォーマンスデータの日付範囲を変更するには、日付メニューでオプションを選択します。

      * プリセット期間を指定するには、次のレポートを選択します：（*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],*&#x200B;または&#x200B;*[!UICONTROL Yesterday]*。

      * カスタムの日付範囲を指定するには、開始日と終了日を入力するか、フィールドの横にある![&#x200B; カレンダーアイコン &#x200B;](/help/search-social-commerce/assets/calendar.png)をクリックして、日付を選択します。

   * （オプション）コンバージョンにつながる一連のイベントのコンバージョンデータの属性に使用するルールを変更するには、![設定](/help/creative/assets/settings.png)をクリックし、**[!UICONTROL Attribution Rule]**&#x200B;を変更します。

     アトリビューションルールについて詳しくは、「[&#x200B; アトリビューションルールの計算方法](/help/search-social-commerce/reports/attribution-rules.md)」を参照してください。

   * （オプション）報告されたコンバージョンを変更するには、![設定](/help/creative/assets/settings.png)をクリックし、**[!UICONTROL Conversions]** メニューでコンバージョン名を選択します。 現在、利用可能な指標は、すべてのコンバージョン指標を含む「すべてを選択」のみです。

     使用可能なコンバージョン列には、Search、Social、およびCommerceのお客様であるかどうかにかかわらず、Advertising Search、Social、およびCommerceで使用可能なコンバージョンが含まれます。 リストには、広告主が[an [!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md)を持つ場合にAdobe Analyticsから同期されたコンバージョンとサイトエンゲージメントの指標を含めることができます。 [!DNL Analytics]個の計算指標と高度な計算指標は使用できません。 収集したコンバージョンをレポートに含める方法について詳しくは、Search, Social, &amp; Commerce ガイドのトピック「[広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)」を参照してください。

1. （[!UICONTROL Overview] タブで）:

   * （オプション）「[!UICONTROL Overall Regional Performance]」セクションで、グラフのポイントにカーソルを合わせると、そのポイントのデータが表示されます。

   * （オプション）「[!UICONTROL Regional Performance]」セクションで、次のいずれかの操作を行います。

      * 指標の名前（[!UICONTROL Impressions]など）をクリックすると、その指標が表示されます。

      * [!UICONTROL Region] メニューで地域を選択します。

      * 国または州の上にカーソルを置くと、その地域のデータが表示されます。

   * （オプション）「[!UICONTROL Device Performance]」セクションで、次のいずれかの操作を行います。

      * 任意のデバイスカテゴリの値にカーソルを合わせると、その条件のデータが表示されます。

      * 任意のデバイスカテゴリの値をクリックすると、その条件で配信された上位<!-- NN-->人のクリエイターのリストが表示されます。

1. （オプション）クリエイティブ別、バンドル別または広告タグ別にデータを表示するには、「**[!UICONTROL Creative Performance]**」タブをクリックします。

   * 「[!UICONTROL Creatives]」サブタブでは、次のいずれかを実行できます。

      * （オプション）グラフ表示とグリッド表示を切り替えるには、それぞれ![&#x200B; グラフ &#x200B;](/help/creative/assets/chart-view-button.png " グラフ ")と![グリッド](/help/creative/assets/table-view-button.png "グリッド")をクリックします。

      * （オプション）グラフ表示で、グラフ内のポイントにカーソルを合わせると、そのポイントのデータが表示されます。

      * （決定木ターゲティングのエクスペリエンスのみ。オプション）適用された各広告ターゲットのパフォーマンスを分割するには、**[!UICONTROL Split targeting]**&#x200B;を有効にします。

1. バンドル別（デシジョンツリーターゲティングを使用したエクスペリエンス）または広告タグ別（デシジョンツリーターゲティングを使用しないエクスペリエンス）にデータを表示するには、**[!UICONTROL Bundles]** サブタブをクリックします。 次のいずれかを実行できます。

   * （オプション）グラフ表示とグリッド表示を切り替えるには、それぞれ![&#x200B; グラフ &#x200B;](/help/creative/assets/chart-view-button.png " グラフ ")と![グリッド](/help/creative/assets/table-view-button.png "グリッド")をクリックします。

   * （オプション）グラフ表示で、グラフ内のポイントにカーソルを合わせると、そのポイントのデータが表示されます。

   * （決定木ターゲティングのエクスペリエンスのみ。オプション）適用された各広告ターゲットのパフォーマンスを分割するには、**[!UICONTROL Split targeting]**&#x200B;を有効にします。

## エクスペリエンスのパフォーマンスレポートのダウンロード

* パフォーマンスレポートの上部にあるツールバーで、![&#x200B; ダウンロード &#x200B;](/help/creative/assets/download.png " ダウンロード ")をクリックします。

  ファイルは、ブラウザーの通常の手順に従って、スプレッドシート （XLSX）形式の[!DNL Microsoft Excel] ファイルでダウンロードされます。

>[!MORELIKETHIS]
>
>* [&#x200B; カスタムレポートについて](/help/creative/reports/reports-about.md)
>* [&#x200B; カスタムレポートの管理](/help/creative/reports/report-manage.md)
>* [&#x200B; ビュー内のすべてのエクスペリエンスをダウンロード &#x200B;](/help/creative/experiences/experience-download-view.md)
>* [&#x200B; エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
>* [Advertising Creativeでの体験について](/help/creative/experiences/experience-about.md)
>* [&#x200B; アラートの表示](/help/creative/reports/alerts-view.md)
