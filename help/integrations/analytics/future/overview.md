---
title: Adobe AnalyticsとのAdobe Advertising統合
description: Adobe AdvertisingでAdobe Analyticsとデータを交換する方法と、検索、ソーシャル、Commerce内でのデータの使用方法について説明します。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe AnalyticsとのAdobe Advertising統合

Adobe Advertisingを Analytics と統合するには、次の方法があります。

## [!DNL Analytics] とAdobe Advertising間でのデータの交換

### データ [!DNL Analytics]Adobe Advertisingに取り込む

[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)、[!DNL Search, Social, & Commerce] およびDSPを使用した導入：

* **[!DNL Analytics]セグメント：[!DNL Analytics] で作成されExperience Cloudに公開されるすべての広告主またはエージェンシーのセグメントのメタデータ、階層データおよび一意のオーディエンスデータを** します。

* **[!DNL Analytics]サイトエンゲージメント指標**

* 標準指標、カスタム指標および予約済み指標に **[!DNL Analytics]いて**

### [!DNL Analytics] へのAdobe Advertisingデータの送信

* **Adobe Advertisingからのトラフィック指標**

* Adobe Advertisingからの **Dimension**

>[!NOTE]
>
>[!DNL Search, Social, & Commerce]：この機能は、ほとんどの広告ネットワークとキャンペーンタイプでサポートされています。 詳しくは、[!DNL Search, Social, & Commerce] ガイドの「サポート対象インベントリ」を参照してください。<!-- add link when that's published in ExL -->

### [!DNL Analytics] セグメントを使用した [!DNL Google Ads Audiences] の作成 {#audience-manager-google-audiences}

*オプトイン済みの [!DNL Advertising Search, Social, & Commerce] のみを使用する広告主*

<!-- Verify all -->

[!DNL Search, Social, & Commerce] 内では、既存の [!DNL Analytics] セグメント [!DNL Google Ads] 使用して、ユーザー ID からGoogle カスタマーマッチオーディエンスを作成できます。 これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントと、Adobe Experience Cloud [!DNL Audience Library] を使用して作成されるセグメントが含まれます。 詳しくは、「[&#x200B; オーディエンスから  [!DNL Google Ads]  オーディエンスに一致する顧客の作成  [!DNL Adobe]  オーディエンス &#x200B;](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)」を参照してください。

[&#x200B; ユーザー ID からのカスタマーマッチオーディエンス &#x200B;](https://support.google.com/google-ads/answer/9199250) は web サイトタグベースのオーディエンスと同様に機能しますが、非 PII ID は一意のオーディエンスメンバーに割り当てられるので、標準のカスタマーマッチや web サイトタグベースのオーディエンスよりも明確なメリットがあります。

必要なユーザー ID を作成するには、web サイトでAdobe AdvertisingのJavaScript タグ <!-- with a user ID parameter --> を使用する必要があります。 詳しくは、Adobeアカウントチームにお問い合わせください。

![&#x200B; セグメント作成プロセス &#x200B;](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、[!DNL Google Ads] のキャンペーンで [&#x200B; キャンペーンレベルまたは広告グループレベルのターゲットまたは除外 &#x200B;](#audience-manager-targets) として使用できます。

### [!DNL Analytics] セグメントを使用した広告のターゲティングまたは除外 {#analytics-targets}

* （[!DNL Search, Social, & Commerce] を使用したオプトインの広告主）キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [&#x200B; [!DNL Analytics]  セグメントを使用して作成 &#x200B;](#audience-manager-google-audiences) された任意の [!DNL Google Ads] オーディエンスを、[!DNL Google Ads] キャンペーンで使用できます。

* （DSPを使用する広告主）既存の [!DNL Analytics] セグメントを広告プレースメントのターゲットとして使用できます。 オプションで、再利用可能なオーディエンスにセグメントを含めることができ、複数のプレースメントのターゲットまたは除外として使用できます。

* （Advertising Creativeを持つ広告主）既存の [!DNL Analytics] セグメントを、広告体験における特定のクリエイティブのターゲットとして使用できます。
