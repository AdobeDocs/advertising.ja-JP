---
title: ファーストパーティオーディエンスソースについて
description: ファーストパーティセグメントの他のユーザー識別子をユニバーサル ID に変換して、クッキーなしのターゲティングを実現する方法を説明します。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 62d27f4af9705194f4254ffcb3145719dfd5af2f
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# ファーストパーティオーディエンスソースについて

*Beta機能*

DSPは、顧客データプラットフォーム（CDP）内で作成されたハッシュ化されたメール ID で構成されるファーストパーティセグメントを取り込み、ユニバーサル ID で構成されるセグメントに変換できます。 結果として得られる各 ID は人物ベースであり、広告のフリークエンシーキャップは ID レベル <!-- Move that info. to somewhere else? --> で適用されます。

セグメントの詳細には、各ユニバーサル ID タイプのサイズと、Cookie またはデバイス ID によって追跡される各デバイスタイプのサイズが含まれます。

## ユニバーサル ID タイプ {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

次のユニバーサル ID パートナーの認証済み（決定論的） ID を使用して、ファーストパーティセグメントをセグメントに翻訳できます。

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * ログインしたユーザーをリターゲティングする場合。

     [!DNL RampIDs] は、北米、オーストラリア、ニュージーランドのユーザーが利用できます。

     料金は、配信されたディスプレイ広告インプレッションあたり 0.15 ドル、配信されたビデオ広告インプレッションあたり 0.25 ドルです。

   * [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用した測定に。

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * ログインしたユーザーをリターゲティングする場合。

     [!DNL UID2 IDs] は、欧州経済地域および一部の国のユーザーは利用できません。 [&#x200B; 禁止国のリスト &#x200B;](/help/policies/universal-id-policy.md#prohibited-countries-uid2) をご覧ください。

     料金は、配信されたディスプレイ広告インプレッションあたり 0.15 ドル、配信されたビデオ広告インプレッションあたり 0.25 ドルです。

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## ファーストパーティセグメントでサポートされる顧客データプラットフォーム

DSPは、ファーストパーティセグメントをすばやく取り込むために、次の CDP へのコネクタを確立しています。

DSPは、バッチ、ストリーミング、API ベースのデータ共有を使用して、追加の CDP にも接続できます。 新しい CDP と統合するには、Adobe アカウントチームにお問い合わせください。

### [!DNL Adobe Real-Time CDP]

DSPは、Adobe Experience Platformの一部である *the*[&#x200B; の統合  [!DNL Adobe Real-Time CDP] 宛先 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=ja) です。

ま [!DNL Real-Time CDP]、宛先は、シームレスなデータのアクティベーションを可能にする外部データプラットフォームへの接続です。 宛先を使用して、DSPでのターゲット広告用にハッシュ化されたメールアドレスをアクティブ化できます。 宛先について詳しくは、Experience Platform[&#x200B; 宛先ガイド &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html?lang=ja) を参照してください。これには、製品の概要、[&#x200B; 宛先ワークスペースの作成 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html?lang=ja) および [&#x200B; 宛先接続の作成 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=ja) の手順、[&#x200B; 宛先へのデータのアクティブ化 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html?lang=ja) が含まれます。

DSPが [!DNL Adobe] ーザーをファーストパーティセグメント [!DNL Real-time CDP] 取り込み、ハッシュ化されたメールアドレスをユニバーサル ID に変換できるようにするには、「[&#x200B; ユーザー ID を  [!DNL Adobe Real-Time CDP]  ユニバーサル ID から変換 &#x200B;](/help/dsp/audiences/sources/source-adobe-rtcdp.md) を参照してください。

### [!DNL ActionIQ]

組織のファーストパーティデータを [!DNL ActionIQ] カスタマーデータプラットフォームからDSPと共有して、ハッシュ化されたメールアドレスをユニバーサル ID に変換し、DSPでターゲット広告を行うことができます。 この統合にはカスタマイズが必要です。 詳しくは、Adobe アカウントチームにお問い合わせください。

### [!DNL Amperity]

組織のファーストパーティデータを [!DNL Amperity] カスタマーデータプラットフォームからDSPと共有して、ハッシュ化されたメールアドレスをユニバーサル ID に変換し、DSPでターゲット広告を行うことができます。 詳しくは、[&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Amperity]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-amperity.md) を参照してください。

### [!DNL Optimizely]

組織のファーストパーティデータを [!DNL Optimizely] カスタマーデータプラットフォームからDSPと共有して、ハッシュ化されたメールアドレスをユニバーサル ID に変換し、DSPでターゲット広告を行うことができます。 詳しくは、[&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Optimizely]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-optimizely.md) を参照してください。

### [!DNL Tealium]

[!DNL Tealium] を使用して、組織のファーストパーティデータを [!DNL Amazon Web Services] 顧客データプラットフォームから共有できます。 DSPでのターゲット広告用にハッシュ化されたメールアドレスをユニバーサル ID に変換する方法について詳しくは、「[&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Tealium]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-tealium.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 &#x200B;](source-manage.md)
>* [&#x200B; ユニバーサル ID のアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Adobe Real-Time CDP]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Amperity]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-amperity.md)
>* [&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Optimizely]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-optimizely.md)
>* [&#x200B; ユーザー ID をユニバーサル ID から  [!DNL Tealium]  ユニバーサル ID に変換 &#x200B;](/help/dsp/audiences/sources/source-tealium.md)
>* [Audience Management について &#x200B;](/help/dsp/audiences/audience-about.md)
>* [&#x200B; プレースメント設定 &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
