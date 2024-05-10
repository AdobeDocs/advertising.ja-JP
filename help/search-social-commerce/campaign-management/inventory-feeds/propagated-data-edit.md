---
title: フィードから生成されたデータを編集
description: 在庫データフィードから生成されたデータを編集する方法を説明します。
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# フィードから生成されたデータを編集

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] （削除アクションのみ）、 [!DNL Yandex] アカウントのみ*

フィード データを広告ネットワークに同時に投稿せずに伝達する場合は、次のいずれかの方法でデータを編集できます。 後で必要に応じて実行できます [データを投稿](propagated-data-post.md) どちらかの場所から関連する広告ネットワークに移動します。

* オプションを使用して「[!UICONTROL Propagate and Preview]」を選択した場合、生成されたバルクシートファイル（「」という名前）を編集できます`<feed file name>_<template name>`&quot;）に設定する必要があります。 [!UICONTROL Bulksheets] ファイルを表示、編集、再度アップロードします。 にはデータは含まれていません [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ。

* オプションを使用して「[!UICONTROL Propagate only]を使用すると、コンポーネント用に生成されたデータを [[!UICONTROL New] ステータス](propagated-data-status.md) からのキャンペーン階層内の表示 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ。

  キャンペーン階層ビューには、フィードファイルから生成されたデータのみが表示され、既存のアカウントコンポーネントは表示されません。 コンポーネントとそのすべてのサブコンポーネントのデータが広告ネットワークに投稿されると、キャンペーン階層に表示されなくなります。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

   1. （任意）特定のテンプレート用に作成されたキャンペーンコンポーネントのみを表示するには、次の手順を実行します。

      1. テンプレート名をクリックします。

      1. が含まれる [!UICONTROL Accounts] メニュー左側のナビゲーションウィンドウで、ad network ノード、ad network account ノードの順に展開し、テンプレート名の横にあるチェックボックスをオンにします。

   1. 「」をクリックします **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**、または **[!UICONTROL Ads]** タブをクリックします（表示するコンポーネントによって異なります）。

      >[!NOTE]
      >
      >* 特定のテンプレートのデータを表示しない限り、 [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブには、すべてのテンプレートおよびフィードファイルから作成されたすべての広告グループ、キーワード、および広告が一覧表示されます。 使用される製品グループ [!DNL Google Ads] ショッピング広告のリスト [!UICONTROL Keywords] タブ。
      >* 特定のキャンペーンのサブコンポーネントのみを表示するには、最初に以下を表示します。 [!UICONTROL Campaigns] タブ。 同様に、特定の広告グループのサブコンポーネントのみを表示するには、まず次の項目を表示します [!UICONTROL Ad Groups] タブ。

   1. （オプション：広告グループ、キーワードまたは広告のみを編集する場合）リストをフィルタリングして、特定のキャンペーンまたは広告グループのサブコンポーネントのみを含めます。

      * キャンペーンのすべての広告グループをリストするには、キャンペーン名をクリックします。

      * 広告グループ内のすべてのキーワードをリストするには、広告グループ名をクリックします。

      * 広告グループ内のすべての名前を一覧表示するには、広告グループ名をクリックし、 [!UICONTROL Ads] タブ。

   1. クリック [設定を表示/編集アイコン](/help/search-social-commerce/assets/settings.png "設定を表示/編集アイコン") キャンペーン、広告グループ、キーワードまたは広告名の横。

   1. 設定を編集し、 **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから広告ネットワークにキャンペーン データを投稿](propagated-data-post.md)
>* [在庫フィード データの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)
