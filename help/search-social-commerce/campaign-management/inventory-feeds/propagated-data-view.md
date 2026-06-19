---
title: フィードから生成されたデータを表示
description: 在庫データフィードから生成されたデータを表示する方法について説明します。
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/AG-bR4RcQZcDjJTLkrWhC4J3RcYb7kBRRiC3moSCxp0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 429
ht-degree: 0%

---

# フィードから生成されたデータを表示

*[!DNL Google Ads]、[!DNL LY Ads] （削除操作のみ）、[!DNL Microsoft Advertising]、および[!DNL Yandex] アカウントのみ*

フィード データを広告ネットワークに同時に投稿せずに反映する場合は、次のいずれかの方法でデータをプレビューできます。 後で、オプションで[ データを投稿](propagated-data-post.md)して、いずれかの場所から関連する広告ネットワークに送信できます。

* このオプションを「[!UICONTROL Propagate and Preview]」に使用した場合は、生成されたバルクシート （「`<feed file name>_<template name>`」という名前）を[!UICONTROL Bulksheets] ビューから表示します。 データが[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads]のタブに含まれていません。 このオプションを使用すると、データを投稿する前に、広告とキーワードに関連付けられているランディングページ ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)を[検証できます。

* このオプションを「[!UICONTROL Propagate only]」に使用した場合、生成されたデータは、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads]のタブからキャンペーン階層ビューで表示されます。

  キャンペーン階層ビューには、フィードファイルから生成されたデータのみが表示され、既存のアカウントコンポーネントは表示されません。 コンポーネントとそのすべてのサブコンポーネントのデータが広告ネットワークに投稿されると、キャンペーン階層ビューにリストされなくなります。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックすると、[!UICONTROL Templates] タブが開きます。

   1. （オプション）特定のテンプレート用に作成されたキャンペーンコンポーネントのみを表示するには：

      1. テンプレート名をクリックします。

      1. 左側のナビゲーションパネルの[!UICONTROL Accounts] メニューで、広告ネットワークノードと広告ネットワークアカウントノードを展開し、テンプレート名の横にあるチェックボックスを選択します。

   1. 表示するコンポーネントに応じて、「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」、「**[!UICONTROL Keywords]**」または「**[!UICONTROL Ads]**」タブをクリックします。

      >[!NOTE]
      >
      >* 特定のテンプレートのデータを表示しない限り、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]および[!UICONTROL Ads]のタブには、すべてのテンプレートとフィード ファイルから作成されたすべての広告グループ、キーワード、および広告が一覧表示されます。 [!DNL Google Ads]件のショッピング広告に使用されている製品グループは、[!UICONTROL Keywords] タブに一覧表示されます。
      >* 特定のキャンペーンのサブコンポーネントのみを表示するには、まず「[!UICONTROL Campaigns]」タブを表示します。 同様に、特定の広告グループのサブコンポーネントのみを表示するには、まず「[!UICONTROL Ad Groups]」タブを表示します。

   1. （オプション）詳細を表示するには、次のいずれかの操作を行います。

      * キャンペーン、広告グループ、キーワード、広告の設定を表示するには、名前の横にある[設定を表示/編集アイコン ](/help/search-social-commerce/assets/settings.png "設定の表示/編集アイコン")をクリックします。

      * キャンペーンまたは広告グループのサブコンポーネントを表示するには、次の操作を行います。

         * キャンペーン内のすべての広告グループを一覧表示するには、キャンペーン名をクリックします。

         * 広告グループ内のすべてのキーワードまたは製品ターゲットを一覧表示するには、広告グループ名をクリックします。

         * 広告グループ内のすべての広告を一覧表示するには、広告グループ名をクリックし、「[!UICONTROL Ads]」タブをクリックします。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [ フィードから生成されたデータを編集](propagated-data-edit.md)
>* [ フィードから生成されたキャンペーンデータを広告ネットワークに投稿](propagated-data-post.md)
>* [在庫フィード データの投稿ジョブを停止](stop-job.md)
>* フィードから生成されたデータの[ ステータス ](propagated-data-status.md)
