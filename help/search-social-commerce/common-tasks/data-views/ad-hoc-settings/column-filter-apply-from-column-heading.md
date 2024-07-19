---
title: 列見出しメニューからのデータフィルターの適用
description: 列見出しメニューのからページデータをフィルタリングする方法を説明します。
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# 列見出しメニューからのデータフィルターの適用

1 つの列に必要な数だけフィルターを適用できます。 すべてのフィルターは、AND 演算子を使用して結合されます。 使用可能なすべての指標を使用して一度に複数のフィルターを追加するには、「[ ツールバーからのデータフィルターの適用 ](column-filter-apply-from-toolbar.md) を参照してください。

1. 列見出しの右側にある ![ 下向き矢印 ](/help/search-social-commerce/assets/arrow-down-dropdown.png " 下向き矢印 ") をクリックし、[**[!UICONTROL Add Filter]**] をクリックします。

1. 列のフィルターを定義：

   * （入力フィールドを含まないフィルター）含める各値の横にあるチェックボックスをオンにして、「![ フィルターを更新 ](/help/search-social-commerce/assets/select.png " フィルターを更新 ")」をクリックします。

   * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力して、![ フィルターを更新 ](/help/search-social-commerce/assets/select.png " フィルターを更新 ") をクリックします。

     例えば、「[!UICONTROL Clicks]」列を選択して、100 回を超えるクリックがある行のみを返す場合は、「*[!UICONTROL greater than]*」を選択し、入力フィールドに「`100`」と入力します。データ型に応じて、使用可能な演算子には *[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]* または *[!UICONTROL no date]が含まれます。*

     >[!NOTE]
     >
     >* テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルタリングした場合、結果には「Consumer Loans」と「loan applications」が含まれます。
     >* 単純な数値フィルター（[!UICONTROL Impressions] \> 100 など）は、1 列につき 1 つだけ適用できます。
