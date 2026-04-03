---
title: Search、Social、Commerceのコンバージョントラッキングオプション
description: Search, Social, & Commerceのコンバージョントラッキングオプションについて説明します。
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
TQID: https://experienceleague.adobe.com/Zv-ncIkpwqM24hoF9I2T8Er9Qf8R0j2fJSSk4jI7HSo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 821
ht-degree: 0%

---

# Search、Social、Commerceのコンバージョントラッキングオプション

Search, Social, &amp; Commerceでは、次の方法で追跡されたコンバージョンデータを使用できます。

* **Adobe Advertisingで追跡されたコンバージョン：**&#x200B;広告主は、各コンバージョンページにAdobe Advertising コンバージョントラッキングタグを挿入します。 タグは、変換データをトラッキングサーバーに送信します。 従来のサードパーティピクセルまたは新しい1st パーティピクセルのいずれかを使用できます。 「[各コンバージョン トラッキング メソッドの比較](#conversion-tracking-comparison)」を参照してください。

* **Adobe Analytics コンバージョン：**&#x200B;広告主は、すべてのコンバージョンにAdobe Analytics トラッキングを使用します。 このオプションを使用するには、Adobe AdvertisingとAdobe Analyticsの統合が必要です。 詳しくは、「[Adobe Analytics コンバージョントラッキング ](conversion-tracking-analytics.md)」を参照してください。

* **[!DNL Google Analytics]コンバージョン：**&#x200B;広告主は[!DNL Google Analytics] タグを使用してすべてのコンバージョンを追跡します。 自動同期されるコンバージョンについて詳しくは、「[[!DNL Google Ads] Search, Social, &amp; Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」のコンバージョンデータを参照してください。

* **広告主によるコンバージョンのトラッキング：** （Search, Social, &amp; Commerce クライアントのみ）広告主は、オンラインとオフラインのコンバージョンデータを任意に組み合わせて、Search, Social, &amp; Commerceにフィードファイルを提供します。 「[EF ID フィードを使用したコンバージョン追跡](feed-efid.md)」および「[ トランザクション ID フィードを使用したコンバージョン追跡](feed-transaction-id.md)」を参照してください。

## 各コンバージョン追跡方法の比較 {#conversion-tracking-comparison}

ブラウザーのクッキーポリシーが厳しくなるにつれ、現在のトラッキング機能を理解し、長期的に最適なオプションを特定することが重要です。

