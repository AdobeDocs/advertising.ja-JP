---
title: ショッピング商品グループの管理
description: ショッピングキャンペーンでショッピング製品グループを作成および管理する方法を説明します。
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# ショッピング商品グループの管理

*[!DNL Google Ads]および [!DNL Microsoft Advertising] のショッピングキャンペーンのみ*

[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]/[!UICONTROL Product Groups] 表示で、製品グループを作成および編集したり、製品グループとその子製品グループを削除したりできます。

## 「[!UICONTROL All Products]」製品グループの作成

特定の属性を持つ製品グループを作成する前に、まず「[!UICONTROL All Products]」と呼ばれる包括的な製品グループを作成する必要があります。 各広告グループには、「[!UICONTROL All Products]」グループを 1 つだけ含めることができます。

>[!TIP]
>
>一度に多くのアカウントコンポーネントを作成するには、[campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、「**[!UICONTROL Continue]**」をクリックします。

1. [[!DNL Google Ads]  製品グループ設定 ](product-group-settings-google.md) または [[!DNL Microsoft Advertising]  製品グループ設定 ](product-group-settings-microsoft.md) を指定します。

1. 「**[!UICONTROL Post]**」をクリックします。

## 既存の製品グループ内に子製品グループノードを作成

広告グループに対して包括的な「[!UICONTROL All Products]」グループを少なくとも 1 つ作成したら、1 つ以上の製品グループが各レベルで同じ属性をターゲットにします（例えば、ある製品グループの [!UICONTROL Brand]=Acme と、同じレベルの別の製品の [!UICONTROL Brand]=AcmePlus など）。これにより、入札に含めたり、入札から除外したりする製品のサブセットの子製品グループノードを作成できます。 「[!UICONTROL All Products]」を含まない子製品グループノードを最大 7 レベル作成できます。

>[!NOTE]
>
>「[!UICONTROL Everything Else]」製品グループ用に子製品グループを作成することはできません。

>[!TIP]
>
>一度に多くのアカウントコンポーネントを作成するには、[campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]** をクリックします。

1. （オプション）ツリー表示で製品グループとその子製品グループのノードを表示するには、製品グループ名の上にカーソルを置き、![ メニューアイコン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ") をクリックしてから「**[!UICONTROL Tree View]**」を選択します。

1. 製品グループ名の上にカーソルを置き、![ 矢印のドロップダウン メニュー ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " 矢印のドロップダウン メニュー ") をクリックし、[**[!UICONTROL + Add Node]**] を選択します。

1. 製品分析コードや属性を含む [[!DNL Google Ads]  製品グループ設定 ](product-group-settings-google.md) または [[!DNL Microsoft Advertising]  製品グループ設定 ](product-group-settings-microsoft.md) を指定します。

1. 「**[!UICONTROL Post]**」をクリックします。

## 製品グループノード設定の編集

広告グループに含まれる単位製品グループノード（子製品グループノードを持たない製品グループ）の入札およびトラッキングテンプレートを編集できます。 除外された単位製品グループ、または含まれているか除外されているサブ分割ノード（子製品グループ ノードを持つ製品グループ）に関する情報は編集できません。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]** をクリックします。

1. （オプション）ツリー表示で製品グループとその子製品グループのノードを表示するには、製品グループ名の上にカーソルを置き、![ メニューアイコン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ") をクリックしてから「**[!UICONTROL Tree View]**」を選択します。

1. 次のいずれかの操作をおこないます。

   1. （単一の製品グループノードの設定を編集する場合）製品グループ名の上にカーソルを置き、![ メニューアイコン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ") をクリックして、**[!UICONTROL + Edit Node]** を選択します。

   1. （1 つ以上の広告グループの設定を編集するには）次の手順を実行します。

      1. 各ノードの横にあるチェックボックスを選択します。

         複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. データ テーブルの上にあるツールバーで、[![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

1. [[!DNL Google Ads]  製品グループ設定 ](product-group-settings-google.md) または [[!DNL Microsoft Advertising]  製品グループ設定 ](product-group-settings-microsoft.md) を編集します。

   複数のノードの場合、変更は選択したすべてのノードに適用されます。 [!UICONTROL Bid] フィールドには、既存の値を指定の値に変更するオプションと、制限を指定して、指定の割合または金額で金額を増減するオプションがあります。 [!UICONTROL Tracking Template] フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。

1. （任意）「**[!UICONTROL Additional Details]**」をクリックし、オプションでプロジェクト名と説明を入力します。

1. 「**[!UICONTROL Post]**」をクリックします。

## 製品グループノードの削除

同じレベルに他の商品グループが存在する場合は、「その他すべて」グループを除いて、任意の商品グループを削除できます。このグループは、広告グループのショッピング広告に含まれるマーチャントセンターアカウントの商品を決定するために使用されます。 製品グループを削除すると、すべての子製品グループが削除されます。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]** をクリックします。

1. （任意）特定の製品グループを含めるようにリストをフィルタリングします。

1. 次のいずれかの操作をおこないます。

   * 製品グループを 1 つ削除するには、**[!UICONTROL Status]** 列をクリックして **[!UICONTROL Delete]** を選択します。

   * 1 つ以上の製品グループを削除するには、次の手順を実行します。

      1. 削除する各製品グループの横にあるチェックボックスをオンにします。

         複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. ツールバーの ![ その他 ") をクリックし ](/help/search-social-commerce/assets/more.png " 選択 **[!UICONTROL Delete]** ます。

      1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ ショッピング商品グループについて ](product-group-about.md)
>* [[!DNL Google Ads]  製品グループ設定 ](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising]  製品グループ設定 ](product-group-settings-microsoft.md)
