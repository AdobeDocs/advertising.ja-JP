---
title: Adobe Analyticsのコンバージョントラッキング
description: Adobe AdvertisingのキャンペーンにAdobe Analytics コンバージョントラッキングを使用する方法を説明します。
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analyticsのコンバージョントラッキング

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

Adobe AdvertisingとAdobe Analyticsの統合を利用する広告主の場合、Advertising Cloudでは、広告のクリック数とインプレッション数を、で追跡されたサイトエンゲージメントおよびコンバージョン指標と結び付けることができます [!DNL Analytics] トークンでリダイレクトを使用する場合（`ef_id` パラメーター）を設定する必要があります [入札単位](/help/search-social-commerce/glossary.md#a-b). この [!DNL Analytics] データは、毎日のフィードファイルを介してAdvertising Cloudに自動送信されます。

参照先」[概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}」を参照してください。

>[!PREREQUISITES]
>
> 検索、ソーシャル、Commerce広告主アカウントのタイムゾーン [!DNL Analytics] レポートスイートと広告ネットワークアカウントが一致する必要があります。 一致しない場合、データの相違はシステム全体で発生します。

## 実装の概要

1. 対象： [!DNL Analytics]検索、ソーシャル、Commerce実装チームは、各レポートスイートに対して、次の設定を変更します。

   * の有効期限 `ef_id` [!DNL eVar] は、Adobe Advertising主の広告のクリックルックバックウィンドウに一致するように変更されます。

   * Adobe Advertisingユーザー ID。

   * 最適化に使用する標準イベントとカスタムイベント。

1. 検索、ソーシャル、Commerceで、実装チームに以下を割り当てます。

   1. 既存の広告ネットワークアカウント階層を検索、ソーシャルおよびCommerceに同期します。

   1. 「」を使用してリダイレクトを追加`ef_id`「トークンはトラッキング URL に渡され、広告ネットワークに投稿されます。

   この手順により、Adobe Advertisingトラッキングサーバーへのリダイレクトが追加されます（を除く） [!DNL Google Ads] および [!DNL Microsoft Advertising] 並列トラッキングをサポートするブラウザーの広告）を渡し、広告クリック時に、動的に入力された「ef_id」パラメーターを URL に追加します。 並列トラッキングが適用されると、エンドユーザーが広告から最終的な URL に直接送信され、トラッキングテンプレート URL （クリック測定を含む）がバックグラウンドで読み込まれます。

統合が完了すると、検索、ソーシャル、Commerceはで追跡されているすべてのオンページイベントデータを自動的に受け取ります [!DNL Analytics] 設定されたレポートスイート用。

>[!MORELIKETHIS]
>
>* [コンバージョントラッキングオプション](conversion-tracking-about.md)
