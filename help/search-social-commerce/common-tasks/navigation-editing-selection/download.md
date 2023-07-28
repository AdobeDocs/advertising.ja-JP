---
title: キャンペーン管理ビューからのデータのダウンロード
description: ほとんどのキャンペーン管理ビューからデータをダウンロードする方法を説明します。
exl-id: 0bbb02df-2ee0-4610-b60a-ca2b58daadbb
feature: Search Common Tasks
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# キャンペーン管理ビューからのデータのダウンロード

データは、 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] を除くビュー [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences]、および [!UICONTROL Extensions] ビュー。 次のいずれかをダウンロードできます。

* のレポート [!DNL XLSM] （マクロが有効） [!DNL Microsoft® Excel] スプレッドシート ) 形式で書き出します。 ビューで特定の行を選択した場合、レポートには選択した行ごとに 1 つの行が含まれます。 行を選択しない場合、ビューの各行に対して 1 つの行が作成されます。

* 関連するすべての子エンティティを含む、TXT 形式のバルクシートファイル。 複数の広告ネットワーク上のエンティティの行を選択した場合、関連する広告ネットワークごとに 1 つのファイルが作成されます。 行を選択しない場合、ビューに表示される広告ネットワークごとに 1 つのファイルが作成されます。 異なる広告ネットワーク用に生成されたバルクシートファイルには、異なるデータ列が含まれます。

  複数のキャンペーンのデータを生成し、結合されたデータが 500,000 行を超える場合、データはキャンペーンごとにさらに 2 つ以上のファイルに分割され、必要に応じて、 `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`など。

  各バルクシートファイル ( [!UICONTROL Downloads] パネルは、 [!UICONTROL Bulksheets] 表示。 ファイルを作成すると、そのファイルのダウンロード元となるリンクが記載された電子メール通知が届きます。コンパイルされるデータの量によっては、通知に数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルが Bulksheets ビューに表示され、エラーファイルへのリンクを含む電子メール通知が届きます。 次の場所からバルクシートファイルを削除する： [!UICONTROL Download] パネルまたは [!UICONTROL Bulksheets] 「 」タブでは、両方の場所から削除されます。

1. （オプション）ファイルに含める個々の行を選択します。

   それ以外の場合は、ビュー内のすべてのデータが含まれます。

1. ツールバーの右側で、 ![レポートのダウンロード](/help/search-social-commerce/assets/download.png "レポートのダウンロード").

1. クリック ![作成](/help/search-social-commerce/assets/add.png "作成") **[!UICONTROL Create]**&#x200B;をクリックし、必要に応じてファイル名を追加して、 **[!UICONTROL Report]** または **[!UICONTROL Bulksheet]**.

1. （オプション）レポートジョブが完了したら、 ![レポートのダウンロード](/help/search-social-commerce/assets/download.png "レポートのダウンロード") 表示する [!UICONTROL Available Reports] パネルに表示され、次の操作を行って、レポートをダウンロードまたは削除します。

   * ブラウザーの通常の手順に従ってファイルを開くか保存するには、 ![スプレッドシートをダウンロード](/help/search-social-commerce/assets/download-spreadsheet.png "スプレッドシートをダウンロード").

     ブラウザの手順の詳細については、ご使用のブラウザのオンラインヘルプを参照してください。

   * ファイルを削除するには、 ![削除](/help/search-social-commerce/assets/delete.png "削除").

>[!MORELIKETHIS]
>
>[パフォーマンスデータレポートまたはバルクシートファイルを [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
