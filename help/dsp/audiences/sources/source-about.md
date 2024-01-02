---
title: オーディエンスソースからの認証済みセグメントのアクティブ化について
description: 顧客データプラットフォームからファーストパーティセグメントを取り込む方法について説明します。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: f01cfbf22628cec0510f4a860ad927b333d5946a
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# オーディエンスソースからの認証済みセグメントのアクティブ化について

DSPは、顧客データプラットフォーム (CDP) 内で構築された、ハッシュ化された電子メール ID またはユニバーサル ID で構成されるファーストパーティセグメントを取り込むことができます。 取り込んだセグメントを配置のターゲットとして使用できます。

次の CDP はコネクタを確立しましたが、DSPは、バッチ、ストリーミング、API ベースのデータ共有を使用して、任意の CDP に接続することもできます。 新しい CDP と統合するには、担当のAdobeアカウントチームにお問い合わせください。

## [!DNL Adobe Real-Time Customer Data Platform]

DSPが [の [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)(Adobe Experience Platformの一部 )

In [!DNL Real-Time CDP], *宛先* は、シームレスなデータアクティベーションを可能にする、外部データプラットフォームへの接続です。 例えば、宛先を使用して、DSPでサポートされる複数のデジタル形式にわたるターゲット化した広告に関する既知の顧客関係（ハッシュ化された電子メールアドレスなど）をアクティブ化できます。 宛先について詳しくは、「Experience Platform [宛先ガイド](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)（製品の概要、手順を含む） [宛先ワークスペースの作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) および [宛先接続の作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、および [宛先へのデータのアクティブ化](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

詳しくは、[とのDSP統合を使用する際のワークフロー [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

## [!DNL ActionIQ]

組織のファーストパーティデータを [!DNL Action IQ] DSPを使用した顧客データプラットフォーム その後、次のコードを使用して、DSPの配置をセグメントにターゲット設定できます。 [!DNL RampIDs] または [!DNL Unified IDs 2.0].

この統合には、カスタマイズが必要です。 詳しくは、Adobeアカウントチームにお問い合わせください。

## [!DNL Tealium]

組織のファーストパーティデータを [!DNL Tealium] を使用した顧客データプラットフォーム [!DNL Amazon Web Services]. その後、次のコードを使用して、DSPの配置をセグメントにターゲット設定できます。 [!DNL RampIDs]. 詳しくは、[とのDSP統合を使用する際のワークフロー [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [とのDSP統合を使用する際のワークフロー [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [とのDSP統合を使用する際のワークフロー [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する](source-create.md)
>* [Audience Source 設定](source-settings.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
