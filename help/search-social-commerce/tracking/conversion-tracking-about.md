---
title: 検索、ソーシャル、コマースのコンバージョントラッキングオプション
description: 検索、ソーシャル、コマースのコンバージョントラッキングオプションについて説明します。
source-git-commit: 5dadb0bea063f454dcfde46c0a4cc747290767c8
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 検索、ソーシャル、コマースのコンバージョントラッキングオプション

検索、ソーシャル、コマースでは、次の方法で追跡されているコンバージョンデータを使用できます。

* **Adobe広告で追跡されたコンバージョン：** 広告主は、各コンバージョンページにAdobe広告のコンバージョントラッキングタグを挿入します。 タグは、コンバージョンデータをトラッキングサーバーに送信します。 従来のサードパーティピクセルか、新しいファーストパーティピクセルのどちらかを使用できます。 参照：[各コンバージョントラッキングメソッドの比較](#conversion-tracking-comparison).&quot;

* **Adobe Analyticsコンバージョン：** 広告主は、すべてのコンバージョンにAdobe Analyticsトラッキングを使用します。 このオプションを使用するには、AdobeAdvertising とAdobe Analyticsの統合が必要です。 参照：[Adobe Analyticsコンバージョントラッキング](conversion-tracking-analytics.md)」を参照してください。

* **[!DNL Google Analytics]コンバージョン：** 広告主が [!DNL Google Analytics] タグで、すべてのコンバージョンを追跡できます。 参照：[[!DNL Google Ads] 検索、ソーシャル、コマースのコンバージョンデータ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」を参照してください。

* **広告主がトラッキングしたコンバージョン：** （Search、Social、および Commerce のクライアントのみ）広告主は、オンラインとオフラインのコンバージョンデータを任意に組み合わせたフィードファイルを Search、Social、および Commerce に提供します。 参照：[EF ID フィードを使用したコンバージョントラッキング](feed-efid.md)&quot;および&quot;[トランザクション ID フィードを使用したコンバージョントラッキング](feed-transaction-id.md).&quot;

## 各コンバージョントラッキングメソッドの比較 {#conversion-tracking-comparison}

ブラウザーの Cookie ポリシーが厳しくなり続けるにつれ、現在のトラッキング機能を理解し、長期的に最適なオプションを特定することが重要です。

| トラッキングメソッド | 説明 | 制限事項 | メリット | 推奨？ |
|----|----|----|----|----|
| Adobe Analytics | 次を持つ広告主 [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) 自動的にインポート [!DNL Analytics] 標準およびカスタムイベントをAdobe Advertisingに追加し、レポートおよび最適化をおこないました。 | <ul><li>[!DNL Safari] では、7 日間のコンバージョンルックバックのみを使用できます。これは、ルックバックウィンドウ中にサイトの再訪問時にリセットされます。</li><li> 同様の制限を期待する [!DNL Chrome] 2024 年に。</li></ul> | <ul><li>とのシームレスな統合 [!DNL Analytics]</li> <li>で有料検索データを確認する [!DNL Analytics] Analysis Workspace</li><li>有料検索以外のメリット</li></ul> | はい |
| レガシーAdobe Advertisingピクセル | 広告主は、コンバージョンページに従来のAdobe Advertising画像または JavaScript ピクセルを追加します。 ピクセルは、広告をクリックしたユーザーがページに到達すると実行されます。 この方法は、サードパーティ Cookie に依存しています。 | <ul><li>[!DNL Safari] は、このメソッドを使用するすべてのコンバージョントラッキングをブロックします。</li><li>同様の制限を期待する [!DNL Chrome] 2024 年に。</li></ul> | ピクセルは既に実装されています。 しかし、まだ [追加の ITP マッピングタグの実装](itp-conversion-mapping-tag.md).<br><br>推奨事項：ファーストパーティピクセルに切り替えます。 | いいえ |
| Adobe Advertisingファーストパーティピクセル | 広告主は次の操作を実行します。 <ul><li>用の JavaScript ライブラリの実装 [Adobe Experience Cloud ID(ECID) サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) サイト全体を通じて</li><li>Adobe Advertising [ITP マッピングを含む JavaScript タグ](itp-conversion-mapping-tag.md) を検索クリックからランディングページになる可能性のある任意のページにドラッグします（ランディングページは時間の経過と共に変化する可能性があるので、理想的にはすべてのページで）。 タグを使用すると、Adobe Advertisingは、大きな数値がランディングページの科学的表記に変換されるページで発生するコンバージョンイベントを追跡できます。</li><li>Adobe Advertising [JavaScript コンバージョントラッキングタグ v3](format-conversion-tag-jsv3.md) をコンバージョンページに変換します。</li></ul> | <ul><li>[!DNL Safari] では、7 日間のコンバージョンルックバックのみを使用できます。これは、ルックバックウィンドウ中にサイトの再訪問時にリセットされます。</li><li>同様の制限を期待する [!DNL Chrome] 2022 年に。</li></ul> | [!DNL Safari] は、7 日間のルックバック中にコンバージョンを追跡します。 ルックバックウィンドウではサイトの再訪問時にルックバックがリセットされるので、この制限はすべてに影響を与えるわけではありません [!DNL Safari] ユーザー。 | いいえ |
| EFID フィード | 広告主の検索アカウントは、Adobe Advertisingの一意の ID（トークン）を使用して宛先 URL/最終 URL を生成するように設定されています。 ユーザーが広告をクリックすると、Adobe広告は一意の ID (`EFID`) の上にマウスポインターを置き、最終 URL の末尾に表示します。 広告主のクライアントシステムは、EFID をクリックによるコンバージョンの一意の識別子としてキャプチャし、EFID、トランザクション日、コンバージョンプロパティを含む収益フィードでAdobe広告に送信します。 Adobe Advertisingは EFID を使用して、元のクリックへの変換を照合します。 | <ul><li>広告主は、EFID を取得し、自動フィードを毎日Adobe Advertisingに送信する方法が必要です。</li><li>コンバージョンは、(Adobe Advertisingごとに ) 最大 180 日間、または広告主のシステムの制限に従って追跡できます。</li></ul> | <ul><li>この方法ではファーストパーティコンバージョンデータを使用するので、サードパーティ Cookie の制限の影響を受けません。</li><li>オンラインとオフラインのコンバージョンを 1 つのフィードで送信できます。</li><li>サイトのコードの変更やタグは必要ありません。</li></ul> | はい |
| トランザクション ID フィード [コンボフィード] | 広告主は、一意のAdobe AdvertisingID (`ev_transid=&lt;transid&gt;`) を Web ページに送信する際に、Adobe Advertisingは、ピクセルが実行されたときに作成される一意のトランザクション ID を取り込みます。 広告主のクライアントシステムも [!UICONTROL Transaction ID] とは、Adobe Advertisingに対し、 [!UICONTROL Transaction ID] 値 | <ul><li>広告主がレガシーピクセル ( [!DNL Safari] ブロックが実行されない場合、ID はキャプチャされず、オフラインデータに使用されます。</li><li>フィードは自動化されていません。</li></ul> | <ul><li>ファーストパーティピクセルを実装する場合、 [!UICONTROL Transaction ID] が [!DNL Safari].</li><li>オフライン/承認済みのコンバージョンイベントの追跡を提供します。</li></ul> | いいえ |
| Google Conversions | でトラッキングされるコンバージョン [!DNL Google Analytics] タグは、API 接続を介してAdobe Advertisingに自動的に読み込まれます。 各コンバージョン名には、 `&quot;GGL_&quot;` プレフィックス | <ul><li>Googleは通常、オフラインデータを追跡しません。</li><li>Microsoft®広告コンバージョンは含まれていません。</li></ul> | Googleは機械学習を使用して「 」を推定する[モデル化された変換](https://support.google.com/google-ads/answer/10081327).&quot; | いいえ |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Adobe広告のコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analyticsコンバージョントラッキング](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [EF ID フィードを使用したコンバージョントラッキング](/help/search-social-commerce/tracking/feed-efid.md)
>* [トランザクション ID フィードを使用したコンバージョントラッキング](/help/search-social-commerce/tracking/feed-transaction-id.md)
