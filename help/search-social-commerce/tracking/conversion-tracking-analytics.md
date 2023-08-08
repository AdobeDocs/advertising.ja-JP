---
title: Adobe Analyticsコンバージョントラッキング
description: Adobe AdvertisingでのキャンペーンにAdobe Analyticsコンバージョントラッキングを使用する方法について説明します。
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Adobe Analyticsコンバージョントラッキング

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

Adobe AdvertisingとAdobe Analyticsを統合した広告主の場合、Advertising Cloudは、 [!DNL Analytics] トークンでリダイレクトを使用する場合 (`ef_id` パラメーター ) を使用して、 [入札単位](/help/search-social-commerce/glossary.md#a-b). The [!DNL Analytics] データは、日別フィードファイル経由で自動的にAdvertising Cloudに送信されます。

参照：[の概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}」を参照してください。

>[!PREREQUISITES]
>
> Search、Social、および Commerce の広告主アカウントのタイムゾーン [!DNL Analytics] レポートスイートと広告ネットワークアカウントが一致する必要があります。 一致しない場合、データの相違はシステム間で存在します。

## 実装の概要

1. In [!DNL Analytics]を変更した場合、Search、Social および Commerce の実装チームは各レポートスイートに対して次の設定を変更します。

   * の有効期限 `ef_id` [!DNL eVar] は、Adobe Advertisingの広告主のクリックルックバックウィンドウに合わせて変更されました。

   * Adobe Advertisingユーザー ID。

   * 最適化に使用する標準イベントとカスタムイベント。

1. Search、Social および Commerce で、実装チームは以下をおこないます。

   1. 既存の広告ネットワークアカウントの階層を Search、Social、&amp; Commerce に同期します。

   1. リダイレクトを「`ef_id`」トークンがトラッキング URL に渡され、広告ネットワークに投稿されます。

   この手順により、Adobe Advertisingトラッキングサーバーへのリダイレクトが先に追加されます ( [!DNL Google Ads] および [!DNL Microsoft Advertising] 並列追跡をサポートするブラウザーの広告 ) を追加し、広告クリック時に動的に設定された「ef_id」パラメーターを URL に追加します。 並列追跡が適用される場合、エンドユーザーは広告から最終的な URL に直接送信され、（クリック測定を使用した）トラッキングテンプレート URL がバックグラウンドで読み込まれます。

統合が完了すると、Search、Social および Commerce は、 [!DNL Analytics] 設定されたレポートスイートの

>[!MORELIKETHIS]
>
>* [コンバージョントラッキングオプション](conversion-tracking-about.md)
