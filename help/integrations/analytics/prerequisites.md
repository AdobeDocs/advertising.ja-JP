---
title: 実装の前提条件と主な情報  [!DNL Analytics for Advertising]
description: 実装の前提条件と主な情報  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] を実装するための前提条件と主な情報

*Advertising DSP[!DNL Advertising Search, Social, & Commerce]* の広告主

Adobe AdvertisingをAdobe Analyticsと統合する前に、次の情報を確認してください。

## [!DNL Analytics] でAdobe Advertising データをレポートするための要件

* 次のいずれかになります。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud ID サービス：`visitorAPI.js` バージョン 2.0 以降
* あらゆるバージョンのAdobe Analytics（[!DNL Prime]、[!DNL Premium]、[!DNL Ultimate] を含む）
* Adobe Analytics:`appMeasurement.js` バージョン 2.1 以降
* （Advertising DSPのお客様） Web ページにデプロイされた [Advertising DSP JavaScript スニペット &#x200B;](javascript.md) で、ビュースルー訪問をトラッキングします。

>[!TIP]
>
>データの忠実性を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdobe Advertisingと共有するための要件

* Experience Cloud ID サービス：`visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics:`appMeasurement.js` バージョン 1.8 以降

## Adobe Advertisingで [!DNL Analytics] データをレポートするための要件

Adobe Advertising導入チームに次の情報を提供します。

* 有料メディアアクティビティのレポートと、Adobe Advertisingでの最適化とレポートのためのサイトアクティビティのフィードに使用する [!DNL Analytics] レポートスイート ID
* 会社のExperience Cloud組織 ID （組織 ID）。

これらの ID は両方とも、[Adobe Experience Cloud Debugger の「概要」タブ &#x200B;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) にあります。

![Experience Cloud Debugger の概要画面 &#x200B;](/help/integrations/assets/a4adc-debugger-summary.png)

## Adobe Advertisingでの [!DNL Analytics] Data {#lookback-a4adc}

レポート [!DNL Analytics] 最適化のためにデータがAdobe Advertisingに送信されるので、データは、Adobe Advertisingの広告主向けに設定されたインプレッションやクリックルックバックウィンドウを含むアトリビューションルールの対象となります。

![Adobe Advertisingでの広告主レベルのルックバックウィンドウの設定 &#x200B;](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising アトリビューションクリックのルックバックウィンドウ：クリックがコンバージョンに関連付けられる、最初のクリックが発生した後の日数。 デフォルトでは、この値は 60 日です（最大 90 日）
* Adobe Advertising アトリビューションインプレッションのルックバックウィンドウ：広告インプレッションが発生してから、インプレッションをコンバージョンに関連付けることができる日数です。 デフォルトでは、この値は 14 日です（最大 30 日）

  >[!NOTE]
  >
  > インプレッションのルックバックウィンドウは、レポートではなく、Adobe Advertisingに固有 [!DNL Analytics for Advertising] ものです。

[!DNL Analytics for Advertising] JavaScriptでは、これらの設定を使用して、サイトへのビュースルーエントリまたはクリックスルーエントリをどのくらい遡って有効と見なすかを決定します。 ビュースルーとクリックスルーが決定される方法について詳しくは、「[Analytics で使用されるAdobe Advertising ID](ids.md)」を参照してください。

## [!DNL Analytics] のAdobe Advertising データ

[!DNL Analytics] は、広告主の [!DNL eVar] 永続性設定に従って、Analytics ヒット内のAdobe Advertising ID （AMO ID）を設定します。これは、クリックスルーとビュースルーの両方に適用されます。 永続性設定はAdobe Advertising バックエンドで設定され、Adobe アカウントチームが変更できます。

* [!DNL Analytics for Advertising] [!DNL eVar] 有効期限：AMO ID の場合、デフォルトで 60 日

>[!NOTE]
>
>異なる時間枠のデータをセグメント化するには、Analysis Workspace内の異なるルックバックウィンドウで [&#x200B; カスタムセグメントを設定 &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) できます。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* 接続された TV
* ネイティブ

各チャネルでサポートされる最新の広告環境については、Adobe アカウントチームにお問い合わせください。

## 実装する前に知っておくべきこと

* Adobe Advertising導入チームが統合をセットアップします。

* この統合に関して追加のコストは請求されず、サーバーコールによって追加の [!DNL Analytics] 料やAdobe Advertising料金が発生することもありません。

* [!DNL Analytics for Advertising] れは、広告サーバーに依存しません。任意の広告サーバーからビュースルーまたはクリックスルーが発生する可能性があり、サイトエントリ時に適切な ID が生成されます。

* 統合では [!DNL Analytics] その後の有料メディアおよび広告の取り組みの入札最適化のために、標準およびカスタムイベントのみがAdobe Advertisingに渡されます。 入札最適化のために、[!DNL Analytics] セグメント、計算指標、[!DNL eVars] がAdobe Advertisingに渡されることはありません。

* Adobe Advertisingは、Adobe Advertisingで設定された [!DNL Analytics] クリックおよびビュースルールックバックウィンドウ [&#x200B; に基づいて、ユーザーがサイトに入る前にクリックまたは表示された最後の広告に基づいて、](#lookback-a4adc) 内に永続的な ID を作成します。 サイト訪問者のプロファイル内に両方のタイプのサイトエントリインタラクションがあり、クリックがルックバック期間内にある場合、訪問者のクリックスルー ID がサイトレポートのビュースルー ID を上書きします。

* Adobe Analyticsのコンバージョントラッキング [!DNL Analytics for Advertising]、設定可能なトラッキングルックバックウィンドウ（デフォルトでは 60 日）を使用します。 Adobe Advertising レポートは、このトラッキングルックバックウィンドウの最後までのサイトコンバージョンとエンゲージメントを反映します。

* すべての広告タイプがサポートされています。<!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] コンバージョンは現在追跡されており、同じデバイス上の 1 人の訪問者にのみ関連付けられています。

* [!DNL Analytics for Advertising] は、アプリ内ビュースルーコンバージョンをサポートしていません。

* [!DNL Analytics] のサーバーサイド転送の実装を使用している広告主では、ビュースルートラッキングはサポートされていません。

### 追加の ID

Experience Cloud ID サービスがサイトに実装されると、[!DNL Analytics] またはAdobe Advertisingのデータを含んだヒットには、追加の ID が含まれます。

例：`sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、コンテンツを配信したり目標指標を記録したりするために [!DNL Analytics for Advertising] アクティビティで使用されるすべてのAdobe Advertising呼び出しには、同じ追加 ID を共有する、対応する [!DNL Analytics] ヒットが必要です。

[!DNL Analytics] でのトラブルシューティングを行う場合は、[!DNL Analytics] のヒットに追加の ID が存在することを確認してください。 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) では、この ID が「Adobe Advertising」タブで `sdid` パラメーターとして表示されます。

>[!NOTE]
>
> この実装は、[!DNL Analytics for Target] 統合と同様に機能します。

>[!MORELIKETHIS]
>
>* [&#x200B; 概要  [!DNL Analytics for Advertising]](overview.md)
>* [Analytics for AdvertisingのJavaScript コード &#x200B;](/help/integrations/analytics/javascript.md)
