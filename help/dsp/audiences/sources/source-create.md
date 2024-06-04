---
title: オーディエンスソースを作成してユニバーサル ID オーディエンスを有効化
description: ソースを作成して、オーディエンスを顧客データプラットフォームから読み込み、ユニバーサル ID を含むセグメントに変換する方法を説明します。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# オーディエンスソースを作成してユニバーサル ID オーディエンスを有効化

*ベータ版機能*

DSPで、顧客データプラットフォーム内のファーストパーティオーディエンスごとに、指定したユニバーサル ID タイプを含むセグメントに変換するソースを作成します。 セグメントは、組織のDSP アカウントまたは広告主アカウントに読み込むことができます。 データ料金は、選択したユニバーサル ID タイプに基づいて適用されます。

各顧客データプラットフォームからオーディエンスを取り込むには、追加の手順が必要です。 手順の最後のメモを参照してください。

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. クリック **[!UICONTROL Add Source]**.

1. が含まれる [!UICONTROL Select a Type] メニューで、顧客データプラットフォームを選択します。

   * *[!UICONTROL RT-CDP]*: [この [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*：です [[!DNL ActionIQ] 顧客データプラットフォーム](source-about.md).

   * *[!UICONTROL Tealium CDP]*: （設定されたユーザーのみ）次の [[!DNL Tealium] 顧客データプラットフォーム](source-about.md).

1. を指定 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* または *[!UICONTROL Account]*.

1. 残りを入力 [ソース設定](source-settings.md).

   のコピーを保持 [!UICONTROL Source Key] が生成されます。 値は後で必要になります。

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
>顧客データプラットフォームのソースを作成したら、追加の手順を完了する必要があります。 を参照してください。 [オーディエンスをから読み込むワークフロー [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> および [オーディエンスをから読み込むワークフロー [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [オーディエンスソース設定](source-settings.md)
>* [ファーストパーティオーディエンスソースについて](source-about.md)
>* [Adobe Advertising Cloud DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
