---
title: '[!UICONTROL Label Classification Report]'
description: '[!UICONTROL Label Classification Report]について説明します。'
exl-id: 847fa384-b9c6-446f-9ebf-da7679ed35ae
feature: Search Reports, Search Basic Reports
TQID: https://experienceleague.adobe.com/75t5C8Cz-EE5vsPYYXHWHSE-6ZDhwSQaEgtAdirYHQU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# [!UICONTROL Label Classification Report]

[!UICONTROL Label Classification Report]には、広告ネットワーク、アカウント、キャンペーン、または広告グループをまたいで集計された、キーワードレベルまたは広告レベルのラベル分類によるコスト、クリック、および（オプションで）コンバージョンデータが含まれます。 デフォルトでは、データには、指定された日付範囲の時間単位ごとにインプレッションを受け取ったキーワード、広告、プレースメントに対する該当するキーワードレベルのラベル分類ごとに1行が含まれます。 行は、最初に時間単位の開始日、次にラベル分類、次にラベル値で昇順になります。

過去36か月間のデータを表示できます。

>[!NOTE]
>
>* 広告レベルのラベル分類によるレポートは、[!DNL Microsoft Advertising]件の動的検索広告（DSA）キャンペーンでは使用できません。
>* 同じエンティティに複数のラベル分類が適用される場合があるため、各指標の合計がエンティティの実際の合計よりも高くなる場合があります。 例えば、「スエードシューズ」というキーワードに「スエード」と「フットウェア」という2つのラベル値があり、キーワードが100 クリックを受け取ったとします。 クリック数の列には、それぞれのラベル値に対して「100」が表示されるので、両方の行の合計は「200」になります。
>* エンティティの分類と子ラベルの値をラベル付けするために行った変更は、約1時間で表示されます。

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
>* [基本レポートまたは詳細レポートを生成](basic-advanced-report-generate.md)
>* [基本および詳細レポート設定](basic-advanced-report-settings.md)
