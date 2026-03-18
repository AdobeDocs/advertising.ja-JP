---
title: Adobe AdvertisingとAdobe Analyticsの統合
description: Adobe AdvertisingでAdobe Analyticsとデータを交換する方法と、検索、ソーシャル、Commerce内でのデータの使用方法について説明します。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Adobe AdvertisingとAdobe Analyticsの統合

次の方法で、Adobe Advertisingと Analytics を統合できます。

## [!DNL Analytics] とAdobe Advertising間でのデータの交換

### データ [!DNL Analytics]Adobe Advertisingに取り込む

[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] とDSPを使用して、以下を取り込みます。

* **[!DNL Analytics]セグメント：** で作成され、Experience Cloudに公開されたすべての広告主または代理店のセグメントのメタデータ、階層データ、一意のオーディエンスデータを [!DNL Analytics] します。

* **[!DNL Analytics]サイトエンゲージメント指標**

* 標準指標、カスタム指標および予約済み指標に **[!DNL Analytics]いて**

### [!DNL Analytics] へのAdobe Advertising データの送信

* **Adobe Advertisingのトラフィック指標**

* **Adobe Advertisingの寸法**

>[!NOTE]
>
>[!DNL Search, Social, & Commerce]：この機能は、ほとんどの広告ネットワークとキャンペーンタイプでサポートされています。 詳しくは、[!DNL Search, Social, & Commerce] ガイドの「サポート対象インベントリ」を参照してください。<!-- add link when that's published in ExL -->

### [!DNL Analytics] セグメントを使用したオーディエンス [!DNL Google Ads] 作成 {#audience-manager-google-audiences}

*オプトイン済みの [!DNL Advertising Search, Social, & Commerce] のみを使用する広告主*

<!-- Verify all -->

[!DNL Search, Social, & Commerce] 内では、既存の [!DNL Google Ads] セグメント [!DNL Analytics] 使用して、ユーザー ID からGoogle カスタマーマッチオーディエンスを作成できます。 これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントと、Adobe Experience Cloud [!DNL Audience Library] を使用して作成されるセグメントが含まれます。 詳しくは、「[&#x200B; オーディエンスから  [!DNL Google Ads]  オーディエンスに一致する顧客の作成  [!DNL Adobe]  オーディエンス &#x200B;](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)」を参照してください。

[&#x200B; ユーザー ID からのカスタマーマッチオーディエンス &#x200B;](https://support.google.com/google-ads/answer/9199250) は web サイトタグベースのオーディエンスと同様に機能しますが、非 PII ID は一意のオーディエンスメンバーに割り当てられるので、標準のカスタマーマッチや web サイトタグベースのオーディエンスよりも明確なメリットがあります。

必要なユーザー ID を作成するには、web サイトでAdobe Advertising JavaScript タグを使用する必要があります <!-- with a user ID parameter --> 詳しくは、Adobe アカウントチームにお問い合わせください。

![&#x200B; セグメント作成プロセス &#x200B;](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、[!DNL Google Ads] のキャンペーンで [&#x200B; キャンペーンレベルまたは広告グループレベルのターゲットまたは除外 &#x200B;](#audience-manager-targets) として使用できます。

### [!DNL Analytics] セグメントを使用した広告のターゲット設定または除外 {#analytics-targets}

* （[!DNL Search, Social, & Commerce] を使用したオプトインの広告主）キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [!DNL Google Ads][&#x200B; セグメントを使用して作成  [!DNL Analytics]  された任意の &#x200B;](#audience-manager-google-audiences) オーディエンスを、[!DNL Google Ads] キャンペーンで使用できます。

* （DSPを使用する広告主）既存の [!DNL Analytics] セグメントを広告プレースメントのターゲットとして使用できます。 オプションで、再利用可能なオーディエンスにセグメントを含めることができ、複数のプレースメントのターゲットまたは除外として使用できます。

* （Advertising Creativeを使用する広告主）既存の [!DNL Analytics] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用できます。
