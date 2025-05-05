---
title: Adobe Analyticsのコンバージョントラッキング
description: Adobe AdvertisingのキャンペーンにAdobe Analytics コンバージョントラッキングを使用する方法を説明します。
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: a6dc9edb12484499069a68222a3007ae08d9dfea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analyticsのコンバージョントラッキング

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

Adobe AdvertisingとAdobe Analyticsの統合を利用する広告主の場合、Advertising Cloudは、[ 入札単位 ](/help/search-social-commerce/glossary.md#a-b) のクリックトラッキング URL でトークン（`ef_id` パラメーター）を使用してリダイレクトを使用する際に、[!DNL Analytics] が追跡するサイトエンゲージメントおよびコンバージョン指標に、広告のクリック数およびインプレッション数を結び付けることができます。 [!DNL Analytics] データは、毎日のフィードファイルを介してAdvertising Cloudに自動的に送信されます。

統合について詳しくは、「[ の概要  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/ja/docs/advertising/integrations/analytics/overview){target="_blank"}」を参照してください。

>[!PREREQUISITES]
>
> 検索、ソーシャル、Commerce広告主アカウントのタイムゾーン、[!DNL Analytics] レポートスイートおよび広告ネットワークアカウントは一致する必要があります。 一致しない場合、データの相違はシステム全体で発生します。

## 実装の概要

1. 検索、ソーシャル、Commerceの導入チームは、[!DNL Analytics] で各レポートスイートに対して次の設定を変更します。

   * `ef_id` [!DNL eVar] の有効期限は、広告主のAdobe Advertisingのクリックルックバックウィンドウに一致するように変更されます。

   * Adobe Advertisingユーザー ID。

   * 最適化に使用する標準イベントとカスタムイベント。

1. 検索、ソーシャル、Commerceで、実装チームに以下を割り当てます。

   1. 既存の広告ネットワークアカウント階層を検索、ソーシャルおよびCommerceに同期します。

   1. トラッキング URL に渡される「`ef_id`」トークンを使用してリダイレクトを追加し、広告ネットワークに投稿します。

   この手順により、Adobe Advertisingトラッキングサーバーへのリダイレクトが追加され（パラレルトラッキングをサポートするブラウザーの [!DNL Google Ads] および [!DNL Microsoft Advertising] 広告を除く）、広告クリック時に、動的に入力された「ef_id」パラメーターが URL に追加されます。 並列トラッキングが適用されると、エンドユーザーが広告から最終的な URL に直接送信され、トラッキングテンプレート URL （クリック測定を含む）がバックグラウンドで読み込まれます。

統合が完了すると、検索、ソーシャル、Commerceは、設定されたレポートスイートについて [!DNL Analytics] で追跡されたすべてのオンページイベントデータを自動的に受け取ります。

>[!MORELIKETHIS]
>
>* [ コンバージョントラッキングオプション ](conversion-tracking-about.md)
