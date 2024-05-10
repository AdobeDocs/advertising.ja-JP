---
title: を作成 [!DNL Excel] スプレッドシートレポートフィードのテンプレート
description: 特別に書式設定されたスプレッドシートテンプレートを作成する方法を説明します。
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# を作成 [!DNL Excel] スプレッドシートレポートフィードのテンプレート

*基本レポートおよびモデル精度レポートのみ*

スプレッドシートフィードを作成するには、まず特別な形式を作成する必要があります [!DNL Microsoft Excel] 通常のレポートテンプレートを使用したスプレッドシートテンプレート。 オプションで、をカスタマイズできます [!DNL Excel] 追加の列とグラフを含めるスプレッドシート。

1. 対象： **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**、を使用して目的のレポートタイプを生成します。 [!UICONTROL Date Aggregation] 単位&quot;[!UICONTROL Daily]」を選択し、必要な他のすべてのデータパラメーターを指定して、レポートをテンプレートとして保存します。

   >[!NOTE]
   >
   > * のスプレッドシートフィードを作成できます [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword]、および [!UICONTROL Forecast Accuracy] レポート。 使用する場合 [!UICONTROL Ad Group Report]含める広告グループの数を制限して、結果を迅速に得られるようにします。
   > * この [!UICONTROL Date Range] テンプレートで定義されている単位は使用されません。 後でスプレッドシートフィードを設定する際に、データを更新する日付を定義します。

1. レポートが生成されたら、に移動します。 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** また、レポート出力の TSV または XLS バージョンをファイルに書き出します。

1. 対象： [!DNL Excel]を作成し、レポート用のカスタムテンプレートを作成します。

   1. でレポートファイルを開きます。 [!DNL Excel].

   1. ワークブックを準備します。

      1. レポートパラメーターを表示する上位の行を削除します。 XLS ファイルの場合、「」も削除します[!UICONTROL Total]``行。 必要に応じて、一部のデータ行を削除することもできますが、a）すべての列が元の順序になっているデータヘッダー行、および b）少なくとも 1 つのデータ行を保持します。 手動でデータを追加しないでください。

         >[!NOTE]
         >
         > 最後の列には 0 以外の値を含める必要があります。

      2. データを開始日の昇順（古い順から新しい順）で並べ替えます。

      3. ワークシートタブ名を「」から変更する[!UICONTROL Sheet1]「」から「」[!UICONTROL RAW].」と入力します。

         この特定のタブ名を使用すると、データを更新できます。

      4. （オプション）必要に応じて、レポートテンプレートの列の右側にカスタム列を追加します。

   1. （オプション）別のワークシートで、ピボットテーブルを作成します。 完了したら、ピボットテーブルの任意のセルを右クリックして選択します **[!UICONTROL Pivot Table Options]**&#x200B;を選択し、 **[!UICONTROL Data]** tab キーを押して選択します **[!UICONTROL Refresh data when opening the file]**.

   1. ファイルをとして保存 [!DNL Excel] .XLSX 形式のスプレッドシート。

>[!MORELIKETHIS]
>
>* [スプレッドシートレポートフィードについて](spreadsheet-feed-about.md)
>* [スプレッドシートレポートフィードの作成](spreadsheet-feed-create.md)
>* [スプレッドシートレポートフィード設定の編集](spreadsheet-feed-edit.md)
>* [スプレッドシートレポートフィードの設定](spreadsheet-feed-settings.md)
>* [スプレッドシート レポート フィード ファイルの表示または保存](spreadsheet-feed-view-or-save.md)
>* [スプレッドシートレポートフィードを手動で更新](spreadsheet-feed-refresh.md)
>* [スプレッドシートレポートフィードの削除](spreadsheet-feed-delete.md)
