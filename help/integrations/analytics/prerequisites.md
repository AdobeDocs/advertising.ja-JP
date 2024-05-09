---
title: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
description: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# 実装の前提条件と主な情報 [!DNL Analytics for Advertising]

*Advertising DSPを使用した広告主[!DNL Advertising Search, Social, & Commerce]*

Adobe AdvertisingをAdobe Analyticsと統合する前に、次の情報を確認してください。

## でのAdobe Advertisingデータのレポートの要件 [!DNL Analytics]

* 次のいずれかになります。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud ID サービス： `visitorAPI.js` バージョン 2.0 以降
* あらゆるバージョンのAdobe Analytics（以下を含む） [!DNL Prime], [!DNL Premium]、または [!DNL Ultimate]）
* Adobe Analytics: `appMeasurement.js` バージョン 2.1 以降
* （Advertising DSPのお客様） [Advertising DSP JavaScript スニペット](javascript.md) web ページにデプロイして、ビュースルー訪問を追跡します。

>[!TIP]
>
>データの忠実性を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdobe Advertisingと共有するための要件

* Experience Cloud ID サービス： `visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics: `appMeasurement.js` バージョン 1.8 以降

## 報告要件 [!DNL Analytics] Adobe Advertising内のデータ

Adobe Advertising導入チームに以下を提供します。

* この [!DNL Analytics] 有料メディアアクティビティに関するレポートおよびAdobe Advertisingの最適化とレポートのためにサイトアクティビティのフィードに使用するレポートスイート ID
* 会社のExperience Cloud組織 ID （組織 ID）。

これらの ID は両方とも [Adobe Experience Cloud Debugger の「概要」タブ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debuggerの概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe Advertising内のデータ {#lookback-a4adc}

なぜなら [!DNL Analytics] レポートと最適化のためにデータがAdobe Advertisingに送信されます。データは、Adobe Advertisingの広告主向けに設定されたインプレッションやクリックルックバックウィンドウなどのアトリビューションルールの対象となります。

![Adobe Advertisingの広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertisingアトリビューションクリックのルックバックウィンドウ：クリックがコンバージョンに関連付けられる、最初のクリックが発生した後の日数。 デフォルトでは、この値は 60 日です（最大 90 日）
* Adobe Advertisingアトリビューションインプレッションルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる、広告インプレッションが発生してからの日数です。 デフォルトでは、この値は 14 日です（最大 30 日）

  >[!NOTE]
  >
  > インプレッションルックバックウィンドウは、Adobe Advertisingに固有のものではありません [!DNL Analytics for Advertising]、レポート。

この [!DNL Analytics for Advertising] JavaScript は、これらの設定を使用して、サイトへのビュースルーエントリまたはクリックスルーエントリを有効と見なすまでの遡りを決定します。 ビュースルーとクリックスルーの決定方法について詳しくは、「」を参照してください[Analytics が使用するAdobe Advertising ID](ids.md).」と入力します。

## Adobe Advertisingデータ： [!DNL Analytics]

[!DNL Analytics] は、Analytics ヒット内のAdobe AdvertisingID （AMO ID）を、広告主の [!DNL eVar] 永続性設定。クリックスルーとビュースルーの両方に適用されます。 永続性設定は、Adobe Advertisingのバックエンドで設定され、Adobeアカウントチームが変更できます。

* [!DNL Analytics for Advertising] [!DNL eVar] 有効期限：AMO ID のデフォルトは 60 日

>[!NOTE]
>
>別の時間枠のデータをセグメント化するには、次の操作を実行します [カスタムセグメントの設定](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace内の様々なルックバックウィンドウを使用する場合。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* ネイティブ

各チャンネルでサポートされている最新のAdobe環境については、広告アカウントチームにお問い合わせください。

## 実装する前に知っておくべきこと

* Adobe Advertising導入チームが連携をセットアップします。

* この統合に追加のコストは請求されず、サーバーコールによって追加のコストが発生することもありません [!DNL Analytics] またはAdobe Advertising料。

* [!DNL Analytics for Advertising] 広告サーバーに依存しない：任意の広告サーバーからビュースルーまたはクリックスルーが発生する可能性があり、サイトエントリ時に適切な ID が生成されます。

* 統合は成功するだけです [!DNL Analytics] その後の有料メディアおよび広告の取り組みの入札最適化のためにAdobe Advertisingにする標準およびカスタムイベント。 通過しません [!DNL Analytics] セグメント、計算指標および [!DNL eVars] 入札最適化のためのAdobe Advertisingを行う。

* Adobe Advertisingが内に永続 ID を作成する [!DNL Analytics] ユーザーがサイトに入る前にクリックまたは表示された最後の広告に基づきます（ [クリックしてビュースルールックバックウィンドウ](#lookback-a4adc) Adobe Advertisingで設定済み。 サイト訪問者のプロファイル内に両方のタイプのサイトエントリインタラクションがあり、クリックがルックバック期間内にある場合、訪問者のクリックスルー ID がサイトレポートのビュースルー ID を上書きします。

* [!DNL Analytics for Advertising] Adobe Analyticsのコンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウ（デフォルトでは 60 日）を使用します。 Adobe Advertisingレポートは、このトラッキングルックバックウィンドウの最後までのサイトコンバージョンとエンゲージメントを反映します。

* すべての広告タイプがサポートされています。 ただし、すべての広告環境がサポートされているわけではありません。

  例えば、接続された TV （CTV）広告は、CTV ではクリックが発生せず、同じデバイスではコンバージョンが発生しないので、追跡されません。 ただし、広告をデスクトップ環境内で表示した場合は、一部のビュースルーサイトエントリデータがトラッキングされる可能性があります。

* [!DNL Analytics] コンバージョンは現在追跡されており、同じデバイス上の 1 人の訪問者にのみ関連付けられています。

* [!DNL Analytics for Advertising] は、アプリ内ビュースルーコンバージョンをサポートしていません。

* のサーバーサイド転送の実装を使用している広告主には、ビュースルートラッキングはサポートされていません [!DNL Analytics].

### 追加の ID

サイトにExperience Cloud ID サービスを実装すると、のデータを含んだヒットが発生します [!DNL Analytics] またはAdobe Advertisingに追加の ID が含まれています。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、によって使用されるすべてのAdobe Advertising呼び出し [!DNL Analytics for Advertising] コンテンツを配信するか、目標指標を記録するアクティビティには、対応する指標が必要です [!DNL Analytics] 同じ追加 ID を共有するヒット。

でトラブルシューティングを行う場合 [!DNL Analytics]に追加の ID が存在することを確認してください [!DNL Analytics] ヒット。 が含まれる [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)この ID は、「Adobe Advertising」タブで、として表示されます `sdid` パラメーター。

>[!NOTE]
>
> この実装は、と同様に機能します。 [!DNL Analytics for Target] 統合。

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [Analytics for Advertising 用 JavaScript コード](/help/integrations/analytics/javascript.md)
