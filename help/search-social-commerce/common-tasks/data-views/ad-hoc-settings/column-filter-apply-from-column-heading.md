---
title: 列見出しメニューからのデータフィルターの適用
description: 列見出しメニューからページデータをフィルタリングする方法を説明します。
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
TQID: https://experienceleague.adobe.com/8HhbDC38BA48vw3c8fqCEaCKNUWs3q2HwCEiDfieWUM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 221
ht-degree: 0%

---

# 列見出しメニューからのデータフィルターの適用

<!-- The same in new UI and legacy CM views -->

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

1つの列に対して1つずつ、必要な数のフィルターを適用できます。<!-- True only for entity names, I think: All filters are joined using the AND operator. -->使用可能なすべての指標を使用して一度に複数のフィルターを追加するには、「[&#x200B; ツールバーからデータフィルターを適用](column-filter-apply-from-toolbar.md)」を参照してください。

1. 列見出しの右側で、![下向き矢印](/help/search-social-commerce/assets/arrow-down-dropdown.png "下向き矢印")をクリックし、**[!UICONTROL Add Filter]**&#x200B;をクリックします。

1. 列にフィルターを定義します。

   * （入力フィールドのないフィルター）含める各値の横にあるチェックボックスを選択し、![&#x200B; フィルターを更新](/help/search-social-commerce/assets/select.png "追加")をクリックします。

   * （入力フィールドを含むフィルター） 2番目のメニューから演算子を選択し、該当する値を入力して、![&#x200B; フィルターを更新](/help/search-social-commerce/assets/select.png "追加")をクリックします。

     例えば、「[!UICONTROL Clicks]」列を選択し、100 クリックを超える行のみを返す場合は、「*[!UICONTROL greater than]*」を選択して入力フィールドに「`100`」と入力します。データタイプによっては、使用可能な演算子に&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;が含まれる場合があります。*[!UICONTROL no date]*

     >[!NOTE]
     >
     >* テキスト値では大文字と小文字は区別されません。 例えば、名前に「ローン」が付いたキャンペーンでフィルタリングすると、「消費者ローン」と「ローン申請」が結果に含まれます。
     >* 1つの列に適用できる単純な数値フィルター（[!UICONTROL Impressions] \> 100など）は1つだけです。

>[!MORELIKETHIS]
>
>* [&#x200B; ツールバーからデータフィルターを適用](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [列フィルターの編集](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [列フィルターを削除] （/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
