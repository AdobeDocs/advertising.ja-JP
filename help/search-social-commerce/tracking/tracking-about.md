---
title: Search, Social, & Commerceのトラッキングについて
description: Search, Social, & Commerceのトラッキングオプションについて説明します。
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
TQID: https://experienceleague.adobe.com/IpPgzsMgRsOCmLv3dyEKBp4EPQwgN90UkVIQy9SaXB8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# Search, Social, &amp; Commerceのトラッキングについて

広告の効果を追跡するには、Search, Social, &amp; Commerceで広告のインプレッション、クリック、コスト、コンバージョン（取引）データが必要です。 Search, Social, &amp; Commerceでは、収集したデータを使用して、広告ポートフォリオを最適化するために必要なデータ予測モデルを構築します。

## コスト、クリック、インプレッションデータ

Search, Social, &amp; Commerceは、毎日[&#x200B; サポートされている広告ネットワーク &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)からインプレッション、クリック、コストのデータを直接取得します。 さらに、Search, Social, &amp; Commerceでは、トラッキングテンプレートと宛先URLに固有のクリックトラッキングコード（トラッキングサーバーへのリダイレクトを含む）を追加して、表示/コンテンツのインプレッション数、クリック数、コストを追跡し、後でイベントをコンバージョンに結び付けることができます。

Search, Social, &amp; Commerceがデータを同期しない広告ネットワーク上のキャンペーンをトラッキングする場合は、インプレッション、クリック、コストデータを含む日次フィードファイルを送信して、キャンペーンのデータを提供する必要があります。

### クリックトラッキングタグ

Search, Social, &amp; Commerceの導入チームは、同期された広告キャンペーン内の広告、キーワード、プレースメント、商品グループ、サイトリンク拡張機能のトラッキングテンプレートと宛先URLを更新して、一意のトラッキング ID文字列とAdobe Advertisingリダイレクトを含めるようにクリックトラッキングを設定します。 また、[!DNL Google Ads]および[!DNL Microsoft Advertising]のアカウントとキャンペーンのランディングページのサフィックス（最終的なURL サフィックス）にトラッキングを追加します。

トラッキングパラメーターを使用すると、Adobe Advertisingで個々のキーワードレベル（検索キャンペーン）または広告バリエーション レベル（コンテンツまたはサイトのターゲティング、表示キャンペーン、ソーシャルキャンペーンを含む検索キャンペーン）でクリックをトラッキングできます。 利用者がディスプレイ/コンテンツ広告を閲覧したり、広告のいずれかをクリックしたりするたびに、広告ネットワークは、キーワードまたは広告に関連付けられたクリックトラッキングタグを使用して、Adobe Advertisingピクセルサーバーにイベントを送信します。 クリック数：

* 並列トラッキングをサポートするブラウザー上の[!DNL Google Ads]広告と[!DNL Microsoft Advertising]広告の場合、広告ネットワークはまずweb サイトにクリックを送信し、次にAdobe Advertising pixel サーバーにクリックを送信します。このサーバーが既に存在しない場合、ユーザーのコンピューターにCookieを配置します。

* それ以外の場合は、アドネットワークが直接Adobe Advertising ピクセルサーバーにクリックを送信します。 ピクセルサーバーは、ユーザーのコンピューターにCookieを配置し（まだ存在しない場合）、ユーザーをweb サイト上の関連URLにリダイレクトします。 エンドユーザーの全体的なエクスペリエンスは、リダイレクトなしと同じです。

Cookieは、[!DNL Adobe] ドメイン （`everesttech.net`）で1st パーティ Cookieとして設定されます。 リダイレクトの後、ユーザーは広告主のドメイン上に存在し、その後、Cookieはサードパーティ Cookieとして扱われます。 Adobe Advertising Cookieについて詳しくは、「[Adobe Advertising Cookie](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html?lang=ja)」を参照してください。

## コンバージョンデータ

顧客が広告をクリックしたり、ディスプレイ広告やソーシャル広告を閲覧したりした場合、Search, Social, &amp; Commerceは、生成される各コンバージョンを、元のクリックまたはディスプレイ広告/ソーシャル広告のインプレッションにマッピングする必要があります。

広告主は、すべてのクリックとディスプレイ/ソーシャルインプレッションに対するコンバージョンデータを提供する役割を果たします。 コンバージョンデータには、入札の最適化に使用できるweb サイトで発生するあらゆる種類のイベントに関する情報を含めることができます。 コンバージョンデータを提供するには、広告主のコンバージョンページ（顧客がトランザクションを完了した後に表示される「成功」ページなど）にコンバージョントラッキングコードを実装するか、別の方法でキャプチャされたコンバージョンデータを毎日フィードファイルに送信します。

### コンバージョン追跡タグ

様々なベンダー[の](/help/search-social-commerce/tracking/conversion-tracking-about.md) コンバージョンタグを使用できます。

Adobe Advertising コンバージョンタグを使用してトランザクションを成功し、「成功」ページに移動すると、Adobe Advertising ピクセルサーバーは、クリックリダイレクト時に設定されたユーザーのコンピューター上のCookieの有無を確認します。 Cookieが見つかると、トランザクションイベントに関する情報がef_transid パラメーターを使用して渡され、トランザクションがコンバージョンとして認識され、前の広告クリックまたは表示インプレッションにクレジットされます。

オーディエンスが複数の広告をクリックした場合、Adobe Advertisingは、特に指定しない限り、最終的な広告クリックまたは（ディスプレイまたは動画キャンペーンの場合）最終的な広告インプレッションにトランザクションをクレジットします。 [&#x200B; クリックのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)と[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)は、イベントがコンバージョンに起因する可能性がある、有料クリックまたはディスプレイ/ビデオインプレッション（それぞれ）が発生してから何日経過したかを判断します。

Adobe Advertising導入チームは、広告主と協力して、広告主が実装する必要のあるコンバージョンタグのフォーマットを決定し、各コンバージョンタグを挿入するweb ページを特定し、実装するコンバージョンタグを提供します。
