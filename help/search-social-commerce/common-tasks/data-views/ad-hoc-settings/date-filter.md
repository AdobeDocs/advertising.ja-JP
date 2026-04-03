---
title: 日付範囲でデータをフィルタリング
description: グローバル日付範囲フィルターの使用方法を説明します。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 398
ht-degree: 0%

---

# 日付範囲でデータをフィルタリング

<!-- The same in new UI and legacy CM views -->

特定の日付範囲を保存したデフォルトビューとカスタムビューを除き、すべての広告主に対して、ほとんどのデータビューに同じグローバル日付範囲フィルターが適用されます。 キャンペーン管理ビューのシステムのデフォルトの日付範囲は「昨日」です。

日付範囲の設定はブラウザー固有のCookieに保存されるので、フィルターを変更するかCookieを削除するまで、同じブラウザーアプリケーションを使用してログインするたびに、日付範囲フィルターの変更がすべての広告主に使用されます。 使用するブラウザーアプリケーションごとに、日付範囲フィルター設定が異なるCookieに保存されます。

デフォルトのビューまたはカスタムビューに特定の日付範囲を保存すると、使用しているブラウザーアプリケーションに関係なく、ビューを適用するたびに、その範囲が適用されます。

>[!NOTE]
>
>* 過去13か月間のデータを表示できますが、既存のカスタムビューには、過去180日間までのデータのみを含めることができます。
>* 以前のデータを表示するには、[[!UICONTROL Reports] ビュー](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)に移動し、基本レポートを実行します。
>* [ デフォルトビューまたはカスタムビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)の日付範囲を保存することもできます。

## キャンペーンビューでのグローバル日付フィルターの変更

1. 検索/ キャンペーン / キャンペーンの任意のデータテーブルの上で、現在の日付範囲をクリックします。

1. **[!UICONTROL Date Range]** フィールドで、範囲を指定します。

   * プリセット範囲の場合：*[!UICONTROL Today]*&#x200B;から&#x200B;*[!UICONTROL Last 180 Days]*&#x200B;までの一般的な時間増分のリストから選択します。 デフォルトは&#x200B;*[!UICONTROL Yesterday]*&#x200B;です。

   * 特定の範囲の場合：**[!UICONTROL Custom Date Range]**&#x200B;を選択し、開始日と終了日を指定します。

     MM/DD/YYYYまたはMM-DD-YYYY形式で日付を入力するか、各フィールドの横にある![ カレンダーアイコン ](/help/search-social-commerce/assets/calendar.png " カレンダーアイコン ")をクリックしてカレンダーを開き、日付を選択します。

1. （オプション）指定した日付範囲のデータと2番目の日付範囲のデータを比較します。

   1. **[!UICONTROL Comparison]** スライダーを「オン」位置に移動します。

      このオプションを選択すると、通常のデータ列ごとに2つの追加の列が追加されます。 例えば、「[!UICONTROL Impressions]」の列を1つだけ含める代わりに、「[!UICONTROL Impressions R1]」、「[!UICONTROL Impressions R2]」、「[!UICONTROL Impressions Diff]」の列がテーブルに含まれます。  データを書き出す場合、同じ列が「[!UICONTROL Impressions Range 1]」、「[!UICONTROL Impressions Range 2]」、「[!UICONTROL Impressions Difference]」とスペルで表示されます。

   1. 2番目の日付範囲を指定します。

   1. 「\[_データフィールド_\]差異」列で、選択した2つの日付範囲のデータの違いを表現する方法を選択します。

      * *[!UICONTROL Variance]* （既定値）：差分を数値として表示します。

      * *[!UICONTROL % Change]:*&#x200B;違いをパーセンテージで表示します。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。
