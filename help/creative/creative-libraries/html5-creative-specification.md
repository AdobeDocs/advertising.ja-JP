---
title: HTML5 クリエイティブの仕様
description: Advertising CreativeのHTML5 クリエイティブの仕様を参照します。
feature: Creative Standard Creatives
exl-id: 06d29442-d688-4fb8-ad6f-cba0a897fde0
source-git-commit: e966058f5fe3fe9eb039f74bda8ea950f717e123
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Advertising CreativeのHTML5 クリエイティブの仕様

このドキュメントでは、[!DNL Creative] 内のHTML5 クリエイティブの要件と API サポートの概要を説明します。 API は、クリエイティブの配信時に属性を設定できるHTML5 クリエイティブの開発をサポートしています。

## 対象範囲

[!DNL Creative] は、ページの設定枠内に表示される非リッチメディアクリエイティブを含むHTML5 バナーをサポートしています。 次のタイプのHTML5 クリエイティブを使用できます。

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** クリエイティブの作成およびトラフィックの処理中に設定できるランディングページ URL を最大 5 つサポートします。

* **柔軟なHTML5:** クリエイティブの作成時およびトラフィック作成時に設定できる最大 5 つのランディングページ URL をサポートし、クリエイティブの作成時およびトラフィック作成時にクリエイティブ属性を変更することもできます。

## 要件

### フォルダーおよび圧縮の要件

* クリエイティブは、ZIP ファイル（.ZIP 形式）にパッケージ化する必要があります。 ネストされた ZIP ファイルはサポートされていないので、外側の圧縮フォルダーに圧縮フォルダーを含めないでください。

* ZIP ファイルには、1 つ以上のHTML ファイル（メインのHTML表示ファイル）が含まれている必要があります。このファイルには、[!DNL Creative] JavaScript ライブラリへの参照が含まれています。 メインのHTML ファイルは、ルートフォルダーまたはサブフォルダーにあります。

* メインのHTML ファイルには、特殊文字が含まれていない限り、任意の名前を付けること `index.html` できます（推奨されます）。

* 最終クリエイティブのレンダリングに必要なサポート対象アセットはすべて、HTML表示ファイルと同じフォルダーか、メインフォルダーのサブフォルダーに存在する必要があります。

* クリエイティブが参照しないファイルをクリエイティブに含めないでください。

### Advertising Creative JavaScript ファイルの組み込み

メインのHTML ファイル（および他のファイル）には、JavaScript ファイル `AMOLibrary.js` への参照を含める必要があります。 次のアドレスを使用して、`<head>` セクションの最初の行にあるファイルを呼び出します。

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

このファイルには、終了イベントのローカルテストが問題なく実行されることを確認する関数が含まれています。

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5 のクリエイティブ要件

#### 静的HTML5 でのクリックスルー URL のサポート

##### `amo.registerClick(clkVar, clkUrl)`

は、クリックスルー URL と、各 URL を参照するために使用される関連パラメーター（`clickTag` と呼ばれます）を登録します。 この API は、クリックの追跡をどこに追加するかを [!DNL Creative] 広告サーバーに通知します。 この API を使用して、最大 5 つのクリックタグ変数を登録し、それぞれに対応するランディングページ URL を登録できます。

>[!NOTE]
>
>HTML5 クリエイティブに含める静的 URL は、ローカルテスト目的でのみ使用され、上書きされます。 HTML5 クリエイティブをアップロードする場合、`clickTag` 変数ごとにデフォルトのランディングページを定義します。 アップロードしたHTML5 クリエイティブを広告エクスペリエンスに割り当てる際に、オプションで各 `clickTag` 変数のデフォルトのランディングページを上書きし、エクスペリエンスを保存す [!DNL Creative] 際に URL にクリックの追跡を追加できます。

###### パラメーター

* `clkVar` - クリック変数の名前（通常は「clickTag」）。二重引用符で囲みます。

* `clkUrl` – このクリック変数のランディングページ URL。二重引用符で囲まれています。

###### 使用状況

メインのHTML ファイルの `<head>` セクションにある `amo.registerClick()` を呼び出します。

###### 例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

exit イベントをトリガーします。このイベントは、`clickTag` ーザーに設定されたランディングページにユーザーをリダイレクトします。 ローカルテスト中に、この関数は、関数に渡される URL が登録されたかどうかを開発者にアラートします。

###### パラメーター

* `clkTag` - `amo.registerClick()` 関数を使用してランディングページ URL を割り当てるために使用するクリック変数の名前。一重引用符で囲まれています。

* `event` — （任意）JavaScriptの「クリック」イベントオブジェクト。 クリックの座標が記録されます。この値は、クリエイティブのパフォーマンスを分析する際に使用できます。

###### 使用状況

メインのHTML ファイルの `<body>` セクションにある `amo.onAdClick()` を呼び出します。

###### 例

`amo.onAdClick('clickTag')` 以 `amo.onAdClick('clickTag',clickEvt)`

### HTML5 の柔軟なクリエイティブ要件

