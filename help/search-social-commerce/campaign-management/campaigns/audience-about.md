---
title: About audiences
description: Learn about options to track, create, and manage [!DNL Google Ads] and [!DNL Microsoft Advertising] audiences.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/B77S28vEpSkrgNmhc-Ekn7PXh3W-y2g9et2y3gCQPK8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 0%

---

# About managing [!DNL Google Ads] and [!DNL Microsoft Advertising] audiences in Search, Social, &amp; Commerce

*[!DNL Google Ads]and [!DNL Microsoft Advertising] only*

The Audiences Library lists all of your [!DNL Google Ads] customer data-based, in-market, and similar audiences and your [!DNL Microsoft Advertising] remarketing and dynamic remarketing, custom, customer match, in-market, and similar audiences. You can use any of the [!DNL Google Ads] audiences as [!DNL Google Ads] campaign-level and ad group-level targets and exclusions, and you can use any of the [!DNL Microsoft Advertising] audiences as [!DNL Microsoft Advertising] campaign-level and ad group-level targets and (dynamic remarketing audiences only) exclusions. You can add or edit a bid adjustment for any audience target.

You can also create and manage audiences using segments or email lists from your existing Adobe CX Enterprise audiences and from various kinds of customer data from your customer relationship management (CRM) system:

* **Adobe audience segments:** Advertisers with opted-in Adobe Audience Manager or Adobe Analytics accounts can create [!DNL Google Ads] customer match audiences from their [!DNL Adobe] segments:

   * (Advertisers with [!DNL Analytics] accounts who don&#39;t also have Audience Manager) You can create [!DNL Google Ads] customer match audiences using user IDs from [!DNL Analytics] segments that are shared with Adobe CX Enterprise.

   * (Advertisers with Audience Manager accounts) You can create [!DNL Google Ads] customer match audiences using user IDs from Audience Manager segments that have Search, Social, &amp; Commerce as a destination. This may include Adobe Analytics segments that are published to Adobe CX Enterprise and segments created using the Adobe CX Enterprise Audience Library.

  To create customer match audiences, the advertiser&#39;s [!DNL Google Ads] account must be [eligible for custom match](https://support.google.com/adspolicy/answer/6299717) and opted in for [user ID segments](https://support.google.com/google-ads/answer/9199250). Also, the advertiser account in Search, Social, &amp; Commerce must be configured to allow the creation of customer match audiences.

  [!DNL Adobe] segment data and cookie sync files for customer data-based audiences are synced to [!DNL Google Ads] daily.

* **Adobe Campaign email lists:** Your Adobe Account Team can help you set up a workflow to create and update a [!DNL Google Ads] customer match audience from an email list within [!DNL Campaign].

* **Customer data lists:** Advertisers with [!DNL Google Ads] or [!DNL Microsoft Advertising] accounts that are eligible for customer match can create and update an ad network-specific customer data-based audience &lt;!-- or dynamic remarketing audience -- included in customer data-based audience, at least for [!DNL Google Ads]?--> by uploading a CSV file with primary identifiers.

* **Dynamic remarketing lists:** Advertisers with [!DNL Microsoft Advertising] accounts can create and manage dynamic remarketing audiences, which you can use to retarget potential customers who have recently interacted with your products in one of multiple ways (such as product viewers or past buyers). Dynamic remarketing audiences require you to use the ad network&#39;s JavaScript conversion- and audience-tracking tag on your webpages. Use dynamic remarketing lists with shopping campaigns on the search and audience networks to retarget audiences with product ads, as well as with search campaigns to retarget audiences with text ads and dynamic search ads. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Bid modifiers for dynamic remarketing audience targets aren&#39;t optimized in portfolios with the &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; setting.

>[!NOTE]
>
>Search, Social, &amp; Commerce doesn&#39;t store any of the customer data you upload or from the [!DNL Adobe] segments used to create or edit a [!DNL Google Ads] or [!DNL Microsoft Advertising] audience.

>[!MORELIKETHIS]
>
>* [Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Adobe Campaignのメールリストから [!DNL Google Ads] 顧客マッチオーディエンスを作成](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
>* [ キャンペーンと広告グループのオーディエンスターゲットの管理](audience-targets-manage.md)
>* [ キャンペーンと広告グループのオーディエンス除外の管理](audience-exclusions-manage.md)
