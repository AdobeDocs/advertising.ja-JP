---
title: ツールバーからのデータフィルターの適用
description: ツールバーからページデータをフィルタリングする方法を説明します。
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# ツールバーからのデータフィルターの適用

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

ビューには、必要な数だけフィルターを適用できます。<!-- True only for entity names, I think: All filters are joined using the AND operator. -->

## （新しい UI）管理表示のツールバーからのデータフィルターの適用

1. ツールバーで、「![ フィルター ](/help/search-social-commerce/assets/filter-new.png " フィルター ")」をクリックします。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、[**[!UICONTROL ADD FILTER]**] をクリックし、次の操作を行います。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]** 入力フィールドに検索文字列を入力します。

      1. 列メニューから列名を選択します。

      1. 列のフィルターを定義：

         * （入力フィールドのないフィルタ） 2 番目のメニューの横にある ![ 下矢印 ](/help/search-social-commerce/assets/arrow-down-expand.png " 下矢印 ") をクリックし、含める値の横のチェック ボックスをオンにします。

         * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。

           例えば、「[!UICONTROL Clicks]」列を選択し、100 クリックを超える行のみを返したい場合は、「*[!UICONTROL greater than]*」を選択して、入力フィールドに「`100`」と入力します。

           データ型に応じて、使用可能な演算子には、*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]* または *[!UICONTROL no date]が含まれます。*

           **メモ：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルタリングした場合、結果には「Consumer Loans」と「loan applications」が含まれます。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更します。

   * 既存のフィルターを削除するには、フィルター定義の横にある「**[!UICONTROL -]**」をクリックします。

## （従来の UI） Campaign 管理ビューのツールバーからのデータフィルターの適用

1. ツールバーで、「![ フィルター ](/help/search-social-commerce/assets/filter.png " フィルター ")」をクリックします。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、「![ フィルターの追加 ](/help/search-social-commerce/assets/add.png " フィルターの追加 ")」をクリック **[!UICONTROL ADD FILTER]**、次の手順を実行します。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]** 入力フィールドに検索文字列を入力します。

      1. 列メニューから列名を選択します。

      1. 列のフィルターを定義：

         * （入力フィールドのないフィルタ） 2 番目のメニューの横にある ![ 下矢印 ](/help/search-social-commerce/assets/arrow-down-expand.png " 下矢印 ") をクリックし、含める値の横のチェック ボックスをオンにします。

         * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。

           例えば、「[!UICONTROL Clicks]」列を選択し、100 クリックを超える行のみを返したい場合は、「*[!UICONTROL greater than]*」を選択して、入力フィールドに「`100`」と入力します。

           データ型に応じて、使用可能な演算子には、*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]* または *[!UICONTROL no date]が含まれます。*

           **メモ：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルタリングした場合、結果には「Consumer Loans」と「loan applications」が含まれます。

         * （[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Product Groups]、[!UICONTROL Placements] および [!UICONTROL Auto Targets] ビューのみ。オプション）設定を「[!UICONTROL Include rows with performance data only]」に変更します。

           **警告：** このオプションの選択を解除した場合、パフォーマンスデータのない多数のエンティティがビューに含まれると、データの表示に時間がかかります。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更します。

   * 既存のフィルターを削除するには、フィルター定義の横にある ![ 削除 ](/help/search-social-commerce/assets/delete.png " 削除 ") をクリックします。

1. 「**[!UICONTROL Apply]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 列見出しメニューからのデータフィルターの適用 ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [ 列フィルターを編集 ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [ 列フィルターの削除 ] （/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
