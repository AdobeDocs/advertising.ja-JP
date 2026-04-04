---
title: Adobe AdvertisingとAdobe Audience Managerの統合
description: Adobe AdvertisingがAdobe Audience Managerとデータを交換する様々な方法について説明します。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Adobe AdvertisingとAdobe Audience Managerの統合

Adobe AdvertisingとAudience Managerは、次の方法で統合できます。

## Audience Managerと他の[!DNL Adobe] セグメントの同期による広告のターゲティング

[!DNL Search, Social, & Commerce]とDSPは、広告主または代理店のAudience Managerおよびその他[!DNL Adobe]のオーディエンスのメタデータ、階層データ、固有のオーディエンスデータを取り込むことができます。 この独自の連携は、Adobe Advertisingを使用しているマーケターのみが利用できます。 「[広告ターゲティング用にAdobe Audience Manager セグメントを読み込む](/help/integrations/audience-manager/import-audiences.md)」を参照してください。

### Audience Managerと他の[!DNL Adobe] セグメントを使用して、[!DNL Google Ads] オーディエンスを作成します {#audience-manager-google-audiences}

*オプトインした広告主で[!DNL Advertising Search, Social, & Commerce]さんのみ*

[!DNL Search, Social, & Commerce]内で、[!DNL Google Ads]と[!UICONTROL Adobe Media Optimizer (HTTP)]を宛先として持つ既存のAudience Manager セグメントを使用して、ユーザーIDから[!UICONTROL Adobe Media Optimizer Batch Destination]個の顧客一致オーディエンスを作成できます。 （[!DNL Media Optimizer]は[!DNL Search, Social, & Commerce]の旧名です）これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントと、Adobe Experience Cloud [!DNL Audience Library]を使用して作成されるセグメントが含まれます。 詳しくは、「[Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)」を参照してください。

[&#x200B; ユーザーIDの顧客マッチオーディエンス &#x200B;](https://support.google.com/google-ads/answer/9199250)は、web サイトのタグベースのオーディエンスと同様に機能しますが、PII以外のIDは、標準の顧客マッチオーディエンスとweb サイトのタグベースのオーディエンスに対して明確なメリットを得るために、一意のオーディエンスメンバーに割り当てられます。

必要なユーザーIDを作成するには、web サイトでAdobe Advertising JavaScript タグ <!-- with a user ID parameter -->を使用する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

![&#x200B; セグメント作成プロセス &#x200B;](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、[!DNL Google Ads] キャンペーンで[&#x200B; キャンペーンレベルまたは広告グループレベルのターゲットまたは除外](#audience-manager-targets)として使用できます。

### Audience Managerおよびその他[!DNL Adobe] セグメントを使用して広告をターゲティングまたは除外する {#audience-manager-targets}

* （オプトインした広告主と[!DNL Search, Social, & Commerce]）キャンペーン レベルまたは広告グループレベルのターゲットまたは除外として[!DNL Google Ads] セグメント [を使用して [!DNL Adobe] 作成された](#audience-manager-google-audiences)個のオーディエンスを[!DNL Google Ads] キャンペーンで使用できます。

* （DSPを使用している広告主）既存の[!DNL Adobe] セグメントを広告プレースメントのターゲットとして使用できます。 オプションで、セグメントを再利用可能なオーディエンスに含めることができます。このオーディエンスは、複数のプレースメントのターゲットまたは除外として使用できます。

* （Advertising Creativeを使用している広告主）既存の[!DNL Adobe] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用できます。

>[!NOTE]
>
>Audience ManagerおよびExperience Cloud [!DNL Audience Library] インターフェイスでオーディエンスを作成する方法と、様々なオーディエンスタイプの一般的なユースケースについて詳しくは、「[&#x200B; オーディエンス作成オプション &#x200B;](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=ja)」を参照してください。

## DSPのメディア露出データをAudience Managerに送信

*DSPのみの広告主*

Adobe Audience Managerを使用しているDSPのお客様は、Audience Managerへのpixel呼び出しを使用して、広告キャンペーンからデータを取得できます。 キャンペーンのデータを使用してルールベースの特性を構築し、新しいセグメントを定義して、より高度なセグメンテーション、頻度の管理、マーケティング分析、レポートインサイトなど、DSPの様々なユースケースを実現できます。

詳しくは、「[Adobe Audience ManagerへのDSP メディア露出データの送信の概要](/help/integrations/audience-manager/media-data-integration/overview.md)」を参照してください。

## Audience Analyticsで、サイトのアクティビティに関するより詳細なインサイトを獲得

[[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ja)のAdobe Advertisingのお客様は、Adobe Advertisingで追跡されたデータとAudience Manager セグメントの両方を[!DNL Analytics]に送信して、サイトのアクティビティに関する詳細なインサイトを得ることができます。

詳しくは、「[[!DNL Adobe Audience Analytics] Adobe Advertisingのお客様](/help/integrations/audience-manager/audience-analytics.md)」を参照してください。
