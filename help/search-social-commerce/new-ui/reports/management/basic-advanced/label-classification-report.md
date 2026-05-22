---
title: '[!UICONTROL Label Classification Report]'
description: '[!UICONTROL Label Classification Report]について説明します。'
feature: Search Reports, Search Basic Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# [!UICONTROL Label Classification Report]

[!UICONTROL Label Classification Report]には、広告ネットワーク、アカウント、キャンペーン、または広告グループをまたいで集計された、キーワードレベルまたは広告レベルのラベル分類によるコスト、クリック、および（オプションで）コンバージョンデータが含まれます。 デフォルトでは、データには、指定された日付範囲の時間単位ごとにインプレッションを受け取ったキーワード、広告、プレースメントに対する該当するキーワードレベルのラベル分類ごとに1行が含まれます。 行は、最初に時間単位の開始日、次にラベル分類、次にラベル値で昇順になります。

過去36か月間のデータを表示できます。

>[!NOTE]
>
>* 広告レベルのラベル分類によるレポートは、[!DNL Microsoft Advertising]件の動的検索広告（DSA）キャンペーンでは使用できません。
>* 同じエンティティに複数のラベル分類が適用される場合があるため、各指標の合計がエンティティの実際の合計よりも高くなる場合があります。 例えば、「スエードシューズ」というキーワードに「スエード」と「フットウェア」という2つのラベル値があり、キーワードが100 クリックを受け取ったとします。 クリック数の列には、それぞれのラベル値に対して「100」が表示されるので、両方の行の合計は「200」になります。
* エンティティの分類と子ラベルの値をラベル付けするために行った変更は、約1時間で表示されます。

## デフォルトの列

すべてのデフォルト列とカスタム列について詳しくは、「[基本レポートと詳細レポートのレポート列](basic-advanced-report-columns.md)」を参照してください。

* [!UICONTROL Label Classification]
* [!UICONTROL Label Value]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Cost]
* [!UICONTROL Clicks]
* [!UICONTROL CPC]
* [!UICONTROL Avg Position]
* [!UICONTROL Impr. (Abs. Top) %]
* [!UICONTROL Impr. (Top) %]

>[!MORELIKETHIS]
>
>* [基本レポートと詳細レポートについて](basic-advanced-report-about.md)
>* [ スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [基本および詳細レポート設定](basic-advanced-report-settings.md)
