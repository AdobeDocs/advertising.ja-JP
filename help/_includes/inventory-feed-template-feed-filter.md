---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# テキストとテンプレート – フィードフィルター

**\[ フィード フィルタ\]:** フィード ファイルのどの行を伝達するか：

* *[!UICONTROL Propagate all rows found in feed:]* （デフォルト）すべての行のデータを伝播します。

* *[!UICONTROL Propagate rows that meet certain conditions:]* 指定した条件を最大 10 個満たす行のデータのみを伝播します。 適用するフィルターを指定：

   1. すべてのフィルターに使用するブール演算（**[!UICONTROL AND]** または **[!UICONTROL OR]**）を選択します。

   1. 最初のメニューから列名を選択し、2 番目のメニューから演算子を選択して、該当する値を入力するか、入力フィールドを空白のままにして、条件のない行のデータを伝播します。

  列リストには、フィードで使用可能なすべての列が含まれます。

  使用可能な演算子には、*[!UICONTROL contains]*、*[!UICONTROL does not contain]*、*[!UICONTROL =]*、*[!UICONTROL <>]* （等しくない）、*[!UICONTROL in]*、*[!UICONTROL not in]*、*[!UICONTROL less than]* および *[!UICONTROL greater than]* があります。 演算子「[!UICONTROL in]」を選択すると、値のコンマ区切りリストを入力できます。レコードが指定されたいずれかの値に一致する場合、それらの行にデータが伝播されます。 その他のすべての演算子には、値を 1 つだけ入力します。 値では大文字と小文字が区別されません。

  例えば、「product_type」列を選択し、「shoes」を含む製品名の行のみを返したい場合は、「**[!UICONTROL contains]**」を選択して、入力フィールドに `shoes` を入力します。

   1. （最大 9 つの追加フィルターを適用する場合）追加のフィルターごとに「**[!UICONTROL Add Condition]**」をクリックし、手順 2 に従って追加のフィルターを指定します。
