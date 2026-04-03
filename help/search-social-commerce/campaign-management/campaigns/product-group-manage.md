---
title: ショッピング商品グループの管理
description: ショッピング施策でショッピング商品グループを作成および管理する方法について説明します。
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/x-B0Ybah1ySNsyIKQz9iY2IT8fhvSawTx-mRDB0da6k
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 720
ht-degree: 0%

---

# ショッピング商品グループの管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising]個のショッピング キャンペーンのみ*

製品グループを作成および編集し、製品グループとその子製品グループを[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] ビューで削除できます。

## 「[!UICONTROL All Products]」製品グループの作成

特定の属性を持つ製品グループを作成する前に、まず「[!UICONTROL All Products]」という名前の包括的な製品グループを作成する必要があります。 各広告グループには、「[!UICONTROL All Products]」グループを1つだけ設定できます。

>[!TIP]
>
>多くのアカウントコンポーネントを一度に作成するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)または[[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)を指定します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## 既存の製品グループに子製品グループノードを作成する

広告グループのオールインクルーシブ「[!UICONTROL All Products]」グループを少なくとも作成したら、入札に含める製品のサブセットまたは入札から除外する製品の子製品グループノードを作成できます。各レベルで同じ属性をターゲットとする製品グループを1つ以上作成できます（例：[!UICONTROL Brand]=1つの製品グループに対してAcme、同じレベルで別の製品グループに対して[!UICONTROL Brand]=AcmePlus。 「[!UICONTROL All Products]」を含めずに、最大7 レベルの子製品グループノードを作成できます。

>[!NOTE]
>
>「[!UICONTROL Everything Else]」製品グループの子製品グループを作成することはできません。

>[!TIP]
>
>多くのアカウントコンポーネントを一度に作成するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]**&#x200B;をクリックします。

1. （オプション）製品グループとその子製品グループノードをツリービューで表示するには、製品グループ名にカーソルを合わせ、![&#x200B; メニューアイコン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ")をクリックし、**[!UICONTROL Tree View]**&#x200B;を選択します。

1. 製品グループ名の上にカーソルを置き、![矢印ドロップダウンメニュー](/help/search-social-commerce/assets/arrow-dropdown-menu.png "矢印ドロップダウンメニュー")をクリックし、**[!UICONTROL + Add Node]**&#x200B;を選択します。

1. 製品ディメンションと属性を含め、[[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)または[[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)を指定します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## 製品グループノード設定の編集

広告グループに含まれるユニット製品グループノード（子製品グループノードのない製品グループ）の入札および追跡テンプレートを編集できます。 除外単位製品グループ、または子の製品グループノードを持つ製品グループである含まれるサブディビジョン ノードまたは除外されたサブディビジョン ノードの情報を編集することはできません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]**&#x200B;をクリックします。

1. （オプション）製品グループとその子製品グループノードをツリービューで表示するには、製品グループ名にカーソルを合わせ、![&#x200B; メニューアイコン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ")をクリックし、**[!UICONTROL Tree View]**&#x200B;を選択します。

1. 次のいずれかの操作を行います。

   1. （単一の製品グループノードの設定を編集するには）製品グループ名にカーソルを合わせ、![&#x200B; メニューアイコン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ")をクリックし、**[!UICONTROL + Edit Node]**&#x200B;を選択します。

   1. （1つ以上の広告グループの設定を編集するには）次の操作を行います。

      1. 各ノードの横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)または[[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)を編集します。

   複数のノードの場合、変更は選択したすべてのノードに適用されます。 [!UICONTROL Bid] フィールドには、既存の値を指定した値に変更するか、指定した割合または金額で金額を増減するか、制限を設けるかを選択できます。 [!UICONTROL Tracking Template] フィールドでは、既存の値を指定された値に変更したり、既存の文字列を指定された文字列に置き換えたり、指定されたプレフィックスを各値の先頭に追加したり、サフィックスを各値の末尾に追加したりできます。

1. （オプション）「**[!UICONTROL Additional Details]**」をクリックし、必要に応じてプロジェクト名と説明を入力します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## 製品グループノードの削除

他の商品グループが同じレベルに存在する場合は、「その他すべて」グループを除いて、あらゆる商品グループを削除できます。このグループは、マーチャント センターのアカウントのどの商品が広告グループのショッピング広告に含まれているかを判断するために使用されます。 製品グループを削除すると、すべての子製品グループが削除されます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Product Groups]**&#x200B;をクリックします。

1. （オプション）リストをフィルタリングして、特定の製品グループを含めます。

1. 次のいずれかの操作を行います。

   * 1つの製品グループを削除するには、**[!UICONTROL Status]**&#x200B;列をクリックし、**[!UICONTROL Delete]**&#x200B;を選択します。

   * 1つ以上の製品グループを削除するには、次の操作を行います。

      1. 削除する各製品グループの横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. ツールバーで、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Delete]**&#x200B;を選択します。

      1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; ショッピング商品グループについて](product-group-about.md)
>* [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)
