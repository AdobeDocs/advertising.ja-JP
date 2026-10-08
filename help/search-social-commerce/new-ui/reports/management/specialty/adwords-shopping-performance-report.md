---
title: '[!UICONTROL AdWords Shopping Performance Report]'
description: '[!UICONTROL AdWords Shopping Performance Report]について説明します。'
feature: Search Reports, Search Specialty Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
  - id: 7de556b7-2c2a-599d-853b-8c282aafa6e3
    internal-label: Search Specialty Reports
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# [!UICONTROL AdWords Shopping Performance Report]

*[!DNL Google Ads]アカウントのみ*

[!UICONTROL AdWords Shopping Performance Report]には、コスト、クリック、インプレッションデータ、[!DNL Google Ads Conversion Optimizer]によって追跡されたコンバージョン済みのクリックとコンバージョンのデータ、[!DNL Adobe]によって追跡された（オプション）コンバージョンのデータ、およびショッピングキャンペーンの1つ以上の広告グループの製品ID レベルで集計された派生指標のデータが含まれます。 デフォルトでは、データには、指定された日付範囲の時間単位ごとに、広告グループごとに製品IDと製品カテゴリごとに1行が含まれます。 行は、アカウント名、キャンペーン名、広告グループ名の順に昇順で表示されます。

過去2か月間のデータを表示できます。 2018年9月21日以前のデータは、2行に表示されます。1行はコストとクリックのデータ、1行はAdobeで追跡されたコンバージョンデータです。 後続のデータは1行に表示されます。

>[!NOTE]
>
>* 製品に[!UICONTROL Product Category]列が含まれ、製品が複数のカテゴリに表示される場合、製品は複数の行に表示され、コンバージョン数は該当する各行に複製されます。 コンバージョンデータの合計は正確ではないため、コンバージョンのトレンドをカテゴリー別に把握するために、データをカテゴリー別に分類する必要があります。
>* 報告書用のデータは、前日の午後23時（11時）に取り込まれます。 得ることができます。 例えば、6月18日の23:00に、6月17日のデータを取得します。 6月19日の09:00 （6月18日のデータが取り込まれる前）にレポートを実行すると、レポートには6月17日の23:00までのデータが含まれます。

## デフォルトの列

すべてのデフォルト列とカスタム列について詳しくは、「[特殊レポートのレポート列](specialty-report-columns.md)」を参照してください。

* [!UICONTROL Account Name]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Product ID]
* [!UICONTROL Category (1st level - 5th level)]
* [!UICONTROL Product Type (1st level - 5th level)]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Google Converted Clicks]
* [!UICONTROL Google Conversions]
* [!UICONTROL CTR]
* [!UICONTROL CPC]

>[!MORELIKETHIS]
>
>* [専門性レポートについて](specialty-report-about.md)
>* [ スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [特殊レポート設定](specialty-report-settings.md)
