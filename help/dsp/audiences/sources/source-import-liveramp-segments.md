---
title: ' [!DNL LiveRamp]から認証済みセグメントを手動でインポートします'
description: ' [!DNL LiveRamp]を通じて認証済みオーディエンスをアクティブ化する方法について説明します。'
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 0%

---

# [!DNL LiveRamp]から認証済みセグメントを手動でインポートします

*Beta機能*

[!DNL LiveRamp] [!DNL LiveRamp] ダッシュボードを使用して、認証済み[!DNL Connect] セグメントをDSPに手動で送信できます。 読み込んだセグメントをプレースメントのターゲティングに使用できます。 1st パーティセグメントの場合、配信されたディスプレイ広告インプレッションあたり0.15米ドル、配信されたビデオ広告インプレッションあたり0.25米ドルの料金が発生します。

各インポートジョブのセグメントマッピングとアップロードには、最大7日かかる場合があります。

<!--
Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. [!DNL Connect] ダッシュボードで次の手順を実行します。

   1. 宛先タイル **[!DNL AAC API 1P Onboarding]**&#x200B;をアクティブ化します。

   1. [!DNL Identifier Settings]を&#x200B;**[!DNL Ramp ID]**&#x200B;のみに設定します。

      ![識別子の設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （オプション） Cookie ベースのIDを引き続き受け取る場合は、「[!DNL AAC API 1P Onboarding]」、「[!DNL Cookies]」、「[!DNL IDFA]」が選択された2番目の[!DNL AAID]宛先タイルを作成します。

   1. オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用可能）で、セグメント数全体が読み込まれたことを確認します。

>[!MORELIKETHIS]
>
>* [&#x200B; ファーストパーティのオーディエンスソースについて](source-about.md)
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=ja)
>* [&#x200B; オーディエンス管理について](/help/dsp/audiences/audience-about.md)
