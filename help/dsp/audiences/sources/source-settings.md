---
title: Audience Source 設定
description: オーディエンスソースの設定について説明します。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Audience Source 設定

**[!UICONTROL Data Visibility Level]:** アカウントにアクセスできる単一の広告主がセグメントを利用できるかどうか (*[!UICONTROL Advertiser]*) またはアカウントへのアクセス権を持つすべての広告主 *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** （広告主レベルの表示のみ）セグメントを利用できる広告主。 アカウントにアクセスできる広告主のリストから 1 つを選択します。

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] （ソースのみ）のAdobe Experience Cloud組織 ID [!DNL Adobe Experience Platform] アカウント。

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] および [!DNL Tealium] ソースのみ ) 個人を特定できる情報 (PII) を変換する ID タイプです。 データ料金は適宜適用されます。

* *[!DNL RampID]:* PII を RampID に変換するには： 次を選択した場合： *[!DNL RampID]*&#x200B;の場合、セグメントは [!DNL RampIDs] 自動的に。

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] ソースのみ )PII を [統合 ID 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** （読み取り専用。自動的に生成）オーディエンスを Advertising DSPにプッシュするために、顧客データプラットフォームで宛先接続の作成に使用できるソースキー。 値をクリップボードにコピーして、宛先接続設定に貼り付けたり、ファイルに貼り付けたりできます。

>[!MORELIKETHIS]
>
>* [オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する](source-create.md)
>* [オーディエンスソースからの認証済みセグメントのアクティブ化について](source-about.md)
>* [ユニバーサル ID パートナーからの認証済みセグメントのアクティブ化](source-universal-id.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
