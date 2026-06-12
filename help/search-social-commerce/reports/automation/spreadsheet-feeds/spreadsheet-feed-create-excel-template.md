---
title: スプレッドシート レポートフィード用の [!DNL Excel]  テンプレートの作成
description: 特別な形式のスプレッドシート テンプレートを作成する方法について説明します。
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
TQID: https://experienceleague.adobe.com/bzrRXYVp7SdGXkdLJpJEaHqYIQKx4GF-Cdi5LxqIIa0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 0%

---

# スプレッドシート レポート フィード用の[!DNL Excel] テンプレートの作成

*基本レポートおよびモデル精度レポートのみ*

スプレッドシート フィードを作成するには、まず、通常のレポートテンプレートを使用して、特殊な形式の[!DNL Microsoft Excel] スプレッドシート テンプレートを作成する必要があります。 必要に応じて、[!DNL Excel] スプレッドシートをカスタマイズして、列とグラフを追加できます。

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;で、「[!UICONTROL Daily]」の[!UICONTROL Date Aggregation] ユニットと、必要な他のすべてのデータパラメーターを使用して、目的のレポートタイプを生成し、レポートをテンプレートとして保存します。

   >[!NOTE]
   >
   > * [!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword]、および[!UICONTROL Forecast Accuracy]のレポート用のスプレッドシート フィードを作成できます。 [!UICONTROL Ad Group Report]を使用する場合は、より迅速な結果を得るために含める広告グループの数を制限してください。
   > * テンプレートで定義されている[!UICONTROL Date Range] ユニットは使用されていません。 スプレッドシート フィードを後で設定する際に、データを更新する日付を定義します。

1. レポートを生成したら、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;に移動し、レポート出力のTSVまたはXLS バージョンをファイルに書き出します。

1. [!DNL Excel]で、レポート用のカスタムテンプレートを作成します。

   1. [!DNL Excel]でレポートファイルを開きます。

   1. ワークブックを準備します。

      1. レポートパラメーターを表示する一番上の行を削除します。 XLS ファイルの場合は、「[!UICONTROL Total]」行も削除します。 必要に応じて、データ行の一部を削除できますが、a）元の順序のすべての列を含むデータヘッダー行とb）少なくとも1つのデータ行を保持します。 手動でデータを追加しないでください。

         >[!NOTE]
         >
         > 最後の列には、ゼロ以外の値を含める必要があります。

      2. 開始日で昇順にデータを並べ替えます（最も古いものから最も新しいものまで）。

      3. ワークシートのタブ名を&quot;[!UICONTROL Sheet1]&quot;から&quot;[!UICONTROL RAW]&quot;に変更します。

         この特定のタブ名を使用すると、データを更新できます。

      4. （オプション）必要に応じて、レポートテンプレートの列の右側にカスタム列を追加します。

   1. （オプション）別のワークシートで、ピボットテーブルを作成します。 完了したら、ピボットテーブルの任意のセルを右クリックして&#x200B;**[!UICONTROL Pivot Table Options]**&#x200B;を選択し、「**[!UICONTROL Data]**」タブをクリックしてから「**[!UICONTROL Refresh data when opening the file]**」を選択します。

   1. ファイルを.XLSX形式の[!DNL Excel] スプレッドシートとして保存します。

>[!MORELIKETHIS]
>
>* [ スプレッドシート レポート フィードについて](spreadsheet-feed-about.md)
>* [ スプレッドシート レポート フィードの作成](spreadsheet-feed-create.md)
>* [ スプレッドシート レポート フィード設定の編集](spreadsheet-feed-edit.md)
>* [ スプレッドシート レポート フィード設定](spreadsheet-feed-settings.md)
>* [ スプレッドシート レポート フィード ファイルを表示または保存する](spreadsheet-feed-view-or-save.md)
>* [ スプレッドシート レポート フィードを手動で更新する](spreadsheet-feed-refresh.md)
>* [ スプレッドシート レポート フィードを削除](spreadsheet-feed-delete.md)
