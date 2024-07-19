---
title: Adobe Audience ManagerとのAdobe Advertising統合
description: Adobe AdvertisingがAdobe Audience Managerとデータを交換する様々な方法について説明します。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Adobe Audience ManagerとのAdobe Advertising統合

次の方法で、Adobe AdvertisingとAudience Managerを統合できます。

## 広告ターゲティング用にAudience Managerと他の [!DNL Adobe] セグメントを同期

[!DNL Search, Social, & Commerce] とDSPは、すべての広告主または代理店のAudience Managerや他の [!DNL Adobe] ーザーオーディエンスのメタデータ、階層データおよび一意のオーディエンスデータを取り込むことができます。 この一意の接続は、Adobe Advertisingを使用しているマーケターのみが利用できます。 「[ 広告ターゲティング用のAdobe Audience Manager セグメントの読み込み ](/help/integrations/audience-manager/import-audiences.md)」を参照してください。

### Audience Managerやその他の [!DNL Adobe] セグメントを使用して [!DNL Google Ads Audiences] を作成する {#audience-manager-google-audiences}

*オプトイン済みの [!DNL Advertising Search, Social, & Commerce] のみを使用する広告主*

[!DNL Search, Social, & Commerce] 内では、[!UICONTROL Adobe Media Optimizer (HTTP)] および [!UICONTROL Adobe Media Optimizer Batch Destination] を宛先として持つ既存のAudience Managerセグメントを使用して、ユーザー ID からカスタマーマッチオーディエンスを作成で [!DNL Google Ads] ます。 （[!DNL Media Optimizer] は [!DNL Search, Social, & Commerce] の旧名称） これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントと、Adobe Experience Cloud [!DNL Audience Library] を使用して作成されるセグメントが含まれます。 詳しくは、「[ オーディエンスから  [!DNL Google Ads]  オーディエンスに一致する顧客の作成  [!DNL Adobe]  オーディエンス ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)」を参照してください。

[ ユーザー ID からのカスタマーマッチオーディエンス ](https://support.google.com/google-ads/answer/9199250) は web サイトタグベースのオーディエンスと同様に機能しますが、非 PII ID は一意のオーディエンスメンバーに割り当てられるので、標準のカスタマーマッチや web サイトタグベースのオーディエンスよりも明確なメリットがあります。

必要なユーザー ID を作成するには、web サイトでAdobe AdvertisingのJavaScript タグ <!-- with a user ID parameter --> を使用する必要があります。 詳しくは、Adobeアカウントチームにお問い合わせください。

![ セグメント作成プロセス ](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、[!DNL Google Ads] のキャンペーンで [ キャンペーンレベルまたは広告グループレベルのターゲットまたは除外 ](#audience-manager-targets) として使用できます。

### Audience Managerおよびその他の [!DNL Adobe] セグメントを使用した広告のターゲティングまたは除外 {#audience-manager-targets}

* （[!DNL Search, Social, & Commerce] を使用したオプトインの広告主）キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [ [!DNL Adobe]  セグメントを使用して作成 ](#audience-manager-google-audiences) された任意の [!DNL Google Ads] オーディエンスを、[!DNL Google Ads] キャンペーンで使用できます。

* （DSPを使用する広告主）既存の [!DNL Adobe] セグメントを広告プレースメントのターゲットとして使用できます。 オプションで、再利用可能なオーディエンスにセグメントを含めることができ、複数のプレースメントのターゲットまたは除外として使用できます。

* （Advertising Creativeを持つ広告主）既存の [!DNL Adobe] セグメントを、広告体験における特定のクリエイティブのターゲットとして使用できます。

>[!NOTE]
>
>Audience ManagerおよびExperience Cloud[!DNL Audience Library] ーザーインターフェイスでのオーディエンスの作成方法、および様々なオーディエンスタイプの一般的なユースケースについて詳しくは、「[ オーディエンス作成オプション ](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)」を参照してください。

## DSP Media の漏洩データをAudience Managerに送信

*DSPのみを使用する広告主*

Adobe Audience Managerを使用するDSPのお客様は、Audience Managerへのピクセル呼び出しを使用して、広告キャンペーンからデータをキャプチャできます。 その後、キャンペーンデータを使用して、ルールベースの特性を作成し、新しいセグメントを定義して、より高度なセグメント化、頻度管理、マーケティング分析、レポートインサイトなど、様々なDSPのユースケースを可能にすることができます。

詳しくは、[Adobe Audience ManagerへのDSP Media 公開データの送信の概要」を参照 ](/help/integrations/audience-manager/media-data-integration/overview.md) てください。

## Audience Analyticsを使用したサイトアクティビティに関する豊富なインサイトの取得

[[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) を使用しているAdobe Advertisingのお客様は、Adobe Advertisingが追跡したデータとAudience Managerセグメントの両方を [!DNL Analytics] に送信して、サイトアクティビティに関する有益なインサイトを得ることができます。

詳しくは、「Adobe Advertisingのお客様向け [[!DNL Adobe Audience Analytics]  を参照してくだ ](/help/integrations/audience-manager/audience-analytics.md) い。
