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

* **Adobe Advertising追跡コンバージョン：** 広告主は、各コンバージョンページにAdobe Advertisingコンバージョントラッキングタグを挿入する。 タグは、変換データをトラッキングサーバーに送信します。 従来のサードパーティピクセルまたは新しいファーストパーティピクセルのいずれかを使用できます。 参照先」[各コンバージョントラッキング方法の比較](#conversion-tracking-comparison).」と入力します。

* **Adobe Analytics変換：** 広告主は、すべてのコンバージョンにAdobe Analyticsのトラッキングを使用します。 このオプションを使用するには、Adobe AdvertisingとAdobe Analyticsの統合が必要です。 参照先」[Adobe Analyticsのコンバージョントラッキング](conversion-tracking-analytics.md)」を参照してください。

* **[!DNL Google Analytics]コンバージョン :** 広告主はを使用します [!DNL Google Analytics] タグを付けてすべてのコンバージョンを追跡します。 参照先」[[!DNL Google Ads] 検索、ソーシャル、Commerceのコンバージョンデータ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)自動的に同期されるコンバージョンについて詳しくは、「」を参照してください。

* **広告主が追跡したコンバージョン：** （検索、ソーシャル、Commerceのクライアントのみ）広告主は、オンラインとオフラインのコンバージョンデータを任意に組み合わせたフィードファイルとして、検索、ソーシャル、Commerceを提供します。 参照先」[EF ID フィードを使用したコンバージョントラッキング](feed-efid.md)「」と「」に対して検査する値[トランザクション ID フィードを使用したコンバージョントラッキング](feed-transaction-id.md).」と入力します。

## 各コンバージョントラッキング方法の比較 {#conversion-tracking-comparison}

ブラウザーの cookie ポリシーは引き続き厳しくなるので、現在のトラッキング機能を理解し、長期的に最適なオプションを特定することが重要です。

| トラッキング方法 | 説明 | 制限事項 | 利点 | 推奨しますか？ |
|----|----|----|----|----|
| Adobe Analytics | を使用した広告主 [広告用Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) 自動的にインポート [!DNL Analytics] レポートおよび最適化のための標準およびカスタムイベントをAdobe Advertisingに送信する。 | <ul><li>[!DNL Safari] では 7 日間のコンバージョンルックバックのみが許可されます。これは、ルックバックウィンドウ中の繰り返しサイト訪問でリセットされます。</li><li> でも同様の制限が想定されます [!DNL Chrome] （2024 年）。</li></ul> | <ul><li>とのシームレスな統合 [!DNL Analytics]</li> <li>での有料検索データの参照 [!DNL Analytics] Analysis Workspace</li><li>有料検索を超えるメリット</li></ul> | はい |
| 従来のAdobe Advertisingピクセル | 広告主は、従来のAdobe Advertising画像や JavaScript ピクセルをコンバージョンページに追加します。 ピクセルが呼び出されるのは、広告をクリックしたユーザーがページに到達したときです。 この方法は、サードパーティ cookie に依存します。 | <ul><li>[!DNL Safari] は、このメソッドを使用するすべてのコンバージョントラッキングをブロックします。</li><li>でも同様の制限が想定されます [!DNL Chrome] （2024 年）。</li></ul> | ピクセルは既に実装されています。 ただし、引き続きその必要があります [追加の ITP マッピングタグの実装](itp-conversion-mapping-tag.md).<br><br>推奨事項：ファーストパーティのピクセルに切り替えます。 | 不可 |
| Adobe Advertisingファーストパーティピクセル | 広告主は次の操作を行います。 <ul><li>用の JavaScript ライブラリの実装 [Adobe Experience Cloud ID （ECID）サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) サイト全体で。</li><li>Adobe Advertisingを追加 [ITP マッピングを使用した JavaScript タグ](itp-conversion-mapping-tag.md) 検索からランディングページである可能性のある任意のページに移動します（ランディングページは時間の経過と共に変化する可能性があるので、理想的にはすべてのページで行います）。 タグを使用すると、Adobe Advertisingは、大きな数値をランディングページの科学表記に変換するページで発生するコンバージョンイベントを追跡できます。</li><li>Adobe Advertisingを追加 [JavaScript コンバージョントラッキングタグ v3](format-conversion-tag-jsv3.md) を変換ページに追加します。</li></ul> | <ul><li>[!DNL Safari] では 7 日間のコンバージョンルックバックのみが許可されます。これは、ルックバックウィンドウ中の繰り返しサイト訪問でリセットされます。</li><li>でも同様の制限が想定されます [!DNL Chrome] （2022 年）。</li></ul> | [!DNL Safari] は、7 日間のルックバック中にコンバージョンを追跡します。 ルックバックウィンドウ中の繰り返しサイト訪問でルックバックがリセットされるので、制限は一部に影響しません [!DNL Safari] ユーザー。 | 不可 |
| EFID フィード | 広告主の検索アカウントは、宛先の URL や最終的な URL をAdobe Advertisingの一意の ID （トークン）で生成するように設定されています。 ユーザーが広告をクリックすると、Adobe Advertisingは一意の ID （`EFID`）を選択し、最終的な URL の末尾に表示します。 広告主のクライアントシステムは、クリックによって生じたコンバージョンの一意の ID として EFID をキャプチャし、EFID、取引日、コンバージョン指標を含む売上高フィードでAdobe Advertisingに送信します。 次に、Adobe Advertisingは EFID を使用して、元のクリックに対するコンバージョンを照合します。 | <ul><li>広告主は、EFID をキャプチャし、自動フィードを毎日Adobe Advertisingに送信する手段を持つ必要があります。</li><li>コンバージョンは、最大 180 日間（Adobe Advertisingあたり）または広告主のシステムの制限に従ってトラッキングできます。</li></ul> | <ul><li>この方法では、ファーストパーティのコンバージョンデータを使用するので、サードパーティ cookie の制限の影響を受けません。</li><li>オンラインおよびオフラインのコンバージョンは、1 つのフィードで送信できます。</li><li>このサイトでは、コードの変更やタグは必要ありません。</li></ul> | はい |
| トランザクション ID フィード [コンボフィード] | Adobe Advertising広告主は、一意のトランザクション ID （`ev_transid=&lt;transid&gt;`）を選択します。Adobe Advertisingはピクセルが実行されたときに作成された一意のトランザクション ID をキャプチャします。 広告主のクライアントシステムでも、 [!UICONTROL Transaction ID] 一致するオフラインコンバージョンの売上高フィードをAdobe Advertisingに送信します [!UICONTROL Transaction ID] 値 | <ul><li>広告主が従来のピクセルを使用している場合、次のようになります [!DNL Safari] が実行をブロックした場合、その ID はキャプチャされず、オフラインデータに使用されません。</li><li>フィードは自動化されません。</li></ul> | <ul><li>ファーストパーティのピクセルを実装する場合は、 [!UICONTROL Transaction ID] はでキャプチャされます。 [!DNL Safari].</li><li>オフラインまたは承認済みのコンバージョンイベントをトラッキングできます。</li></ul> | 不可 |
| [!DNL Google] コンバージョン | で追跡されたコンバージョン [!DNL Google Analytics] タグは、API 接続を介してAdobe Advertisingに自動的に読み込まれます。 各コンバージョン名には、 `&quot;GGL_&quot;` プレフィックス。 | <ul><li>[!DNL Google] は通常、オフラインデータを追跡しません。</li><li>[!DNL Microsoft Advertising] コンバージョンは含まれません。</li></ul> | [!DNL Google] では、機械学習を使用して「」を推定します[モデル化コンバージョン](https://support.google.com/google-ads/answer/10081327).」と入力します。 | 不可 |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analyticsのコンバージョントラッキング](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [EF ID フィードを使用したコンバージョントラッキング](/help/search-social-commerce/tracking/feed-efid.md)
>* [トランザクション ID フィードを使用したコンバージョントラッキング](/help/search-social-commerce/tracking/feed-transaction-id.md)
