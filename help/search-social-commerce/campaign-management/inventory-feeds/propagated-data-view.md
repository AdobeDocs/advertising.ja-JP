---
title: フィードから生成されたデータを表示
description: 在庫データフィードから生成されたデータを表示する方法を説明します。
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# フィードから生成されたデータを表示

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

フィード データを広告ネットワークに同時に投稿せずに伝達する場合は、次のいずれかの方法でデータをプレビューできます。 後で必要に応じて、いずれかの場所から関連する広告ネットワークに [ データを投稿 ](propagated-data-post.md) することもできます。

* オプションを「[!UICONTROL Propagate and Preview]」に設定した場合は、生成されたバルクシート （「`<feed file name>_<template name>`」という名前）を [!UICONTROL Bulksheets] ビューから表示します。 「[!UICONTROL Campaigns]」、「[!UICONTROL Ad Groups]」、「[!UICONTROL Keywords]」、「[!UICONTROL Ads]」の各タブには、データは含まれていません。 このオプションを使用すると、データを投稿する前に、広告およびキーワードに関連付けられた [ ランディングページの検証 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) を行うことができます。

* オプションを「[!UICONTROL Propagate only]」に使用した場合は、キャンペーン階層ビュー内の生成されたデータを「[!UICONTROL Campaigns]」、「[!UICONTROL Ad Groups]」、「[!UICONTROL Keywords]」および「[!UICONTROL Ads]」タブから表示します。

  キャンペーン階層ビューには、フィードファイルから生成されたデータのみが表示され、既存のアカウントコンポーネントは表示されません。 コンポーネントとそのすべてのサブコンポーネントのデータが広告ネットワークに投稿されると、キャンペーン階層ビューにそのデータが表示されなくなります。

   1. メインメニューで、**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

   1. （任意）特定のテンプレート用に作成されたキャンペーンコンポーネントのみを表示するには、次の手順を実行します。

      1. テンプレート名をクリックします。

      1. 左側のナビゲーション ウィンドウの [!UICONTROL Accounts] メニューで、[ 広告ネットワーク ] ノードと [ 広告ネットワーク アカウント ] ノードを展開し、テンプレート名の横にあるチェック ボックスをオンにします。

   1. 表示するコンポーネントに応じて、「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」、「**[!UICONTROL Keywords]**」または「**[!UICONTROL Ads]**」タブをクリックします。

      >[!NOTE]
      >
      >* 特定のテンプレートのデータを表示しない場合、「[!UICONTROL Ad Groups]」、「[!UICONTROL Keywords]」および「[!UICONTROL Ads]」タブには、すべてのテンプレートおよびフィードファイルから作成されたすべての広告グループ、キーワードおよび広告が一覧表示されます。 買い物かごに使用される製品グループ [!DNL Google Ads]、「[!UICONTROL Keywords]」タブに表示されます。
      >* 特定のキャンペーンのサブコンポーネントのみを表示するには、まず「[!UICONTROL Campaigns]」タブを表示します。 同様に、特定の広告グループのサブコンポーネントのみを表示するには、まず「[!UICONTROL Ad Groups]」タブを表示します。

   1. （オプション）詳細情報を表示するには、次のいずれかの操作を行います。

      * キャンペーン、広告グループ、キーワードまたは広告の設定を表示するには、名前の横にある [ 設定を表示/編集アイコン ](/help/search-social-commerce/assets/settings.png "設定を表示/編集アイコン") をクリックします。

      * キャンペーンまたは広告グループのサブコンポーネントを表示するには、次の手順を実行します。

         * キャンペーンのすべての広告グループをリストするには、キャンペーン名をクリックします。

         * 広告グループ内のすべてのキーワードまたは製品ターゲットをリストするには、広告グループ名をクリックします。

         * 広告グループ内のすべての広告を一覧表示するには、広告グループ名をクリックし、[[!UICONTROL Ads]] タブをクリックします。

>[!MORELIKETHIS]
>
>* [ 在庫フィードについて ](inventory-feeds-about.md)
>* [ フィードから生成されたデータを編集 ](propagated-data-edit.md)
>* [ フィードから広告ネットワークにキャンペーンデータを投稿する ](propagated-data-post.md)
>* [ 在庫フィード データの転記ジョブを停止 ](stop-job.md)
>* [ フィードから生成されたデータのステータス ](propagated-data-status.md)
