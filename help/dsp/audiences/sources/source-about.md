---
title: ファーストパーティオーディエンスソースについて
description: ファーストパーティセグメントの他のユーザー識別子をユニバーサル ID に変換して、クッキーなしのターゲティングを実現する方法を説明します。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: bd0586516c2457e4dfcd1a23046707e8bf652e3b
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# ファーストパーティオーディエンスソースについて

*ベータ版機能*

DSPは、Customer Data Platform （CDP）内で作成されたハッシュ化されたメール ID で構成されるファーストパーティセグメントを取り込み、ユニバーサル ID で構成されるセグメントに変換できます。 結果の各 ID は人物ベースであり、広告のフリークエンシーキャップは ID レベルで適用されます<!-- Move that info. to somewhere else? -->.

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

   * を使用した測定 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * ログインしたユーザーをリターゲティングする場合。

     [!DNL UID2 IDs] は、欧州経済地域および一部の国のユーザーは使用できません。 を参照してください。 [禁止国のリスト](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

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

## ファーストパーティセグメント用にサポートされる顧客データプラットフォーム

DSPは、ファーストパーティセグメントをすばやく取り込むために、次の CDP へのコネクタを確立しています。

DSPは、バッチ、ストリーミング、または API ベースのデータ共有を使用して、追加の CDP にも接続できます。 新しい CDP と統合する場合は、Adobeアカウントチームにお問い合わせください。

### [!DNL Adobe Real-Time Customer Data Platform]

DSPはの統合 *宛先* （用） [この [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)（Adobe Experience Platformの一部）

対象： [!DNL Real-Time CDP]の宛先は、シームレスなデータのアクティベーションを可能にする外部データプラットフォームへの接続です。 宛先を使用して、DSPでのターゲット広告用にハッシュ化されたメールアドレスをアクティブ化できます。 宛先について詳しくは、Experience Platformを参照してください [宛先ガイド](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)製品の概要、説明を含む [宛先ワークスペースの作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) および [宛先接続の作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、および [宛先へのデータのアクティブ化](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

DSPでのデータの取り込みを有効にするには [!DNL Adobe] [!DNL Real-time CDP] ファーストパーティセグメントを変換し、ハッシュ化されたメールアドレスをユニバーサル ID に変換します。詳しくは、「[からのユーザー ID の変換 [!DNL Adobe Real-Time CDP] ユニバーサル ID に](/help/dsp/audiences/sources/source-adobe-rtcdp.md).」と入力します。

### [!DNL ActionIQ]

から組織のファーストパーティデータを共有できます [!DNL Action IQ] DSPを使用した customer data platform：ハッシュ化されたメールアドレスをユニバーサル ID に変換して、DSPでのターゲット広告を実現します。 この統合にはカスタマイズが必要です。 詳しくは、Adobeアカウントチームにお問い合わせください。

### [!DNL Tealium]

から組織のファーストパーティデータを共有できます [!DNL Tealium] を使用した顧客データプラットフォーム [!DNL Amazon Web Services]. DSPでのターゲット広告用にハッシュ化されたメールアドレスをユニバーサル ID に変換する方法について詳しくは、「」を参照してください[からのユーザー ID の変換 [!DNL Tealium] ユニバーサル ID に](/help/dsp/audiences/sources/source-tealium.md).」と入力します。

>[!MORELIKETHIS]
>
>* [からのユーザー ID の変換 [!DNL Adobe Real-Time CDP] ユニバーサル ID に](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [からのユーザー ID の変換 [!DNL Tealium] ユニバーサル ID に](/help/dsp/audiences/sources/source-tealium.md)
>* [オーディエンスソースを作成してユニバーサル ID オーディエンスを有効化](source-create.md)
>* [オーディエンスソース設定](source-settings.md)
>* [ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
