---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# テキスト広告テンプレート — フィードフィルター

**\[ フィードフィルター\]:** フィードファイルのどの行を反映するか：

* *[!UICONTROL Propagate all rows found in feed:]* （デフォルト）すべての行のデータを伝播します。

* *[!UICONTROL Propagate rows that meet certain conditions:]* 10 個までの指定した条件を満たす行のみにデータを伝播する場合。 適用するフィルターを指定します。

   1. すべてのフィルターに使用するブール演算を選択します。  **[!UICONTROL AND]** または **[!UICONTROL OR]**.

   1. 最初のメニューから列名を選択し、2 番目のメニューから演算子を選択して、適切な値を入力するか、入力フィールドを空白のままにして、条件を指定せずに行のデータを反映します。

   列リストには、使用可能なすべての列がフィードに含まれます。

   使用可能な演算子は次のとおりです。 *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* （と等しくない） *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]*、および *[!UICONTROL greater than]*. 演算子「[!UICONTROL in]」と入力すると、値のコンマ区切りリストを入力できます。レコードが指定された値のいずれかと一致する場合、それらの行のデータが伝播されます。 その他の演算子の場合は、値を 1 つだけ入力します。 値では大文字と小文字が区別されません。

   例えば、「product_type」列を選択し、「shoes」を含む製品名の行のみを返す場合は、「**[!UICONTROL contains]**」と入力し、 `shoes` を入力フィールドに入力します。

   1. （最大 9 つのフィルターを追加する場合）追加したフィルターごとに、 **[!UICONTROL Add Condition]**&#x200B;をクリックし、手順 2 に従って追加のフィルターを指定します。
