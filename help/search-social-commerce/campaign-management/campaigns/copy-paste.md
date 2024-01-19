---
title: コピー&ペーストを使用して、キャンペーンデータを一括で作成および編集する
description: コピー&ペースト機能を使用して、キャンペーンデータを一括管理する方法を説明します。
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# コピー&amp;ペーストを使用して、キャンペーンデータを一括で作成および編集する

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]、および既存 [!DNL Baidu] アカウントのみ*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] ビュー*

最大 10,000 行までを [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] ビューを表示し、 [!DNL Microsoft Excel] または別のエディターを使用して、ID 以外のフィールドを編集することもできます。 その後、 [!DNL Excel] 行を編集し、タブ区切りのデータとしてビューに貼り付けて、変更を加えます。 この機能は、コンピューターのクリップボードを使用します。

この機能を使用すると、既存のキャンペーンオブジェクト（ID フィールドを含む）を編集したり、ID フィールドを含まない新しいキャンペーンオブジェクトを作成したりできます。

## データ行のコピー

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. コピーする各行の横にあるチェックボックスをオンにします。

   最大 10,000 行までコピーできます。

1. データテーブルの上にあるツールバーで、 ![その他](/help/search-social-commerce/assets/more.png "その他")をクリックし、 **[!UICONTROL Copy]**.

   または、次のように、オペレーティングシステムの「copy」キーボードコマンドを使用できます。 **[!DNL Ctrl+C]** 対象： [!DNL Microsoft Windows] または **[!DNL Command-C]** 対象： [!DNL Apple Mac].

1. Adobe Analytics の [!UICONTROL Copy to Clipboard] ダイアログ、クリック **[!UICONTROL Continue]**. データをコピーする準備が整ったら、「 **[!UICONTROL Copy]**.

1. 行の貼り付け先 [!DNL Excel] または別の編集者。

## データ行の編集と作成

1. 次の要件に従ってデータを編集します。

   * 貼り付けたデータには、ヘッダー行と campaign オブジェクトに必要な値が含まれている必要があります。次に示す必要なバルクシート列を参照してください。 [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [ネーバー](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! ネットワークを表示](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! 日本](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)、および [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). 列の順序は関係ありません。

      * 既存のオブジェクトを編集する場合は、関連する ID 列、エンティティ名、編集する属性をすべて含める必要があります。 オブジェクトの数値 ID は編集しないでください。

      * 新しいキャンペーンオブジェクトの場合は、関連するすべてのエンティティ名と属性を含めますが、オブジェクト ID（自動生成される）は含めません。 例えば、新しい広告を作成する場合、 [!UICONTROL Ad ID] フィールドが空白です。 オブジェクトの投稿時に、広告ネットワークが ID を自動的に作成します。

   * 不要な列の値は null（空白）にすることができますが、各行のタブ区切り値は同数にする必要があります。

1. データをタブ区切り値として保存します。

## キャンペーン管理ビューにデータ行を貼り付ける

>[!NOTE]
>
>貼り付けられた行に、既存のエンティティと同じデータまたは既存のエンティティと重複するデータが含まれている場合、重複データは無視されます。

1. In [!DNL Excel] または他のエディターでは、関連するタブ区切りの行をコピーします。

1. 検索、ソーシャル、コマースのメインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. データを貼り付けるビューを開きます (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**) をクリックします。

1. データテーブルの上にあるツールバーで、 ![その他](/help/search-social-commerce/assets/more.png "その他")をクリックし、 **[!UICONTROL Paste]**.

   または、次のように、オペレーティングシステムの「貼り付け」キーボードコマンドを使用できます。 **[!DNL Ctrl+V]** 対象： [!DNL Microsoft Windows] または **[!DNL Command-V]** 対象： [!DNL Apple Mac].

1. 入力ボックスにデータを貼り付け、「 **[!UICONTROL Process]**.

1. （オプション）追加の詳細を入力します。

   * ( **[!UICONTROL Additional Details]** 圧縮済み ) クリック ![開く](/help/search-social-commerce/assets/chevron-up.png "開く") をクリックして詳細を展開します。

   * オプションを入力 **[!UICONTROL Job Name]** および/またはオプション **[!UICONTROL Job Description]**.

1. クリック **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [行内で直接設定を編集](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [広告グループの管理](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [広告の管理](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
