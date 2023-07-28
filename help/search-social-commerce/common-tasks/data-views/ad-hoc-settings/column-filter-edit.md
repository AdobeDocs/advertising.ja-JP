---
title: 列フィルターを編集
description: 列フィルターの編集方法を説明します。
exl-id: 6e42e006-089b-44b9-b9b1-66835b680413
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 列フィルターを編集

## フィルターセットの編集

1. クリック ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター") 」と入力します。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、 ![フィルターを追加](/help/search-social-commerce/assets/add.png "フィルターを追加") **[!UICONTROL ADD FILTER]** をクリックし、次の操作を実行します。

      1. （オプション）列名をテキスト文字列でフィルターするには、 **[!UICONTROL ADD FILTER]** 入力フィールド。

      1. 列メニューから列名を選択します。

      1. 列でフィルターを定義します。

         * （入力フィールドを含まないフィルター）クリック ![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印") 2 番目のメニューの横にある、含める各値の横のチェックボックスをオンにし、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

         * （入力フィールドを含むフィルター）2 番目のメニューから演算子を選択し、適切な値を入力して、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

           例えば、[!UICONTROL Clicks]」列をクリックし、100 回を超えるクリック数の行のみを返したい場合は、 *[!UICONTROL greater than]*」と入力し、 `100` を入力フィールドに入力します。

           データタイプに応じて、使用可能な演算子は次のとおりです。 *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*&#x200B;または *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*&#x200B;または *[!UICONTROL no date].*

           **注意：** テキスト値では大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンを検索した場合、結果には「Consumer Loans」と「loan applications」が含まれます。

   * 既存のフィルタを編集するには、フィルタをクリックし、フィルタ定義を変更して、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

   * 既存のフィルターを削除するには、 **[!UICONTROL X]** フィルター定義の横に表示されます。

1. ([!UICONTROL Keywords] 表示のみ（オプション）設定を「[!UICONTROL Include rows with no performance data].&quot;

   >[!WARNING]
   >
   >このオプションを選択すると、ページの読み込み時間が長くなります。

1. クリック **[!UICONTROL Apply]**.

## 単一のフィルターの編集

1. （必要に応じて）データテーブルの上にあるフィルターセットで、 ![その他](/help/search-social-commerce/assets/more-filters.png "その他") をクリックして、フィルタセットを展開します。

1. データテーブルの上で、フィルタ定義をクリックします。

1. 適用するフィルターを編集します。

   1. （オプション）列メニューから列名を編集します。

   1. （オプション）列でフィルターを再定義します。

      * （入力フィールドを含まないフィルター）クリック ![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印") 2 番目のメニューの横にある、含める各値の横のチェックボックスをオンにし、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

      * （入力フィールドを含むフィルター）2 番目のメニューから演算子を選択し、適切な値を入力して、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

        例えば、[!UICONTROL Clicks]」列をクリックし、100 回を超えるクリック数の行のみを返したい場合は、 *[!UICONTROL greater than]*」と入力し、 `100` 入力フィールド内

        データタイプに応じて、使用可能な演算子は次のとおりです。 *[!UICONTROL greater than]*, *より小さい*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *次を含まない*&#x200B;または *次で始まる。*

        **注意：** テキスト値では大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンを検索した場合、結果には「Consumer Loans」と「loan applications」が含まれます。
