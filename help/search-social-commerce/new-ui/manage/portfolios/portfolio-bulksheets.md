---
title: バルクシートファイルを使用したポートフォリオ設定の一括編集
description: バルクシート ファイルを使用して複数のポートフォリオの設定を編集する方法について説明します。
feature: Search Portfolios, Search Optimization
hide: yes
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
TQID: https://experienceleague.adobe.com/tKCeMIgFKnW8hOU-6uavT9x7K9lL2Uqo2bWZ-H-Q5TE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 0%

---

# バルクシートファイルを使用したポートフォリオ設定の一括編集

*Beta機能*

ポートフォリオバルクシートは、特定の形式のポートフォリオ設定を含むファイルで、設定をすばやく確認して変更するために使用できます。 1つ以上のポートフォリオの設定を含むバルクシートを生成（ダウンロード）できます。 ファイルは、2つのワークシート （XLSX形式）を含む[!DNL Excel] ワークブックとしてダウンロードされます。 ワークブックには次の内容が含まれます。

* フィールドの編集に関する情報を含む、読み取り専用の[!UICONTROL Instructions] ワークシート。

* 含まれるポートフォリオごとに1行の[!UICONTROL Portfolio Settings Edit] タブ。 必要に応じてフィールドを編集し、ファイルをローカルに保存した後、編集したファイル [をSearch, Social, &amp; Commerceにアップロードすることもできます。 ](#portfolio-bulksheet-upload)編集可能なフィールドがカラーでハイライト表示されます。

## ポートフォリオ設定を含むバルクシートファイルのダウンロード

1. （オプション）バルクシートに含める各ポートフォリオの横にあるチェックボックスをオンにします。

   特定のポートフォリオを選択しない場合は、すべてのポートフォリオの設定をダウンロードできます。

1. データテーブルの上にあるツールバーで、次をクリックします。

   * （すべてのポートフォリオに対して） **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export All Portfolios]**。

   * （選択したポートフォリオの場合） **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**。

1. 作成するバルクシート ファイルの名前を入力し、**[!UICONTROL Export Now]**&#x200B;をクリックします。

   ファイルは、ブラウザーのデフォルトのダウンロードフォルダーに保存されます。

## 更新されたポートフォリオ設定を含むバルクシートファイルのアップロード {#portfolio-bulksheet-upload}

ファイルはXLSX形式である必要があります。

1. データテーブルの上のツールバーで、**[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**&#x200B;をクリックします。

1. [!UICONTROL Import Portfolio Details File] ダイアログで、次の操作を行います。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、**[!UICONTROL Browse File]**&#x200B;をクリックして、デバイスまたはネットワークからファイルを選択します。

   1. **[!UICONTROL Import]**&#x200B;をクリックします。

アップロードのステータスは、日付範囲セレクターの横にある[!UICONTROL Global Sync Status] ボタン（![ グローバル同期ステータス ](/help/search-social-commerce/assets/global-sync-status.png " グローバル同期ステータス ")）から確認できます。 いずれかの変更が成功しなかった場合は、失敗した内容を示すエラーファイルをダウンロードできます。

通知も通知センターに追加され、![ ボタン （](/help/search-social-commerce/assets/notifications-new.png "）の横にある")通知[!UICONTROL Global Sync Status]通知![グローバル同期ステータス](/help/search-social-commerce/assets/global-sync-status.png "グローバル同期ステータス") アイコンから通知ペインを開くことができます。

## アップロードされたバルクシートファイルのデータ要件

すべてのバルクシートファイルには列[!UICONTROL Portfolio ID]を含める必要があり、データ行ごとに[!UICONTROL Portfolio ID]の値を含めてアクションを実行する必要があります。 データ要件について詳しくは、ダウンロードしたバルクシート ファイルの「[!UICONTROL Instructions]」タブを参照してください。

「[!UICONTROL Portfolio Settings Edit]」タブのポートフォリオ設定列について詳しくは、検索、ソーシャル、およびCommerce内から入手できる最適化ガイドを参照してください。

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
>* [ （新しいUI） ポートフォリオの編集](portfolio-edit.md)
>* [ ポートフォリオを作成](portfolio-create.md)
>* [ （新しいUI） ポートフォリオについて](portfolio-about.md)
