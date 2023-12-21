---
title: DSP統合を次と共に使用するためのワークフロー [!DNL Adobe] [!DNL Real-time CDP]"
description: 「DSPが [!DNL Adobe] [!DNL Real-time CDP] ファーストパーティセグメント」と呼ばれます。
feature: DSP Audiences
source-git-commit: fb42e4aacaf0ea22890e0b4a46719725c99fffdc
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# とのDSP統合を使用する際のワークフロー [!DNL Adobe Real-Time CDP]

1. [DSPによる顧客データセグメントの変換を許可 [!DNL LiveRamp RampIDs]](source-universal-id.md) 入札可能な環境で認識可能な<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [オーディエンスソースの作成](source-create.md) オーディエンスをDSPアカウントまたは広告主アカウントにインポートする場合。

1. Experience Platformで、 [!UICONTROL Source Key] DSPのソース設定で生成された

   DSPの宛先接続をアクティブ化し、セグメントを選択し、制御権限にアクセスする手順については、「[Adobe Advertising Cloud DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

その他のサポートについては、Adobeアカウントチームにお問い合わせください。 `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [ユニバーサル ID パートナーからの認証済みセグメントのアクティブ化](source-universal-id.md)
>* [オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する](source-create.md)
>* [Audience Source 設定](source-settings.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [宛先カタログの概要](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [とのDSP統合を使用する際のワークフロー [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
