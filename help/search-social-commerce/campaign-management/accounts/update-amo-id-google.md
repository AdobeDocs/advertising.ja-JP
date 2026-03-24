---
title: ' [!DNL Google Ads]  アカウントのAMO ID （s_kwcid） トラッキングコードを更新する'
description: ' [!DNL Google Ads]  アカウントの最新のAMO ID トラッキングコードに切り替える方法について説明します。'
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# [!DNL Google Ads] アカウントのAMO ID （s_kwcid） トラッキングコードを更新

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

*[!DNL Google Ads]アカウントのみ*

既存の[&#x200B; アカウントの](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)AMO ID トラッキングコード [!DNL Google Ads]の従来の（2019年10月より前）形式では、Analyticsの一部の機能がサポートされていません。例えば、[!DNL Google Ads] パフォーマンスの最大キャンペーンのキャンペーンやドラフトおよび実験キャンペーンのキャンペーンのキャンペーンおよび広告グループレベルでのレポート、および同じ広告+キーワード+マッチタイプの組み合わせが複数のキャンペーンに存在するユースケース場合場合などがあります。

現在の形式には、キャンペーン IDと広告グループ IDのパラメーターが含まれています。

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

従来の形式を使用する既存のアカウントの場合は、現在の形式に変更できます。 パフォーマンス最大数キャンペーンやドラフトおよび実験キャンペーンがない場合、新しい形式への移行はオプションです。

新しい[!DNL Google Ads] アカウントはすべて、現在のAMO ID形式を自動的に使用します。

>[!NOTE]
>
>このオプションは、現在の形式を使用していないアカウントでのみ使用できます。
>
>アカウントを移行すると、変更後にすべてのクリック、コスト、インプレッションデータが正しくレポートされますが、移行前に発生したクリックスルーは、引き続き古いAMO ID形式に基づくコンバージョンデータに関連付けられます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. アカウント名の上にカーソルを置き、![矢印ドロップダウンアイコン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png)をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

1. **[!UICONTROL Set Account Tracking]**&#x200B;をクリックします。

1. 移行を開始します。

   1. **[!UICONTROL S_KWCID FORMAT]**&#x200B;設定の[!UICONTROL Account Tracking]の横にある「**[!UICONTROL LEGACY S_KWCID FORMAT]**」をクリックします。

   1. **[!UICONTROL Migrate to new s_kwcid format]**&#x200B;をクリックします。

   1. 確認メッセージで、チェックボックスを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

   1. アカウント設定で、**[!UICONTROL Post]**&#x200B;をクリックします。

   キャンペーンのメタデータは、数日以内に[!DNL Analytics]に更新されます。 トラッキングは中断なく続くため、データは失われませんが、[!DNL Analytics]がすべてのメタデータを受信するまで、レポートに新しいトラッキングコードが反映されない場合があります。

   >[!NOTE]
   >
   >移行前に発生したすべてのクリックスルーでは、古い形式に基づいてコンバージョンデータがレポートされます。

1. 移行を開始したら、必要に応じてランディングページサフィックス設定（一部の広告ネットワークでは「最終URL サフィックス」と呼ばれます）を更新します。

   * トラッキング設定で「[!UICONTROL Auto Upload]」機能が有効になっている場合、Search, Social, &amp; Commerceは、このアカウントとそのキャンペーンのランディングページサフィックスのトラッキングコードを自動的に更新します。 何もする必要はありません。

   * [!UICONTROL Auto Upload]&quot;機能が有効になっておらず、[&#x200B; サーバーサイド AMO ID機能](/help/integrations/analytics/ids.md#)を使用しない場合は、ランディングページサフィックス設定でAMO ID パラメーターを手動で更新する必要があります。 アカウントおよびキャンペーンレベルのサフィックスは、[&#x200B; アカウント設定](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)および[&#x200B; キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)で手動で変更するか、バルクシート [に変更をアップロード &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)することで変更できます。 広告グループレベル以下でサフィックスを設定するには、[!DNL Google Ads] エディターを使用します。

   * キャンペーンコンポーネントのベース URL設定にAMO IDを含める場合は、関連するランディングページサフィックス設定に移動します。

1. （推奨）追加のアカウントを移行する前に、[!DNL Analytics]でこのアカウントのデータを確認してください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
>* [様が使用している [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID
>* [概要： [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html?lang=ja){target="_blank"}
