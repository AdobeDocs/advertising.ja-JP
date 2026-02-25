---
title: アカウントコンポーネントからラベル分類値を削除
description: ラベル分類値とアカウントコンポーネント間の関連付けを削除する方法を説明します。
exl-id: 8697367b-0bf9-48c9-8dd3-e733360e1df2
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# アカウントコンポーネントからラベル分類値を削除

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値もアカウントのコンポーネントも削除されません。

>[!NOTE]
>
>ラベル分類から値を削除するには、「[&#x200B; ラベル分類値の削除 &#x200B;](classification-values-delete.md)」を参照してください。

## （新しい UI）アカウントコンポーネントからのラベル分類値の削除

新しい UI で使用できる、該当するアカウントコンポーネントから分類値を削除できます。

1. **[!UICONTROL Manage]** または **[!UICONTROL Target]** メニューからエンティティビューを開きます。

1. 関連する各行の横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[&#x200B; 複数行を選択 &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. 一括アクションツールバーで、**-[!UICONTROL Unassign]**/**[!UICONTROL Label Classification]** をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   割り当てられたすべての値を選択するには、「**[!UICONTROL Select All]**」をクリックします。 割り当てられている値をすべて選択解除するには、「**[!UICONTROL Deselect All]**」をクリックします。

1. 「**[!UICONTROL Unassign Selected]**」をクリックします。

## （レガシー UI）アカウントコンポーネントからラベル分類値を削除する

1. **[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** で、エンティティ表示を選択します。

1. 次のいずれかの操作をおこないます。

   * （1 つの図形から値を削除するには）図形名の上にカーソルを置き、![&#x200B; メニューボタン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューボタン ") をクリックして、**[!UICONTROL Classification]** を選択します。

   * （1 つ以上のエンティティから値を削除するには）次の手順を実行します。

      * 各行の横にあるチェックボックスをオンにします。

        複数行の選択に関するヒントについては、「[&#x200B; 複数行を選択 &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      * データ テーブルの上にあるツールバーで、&lbrack;![&#x200B; その他 &#x200B;](/help/search-social-commerce/assets/more.png " を表示 ") をクリックし、[**[!UICONTROL Classification]**] をクリックします。

1. [!UICONTROL Assignment Details] で、「**[!UICONTROL Remove]**」を選択します。

1. 削除する分類値ごとに、次の操作を行います。

   * **[!UICONTROL Classification]** 列で、分類名をクリックして展開します。

   * **[!UICONTROL Value Name]** 列で、値の名前をクリックして選択します。

1. （オプション）追加の詳細を入力します。

   * 「**[!UICONTROL Additional Details]**」の横にある「![&#x200B; 開く &#x200B;](/help/search-social-commerce/assets/chevron-up.png " 開く ") をクリックして、詳細を展開します。

   * オプションの **[!UICONTROL Project Name]** や **[!UICONTROL Description]** を入力します。

   * 「**[!UICONTROL Save]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; ラベル分類について &#x200B;](classification-about.md)
>* [&#x200B; ラベル分類の作成 &#x200B;](classification-create.md)
>* [&#x200B; キャンペーン管理ビューからアカウントコンポーネントへの分類値の割り当て &#x200B;](classification-values-assign-campaign-management.md)
>* [&#x200B; バルクシートを使用した勘定科目コンポーネントへの分類値の割当て &#x200B;](classification-values-assign-bulksheets.md)
>* [&#x200B; ラベル分類値を削除 &#x200B;](classification-values-delete.md)
>* [&#x200B; ラベル分類を削除 &#x200B;](classification-delete.md)
