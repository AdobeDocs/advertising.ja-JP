---
title: オーディエンスソースを作成してファーストパーティオーディエンスをアクティベート
description: ソースを作成して、オーディエンスをアカウントまたは広告主アカウントにインポートする方法を説明します。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# オーディエンスソースを作成してファーストパーティオーディエンスをアクティベート

<!-- Will this remain for admin users/Adobe Account Team users only? -->

DSPでソースを作成して、ファーストパーティオーディエンスをDSP アカウントまたは広告主アカウントに読み込みます。

特定の顧客データプラットフォームからセグメントを取り込むために必要な、その他の手順については、以下を参照してください [オーディエンス固有のアクティベーションワークフロー](source-about.md)

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. クリック **[!UICONTROL Add Source]**.

1. が含まれる [!UICONTROL Select a Type] メニューで、ソースタイプを選択します。

   * *[!UICONTROL RT-CDP]*: [この [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*：です [[!DNL Tealium] 顧客データプラットフォーム](source-about.md).

1. を指定 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* または *[!UICONTROL Account]*.

1. 残りを入力 [ソース設定](source-settings.md).

   のコピーを保持 [!UICONTROL Source Key] が生成されます。 値は後で必要になります。

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
>顧客データプラットフォームのソースを作成したら、追加の手順を完了する必要があります。 を参照してください。 [のアクティベーションワークフロー [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> および [のアクティベーションワークフロー [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [オーディエンスソース設定](source-settings.md)
>* [オーディエンスソースからの認証済みセグメントのアクティブ化について](source-about.md)
>* [ユニバーサル ID パートナーからの認証済みセグメントの有効化](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
