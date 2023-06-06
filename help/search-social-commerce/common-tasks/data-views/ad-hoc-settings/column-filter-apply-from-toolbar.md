---
title: ツールバーからのデータフィルターの適用
description: ツールバーからページデータをフィルタリングする方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# ツールバーからのデータフィルターの適用

フィルターは、ビューに適用する数だけ適用できます。 すべてのフィルターは、AND 演算子を使用して結合されます。

1. ツールバーで、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター").

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、 ![フィルターを追加](/help/search-social-commerce/assets/add.png "フィルターを追加") **[!UICONTROL ADD FILTER]**&#x200B;をクリックし、次の操作を実行します。

      1. （オプション）列名をテキスト文字列でフィルターするには、 **[!UICONTROL ADD FILTER]** 入力フィールド。

      1. 列メニューから列名を選択します。

      1. 列でフィルターを定義します。

         * （入力フィールドを含まないフィルター）クリック ![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印") 2 番目のメニューの横にあるをクリックし、含める各値の横にあるチェックボックスをオンにします。

         * （入力フィールドを含むフィルター）2 番目のメニューから演算子を選択し、適切な値を入力します。

            例えば、[!UICONTROL Clicks]」列をクリックし、100 回を超えるクリック数の行のみを返す場合は、 *[!UICONTROL greater than]*」と入力し、 `100` を入力フィールドに入力します。

            データタイプに応じて、使用可能な演算子は次のとおりです。 *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*&#x200B;または *[!UICONTROL no date].*

            **注意：** テキスト値では大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルターする場合、結果には「Consumer Loans」と「loan applications」が含まれます。

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements]、および [!UICONTROL Auto Targets] 表示のみ（オプション）設定を「[!UICONTROL Include rows with performance data only].&quot;

            **警告：** このオプションの選択を解除し、パフォーマンスデータを持たない多数のエンティティがビューに含まれている場合、データの表示に時間がかかります。
   * 既存のフィルタを編集するには、フィルタをクリックし、フィルタ定義を変更して、 ![フィルターを更新](/help/search-social-commerce/assets/select.png "フィルターを更新").

   * 既存のフィルターを削除するには、 **[!UICONTROL X]** をクリックします。


1. クリック **[!UICONTROL Apply]**.
