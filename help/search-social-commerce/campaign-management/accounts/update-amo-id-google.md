---
title: アカウントの AMO ID （s_kwcid） トラッキングコード  [!DNL Google Ads]  更新
description: アカウントの最新の AMO ID トラッキングコードに切り替える方法  [!DNL Google Ads]  説明します。
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# [!DNL Google Ads] アカウントの AMO ID （s_kwcid） トラッキングコードの更新

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

*[!DNL Google Ads]アカウントのみ*

既存の [ アカウントの ](/help/integrations/analytics/ids.md#amo-id-formats)AMO ID トラッキングコード [!DNL Google Ads] の従来（2019 年 10 月以前）の形式では、Analytics の一部の機能がサポートされません。例えば、[!DNL Google Ads] Performance MAX キャンペーン、ドラフトおよび実験キャンペーンのキャンペーンレベルおよび広告グループレベルでのレポートや、複数のキャンペーンで同じ広告+キーワード+一致タイプの組み合わせが存在する他のユースケースなどです。

現在の形式には、キャンペーン ID と広告グループ ID のパラメーターが含まれます。

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

従来の形式を使用する既存のアカウントの場合は、現在の形式に変更できます。 Performance MAX キャンペーンまたはドラフトと実験キャンペーンがない場合は、新しい形式への移行はオプションです。

すべての新しい [!DNL Google Ads] アカウントで、現在の AMO ID 形式が自動的に使用されます。

>[!NOTE]
>
>このオプションは、現在の形式を使用していないアカウントでのみ使用できます。
>
>アカウントの移行後、すべてのクリック、コスト、インプレッションのデータは変更後に正しくレポートされますが、移行前に発生したクリックスルーは引き続き古い AMO ID 形式に基づくコンバージョンデータに関連付けられます。

1. メインメニューで、「\>」 **[!UICONTROL Search, Social, & Commerce]** 「\>」 **[!UICONTROL Campaigns]** 「\>」をクリッ **[!UICONTROL Campaigns]** します。 サブメニューで、[\> **[!UICONTROL Live]**]&#x200B;**[!UICONTROL Accounts]** クリックします。

1. アカウント名の上にカーソルを置き、![ 矢印ドロップダウンアイコン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png) をクリックして、「**[!UICONTROL Edit]**」を選択します。

1. 「**[!UICONTROL Set Account Tracking]**」をクリックします。

1. 移行を開始します。

   1. **[!UICONTROL S_KWCID FORMAT]** 設定の「[!UICONTROL Account Tracking]」の横にある「**[!UICONTROL LEGACY S_KWCID FORMAT]**」をクリックします。

   1. 「**[!UICONTROL Migrate to new s_kwcid format]**」をクリックします。

   1. 確認メッセージで、チェック ボックスをオンにし、[**[!UICONTROL Continue]**] をクリックします。

   1. アカウント設定で、「**[!UICONTROL Post]**」をクリックします。

   キャンペーンのメタデータは、数日以内に [!DNL Analytics] で更新されます。 トラッキングは中断されることなく継続されるので、データは失われませんが、すべてのメタデータを受け取るまでは、レポートに新しいトラッキングコード [!DNL Analytics] 反映されない場合があります。

   >[!NOTE]
   >
   >移行前に発生したすべてのクリックスルーで、引き続き古い形式に基づいたコンバージョンデータがレポートされます。

1. 移行を開始した後、必要に応じてランディングページのサフィックス設定（一部の広告ネットワークでは「最終的な URL サフィックス」と呼ばれます）を更新します。

   * トラッキング設定で「[!UICONTROL Auto Upload]」機能が有効になっている場合、検索、ソーシャルおよびCommerceは、このアカウントおよびそのキャンペーンのランディングページサフィックスのトラッキングコードを自動的に更新します。 何もする必要はありません。

   * [!UICONTROL Auto Upload]」機能が有効ではなく、[ サーバーサイド AMO ID 機能 ](/help/integrations/analytics/ids.md#amo-id-formats) を使用しない場合、ランディングページのサフィックス設定の AMO ID パラメーターを手動で更新する必要があります。 アカウントレベルとキャンペーンレベルのサフィックスは、[ アカウント設定 ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) および [ キャンペーン設定 ](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) または [ バルクシートに変更内容をアップロード ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) することで手動で変更できます。 広告グループレベル以下にサフィックスを設定するには、[!DNL Google Ads] エディターを使用します。

   * キャンペーンコンポーネントのベース URL 設定に AMO ID を含める場合は、関連するランディングページのサフィックス設定に移動します。

1. （推奨）追加のアカウントを移行する前に、[!DNL Analytics] でこのアカウントのデータを確認してください。

>[!MORELIKETHIS]
>
>* [ 広告ネットワークアカウントの管理 ](ad-network-account-manage.md)
>* [ 使用するAdobe Advertising ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [ 概要  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html?lang=ja){target="_blank"}
