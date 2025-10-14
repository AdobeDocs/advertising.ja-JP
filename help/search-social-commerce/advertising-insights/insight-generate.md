---
title: ' [!DNL Advertising Insight] を生成'
description: ' [!DNL Advertising Insight] の作成方法を説明します。'
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# [!DNL Advertising Insight] の生成

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Insights & Reports]/[!UICONTROL Advertising Insights]** をクリックします。

2. 生成するinsightをクリックします。

3. 次のようにinsightを指定します。

   1. （一部のレポート。オプション）insightの日付範囲を指定します。

   2. （ほとんどのインサイト）分析するポートフォリオを選択します。

      一般に、アクティブなキャンペーンを含んだ最適化されたアクティブなポートフォリオをすべて使用できます。 一部のインサイトでは、ポートフォリオリストをフィルタリングして、**[!UICONTROL Only Optimized Portfolios]** を含めることができます。

      インサイトの [!UICONTROL Day of Week] 合は、十分な支出があり、過去 2 日間にターゲットに費やしたポートフォリオのみを使用できます。

   3. （[!UICONTROL Event Path Beta] insightのみ）次の手順を実行します。

      1. **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* （[!UICONTROL Channel Assist Report] または [!UICONTROL Campaign Assist Report] をアップロードし、ユーザーイベントを分析のために個別のグループに分類する場合）または *[!UICONTROL Analyze classified events]* （イベントグループをアップロードし、insightの生成に使用する場合）。

      1. 「**[!UICONTROL Select]**」をクリックして XLSX および ZIP （圧縮 XLSX）形式のファイルを探し、「**[!UICONTROL Upload]**」をクリックします。

   4. （[!UICONTROL Google Account Audit] insightのみ）次の手順を実行します。

      1. **[!UICONTROL Advertiser Name]** と **[!UICONTROL Account Name]** を入力します。

      1. **[!UICONTROL Account Currency]**、**[!UICONTROL File Format Region]** （*[!UICONTROL United States]* または *[!UICONTROL United Kingdom]*）および **[!UICONTROL Output Language]** （*[!UICONTROL English (USA)]*、*[!UICONTROL French]* または *[!UICONTROL German]*）を選択します。

      1. 「**[!UICONTROL Select]**」をクリックして、[!DNL Google Ads] web ユーザーインターフェイスからアカウントにダウンロードされたキャンペーン、キーワード、変更履歴レポートと、[!DNL Google Ads Editor] アプリケーションからアカウントにダウンロードされたバルクシートファイルを探します。 次に、「**[!UICONTROL Upload]**」をクリックします。

         すべてのファイルは、CSV、TSV、TXT、または ZIP （圧縮された CSV、TSV、TXT）形式である必要があります。

   5. （insight[!UICONTROL Location Target Performance] み。オプション）概要としてではなく毎日データを集計するには、*[!UICONTROL Daily]* の **[!UICONTROL Time Aggregation]** を選択します。

   6. （[!UICONTROL Normalized Sim (Combined)] insightのみ）次の手順を実行します。

      1. **[!UICONTROL Step]** フィールドで、insightに含める目標支出レベルまたはステップの数を指定します。 値は 3 ～ 100 の範囲で指定します。

      1. 「**[!UICONTROL Type]**」フィールドで、シミュレーションのタイプを選択します。

         * *[!UICONTROL Optimized Multi-portfolio]*：同じ目的と通貨を持つ複数のポートフォリオをまたいで 1 つのシミュレーションを生成します。

         * *[!UICONTROL Individual Normalized]*：選択したポートフォリオごとに個別のシミュレーションを生成します。 ポートフォリオには、異なる目的と通貨が含まれる場合があります。

   7. （insight[!UICONTROL Portfolio Launch] み。オプション）ローンチ日を将来の日付に設定するには、「**[!UICONTROL Optional Date]**」フィールドに日付を入力します。

   8. （[!UICONTROL Quality Score] insightのみ）該当する広告ネットワークを選択します。

   9. （insight[!UICONTROL Query Cross Matching] み） **[!UICONTROL Google Accounts]** メニューで、アカウントを選択します。

4. 「**[!UICONTROL Generate Insight]**」をクリックします。

   [!UICONTROL Advertising Insights] で設定した [&#x200B; 通知設定 &#x200B;](/help/search-social-commerce/notifications/notification-edit.md) に基づいて、ジョブが完了するか失敗すると、通知が届きます。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Advertising Insights]](insight-about.md) について
>* [&#x200B; アセットの表示または保存  [!DNL Advertising Insight]](insight-view-save.md)
>* [&#x200B; を削除  [!DNL Advertising Insight]](insight-delete.md)
