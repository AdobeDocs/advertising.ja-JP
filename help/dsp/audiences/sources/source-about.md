---
title: 1st パーティオーディエンスソースについて
description: クッキーレスターゲティングのために、ファーストパーティセグメント内の他のユーザーIDをユニバーサル IDに変換する方法について説明します。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 2dddf3560e1f98dab7158c28625bcd54b4efbdb2
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# 1st パーティオーディエンスソースについて

*Beta機能*

DSPは、CDP内に構築されたハッシュ化された電子メール ID、Cookie、モバイル広告ID （MAID）で構成されるファーストパーティセグメントを取り込み、ユニバーサル IDで構成されるセグメントに変換できます。 結果の各IDは個人ベースで、広告頻度の上限はID レベル <!-- Move that info. to somewhere else? -->で適用されます。

セグメントの詳細には、各ユニバーサル ID タイプのサイズと、Cookieまたはデバイス IDによって追跡される各デバイスタイプのサイズが含まれます。

## ユニバーサル ID タイプ {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

次のユニバーサル ID パートナーの認証（決定論的） IDを使用して、ファーストパーティセグメントをセグメントに変換できます。

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * フォームフィールドを使用できます。

     [!DNL RampIDs]は、北米、オーストラリア、ニュージーランドのユーザーが利用できます。

     料金は、配信されたディスプレイ広告インプレッションあたり0.15 USD、配信されたビデオ広告インプレッションあたり0.25 USDです。

   * [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を使用した測定の場合。

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * フォームフィールドを使用できます。

     [!DNL UID2 IDs]は、欧州経済領域およびその他の一部の国では利用できません。 [禁止国の一覧](/help/policies/universal-id-policy.md#prohibited-countries-uid2)を参照してください。

     料金は、配信されたディスプレイ広告インプレッションあたり0.15 USD、配信されたビデオ広告インプレッションあたり0.25 USDです。

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## ファーストパーティセグメントでサポートされる顧客データプラットフォーム

DSPでは、ファーストパーティセグメントを迅速に取り込むために、次のCDPへのコネクタを確立しています。

DSPは、バッチ、ストリーミング、API ベースのデータ共有機能を利用して、他のCDPと接続することもできます。 新しいCDPとの連携については、Adobeアカウントチームにお問い合わせください。

### [!DNL Adobe Real-Time CDP]

DSPは、Adobe Experience Platformの一部である&#x200B;*the*[の統合 [!DNL Adobe Real-Time CDP]destination](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=ja)です。

[!DNL Real-Time CDP]では、宛先は、シームレスなデータのアクティベーションを可能にする外部データプラットフォームへの接続です。 宛先を使用して、DSPのターゲット広告に対して、ハッシュ化されたメールアドレス、Cookie、モバイル広告IDをアクティブ化できます。 宛先について詳しくは、Experience Platform [宛先ガイド &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html?lang=ja)を参照してください。これには、製品の概要、[宛先ワークスペースの作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html?lang=ja)および[宛先の接続の作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=ja)、[宛先へのデータのアクティブ化](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html?lang=ja)に関する説明が含まれます。

DSPで[!DNL Adobe] [!DNL Real-time CDP]のファーストパーティセグメントを取り込み、ハッシュ化された電子メールアドレス、Cookie、モバイル広告IDをユニバーサル IDに変換できるようにするには、「[&#x200B; ユーザーIDを [!DNL Adobe Real-Time CDP] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-adobe-rtcdp.md)」を参照してください。

### [!DNL ActionIQ]

組織のファーストパーティデータを[!DNL ActionIQ]のCustomer Data PlatformからDSPと共有して、DSPでターゲット広告のためにハッシュ化されたメールアドレスをユニバーサル IDに変換できます。 この統合にはカスタマイズが必要です。 詳しくは、Adobe アカウントチームにお問い合わせください。

### [!DNL Amperity]

組織のファーストパーティデータを[!DNL Amperity]のCustomer Data PlatformからDSPと共有して、DSPでターゲット広告のためにハッシュ化されたメールアドレスをユニバーサル IDに変換できます。 詳しくは、「[&#x200B; ユーザーIDを [!DNL Amperity] からユニバーサル ID](/help/dsp/audiences/sources/source-amperity.md)に変換する」を参照してください。

### [!DNL Optimizely]

組織のファーストパーティデータを[!DNL Optimizely]のCustomer Data PlatformからDSPと共有して、DSPでターゲット広告のためにハッシュ化されたメールアドレスをユニバーサル IDに変換できます。 詳しくは、「[&#x200B; ユーザーIDを [!DNL Optimizely] からユニバーサル ID](/help/dsp/audiences/sources/source-optimizely.md)に変換する」を参照してください。

### [!DNL Tealium]

[!DNL Tealium]を使用して、組織の1st パーティデータを[!DNL Amazon Web Services]顧客データプラットフォームから共有できます。 DSPでのターゲット広告のためにハッシュ化された電子メールアドレスをユニバーサル IDに変換する方法について詳しくは、「[&#x200B; ユーザーIDを [!DNL Tealium] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-tealium.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [&#x200B; ユーザーIDを [!DNL Adobe Real-Time CDP] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [&#x200B; ユーザーIDを [!DNL Amperity] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-amperity.md)
>* [&#x200B; ユーザーIDを [!DNL Optimizely] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-optimizely.md)
>* [&#x200B; ユーザーIDを [!DNL Tealium] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-tealium.md)
>* [&#x200B; オーディエンス管理について](/help/dsp/audiences/audience-about.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
