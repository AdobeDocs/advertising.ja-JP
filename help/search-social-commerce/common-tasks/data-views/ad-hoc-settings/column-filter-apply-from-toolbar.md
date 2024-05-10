---
title: ツールバーからのデータフィルターの適用
description: ツールバーからページデータをフィルタリングする方法を説明します。
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# ツールバーからのデータフィルターの適用

ビューには、必要な数だけフィルターを適用できます。 すべてのフィルターは、AND 演算子を使用して結合されます。

1. ツールバーで、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター").

1. フィルター設定で、次のいずれかの操作を行います。

   * フィルターを追加するには、をクリックします ![フィルターを追加](/help/search-social-commerce/assets/add.png "フィルターを追加") **[!UICONTROL ADD FILTER]**&#x200B;次に、以下を実行します。

      1. （オプション）列名をテキスト文字列でフィルタリングするには、検索文字列を **[!UICONTROL ADD FILTER]** 入力フィールド。

      1. 列メニューから列名を選択します。

      1. 列のフィルターを定義：

         * （入力フィールドのないフィルター）をクリック ![下矢印キー](/help/search-social-commerce/assets/arrow-down-expand.png "下矢印キー") 2 番目のメニューの横で、含める各値の横にあるチェックボックスをオンにします。

         * （入力フィールド付きのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。

           例えば、「[!UICONTROL Clicks]「列」を選択し、100 クリックを超える行のみを返す場合は、 *[!UICONTROL greater than]*」と入力して、 `100` 入力フィールドに移動します。

           データタイプに応じて、使用可能な演算子は次のとおりです *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*、または *[!UICONTROL no date].*

           **注意：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルタリングした場合、結果には「Consumer Loans」と「loan applications」が含まれます。

         * （[!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements]、および [!UICONTROL Auto Targets] 表示のみ（オプション）。設定を「」に変更します。[!UICONTROL Include rows with performance data only].」と入力します。

           **警告：** このオプションの選択を解除した場合、ビューにパフォーマンス データのない多数のエンティティが含まれると、データの表示に時間がかかります。

   * 既存のフィルターを編集するには、フィルターをクリックし、フィルター定義を変更して、 ![フィルターの更新](/help/search-social-commerce/assets/select.png "フィルターの更新").

   * 既存のフィルターを削除するには、をクリックします **[!UICONTROL X]** フィルター定義の横。

1. クリック **[!UICONTROL Apply]**.
