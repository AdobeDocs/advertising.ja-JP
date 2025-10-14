---
title: コピーと貼り付けを使用したキャンペーンデータの一括作成と編集
description: コピーと貼り付け機能を使用して、Campaign データを一括管理する方法を説明します。
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# コピーと貼り付けを使用したキャンペーンデータの一括作成と編集

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex] および既存の [!DNL Baidu] アカウントのみ*

*[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords] および [!UICONTROL Ads] ビュー*

[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords] および [!UICONTROL Ads] ビューから最大 10,000 行をコピーし、[!DNL Microsoft Excel] または別のエディターに貼り付けて、非 ID フィールドを編集できます。 その後、[!DNL Excel] の行をコピーし、タブ区切りデータとして貼り付けてビューに戻し、変更を行うことができます。 この機能はコンピュータのクリップボードを使用します。

この機能を使用すると、ID フィールドを持つ既存のキャンペーンオブジェクトを編集したり、ID フィールドを持たない新しいキャンペーンオブジェクトを作成したりできます。

## データ行のコピー

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]** をクリックします。

1. コピーする各行の横にあるチェックボックスをオンにします。

   最大 10,000 行までコピーできます。

1. データ テーブルの上にあるツールバーで、&lbrack;![&#x200B; その他 &#x200B;](/help/search-social-commerce/assets/more.png " を表示 ") をクリックし、[**[!UICONTROL Copy]**] をクリックします。

   または、オペレーティングシステムの「コピー」キーボードコマンド（[!DNL Microsoft Windows] の場合は **[!DNL Ctrl+C]**、[!DNL Apple Mac] の場合は **[!DNL Command-C]** など）を使用できます。

1. [!UICONTROL Copy to Clipboard] ダイアログで、「**[!UICONTROL Continue]**」をクリックします。 データをコピーする準備ができたら、「**[!UICONTROL Copy]**」をクリックします。

1. 行を [!DNL Excel] または別のエディターに貼り付けます。

## データ行の編集と作成

1. 次の要件に従ってデータを編集します。

   * 貼り付けたデータには、ヘッダー行と必要なキャンペーンオブジェクト値が含まれている必要があります。[Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)、[Google広告 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)、[Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)、&lbrace;Naver[、Yahoo](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md) の必須のバルクシート列を参照してください [&#x200B; ディスプレイのネットワーク &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)、[Yahoo! 日本 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)、および [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md) 列の順序は関係ありません。

      * 編集する既存のオブジェクトの場合、関連するすべての ID 列、エンティティ名、編集する属性を含める必要があります。 オブジェクトの数値 ID を編集しないでください。

      * 新しいキャンペーンオブジェクトの場合、関連するすべてのエンティティ名と属性を含めますが、（自動的に生成される）オブジェクト ID は含めないでください。 例えば、新しい広告を作成する場合、「[!UICONTROL Ad ID]」フィールドは空白のままにします。 オブジェクトを投稿すると、広告ネットワークによって ID が自動的に作成されます。

   * 必須でない列の値は null （空白）にすることができますが、各行のタブ区切り値の数は同じにする必要があります。

1. データをタブ区切り値として保存します。

## キャンペーン管理ビューへのデータ行の貼り付け

>[!NOTE]
>
>貼り付けた行に、既存のエンティティと同じデータが含まれている場合や、既存のエンティティと重複するデータが含まれている場合、重複するデータは無視されます。

1. [!DNL Excel] または他のエディターで、関連するタブ区切りの行をコピーします。

1. 検索、ソーシャル、Commerceのメインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 データを貼り付けるビューを開きます（**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**）。

1. データ テーブルの上にあるツールバーで、&lbrack;![&#x200B; その他 &#x200B;](/help/search-social-commerce/assets/more.png " を表示 ") をクリックし、[**[!UICONTROL Paste]**] をクリックします。

   または、オペレーティングシステムの「貼り付け」キーボードコマンド（[!DNL Microsoft Windows] の場合は **[!DNL Ctrl+V]**、[!DNL Apple Mac] の場合は **[!DNL Command-V]** など）を使用できます。

1. データを入力ボックスに貼り付け、[**[!UICONTROL Process]**] をクリックします。

1. （オプション）追加の詳細を入力します。

   * （**[!UICONTROL Additional Details]** が圧縮されている場合） ![&#x200B; 開く &#x200B;](/help/search-social-commerce/assets/chevron-up.png " 開く ") をクリックして詳細を展開します。

   * オプションの **[!UICONTROL Job Name]** や **[!UICONTROL Job Description]** を入力します。

1. 「**[!UICONTROL Post Now]**」をクリックします。


>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用した Campaign データの管理について &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [&#x200B; 行内で設定を直接編集する &#x200B;](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [&#x200B; キャンペーンの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [&#x200B; 広告グループの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [&#x200B; キーワードの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [&#x200B; 広告の管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
