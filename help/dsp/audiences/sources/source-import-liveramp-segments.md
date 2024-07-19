---
title: 認証済みセグメントの手動インポート  [!DNL LiveRamp]
description: ' [!DNL LiveRamp] を使用した認証済みオーディエンスのアクティブ化について説明します。'
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 認証済みセグメントの [!DNL LiveRamp] からの手動インポート

*Beta機能*

[!DNL LiveRamp] [!DNL Connect] ダッシュボードを使用すると、認証済み [!DNL LiveRamp] セグメントを手動でDSPに送信できます。 読み込んだセグメントをプレースメントのターゲティングに使用できます。 ファーストパーティセグメントの場合、料金は配信されたディスプレイ広告インプレッションあたり 0.15 ドル、ビデオ広告インプレッションあたり 0.25 ドルです。

各インポートジョブのセグメントマッピングとアップロードには、最大 7 日間かかる場合があります。

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. [!DNL Connect] ダッシュボードで次の手順を実行します。

   1. 宛先タイル **[!DNL AAC API 1P Onboarding]** をアクティブ化します。

   1. [!DNL Identifier Settings] を **[!DNL Ramp ID]** のみに設定します。

      ![ 識別子の設定 ](/help/dsp/assets/liveramp-tile-settings.png)

   1. （任意） cookie ベースの識別子を引き続き受け取る場合は、「[!DNL Cookies]」、「[!DNL IDFA]」、「[!DNL AAID]」を選択して、2 つ目の [!DNL AAC API 1P Onboarding] 宛先タイルを作成します。

   1. オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する場合に使用できます）で、セグメント数全体が読み込まれていることを確認します。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](source-manage.md)
>* [Adobe Advertising DSP接続 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
