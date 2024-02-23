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

## Audience Managerとその他の同期 [!DNL Adobe] 広告ターゲティングのセグメント

[!DNL Search, Social, & Commerce] とDSPは、すべての広告主や代理店のAudience Managerやその他の情報用に、メタデータ、階層データ、一意のオーディエンスデータを取り込むことができます。 [!DNL Adobe] オーディエンス。 この一意の接続は、Adobe Advertisingを使用するマーケターのみが使用できます。 参照：[広告ターゲティング用のAdobe Audience Managerセグメントのインポート](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Managerとその他を使用 [!DNL Adobe] 作成するセグメント [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*次を使用してオプトインした広告主 [!DNL Advertising Search, Social, & Commerce] のみ*

Within [!DNL Search, Social, & Commerce]を使用する場合、 [!DNL Google Ads] 顧客が、 [!UICONTROL Adobe Media Optimizer (HTTP)] および [!UICONTROL Adobe Media Optimizer Batch Destination] を宛先として使用する場合。 ([!DNL Media Optimizer] は～の旧称である [!DNL Search, Social, & Commerce].) これには、Adobe Experience Cloudに公開されたAdobe Analyticsセグメントや、Adobe Experience Cloudを使用して作成されたセグメントが含まれます [!DNL Audience Library]. 詳しくは、[作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[ユーザー ID からの顧客一致オーディエンス](https://support.google.com/google-ads/answer/9199250) は web サイトのタグベースのオーディエンスと同様に機能しますが、一意のオーディエンスメンバーには、標準の顧客一致や web サイトのタグベースのオーディエンスよりも明確なメリットを得るために、PII 以外の ID が割り当てられます。

必要なユーザー ID を作成するには、 JavaScript タグを使用するAdobe Advertisingが必要です <!-- with a user ID parameter -->を Web サイト上でクリックします。 詳しくは、Adobeアカウントチームにお問い合わせください。

![セグメント作成プロセス](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、 [!DNL Google Ads] キャンペーンとして [キャンペーンレベルまたは広告グループレベルのターゲットまたは除外](#audience-manager-targets).

### Audience Managerとその他を使用 [!DNL Adobe] 広告のターゲットにする、または広告を除外するセグメント {#audience-manager-targets}

* ( 次を持つオプトイン広告主 [!DNL Search, Social, & Commerce]) 任意の [!DNL Google Ads] オーディエンス： [次を使用して作成 [!DNL Adobe] セグメント](#audience-manager-google-audiences) キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [!DNL Google Ads] キャンペーン。

* (DSPの広告主 ) 既存の [!DNL Adobe] セグメントを、広告プレースメントのターゲットとして使用します。 オプションで、セグメントを再利用可能なオーディエンスに含めることができます。このオーディエンスは、複数の配置のターゲットまたは除外として使用できます。

* (Advertising Creativeを持つ広告主 ) 既存の [!DNL Adobe] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用します。

>[!NOTE]
>
>Audience ManagerとExperience Cloudでオーディエンスを作成する方法の詳細 [!DNL Audience Library] 様々なオーディエンスタイプに対するインターフェイス、および一般的な使用例については、[オーディエンス作成オプション](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## DSP Media Exposure データをAudience Managerに送信

*DSPのみの広告主*

Adobe Audience Managerをご使用のDSPのお客様は、Audience Managerへのピクセル呼び出しを使用して広告キャンペーンからデータをキャプチャできます。 その後、キャンペーンデータを使用してルールベースの特性を作成し、新しいセグメントを定義して、より高度なセグメント化、頻度管理、マーケティング分析、レポートインサイトなど、様々なDSPのユースケースを有効にできます。

参照：[DSP Media Exposure データのAdobe Audience Managerへの送信の概要](/help/integrations/audience-manager/media-data-integration/overview.md)」を参照してください。

## Audience Analyticsでサイトのアクティビティに関する豊富なインサイトを得る

Adobe Advertisingのお客様： [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) は、Adobe Advertising追跡データセグメントとAudience Managerセグメントの両方を [!DNL Analytics] サイトアクティビティに関するインサイトを強化します。

詳しくは、[[!DNL Adobe Audience Analytics] (Adobe Advertisingのお客様向け )](/help/integrations/audience-manager/audience-analytics.md).&quot;
