---
title: ' [!DNL Advertising Insight] を生成'
description: ' [!DNL Advertising Insight] の作成方法を説明します。'
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# [!DNL Advertising Insight] の生成

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Insights & Reports]/[!UICONTROL Advertising Insights]** をクリックします。

2. 生成するインサイトをクリックします。

3. インサイト設定を指定します。

   1. （一部のレポート。オプション）インサイトの日付範囲を指定します。

   2. （ほとんどのインサイト）分析するポートフォリオを選択します。

      一般に、アクティブなキャンペーンを含んだ最適化されたアクティブなポートフォリオをすべて使用できます。 一部のインサイトでは、ポートフォリオリストをフィルタリングして、**[!UICONTROL Only Optimized Portfolios]** を含めることができます。

      インサイトの [!UICONTROL Day of Week] 合は、十分な支出があり、過去 2 日間にターゲットに費やしたポートフォリオのみを使用できます。

   3. （[!UICONTROL Event Path Beta] insight のみ）次の手順を実行します。

      1. **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* （[!UICONTROL Channel Assist Report] または [!UICONTROL Campaign Assist Report] をアップロードし、ユーザーイベントを分析のために個別のグループに分類する場合）または *[!UICONTROL Analyze classified events]* （イベントグループをアップロードし、インサイトを生成するために使用する場合）を選択します。

      1. 「**[!UICONTROL Select]**」をクリックして XLSX および ZIP （圧縮 XLSX）形式のファイルを探し、「**[!UICONTROL Upload]**」をクリックします。

   4. （[!UICONTROL Google Account Audit] insight のみ）次の手順を実行します。

      1. **[!UICONTROL Advertiser Name]** と **[!UICONTROL Account Name]** を入力します。

      1. **[!UICONTROL Account Currency]**、**[!UICONTROL File Format Region]** （*[!UICONTROL United States]* または *[!UICONTROL United Kingdom]*）および **[!UICONTROL Output Language]** （*[!UICONTROL English (USA)]*、*[!UICONTROL French]* または *[!UICONTROL German]*）を選択します。

      1. 「**[!UICONTROL Select]**」をクリックして、[!DNL Google Ads] web ユーザーインターフェイスからアカウントにダウンロードされたキャンペーン、キーワード、変更履歴レポートと、[!DNL Google Ads Editor] アプリケーションからアカウントにダウンロードされたバルクシートファイルを探します。 次に、「**[!UICONTROL Upload]**」をクリックします。

         すべてのファイルは、CSV、TSV、TXT、または ZIP （圧縮された CSV、TSV、TXT）形式である必要があります。

   5. （[!UICONTROL Location Target Performance] insight のみ。オプション）概要としてではなく毎日データを集計するには、*[!UICONTROL Daily]* の **[!UICONTROL Time Aggregation]** を選択します。

   6. （[!UICONTROL Normalized Sim (Combined)] insight のみ）次の手順を実行します。

      1. 「**[!UICONTROL Step]**」フィールドで、インサイトに含めるターゲット支出レベルまたはステップの数を指定します。 値は 3 ～ 100 の範囲で指定します。

      1. 「**[!UICONTROL Type]**」フィールドで、シミュレーションのタイプを選択します。

         * *[!UICONTROL Optimized Multi-portfolio]*：同じ目的と通貨を持つ複数のポートフォリオをまたいで 1 つのシミュレーションを生成します。

         * *[!UICONTROL Individual Normalized]*：選択したポートフォリオごとに個別のシミュレーションを生成します。 ポートフォリオには、異なる目的と通貨が含まれる場合があります。

   7. （インサイトのみ [!UICONTROL Portfolio Launch]、オプション）今後のローンチ日を指定するには、「**[!UICONTROL Optional Date]**」フィールドで日付を指定します。

   8. （[!UICONTROL Quality Score] insight のみ）該当する広告ネットワークを選択します。

   9. （[!UICONTROL Query Cross Matching] insight のみ） **[!UICONTROL Google Accounts]** メニューで、アカウントを選択します。

4. 「**[!UICONTROL Generate Insight]**」をクリックします。

   [!UICONTROL Advertising Insights] で設定した [ 通知設定 ](/help/search-social-commerce/notifications/notification-edit.md) に基づいて、ジョブが完了するか失敗すると、通知が届きます。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Advertising Insights]](insight-about.md) について
>* [ アセットの表示または保存  [!DNL Advertising Insight]](insight-view-save.md)
>* [ を削除  [!DNL Advertising Insight]](insight-delete.md)
