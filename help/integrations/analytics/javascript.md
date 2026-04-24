---
title: ' [!DNL Analytics for Advertising]のJavaScript コード'
description: ' [!DNL Analytics for Advertising]のJavaScript コード'
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
TQID: https://experienceleague.adobe.com/g9onwe1IQl1kbyQ82W2KmODPGUAReKiotxy65yCZcNY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 941
ht-degree: 0%

---

# [!DNL Analytics for Advertising]のJavaScript コード

*Advertising DSPのみの広告主*

Advertising DSPの場合、[!DNL Analytics for Advertising]統合は、ビュースルーとクリックスルーのサイトインタラクションを追跡します。 クリックスルー訪問は、web ページ上の標準のAdobe Analytics コードによって追跡されます。[!DNL Analytics] コードは、ランディングページ URLのAMO IDおよびEF ID パラメーターをキャプチャし、それぞれの予約[!DNL eVars]で追跡します。 JavaScriptスニペットをweb ページにデプロイすることで、ビュースルー訪問を追跡できます。

Adobe Advertising JavaScriptのコードにより、サイトへの訪問の最初のページビューで、訪問者が以前に広告を見たりクリックしたりしたことがあるかどうかを確認します。 ユーザーがクリックスルーでサイトにアクセスしたことがある、広告が表示されていない場合、訪問者は無視されます。 Adobe Advertising内で設定された[&#x200B; クリックルックバックウィンドウ &#x200B;](/help/integrations/analytics/prerequisites.md#lookback-a4adc)の間に、訪問者が広告を見てクリックスルーでサイトに入っていない場合、Adobe Advertising JavaScript コードは、a）が[Experience Cloud ID サービス &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)を使用して追加ID （`SDID`）を生成するか、b）がAdobe Experience Platform [!DNL Web SDK] `generateRandomID` メソッドを使用して`[!DNL StitchID]`を生成します。 どちらのIDも、Adobe Advertisingから訪問者のAdobe Analytics ヒットにデータを合成するために使用されます。 次に、Adobe AnalyticsはAdobe Advertisingに対して、広告露出に関連付けられたAMO IDとEF IDを問い合わせます。 次に、AMO IDとEF IDがそれぞれの[!DNL eVars]に入力されます。 これらの値は、指定した期間（デフォルトでは60日）保持されます。

[!DNL Analytics]は、EF IDをキーとして使用して、サイトトラフィック指標（ページビュー、訪問数、滞在時間など）と[!DNL Analytics]個のカスタムイベントまたは標準イベントをAdobe Advertisingに毎時送信します。 これらの[!DNL Analytics]指標は、Adobe Advertisingアトリビューションシステムを通じて実行され、コンバージョンをクリック履歴や露出の履歴に結び付けます。

>[!NOTE]
>
>Adobe Advertising JavaScriptのトラッキングロジックはAdobe側で実行されるため、ページの読み込み時間にほとんど影響しません。
>
>対照的に、Advertising DSPの[!DNL DCM] データコネクタの[!DNL Analytics]へのロジック（[!DNL Google Campaign Manager 360]を使用）は、クライアント側で実行されます。 クライアント側でステッチングをおこなうと、ページの読み込みが遅くなり、データが失われるリスクが高まります。 これは、[!DNL Analytics] JavaScriptが[!DNL DoubleClick]にpingを送信し、[!DNL DoubleClick]が最後のクリック/インプレッションデータを[!DNL Analytics]に返すのを待つ必要があるために発生します。 [!DNL DSP] チームが[!DNL DCM] データコネクタを設定する際は、ページを遅延させる期間を指定する必要があります。

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

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

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5's technical team will provide a unique tag for your organization to implement on your webpages.
-->

## JavaScript コードのデプロイ

JavaScript ライブラリは、[!DNL Analytics]とAdobe Advertisingが互いに通信できる2行で構成されています。 Adobe Advertisingの実装中に[!DNL Analytics for Advertising]統合が完了した場合は、このコードを既に受け取っている必要があります。このコードには、デプロイ方法に関する説明が記載されています。

### コード

#### Experience Cloud Identity Service `visitorAPI.js` コードを使用する実装

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Experience Platform [!DNL Web SDK] `alloy.js` コードを使用する実装

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### コードを配置する場所

[!DNL Analytics for Advertising] JavaScript関数は、Experience Cloud ID サービスの後で、Analytics アプリ測定コードの前に指定する必要があります。 これにより、補足ID （`SDID`）または`[!DNL StitchID]`がAnalytics呼び出しに含まれるようになります。

![&#x200B; コード プレースメント &#x200B;](/help/integrations/assets/a4adc-code-placement.png)

### コード展開の検証

任意のパケットスニファの種類のツール（[!DNL Charles]、[!DNL Fiddler]、[!DNL Chrome Developer Tools]など）を使用して検証を実行するには、次に示すように、Adobe Advertisingに送信するリクエストと[!DNL Analytics]に送信するリクエストの4つのIDの値を比較します。

#### [!DNL Chrome Developer Tools]でコードを確認する方法 {#validate-js-chrome}

1. [!DNL Chrome Developer Tools]を開き、「**ネットワーク**」タブをクリックします。

1. [!DNL Analytics for Advertising] JavaScriptを含むweb サイト ページを読み込みます。

1. [!UICONTROL Network] タブを`last`でフィルタリングし、2行を確認します。

   ![最後の](/help/integrations/assets/a4adc-code-validation-filter-last.png)にフィルターを実行しています

   * 最初の行はJavaScript ライブラリへの呼び出しであり、タイトルは`last-event-tag-latest.min.js`です。
   * 2行目は、Adobe Advertisingにリクエストを送信する呼び出しです。 次のように始まります：`_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Adobe Advertisingへの呼び出しが表示されない場合は、訪問の最初のページビューではない可能性があります。 テストの目的で、次の呼び出しが対応する訪問の最初のページビューになるように、Cookieを削除できます。

   1. 「アプリケーション」タブで、`adcloud` Cookieを見つけ、Cookieに`_les_v` （前回の訪問）の値`y`と30分で有効期限が切れるUTC エポックタイムスタンプが含まれていることを確認します。
      1. `adcloud` Cookieを削除してページを更新します。

1. （`/b/ss`のExperience Cloud ID サービス `visitorAPI.js` コードを使用する実装）フィルターを使用して、Analytics ヒットを確認します。

   ![&#x200B; フィルター：`/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. （Edge Networkへのリクエストペイロードに`advertisingStitchID`が含まれていることを確認するために、`/interact`でExperience Platform [!DNL Web SDK] `alloy.js` コード）フィルターを使用する実装。

   ![&#x200B; フィルター：`/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 2つのヒット間のID値を比較します。 すべての値は、Analytics ヒットのレポートスイート ID （`/b/ss/`の直後のURL パス）を除いて、クエリ文字列パラメーターにする必要があります。

   | ID | Analytics パラメーター | Edge Network | Adobe Advertising パラメーター |
   | --- | --- | --- | --- |
   | Experience Cloud IMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補足データ ID | sdid |  | `_les_sdid` |
   | ステッチ ID | stitchId | `_adcloud` プロパティの`advertisingStitchID` |  |
   | Analytics レポートスイート | `/b/ss/`の後の値 | | `_les_rsid` |
   | Experience Cloud訪問者ID | 中 |  | `_les_mid` |

   ID値が一致する場合は、JavaScriptの実装が確定されます。 Adobe Advertisingは、クリックスルーまたはビュースルーのトラッキングの詳細が存在する場合、その詳細を[!DNL Analytics] サーバーに送信します。

#### [!DNL Adobe Experience Platform Debugger]でコードを確認する方法

1. ホームページで[the [!DNL Adobe Experience Platform Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=ja)を開きます。
1. 「[!UICONTROL Network]」タブに移動します。
1. [!UICONTROL Solutions Filter] ツールバーで、[!UICONTROL Adobe Advertising]と[!UICONTROL Analytics]をクリックします。
1. [!UICONTROL Request URL - Hostname] パラメーター行で、`lasteventf-tm.everesttech.net`を見つけます。
1. 「[&#x200B; コードを [!DNL Chrome Developer Tools]](#validate-js-chrome)で確認する方法」のステップ 3と同様に、[!UICONTROL Request - Parameters]行で、生成されたシグナルを監査します。
   * (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Make sure the `Sdid` parameter matches the `Supplemental Data ID` in the Adobe Analytics filter.
   * (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Make sure the value of the `advertisingStitchID` parameter matches the `Sdid` sent to the Experience Platform Edge Network.
   * If the code isn&#39;t generating, then check to make sure the Adobe Advertising cookie has been removed in the [!UICONTROL Application] tab. Once it&#39;s removed, refresh the page and repeat the process.

   ![Auditing [!DNL Analytics for Advertising] JavaScript code in [!DNL Platform Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisites and key information for implementing [!DNL Analytics for Advertising]](prerequisites.md)
