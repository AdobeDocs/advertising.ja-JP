---
title: 検索、ソーシャル、Commerceのコンバージョントラッキングオプション
description: 検索、ソーシャル、Commerceのコンバージョントラッキングオプションについて説明します。
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# 検索、ソーシャル、Commerceのコンバージョントラッキングオプション

検索、ソーシャル、Commerceでは、次の方法でトラッキングされるコンバージョンデータを使用できます。

* **Adobe Advertisingトラッキングコンバージョン：** 広告主は各コンバージョンページにAdobe Advertisingコンバージョントラッキングタグを挿入します。 タグは、変換データをトラッキングサーバーに送信します。 従来のサードパーティピクセルまたは新しいファーストパーティピクセルのいずれかを使用できます。 [ 各コンバージョントラッキング方法の比較 ](#conversion-tracking-comparison) を参照してください。

* **Adobe Analytics コンバージョン：** 広告主はすべてのコンバージョンにAdobe Analytics トラッキングを使用します。 このオプションを使用するには、Adobe AdvertisingとAdobe Analyticsの統合が必要です。 詳しくは、「[Adobe Analyticsのコンバージョントラッキング ](conversion-tracking-analytics.md)」を参照してください。

* **[!DNL Google Analytics]コンバージョン：** 広告主は [!DNL Google Analytics] タグを使用してすべてのコンバージョンを追跡します。 自動同期されるコンバージョンについて詳しくは、「[[!DNL Google Ads]  検索、ソーシャル、Commerceのコンバージョンデータ ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」を参照してください。

* **広告主が追跡するコンバージョン：** （検索、ソーシャル、Commerceのクライアントのみ）広告主は、オンラインとオフラインのコンバージョンデータを任意に組み合わせたフィードファイルを検索、ソーシャル、Commerceに提供します。 「[EF ID フィードを使用したコンバージョントラッキング ](feed-efid.md)」および「[ トランザクション ID フィードを使用したコンバージョントラッキング ](feed-transaction-id.md)」を参照してください。

## 各コンバージョントラッキング方法の比較 {#conversion-tracking-comparison}

ブラウザーの cookie ポリシーは引き続き厳しくなるので、現在のトラッキング機能を理解し、長期的に最適なオプションを特定することが重要です。

| トラッキング方法 | 説明 | 制限事項 | 利点 | 推奨しますか？ |
|----|----|----|----|----|
| Adobe Analytics | [AdvertisingのAdobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=ja) を使用している広告主は、レポートおよび最適化のために、[!DNL Analytics] の標準イベントとカスタムイベントをAdobe Advertisingに自動的に読み込みます。 | <ul><li>[!DNL Safari] では 7 日間のコンバージョンルックバックのみが許可されます。これは、ルックバックウィンドウ中の繰り返しサイト訪問でリセットされます。</li><li> 2024 年にも [!DNL Chrome] で同様の制限が予定されています。</li></ul> | <ul><li>[!DNL Analytics] とのシームレスな統合</li> <li>[!DNL Analytics] Analysis Workspaceの有料検索データを参照してください</li><li>有料検索を超えるメリット</li></ul> | はい |
| 従来のAdobe Advertisingピクセル | 広告主は、従来のAdobe Advertising画像やJavaScript ピクセルをコンバージョンページに追加します。 ピクセルが呼び出されるのは、広告をクリックしたユーザーがページに到達したときです。 この方法は、サードパーティ cookie に依存します。 | <ul><li>[!DNL Safari] は、このメソッドを使用するすべてのコンバージョントラッキングをブロックします。</li><li>2024 年にも [!DNL Chrome] で同様の制限が予定されています。</li></ul> | ピクセルは既に実装されています。 ただし、引き続き [ 追加の ITP マッピングタグを実装する ](itp-conversion-mapping-tag.md) 必要があります。<br><br> 推奨事項：ファーストパーティのピクセルに切り替えます。 | 不可 |
| Adobe Advertisingファーストパーティピクセル | 広告主は次の操作を行います。 <ul><li>サイト全体に [Adobe Experience Cloud ID （ECID） サービスのJavaScript ライブラリ ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja) 実装します。</li><li>Adobe Advertising[ITP マッピングを使用したJavaScript タグ ](itp-conversion-mapping-tag.md) を、検索クリックからランディングページになる可能性のある任意のページに追加します（ランディングページは時間と共に変化する可能性があるので、すべてのページで行うのが理想的です）。 タグを使用すると、Adobe Advertisingは、大きな数値をランディングページの科学表記に変換するページで発生するコンバージョンイベントを追跡できます。</li><li>Adobe Advertising [JavaScript コンバージョントラッキングタグ v3](format-conversion-tag-jsv3.md) をコンバージョンページに追加します。</li></ul> | <ul><li>[!DNL Safari] では 7 日間のコンバージョンルックバックのみが許可されます。これは、ルックバックウィンドウ中の繰り返しサイト訪問でリセットされます。</li><li>2022 年にも [!DNL Chrome] で同様の制限が予定されています。</li></ul> | [!DNL Safari] は、7 日間のルックバック中にコンバージョンを追跡します。 ルックバックウィンドウ中の繰り返しサイト訪問でルックバックがリセットされるので、この制限が一部の [!DNL Safari] ユーザーに影響するわけではありません。 | 不可 |
| EFID フィード | 広告主の検索アカウントは、宛先の URL や最終的な URL をAdobe Advertisingの一意の ID （トークン）で生成するように設定されています。 Adobe Advertisingが広告をクリックすると、ユーザーは一意の ID （`EFID`）を作成し、最終的な URL の最後に表示します。 広告主のクライアントシステムは、クリックによって生じたコンバージョンの一意の ID として EFID をキャプチャし、EFID、取引日、コンバージョン指標を含む売上高フィードでAdobe Advertisingに送信します。 次に、Adobe Advertisingは EFID を使用して、元のクリックに対するコンバージョンを照合します。 | <ul><li>広告主は、EFID をキャプチャし、自動フィードを毎日Adobe Advertisingに送信する手段を持つ必要があります。</li><li>コンバージョンは、最大 180 日間（Adobe Advertisingあたり）または広告主のシステムの制限に従ってトラッキングできます。</li></ul> | <ul><li>この方法では、ファーストパーティのコンバージョンデータを使用するので、サードパーティ cookie の制限の影響を受けません。</li><li>オンラインおよびオフラインのコンバージョンは、1 つのフィードで送信できます。</li><li>このサイトでは、コードの変更やタグは必要ありません。</li></ul> | はい |
| トランザクション ID フィード [ コンボフィード ] | Adobe Advertising主は、一意のトランザクション ID （`ev_transid=&lt;transid&gt;`）のパラメーターを含んだ広告ピクセルを web ページに追加します。Adobe Advertisingは、ピクセルが実行されたときに作成された一意のトランザクション ID をキャプチャします。 広告主のクライアントシステムも [!UICONTROL Transaction ID] をキャプチャし、[!UICONTROL Transaction ID] 値が一致するオフラインコンバージョンの売上高フィードをAdobe Advertisingに送信します | <ul><li>広告主が従来のピクセルを使用しており、それがトリガーをブロックし [!DNL Safari] いる場合、ID はキャプチャされず、オフラインデータに使用されません。</li><li>フィードは自動化されません。</li></ul> | <ul><li>ファーストパーティピクセルを実装する場合、[!UICONTROL Transaction ID] は [!DNL Safari] でキャプチャされます。</li><li>オフラインまたは承認済みのコンバージョンイベントをトラッキングできます。</li></ul> | 不可 |
| [!DNL Google] コンバージョン | [!DNL Google Analytics] タグで追跡されたコンバージョンは、API 接続を介してAdobe Advertisingに自動的に読み込まれます。 各コンバージョン名には `&quot;GGL_&quot;` のプレフィックスが付きます。 | <ul><li>[!DNL Google] は通常、オフラインデータを追跡しません。</li><li>[!DNL Microsoft Advertising] コンバージョンは含まれません。</li></ul> | [!DNL Google] は、機械学習を使用して「モデル化されたコンバージョン [ を推定 ](https://support.google.com/google-ads/answer/10081327) ます。 | 不可 |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analyticsのコンバージョントラッキング ](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [EF ID フィードを使用したコンバージョントラッキング ](/help/search-social-commerce/tracking/feed-efid.md)
>* [ トランザクション ID フィードを使用したコンバージョントラッキング ](/help/search-social-commerce/tracking/feed-transaction-id.md)
