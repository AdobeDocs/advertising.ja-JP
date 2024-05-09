---
title: の JavaScript コード [!DNL Analytics for Advertising]
description: の JavaScript コード [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# の JavaScript コード [!DNL Analytics for Advertising]

*Advertising DSPのみを使用する広告主*

広告DSPの場合、 [!DNL Analytics for Advertising] 統合では、ビュースルーおよびクリックスルーサイトのインタラクションを追跡します。 クリックスルー訪問は、web ページ上の標準Adobe Analytics コードによってトラッキングされます。 [!DNL Analytics] コードは、ランディングページ URL 内の AMO ID パラメーターと EF ID パラメーターをキャプチャし、それぞれの予約済みパラメーターで追跡します [!DNL eVars]. Web ページに JavaScript スニペットをデプロイすることで、ビュースルーの訪問を追跡できます。

サイトへの訪問の最初のページビューで、Adobe Advertising JavaScript コードは、訪問者が以前に広告を表示またはクリックしたかどうかを確認します。 ユーザーがクリックスルーから以前にサイトに入った場合や、広告を表示していない場合、訪問者は無視されます。 訪問者が広告を表示し、その間にクリックスルーからサイトに入っていない場合 [クリックルックバックウィンドウ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) Adobe Advertising内に設定した場合、Adobe AdvertisingJavaScript コードは（a）を使用します [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 追加の ID を生成するには：（`SDID`）または b） Adobe Experience Platformを使用します。 [!DNL Web SDK] `generateRandomID` を生成する方法 `[!DNL StitchID]`. どちらの ID を使用しても、Adobe Advertisingから訪問者のAdobe Analytics ヒットにデータが結び付けられます。 次に、Adobe Analyticsは、広告公開に関連付けられた AMO ID および EF ID のAdobe Advertisingに対してクエリを実行します。 次に、AMO ID と EF ID がそれぞれ設定されます [!DNL eVars]. これらの値は、指定した期間（デフォルトでは 60 日）保持されます。

[!DNL Analytics] サイトトラフィック指標（ページビュー数、訪問回数、滞在時間など）および [!DNL Analytics] ef ID をキーとして使用して、1 時間ごとにAdobe Advertisingするカスタムイベントまたは標準イベント。 これら [!DNL Analytics] 次に、指標がコンバージョンアトリビューションシステムを実行し、Adobe Advertisingをクリック数と公開回数の履歴に結び付けます。

>[!NOTE]
>
>Adobe Advertisingの JavaScript トラッキングロジックはAdobe側で行われるので、ページ読み込み時間にはほとんど影響しません。
>
>これに対し、のロジックは [!DNL DCM] へのデータコネクタ [!DNL Analytics] （使用 [!DNL Google Campaign Manager 360]）に設定する必要があります。広告DSPの場合は、クライアントサイドで行われます。 クライアントサイドでステッチすると、ページの読み込みが遅くなり、データ損失のリスクが高くなります。 これは、 [!DNL Analytics] JavaScript は ping が必要 [!DNL DoubleClick] 待機 [!DNL DoubleClick] 最後のクリックまたはインプレッションデータをに返します [!DNL Analytics]. いつ [!DNL DSP] チームによるタスクの設定 [!DNL DCM] データコネクタです。ページを遅らせる期間を指定する必要があります。

## JavaScript コードのデプロイ

JavaScript ライブラリは、 [!DNL Analytics] お互いにコミュニケーションをとるAdobe Advertising。 次の場合 [!DNL Analytics for Advertising] Adobe Advertisingが統合の実装中に完了しました。デプロイ方法の説明を含むこのコードは既に受け取っているはずです。

### コード

#### Experience Cloud ID サービスを使用する実装 `visitorAPI.js` コード

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Experience Platformを使用する実装 [!DNL Web SDK] `alloy.js`コード

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### コードの配置場所

この [!DNL Analytics for Advertising] JavaScript 関数は、Experience CloudID サービスの後、Analytics アプリ測定コードの前に置く必要があります。 これにより、追加の ID （`SDID`）または `[!DNL StitchID]` は、Analytics 呼び出しに含まれます。

![コード配置](/help/integrations/assets/a4adc-code-placement.png)

### コードのデプロイメントの検証

任意の種類のパケットスニファータイプのツール（など）を使用して、検証を実行できます [!DNL Charles], [!DNL Fiddler]、または [!DNL Chrome Developer Tools]）に設定します。そのためには、Adobe Advertisingに送信されるリクエストと、に送信されるリクエストの間で、4 つの ID の値を比較します [!DNL Analytics]（以下で説明します）。

#### でコードを確認する方法 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開く [!DNL Chrome Developer Tools] をクリックし、 **ネットワーク** タブ。

1. を含む web サイトページを読み込む [!DNL Analytics for Advertising] JavaScript。

1. をフィルター [!UICONTROL Network] tab by `last` 2 つの行を確認します。

   ![前回のフィルタリング](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 最初の行は JavaScript ライブラリの呼び出しであり、というタイトルが付いています `last-event-tag-latest.min.js`.
   * 2 行目は、リクエストをAdobe Advertisingに送信する呼び出しです。 まず次の手順を実行します。 `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     コールトゥAdobe Advertisingが表示されない場合は、訪問の最初のページビューではない可能性があります。 テストの目的で、cookie を削除して、対応する訪問の最初のページビューが次の呼び出しになるようにすることができます。

   1. 「アプリケーション」タブで、次の項目を検索します `adcloud` cookie を使用し、cookie にが含まれていることを確認します `_les_v` （前回の訪問）の値は `y` そして、30 分で有効期限が切れる UTC エポックタイムスタンプ。
      1. を削除 `adcloud` cookie を使用してページを更新します。

1. （Experience CloudID サービスを利用する実装 `visitorAPI.js` コード）フィルターの条件 `/b/ss` Analytics ヒットを確認します。

   ![フィルタリング対象 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. （Experience Platformを使用する実装） [!DNL Web SDK] `alloy.js`コード）フィルターの条件 `/interact` Edge Networkへのリクエストペイロードにが含まれていることを確認します `advertisingStitchID`.

   ![フィルタリング対象 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 2 つのヒット間の ID 値を比較します。 Analytics ヒットのレポートスイート ID （の直後の URL パス）を除き、すべての値はクエリ文字列パラメーターにする必要があります `/b/ss/`.

   | ID | Analytics パラメーター | Edge Network | Adobe Advertisingパラメーター |
   | --- | --- | --- | --- |
   | Experience CloudIMS 組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 追加データ ID | sdid |  | `_les_sdid` |
   | ステッチ ID | stitchId | `advertisingStitchID` の下 `_adcloud` プロパティ |  |
   | Analytics レポートスイート | 次の後の値 `/b/ss/` | | `_les_rsid` |
   | Experience Cloud訪問者 ID | mid |  | `_les_mid` |

   ID 値が一致する場合、JavaScript 実装が確認されます。 Adobe Advertisingは、 [!DNL Analytics] サーバークリックスルーまたはビュースルートラッキングの詳細（存在する場合）。

#### でコードを確認する方法 [!DNL Adobe Experience Cloud Debugger]

1. を開きます [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) ホームページで。
1. に移動します [!UICONTROL Network] タブ。
1. が含まれる [!UICONTROL Solutions Filter] ツールバー、クリック [!UICONTROL Adobe Advertising] および [!UICONTROL Analytics].
1. が含まれる [!UICONTROL Request URL - Hostname] パラメータ行、を検索 `lasteventf-tm.everesttech.net`.
1. が含まれる [!UICONTROL Request - Parameters] 行。生成されたシグナルを監査します（「」の手順 3 と同様）[でコードを確認する方法 [!DNL Chrome Developer Tools]](#validate-js-chrome).」と入力します。
   * （Experience CloudID サービスを利用する実装 `visitorAPI.js` code）次のことを確認します `Sdid` パラメーターがに一致 `Supplemental Data ID` Adobe Analytics フィルターで上書きできます。
   * （Experience Platformを使用する実装） [!DNL Web SDK] `alloy.js`（コード）の値 `advertisingStitchID` パラメーターがに一致 `Sdid` がExperience PlatformEdge Networkに送信されました。
   * コードが生成されない場合は、でAdobe Advertising Cookie が削除されていることを確認します [!UICONTROL Application] タブ。 削除したら、ページを更新して手順を繰り返します。

   ![監査 [!DNL Analytics for Advertising] の JavaScript コード [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising]](prerequisites.md)
