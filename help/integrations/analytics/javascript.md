---
title: ' [!DNL Analytics for Advertising] のJavaScript コード'
description: ' [!DNL Analytics for Advertising] のJavaScript コード'
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] のJavaScript コード

*Advertising DSPのみの広告主*

Advertising DSPの場合、[!DNL Analytics for Advertising] 統合は、ビュースルーおよびクリックスルーサイトのインタラクションを追跡します。 クリックスルーの訪問は、web ページ上で標準のAdobe Analytics コードによってトラッキングされます。[!DNL Analytics] コードは、ランディングページの URL にある AMO ID および EF ID パラメーターをキャプチャし、それぞれの予約済み [!DNL eVars] でトラッキングします。 Web ページにJavaScript スニペットをデプロイすることで、ビュースルーの訪問をトラッキングできます。

サイトへの訪問の最初のページビューで、Adobe AdvertisingのJavaScript コードが、訪問者が以前に広告を表示またはクリックしたかどうかを確認します。 ユーザーがクリックスルーから以前にサイトに入った場合や、広告を表示していない場合、訪問者は無視されます。 訪問者が広告を表示し、Adobe Advertising内に設定された [ クリックルックバックウィンドウ ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) の間にクリックスルーからサイトに入っていない場合、Adobe AdvertisingのJavaScript コードは、a） [Experience CloudID サービスを使用して追加の ID を生成する（`SDID`） ](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja) または b） Adobe Experience Platform [!DNL Web SDK] `generateRandomID` メソッドを使用して `[!DNL StitchID]` を生成します。 どちらの ID を使用しても、Adobe Advertisingから訪問者のAdobe Analytics ヒットにデータが結び付けられます。 次に、Adobe Analyticsは、広告公開に関連付けられた AMO ID および EF ID のAdobe Advertisingに対してクエリを実行します。 次に、AMO ID と EF ID がそれぞれの [!DNL eVars] に入力されます。 これらの値は、指定した期間（デフォルトでは 60 日）保持されます。

[!DNL Analytics] は、EF ID をキーとして使用して、サイトトラフィック指標（ページビュー数、訪問回数、滞在時間など）および [!DNL Analytics] のカスタムイベントまたは標準イベントを 1 時間ごとにAdobe Advertisingに送信します。 これらの [!DNL Analytics] 指標は、コンバージョンのアトリビューションシステムを通じて実行され、Adobe Advertisingをクリック数と公開数の履歴に結び付けます。

>[!NOTE]
>
>Adobe Advertising JavaScriptのトラッキングロジックはAdobe側で行われるので、ページ読み込み時間にはほとんど影響しません。
>
>これに対し、Advertising DSPでは [!DNL DCM] コネクタのロジックは [!DNL Analytics] （[!DNL Google Campaign Manager 360] を使用）に対してクライアント側で行われます。 クライアントサイドでステッチすると、ページの読み込みが遅くなり、データ損失のリスクが高くなります。 これは、[!DNL Analytics] JavaScriptが ping を実行し、[!DNL DoubleClick] が最後のクリックまたはインプレッション [!DNL DoubleClick] ータを [!DNL Analytics] に返すのを待つ必要があるために発生します。 [!DNL DSP] チームが [!DNL DCM] データコネクタを設定する際に、ページを遅らせる時間を指定する必要があります。

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## JavaScript コードのデプロイ

JavaScript ライブラリは、[!DNL Analytics] とAdobe Advertisingが相互に通信できる 2 行で構成されています。 Adobe Advertisingの実装中に [!DNL Analytics for Advertising] 統合が完了した場合は、このコードを既に受け取っていて、デプロイ方法の手順を示しているはずです。

### コード

#### Experience Cloud ID サービスの `visitorAPI.js` コードを使用する実装

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### `alloy.js` コードのExperience Platformを使用 [!DNL Web SDK] る実装

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### コードの配置場所

[!DNL Analytics for Advertising] JavaScript関数は、Experience CloudID サービスの後、Analytics アプリ測定コードの前に配置する必要があります。 これにより、追加の ID （`SDID`）または `[!DNL StitchID]` が Analytics 呼び出しに含まれるようになります。

![ コード配置 ](/help/integrations/assets/a4adc-code-placement.png)

### コードのデプロイメントの検証

