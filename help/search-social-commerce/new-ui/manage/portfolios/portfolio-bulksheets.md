---
title: バルクシートファイルを使用したポートフォリオ設定の一括編集
description: バルクシートファイルを使用して複数のポートフォリオの設定を編集する方法を説明します。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 04b6fbaf4a8b360bc3a60bdad4871694d50f1bf9
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# バルクシートファイルを使用したポートフォリオ設定の一括編集

*Beta機能*

ポートフォリオ バルクシートは、特定の形式のポートフォリオ設定を含むファイルで、設定をすばやく確認および変更するために使用できます。 1 つ以上のポートフォリオの設定を含むバルクシートを生成（ダウンロード）できます。 ファイルは、2 つのワークシート（XLSX 形式）を持つ [!DNL Excel] ワークブックとしてダウンロードされます。 ワークブックには次が含まれます。

* フィールドの編集に関する情報を含む読み取り専用の [!UICONTROL Instructions] ワークシート。

* 含まれるポートフォリオごとに 1 行の [!UICONTROL Portfolio Settings Edit] しいタブ。 必要に応じてフィールドを編集し、ファイルをローカルに保存したあと、検索、ソーシャルおよびCommerceに [ 編集したファイルをアップロード ](#portfolio-bulksheet-upload) することもできます。 編集可能なフィールドはカラーでハイライト表示されます。

## ポートフォリオ設定を含むバルクシート ファイルのダウンロード

1. （オプション）バルクシートに含める各ポートフォリオの横にあるチェックボックスをオンにします。

   特定のポートフォリオを選択しない場合は、すべてのポートフォリオの設定をダウンロードできます。

1. データ テーブルの上にあるツールバーで、次のいずれかをクリックします。

   * （すべてのポートフォリオの場合） **[!UICONTROL Bulk Operations]**/**[!UICONTROL Export All Portfolios]**。

   * （選択したポートフォリオの場合） **[!UICONTROL Bulk Operations]**/**[!UICONTROL Export Selected Portfolios]**。

1. 作成するバルクシート ファイルの名前を入力し、[**[!UICONTROL Export Now]**] をクリックします。

   ファイルは、ブラウザーのデフォルトのダウンロードフォルダーに保存されます。

## 更新されたポートフォリオ設定を含むバルクシート ファイルのアップロード {#portfolio-bulksheet-upload}

ファイルは XLSX 形式である必要があります。

1. データテーブルの上にあるツールバーで、**[!UICONTROL Bulk Operations]**/**[!UICONTROL Import Portfolio Details]** をクリックします。 &lt;!— 「Portfolio設定の読み込み」にする必要があります。「詳細」が曖昧すぎて、何か他のものを含んでいる可能性があります。—>

1. [!UICONTROL Import Portfolio Details File] ダイアログで、次の操作を行います。<!-- reword if we change the name of the operation -->

   1. ボックスにファイルをドラッグ&amp;ドロップするか、**[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. 「**[!UICONTROL Import]**」をクリックします。

アップロードのステータスは、日付範囲セレクターの横にある [!UICONTROL Global Sync Status] ボタン（![ グローバル同期ステータス ](/help/search-social-commerce/assets/global-sync-status.png " グローバル同期ステータス ")）から確認できます。<!-- icon similar to Refresh -->。 いずれかの変更が成功しなかった場合は、失敗したことを示すエラーファイルをダウンロードできます。

通知も通知センターに追加され、通知ボタンの横にある ![ 通知 ](/help/search-social-commerce/assets/notifications-new.png " 通知 ") アイコンから [!UICONTROL Global Sync Status] 知ペインを開くことができます（![グローバル同期ステータス](/help/search-social-commerce/assets/global-sync-status.png "グローバル同期ステータス")）。

## アップロードしたバルクシートファイルのデータ要件

すべてのバルクシート ファイルには列 [!UICONTROL Portfolio ID] を含める必要があり、各データ行にはアクションを起こせる [!UICONTROL Portfolio ID] の値を含める必要があります。 データ要件について詳しくは、ダウンロードしたバルクシートファイルの「[!UICONTROL Instructions]」タブを参照してください。

「[!UICONTROL Portfolio Settings Edit]」タブのポートフォリオ設定列の説明については、最適化ガイドを参照してください。このガイドは、検索、ソーシャル、Commerce内から利用できます。

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [ （新しい UI）ポートフォリオの編集 ](portfolio-edit.md)
>* [ ポートフォリオの作成 ](portfolio-create.md)
>* ポートフォリオに関する [ （新しい UI） ](portfolio-about.md)
