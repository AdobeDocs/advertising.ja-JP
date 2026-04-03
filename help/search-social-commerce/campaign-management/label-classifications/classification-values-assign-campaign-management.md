---
title: キャンペーン管理ビューからアカウントコンポーネントに分類値を割り当て
description: アカウントコンポーネントに分類値を割り当てる方法について説明します。
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
TQID: https://experienceleague.adobe.com/r08RxDrdXIkUP7ZJgw8x-g47m0Ioxjo9SySjg71-PkM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 764
ht-degree: 0%

---

# キャンペーン管理ビューからアカウントコンポーネントに分類値を割り当て

キャンペーン管理ビューから、キャンペーン、広告グループ、キーワード、広告、プレースメント、ユニットレベルの製品グループ、動的検索ターゲットの次の検索エンティティの分類値を割り当てて削除できます。 必要に応じて、割り当てプロセス中に分類と分類値を作成できます。 各ラベル分類には、最大2000個の値を指定できます。

各エンティティは、分類ごとに1つのラベル値を持つことができます。 例えば、Shoes_Campaignでは、「Color」の値に「red」を、Geoの値に「Los Angeles」を指定できますが、「Color」または「Geo」に複数の値を指定することはできません。

ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードと広告コピーは[変更不可](/help/search-social-commerce/campaign-management/faqs-campaigns.md)です。これは、編集すると既存のエンティティが削除され、新しいエンティティが作成されることを意味します。 この方法で既存のエンティティが削除された場合、ラベル分類は新しいエンティティに割り当てられません。

## （新しいUI）分類の値をアカウントコンポーネントに割り当て

新しいUIで使用可能な該当するアカウントコンポーネントに分類値を割り当てることができます。

1. **[!UICONTROL Manage]**&#x200B;または&#x200B;**[!UICONTROL Target]** メニューからエンティティ ビューを開きます。

1. 各関連行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 適用できる各分類値について、次の操作を行います。

   1. **[!UICONTROL Classifications]**&#x200B;列で、分類を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、列見出しの[!UICONTROL +]をクリックします。 入力フィールドに分類名を入力し、![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")をクリックして、分類をすぐに保存します。 新しい分類を使用するには、分類名をクリックして展開します。

        名前は[ASCII文字32 ～ 126](https://www.asciitable.com/)で、最大長は27文字です。

   1. **[!UICONTROL Value Name]**&#x200B;列で、選択した分類の値を指定します。

      * 既存の値を使用するには、値を選択します。

      * 値を作成するには、列見出しの[!UICONTROL +]をクリックします。 入力フィールドに値を入力し、![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")をクリックして値をすばやく保存し、デフォルトで選択します。

        最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

1. **+[!UICONTROL Assign Now]**&#x200B;をクリックします。

## （従来のUI）分類の値をアカウントコンポーネントに割り当て

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックし、アカウントコンポーネントビューを選択します。

1. 次のいずれかの操作を行います。

   * （1つのエンティティに値を割り当てるには） エンティティ名の上にカーソルを置き、![ メニューボタン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューボタン ")をクリックし、**[!UICONTROL Classification]**&#x200B;を選択します。

   * （1つ以上のエンティティに値を割り当てるには）次の操作を行います。

      * 各関連行の横にあるチェックボックスをオンにします。

        複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      * データテーブルの上にあるツールバーで、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Classification]**&#x200B;をクリックします。

1. [!UICONTROL Assignment Details]で、次のいずれかの操作を行います。

   * 既存の分類値を新しい値に変更するには、**[!UICONTROL Set To]**&#x200B;を選択します。

     各値の最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

   * 既存の値を削除せずに指定された分類値を割り当てるには、**[!UICONTROL Assign]**&#x200B;を選択します。

   * 現在割り当てられている特定の分類値を削除するには、**[!UICONTROL Remove]**&#x200B;を選択します。

     分類値を削除すると、その値のレポートデータは、指定されたアカウントコンポーネントでは使用できなくなります。

   * 指定した分類値を削除するには、**[!UICONTROL Delete]**&#x200B;を選択します。

     分類値を削除すると、後で使用できなくなり、その値に対するレポートデータは使用できなくなります。 値と特定のアカウントコンポーネント間のすべての割り当ては削除されますが、アカウントコンポーネントは削除されません。

1. 適用できる各分類値について、次の操作を行います。

   1. **[!UICONTROL Classification]**&#x200B;列で、分類名を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、[!UICONTROL +]をクリックします。 入力フィールドに分類名を入力し、![保存](/help/search-social-commerce/assets/select.png "保存")をクリックして、分類をすぐに保存します。

        名前は[ASCII文字32 ～ 126](https://www.asciitable.com/)で、最大長は27文字です。

   1. **[!UICONTROL Value Name]**&#x200B;列で、値の名前を指定します。

      * 既存の値を使用するには、値の名前をクリックして選択します。

      * 値を作成するには、[!UICONTROL +]をクリックします。 入力フィールドに値を入力し、![保存](/help/search-social-commerce/assets/select.png "保存")をクリックして、値をすぐに保存します。

        最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

1. （オプション）追加の詳細を入力します。

   1. **[!UICONTROL Additional Details]**&#x200B;の横にある![開く](/help/search-social-commerce/assets/chevron-up.png "開く")をクリックして、詳細を展開します。

   1. オプションの&#x200B;**[!UICONTROL Project Name]**&#x200B;またはオプションの&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ ラベル分類について](classification-about.md)
>* [ ラベル分類を作成](classification-create.md)
>* [ バルクシートを使用してアカウントコンポーネントに分類値を割り当てる](classification-values-assign-bulksheets.md)
>* [ アカウントコンポーネントからラベル分類値を削除](classification-values-remove.md)
>* [ ラベル分類値を削除](classification-values-delete.md)
>* [ ラベル分類を削除](classification-delete.md)
