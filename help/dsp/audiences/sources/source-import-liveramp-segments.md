---
title: 認証済みセグメントの手動インポート： [!DNL LiveRamp]
description: を使用した、認証済みオーディエンスのアクティブ化について説明します [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 認証済みセグメントの手動インポート： [!DNL LiveRamp]

*ベータ版機能*

認証済みを手動で送信できます [!DNL LiveRamp] を使用したDSPへのセグメント [!DNL LiveRamp] [!DNL Connect] ダッシュボード。 読み込んだセグメントをプレースメントのターゲティングに使用できます。 ファーストパーティセグメントの場合、料金は配信されたディスプレイ広告インプレッションあたり 0.15 ドル、ビデオ広告インプレッションあたり 0.25 ドルです。

各インポートジョブのセグメントマッピングとアップロードには、最大 7 日間かかる場合があります。

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. で次の手順を実行します [!DNL Connect] ダッシュボード：

   1. 宛先タイルのアクティブ化 **[!DNL AAC API 1P Onboarding]**.

   1. を設定 [!DNL Identifier Settings] 対象： **[!DNL Ramp ID]** のみ。

      ![識別子の設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （オプション） cookie ベースの識別子を引き続き受け取る場合は、2 つ目のを作成します [!DNL AAC API 1P Onboarding] 宛先タイル （「」付き）[!DNL Cookies],&quot; &quot;[!DNL IDFA]、」および「[!DNL AAID]が選択されました。

   1. オーディエンスライブラリでの検証（オーディエンスの作成または編集時に使用できます） [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択して、セグメント数全体が読み込まれました。

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
