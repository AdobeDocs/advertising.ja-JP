---
title: スプレッドシートレポ  [!DNL Excel]  トフィード用のテンプレートの作成
description: 特別に書式設定されたスプレッドシートテンプレートを作成する方法を説明します。
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# スプレッドシートレポートフィード用の [!DNL Excel] テンプレートの作成

*基本レポートおよびモデル精度レポートのみ*

スプレッドシートフィードを作成するには、まず、通常のレポートテンプレートを使用して、特別な形式の [!DNL Microsoft Excel] スプレッドシートテンプレートを作成する必要があります。 必要に応じて、[!DNL Excel] スプレッドシートをカスタマイズして、列とグラフを追加できます。

1. **[!UICONTROL Search]/[!UICONTROL Insights & Reports]/[!UICONTROL Reports]** で、[!UICONTROL Date Aggregation] 単位「[!UICONTROL Daily]」を使用し、必要なその他すべてのデータパラメーターを使用して目的のレポートタイプを生成し、レポートをテンプレートとして保存します。

   >[!NOTE]
   >
   > * [!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword] および [!UICONTROL Forecast Accuracy] レポートのスプレッドシートフィードを作成できます。 [!UICONTROL Ad Group Report] を使用する場合は、結果を迅速に得るために、含める広告グループの数を制限します。
   > * テンプレートで定義されている [!UICONTROL Date Range] 単位は使用されません。 後でスプレッドシートフィードを設定する際に、データを更新する日付を定義します。

1. レポートが生成されたら、**[!UICONTROL Search]/ [!UICONTROL Insights & Reports] /[!UICONTROL Reports]** に移動し、レポート出力の TSV または XLS バージョンをファイルに書き出します。

1. [!DNL Excel] で、レポートのカスタムテンプレートを作成します。

   1. [!DNL Excel] でレポートファイルを開きます。

   1. ワークブックを準備します。

      1. レポートパラメーターを表示する上位の行を削除します。 XLS ファイルの場合は、「[!UICONTROL Total]」行も削除します。 必要に応じて、一部のデータ行を削除することもできますが、a）すべての列が元の順序になっているデータヘッダー行、および b）少なくとも 1 つのデータ行を保持します。 手動でデータを追加しないでください。

         >[!NOTE]
         >
         > 最後の列には 0 以外の値を含める必要があります。

      2. データを開始日の昇順（古い順から新しい順）で並べ替えます。

      3. ワークシートタブ名を「[!UICONTROL Sheet1]」から「[!UICONTROL RAW]」に変更します。

         この特定のタブ名を使用すると、データを更新できます。

      4. （オプション）必要に応じて、レポートテンプレートの列の右側にカスタム列を追加します。

   1. （オプション）別のワークシートで、ピボットテーブルを作成します。 完了したら、ピボットテーブルの任意のセルを右クリックして「**[!UICONTROL Pivot Table Options]**」を選択し、「**[!UICONTROL Data]**」タブをクリックして「**[!UICONTROL Refresh data when opening the file]**」を選択します。

   1. ファイルを.XLSX 形式の [!DNL Excel] スプレッドシートとして保存します。

>[!MORELIKETHIS]
>
>* [ スプレッドシートレポートフィードについて ](spreadsheet-feed-about.md)
>* [ スプレッドシートレポートフィードの作成 ](spreadsheet-feed-create.md)
>* [ スプレッドシートレポートフィード設定の編集 ](spreadsheet-feed-edit.md)
>* [ スプレッドシートレポートフィードの設定 ](spreadsheet-feed-settings.md)
>* [ スプレッドシートレポートフィードファイルの表示または保存 ](spreadsheet-feed-view-or-save.md)
>* [ スプレッドシートレポートフィードを手動で更新 ](spreadsheet-feed-refresh.md)
>* [ スプレッドシートレポートフィードの削除 ](spreadsheet-feed-delete.md)
