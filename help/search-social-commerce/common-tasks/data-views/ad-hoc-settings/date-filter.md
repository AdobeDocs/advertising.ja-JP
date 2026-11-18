---
title: 日付範囲でデータをフィルタリング
description: グローバル日付範囲フィルターの使用方法を説明します。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 968023d95217d4d17b1441ae717f3e472b31f7c4
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%
---
# 日付範囲でデータをフィルタリング

日付範囲フィルターを使用して、パフォーマンスデータを表示する期間を指定します。 日付比較をサポートするビューでは、2つの期間のパフォーマンスを比較することもできます。

## （新しいUI）日付範囲の変更 {#date-filter-new-ui}

1. ページヘッダーで、カレンダーアイコンが表示されている日付範囲コントロールをクリックします。

1. 日付範囲を指定します。

   * プリセット範囲を使用するには、最初のカレンダーの上にあるメニュー（**[!UICONTROL Yesterday]**&#x200B;や&#x200B;**[!UICONTROL Last 7 Days]**&#x200B;など）からオプションを選択します。

   * カスタム範囲を使用するには、**[!UICONTROL Custom Date Range]**&#x200B;を選択し、カレンダーの開始日と終了日を選択します。 カレンダーの矢印を使用して、月を移動します。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。

## （新しいUI） 2つの期間のデータを比較する {#compare-periods-new-ui}

日付比較のみをサポートする&#x200B;*ビュー*

1. ページヘッダーで、カレンダーアイコンが表示されている日付範囲コントロールをクリックします。

1. **[!UICONTROL Compare Periods]**&#x200B;を有効にします。

   2つのカレンダーパネルが並べて表示されます。 最初のピリオドには青緑色のマーカーがあり、比較ピリオドには紫色のマーカーがあります。

1. 最初のパネルで、日付範囲を指定します。

   * プリセット範囲を使用するには、最初のカレンダーの上にあるメニュー（**[!UICONTROL Yesterday]**&#x200B;や&#x200B;**[!UICONTROL Last 7 Days]**&#x200B;など）からオプションを選択します。

   * カスタム範囲を使用するには、**[!UICONTROL Custom Date Range]**&#x200B;を選択し、カレンダーの開始日と終了日を選択します。 カレンダーの矢印を使用して、月を移動します。

1. 2番目のパネルで、比較プリセットを選択するか、カレンダーの開始日をクリックします。

   比較期間は、最初の期間と同じ日数です。 両方のカレンダーの上にある完全な日付範囲を確認します。

1. **[!UICONTROL Comparison Format]**&#x200B;から、違いを表示する方法を選択します。

   * **[!UICONTROL As percentage]:**&#x200B;違いをパーセンテージで表示します。

   * **[!UICONTROL As variance]:**&#x200B;差を数値として表示します。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。

   日付範囲コントロールには、期間ラベルとカラーマーカーを含む完全な日付範囲の両方が表示されます。 各比較指標は、2つのピリオド列と&#x200B;**[!UICONTROL Change]**&#x200B;列にグループ化されます。 比較できないフィールドは、単一の列のままです。 列見出しの期間マーカーは、対応する日付範囲を識別します。

期間の比較を停止するには、日付範囲コントロールを開き、**[!UICONTROL Compare Periods]**&#x200B;をオフにして、**[!UICONTROL Apply]**&#x200B;をクリックします。 比較をオフにすると、比較データに基づいてフィルターがクリアされます。

### 列メニューから比較形式を変更する

1. 日付比較を有効にした状態で、**[!UICONTROL Change]**&#x200B;列の列見出しメニューを開くか、同等の指標のピリオド列を開きます。

1. **[!UICONTROL As percentage]**&#x200B;または&#x200B;**[!UICONTROL As variance]**&#x200B;を選択してください。

   選択は、選択した列だけでなく、データテーブル内のすべての比較指標に適用されます。 日付範囲コントロールは選択範囲と同期され、保存された日付範囲を含むビューを含め、現在の広告主に適用されるページ間で形式が共有されます。

   データテーブルが正常に更新された後、確認メッセージが表示されます。 選択した形式でデータテーブルを更新できない場合は、代わりにエラーメッセージが表示されます。形式をもう一度選択してみてください。

並べ替えとフィルタリングのオプションは、サポートされている列メニューでも引き続き使用できます。

## （従来のUI）日付範囲の設定

特定の日付範囲を保存したデフォルトビューとカスタムビューを除き、すべての広告主に対して、ほとんどのデータビューに同じグローバル日付範囲フィルターが適用されます。 キャンペーン管理ビューのシステムのデフォルトの日付範囲は「昨日」です。

日付範囲の設定はブラウザー固有のCookieに保存されるので、フィルターを変更するかCookieを削除するまで、同じブラウザーアプリケーションを使用してログインするたびに、日付範囲フィルターの変更がすべての広告主に使用されます。 使用するブラウザーアプリケーションごとに、日付範囲フィルター設定が異なるCookieに保存されます。

デフォルトのビューまたはカスタムビューに特定の日付範囲を保存すると、使用しているブラウザーアプリケーションに関係なく、ビューを適用するたびに、その範囲が適用されます。

>[!NOTE]
>
>* 過去13か月間のデータを表示できますが、既存のカスタムビューには、過去180日間までのデータのみを含めることができます。
>* 以前のデータを表示するには、[[!UICONTROL Reports] ビュー](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)に移動し、基本レポートを実行します。
>* [ デフォルトビューまたはカスタムビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)の日付範囲を保存することもできます。

## （従来のUI）キャンペーンビューでのグローバル日付フィルターの変更

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
