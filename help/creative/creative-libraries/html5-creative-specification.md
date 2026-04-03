---
title: HTML5のクリエイティブ仕様
description: Advertising CreativeのHTML5 クリエイティブ仕様を参照してください。
feature: Creative Standard Creatives
exl-id: 06d29442-d688-4fb8-ad6f-cba0a897fde0
TQID: https://experienceleague.adobe.com/a4XiPoEgYQQJCkRTgFT5wPr-XQzzIiC-A8eyIhIyMD8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1157
ht-degree: 1%

---

# Advertising CreativeのHTML5 クリエイティブ仕様

このドキュメントでは、[!DNL Creative]内のHTML5 クリエイターの要件とAPI サポートの概要を説明します。 このAPIは、クリエイティブ配信時に属性を設定できるHTML5 クリエイターの開発をサポートしています。

## 範囲

[!DNL Creative]は、ページ上の設定された境界線内に表示されるリッチメディア以外のクリエイティブを含むHTML5 バナーをサポートしています。 次の種類のHTML5 クリエイティブを使用できます。

<!--
Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** クリエイティブの作成と人身売買の際に設定可能なランディングページ URLを5つまでサポートします。

* **柔軟なHTML5:** クリエイティブの作成と人身売買の際に設定できるランディングページ URLを5つまでサポートしています。また、クリエイティブの作成と人身売買の際にクリエイティブ属性を変更することもできます。

## 要件定義

### フォルダーと圧縮の要件

* クリエイティブは、ZIP ファイル（.ZIP形式）でパッケージ化する必要があります。 ネストされたZIP ファイルはサポートされていないので、外部の圧縮フォルダー内に圧縮フォルダーを含めないでください。

* ZIP ファイルには、少なくとも1つのHTML ファイル（メインのHTML表示ファイル）が含まれている必要があります。これには、[!DNL Creative] JavaScript ライブラリへの参照が含まれます。 メインのHTML ファイルは、ルートフォルダーまたはサブフォルダーのどちらかにできます。

* HTMLのメインファイルには、特殊文字が含まれていない限り、任意の名前を付けることができます。ただし、`index.html`をお勧めします。

* 最終的なクリエイティブをレンダリングするために必要なすべてのサポートアセットは、HTMLの表示ファイルと同じフォルダーか、メインフォルダーのサブフォルダーにある必要があります。

* クリエイティブで参照していないファイルをクリエイティブに含めないでください。

### Advertising Creative JavaScript ファイルのインクルード

メインのHTML ファイルには、JavaScript ファイル `AMOLibrary.js`への参照を含める必要があります。他のファイルは含まれません。 次のアドレスを使用して、`<head>` セクションの最初の行にあるファイルを呼び出します。

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

このファイルには、終了イベントのローカルテストが問題なく実行されるように機能が含まれています。

<!--
 Remove to simplify:

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

<!--
 Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5のクリエイティブ要件

#### 静的HTML5でのクリックスルーURLのサポート

##### `amo.registerClick(clkVar, clkUrl)`

クリックスルーURLと、各URLの参照に使用される関連パラメーター（`clickTag`と呼ばれます）を登録します。 このAPIは、クリック トラッキングを追加する場所を[!DNL Creative]広告サーバーに通知します。 このAPIを使用して、対応するランディングページのURLを持つクリックタグ変数を5つまで登録できます。

>[!NOTE]
>
>HTML5 クリエイティブに含める静的URLは、ローカルテストの目的でのみ使用され、上書きされます。 HTML5 クリエイティブをアップロードする場合、各`clickTag`変数のデフォルトのランディングページを定義します。 アップロードしたHTML5 クリエイティブを広告エクスペリエンスに割り当てる場合、オプションで各`clickTag`変数のデフォルトのランディングページを上書きでき、[!DNL Creative]はエクスペリエンスの保存時にURLにクリックトラッキングを追加します。

###### パラメーター

* `clkVar` — クリック変数（通常は「clickTag」）の名前。二重引用符で囲みます。

* `clkUrl` – このクリック変数のランディングページ URL。二重引用符で囲みます。

###### 使用状況

メイン HTML ファイルの`amo.registerClick()` セクションで`<head>`を呼び出します。

###### 例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

終了イベントをトリガーします。これにより、ユーザーは`clickTag`用に設定されたランディングページにリダイレクトされます。 ローカルテスト中、この関数は、関数に渡されるURLが登録されたかどうかを開発者に警告します。

###### パラメーター

* `clkTag` — ランディングページ URLを割り当てるために使用するクリック変数の名前。1つの引用符で囲んだ`amo.registerClick()`関数を使用します。

* `event` — （オプション）JavaScriptの「クリック」イベントオブジェクト。 これはクリック数の座標を記録し、クリエイティブのパフォーマンスを分析するためにさらに使用できます。

