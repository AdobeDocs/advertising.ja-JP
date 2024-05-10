---
title: 生成 [!DNL Advertising Insight]
description: を作成する方法を学ぶ [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 生成 [!DNL Advertising Insight]

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. 生成するインサイトをクリックします。

3. インサイト設定を指定します。

   1. （一部のレポート。オプション）インサイトの日付範囲を指定します。

   2. （ほとんどのインサイト）分析するポートフォリオを選択します。

      一般に、アクティブなキャンペーンを含んだ最適化されたアクティブなポートフォリオをすべて使用できます。 一部のインサイトでは、ポートフォリオリストをフィルタリングして、次の項目を含めることができます **[!UICONTROL Only Optimized Portfolios]**.

      の場合 [!UICONTROL Day of Week] インサイトは、十分な支出があり、過去 2 日間にターゲットに費やしたポートフォリオでのみ使用できます。

   3. （[!UICONTROL Event Path Beta] insight のみ）次の手順を実行します。

      1. 「」を選択します **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* （をアップロードする） [!UICONTROL Channel Assist Report] または [!UICONTROL Campaign Assist Report] さらに、ユーザーイベントを分析用に個別のグループに分類する）または *[!UICONTROL Analyze classified events]* （イベントグループをアップロードし、それらを使用してインサイトを生成する方法）。

      1. クリック **[!UICONTROL Select]** xlsx および ZIP （圧縮 XLSX）形式のファイルを見つけるには、をクリックします **[!UICONTROL Upload]**.

   4. （[!UICONTROL Google Account Audit] insight のみ）次の手順を実行します。

      1. を入力 **[!UICONTROL Advertiser Name]** および **[!UICONTROL Account Name]**.

      1. 「」を選択します **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** （*[!UICONTROL United States]* または *[!UICONTROL United Kingdom]*）、および **[!UICONTROL Output Language]** （*[!UICONTROL English (USA)]*, *[!UICONTROL French]*、または *[!UICONTROL German]*）に設定します。

      1. クリック **[!UICONTROL Select]** からアカウントにダウンロードされたキャンペーン、キーワードおよび変更履歴レポートを検索するには [!DNL Google Ads] からアカウント用にダウンロードされた web ユーザーインターフェイスとバルクシートファイル [!DNL Google Ads Editor] アプリケーション。 次に、 **[!UICONTROL Upload]**.

         すべてのファイルは、CSV、TSV、TXT、または ZIP （圧縮された CSV、TSV、TXT）形式である必要があります。

   5. （[!UICONTROL Location Target Performance] インサイトのみ（オプション） データを概要としてではなく毎日集計するには、 **[!UICONTROL Time Aggregation]** 件中 *[!UICONTROL Daily]*.

   6. （[!UICONTROL Normalized Sim (Combined)] insight のみ）次の手順を実行します。

      1. が含まれる **[!UICONTROL Step]** フィールドで、インサイトに含めるターゲット支出レベルまたはステップの数を指定します。 値は 3 ～ 100 の範囲で指定します。

      1. が含まれる **[!UICONTROL Type]** 「」フィールドで、シミュレーションのタイプを選択します。

         * *[!UICONTROL Optimized Multi-portfolio]*：同じ目的と通貨を持つ複数のポートフォリオをまたいで単一のシミュレーションを生成します。

         * *[!UICONTROL Individual Normalized]*：選択したポートフォリオごとに個別のシミュレーションを生成します。 ポートフォリオには、異なる目的と通貨が含まれる場合があります。

   7. （[!UICONTROL Portfolio Launch] インサイトのみ（オプション）。今後のローンチ日を指定するには、 **[!UICONTROL Optional Date]** フィールド。

   8. （[!UICONTROL Quality Score] insight のみ）該当する広告ネットワークを選択します。

   9. （[!UICONTROL Query Cross Matching] insight のみ） **[!UICONTROL Google Accounts]** メニューで、アカウントを選択します。

4. クリック **[!UICONTROL Generate Insight]**.

   ジョブが完了するか、失敗すると、に基づいて通知が届きます [設定済みの通知設定](/help/search-social-commerce/notifications/notification-edit.md) （用） [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [について [!UICONTROL Advertising Insights]](insight-about.md)
>* [を表示または保存します [!DNL Advertising Insight]](insight-view-save.md)
>* [を削除 [!DNL Advertising Insight]](insight-delete.md)
