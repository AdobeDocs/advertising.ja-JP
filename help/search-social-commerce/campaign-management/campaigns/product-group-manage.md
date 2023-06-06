---
title: 買い物製品グループの管理
description: 買い物キャンペーンで買い物製品グループを作成および管理する方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# 買い物製品グループの管理

*[!DNL Google Ads]および [!DNL Microsoft Advertising] ショッピングキャンペーンのみ*

で、製品グループを作成および編集したり、製品グループとその子製品グループを削除したりできます。 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 表示

## 「[!UICONTROL All Products]&quot;製品グループ&quot;

特定の属性を持つ製品グループを作成する前に、「[!UICONTROL All Products].&quot; 各広告グループに設定できる「[!UICONTROL All Products]&quot;グループ。

>[!TIP]
>
>一度に多数のアカウントコンポーネントを作成するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、 **[!UICONTROL Continue]**.

1. 次を指定： [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md) または [[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md).

1. クリック **[!UICONTROL Post]**.

## 既存の製品グループに子製品グループノードを作成する

少なくともすべてを含む「[!UICONTROL All Products]&quot;広告グループの場合、製品のサブセットに対して子製品グループノードを作成し、各レベルで 1 つ以上の製品グループが同じ属性 ( 例えば、 [!UICONTROL Brand]=1 つの製品グループの Acme および [!UICONTROL Brand]=AcmePlus（同じレベルの別のの） 子製品グループノードは、「[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>「[!UICONTROL Everything Else]&quot;製品グループ。

>[!TIP]
>
>一度に多数のアカウントコンポーネントを作成するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. （オプション）製品グループとその子製品グループノードをツリー表示で表示するには、製品グループ名の上にカーソルを置いたまま、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL Tree View]**.

1. 製品グループ名の上にカーソルを置き、 ![矢印ドロップダウンメニュー](/help/search-social-commerce/assets/arrow-dropdown-menu.png "矢印ドロップダウンメニュー")を選択し、 **[!UICONTROL + Add Node]**.

1. 次を指定： [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md) または [[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)（製品ディメンションと属性を含む）

1. クリック **[!UICONTROL Post]**.

## 製品グループノード設定の編集

広告グループに含まれる単体製品グループノード（子製品グループノードのない製品グループ）の入札およびトラッキングテンプレートを編集できます。 子の製品グループノードを持つ製品グループである、除外された単体製品グループや、含まれるまたは除外されたサブ分割ノードに関する情報は編集できません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. （オプション）製品グループとその子製品グループノードをツリー表示で表示するには、製品グループ名の上にカーソルを置いたまま、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL Tree View]**.

1. 次のいずれかの操作を行います。

   1. （1 つの製品グループノードの設定を編集するには）製品グループ名の上にカーソルを置いたまま、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL + Edit Node]**.

   1. （1 つ以上の広告グループの設定を編集するには）次の操作を行います。

      1. 各ノードの横にあるチェックボックスを選択します。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集します。 [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md) または [[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md).

   複数のノードの場合、変更は選択したすべてのノードに適用されます。 の [!UICONTROL Bid] フィールドに、既存の値を指定した値に変更するか、指定した割合または金額で金額を上限に従って増減するかを選択できます。 の [!UICONTROL Tracking Template] フィールドの先頭には、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、指定したプレフィックスを各値の先頭に追加したり、各値の末尾にサフィックスを追加したりできます。

1. （オプション）「 **[!UICONTROL Additional Details]** 必要に応じて、プロジェクト名と説明を入力します。

1. クリック **[!UICONTROL Post]**.

## 製品グループノードの削除

他の製品グループが同じレベルに存在する場合は、「他のすべて」グループを除き、広告グループのショッピング広告に含まれる商品を決定するために使用する製品グループを削除できます。 製品グループを削除すると、すべての子製品グループが削除されます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. （オプション）リストをフィルタリングして、特定の製品グループを含めます。

1. 次のいずれかの操作を行います。

   * 1 つの製品グループを削除するには、 **[!UICONTROL Status]** 列と選択 **[!UICONTROL Delete]**.

   * 1 つ以上の製品グループを削除するには、以下の手順を実行します。

      1. 削除する各製品グループの横にあるチェックボックスをオンにします。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. ツールバーで、 ![詳細](/help/search-social-commerce/assets/more.png "詳細") を選択し、 **[!UICONTROL Delete]**.

      1. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [買い物製品グループについて](product-group-about.md)
>* [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)

