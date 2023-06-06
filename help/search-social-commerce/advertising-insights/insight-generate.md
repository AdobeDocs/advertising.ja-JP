---
title: を生成 [!DNL Advertising Insight]
description: 以下を作成する方法を説明します。 [!DNL Advertising Insight].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# を生成 [!DNL Advertising Insight]

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. 生成するインサイトをクリックします。

3. インサイト設定を指定します。

   1. ( 一部の報告は、（オプション）インサイトの日付範囲を指定します。

   2. （ほとんどのインサイト）分析するポートフォリオを選択します。

      一般に、アクティブなキャンペーンを含む最適化されたポートフォリオとアクティブなポートフォリオはすべて使用できます。 一部のインサイトについては、ポートフォリオリストをフィルタリングして、 **[!UICONTROL Only Optimized Portfolios]**.

      の場合 [!UICONTROL Day of Week] 十分な費用を持ち、過去 2 日間にターゲティングに費やしたポートフォリオのみを利用できます。

   3. ([!UICONTROL Event Path Beta] insight のみ ) 次の操作を行います。

      1. を選択します。 **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* ( [!UICONTROL Channel Assist Report] または [!UICONTROL Campaign Assist Report] を参照して、ユーザーイベントを分析用に個別のグループに分類する ) または *[!UICONTROL Analyze classified events]* （イベントグループをアップロードし、それらを使用してインサイトを生成する場合）。

      1. クリック **[!UICONTROL Select]** XLSX および ZIP（圧縮 XLSX）形式のファイルを見つけるには、 **[!UICONTROL Upload]**.
   4. ([!UICONTROL Google Account Audit] insight のみ ) 次の操作を行います。

      1. 次を入力します。 **[!UICONTROL Advertiser Name]** および **[!UICONTROL Account Name]**.

      1. を選択します。 **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* または *[!UICONTROL United Kingdom]*)、および **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]*&#x200B;または *[!UICONTROL German]*) をクリックします。

      1. クリック **[!UICONTROL Select]** アカウントに関してダウンロードしたキャンペーン、キーワード、履歴レポートを [!DNL Google Ads] web ユーザーインターフェイスと、そのアカウント用にからダウンロードした一括送信シートファイル [!DNL Google Ads Editor] アプリケーション。 次に、 **[!UICONTROL Upload]**.

         すべてのファイルは、CSV、TSV、TXT、ZIP（圧縮 CSV、TSV、TXT）形式である必要があります。
   5. ([!UICONTROL Location Target Performance] インサイトのみ（オプション）データを概要ではなく毎日集計するには、「 **[!UICONTROL Time Aggregation]** / *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] insight のみ ) 次の操作を行います。

      1. 内 **[!UICONTROL Step]** 「 」フィールドで、インサイトに含める目標支出レベルまたはステップの数を指定します。 値は、3(3) ～ 100 の間で指定できます。

      1. 内 **[!UICONTROL Type]** 「 」フィールドで、シミュレーションタイプを選択します。

         * *[!UICONTROL Optimized Multi-portfolio]*:同じ目標と通貨を持つ複数のポートフォリオにわたって、単一のシミュレーションを生成します。

         * *[!UICONTROL Individual Normalized]*:選択したポートフォリオごとに個別のシミュレーションを生成します。 ポートフォリオの目標と通貨が異なる場合があります。
   7. ([!UICONTROL Portfolio Launch] インサイトのみ（オプション）将来のローンチ日を指定するには、 **[!UICONTROL Optional Date]** フィールドに入力します。

   8. ([!UICONTROL Quality Score] insight のみ ) 該当する広告ネットワークを選択します。

   9. ([!UICONTROL Query Cross Matching] インサイトのみ ) **[!UICONTROL Google Accounts]** メニューで、アカウントを選択します。




4. クリック **[!UICONTROL Generate Insight]**.

   ジョブが完了した場合、またはジョブが失敗した場合、 [通知設定の構成](/help/search-social-commerce/notifications/notification-edit.md) 対象 [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [について [!UICONTROL Advertising Insights]](insight-about.md)
>* [表示または保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [の削除 [!DNL Advertising Insight]](insight-delete.md)

