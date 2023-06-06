---
title: 列見出しメニューからのデータフィルターの適用
description: 列見出しメニューからページデータをフィルタリングする方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 列見出しメニューからのデータフィルターの適用

1 つの列に対して、必要な数のフィルターを 1 つずつ適用できます。 すべてのフィルターは、AND 演算子を使用して結合されます。 利用可能なすべての指標を使用して一度に複数のフィルターを追加するには、[ツールバーからのデータフィルターの適用](column-filter-apply-from-toolbar.md).&quot;

1. 列見出しの右側で、 ![下向き矢印](/help/search-social-commerce/assets/arrow-down-dropdown.png "下向き矢印")をクリックし、 **[!UICONTROL Add Filter]**.

1. 列でフィルターを定義します。

   * （入力フィールドを含まないフィルター）含める各値の横にあるチェックボックスをオンにし、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

   * （入力フィールドを含むフィルター）2 番目のメニューから演算子を選択し、適切な値を入力して、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

      例えば、[!UICONTROL Clicks]」列をクリックし、100 回を超えるクリック数の行のみを返す場合は、 *[!UICONTROL greater than]*」と入力し、 `100` 入力フィールド：データタイプに応じて、使用可能な演算子には次のものが含まれます。 *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*&#x200B;または *[!UICONTROL no date].*

      >[!NOTE]
      >
      >* テキスト値では大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルターする場合、結果には「Consumer Loans」と「loan applications」が含まれます。
      >* 適用できる単純な数値フィルターは 1 つだけです ( 例： [!UICONTROL Impressions] \> 100) を返します。

