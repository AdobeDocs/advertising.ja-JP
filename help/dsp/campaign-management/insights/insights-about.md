---
title: Performance Insights について
description: ビジュアライゼーションを使用したパフォーマンスインサイトについて説明します。
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: ca531db43b9e07dc767da3d0e866bfc85add7ee9
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Performance Insights について

*Beta機能*

<!-- Edit title and metadata as necessary -->

ビジュアライゼーションを使用した高レベルのパフォーマンスインサイトは、キャンペーンを効率的に最適化し、パフォーマンスを拡張する新しい機会を見つけるために必要な情報を提供します。 キャンペーン全体のデータを表示したり、下位レベルにドリルダウンしたりできます。

パフォーマンスインサイトを使用して、次のことを行います。

* 戦略的計画および十分な情報に基づいた意思決定のための長期的なトレンドを追跡します。

* より良い結果を得るための機会を特定する。

* 生データの取得から実用的なインサイトの獲得までの時間を短縮することで、効率を向上させます。

Microsoft Excel スプレッドシート（XLSX）形式のビジュアライゼーションを使用せずに、タブのすべてのビジュアライゼーションをPDF ファイルに書き出したり、特定のinsightのデータをダウンロードしたりできます。

また、キャンペーン管理ビューの場合と同様に、[ 日付範囲の変更、ビューの設定 ](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"} カスタムビューの保存を行うこともできます。

## インサイトのタイプ

### 「[!UICONTROL Home]」タブ

「[!UICONTROL Home]」タブには、広告主のすべてのキャンペーンをまたぐ主要な標準、パフォーマンス、ビューアビリティの指標が表示され <!-- active only? --> す。 デフォルトでは、クロスキャンペーンデータが表示されます。 オプションで、フィルターを設定して、異なる広告主のデータや、特定のキャンペーン <!-- active only? -->、パッケージ <!-- active only? -->、カスタム目標、プレースメントのデータのみを表示 <!-- active only? --> きます。 インサイトには次のものが含まれます。

* 顧客が指定した 3 つの指標（デフォルトでは、[!UICONTROL Net Spend]、[!UICONTROL Impressions]、[!UICONTROL Net CPM]）のトレンドグラフ。

* キャンペーン別、公開者別、メディアタイプ別など、顧客が指定した 3 つのディメンションによる、特定の指標のデータの分類。 ディメンションの分類ごとに、異なる指標を選択できます。

### 「[!UICONTROL Household Reach]」タブ

「[!UICONTROL Household Reach]」タブには、広告主のすべてのキャンペーン全体で世帯のリーチ指標が表示され <!-- active only? --> す。 デフォルトでは、クロスキャンペーンデータが表示されます。 オプションで、別の広告主のデータや特定のキャンペーンのデータのみを表示するフィルターを設定 <!-- active only? --> きます。 インサイトには次のものが含まれます。

* 顧客が指定した 3 つの指標（デフォルトでは、[!UICONTROL Net Spend]、[!UICONTROL Unique Reach] および [!UICONTROL Net CPM]）について日別または週別にトレンド・グラフを作成します。

* [!UICONTROL Media Type]、[!UICONTROL Device Type]、[!UICONTROL Inventory Type] による世帯の増分的なリーチを示すドーナツグラフ。 *増分世帯リーチ* は、単一のメディア、デバイスまたは在庫タイプを排他的に通じて到達した世帯として定義されます。

* 世帯のリーチの増分と、[!UICONTROL Media Type]、[!UICONTROL Device Type]、[!UICONTROL Inventory Type] による重複の世帯のリーチの比較。

  *増分世帯リーチ* は、単一のメディア、デバイスまたは在庫タイプを排他的に通じて到達した世帯として定義されます。 *重複する世帯リーチ* は、複数のメディア、デバイスまたは在庫タイプが到達する世帯と定義されます。

* 最もパフォーマンスの高いキャンペーン、プレースメント、パッケージ、公開者、サイト/アプリ、メディアタイプ、在庫タイプ、デバイスタイプ （[!UICONTROL Unique Reach]、[!UICONTROL Net Spend]、[!UICONTROL Cost per Reach] 別）。

* パッケージ、パブリッシャー、サイト/アプリ別の [!UICONTROL Cost per Reach] と [!UICONTROL Net Spend]。 このinsightを使用して、どのパッケージ、パブリッシャー、またはサイト/アプリが大幅な増分リーチの可能性を示しているかを確認します。

## パフォーマンスインサイトを開く

* （すべてのキャンペーンのインサイトを開くには）メインメニューで「イン **[!UICONTROL Insights BETA]** イト」をクリックします。

* （特定のキャンペーン、パッケージまたはプレースメントのインサイトを開くには） [!UICONTROL Campaigns]、[!UICONTROL Packages] または [!UICONTROL Placements] ビューで、エンティティ名の横にある **[!UICONTROL ...]**/**[!UICONTROL Insights]** をクリックします。

## タブへのフィルターの適用

1. タブ上部のツールバーで、「![ フィルターボタン ](/help/dsp/assets/filter.png)」をクリックします。

1. 必要に応じて、左側の列でディメンションを選択したあと、右側の列で 1 つ以上の値を選択します。

   一度に選択できる広告主は 1 人のみです。

1. 「**[!UICONTROL Apply]**」をクリックします。

1. （オプション）データをさらに絞り込むには、ツールバーでエンティティタイプを選択して、特定のエンティティ値（単一のキャンペーン、パッケージまたはプレースメント）を選択します。

## insightについてレポートされるDimensionの変更

* insightの左上にあるドロップダウンメニューから、寸法を選択します。

## insightについてレポートされる指標の変更

1. insightの右上にある ![ 指標設定 ](/help/dsp/assets/metric-settings.png " 指標設定 ") をクリックします。

1. 指標を選択し、「**[!UICONTROL Apply]**」をクリックします。

## タブのすべてのビジュアライゼーションをPDF ファイルにエクスポート

* タブの上で、**[!UICONTROL ...]**/**[!UICONTROL Export]** をクリックします。

  ファイルは、ブラウザーのデフォルトのダウンロードフォルダーに保存されます。

## XLSX ファイルへの特定のInsightのダウンロード

* insightの右上にある「![ ダウンロード ](/help/creative/assets/download.png " ダウンロード ")」をクリックします。

  ファイルは、ブラウザーのデフォルトのダウンロードフォルダーに保存されます。

>[!MORELIKETHIS]
>
>* [ カスタムレポートについて ](/help/dsp/reports/report-about.md)
>* [ キャンペーン管理ビューでのパフォーマンスレポートのタイプ ](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [ 使用可能なレポート列 ](/help/dsp/reports/report-columns.md)
>* [ キャンペーンデータビューの管理 ](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