以下に示すように、Adobe Advertisingに送信されるリクエストと [!DNL Analytics] に送信されるリクエストの間で 4 つの ID の値を比較することで、任意のパケットスニファータイプのツール（[!DNL Charles]、[!DNL Fiddler]、[!DNL Chrome Developer Tools] など）を使用して検証を実行できます。

#### [!DNL Chrome Developer Tools] でコードを確認する方法 {#validate-js-chrome}

1. [!DNL Chrome Developer Tools] を開いて「**ネットワーク**」タブをクリックします。

1. [!DNL Analytics for Advertising] JavaScriptを含む web サイトページを読み込みます。

1. 「[!UICONTROL Network]」タブを `last` でフィルタリングし、2 つの行を確認します。

   ![ 前回のフィルタリング ](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 最初の行はJavaScript ライブラリの呼び出しで、タイトルは `last-event-tag-latest.min.js` です。
   * 2 行目は、リクエストをAdobe Advertisingに送信する呼び出しです。 `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]` の手順で開始します。

     コールトゥAdobe Advertisingが表示されない場合は、訪問の最初のページビューではない可能性があります。 テストの目的で、cookie を削除して、対応する訪問の最初のページビューが次の呼び出しになるようにすることができます。

   1. 「アプリケーション」タブで `adcloud` Cookie を検索し、値が `y` で UTC エポックタイムスタンプが 30 分で期限切れになる `_les_v` （最終訪問）が Cookie に含まれていることを確認します。
      1. `adcloud` の Cookie を削除してページを更新します。

1. （Experience Cloud ID サービスの `visitorAPI.js` コードを使用する実装） `/b/ss` でフィルタリングして、Analytics ヒットを確認します。

   ![`/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png) のフィルタリング

1. （Edge Networkへのリクエストペイロードに `advertisingStitchID` が含まれていることを確認するために `/interact` のExperience Platform[!DNL Web SDK] コード `alloy.js` フィルターを使用する実装。

   ![`/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png) のフィルタリング

1. 2 つのヒット間の ID 値を比較します。 Analytics ヒットのレポートスイート ID （`/b/ss/` の直後の URL パス）を除き、すべての値はクエリ文字列パラメーターに含める必要があります。

   | ID | Analytics パラメーター | Edge Network | Adobe Advertisingパラメーター |
   | --- | --- | --- | --- |
   | Experience CloudIMS 組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 追加データ ID | sdid |  | `_les_sdid` |
   | ステッチ ID | stitchId | `_adcloud` プロパティの下の `advertisingStitchID` |  |
   | Analytics レポートスイート | `/b/ss/` の後の値 | | `_les_rsid` |
   | Experience Cloud訪問者 ID | mid |  | `_les_mid` |

   ID 値が一致する場合は、JavaScriptの実装が確認されます。 Adobe Advertisingは、クリックスルーまたはビュースルートラッキングの詳細（存在する場合）を [!DNL Analytics] サーバーに送信します。

#### [!DNL Adobe Experience Cloud Debugger] でコードを確認する方法

1. ホームページで [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=ja) を開きます。
1. 「[!UICONTROL Network]」タブに移動します。
1. [!UICONTROL Solutions Filter] のツールバーで、「[!UICONTROL Adobe Advertising]」をクリックし、「[!UICONTROL Analytics]」をクリックします。
1. [!UICONTROL Request URL - Hostname] パラメーター行で、`lasteventf-tm.everesttech.net` を見つけます。
1. [!UICONTROL Request - Parameters] の行で、「コードの確認方法 [ の手順 3 と同様に、生成されたシグナルを監査  [!DNL Chrome Developer Tools]](#validate-js-chrome) ます。
   * （Experience Cloud ID サービス `visitorAPI.js` コードを使用する実装） `Sdid` パラメーターがAdobe Analytics フィルターの `Supplemental Data ID` と一致していることを確認します。
   * （Experience Platform[!DNL Web SDK] コード `alloy.js` を使用する実装。`advertisingStitchID` パラメーターの値が、Experience PlatformEdge Networkに送信される `Sdid` と一致していることを確認します。
   * コードが生成されない場合は、「[!UICONTROL Application]」タブでAdobe Advertising cookie が削除されていることを確認します。 削除したら、ページを更新して手順を繰り返します。

   ![[!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png) でのJavaScript コード [!DNL Analytics for Advertising] 監査

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [ 実装の前提条件と主な情報  [!DNL Analytics for Advertising]](prerequisites.md)
