---
title: 日付範囲でデータをフィルター
description: グローバル日付範囲フィルターの使用方法を説明します。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 日付範囲でデータをフィルター

同じグローバル日付範囲フィルターが、すべての広告主にわたるほとんどのキャンペーンデータビューに適用されます。ただし、特定の日付範囲を保存したデフォルトおよびカスタムビューは除きます。 キャンペーン管理ビューのシステムのデフォルトの日付範囲は「昨日」です。

日付範囲設定はブラウザー固有の cookie に保存されるので、日付範囲フィルターに対する変更は、フィルターを変更するか、cookie を削除するまで、同じブラウザーアプリケーションを使用してログインするたびに、すべての広告主に対して使用されます。 使用するブラウザーアプリケーションごとに、日付範囲フィルター設定が異なる cookie に保存されます。

既定のビューまたはカスタム ビューに対して特定の日付範囲を保存すると、その日付範囲は、使用しているブラウザ アプリケーションに関係なく、ビューを適用するたびに適用されます。

>[!NOTE]
>
>* 過去 13 か月のデータを表示できますが、既存のカスタムビューには、過去 180 日間のデータのみを含めることができます。
>* 以前のデータを表示するには、 [[!UICONTROL Reports] 表示](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) 基本レポートを実行します。
>* の日付範囲を保存することもできます。 [デフォルトビューまたはカスタムビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## キャンペーンビューでのグローバル日付フィルターの変更

1. 検索\> キャンペーン \> キャンペーンの任意のデータテーブルの上で、現在の日付範囲をクリックします。

1. が含まれる **[!UICONTROL Date Range]** フィールドで、範囲を指定します。

   * プリセット範囲の場合：次の範囲の、一般的な時間増分のリストから選択します *[!UICONTROL Today]* 対象： *[!UICONTROL Last 180 Days]*. デフォルトはです *[!UICONTROL Yesterday]*.

   * 特定の範囲の選択： **[!UICONTROL Custom Date Range]** を選択し、開始日と終了日を指定します。

     MM/DD/YYYY または MM-DD-YYYY の形式で日付を入力するか、 ![カレンダーアイコン](/help/search-social-commerce/assets/calendar.png "カレンダーアイコン") 各フィールドの横でカレンダーを開いて日付を選択します。

1. （任意）指定した日付範囲のデータと 2 つ目の日付範囲のデータを比較します。

   1. を移動 **[!UICONTROL Comparison]** スライダー先 *[!UICONTROL On]*.

      このオプションを選択すると、通常のデータ列ごとに 2 つの列が追加されます。 例えば、「」に列を 1 つだけ含めるのではなく、[!UICONTROL Impressions],&quot;テーブルには&quot;の列が含まれています[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2]、」および「[!UICONTROL Impressions Diff].」と入力します。  データを書き出す場合、同じ列には「[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2]、」および「[!UICONTROL Impressions Difference].」と入力します。

   1. 2 番目の日付範囲を指定します。

   1. 選択した 2 つの日付範囲のデータ間の差異を「\[_データフィールド_\] Difference&quot; カラム：

      * *[!UICONTROL Variance]* （デフォルト）：差異を数値で表示します。

      * *[!UICONTROL % Change]:*  差異をパーセンテージで表示します。

1. クリック **[!UICONTROL Apply]**.
