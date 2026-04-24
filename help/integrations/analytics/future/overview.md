---
title: Adobe AdvertisingとAdobe Analyticsの統合
description: Adobe AdvertisingでAdobe Analyticsとデータを交換する方法と、Search, Social, & Commerce内でデータを使用する方法について説明します。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Adobe AdvertisingとAdobe Analyticsの統合

Adobe AdvertisingとAnalyticsは、次の方法で統合できます。

## [!DNL Analytics]とAdobe Advertising間のデータ交換

### [!DNL Analytics] データをAdobe Advertisingに取り込みます

[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)、[!DNL Search, Social, & Commerce]およびDSPで次の操作を行います。

* **[!DNL Analytics]セグメント：** [!DNL Analytics]に作成され、Adobe CX Enterpriseに公開されたすべての広告主または代理店のセグメントのメタデータ、階層データ、および一意のオーディエンスデータ。

* **[!DNL Analytics]サイトエンゲージメント指標**

* **[!DNL Analytics]標準、カスタム、および予約済み指標**

### Adobe Advertising データを[!DNL Analytics]に送信

* **Adobe Advertisingからのトラフィック指標**

* **Adobe Advertisingからのディメンション**

>[!NOTE]
>
>[!DNL Search, Social, & Commerce]の場合、この機能はほとんどの広告ネットワークとキャンペーンの種類でサポートされています。 詳しくは、[!DNL Search, Social, & Commerce] ガイドの「サポートされているインベントリ」を参照してください。<!-- add link when that's published in ExL -->

### [!DNL Analytics] セグメントを使用して[!DNL Google Ads] オーディエンスを作成 {#audience-manager-google-audiences}

*オプトインした広告主で[!DNL Advertising Search, Social, & Commerce]さんのみ*

<!-- Verify all -->

[!DNL Search, Social, & Commerce]内で、既存の[!DNL Analytics] セグメントを使用して、ユーザーIDから[!DNL Google Ads]個のGoogle カスタマーマッチオーディエンスを作成できます。 これには、Adobe CX Enterpriseに公開されるAdobe Analytics セグメントと、Adobe CX Enterprise [!DNL Audience Library]を使用して作成されるセグメントが含まれます。 詳しくは、「[Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)」を参照してください。

[ ユーザーIDの顧客マッチオーディエンス ](https://support.google.com/google-ads/answer/9199250)は、web サイトのタグベースのオーディエンスと同様に機能しますが、PII以外のIDは、標準の顧客マッチオーディエンスとweb サイトのタグベースのオーディエンスに対して明確なメリットを得るために、一意のオーディエンスメンバーに割り当てられます。

必要なユーザーIDを作成するには、web サイトでAdobe Advertising JavaScript タグ <!-- with a user ID parameter -->を使用する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

![ セグメント作成プロセス ](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、[!DNL Google Ads] キャンペーンで[ キャンペーンレベルまたは広告グループレベルのターゲットまたは除外](#audience-manager-targets)として使用できます。

### [!DNL Analytics] セグメントを使用した広告のターゲティングまたは除外 {#analytics-targets}

* （オプトインした広告主と[!DNL Search, Social, & Commerce]）キャンペーン レベルまたは広告グループレベルのターゲットまたは除外として [!DNL Analytics]  セグメント ](#audience-manager-google-audiences)を使用して[作成された[!DNL Google Ads]個のオーディエンスを[!DNL Google Ads] キャンペーンで使用できます。

* （DSPを使用している広告主）既存の[!DNL Analytics] セグメントを広告プレースメントのターゲットとして使用できます。 オプションで、セグメントを再利用可能なオーディエンスに含めることができます。このオーディエンスは、複数のプレースメントのターゲットまたは除外として使用できます。

* （Advertising Creativeを使用している広告主）既存の[!DNL Analytics] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用できます。
