---
title: ' [!DNL Analytics for Advertising]を実装するための前提条件と主要情報'
description: ' [!DNL Analytics for Advertising]を実装するための前提条件と主要情報'
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
TQID: https://experienceleague.adobe.com/ZUROuxkhySqUbUOInKkdhgvmqJth3P-9-fVDHojrn34
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
source-git-commit: 074ca9f026dd75cffc0d7dbb2d3e1290aac3eaef
workflow-type: tm+mt
source-wordcount: 840
ht-degree: 0%

---

# [!DNL Analytics for Advertising]を実装するための前提条件と主要情報

*Advertising Creative、Advertising DSP、Advertising Search, Social, &amp; Commerceの広告主*

Adobe AdvertisingとAdobe Analyticsを統合する前に、次の情報を確認してください。

## [!DNL Analytics]でAdobe Advertising データをレポートするための要件

* 次のいずれかです。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` バージョン 2.0以降
* 任意のバージョンのAdobe Analytics （[!DNL Prime]、[!DNL Premium]または[!DNL Ultimate]を含む）
* Adobe Analytics: `appMeasurement.js` バージョン 2.1以降
* （Advertising DSPのお客様） ビュースルー訪問を追跡するために、web ページにデプロイされた[Advertising DSP JavaScript スニペット ](javascript.md)。

>[!TIP]
>
>データの品質を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdobe Advertisingと共有するための要件

* Experience Cloud Identity Service: `visitorAPI.js` バージョン 2.1以降
* Adobe Analytics: `appMeasurement.js` バージョン 1.8以降

## Adobe Advertisingで[!DNL Analytics] データをレポートするための要件

Adobe Advertising導入チームに以下を提供します。

* 有料メディアアクティビティのレポートと、Adobe Advertisingでの最適化とレポート作成のためのサイトアクティビティのフィードに使用する[!DNL Analytics] レポートスイート ID
* 会社のCX Enterprise Organization ID （組織ID）。

両方のIDは、Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)の「[概要」タブにあります。

![Experience Platform デバッガーの概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## Adobe Advertisingの[!DNL Analytics] データ {#lookback-a4adc}

[!DNL Analytics] データはレポートと最適化のためにAdobe Advertisingに送信されるため、データは、Adobe Advertisingの広告主向けに設定されたインプレッションとクリックのルックバックウィンドウを含むアトリビューションルールの対象となります。

Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)の![広告主レベルのルックバックウィンドウ設定

* Adobe Advertisingアトリビューションクリックのルックバックウィンドウ：最初のクリックが発生してからクリックがコンバージョンに起因する日数。 デフォルトでは、この値は60日です。最大は90日です
* Adobe Advertising アトリビューションインプレッションのルックバックウィンドウ：広告インプレッションが発生してから、インプレッションがコンバージョンに起因する可能性がある日数。 デフォルトでは、この値は14日です。最大は30日です

  >[!NOTE]
  >
  > インプレッションのルックバックウィンドウは、[!DNL Analytics for Advertising]ではなくAdobe Advertisingに固有です。

[!DNL Analytics for Advertising] JavaScriptでは、これらの設定を使用して、サイトへのビュースルーエントリまたはクリックスルーエントリを有効と見なす距離を決定します。 ビュースルーとクリックスルーの決定方法について詳しくは、「[Analyticsで使用されるAdobe Advertising ID](ids.md)」を参照してください。

## [!DNL Analytics]のAdobe Advertising データ

[!DNL Analytics]は、広告主の[!DNL eVar]の永続性設定に従って、Analytics ヒット内でAdobe Advertising ID （AMO ID）を設定します。この設定は、クリックスルーとビュースルーの両方に適用されます。 永続性設定はAdobe Advertising バックエンドで設定され、Adobe アカウントチームが変更できます。

* [!DNL Analytics for Advertising] [!DNL eVar]有効期限：AMO IDのデフォルトでは60日

>[!NOTE]
>
>異なる期間のデータをセグメント化するには、Analysis Workspace内で異なるルックバックウィンドウを使用して[ カスタムセグメント ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)を設定できます。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* コネクテッド TV
* ネイティブ

各チャネルでサポートされている最新の広告環境については、Adobe アカウントチームにお問い合わせください。

## 導入する前に把握しておくべきこと

* Adobe Advertising導入チームが連携の設定を行います。

* この統合に追加料金は請求されず、サーバー呼び出しによって[!DNL Analytics]またはAdobe Advertisingの追加料金が発生することもありません。

* [!DNL Analytics for Advertising]は広告サーバーに依存しません。任意の広告サーバーからビュースルーまたはクリックスルーが発生する可能性があり、サイトの入力時に適切なIDが生成されます。

* この統合では、後続の有料メディアおよび広告施策の入札を最適化するために、[!DNL Analytics]件の標準イベントとカスタムイベントのみがAdobe Advertisingに渡されます。 入札最適化のために[!DNL Analytics] セグメント、計算指標、および[!DNL eVars]をAdobe Advertisingに渡しません。

* Adobe Advertisingは、Adobe Advertisingで設定された[ クリック&amp;ビュースルーのルックバックウィンドウ ](#lookback-a4adc)に基づいて、ユーザーがサイトに入る前に最後にクリックまたは閲覧した広告に基づいて、[!DNL Analytics]内に永続的IDを作成します。 サイト訪問者がプロファイル内で両方のタイプのサイト入力インタラクションを持ち、クリックがルックバック期間内である場合、訪問者のクリックスルーIDはサイトレポートのビュースルーIDを上書きします。

* Adobe Analyticsの[!DNL Analytics for Advertising] コンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウが使用されます（デフォルトでは60日）。 このトラッキングルックバックウィンドウの最後まで、Adobe Advertisingのレポートにはサイトコンバージョンとエンゲージメントが反映されています。

* あらゆる広告タイプに対応しています。<!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics]個のコンバージョンが現在追跡されており、同じデバイスの訪問者にのみ関連付けられています。

* [!DNL Analytics for Advertising]は、アプリ内ビュースルーコンバージョンをサポートしていません。

* [!DNL Analytics]のサーバーサイド転送実装を使用している広告主では、ビュースルー追跡はサポートされていません。

### 補足ID

Experience Cloud Identity Serviceがサイトに実装されると、[!DNL Analytics]またはAdobe Advertisingのデータを含むヒットには補足IDが含まれます。

例：`sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合を行うには、[!DNL Analytics for Advertising] アクティビティがコンテンツの配信または目標指標の記録に使用するすべてのAdobe Advertising呼び出しに、同じ補足IDを共有する対応する[!DNL Analytics] ヒットが必要です。

[!DNL Analytics]でトラブルシューティングを行う場合は、必ず[!DNL Analytics] ヒットの補足IDが存在することを確認してください。 [Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)では、このIDを「`sdid`」パラメーターとして「Adobe Advertising」タブに表示できます。

>[!NOTE]
>
> この実装は、[!DNL Analytics for Target]統合と同様に機能します。

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [Advertising向けAnalyticsのJavaScript コード ](/help/integrations/analytics/javascript.md)
