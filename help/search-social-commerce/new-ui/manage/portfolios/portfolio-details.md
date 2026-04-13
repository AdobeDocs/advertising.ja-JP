---
title: （新しいUI） ポートフォリオパフォーマンスの詳細の表示
description: ポートフォリオレベルおよび割り当てられた各キャンペーンの実際の指標と予測指標を含む、ポートフォリオパフォーマンスの詳細を表示する方法について説明します。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
TQID: https://experienceleague.adobe.com/5hNxKu6YjJTWI4KGEc6aaYnpgXK6k3OsN0-YfetzENw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 235ba59f2d9e37259431b415c2e34c0da8209ef9
workflow-type: tm+mt
source-wordcount: 735
ht-degree: 0%

---

# （新しいUI） ポートフォリオパフォーマンスの詳細の表示

*Beta機能*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

ポートフォリオの詳細ビューには、ポートフォリオに関する次の情報が含まれます。

* 最大3つのパフォーマンス指標の実際の値と予測値。 レポートには、ポートフォリオの合計指標値と、日付ごとの指標の内訳が含まれます。<!-- Not for active portfolios only?  -->

* アクティブなポートフォリオのモデル精度データ。モデルが予測からどの程度偏差しているかを示します。 このレポートには、毎日またはローリングの7日間のコスト精度、クリック精度、および目標値の精度が全体的に表示されます。

  クリック日（デフォルト）またはトランザクション日別にデータを表示できます。   データは、トレンドチャート（デフォルト）またはテーブルとして表示することもできます。

* アクティブなポートフォリオの実際の費用に対するターゲット支出。 オプションで、ポートフォリオのキャンペーン予算合計も含めることができます。

* 広告ネットワーク別のアクティブなポートフォリオのコスト、クリック、または[目標値](/help/search-social-commerce/glossary.md#o-p)予測の正確性。<!-- Verify -->

* ポートフォリオ設定。

  必要に応じて、ポートフォリオ設定を開いて編集できます。

## ポートフォリオのパフォーマンスの詳細を開く

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Portfolios]**&#x200B;をクリックします。

1. ポートフォリオ名をクリックします。

1. （オプション） **[!UICONTROL Granularity]** メニューから、*[!UICONTROL Daily]、*、*[!UICONTROL Weekly]、*&#x200B;または&#x200B;*[!UICONTROL Monthly]の間のデータの精度を変更します。*

1. （オプション）ポートフォリオの詳細の日付範囲を変更するには、右上の日付範囲をクリックし、日付範囲を指定してから「**[!UICONTROL Apply]**」をクリックします。

## [!UICONTROL Portfolio Overview] タブをカスタマイズ

* （オプション） [!UICONTROL Portfolio Performance] レポートをカスタマイズするには、次のいずれかの操作を行います。

   * 合計指標と詳細指標の両方に使用されるパフォーマンス指標を変更するには、**[!UICONTROL Metrics]**&#x200B;をクリックし、最大3つの指標を選択します。

     デフォルトの指標は&#x200B;*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*、および&#x200B;*[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->です

   * 詳細な指標については、次を参照してください。

      * **[!UICONTROL Display predictions]**&#x200B;の横にあるスイッチを移動して、予測指標の値を表示または非表示にします。

      * グラフ ビュー（![ グラフ ビュー](/help/search-social-commerce/assets/chart-view.png " グラフ ビュー")）とテーブル ビュー（![テーブルビュー](/help/search-social-commerce/assets/table-view.png "テーブルビュー")）を切り替えます。

      * （グラフ表示）グラフ上の任意のポイントのデータを表示するには、そのポイントにカーソルを合わせます。

