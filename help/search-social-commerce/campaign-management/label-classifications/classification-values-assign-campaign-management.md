---
title: キャンペーン管理ビューからのアカウントコンポーネントへの分類値の割り当て
description: アカウントコンポーネントに分類値を割り当てる方法を説明します。
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# キャンペーン管理ビューからのアカウントコンポーネントへの分類値の割り当て

キャンペーン管理ビューで、キャンペーン、広告グループ、キーワード、広告、プレースメント、単位レベルの製品グループ、動的検索ターゲットの検索エンティティに対する分類値を割り当て、削除できます。 必要に応じて、割り当てプロセス中に分類と分類値を作成できます。 各ラベル分類には、最大 2000 個の値を設定できます。

各エンティティには、分類ごとに 1 つのラベル値を設定できます。 例えば、Shoes_Campaign では、カラー値が「red」、地域値が「Los Angeles」に設定できますが、カラーと地域に複数の値を設定することはできません。

ラベル値は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードと広告コピーは [&#x200B; 不変 &#x200B;](/help/search-social-commerce/campaign-management/faqs-campaigns.md) です。つまり、それらを編集すると、既存のエンティティが削除され、新しいエンティティが作成されます。 この方法で既存の図形を削除すると、ラベル分類は新しい図形に割り当てられません。

## （新しい UI）アカウントコンポーネントへの分類値の割り当て

新しい UI で使用できる、適用可能なアカウントコンポーネントに分類値を割り当てることができます。

1. **[!UICONTROL Manage]** または **[!UICONTROL Target]** メニューからエンティティビューを開きます。

1. 関連する各行の横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[&#x200B; 複数行を選択 &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. 一括アクションツールバーで、**+[!UICONTROL Assign]**/**[!UICONTROL Label Classification]** をクリックします。

1. 該当する各分類値に対して、次の手順を実行します。

   1. **[!UICONTROL Classifications]** 列で、分類を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、列見出しの [!UICONTROL +] をクリックします。 入力フィールドに分類名を入力し、![&#x200B; 保存 &#x200B;](/help/search-social-commerce/assets/save-checkmark.png " 保存 ") をクリックして、分類をすぐに保存します。 新しい分類を使用するには、分類名をクリックして展開します。

        名前は [ASCII 文字 32 ～ 126](https://www.asciitable.com/) で構成する必要があり、最大長は 27 個のシングルバイト文字です。

   1. **[!UICONTROL Value Name]** 列で、選択した分類の値を指定します。

      * 既存の値を使用するには、値を選択します。

      * 値を作成するには、列見出しの [!UICONTROL +] をクリックします。 入力フィールドに値を入力し、![&#x200B; 保存 &#x200B;](/help/search-social-commerce/assets/save-checkmark.png " 保存 ") をクリックして、すぐに値を保存し、デフォルトで選択します。

        最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

1. **+[!UICONTROL Assign Now]** をクリックします。

## （従来の UI）アカウントコンポーネントへの分類値の割り当て

1. **[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックし、アカウントコンポーネント表示を選択します。

1. 次のいずれかの操作をおこないます。

   * （単一の図形に値を割り当てるには）図形名の上にカーソルを置き、![&#x200B; メニューボタン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューボタン ") をクリックして、**[!UICONTROL Classification]** を選択します。

   * （1 つ以上のエンティティに値を割り当てるには）次の手順を実行します。

      * 関連する各行の横にあるチェックボックスをオンにします。

        複数行の選択に関するヒントについては、「[&#x200B; 複数行を選択 &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      * データ テーブルの上にあるツールバーで、&lbrack;![&#x200B; その他 &#x200B;](/help/search-social-commerce/assets/more.png " を表示 ") をクリックし、[**[!UICONTROL Classification]**] をクリックします。

1. [!UICONTROL Assignment Details] で、次のいずれかの操作を行います。

   * 既存の分類の値を新しい値に変更するには、「**[!UICONTROL Set To]**」を選択します。

     各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

   * 既存の値を削除せずに、指定した分類値を割り当てるには、[**[!UICONTROL Assign]**] を選択します。

   * 現在割り当てられている特定の分類値を削除するには、「**[!UICONTROL Remove]**」を選択します。

     分類値を削除すると、その値のレポートデータは、指定したアカウントコンポーネントで使用できなくなります。

   * 指定した分類値を削除するには、「**[!UICONTROL Delete]**」を選択します。

     分類値を削除すると、その値は今後使用できなくなり、レポートデータはその値では使用できなくなります。 値と特定の勘定科目コンポーネント間のすべての割当ては削除されますが、勘定科目コンポーネントは削除されません。

1. 該当する各分類値に対して、次の手順を実行します。

   1. **[!UICONTROL Classification]** 列で、分類名を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、「分 [!UICONTROL +]」をクリックします。 入力フィールドに分類名を入力し、![&#x200B; 保存 &#x200B;](/help/search-social-commerce/assets/select.png " 保存 ") をクリックして、分類をすぐに保存します。

        名前は [ASCII 文字 32 ～ 126](https://www.asciitable.com/) で構成する必要があり、最大長は 27 個のシングルバイト文字です。

   1. **[!UICONTROL Value Name]** 列で、値の名前を指定します。

      * 既存の値を使用するには、値の名前をクリックして選択します。

      * 値を作成するには、「[!UICONTROL +]」をクリックします。 入力フィールドに値を入力し、![&#x200B; 保存 &#x200B;](/help/search-social-commerce/assets/select.png " 保存 ") をクリックして、すぐに値を保存します。

        最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

1. （オプション）追加の詳細を入力します。

   1. 「**[!UICONTROL Additional Details]**」の横にある「![&#x200B; 開く &#x200B;](/help/search-social-commerce/assets/chevron-up.png " 開く ") をクリックして、詳細を展開します。

   1. オプションの **[!UICONTROL Project Name]** や **[!UICONTROL Description]** を入力します。

1. 「**[!UICONTROL Save]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; ラベル分類について &#x200B;](classification-about.md)
>* [&#x200B; ラベル分類の作成 &#x200B;](classification-create.md)
>* [&#x200B; バルクシートを使用した勘定科目コンポーネントへの分類値の割当て &#x200B;](classification-values-assign-bulksheets.md)
>* [&#x200B; アカウントコンポーネントからラベル分類値を削除する &#x200B;](classification-values-remove.md)
>* [&#x200B; ラベル分類値を削除 &#x200B;](classification-values-delete.md)
>* [&#x200B; ラベル分類を削除 &#x200B;](classification-delete.md)
