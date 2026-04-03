---
title: ' [!DNL Advertising Insight]を生成'
description: ' [!DNL Advertising Insight]の作成方法を説明します。'
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
TQID: https://experienceleague.adobe.com/meXmiqRiNyUxVnnMdl8S-GfHk0xWWu-62tU0W5Ogtd8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# [!DNL Advertising Insight]を生成

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**&#x200B;をクリックします。

2. 生成するinsightをクリックします。

3. Insightの設定を指定します。

   1. （一部のレポート。オプション）insightの日付範囲を指定します。

   2. （最も多くのインサイト）分析するポートフォリオを選択します。

      一般的に、アクティブなキャンペーンを含む、最適化されたアクティブなポートフォリオはすべて使用できます。 一部のインサイトでは、ポートフォリオリストをフィルタリングして&#x200B;**[!UICONTROL Only Optimized Portfolios]**&#x200B;を含めることができます。

      [!UICONTROL Day of Week]個のインサイトの場合、十分な支出があり、過去2日間のターゲティングにも費やしたポートフォリオのみが使用できます。

   3. （[!UICONTROL Event Path Beta] insightのみ）次の操作を行います。

      1. **[!UICONTROL Operation]**: *[!UICONTROL Extract events]*&#x200B;を選択します（[!UICONTROL Channel Assist Report]または[!UICONTROL Campaign Assist Report]をアップロードし、分析のためにユーザーイベントを個別のグループに分類します）。または&#x200B;*[!UICONTROL Analyze classified events]*&#x200B;を選択します（イベントグループをアップロードし、insightを生成するために使用します）。

      1. **[!UICONTROL Select]**&#x200B;をクリックしてXLSXおよびZIP （圧縮XLSX）形式のファイルを検索し、**[!UICONTROL Upload]**&#x200B;をクリックします。

   4. （[!UICONTROL Google Account Audit] insightのみ）次の操作を行います。

      1. **[!UICONTROL Advertiser Name]**&#x200B;と&#x200B;**[!UICONTROL Account Name]**&#x200B;を入力します。

      1. **[!UICONTROL Account Currency]**、**[!UICONTROL File Format Region]** （*[!UICONTROL United States]*&#x200B;または&#x200B;*[!UICONTROL United Kingdom]*）および&#x200B;**[!UICONTROL Output Language]** （*[!UICONTROL English (USA)]*、*[!UICONTROL French]*、または&#x200B;*[!UICONTROL German]*）を選択します。

      1. 「**[!UICONTROL Select]**」をクリックして、[!DNL Google Ads] web ユーザーインターフェイスからアカウント用にダウンロードされたキャンペーン、キーワード、変更履歴レポートと、[!DNL Google Ads Editor] アプリケーションからアカウント用にダウンロードされたバルクシート ファイルを探します。 次に、**[!UICONTROL Upload]**&#x200B;をクリックします。

         すべてのファイルは、CSV、TSV、TXT、またはZIP （圧縮CSV、TSV、またはTXT）形式である必要があります。

   5. （[!UICONTROL Location Target Performance] insightのみ。オプション）要約ではなく毎日データを集計するには、**[!UICONTROL Time Aggregation]**&#x200B;の&#x200B;*[!UICONTROL Daily]*&#x200B;を選択します。

   6. （[!UICONTROL Normalized Sim (Combined)] insightのみ）次の操作を行います。

      1. 「**[!UICONTROL Step]**」フィールドで、insightに含める目標支出レベルまたはステップの数を指定します。 値は、3 ～ 100の範囲で指定できます。

      1. **[!UICONTROL Type]** フィールドで、シミュレーションタイプを選択します。

         * *[!UICONTROL Optimized Multi-portfolio]*：目的と通貨が同じ複数のポートフォリオにまたがる単一のシミュレーションを生成します。

         * *[!UICONTROL Individual Normalized]*：選択した各ポートフォリオに対して個別のシミュレーションを生成します。 ポートフォリオには、目的や通貨が異なる場合があります。

   7. （[!UICONTROL Portfolio Launch] insightのみ。オプション）将来の起動日を指定するには、**[!UICONTROL Optional Date]** フィールドに日付を指定します。

   8. （[!UICONTROL Quality Score] insightのみ）該当する広告ネットワークを選択します。

   9. （[!UICONTROL Query Cross Matching] insightのみ） **[!UICONTROL Google Accounts]** メニューで、アカウントを選択します。

4. **[!UICONTROL Generate Insight]**&#x200B;をクリックします。

   ジョブが完了または失敗したときに、[の](/help/search-social-commerce/notifications/notification-edit.md)設定済みの通知設定[!UICONTROL Advertising Insights]に基づいて通知を受け取ります。

>[!MORELIKETHIS]
>
>* [約[!UICONTROL Advertising Insights]](insight-about.md)
>* [を表示または保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [を削除 [!DNL Advertising Insight]](insight-delete.md)