| トラッキング方法 | 説明 | 制限 | Adobe Workfrontの利点 | 推奨？ |
|----|----|----|----|----|
| Adobe Analytics | [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)を使用している広告主は、レポートと最適化のために、[!DNL Analytics]標準イベントとカスタムイベントを自動的にAdobe Advertisingに読み込みます。 | <ul><li>[!DNL Safari]では、ルックバックウィンドウ中に繰り返しサイトを訪問した場合にリセットされる、7日間のコンバージョンルックバックのみが許可されます。</li><li> 2024年の[!DNL Chrome]にも同様の制限が見込まれます。</li></ul> | <ul><li>[!DNL Analytics]とのシームレスな統合</li> <li>[!DNL Analytics] Analysis Workspaceの有料検索データを見る</li><li>検索連動型広告の枠を超えた利点</li></ul> | はい |
| レガシーAdobe Advertising Pixel | 広告主は、従来のAdobe Advertisingの画像やJavaScriptのピクセルをコンバージョンページに追加しています。 ピクセルは、広告をクリックしたユーザーがページに到達したときに起動されます。 この方法は、サードパーティ Cookieに依存しています。 | <ul><li>[!DNL Safari]は、このメソッドを使用するすべてのコンバージョン追跡をブロックします。</li><li>2024年の[!DNL Chrome]にも同様の制限が見込まれます。</li></ul> | ピクセルは既に実装されています。 ただし、追加のITP マッピングタグ [を](itp-conversion-mapping-tag.md)実装する必要があります。<br><br>推奨事項：1st パーティピクセルに切り替えます。 | いいえ |
| Adobe Advertising ファーストパーティピクセル | 広告主は次のことをおこないます。 <ul><li>サイト全体で[Adobe Experience Cloud ID （ECID） サービス ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html)のJavaScript ライブラリを実装します。</li><li>ITP マッピング [を含むAdobe Advertising ](itp-conversion-mapping-tag.md)JavaScript タグを、検索クリックからランディングページになる可能性のある任意のページ（理想的には、すべてのページで、ランディングページは時間の経過とともに変化する可能性があるため）に追加します。 このタグを使用すると、Adobe Advertisingは、大量のデータをランディングページの科学的表記法に変換するページ上で発生するコンバージョンイベントを追跡できます。</li><li>Adobe Advertising [JavaScript コンバージョントラッキングタグ v3](format-conversion-tag-jsv3.md)をコンバージョンページに追加します。</li></ul> | <ul><li>[!DNL Safari]では、ルックバックウィンドウ中に繰り返しサイトを訪問した場合にリセットされる、7日間のコンバージョンルックバックのみが許可されます。</li><li>2022年の[!DNL Chrome]にも同様の制限が見込まれます。</li></ul> | [!DNL Safari]は、7日間のルックバック中にコンバージョンを追跡します。 ルックバックは、ルックバックウィンドウ中に繰り返しサイトを訪問したときにリセットされるので、制限はすべての[!DNL Safari] ユーザーに影響するわけではありません。 | いいえ |
| EFID フィード | 広告主の検索アカウントは、Adobe Advertisingの一意のID （トークン）を使用して宛先URL/最終的なURLを生成するように設定されています。 ユーザーが広告をクリックすると、Adobe Advertisingは一意のID （`EFID`）を作成し、最終的なURLの最後に表示します。 広告主のクライアントシステムは、クリックの結果として生じたコンバージョンの一意のIDとしてEFIDを取得し、EFID、トランザクション日、コンバージョン指標を含む収益フィードとしてAdobe Advertisingに送信します。 その後、Adobe AdvertisingはEFIDを使用して、コンバージョンを元のクリックに一致させます。 | <ul><li>広告主は、EFIDを取得し、自動化されたフィードを毎日Adobe Advertisingに送信する方法を持っている必要があります。</li><li>コンバージョンは、最大180日間（Adobe Advertisingごと）または広告主のシステムの制限に従って追跡できます。</li></ul> | <ul><li>この方法は、ファーストパーティのコンバージョンデータを使用するため、サードパーティのCookieの制限の影響を受けません。</li><li>オンラインとオフラインのコンバージョンをひとつのフィードで送信できます。</li><li>サイトにコードの変更やタグは必要ありません。</li></ul> | はい |
| トランザクション ID フィード [ コンボフィード ] | 広告主は、一意のトランザクション ID （`ev_transid=&lt;transid&gt;`）のパラメーターを含むAdobe Advertising ピクセルをweb ページに追加し、Adobe Advertisingは、ピクセルの起動時に作成された一意のトランザクション IDをキャプチャします。 広告主のクライアントシステムも[!UICONTROL Transaction ID]をキャプチャし、一致する[!UICONTROL Transaction ID]値のオフラインコンバージョンの収益フィードをAdobe Advertisingに送信します | <ul><li>広告主が従来のピクセルを使用しており、[!DNL Safari]が起動をブロックしている場合、IDはオフラインデータに使用するようにキャプチャされません。</li><li>フィードは自動化されていません。</li></ul> | <ul><li>1st パーティピクセルを実装すると、[!UICONTROL Transaction ID]が[!DNL Safari]にキャプチャされます。</li><li>オフライン/承認済みのコンバージョンイベントのトラッキングを提供します。</li></ul> | いいえ |
| [!DNL Google] コンバージョン | [!DNL Google Analytics] タグでトラッキングされたコンバージョンは、API接続を介して自動的にAdobe Advertisingにインポートされます。 各コンバージョン名には`&quot;GGL_&quot;`という接頭辞が付きます。 | <ul><li>[!DNL Google]は通常、オフラインデータを追跡しません。</li><li>[!DNL Microsoft Advertising]個のコンバージョンは含まれていません。</li></ul> | [!DNL Google]は機械学習を使用して、「[ モデル化されたコンバージョン ](https://support.google.com/google-ads/answer/10081327)」を推定します。 | いいえ |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics コンバージョン トラッキング ](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [EF ID フィードを使用したコンバージョンの追跡](/help/search-social-commerce/tracking/feed-efid.md)
>* [ トランザクション ID フィードを使用したコンバージョン追跡](/help/search-social-commerce/tracking/feed-transaction-id.md)
