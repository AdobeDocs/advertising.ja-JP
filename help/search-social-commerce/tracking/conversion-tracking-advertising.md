---
title: Adobe Advertisingのコンバージョントラッキングタグについて
description: Adobe Advertisingのコンバージョントラッキングタグの使用について説明します。
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
TQID: https://experienceleague.adobe.com/SKNAm2olxXOI-qdf67XVYpo9GtQCpQO9acywqE7YTv0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 0%

---

# Adobe Advertisingのコンバージョントラッキングタグについて

Adobe Advertisingは、「成功」ページなど、コンバージョンイベントが発生したときに開くweb ページに挿入されるAdobe Advertising コンバージョントラッキングタグを使用して、広告のクリックに起因するコンバージョンをトラッキングします。 このタグには、トランザクションデータとユーザーのAdobe Advertising cookieをトラッキングサーバーに送信するための埋め込み情報が含まれており、トラッキングサーバーから適切な広告のクリックまたはインプレッション（広告主のコンバージョンアトリビューション設定に従って）にトランザクションがクレジットされます。

Search, Social, &amp; Commerce内で[ コンバージョントラッキングタグを生成するか、Adobe Experience Platform（旧Adobe Experience Platform Launch）でタグを使用できます](/help/search-social-commerce/tools/conversion-tag-generate.md)。

>[!NOTE]
>
>ユーザーが有効なCookieを持っていない場合、Adobe Advertisingはコンバージョンをレポートしません。

追跡するコンバージョン指標のセットごとに、個別のコンバージョンタグを作成して実装する必要があります。 次のいずれかのタイプのコンバージョンタグを生成できます。

* （推奨）JavaScript タグ（バージョン 3またはバージョン 2）。web ページには表示されません。

* HTMLの画像タグを使用すると、エンドユーザーには見えない1 ピクセル x 1 ピクセルの透明画像（ピクセル）がweb ページに表示されます。 JavaScriptのタグの使用を禁止しているポリシーがある場合にのみ、画像タグを使用します。

タグタイプの違いについて詳しくは、「[Advertising Cloud コンバージョントラッキングタグに関するよくある質問](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。

>[!NOTE]
>
>* この機能は、広告主のweb ページに画像タグやJavaScriptタグを追加するものではありません。 タグは、web ページを更新するための広告主の通常の手順に従って追加する必要があります。
>* タグの実装にかかる時間を必ず考慮してください。 企業のポリシーによっては、実装に数週間から数カ月かかる場合もあります。

## Adobe Advertisingのコンバージョントラッキングタグの機能

コンバージョントラッキングピクセルを使用すると、Adobe Advertisingで次のことが可能になります。

* 検索キャンペーンのキーワードレベルでコンバージョンデータを追跡し、レポートできます。

* あらゆるマーケティングチャネル（有料検索とディスプレイ）をまたいで、広告（クリエイティブ）レベルでコンバージョンデータを追跡およびレポートします。これによりクリエイティブテストを促進できます。

* あらゆるマーケティングチャネルをまたいで、トランザクションレベルのコンバージョンデータを追跡してレポートできます。

* コンバージョンがさまざまなマーケティングチャネルにどのように分布しているかを明らかにし、最も効果的な方法を特定します。

* 様々なアトリビューションレベルでのレポートと最適化（最後の関連イベントへのコンバージョンのアトリビューションや、すべてのイベントの均等な重み付けなど）。

* クリックアシスト（コンバージョン funnelに貢献した検索キーワードまたはプレースメント）とチャネルアシスト（コンバージョン funnelに貢献したユーザーイベント）に関する可視性を提供します。

* サイトトラフィックとコンバージョンの地理的分布と参照ドメインを可視化することで、地理的およびweb サイトのターゲティングを絞り込むことができます。

* コンバージョン率の向上に役立つ、曜日や日中のトレンドを分析します。

>[!MORELIKETHIS]
>
>* [ コンバージョン追跡オプション ](conversion-tracking-about.md)
>* [Adobe Advertising コンバージョンタグを生成して実装](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3](format-conversion-tag-jsv3.md)の形式
>* [JavaScript コンバージョントラッキングタグバージョン 2](format-conversion-tag-jsv2.md)の形式
>* [画像コンバージョントラッキングタグの形式](format-conversion-tag-image.md)
>* コンバージョンとページビューのトラッキングタグに関する[FAQ](faqs-conversion-page-view-tracking-tags.md)
>* [Adobe Advertising JavaScript コンバージョンマッピングタグ ](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
