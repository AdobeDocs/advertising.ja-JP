---
title: フィードから生成されたデータを表示
description: 在庫データフィードから生成されたデータを表示する方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# フィードから生成されたデータを表示

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

広告ネットワークに同時に投稿せずにフィードデータを伝播する場合、次のいずれかの方法でデータをプレビューできます。 後でオプションで [投稿データ](propagated-data-post.md) どちらの場所からも、関連する広告ネットワークに到達します。

* このオプションを[!UICONTROL Propagate and Preview]」、「`<feed file name>_<template name>`」) を [!UICONTROL Bulksheets] 表示 データが [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ このオプションを使用すると、次のことができます。 [ランディングページの検証](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) を、データを投稿する前の広告およびキーワードに関連付けました。

* このオプションを[!UICONTROL Propagate only]」と表示された場合、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ

   キャンペーン階層ビューには、フィードファイルから生成されたデータのみが表示され、既存のアカウントコンポーネントは表示されません。 コンポーネントとそのすべてのサブコンポーネントのデータが広告ネットワークに投稿されると、キャンペーン階層ビューには表示されなくなります。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;は、 [!UICONTROL Templates] タブをクリックします。

   1. （オプション）特定のテンプレート用に作成されたキャンペーンコンポーネントのみを表示するには、次の手順を実行します。

      1. テンプレート名をクリックします。

      1. 内 [!UICONTROL Accounts] 左側のナビゲーションウィンドウのメニューで、「広告ネットワーク」ノードと「広告ネットワークアカウント」ノードを展開し、テンプレート名の横にあるチェックボックスをオンにします。
   1. 次をクリック： **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**&#x200B;または **[!UICONTROL Ads]** タブに表示されます。

      >[!NOTE]
      >
      >* 特定のテンプレートのデータを表示しない限り、 [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブには、すべてのテンプレートおよびフィードファイルから作成されたすべての広告グループ、キーワードおよび広告が一覧表示されます。 使用する製品グループ [!DNL Google Ads] ショッピング広告は [!UICONTROL Keywords] タブをクリックします。
      >* 特定のキャンペーンのサブコンポーネントのみを表示するには、まず [!UICONTROL Campaigns] タブをクリックします。 同様に、特定の広告グループのサブコンポーネントのみを表示するには、まず [!UICONTROL Ad Groups] タブをクリックします。


   1. （オプション）詳細情報を表示するには、次のいずれかの操作を行います。

      * 任意のキャンペーン、広告グループ、キーワードまたは広告の設定を表示するには、 [設定を表示/編集アイコン](/help/search-social-commerce/assets/settings.png "設定を表示/編集アイコン") 名前の横にある

      * キャンペーンまたは広告グループのサブコンポーネントを表示するには、以下の手順を実行します。

         * キャンペーン内のすべての広告グループをリストするには、キャンペーン名をクリックします。

         * 広告グループ内のすべてのキーワードまたは製品ターゲットを一覧表示するには、広告グループ名をクリックします。

         * 広告グループ内のすべての広告を一覧表示するには、広告グループ名をクリックし、 [!UICONTROL Ads] タブをクリックします。


>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [フィードから生成されたデータを編集](propagated-data-edit.md)
>* [フィードから広告ネットワークに生成されたキャンペーンデータを投稿](propagated-data-post.md)
>* [在庫フィードデータの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)

