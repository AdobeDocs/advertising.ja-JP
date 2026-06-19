---
title: フィードから生成されたデータの編集
description: 在庫データフィードから生成されたデータを編集する方法について説明します。
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/YAjOramjWXPJmOkLB2dhjG3PLUUAEbDAPRBYLVSl3vo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 426
ht-degree: 0%

---

# フィードから生成されたデータの編集

*[!DNL Google Ads]、[!DNL LY Ads] （削除操作のみ）、[!DNL Microsoft Advertising]、および[!DNL Yandex] アカウントのみ*

フィード データを広告ネットワークに同時に投稿せずに反映する場合は、次のいずれかの方法でデータを編集できます。 後で、オプションで[ データを投稿](propagated-data-post.md)して、いずれかの場所から関連する広告ネットワークに送信できます。

* このオプションを「[!UICONTROL Propagate and Preview]」に使用した場合は、生成されたバルクシート ファイル （「`<feed file name>_<template name>`」という名前）を、[!UICONTROL Bulksheets] ビューからダウンロードし、ファイルを編集して、再度アップロードすることで編集できます。 データが[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads]のタブに含まれていません。

* このオプションを「[!UICONTROL Propagate only]」に使用した場合、キャンペーン階層ビュー内の[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads]のタブから、[[!UICONTROL New] ステータス ](propagated-data-status.md)のコンポーネントに対して生成されたデータを編集できます。

  キャンペーン階層ビューには、フィードファイルから生成されたデータのみが表示され、既存のアカウントコンポーネントは表示されません。 コンポーネントとそのすべてのサブコンポーネントのデータが広告ネットワークに投稿されると、キャンペーン階層にリストされなくなります。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックすると、[!UICONTROL Templates] タブが開きます。

   1. （オプション）特定のテンプレート用に作成されたキャンペーンコンポーネントのみを表示するには：

      1. テンプレート名をクリックします。

      1. 左側のナビゲーションパネルの[!UICONTROL Accounts] メニューで、広告ネットワークノードと広告ネットワークアカウントノードを展開し、テンプレート名の横にあるチェックボックスを選択します。

   1. 表示するコンポーネントに応じて、「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」、「**[!UICONTROL Keywords]**」または「**[!UICONTROL Ads]**」タブをクリックします。

      >[!NOTE]
      >
      >* 特定のテンプレートのデータを表示しない限り、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]および[!UICONTROL Ads]のタブには、すべてのテンプレートとフィード ファイルから作成されたすべての広告グループ、キーワード、および広告が一覧表示されます。 [!DNL Google Ads]件のショッピング広告に使用されている製品グループは、[!UICONTROL Keywords] タブに一覧表示されます。
      >* 特定のキャンペーンのサブコンポーネントのみを表示するには、まず「[!UICONTROL Campaigns]」タブを表示します。 同様に、特定の広告グループのサブコンポーネントのみを表示するには、まず「[!UICONTROL Ad Groups]」タブを表示します。

   1. （オプション、広告グループ、キーワード、または広告のみを編集するには）特定のキャンペーンまたは広告グループのサブコンポーネントのみを含めるようにリストをフィルタリングします。

      * キャンペーン内のすべての広告グループを一覧表示するには、キャンペーン名をクリックします。

      * 広告グループ内のすべてのキーワードを一覧表示するには、広告グループ名をクリックします。

      * 広告グループ内のすべてをリストするには、広告グループ名をクリックし、「[!UICONTROL Ads]」タブをクリックします。

   1. キャンペーン、広告グループ、キーワード、または広告名の横にある[設定の表示/編集アイコン ](/help/search-social-commerce/assets/settings.png "設定の表示/編集アイコン")をクリックします。

   1. 設定を編集し、**[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [ フィードから生成されたデータを表示](propagated-data-view.md)
>* [ フィードから生成されたキャンペーンデータを広告ネットワークに投稿](propagated-data-post.md)
>* [在庫フィード データの投稿ジョブを停止](stop-job.md)
>* フィードから生成されたデータの[ ステータス ](propagated-data-status.md)