#### フレキシブル HTMLでのクリックスルー URL のサポート 5

##### `amo.registerClick(clkVar, clkUrl)`

は、クリックスルー URL と、各 URL を参照するために使用される関連パラメーター（`clickTag` と呼ばれます）を登録します。 この API は、クリックの追跡をどこに追加するかを [!DNL Creative] 広告サーバーに通知します。 この API を使用して、最大 5 つのクリックタグ変数を登録し、それぞれに対応するランディングページ URL を登録できます。

>[!NOTE]
>
>HTML5 クリエイティブに含める静的 URL は、ローカルテスト目的でのみ使用され、上書きされます。 HTML5 クリエイティブをアップロードする場合、`clickTag` 変数ごとにデフォルトのランディングページを定義します。 アップロードしたHTML5 クリエイティブを広告エクスペリエンスに割り当てる際に、オプションで各 `clickTag` 変数のデフォルトのランディングページを上書きし、エクスペリエンスを保存す [!DNL Creative] 際に URL にクリックの追跡を追加できます。

###### パラメーター

* `clkVar` - クリック変数の名前（通常は「clickTag」）。二重引用符で囲みます。

* `clkUrl` – このクリック変数のランディングページ URL。二重引用符で囲まれています。

###### 使用状況

メインのHTML ファイルの `<head>` セクションにある `amo.registerClick()` を呼び出します。

###### 例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

exit イベントをトリガーします。このイベントは、`clickTag` ーザーに設定されたランディングページにユーザーをリダイレクトします。 ローカルテスト中に、この関数は、関数に渡される URL が登録されたかどうかを開発者にアラートします。

###### パラメーター

* `clkTag` - `amo.registerClick()` 関数を使用してランディングページ URL を割り当てるために使用するクリック変数の名前。一重引用符で囲まれています。

* `event` — （任意）JavaScriptの「クリック」イベントオブジェクト。 クリックの座標が記録されます。この値は、クリエイティブのパフォーマンスを分析する際に使用できます。

###### 使用状況

メインのHTML ファイルの `<body>` セクションにある `amo.onAdClick()` を呼び出します。

###### 例

`amo.onAdClick('clickTag')` 以 `amo.onAdClick('clickTag',clickEvt)`

#### 柔軟なHTML5 でのクリエイティブ属性のサポート

##### `amo.registerAttribute(key, type, value)`

クリエイティブまたはエクスペリエンスの作成時に変更できるクリエイティブの属性を定義します。 クリエイティブまたはエクスペリエンスの作成時に設定できるクリエイティブ属性は、最大 20 個まで定義できます。

>[!NOTE]
>
>この方法で定義された値は、ローカル開発のみに使用され、ライブ広告サービングでは使用されません。

###### パラメーター

* `key` – 属性の英数字の名前。 英字で始める必要があります。

* `type` – 属性のタイプ （`TEXT` または `IMAGE`）。

* `value` - テスト用の属性の値。 `IMAGE` タイプの属性の場合、値は画像ファイルへの相対パスである必要があります。

###### 使用状況

ローカルモードでのテスト中に `amo.registerAttribute()` を呼び出して、1 つのクリエイティブ属性、タイプ、値を登録します。 サンプル値として使用する画像ファイルは、アップロードされたパッケージと共に ZIP ファイルにパッケージ化してください。

##### `amo.attributes`

クリエイティブ属性の変数の名前と値をクエリする JSON オブジェクト。 オブジェクトキーは属性名で、値はこれらの属性の値です。

ローカルテストモードでは、キーと値のペアは `amo.registerAttribute` API によって登録されたペアです。 実稼動環境の場合は、クリエイティブの作成時およびトラフィック作成時に、クリエイティブ属性変数の名前と値を設定する必要があります。

### Creative コンテンツの要件

Advertising DSPで利用可能なほとんどのディスプレイ交換には、次のようなクリエイティブな要件があります。

* 実線の境界線はすべての広告画像を囲む必要があります。

* 広告の拡張は許可されていません。

* ランディングページは、新しいウィンドウで開く必要があります。

* ランディングページのドメインとそのサブドメインは、35 文字未満にする必要があります。 **メモ：** 最終的なランディングページの URL は、HTML5 Assets 自体ではなく、DSPで定義されます。

* 広告のオファーに対する免責事項は、ランディングページだけでなく、広告自体に含める必要があります。

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## JSON オブジェクトおよび配列としてのコンテンツの例

### JSON オブジェクトとしてのコンテンツの例

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### JSON 配列としてのコンテンツの例

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## HTML5 クリエイティブの例

### フォルダー構造の例（解凍後）

* index.html

* /assets （フォルダー）

   * bg.jpg （JPG、PNG、SVGまたはGIF画像）

### 単純なHTML5 クリエイティブのHTML ファイルの例（index.html）

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### 静的HTML5 クリエイティブのHTML ファイルの例（index.html）

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリへの標準クリエイティブの追加 ](/help/creative/creative-libraries/creative-add-standard.md)
