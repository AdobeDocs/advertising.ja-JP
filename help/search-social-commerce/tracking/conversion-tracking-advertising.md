---
title: Adobe Advertisingのコンバージョントラッキングタグについて
description: Adobe Advertisingコンバージョントラッキングタグの使用について説明します。
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Adobe Advertisingのコンバージョントラッキングタグについて

Adobe Advertisingは、「成功」ページなど、コンバージョンイベントの発生時に開く web ページに挿入されたAdobe Advertisingコンバージョントラッキングタグを使用して、広告のクリックによって発生したコンバージョンを追跡します。 タグには、トランザクションデータをユーザーのAdobe Advertising cookie と共にトラッキングサーバーに送信するための埋め込み情報が含まれており、そこから（広告主のコンバージョン アトリビューション設定に従って）適切な広告クリックまたはインプレッションにトランザクションがクレジットされます。

>[!NOTE]
>
>ユーザーが有効な Cookie を持っていない場合、Adobe Advertisingはコンバージョンをレポートしません。

追跡するコンバージョン指標のセットごとに、個別のコンバージョンタグを作成する必要があります。 広告主または代理店に、それぞれ挿入する web ページのリストをタグに提供します。 次のいずれかのタイプのコンバージョンタグを生成できます。 手順については、「[Adobe Advertisingコンバージョンタグを生成 ](/help/search-social-commerce/tools/conversion-tag-generate.md)」を参照してください。

* （推奨）JavaScript タグ（バージョン 3 またはバージョン 2）が web ページに表示されない。

* HTMLイメージタグを使用すると、エンドユーザーには表示されない 1 ピクセル x 1 ピクセルの透明な画像（ピクセル）を web ページに表示できます。 画像タグの使用は、会社がJavaScript タグの使用に対するポリシーを持っている場合にのみ行います。

タグタイプの違いについて詳しくは、「[Advertising Cloud コンバージョントラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。

>[!NOTE]
>
>* この機能では、広告主の web ページに画像タグやJavaScript タグを追加しません。 Web ページを更新する際は、広告主の通常の手順に従ってタグを追加する必要があります。
>* タグの実装に要する時間を必ず考慮してください。 会社のポリシーによっては、実装に数週間または数か月かかる場合があります。

## Adobe Advertisingのコンバージョントラッキングタグの機能

コンバージョントラッキングのピクセルを使用すると、Adobe Advertisingで次の操作を実行できます。

* 検索キャンペーン用のキーワードレベルでのコンバージョンデータの追跡とレポート。

* すべてのマーケティングチャネル（有料検索および表示）をまたいで、広告（クリエイティブ）レベルでコンバージョンデータを追跡しレポートします。これにより、クリエイティブテストを容易におこなうことができます。

* すべてのマーケティングチャネルにわたって、トランザクションレベルでコンバージョンデータを追跡し、レポートします。

* 様々なマーケティングチャネル間でのコンバージョンの配分方法を表示して、どれが最も効果的かを確認できます。

* 様々なアトリビューションレベルでレポートおよび最適化します（最後の関連イベントに対するコンバージョンの帰属や、すべてのイベントの均等加重など）。

* クリック支援（コンバージョンファネルに貢献した検索キーワードまたはプレースメント）とチャネル支援（コンバージョンファネルに貢献したユーザーイベント、複数のマーケティングチャネルにわたる可能性あり）を可視化します。

* サイトトラフィックやコンバージョンの地理的分布および参照ドメインを可視化して、地理的および web サイトのターゲティングを絞り込むことができます。

* コンバージョン率の向上に使用できる、曜日または日中のトレンドを分析します。

>[!MORELIKETHIS]
>
>* [ コンバージョントラッキングオプション ](conversion-tracking-about.md)
>* [Adobe Advertisingコンバージョンタグを生成 ](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式 ](format-conversion-tag-jsv3.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式 ](format-conversion-tag-jsv2.md)
>* [ 画像変換トラッキングタグの形式 ](format-conversion-tag-image.md)
>* [ コンバージョンおよびページビューのトラッキングタグに関する FAQ](faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョンマッピングタグのAdobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
