---
title: キャンペーン管理ビューからのデータのダウンロード
description: ほとんどのキャンペーン管理ビューからデータをダウンロードする方法を説明します。
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# キャンペーン管理ビューからのデータのダウンロード

[!UICONTROL Keywords] - [!UICONTROL Keyword Negatives]、[!UICONTROL Placements] - [!UICONTROL Placement Negatives]、[!UICONTROL Audiences] および [!UICONTROL Extensions] ビューを除き、[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns] ビューからデータをダウンロードできます。 次のいずれかをダウンロードできます。

* [!DNL XLSM] （マクロが有効な [!DNL Microsoft Excel] スプレッドシート）形式のレポート。 ビューで特定の行を選択した場合、選択した行ごとに 1 行がレポートに含まれます。 行を選択しない場合は、ビューの行ごとに 1 つの行が作成されます。

* 関連するすべての子エンティティを含んだ TXT 形式のバルクシートファイル。 複数の広告ネットワーク上のエンティティに対して行を選択した場合、関連する広告ネットワークごとに 1 つのファイルが作成されます。 行を選択しない場合、ビューに表示される広告ネットワークごとに 1 つのファイルが作成されます。 異なる広告ネットワーク用に生成されたバルクシート ファイルには、異なるデータ列が含まれます。

  複数のキャンペーンのデータを生成し、組み合わせたデータが 500,000 行を超える場合は、データが、必要に応じて `<bulksheet name>_1.txt`、`<bulksheet name>_2.txt` などの名前を持つ 2 つ以上のファイルに Campaign でさらに分割されます。

  [!UICONTROL Downloads] パネル内の各バルクシート ファイルも [!UICONTROL Bulksheets] ビューに一覧表示されます。 ファイルを作成すると、ファイルをダウンロードできるリンクが記載されたメール通知が届きます。コンパイルするデータの量によっては、通知に数分以上かかることがあります。 ただし、ファイルの生成に失敗した場合は、エラーファイルがバルクシート ビューに表示され、エラーファイルへのリンクが記載されたメール通知が届きます。 [!UICONTROL Download] のパネルまたは [!UICONTROL Bulksheets] のタブからバルクシート ファイルを削除すると、両方の場所からバルクシート ファイルが削除されます。

1. （オプション）ファイルに含める行を個別に選択します。

   それ以外の場合は、ビュー内のすべてのデータが含まれます。

1. ツールバーの右側にある「![ レポートのダウンロード ](/help/search-social-commerce/assets/download.png " レポートのダウンロード ")」をクリックします。

1. ![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ") **[!UICONTROL Create]** をクリックし、必要に応じてファイル名を追加して、「**[!UICONTROL Report]**」または「**[!UICONTROL Bulksheet]**」をクリックします。

1. （任意）レポートジョブが完了したら、「![ レポートのダウンロード ](/help/search-social-commerce/assets/download.png " レポートのダウンロード ")」をクリックして [!UICONTROL Available Reports] パネルを表示し、レポートをダウンロードまたは削除します。

   * ブラウザーの通常の手順に従ってファイルを開いたり保存したりするには、「![ スプレッドシートをダウンロード ](/help/search-social-commerce/assets/download-spreadsheet.png " スプレッドシートをダウンロード ")」をクリックします。

     ブラウザの手順の詳細については、ブラウザのオンライン ヘルプを参照してください。

   * ファイルを削除するには、「![ 削除 ](/help/search-social-commerce/assets/delete.png " 削除 ")」をクリックします。

>[!MORELIKETHIS]
>
>[[!UICONTROL Downloads] メニューからパフォーマンス データ レポートまたはバルクシート ファイルを削除する ](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
