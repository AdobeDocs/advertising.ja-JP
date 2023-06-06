---
title: フィードから生成されたデータを編集
description: 在庫データフィードから生成されたデータを編集する方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# フィードから生成されたデータを編集

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

広告ネットワークに同時に投稿せずにフィードデータを伝播する場合、次のいずれかの方法でデータを編集できます。 後でオプションで [投稿データ](propagated-data-post.md) どちらの場所からも、関連する広告ネットワークに対して、次の操作を実行します。

* このオプションを[!UICONTROL Propagate and Preview]」と入力すると、生成された bulksheet ファイル (`<feed file name>_<template name>`」) を [!UICONTROL Bulksheets] ファイルを表示、編集し、再度アップロードする。 データが [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ

* このオプションを[!UICONTROL Propagate only]」と表示された場合、 [[!UICONTROL New] ステータス](propagated-data-status.md) を [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ

   キャンペーン階層ビューには、フィードファイルから生成されたデータのみが表示され、既存のアカウントコンポーネントは表示されません。 コンポーネントとそのすべてのサブコンポーネントのデータが広告ネットワークに投稿されると、キャンペーン階層には表示されなくなります。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;は、 [!UICONTROL Templates] タブをクリックします。

   1. （オプション）特定のテンプレート用に作成されたキャンペーンコンポーネントのみを表示するには、次の手順を実行します。

      1. テンプレート名をクリックします。

      1. 内 [!UICONTROL Accounts] 左側のナビゲーションウィンドウのメニューで、「広告ネットワーク」ノードと「広告ネットワークアカウント」ノードを展開し、テンプレート名の横にあるチェックボックスをオンにします。
   1. 次をクリック： **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**&#x200B;または **[!UICONTROL Ads]** タブに表示されます。

      >[!NOTE]
      >
      >* 特定のテンプレートのデータを表示しない限り、 [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブには、すべてのテンプレートおよびフィードファイルから作成されたすべての広告グループ、キーワードおよび広告が一覧表示されます。 使用する製品グループ [!DNL Google Ads] ショッピング広告は [!UICONTROL Keywords] タブをクリックします。
      >* 特定のキャンペーンのサブコンポーネントのみを表示するには、まず [!UICONTROL Campaigns] タブをクリックします。 同様に、特定の広告グループのサブコンポーネントのみを表示するには、まず [!UICONTROL Ad Groups] タブをクリックします。


   1. ( オプション、広告グループ、キーワード、広告のみを編集する場合 ) リストをフィルタリングして、特定のキャンペーンまたは広告グループのサブコンポーネントのみを含めます。

      * キャンペーン内のすべての広告グループをリストするには、キャンペーン名をクリックします。

      * 広告グループ内のすべてのキーワードを一覧表示するには、広告グループ名をクリックします。

      * 広告グループ内のすべてをリストするには、広告グループ名をクリックし、 [!UICONTROL Ads] タブをクリックします。
   1. クリック [設定を表示/編集アイコン](/help/search-social-commerce/assets/settings.png "設定を表示/編集アイコン") キャンペーン、広告グループ、キーワードまたは広告名の横に表示されます。

   1. 設定を編集し、 **[!UICONTROL Save]**.



>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから広告ネットワークに生成されたキャンペーンデータを投稿](propagated-data-post.md)
>* [在庫フィードデータの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)