###### 使用状況

メイン HTML ファイルの`amo.onAdClick()` セクションで`<body>`を呼び出します。

###### 例

`amo.onAdClick('clickTag')`または`amo.onAdClick('clickTag',clickEvt)`

### 柔軟なHTML5のクリエイティブ要件

#### 柔軟なHTML5でのクリックスルーURLのサポート

##### `amo.registerClick(clkVar, clkUrl)`

クリックスルーURLと、各URLの参照に使用される関連パラメーター（`clickTag`と呼ばれます）を登録します。 このAPIは、クリック トラッキングを追加する場所を[!DNL Creative]広告サーバーに通知します。 このAPIを使用して、対応するランディングページのURLを持つクリックタグ変数を5つまで登録できます。

>[!NOTE]
>
>HTML5 クリエイティブに含める静的URLは、ローカルテストの目的でのみ使用され、上書きされます。 HTML5 クリエイティブをアップロードする場合、各`clickTag`変数のデフォルトのランディングページを定義します。 アップロードしたHTML5 クリエイティブを広告エクスペリエンスに割り当てる場合、オプションで各`clickTag`変数のデフォルトのランディングページを上書きでき、[!DNL Creative]はエクスペリエンスの保存時にURLにクリックトラッキングを追加します。

###### パラメーター

* `clkVar` — クリック変数（通常は「clickTag」）の名前。二重引用符で囲みます。

* `clkUrl` – このクリック変数のランディングページ URL。二重引用符で囲みます。

###### 使用状況

メイン HTML ファイルの`amo.registerClick()` セクションで`<head>`を呼び出します。

###### 例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

終了イベントをトリガーします。これにより、ユーザーは`clickTag`用に設定されたランディングページにリダイレクトされます。 ローカルテスト中、この関数は、関数に渡されるURLが登録されたかどうかを開発者に警告します。

###### パラメーター

* `clkTag` — ランディングページ URLを割り当てるために使用するクリック変数の名前。1つの引用符で囲んだ`amo.registerClick()`関数を使用します。

* `event` — （オプション）JavaScriptの「クリック」イベントオブジェクト。 これはクリック数の座標を記録し、クリエイティブのパフォーマンスを分析するためにさらに使用できます。

###### 使用状況

メイン HTML ファイルの`amo.onAdClick()` セクションで`<body>`を呼び出します。

###### 例

`amo.onAdClick('clickTag')`または`amo.onAdClick('clickTag',clickEvt)`

#### 柔軟なHTML5でのクリエイティブ属性のサポート

##### `amo.registerAttribute(key, type, value)`

クリエイティブまたはエクスペリエンスの作成時に変更できるクリエイティブの属性を定義します。 クリエイティブまたはエクスペリエンスの作成時に設定できるクリエイティブ属性は、最大20個まで定義できます。

>[!NOTE]
>
>このメソッドで定義された値はローカル開発にのみ使用され、ライブ広告の配信では使用されません。

###### パラメーター

* `key` – 属性の英数字の名前。 アルファベット文字で始める必要があります。

* `type` – 属性の種類（`TEXT`または`IMAGE`）。

* `value` — テスト用の属性の値。 タイプ `IMAGE`の属性の場合、値は画像ファイルへの相対パスである必要があります。

###### 使用状況

`amo.registerAttribute()`を呼び出して、ローカルモードでのテスト中に1つのクリエイティブ属性、タイプ、値を登録します。 サンプル値として使用される画像ファイルは、アップロードされたパッケージと共にZIP ファイルにパッケージ化する必要があります。

##### `amo.attributes`

クリエイティブ属性変数の名前と値をクエリするJSON オブジェクト。 オブジェクトキーは属性名で、値はその属性の値です。

ローカル テスト モードでは、キーと値のペアは、`amo.registerAttribute` APIによって登録されたペアです。 制作の場合、クリエイティブの作成および人身売買の際に、クリエイティブ属性変数名と値を設定する必要があります。

### Creativeの必要コンテンツ構成

Advertising DSPで利用可能なディスプレイ交換のほとんどは、次のクリエイティブ要件を備えています。

* すべての広告画像を囲むには、しっかりとした境界線が必要です。

* 拡大する広告は許可されていません。

* ランディングページを新しいウィンドウで開く必要があります。

* ランディングページドメインとそのサブドメインは、35文字以下である可能性があります。 **注意：**&#x200B;最終的なランディングページ URLは、HTML5 アセット自体ではなく、DSPで定義されます。

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

### JSON配列としてのコンテンツの例

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

   * bg.jpg （JPG、PNG、SVG、またはGIFの画像）

### 単純なHTML5 クリエイティブ用のHTML ファイル（index.html）の例

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

### 静的なHTML5 クリエイティブ用のHTML ファイル（index.html）の例

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
>* [標準クリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-standard.md)
