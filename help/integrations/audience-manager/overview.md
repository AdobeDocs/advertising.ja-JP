---
title: Adobe AdvertisingとAdobe Audience Managerの統合
description: Adobe AdvertisingとAdobe Audience Managerでデータを交換する様々な方法について説明します。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Adobe AdvertisingとAdobe Audience Managerの統合

Adobe AdvertisingをAudience Managerと統合するには、次の方法があります。

## 広告ターゲティング用にAudience Managerと他の [!DNL Adobe] セグメントを同期

[!DNL Search, Social, & Commerce] とDSPは、すべての広告主または代理店のAudience Managerやその他の [!DNL Adobe] ーザーオーディエンスのメタデータ、階層データおよび一意のオーディエンスデータを取り込むことができます。 この一意の接続は、Adobe Advertisingを使用しているマーケターのみが利用できます。 「[ 広告ターゲティング用のAdobe Audience Manager セグメントの読み込み ](/help/integrations/audience-manager/import-audiences.md)」を参照してください。

### Audience Managerやその他の [!DNL Adobe] セグメントを使用して、オーディエンスを作成 [!DNL Google Ads] ます {#audience-manager-google-audiences}

*オプトイン済みの [!DNL Advertising Search, Social, & Commerce] のみを使用する広告主*

[!DNL Search, Social, & Commerce] 内では、[!DNL Google Ads] および [!UICONTROL Adobe Media Optimizer (HTTP)] を宛先として持つ既存のAudience Manager セグメントを使用して、ユーザー ID からカスタマーマッチオーディエンスを作成で [!UICONTROL Adobe Media Optimizer Batch Destination] ます。 （[!DNL Media Optimizer] は [!DNL Search, Social, & Commerce] の旧名称です。）これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントと、Adobe Experience Cloud [!DNL Audience Library] を使用して作成されるセグメントが含まれます。 詳しくは、「[ オーディエンスから  [!DNL Google Ads]  オーディエンスに一致する顧客の作成  [!DNL Adobe]  オーディエンス ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)」を参照してください。

[ ユーザー ID からのカスタマーマッチオーディエンス ](https://support.google.com/google-ads/answer/9199250) は web サイトタグベースのオーディエンスと同様に機能しますが、非 PII ID は一意のオーディエンスメンバーに割り当てられるので、標準のカスタマーマッチや web サイトタグベースのオーディエンスよりも明確なメリットがあります。

必要なユーザー ID を作成するには、web サイトでAdobe Advertising JavaScript タグを使用する必要があります <!-- with a user ID parameter --> 詳しくは、Adobe アカウントチームにお問い合わせください。

![ セグメント作成プロセス ](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、[!DNL Google Ads] のキャンペーンで [ キャンペーンレベルまたは広告グループレベルのターゲットまたは除外 ](#audience-manager-targets) として使用できます。

### Audience Managerやその他の [!DNL Adobe] セグメントを使用して、広告のターゲティングや除外を行います {#audience-manager-targets}

* （[!DNL Search, Social, & Commerce] を使用したオプトインの広告主）キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [!DNL Google Ads][ セグメントを使用して作成  [!DNL Adobe]  された任意の ](#audience-manager-google-audiences) オーディエンスを、[!DNL Google Ads] キャンペーンで使用できます。

* （DSPを使用する広告主）既存の [!DNL Adobe] セグメントを広告プレースメントのターゲットとして使用できます。 オプションで、再利用可能なオーディエンスにセグメントを含めることができ、複数のプレースメントのターゲットまたは除外として使用できます。

* （Advertising Creativeを使用する広告主）既存の [!DNL Adobe] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用できます。

>[!NOTE]
>
>Audience ManagerおよびExperience Cloudの [!DNL Audience Library] インターフェイスでオーディエンスを作成する方法、およびさまざまなオーディエンスタイプの一般的なユースケースについて詳しくは、「[ オーディエンス作成オプション ](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)」を参照してください。

## DSP Media の公開データをAudience Managerに送信する

*DSPのみの広告主*

Adobe Audience Managerを使用するDSPのお客様は、Audience Managerへのピクセル呼び出しを使用して、広告キャンペーンからデータをキャプチャできます。 その後、キャンペーンデータを使用して、ルールベースの特性を作成し、新しいセグメントを定義して、より高度なセグメント化、頻度管理、マーケティング分析、レポートインサイトなど、DSPの様々なユースケースを可能にすることができます。

詳しくは、[DSP media の公開データをAdobe Audience Managerに送信する方法の概要」を参照 ](/help/integrations/audience-manager/media-data-integration/overview.md) てください。

## Audience Analyticsでサイトアクティビティに関する豊富なインサイトを取得

[[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) を使用しているAdobe Advertisingのお客様は、Adobe Advertisingで追跡されたデータとAudience Manager セグメントの両方を [!DNL Analytics] に送信して、サイトアクティビティに関する有益なインサイトを得ることができます。

詳しくは、[[!DNL Adobe Audience Analytics] Adobe Advertisingのお客様向け ](/help/integrations/audience-manager/audience-analytics.md) を参照してください。
