---
title: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
description: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---

# 実装の前提条件と主な情報 [!DNL Analytics for Advertising]

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*

Adobe AnalyticsとAdobe Advertisingを統合する前に、次の情報を確認してください。

## でのレポートAdobe Advertisingデータの要件 [!DNL Analytics]

* 次のいずれかを実行します。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience CloudID サービス： `visitorAPI.js` バージョン 2.0 以降
* Adobe Analyticsの任意のバージョン ( [!DNL Prime], [!DNL Premium]または [!DNL Ultimate])
* ADOBE ANALYTICS: `appMeasurement.js` バージョン 2.1 以降

>[!TIP]
>
>データの正確性を向上させるには、各ライブラリの最新バージョンを使用します。

## Analytics セグメントをAdobe Advertisingと共有する際の要件

* Experience CloudID サービス： `visitorAPI.js` バージョン 2.1 以降
* ADOBE ANALYTICS: `appMeasurement.js` バージョン 1.8 以降

## 報告の要件 [!DNL Analytics] データのAdobe Advertising

以下をAdobe Advertising実装チームに提供します。

* The [!DNL Analytics] 有料メディアアクティビティのレポートや、Adobe Advertisingの最適化とレポートのためのサイトアクティビティのフィードに使用されるレポートスイート ID です。
* 会社のExperience Cloud組織 ID （組織 ID）。

これらの ID はどちらも [Adobe Experience Cloud Debugger の「概要」タブ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debuggerの概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] データのAdobe Advertising {#lookback-a4adc}

理由： [!DNL Analytics] レポートと最適化のためにデータがAdobe Advertisingに送信され、データは、Adobe Advertising内の広告主に対して設定されたインプレッションウィンドウやクリックルックバックウィンドウなどのアトリビューションルールに従います。

![Adobe Advertisingの広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising属性クリックのルックバックウィンドウ：最初のクリックが発生してからの日数で、クリックをコンバージョンに関連付けることができます。 デフォルトでは、この値は 60 日です。最大 90 日です
* Adobe Advertising属性インプレッションのルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる、広告インプレッションが発生してからの日数。 デフォルトでは、この値は 14 日です。最大 30 日です

  >[!NOTE]
  >
  > インプレッションのルックバックウィンドウはAdobe Advertisingに固有で、 [!DNL Analytics for Advertising]、レポート。

The [!DNL Analytics for Advertising] JavaScript では、これらの設定を使用して、ビュースルーエントリまたはクリックスルーエントリをサイトへの有効と見なすまでの距離を判断します。 ビュースルー数とクリックスルー数の決定方法について詳しくは、[Analytics で使用されるAdobe AdvertisingID](ids.md).&quot;

## Adobe Advertisingデータ [!DNL Analytics]

[!DNL Analytics] は、広告主の条件に従って、Analytics ヒット内のAdobe AdvertisingID(AMO ID) を設定します。 [!DNL eVar] 永続性設定。クリックスルーとビュースルーの両方に適用されます。 永続性設定はAdobe Advertisingのバックエンドで設定され、Adobeアカウントチームが変更できます。

* [!DNL Analytics for Advertising] [!DNL eVar] 有効期限：AMO ID のデフォルトで 60 日間

>[!NOTE]
>
>別の期間でデータをセグメント化するには、次の操作を実行します。 [カスタムセグメントの設定](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace内の様々なルックバックウィンドウを使用できます。

## サポートされる広告環境

* 検索
* 表示
* ビデオ
* オンラインビデオ
* ネイティブ

各チャネルでサポートされる最新のAdobe環境については、アドビの広告アカウントチームにお問い合わせください。

## 導入の前に知っておくべきこと

* Adobe Advertising実装チームが統合を設定します。

* この統合に対して追加のコストは請求されず、サーバー呼び出しによって追加の費用が発生することもありません。 [!DNL Analytics] またはAdobe Advertising料

* [!DNL Analytics for Advertising] が広告サーバーに依存しない：ビュースルーまたはクリックスルーは、どの広告サーバーからでも発生する場合があり、サイトへのエントリ時に適切な ID が生成されます。

* 統合が渡すのは [!DNL Analytics] 標準およびカスタムイベントを使用して、後続の有料メディアおよび広告活動の入札最適化にAdobe Advertising。 通り過ぎない [!DNL Analytics] セグメント、計算指標および [!DNL eVars] を入札の最適化用のAdobe Advertisingに追加します。

* Adobe Advertisingが内で永続 ID を作成する [!DNL Analytics] ユーザーがサイトに入る前にクリックまたは表示された最後の広告に基づき、 [クリックおよびビュースルーのルックバックウィンドウ](#lookback-a4adc) Adobe Advertisingで設定。 サイト訪問者がプロファイル内で両方のタイプのサイトエントリインタラクションをおこなう場合で、クリックがルックバック期間内の場合、訪問者のクリックスルー ID は、サイトレポートのビュースルー ID よりも優先されます。

* [!DNL Analytics for Advertising] Adobe Analyticsのコンバージョントラッキングでは、設定可能なトラッキングルックバックウィンドウが使用されます（デフォルトで 60 日間）。 Adobe Advertisingレポートは、このトラッキングルックバックウィンドウの終わりを通じてサイトのコンバージョンとエンゲージメントを反映しています。

* すべての広告タイプがサポートされています。 ただし、一部の広告環境がサポートされているわけではありません。

  例えば、接続された TV(CTV) 広告は、CTV でクリックが発生せず、同じデバイスでコンバージョンが発生しないので、追跡されません。 ただし、広告がデスクトップ環境内で表示される場合、一部のビュースルーサイトエントリデータが追跡される可能性があります。

* [!DNL Analytics] コンバージョンは現在追跡されており、同じデバイス上の訪問者にのみ関連付けられます。

* [!DNL Analytics for Advertising] では、アプリ内ビュースルーコンバージョンをサポートしていません。

* ビュースルートラッキングは、 [!DNL Analytics].

### 追加の ID

サイトにExperience CloudID サービスを実装すると、 [!DNL Analytics] またはAdobe Advertisingには追加の ID が含まれています。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、 [!DNL Analytics for Advertising] コンテンツを配信または目標指標を記録するアクティビティには、対応する [!DNL Analytics] 同じ追加の ID を共有するヒット。

を使用して [!DNL Analytics]に設定する場合は、 [!DNL Analytics] ヒット数。 Adobe Analytics の [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)を使用する場合、この ID は「Adobe Advertising」タブで `sdid` パラメーター。

>[!NOTE]
>
> この実装は、 [!DNL Analytics for Target] 統合とも呼ばれます。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [広告用 Analytics の JavaScript コード](/help/integrations/analytics/javascript.md)
