---
title: 日付範囲でのデータのフィルタリング
description: グローバル日付範囲フィルターの使用方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 日付範囲でのデータのフィルタリング

特定の日付範囲を保存したデフォルトビューとカスタムビューを除く、ほとんどのキャンペーンデータビューに同じグローバル日付範囲フィルターが適用されます。 キャンペーン管理表示のシステムのデフォルトの日付範囲は、「昨日」です。

日付範囲の設定はブラウザー固有の Cookie に保存されるので、フィルターを変更または削除するまで、同じブラウザーアプリケーションを使用してログインするたびに、日付範囲フィルターに対する変更がすべての広告主で使用されます。 使用するブラウザーアプリケーションごとに、異なる cookie に日付範囲フィルター設定が保存されます。

デフォルトビューまたはカスタムビューの特定の日付範囲を保存すると、使用しているブラウザーアプリケーションに関係なく、ビューを適用するたびにその範囲が適用されます。

>[!NOTE]
>
>* 過去 13 ヶ月間のデータを表示できますが、既存のカスタムビューには過去 180 日間のデータのみを含めることができます。
>* 以前のデータを表示するには、 [[!UICONTROL Reports] 表示](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) 基本レポートを実行します。
>* また、 [デフォルトビューまたはカスタムビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).


## キャンペーン表示でのグローバル日付フィルタの変更

1. 検索/キャンペーン/キャンペーンのデータテーブルの上にある現在の日付範囲をクリックします。

1. 内 **[!UICONTROL Date Range]** フィールドで、範囲を指定します。

   * プリセット範囲の場合：共通の時間増分のリストから選択し、 *[!UICONTROL Today]* から *[!UICONTROL Last 180 Days]*. デフォルトはです。 *[!UICONTROL Yesterday]*.

   * 特定の範囲の場合：選択 **[!UICONTROL Custom Date Range]** をクリックし、開始日と終了日を指定します。

      MM/DD/YYYY または MM-DD-YYYY の形式で日付を入力するか、 ![カレンダーアイコン](/help/search-social-commerce/assets/calendar.png "カレンダーアイコン") 各フィールドの横にあるカレンダーを開き、日付を選択します。

1. （オプション）指定した日付範囲のデータを 2 番目の日付範囲のデータと比較します。

   1. を **[!UICONTROL Comparison]** スライダーで *[!UICONTROL On]*.

      このオプションを選択すると、通常のデータ列ごとに 2 つの列が追加されます。 例えば、「[!UICONTROL Impressions]」の場合、「[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2],&quot;および&quot;[!UICONTROL Impressions Diff].&quot;  データを書き出す場合、同じ列は「[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot;および&quot;[!UICONTROL Impressions Difference].&quot;

   1. 2 番目の日付範囲を指定します。

   1. 「\[」で選択した 2 つの日付範囲のデータ間の違いを表す方法を選択します&#x200B;_データフィールド_「\] 差異」列：

      * *[!UICONTROL Variance]* （デフォルト）:差異を数値として表示します。

      * *[!UICONTROL % Change]:*  差異をパーセンテージで表示します。

1. クリック **[!UICONTROL Apply]**.
