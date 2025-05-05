---
title: 実装の前提条件と主な情報  [!DNL Analytics for Advertising]
description: 実装の前提条件と主な情報  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] を実装するための前提条件と主な情報

*Advertising DSP[!DNL Advertising Search, Social, & Commerce]* の広告主

Adobe AdvertisingをAdobe Analyticsと統合する前に、次の情報を確認してください。

## [!DNL Analytics] でのAdobe Advertisingデータのレポートの要件

* 次のいずれかになります。
   * Adobe Experience Platform Web SDK:`alloy.js`
   * Experience Cloud ID サービス：`visitorAPI.js` バージョン 2.0 以降
* あらゆるバージョンのAdobe Analytics（[!DNL Prime]、[!DNL Premium]、[!DNL Ultimate] を含む）
* Adobe Analytics:`appMeasurement.js` バージョン 2.1 以降
* （Advertising DSPのお客様） Web ページにデプロイされた [Advertising DSP JavaScript スニペット ](javascript.md) で、ビュースルー訪問をトラッキングします。

>[!TIP]
>
>データの忠実性を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdobe Advertisingと共有するための要件

* Experience Cloud ID サービス：`visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics:`appMeasurement.js` バージョン 1.8 以降

## Adobe Advertisingにおける [!DNL Analytics] データのレポートの要件

Adobe Advertising導入チームに以下を提供します。

* 有料メディアアクティビティに関するレポートおよびAdobe Advertisingでの最適化とレポートのためにサイトアクティビティのフィードに使用する [!DNL Analytics] レポートスイート ID
* 会社のExperience Cloud組織 ID （組織 ID）。

これらの ID は両方とも、[Adobe Experience Cloud Debugger の「概要」タブ ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=ja) にあります。

![Experience Cloud Debuggerの概要画面 ](/help/integrations/assets/a4adc-debugger-summary.png)

## Adobe Advertising内の [!DNL Analytics] データ {#lookback-a4adc}

レポ [!DNL Analytics] トと最適化のためにデータがAdobe Advertisingに送信されるので、データは、Adobe Advertisingの広告主向けに設定されたインプレッションウィンドウやクリックルックバックウィンドウなどのアトリビューションルールの対象となります。

![Adobe Advertisingでの広告主レベルのルックバックウィンドウ設定 ](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertisingアトリビューションクリックのルックバックウィンドウ：クリックがコンバージョンに関連付けられる、最初のクリックが発生した後の日数。 デフォルトでは、この値は 60 日です（最大 90 日）
* Adobe Advertisingアトリビューションインプレッションルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる、広告インプレッションが発生してからの日数です。 デフォルトでは、この値は 14 日です（最大 30 日）

  >[!NOTE]
  >
  > インプレッションのルックバックウィンドウは、レポートではなく、Adobe Advertisingに固有 [!DNL Analytics for Advertising] す。

[!DNL Analytics for Advertising] JavaScriptでは、これらの設定を使用して、サイトへのビュースルーエントリまたはクリックスルーエントリをどのくらい遡って有効と見なすかを決定します。 ビュースルーおよびクリックスルーが決定される方法について詳しくは、「[Analytics が使用するAdobe AdvertisingID](ids.md)」を参照してください。

## [!DNL Analytics] のAdobe Advertisingデータ

[!DNL Analytics] は、Adobe Advertising主の [!DNL eVar] 永続性設定に従って、Analytics ヒット内の広告 ID （AMO ID）を設定します。これは、クリックスルーとビュースルーの両方に適用されます。 永続性設定は、Adobe Advertisingのバックエンドで設定され、Adobeアカウントチームが変更できます。

* [!DNL Analytics for Advertising] [!DNL eVar] 有効期限：AMO ID の場合、デフォルトで 60 日

>[!NOTE]
>
>異なる時間枠のデータをセグメント化するには、Analysis Workspace内の異なるルックバックウィンドウで [ カスタムセグメントを設定 ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=ja) できます。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* 接続された TV
* ネイティブ

各チャンネルでサポートされている最新のAdobe環境については、広告アカウントチームにお問い合わせください。

## 実装する前に知っておくべきこと

* Adobe Advertising導入チームが連携を設定します。

* この統合に関して追加コストは請求されません。また、サーバーコールによって追加の [!DNL Analytics] ールやAdobe Advertising料金が発生することはありません。

* [!DNL Analytics for Advertising] れは、広告サーバーに依存しません。任意の広告サーバーからビュースルーまたはクリックスルーが発生する可能性があり、サイトエントリ時に適切な ID が生成されます。

* 統合では、その後の有料メディア [!DNL Analytics] 広告活動の入札最適化のために、標準イベントとカスタムイベントのみがAdobe Advertisingに渡されます。 入札最適化のために、[!DNL Analytics] セグメント、計算指標、[!DNL eVars] がAdobe Advertisingに渡されることはありません。

* Adobe Advertisingは、Adobe Advertisingで設定された [ クリックおよびビュースルールックバックウィンドウ ](#lookback-a4adc) に基づいて、サイトに入る前にクリックまたは表示された最後の広告に基づいて、[!DNL Analytics] 内に永続的な ID を作成します。 サイト訪問者のプロファイル内に両方のタイプのサイトエントリインタラクションがあり、クリックがルックバック期間内にある場合、訪問者のクリックスルー ID がサイトレポートのビュースルー ID を上書きします。

* Adobe Analyticsのコンバージョントラッキング [!DNL Analytics for Advertising]、設定可能なトラッキングルックバックウィンドウ（デフォルトでは 60 日）を使用します。 Adobe Advertisingレポートは、このトラッキングルックバックウィンドウの最後までのサイトコンバージョンとエンゲージメントを反映します。

* すべての広告タイプがサポートされています。<!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] コンバージョンは現在追跡されており、同じデバイス上の 1 人の訪問者にのみ関連付けられています。

* [!DNL Analytics for Advertising] は、アプリ内ビュースルーコンバージョンをサポートしていません。

* [!DNL Analytics] のサーバーサイド転送の実装を使用している広告主では、ビュースルートラッキングはサポートされていません。

### 追加の ID

Experience Cloud ID サービスがサイトに実装されると、[!DNL Analytics] またはAdobe Advertisingのデータを含んだヒットには、追加の ID が含まれます。

例：`sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、コンテンツを配信したり目標指標を記録したりするために [!DNL Analytics for Advertising] アクティビティで使用されるすべてのAdobe Advertising呼び出しには、同じ追加 ID を共有する、対応する [!DNL Analytics] ヒットが必要です。

[!DNL Analytics] でのトラブルシューティングを行う場合は、[!DNL Analytics] のヒットに追加の ID が存在することを確認してください。 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=ja) では、この ID が「Adobe Advertising」タブに `sdid` パラメーターとして表示されます。

>[!NOTE]
>
> この実装は、[!DNL Analytics for Target] 統合と同様に機能します。

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [Analytics for AdvertisingのJavaScript コード ](/help/integrations/analytics/javascript.md)
