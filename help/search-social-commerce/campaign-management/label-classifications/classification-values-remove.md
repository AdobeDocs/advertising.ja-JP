---
title: アカウントコンポーネントからのラベル分類値の削除
description: ラベル分類値とアカウントコンポーネントの関連付けを削除する方法について説明します。
exl-id: 8697367b-0bf9-48c9-8dd3-e733360e1df2
feature: Search Label Classifications
TQID: https://experienceleague.adobe.com/xT4LpYXeTtuptPWK-HNQPylOzCFi1TT2FfbfEiuSJeo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# アカウントコンポーネントからのラベル分類値の削除

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

>[!NOTE]
>
>ラベル分類から値を削除するには、「[ ラベル分類値を削除](classification-values-delete.md)」を参照してください。

## （新しいUI）アカウントコンポーネントからのラベル分類値の削除

新しいUIで使用可能な該当するアカウントコンポーネントから分類値を削除できます。

1. **[!UICONTROL Manage]**&#x200B;または&#x200B;**[!UICONTROL Target]** メニューからエンティティ ビューを開きます。

1. 各関連行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられた値をすべて選択解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

## （従来のUI）アカウントコンポーネントからのラベル分類値の削除

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;で、エンティティ ビューを選択します。

1. 次のいずれかの操作を行います。

   * （単一のエンティティから値を削除するには） エンティティ名の上にカーソルを置き、![ メニューボタン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューボタン ")をクリックし、**[!UICONTROL Classification]**&#x200B;を選択します。

   * （1つ以上のエンティティから値を削除するには）次の操作を行います。

      * 各行の横にあるチェックボックスをオンにします。

        複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      * データテーブルの上にあるツールバーで、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Classification]**&#x200B;をクリックします。

1. [!UICONTROL Assignment Details]で、**[!UICONTROL Remove]**&#x200B;を選択します。

1. 削除する各分類値について、次の操作を行います。

   * **[!UICONTROL Classification]**&#x200B;列で、分類名をクリックして展開します。

   * **[!UICONTROL Value Name]**&#x200B;列で、値の名前をクリックして選択します。

1. （オプション）追加の詳細を入力します。

   * **[!UICONTROL Additional Details]**&#x200B;の横にある![開く](/help/search-social-commerce/assets/chevron-up.png "開く")をクリックして、詳細を展開します。

   * オプションの&#x200B;**[!UICONTROL Project Name]**&#x200B;またはオプションの&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

   * **[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ ラベル分類について](classification-about.md)
>* [ ラベル分類を作成](classification-create.md)
>* [ キャンペーン管理ビューからアカウントコンポーネントに分類値を割り当てる](classification-values-assign-campaign-management.md)
>* [ バルクシートを使用してアカウントコンポーネントに分類値を割り当てる](classification-values-assign-bulksheets.md)
>* [ ラベル分類値を削除](classification-values-delete.md)
>* [ ラベル分類を削除](classification-delete.md)
