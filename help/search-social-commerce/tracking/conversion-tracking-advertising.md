---
title: Adobe Advertisingのコンバージョントラッキングタグについて
description: コンバージョントラッキングタグのAdobe Advertisingについて説明します。
exl-id: 07403d60-6db2-47e7-977b-4b59c8797c3d
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Adobe Advertisingのコンバージョントラッキングタグについて

Adobe Advertisingは、「成功」ページなど、コンバージョンイベントの発生時に開く Web ページに挿入されるAdobe Advertisingコンバージョントラッキングタグを使用して、広告のクリックによるコンバージョンを追跡します。 タグには、トランザクションデータをユーザーのAdobe AdvertisingCookie と共にトラッキングサーバーに送信する埋め込み情報が含まれます。このトラッキングサーバーから、（広告主のコンバージョン属性設定ごとに）適切な広告クリックまたはインプレッションにトランザクションが付与されます。

>[!NOTE]
>
>ユーザーが有効な cookie を持っていない場合、Adobe Advertisingはコンバージョンをレポートしません。

追跡する一連のコンバージョン指標ごとに、個別のコンバージョンタグを作成する必要があります。 広告主または代理店に各タグを挿入する Web ページのリストを提供します。 次のいずれかのタイプのコンバージョンタグを生成できます。 参照：[Adobe Advertisingコンバージョンタグの生成](/help/search-social-commerce/tools/conversion-tag-generate.md)」を参照してください。

* （推奨）Web ページに表示されない JavaScript タグ（バージョン 3 またはバージョン 2）。

* Web ページに 1 ピクセル x 1 ピクセルの透明画像（ピクセル）を表示するHTML画像タグ。エンドユーザーはこの画像を表示できません。 画像タグは、会社が JavaScript タグの使用に対するポリシーを持っている場合にのみ使用してください。

タグタイプの違いについて詳しくは、[Advertising Cloudコンバージョントラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* この機能では、画像タグや JavaScript タグは広告主の Web ページに追加されません。 タグは、Web ページを更新する際の広告主の通常の手順に従って追加する必要があります。
>* タグの実装にかかる時間を必ず考慮してください。 会社の方針によっては、導入に数週間から数ヶ月かかる場合があります。

## Adobe Advertisingのコンバージョントラッキングタグの機能

コンバージョントラッキングピクセルを使用すると、Adobe Advertisingは次の操作を実行できます。

* 検索キャンペーンのキーワードレベルでコンバージョンデータを追跡し、レポートします。

* すべてのマーケティングチャネル（有料検索とディスプレイ）にわたって広告（クリエイティブ）レベルでコンバージョンデータを追跡およびレポートできるので、クリエイティブテストを容易におこなえます。

* すべてのマーケティングチャネルをまたいで、トランザクションレベルでコンバージョンデータを追跡し、レポートします。

* コンバージョンが様々なマーケティングチャネルにどのように分布しているかを示し、最も効果的なマーケティングチャネルを確認できます。

* 様々な属性レベルでレポートし、最適化します（コンバージョンを最後の関連イベントに関連付けたり、すべてのイベントに均等に重み付けしたりするなど）。

* クリック支援（コンバージョンファネルに貢献した検索キーワードまたはプレースメント）やチャネル支援（コンバージョンファネルに貢献したユーザーイベント、複数のマーケティングチャネルにわたる場合もある）を視覚的に表示します。

* サイトトラフィックおよびコンバージョンの地理的分布および参照ドメインを表示し、地理的および Web サイトのターゲティングをより細かく調整できます。

* コンバージョン率の向上に使用できる、曜日または日内トレンドを分析します。

>[!MORELIKETHIS]
>
>* [コンバージョントラッキングオプション](conversion-tracking-about.md)
>* [Adobe Advertisingコンバージョンタグの生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式](format-conversion-tag-jsv3.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式](format-conversion-tag-jsv2.md)
>* [画像コンバージョントラッキングタグの形式](format-conversion-tag-image.md)
>* [コンバージョンおよびページビューのトラッキングタグに関する FAQ](faqs-conversion-page-view-tracking-tags.md)
>* [Adobe Advertisingの JavaScript コンバージョンマッピングタグ](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