* （オプション） [!UICONTROL Model accuracy]傾向グラフをカスタマイズするには、次のいずれかの操作を行います。

   * グラフ ビュー（![ グラフ ビュー](/help/search-social-commerce/assets/chart-view.png " グラフ ビュー")）とテーブル ビュー（![テーブルビュー](/help/search-social-commerce/assets/table-view.png "テーブルビュー")）を切り替えます。

   * *[!UICONTROL Click Date]*&#x200B;と&#x200B;*[!UICONTROL Transaction Date]*&#x200B;によるデータの表示を切り替えます。

   * *[!UICONTROL Daily Accuracy]*&#x200B;と&#x200B;*[!UICONTROL 7 Day Rolling Accuracy]*&#x200B;に関するデータの表示を切り替えます。

     [!UICONTROL 7 Day Rolling Accuracy]は、過去7日間の予測の平均精度で、パーセントで表されます。 例えば、2025年5月8日の値は、2025年5月1日～5月7日の平均精度です。

   * （グラフ表示）グラフ上の任意のポイントのデータを表示するには、そのポイントにカーソルを合わせます。

* （オプション） [!UICONTROL Target vs actual spend]傾向グラフをカスタマイズするには、次のいずれかの操作を行います。

   * **[!UICONTROL Display budget]**&#x200B;の横にあるスイッチを移動して、各日付のキャンペーンの総予算を表示または非表示にします。

   * グラフ上の任意のポイントのデータを表示するには、そのポイントの上にカーソルを置きます。

* （オプション） [!UICONTROL Network Accuracy]傾向グラフをカスタマイズするには、次のいずれかの操作を行います。

   * 報告された指標を&#x200B;*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*&#x200B;または&#x200B;*[!UICONTROL Objective Value]*&#x200B;に変更します。

   * グラフ上の任意のポイントのデータを表示するには、そのポイントの上にカーソルを置きます。

1. **[!UICONTROL Download report]**&#x200B;をクリックします。

## ポートフォリオ内のキャンペーンのリスト

* 「**[!UICONTROL Campaigns]**」タブをクリックします。

## ポートフォリオ内の広告グループのリスト

* ポートフォリオ内のキャンペーン内のすべての広告グループを表示するには、「**[!UICONTROL Campaigns]**」タブをクリックし、キャンペーン名をクリックします。

## ポートフォリオ内のキーワードのリスト

* ポートフォリオ内のすべてのキーワードを表示するには、「**[!UICONTROL Keywords]**」タブをクリックします。

* ポートフォリオ内の広告グループ内のすべてのキーワードを表示するには、「**[!UICONTROL Ad Groups]**」タブをクリックし、広告グループ名をクリックします。

## ポートフォリオ設定の表示と編集

* ポートフォリオ設定を表示または非表示にするには、**[!UICONTROL Portfolio Settings]**&#x200B;をクリックします。

   * 表示されているポートフォリオ設定を編集するには、設定セクションの横にある![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックし、[ ポートフォリオ設定を編集](portfolio-edit.md)します。

ポートフォリオ設定について詳しくは、Search, Social, &amp; Commerce内から入手できる最適化ガイドを参照してください。

## ポートフォリオパフォーマンスレポートとポートフォリオコンポーネントのリストをダウンロードします

* すべてのレポートをダウンロードするには：

   1. ツールバーで、**[!UICONTROL Download report]**&#x200B;をクリックします。

   1. 含める各パフォーマンスレポートとポートフォリオコンポーネントタイプの横にあるチェックボックスをオンにします。

      一部のパフォーマンスレポートでは、データをチャートまたはテーブルとしてダウンロードするかどうかを選択できます。

   1. **[!UICONTROL Download report]**&#x200B;をクリックします。

* 特定の種類のデータを含む[!DNL model accuracy] レポートをダウンロードするには：

   1. レポートのツールバーで、**[!UICONTROL Download report]**&#x200B;をクリックします。

   1. 含めるデータの各タイプの横にあるチェックボックスと、データの分類の方法（入札単位またはクリックボリューム別）を選択します。

   1. **[!UICONTROL Download report]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ （新しいUI） ポートフォリオについて](portfolio-about.md)
>* [ （新しいUI） ポートフォリオの編集](portfolio-edit.md)
>* [ （新しいUI） [!UICONTROL Portfolios] ビューでデータをダウンロード ](portfolio-view-report.md)
