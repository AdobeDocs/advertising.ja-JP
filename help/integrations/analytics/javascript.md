---
title: 用 JavaScript コード [!DNL Analytics for Advertising]
description: 用 JavaScript コード [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 9158ed3fc8b35b5f79f217b619c2ff8e596895ab
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# 用 JavaScript コード [!DNL Analytics for Advertising]

*Advertising DSPのみの広告主*

Advertising DSPの場合、 [!DNL Analytics for Advertising] 統合は、ビュースルーおよびクリックスルーサイトのインタラクションを追跡します。 クリックスルー訪問は、Web ページ上の標準のAdobe Analyticsコードで追跡されます。 [!DNL Analytics] コードはランディングページ URL の AMO ID および EF ID パラメーターをキャプチャし、それぞれの予約済みので追跡します。 [!DNL eVars]. Web ページに JavaScript スニペットをデプロイすることで、ビュースルー訪問を追跡できます。

サイトへの訪問の最初のページビューで、Adobe Advertisingの JavaScript コードは、訪問者が以前に広告を閲覧またはクリックしたかどうかを確認します。 ユーザーが以前にクリックスルーでサイトに入ったことがある場合や、広告を表示していない場合、訪問者は無視されます。 訪問者が広告を閲覧した後、 [ルックバックウィンドウをクリック](/help/integrations/analytics/prerequisites.md#lookback-a4adc) Adobe Advertising内で設定した場合、Adobe AdvertisingJavaScript コード a) は、 [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 追加の ID(`SDID`) または b) Adobe Experience Platformを使用 [!DNL Web SDK] `generateRandomID` メソッドを使用して `[!DNL StitchID]`. どちらの ID も、データを訪問者から訪問者のAdobe AnalyticsヒットにAdobe Advertisingするために使用されます。 次に、Adobe Analyticsは、広告公開に関連付けられた AMO ID と EF ID に対するAdobe Advertisingをクエリします。 AMO ID と EF ID は、それぞれの [!DNL eVars]. これらの値は、指定された期間（デフォルトでは 60 日）保持されます。

[!DNL Analytics] サイトトラフィック指標（ページビュー数、訪問回数、滞在時間など）と [!DNL Analytics] EF ID をキーとして使用し、1 時間ごとにAdobe Advertisingを設定するカスタムイベントまたは標準イベント。 これら [!DNL Analytics] 次に、指標のアトリビューションシステムを実行して、Adobe Advertisingをクリック数および露出数の履歴に結び付けます。

>[!NOTE]
>
>Adobe Advertisingの JavaScript トラッキングロジックはAdobe側で発生するので、ページの読み込み時間にほとんど影響しません。
>
>これに対し、 [!DNL DCM] データコネクタ： [!DNL Analytics] ( [!DNL Google Campaign Manager 360])Advertising DSPの場合は、クライアント側で発生します。 クライアント側のステッチでは、ページの読み込みが遅くなり、データの損失のリスクが高まります。 これは、 [!DNL Analytics] JavaScript は ping が必要 [!DNL DoubleClick] そして待つ [!DNL DoubleClick] を呼び出して、最後のクリック/インプレッションデータを [!DNL Analytics]. 次の場合に、 [!DNL DSP] チームが設定 [!DNL DCM] data connector を使用する場合は、ページの遅延時間を指定する必要があります。

## JavaScript コードのデプロイ

JavaScript ライブラリは、 [!DNL Analytics] お互いにコミュニケーションを取るAdobe Advertising。 次の場合、 [!DNL Analytics for Advertising] の統合はAdobe Advertisingの実装中に完了しているので、このコードとデプロイ方法に関する手順を既に受け取っているはずです。

### コード

#### Experience CloudID サービスを使用する実装 `visitorAPI.js` コード

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Experience Platform [!DNL Web SDK] `alloy.js`コード

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### コードの配置場所

The [!DNL Analytics for Advertising] JavaScript 関数は、Experience CloudID サービスの後、Analytics App Measurement コードの前に配置する必要があります。 これにより、追加の ID(`SDID`) または `[!DNL StitchID]` が Analytics 呼び出しに含まれます。

![コードの配置](/help/integrations/assets/a4adc-code-placement.png)

### コードのデプロイメントの検証

任意の種類のパケットスニファー ( [!DNL Charles], [!DNL Fiddler]または [!DNL Chrome Developer Tools]) を比較することで、Adobe Advertisingになるリクエストと [!DNL Analytics]（以下に概要を示します）。

#### を使用してコードを確認する方法 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開く [!DNL Chrome Developer Tools] をクリックし、 **ネットワーク** タブをクリックします。

1. を含む Web サイトページを読み込みます。 [!DNL Analytics for Advertising] JavaScript。

1. フィルター [!UICONTROL Network] タブの基準 `last` とで、2 つの行を確認します。

   ![最後のフィルター](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 最初の行は JavaScript ライブラリへの呼び出しで、タイトルは `last-event-tag-latest.min.js`.
   * 2 番目の行は、リクエストをAdobe Advertisingに送信する呼び出しです。 最初は次のようになります。 `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Adobe Advertisingへの呼び出しが表示されない場合は、訪問の最初のページビューではない可能性があります。 テストの目的で、cookie を削除して、次の呼び出しが対応する訪問の最初のページビューになるようにできます。

   1. 「アプリケーション」タブで、 `adcloud` cookie を確認し、cookie に `_les_v` （最後の訪問）の値が `y` と、30 分で期限切れになる UTC エポックタイムスタンプ。
      1. を削除します。 `ad cloud` cookie を更新し、ページを更新します。

1. (Experience CloudID サービスを使用する実装 ) `visitorAPI.js` コード ) フィルター `/b/ss` をクリックして Analytics ヒットを確認します。

   ![フィルター： `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (EXPERIENCE PLATFORM [!DNL Web SDK] `alloy.js`コード ) フィルター `/interact` を使用して、Edge ネットワークへのリクエストペイロードにが含まれていることを確認します。 `advertisingStitchID`.

   ![フィルター： `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 2 つのヒット間で ID 値を比較します。 すべての値は、Analytics ヒット内のレポートスイート ID（の直後の URL パス）を除く、クエリー文字列パラメーターに含まれます `/b/ss/`.

   | ID | Analytics パラメーター | Edge Network | Adobe Advertisingパラメータ |
   | --- | --- | --- | --- |
   | Experience CloudIMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | 追加データ ID | sdid |  | `_les_sdid` |
   | ステッチ ID | stitchId | `advertisingStitchID` の下に `_adcloud` プロパティ |  |
   | Analytics レポートスイート | 次の後の値： `/b/ss/` | | `_les_rsid` |
   | Experience Cloud訪問者 ID | mid |  | `_les_mid` |

   ID 値が一致する場合、JavaScript の実装が確認されます。 Adobe Advertisingが [!DNL Analytics] クリックスルーまたはビュースルートラッキングの詳細（存在する場合）をサーバーに送信します。

#### を使用してコードを確認する方法 [!DNL Adobe Experience Cloud Debugger]

1. を開きます。 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) をホームページに追加します。
1. 次に移動： [!UICONTROL Network] タブをクリックします。
1. Adobe Analytics の [!UICONTROL Solutions Filter] ツールバー、クリック [!UICONTROL Adobe Advertising] および [!UICONTROL Analytics].
1. Adobe Analytics の [!UICONTROL Request URL - Hostname] パラメータ行、を見つけます。 `lasteventf-tm.everesttech.net`.
1. Adobe Analytics の [!UICONTROL Request - Parameters] 行で、「 」の手順 3 と同様に、生成されたシグナルを監査します。[を使用してコードを確認する方法 [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Experience CloudID サービスを使用する実装 ) `visitorAPI.js` コード ) `Sdid` パラメーターは `Supplemental Data ID` ( Adobe Analyticsフィルター )
   * (EXPERIENCE PLATFORM [!DNL Web SDK] `alloy.js`コード ) `advertisingStitchID` パラメーターは `Sdid` をExperience PlatformEdge ネットワークに送信しました。
   * コードが生成されない場合は、Adobe AdvertisingCookie が [!UICONTROL Application] タブをクリックします。 削除したら、ページを更新し、処理を繰り返します。

   ![監査 [!DNL Analytics for Advertising] の JavaScript コード [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising]](prerequisites.md)
