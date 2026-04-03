---
title: 列フィルターの編集
description: 列フィルターの編集方法を説明します。
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
TQID: https://experienceleague.adobe.com/BeMoK7e--CoIqQDg364E9nnb28nGDYwP6YaKu3swzHY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 586
ht-degree: 0%

---

# 列フィルターの編集

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

## （新しいUI）管理ビューでのフィルターセットの編集

1. ツールバーで、![&#x200B; フィルター](/help/search-social-commerce/assets/filter-new.png " フィルター")をクリックします。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、**[!UICONTROL ADD FILTER]**&#x200B;をクリックし、次の操作を行います。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]**&#x200B;入力フィールドに検索文字列を入力します。

      1. 列メニューから列名を選択します。

      1. 列にフィルターを定義します。

         * （入力フィールドのないフィルター） 2番目のメニューの横にある![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")をクリックし、含める各値の横にあるチェックボックスを選択します。

         * （入力フィールドを含むフィルター） 2番目のメニューから演算子を選択し、該当する値を入力します。

           例えば、「[!UICONTROL Clicks]」列を選択し、クリック数が100を超える行のみを返す場合は、「*[!UICONTROL greater than]*」を選択して入力フィールドに「`100`」と入力します。

           データ型に応じて、使用可能な演算子には&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*、または&#x200B;*[!UICONTROL no date]が含まれる場合があります。*

           **注意：** テキスト値では、大文字と小文字は区別されません。 例えば、名前に「ローン」が付いたキャンペーンでフィルタリングした場合、結果には「消費者ローン」と「ローン申請」が含まれます。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更します。

   * 既存のフィルターを削除するには、フィルター定義の横にある&#x200B;**[!UICONTROL -]**&#x200B;をクリックします。

## （従来のUI）キャンペーン管理ビューでのフィルターセットの編集

1. ツールバーの「![&#x200B; フィルター](/help/search-social-commerce/assets/filter.png " フィルター")」をクリックします。

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、![&#x200B; フィルターを追加](/help/search-social-commerce/assets/add.png " フィルターを追加") **[!UICONTROL ADD FILTER]**&#x200B;をクリックし、次の操作を行います。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]**&#x200B;入力フィールドに検索文字列を入力します。

      1. 列メニューから列名を選択します。

      1. 列にフィルターを定義します。

         * （入力フィールドのないフィルター） 2番目のメニューの横にある![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")をクリックし、含める各値の横にあるチェックボックスを選択します。

         * （入力フィールドを含むフィルター） 2番目のメニューから演算子を選択し、該当する値を入力します。

           例えば、「[!UICONTROL Clicks]」列を選択し、クリック数が100を超える行のみを返す場合は、「*[!UICONTROL greater than]*」を選択して入力フィールドに「`100`」と入力します。

           データ型に応じて、使用可能な演算子には&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*&#x200B;または&#x200B;*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*、または&#x200B;*[!UICONTROL no date]が含まれます。*

           **注意：** テキスト値では、大文字と小文字は区別されません。 例えば、名前に「ローン」が付いたキャンペーンを検索すると、「消費者ローン」と「ローン申し込み」が結果として表示されます。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更します。

   * 既存のフィルターを削除するには、フィルター定義の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

1. （[!UICONTROL Keywords] ビューのみ。オプション）設定を「[!UICONTROL Include rows with no performance data]」に選択または選択解除します。

   >[!WARNING]
   >
   >このオプションを選択すると、ページの読み込み時間が長くなります。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。

## 管理ビューでの1つのフィルターの編集

1. データテーブルの上で、フィルター定義をクリックします。

1. 列のフィルターを再定義します。

   * （入力フィールドのないフィルター） 2番目のメニューの横にある![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")をクリックし、含める各値の横にあるチェックボックスを選択します。

   * （入力フィールドを含むフィルター） 2番目のメニューから演算子を選択し、該当する値を入力します。

     例えば、「[!UICONTROL Clicks]」列を選択し、クリック数が100を超える行のみを返す場合は、「*[!UICONTROL greater than]*」を選択して入力フィールドに「`100`」と入力します。

     データ型に応じて、使用可能な演算子には、*[!UICONTROL greater than]*、*より小さい*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*含まない*、または&#x200B;*から始まる*&#x200B;が含まれる場合があります。

     **注意：** テキスト値では、大文字と小文字は区別されません。 例えば、名前に「ローン」が付いたキャンペーンを検索すると、「消費者ローン」と「ローン申し込み」が結果として表示されます。

>[!MORELIKETHIS]
>
>* [列見出しメニューからデータフィルターを適用](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [&#x200B; ツールバーからデータフィルターを適用](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [列フィルターを削除] （/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
