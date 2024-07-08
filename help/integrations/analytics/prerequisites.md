---
title: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
description: 実装の前提条件と主な情報 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# 実装の前提条件と主な情報 [!DNL Analytics for Advertising]

*Advertising DSP およびを使用する広告主[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising を Adobe Analytics と統合する前に、次の情報を確認してください。

## での Adobe Advertising データのレポートの要件 [!DNL Analytics]

* 次のいずれかになります。
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud IDサービス サービス: `visitorAPI.js` バージョン 2.0 以降
* Adobe Analytics のすべてのバージョン( [!DNL Prime]、 [!DNL Premium]、 [!DNL Ultimate] を含む)
* Adobe Analytics: `appMeasurement.js` バージョン 2.1 以降
* (顧客DSP広告) [広告DSP JavaScriptスニペット](javascript.md) を Web ページに導入し、表示スルー訪問を追跡します。

>[!TIP]
>
>データ会員ステータスを向上させるには、各ライブラリの最新バージョンを使用してください。

## Analyticsセグメントを Adobe Systems Advertising と共有するための要件

* Experience Cloud IDサービス サービス: `visitorAPI.js` バージョン 2.1 以降
* Adobe Analytics: `appMeasurement.js` バージョン 1.8 以降

## Adobe Systems広告における [!DNL Analytics] データの報告の要件

以下の情報を Adobe Systems Advertising 実装 チームに提供します。

* この [!DNL Analytics] 有料メディアアクティビティのレポートと、Adobe Advertising での最適化とレポートのためのサイトアクティビティのフィードに使用するレポートスイート ID
* 会社の Experience Cloud 組織 ID （組織 ID）。

これらの ID は両方とも [Adobe Experience Cloud デバッガーの「概要」タブ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloudデバッガ概要画面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe Systems広告データ {#lookback-a4adc}

[!DNL Analytics]データはレポートと最適化のために Adobe Systems Advertising に送信されるため、データは Adobe Systems Advertising の広告主用に設定されたインプレッションウィンドウやクリックルックバックウィンドウなど、属性ルールの対象となります。

![adobe Advertising の広告主レベルのルックバックウィンドウ設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising アトリビューションクリックのルックバックウィンドウ：クリックがコンバージョンに関連付けられる、最初のクリックが発生してからの日数。 デフォルトでは、この値は 60 日です（最大 90 日）
* Adobe Advertising アトリビューションインプレッションルックバックウィンドウ：インプレッションがコンバージョンに関連付けられる、広告インプレッション発生後の日数です。 デフォルトでは、この値は 14 日です（最大 30 日）

  >[!NOTE]
  >
  > インプレッションルックバックウィンドウは、Adobe Advertising に固有のものではありません [!DNL Analytics for Advertising]、レポート。

[!DNL Analytics for Advertising] JavaScriptは、これらの設定を使用して、サイトへの表示スルー エントリまたはクリックスルー エントリを有効と見なす期間を決定します。表示スルー数とクリックスルー数の決定方法について詳しくは、「Analytics](ids.md)を使用する広告 ID [Adobe Systems」を参照してください。

## Adobe Systems での広告データ [!DNL Analytics]

[!DNL Analytics] は、クリックスルーと表示スルーの両方に適用される広告主の [!DNL eVar] 持続性設定に従い、Analytics ヒット内の広告 ID(AMO ID)Adobe Systemsを設定します。 永続性設定は Adobe Systems Advertising バックエンドで構成され、Adobe Systems アカウントチームが変更できます。

* [!DNL Analytics for Advertising][!DNL eVar] 有効期限:AMO ID のデフォルトは 60 日

>[!NOTE]
>
>異なる期間のデータセグメントには、Analysis Workspace内の異なるルックバックウィンドウで [カスタムセグメントを設定](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) できます。

## サポートされている広告環境

* 捜索
* 陳列
* ビデオ
* オンラインビデオ
* 接続された TV
* ネイティブ

各チャネルでサポートされる最新の広告環境については、アドビアカウントチームにお問い合わせください。

## 導入の前に知っておくべきこと

* Adobe Systems Advertising 実装 チーム により、統合が設定されます。

* この統合に追加費用は請求されず、サーバーコールによって追加の [!DNL Analytics] やAdobe Systems広告料金が発生することもありません。

* [!DNL Analytics for Advertising] 広告サーバーに依存しない:表示スルーまたはクリックスルーはどの広告サーバーからでも発生し、サイトに入ると適切な ID が生成されます。

* この統合では [!DNL Analytics] 標準イベントとカスタムイベントのみが Adobe Systems Advertising に渡され入札後続の有料メディアおよび広告活動の最適化が行われます。 セグメント、計算指標、[!DNL eVars][!DNL Analytics]、入札最適化のために Adobe Systems Advertising に渡されることはありません。

* Adobe Systems Advertising は、Adobe Systems Advertising で設定された [クリック ウィンドウと表示スルー ルックバック ウィンドウ](#lookback-a4adc)に基づいて、ユーザーがサイトに入る前に最後にクリックまたは表示された広告に基づいて、[!DNL Analytics]内に永続的な ID を作成します。サイト訪問者プロファイル内に両方のタイプのサイトエントリインタラクションがあり、クリックがルックバック期間内である場合、訪問者のクリックスルーIDはサイトレポートの表示スルーIDよりも優先されます。

* [!DNL Analytics for Advertising] Adobe Analytics の コンバージョン トラッキング では、設定可能な トラッキング ルックバックウィンドウ(デフォルトでは 60 日間)が使用されます。 Adobe Systems広告レポートは、このトラッキングルックバックウィンドウの終わりまで、サイトのコンバージョンとエンゲージメントを反映します。

* すべてを選択 広告タイプがサポートされています。 ただし、すべての広告環境がサポートされているわけではありません。

* [!DNL Analytics] コンバージョンは現在トラッキングされ、同じデバイス上の訪問者にのみ結び付けられます。

* [!DNL Analytics for Advertising] アプリ内表示スルー コンバージョンには対応していません。

* 表示経由トラッキングは、 [!DNL Analytics]のサーバーサイド転送実装を使用している広告主様には対応していません。

### 追加の ID

サイトに Experience Cloud ID サービスを実装すると、からのデータを含んだヒットが発生します [!DNL Analytics] または Adobe Advertising に追加の ID が含まれている場合。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

正確なデータ統合のために、すべての Adobe Advertising 呼び出しは、 [!DNL Analytics for Advertising] コンテンツを配信するか、目標指標を記録するアクティビティには、対応する指標が必要です [!DNL Analytics] 同じ追加 ID を共有するヒット。

でトラブルシューティングを行う場合 [!DNL Analytics]に追加の ID が存在することを確認してください [!DNL Analytics] ヒット。 が含まれる [Adobe Experience Cloud デバッガー](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)この ID は、「Adobe Advertising」タブでとして表示されます `sdid` パラメーター。

>[!NOTE]
>
> この実装は、 [!DNL Analytics for Target] 統合と同様に機能します。

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [Analytics for Advertising 用 JavaScript コード](/help/integrations/analytics/javascript.md)
