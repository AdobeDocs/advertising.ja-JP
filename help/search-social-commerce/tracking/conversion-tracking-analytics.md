---
title: Adobe Analyticsのコンバージョン追跡
description: Adobe AdvertisingのAdobe Analyticsコンバージョントラッキングを使用して、キャンペーンの成果を向上させる方法を説明します。
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
TQID: 'https://experienceleague.adobe.com/CM0S4RvR4RJ5Ylta5EJTdZh-VDDHYIfa7Qsd1Dm4D78'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2206c6aa-b5c2-51b3-88e0-706d57048fe4
    internal-label: Search Tracking
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%
---
# Adobe Analyticsのコンバージョン追跡

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

Adobe AdvertisingとAdobe Analyticsの統合を持つ広告主の場合、[入札ユニット &#x200B;](/help/search-social-commerce/glossary.md#a-b)のクリックトラッキング URLでトークン （`ef_id` パラメーター）を使用すると、Advertising Cloudは、広告クリックとインプレッションを[!DNL Analytics]によって追跡されたサイトエンゲージメントとコンバージョン指標に結び付けることができます。 [!DNL Analytics] データは、毎日のフィード ファイルを介して自動的にAdvertising Cloudに送信されます。

統合について詳しくは、「[概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview){target="_blank"}」を参照してください。

>[!PREREQUISITES]
>
> Search, Social, &amp; Commerce広告主アカウント、[!DNL Analytics] レポートスイート、および広告ネットワークアカウントのタイムゾーンは一致する必要があります。 一致しない場合、システム全体でデータの相違が発生します。

## 導入の概要

1. [!DNL Analytics]では、Search, Social, &amp; Commerceの実装チームが、各レポートスイートに対して次の設定を変更します。

   * `ef_id` [!DNL eVar]の有効期限が、広告主のAdobe Advertisingのクリックルックバックウィンドウと一致するように変更されました。

   * Adobe Advertising ユーザーID。

   * 最適化に使用する標準イベントとカスタムイベント。

1. Search, Social, &amp; Commerceの導入チーム：

   1. 既存の広告ネットワークアカウントの階層をSearch、Social、およびCommerceに同期します。

   1. トラッキング URLに渡される&quot;`ef_id`&quot; トークンを持つリダイレクトを追加し、広告ネットワークに投稿します。

   この手順では、Adobe Advertising トラッキングサーバーへのリダイレクトを追加し（並列トラッキングをサポートするブラウザーの[!DNL Google Ads]広告と[!DNL Microsoft Advertising]広告を除く）、広告のクリック時に動的に入力された「ef_id」パラメーターをURLに追加します。 並行トラッキングが適用されると、エンドユーザーは広告から最終的なURLに直接送信され、トラッキングテンプレートのURL （クリック測定付き）がバックグラウンドで読み込まれます。

統合が完了すると、Search, Social, &amp; Commerceは、設定されたレポートスイートに対して[!DNL Analytics]で追跡されたすべてのページ上イベントデータを自動的に受け取ります。

>[!MORELIKETHIS]
>
>* [&#x200B; コンバージョン追跡オプション &#x200B;](conversion-tracking-about.md)
