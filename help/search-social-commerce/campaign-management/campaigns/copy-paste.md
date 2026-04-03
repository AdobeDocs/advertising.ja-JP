---
title: コピー&ペースト機能を利用してキャンペーンデータを一括作成、編集できます
description: コピー&ペースト機能を使用してキャンペーンデータを一括管理する方法について説明します。
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/z-CaAsySMH-nF2IGPRpM1KY6MYdVz1xZhgjPsBShD7c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 486
ht-degree: 0%

---

# コピー&amp;ペースト機能を利用してキャンペーンデータを一括作成、編集できます

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]および既存の[!DNL Baidu] アカウントのみ*

*[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および[!UICONTROL Ads] ビュー*

[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads]のビューから最大10,000行をコピーし、それらを[!DNL Microsoft Excel]または別のエディターに貼り付けて、ID以外のフィールドを編集できます。 次に、[!DNL Excel]行をコピーし、タブ区切りのデータとしてビューに貼り付けて、変更を加えることができます。 この機能は、コンピューターのクリップボードを使用します。

この機能を使用すると、既存のキャンペーンオブジェクト（ID フィールドを含む）を編集したり、ID フィールドを含まない新しいキャンペーンオブジェクトを作成したりできます。

## データ行をコピー

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**&#x200B;をクリックします。

1. コピーする各行の横にあるチェックボックスをオンにします。

   最大10,000行までコピーできます。

1. データテーブルの上にあるツールバーで、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Copy]**&#x200B;をクリックします。

   または、**[!DNL Ctrl+C]**&#x200B;の[!DNL Microsoft Windows]や&#x200B;**[!DNL Command-C]**&#x200B;の[!DNL Apple Mac]など、オペレーティングシステムの「コピー」キーボードコマンドを使用することもできます。

1. [!UICONTROL Copy to Clipboard] ダイアログで、**[!UICONTROL Continue]**&#x200B;をクリックします。 データをコピーする準備ができたら、**[!UICONTROL Copy]**&#x200B;をクリックします。

1. 行を[!DNL Excel]または別のエディターに貼り付けます。

## データ行の編集と作成

1. 次の要件に従ってデータを編集します。

   * 貼り付けられたデータには、ヘッダー行と必要なキャンペーンオブジェクトの値が含まれている必要があります。[Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)、[Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)、[Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)、[Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)、[Yahoo！の必要なバルクシート列を参照してください。 ディスプレイ ネットワーク &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)、[Yahoo! 日本](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)、および[Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)。 列の順序は問題ありません。

      * 編集する既存のオブジェクトの場合は、編集する関連ID列、エンティティ名、属性をすべて含める必要があります。 オブジェクトの数値IDは編集しないでください。

      * 新しいキャンペーンオブジェクトの場合は、関連するすべてのエンティティ名と属性を含めますが、（自動生成される）オブジェクト IDは含みません。 例えば、新しい広告を作成する場合は、[!UICONTROL Ad ID] フィールドを空白のままにします。 オブジェクトを投稿すると、広告ネットワークが自動的にIDを作成します。

   * 必須でない列の値はnull （空白）である可能性がありますが、各行には同じ数のタブ区切り値が必要です。

1. データをタブ区切りの値として保存します。

## キャンペーン管理ビューへのデータ行のペースト

>[!NOTE]
>
>貼り付けられた行に、既存のエンティティと同じデータが含まれている場合、または既存のエンティティと重複するデータが含まれている場合、重複したデータは無視されます。

1. [!DNL Excel]またはその他のエディターで、関連するタブ区切りの行をコピーします。

1. Search, Social, &amp; Commerce メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 データを貼り付けるビューを開きます（**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**）。

1. データテーブルの上にあるツールバーで、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Paste]**&#x200B;をクリックします。

   または、オペレーティングシステムの「貼り付け」キーボードコマンド（**[!DNL Ctrl+V]**&#x200B;の場合は[!DNL Microsoft Windows]、**[!DNL Command-V]**&#x200B;の場合は[!DNL Apple Mac]）を使用することもできます。

1. 入力ボックスにデータを貼り付け、**[!UICONTROL Process]**&#x200B;をクリックします。

1. （オプション）追加の詳細を入力します。

   * （**[!UICONTROL Additional Details]**&#x200B;が圧縮されている場合）「![開く](/help/search-social-commerce/assets/chevron-up.png "開く")」をクリックして、詳細を展開します。

   * オプションの&#x200B;**[!UICONTROL Job Name]**&#x200B;またはオプションの&#x200B;**[!UICONTROL Job Description]**&#x200B;を入力します。

1. **[!UICONTROL Post Now]**&#x200B;をクリックします。


>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用したキャンペーンデータの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [行内で直接設定を編集](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [&#x200B; キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [広告グループの管理](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [&#x200B; キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [広告の管理](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
