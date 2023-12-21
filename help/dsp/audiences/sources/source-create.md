---
title: オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する
description: オーディエンスをアカウントまたは広告主アカウントにインポートするソースを作成する方法を説明します。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する

<!-- Will this remain for admin users/Adobe Account Team users only? -->

DSPでソースを作成して、ファーストパーティのオーディエンスをDSPアカウントまたは広告主アカウントにインポートします。

特定の顧客データプラットフォームからセグメントを取り込むために必要な追加の手順については、 [オーディエンス固有のアクティベーションワークフロー](source-about.md)

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. クリック **[!UICONTROL Add Source]**.

1. Adobe Analytics の [!UICONTROL Select a Type] メニューで、ソースタイプを選択します。

   * *[!UICONTROL RT-CDP]*: [The [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: [[!DNL Tealium] 顧客データプラットフォーム](source-about.md).

1. 次を指定します。 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* または *[!UICONTROL Account]*.

1. 残りの [ソース設定](source-settings.md).

   のコピーを保持 [!UICONTROL Source Key] が生成されます。 値は後で必要になります。

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
>顧客データプラットフォーム用のソースを作成したら、追加の手順を完了する必要があります。 詳しくは、 [有効化ワークフロー [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> そして [有効化ワークフロー [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Audience Source 設定](source-settings.md)
>* [オーディエンスソースからの認証済みセグメントのアクティブ化について](source-about.md)
>* [ユニバーサル ID パートナーからの認証済みセグメントのアクティブ化](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
