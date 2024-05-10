---
title: キャンペーン管理ビューからのデータのダウンロード
description: ほとんどのキャンペーン管理ビューからデータをダウンロードする方法を説明します。
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# キャンペーン管理ビューからのデータのダウンロード

からデータをダウンロードできます [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] を除くビュー [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences]、および [!UICONTROL Extensions] ビュー。 次のいずれかをダウンロードできます。

* のレポート [!DNL XLSM] （マクロ有効 [!DNL Microsoft Excel] spreadsheet）形式です。 ビューで特定の行を選択した場合、選択した行ごとに 1 行がレポートに含まれます。 行を選択しない場合は、ビューの行ごとに 1 つの行が作成されます。

* 関連するすべての子エンティティを含んだ TXT 形式のバルクシートファイル。 複数の広告ネットワーク上のエンティティに対して行を選択した場合、関連する広告ネットワークごとに 1 つのファイルが作成されます。 行を選択しない場合、ビューに表示される広告ネットワークごとに 1 つのファイルが作成されます。 異なる広告ネットワーク用に生成されたバルクシート ファイルには、異なるデータ列が含まれます。

  複数のキャンペーンのデータを生成し、結合されたデータが 500,000 行を超える場合、データは、必要に応じて、という名前の 2 つ以上のファイルに Campaign でさらに分割されます。 `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`など。

  内の各バルクシートファイル [!UICONTROL Downloads] パネルは次の場所にもリストされます [!UICONTROL Bulksheets] 表示。 ファイルを作成すると、ファイルをダウンロードできるリンクが記載されたメール通知が届きます。コンパイルするデータの量によっては、通知に数分以上かかることがあります。 ただし、ファイルの生成に失敗した場合は、エラーファイルがバルクシート ビューに表示され、エラーファイルへのリンクが記載されたメール通知が届きます。 からバルクシートファイルを削除する [!UICONTROL Download] パネルまたは [!UICONTROL Bulksheets] tab キーを押すと、両方の場所からテンプレートが削除されます。

1. （オプション）ファイルに含める行を個別に選択します。

   それ以外の場合は、ビュー内のすべてのデータが含まれます。

1. ツールバーの右側で、をクリックします ![レポートのダウンロード](/help/search-social-commerce/assets/download.png "レポートのダウンロード").

1. クリック ![作成](/help/search-social-commerce/assets/add.png "作成") **[!UICONTROL Create]**（オプション）ファイル名を追加し、次のいずれかをクリックします **[!UICONTROL Report]** または **[!UICONTROL Bulksheet]**.

1. （オプション）レポートジョブが完了したら、 ![レポートのダウンロード](/help/search-social-commerce/assets/download.png "レポートのダウンロード") を表示するには [!UICONTROL Available Reports] パネルを開き、レポートをダウンロードまたは削除します。

   * ブラウザの通常の手順に従ってファイルを開くか保存するには、をクリックします。 ![スプレッドシートをダウンロード](/help/search-social-commerce/assets/download-spreadsheet.png "スプレッドシートをダウンロード").

     ブラウザの手順の詳細については、ブラウザのオンライン ヘルプを参照してください。

   * ファイルを削除するには、 ![削除](/help/search-social-commerce/assets/delete.png "削除").

>[!MORELIKETHIS]
>
>[からパフォーマンスデータレポートまたはバルクシートファイルを削除する [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
