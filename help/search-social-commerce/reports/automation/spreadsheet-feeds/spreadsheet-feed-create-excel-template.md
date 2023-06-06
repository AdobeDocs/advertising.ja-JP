---
title: の作成 [!DNL Excel] スプレッドシートレポートフィードのテンプレート
description: 特別な形式のスプレッドシートテンプレートを作成する方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# の作成 [!DNL Excel] スプレッドシートレポートフィードのテンプレート

*基本レポートおよびモデル精度レポートのみ*

スプレッドシートフィードを作成するには、まず特別な形式のを作成する必要があります [!DNL Microsoft® Excel] スプレッドシートテンプレートを使用します。 オプションで、 [!DNL Excel] スプレッドシートを使用して、追加の列とグラフを含めることができます。

1. In **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;を使用して、目的のレポートタイプを生成します。 [!UICONTROL Date Aggregation] 単位&quot;[!UICONTROL Daily]」をクリックし、他のすべてのデータパラメーターが必要に応じて、レポートをテンプレートとして保存します。

   >[!NOTE]
   >
   > * のスプレッドシートフィードを作成できます。 [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword]、および [!UICONTROL Forecast Accuracy] レポート。 次の [!UICONTROL Ad Group Report]を使用する場合は、含める広告グループの数を制限し、結果を迅速に得ることができます。
   > * この [!UICONTROL Date Range] テンプレートで定義された単位が使用されていません。 後でスプレッドシートフィードを設定する際に、データを更新する日付を定義します。


1. レポートが生成されたら、に移動します。 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** をクリックし、TSV または XLS バージョンのレポート出力をファイルにエクスポートします。

1. In [!DNL Excel]、レポートのカスタムテンプレートを作成します。

   1. でレポートファイルを開きます。 [!DNL Excel].

   1. ワークブックの準備：

      1. レポートのパラメーターを表示する上位の行を削除します。 XLS ファイルの場合は、[!UICONTROL Total]&quot;行 必要に応じて、一部のデータ行を削除できますが、a) 元の順序のすべての列と b) 少なくとも 1 つのデータ行を含むデータヘッダー行を残します。 データを手動で追加しないでください。

         >[!NOTE]
         >
         > 最後の列には、ゼロ以外の値を含める必要があります。

      2. 開始日を昇順（古い順）に並べ替えます。

      3. ワークシートのタブ名を[!UICONTROL Sheet1]&quot;から&quot;[!UICONTROL RAW].&quot;

         この特定のタブ名は、データの更新を有効にします。

      4. （オプション）必要に応じて、レポートテンプレートの列の右側にカスタム列を追加します。
   1. （オプション）別のワークシートにピボットテーブルを作成します。 完了したら、ピボットテーブルの任意のセルを右クリックし、「 」を選択します **[!UICONTROL Pivot Table Options]**、 **[!UICONTROL Data]** 「 」タブで、「 」を選択します。 **[!UICONTROL Refresh data when opening the file]**.

   1. ファイルを [!DNL Excel] スプレッドシートを.XLSX 形式で指定します。


>[!MORELIKETHIS]
>
>* [スプレッドシートレポートフィードについて](spreadsheet-feed-about.md)
>* [スプレッドシートレポートフィードの作成](spreadsheet-feed-create.md)
>* [スプレッドシートレポートフィード設定の編集](spreadsheet-feed-edit.md)
>* [スプレッドシートレポートフィードの設定](spreadsheet-feed-settings.md)
>* [スプレッドシートレポートフィードファイルの表示または保存](spreadsheet-feed-view-or-save.md)
>* [スプレッドシートレポートフィードを手動で更新](spreadsheet-feed-refresh.md)
>* [スプレッドシートレポートフィードの削除](spreadsheet-feed-delete.md)

