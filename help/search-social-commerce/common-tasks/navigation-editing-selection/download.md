---
title: キャンペーン管理ビューからデータをダウンロードする
description: ほとんどのキャンペーン管理ビューからデータをダウンロードする方法を説明します。
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
TQID: https://experienceleague.adobe.com/Wg-OZ-59-SkdA96KQgLWuY8seK10bK0tnt94TdKXzeQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 433
ht-degree: 0%

---

# （従来のUI） キャンペーン管理ビューからのデータのダウンロード

*レガシーユーザーインターフェイス*

[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] ビューからデータをダウンロードできます。ただし、[!UICONTROL Keywords] - [!UICONTROL Keyword Negatives]、[!UICONTROL Placements] - [!UICONTROL Placement Negatives]、[!UICONTROL Audiences]、および[!UICONTROL Extensions] ビューは除きます。 次のいずれかをダウンロードできます。

* [!DNL XLSM] （マクロ対応[!DNL Microsoft Excel] スプレッドシート）形式のレポート。 ビューで特定の行を選択すると、選択した各行に1行がレポートに含まれます。 行を選択しない場合は、ビューの各行に1行が作成されます。

* 関連するすべての子エンティティを含むTXT形式のバルクシートファイル。 複数の広告ネットワーク上のエンティティの行を選択すると、関連する広告ネットワークごとに1つのファイルが作成されます。 行を選択しない場合は、ビューに表示される広告ネットワークごとに1つのファイルが作成されます。 広告ネットワークごとに生成されたバルクシートファイルには、様々なデータ列が含まれます。

  複数のキャンペーンのデータを生成し、結合されたデータが500,000行を超える場合、データはキャンペーンによってさらに2つ以上のファイルに分割され、必要に応じて`<bulksheet name>_1.txt`、`<bulksheet name>_2.txt`などの名前が付けられます。

  [!UICONTROL Downloads] パネルの各バルクシート ファイルも[!UICONTROL Bulksheets] ビューに一覧表示されます。 ファイルが作成されると、ファイルのダウンロード元のリンクを含むメール通知が届きます。コンパイルされるデータ量によっては、通知に数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルがバルクシート ビューに表示され、エラーファイルへのリンクを含むメール通知が届きます。 [!UICONTROL Download] パネルまたは[!UICONTROL Bulksheets] タブからバルクシート ファイルを削除すると、両方の場所から削除されます。

>[!NOTE]
>
>「[[!UICONTROL Portfolios] ビュー](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)」、「[[!UICONTROL Campaigns] ビュー](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)」、「[[!UICONTROL Ad Groups] ビュー](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)」から新しいユーザーインターフェイスにデータをダウンロードする際のヘルプも参照してください。

1. （オプション）ファイルに含める個々の行を選択します。

   それ以外の場合は、ビュー内のすべてのデータが含まれます。

1. ツールバーの右側にある「![&#x200B; レポートのダウンロード &#x200B;](/help/search-social-commerce/assets/download.png " レポートのダウンロード ")」をクリックします。

1. ![作成](/help/search-social-commerce/assets/add.png "作成") **[!UICONTROL Create]**&#x200B;をクリックし、オプションでファイル名を追加してから、**[!UICONTROL Report]**&#x200B;または&#x200B;**[!UICONTROL Bulksheet]**&#x200B;のいずれかをクリックします。

1. （オプション）レポートジョブが完了したら、![&#x200B; レポートのダウンロード &#x200B;](/help/search-social-commerce/assets/download.png " レポートのダウンロード ")をクリックして[!UICONTROL Available Reports] パネルを表示し、レポートをダウンロードまたは削除します。

   * ブラウザーの通常の手順に従ってファイルを開くか保存するには、![&#x200B; スプレッドシートのダウンロード &#x200B;](/help/search-social-commerce/assets/download-spreadsheet.png " スプレッドシートのダウンロード ")をクリックします。

     ブラウザーの手順について詳しくは、ブラウザーのオンラインヘルプを参照してください。

   * ファイルを削除するには、![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; （従来のUI） [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)からパフォーマンス データ レポートまたはバルクシート ファイルを削除します
>* [&#x200B; （新しいUI） [!UICONTROL Portfolios] ビュー](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)からデータビューレポートを管理します
>* [&#x200B; （新しいUI） [!UICONTROL Campaigns] ビュー](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)からデータビューレポートを管理します
>* [&#x200B; （新しいUI） [!UICONTROL Ad Groups] ビュー](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)からデータビューレポートを管理します
