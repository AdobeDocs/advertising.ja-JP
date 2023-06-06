---
title: 分類値をキャンペーン管理ビューからアカウントコンポーネントに割り当てる
description: アカウントコンポーネントに分類値を割り当てる方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# 分類値をキャンペーン管理ビューからアカウントコンポーネントに割り当てる

キャンペーン管理ビューでは、以下の検索エンティティの分類値を割り当てたり、削除したりできます。キャンペーン、広告グループ、キーワード、広告、プレースメント、ユニットレベルの製品グループ、動的検索ターゲット。 必要に応じて、割り当てプロセス中に分類および分類値を作成できます。 各ラベル分類には、最大 2,000 個の値を含めることができます。

各エンティティは、分類ごとに 1 つのラベル値を持つことができます。 例えば、Shoes_Campaign のカラー値は「red」、地域値は「Los Angeles」にできますが、カラーまたは地域に複数の値を含めることはできません。

ラベル値は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードおよび広告コピーは、次のとおりです [不変](/help/search-social-commerce/campaign-management/faqs-campaigns.md)を編集すると、既存のエンティティが削除され、新しいエンティティが作成されます。 この方法で既存のエンティティを削除した場合、ラベルの分類は新しいエンティティに割り当てられません。

1. クリック **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックし、アカウントコンポーネントビューを選択します。

1. 次のいずれかの操作を行います。

   * （単一のエンティティに値を割り当てる場合）エンティティ名の上にカーソルを置いたまま、 ![メニューボタン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューボタン")を選択し、 **[!UICONTROL Classification]**.

   * （1 つ以上のエンティティに値を割り当てるには）次の手順を実行します。

      * 各関連行の横にあるチェックボックスをオンにします。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * データテーブルの上にあるツールバーで、 ![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、 **[!UICONTROL Classification]**.

1. 内 [!UICONTROL Assignment Details]、次のいずれかの操作を行います。

   * 既存の分類値を新しい値に変更するには、 **[!UICONTROL Set To]**.

      各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

   * 既存の値を削除せずに、指定した分類値を割り当てるには、「 **[!UICONTROL Assign]**.

   * 現在割り当てられている特定の分類値を削除するには、「 」を選択します。 **[!UICONTROL Remove]**.

      分類値を削除すると、その値のレポートデータは、指定したアカウントコンポーネントでは使用できなくなります。

   * 指定した分類値を削除するには、 **[!UICONTROL Delete]**.

      分類値を削除すると、今後使用できなくなり、その値でレポートデータを使用できなくなります。 値と特定のアカウントコンポーネント間の割り当てはすべて削除されますが、アカウントコンポーネントは削除されません。

1. 該当する分類値ごとに、次の操作を行います。

   1. 内 **[!UICONTROL Classification]** 列に、分類名を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、 [!UICONTROL +]. 入力フィールドに分類名を入力し、「 ![保存](/help/search-social-commerce/assets/select.png "保存") をクリックして、分類を直ちに保存します。

         名前は次の要素で構成する必要があります： [ASCII 文字 32～126](https://www.asciitable.com/)の最大長は 27 文字です。
   1. 内 **[!UICONTROL Value Name]** 列に、値の名前を指定します。

      * 既存の値を使用するには、値名をクリックして選択します。

      * 値を作成するには、 [!UICONTROL +]. 入力フィールドに値を入力し、「 ![保存](/help/search-social-commerce/assets/select.png "保存") をクリックして、値を直ちに保存します。

         最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。


1. （オプション）追加の詳細を入力します。

   1. 次の隣 **[!UICONTROL Additional Details]**&#x200B;をクリックし、 ![開く](/help/search-social-commerce/assets/chevron-up.png "開く") をクリックして詳細を展開します。

   1. オプションを入力 **[!UICONTROL Project Name]** および/またはオプション **[!UICONTROL Description]**.

1. クリック **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [ラベルの分類について](classification-about.md)
>* [ラベルの分類の作成](classification-create.md)
>* [一括送信シートを使用して、勘定科目コンポーネントに分類値を割り当てます。](classification-values-assign-bulksheets.md)
>* [顧客コンポーネントからラベル分類値を削除](classification-values-remove.md)
>* [ラベル分類値の削除](classification-values-delete.md)
>* [ラベルの分類を削除](classification-delete.md)

