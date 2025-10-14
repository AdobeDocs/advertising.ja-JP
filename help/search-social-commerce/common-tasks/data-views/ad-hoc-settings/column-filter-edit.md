---
title: 列フィルターを編集
description: 列フィルターの編集方法を説明します。
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# 列フィルターを編集

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

## （新しい UI）管理ビューでフィルターセットを編集する

1. ツールバーで、「![&#x200B; フィルター &#x200B;](/help/search-social-commerce/assets/filter-new.png " フィルター ")」をクリックします。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、[**[!UICONTROL ADD FILTER]**] をクリックし、次の操作を行います。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]** 入力フィールドに検索文字列を入力します。

      1. 列メニューから列名を選択します。

      1. 列のフィルターを定義：

         * （入力フィールドのないフィルタ） 2 番目のメニューの横にある ![&#x200B; 下矢印 &#x200B;](/help/search-social-commerce/assets/arrow-down-expand.png " 下矢印 ") をクリックし、含める値の横のチェック ボックスをオンにします。

         * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。

           例えば、「[!UICONTROL Clicks]」列を選択し、100 クリックを超える行のみを返したい場合は、「*[!UICONTROL greater than]*」を選択して、入力フィールドに「`100`」と入力します。

           データ型に応じて、使用可能な演算子には、*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]* または *[!UICONTROL no date]が含まれます。*

           **メモ：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルタリングした場合、結果には「Consumer Loans」と「loan applications」が含まれます。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更します。

   * 既存のフィルターを削除するには、フィルター定義の横にある「**[!UICONTROL -]**」をクリックします。

## （従来の UI）キャンペーン管理ビューでフィルターセットを編集する

1. ツールバーの ![&#x200B; フィルター &#x200B;](/help/search-social-commerce/assets/filter.png " フィルター ") をクリックします。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、「![&#x200B; フィルターを追加 &#x200B;](/help/search-social-commerce/assets/add.png " フィルターを追加 ")」をクリック **[!UICONTROL ADD FILTER]**、次の手順を実行します。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]** 入力フィールドに検索文字列を入力します。

      1. 列メニューから列名を選択します。

      1. 列のフィルターを定義：

         * （入力フィールドのないフィルタ） 2 番目のメニューの横にある ![&#x200B; 下矢印 &#x200B;](/help/search-social-commerce/assets/arrow-down-expand.png " 下矢印 ") をクリックし、含める値の横のチェック ボックスをオンにします。

         * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。

           例えば、「[!UICONTROL Clicks]」列を選択し、100 クリックを超える行のみを返したい場合は、「*[!UICONTROL greater than]*」を選択して、入力フィールドに「`100`」と入力します。

           データ型に応じて、使用可能な演算子には、*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*、*[!UICONTROL no date]などがあります。*

           **メモ：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンを検索すると、結果には「Consumer Loans」と「loan applications」が含まれます。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更します。

   * 既存のフィルターを削除するには、フィルター定義の横にある ![&#x200B; 削除 &#x200B;](/help/search-social-commerce/assets/delete.png " 削除 ") をクリックします。

1. （[!UICONTROL Keywords] 表示のみ。オプション）「[!UICONTROL Include rows with no performance data]」に設定を選択または選択解除します。

   >[!WARNING]
   >
   >このオプションを選択すると、ページの読み込み時間が長くなります。

1. 「**[!UICONTROL Apply]**」をクリックします。

## 管理ビューで 1 つのフィルターを編集する

1. データテーブルの上で、フィルター定義をクリックします。

1. 列のフィルターを再定義：

   * （入力フィールドのないフィルター） 2 番目のメニューの横にある ![&#x200B; 下矢印 &#x200B;](/help/search-social-commerce/assets/arrow-down-expand.png " 下矢印 ") をクリックし、含める各値の横にあるチェックボックスを選択します。

   * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。

     例えば、「[!UICONTROL Clicks]」列を選択し、100 クリックを超える行のみを返したい場合は、「*[!UICONTROL greater than]*」を選択して、入力フィールドに「`100`」と入力します。

     データ型に応じて、使用可能な演算子には、*[!UICONTROL greater than]*、*より小さい*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*含まない* または *次で始まる* が含まれます。

     **メモ：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンを検索すると、結果には「Consumer Loans」と「loan applications」が含まれます。

>[!MORELIKETHIS]
>
>* [&#x200B; 列見出しメニューからのデータフィルターの適用 &#x200B;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [&#x200B; ツールバーからのデータフィルターの適用 &#x200B;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [ 列フィルターの削除 ] （/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
