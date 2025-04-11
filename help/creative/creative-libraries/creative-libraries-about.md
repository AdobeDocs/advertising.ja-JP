---
title: クリエイティブライブラリについて
description: 広告エクスペリエンスのクリエイティブの管理について説明します。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 731728964eef89aa1299c02fd90c805e13a0b163
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# クリエイティブライブラリについて

*クローズドベータ版機能*

クリエイティブ ライブラリを使用すると、広告エクスペリエンスで使用するクリエイティブを管理できます。 クリエイティブのセットと *クリエイティブバンドル*(1 つのユニットとしてエクスペリエンスに追加できるクリエイティブのグループ)を含む複数のライブラリを作成できます。

ライブラリには次のものを含めることができます。

* **個々のクリエイティブ:** ターゲットが定義されていない広告エクスペリエンス内に個人クリエイティブを直接含めユーザー。 また、クリエイティブを使用してバンドルを作成し、ターゲットを絞った [広告エクスペリエンスに含めることもできます](/help/creative/experiences/experience-about.md)。

   * **クリエイティブ標準:** クリエイティブを [さまざまなフォーマット](#creative-creative-formats)でアップロードして管理できます。 クリエイティブごとに、クリエイティブを関連付ける各広告の既定の言語、クリエイティブを含む広告をユーザーがクリックしたときに開く既定のランディングページ、および [!DNL Creative]内のさまざまなビューでフィルターとして使用するオプションのラベルを指定します。

   * **動的クリエイティブ：** （既存のAdobe Advertising DCO のお客様のみ）管理者ユーザーは、広告テンプレート内の動的変数をフィードファイル内の値にマッピングすることで、動的に生成されたクリエイティブを作成できます。 すべてのユーザーは、既存の動的広告をプレビュー、複製および削除できます。

* **クリエイティブバンドル：** 定義済みのユーザターゲットを持つ複数のエクスペリエンスで使用するために、クリエイティブをバンドルにグループ化します。 標準広告で構成される *標準バンドル* と、動的に生成された広告で構成される *動的バンドル* を作成できます。

## サポートされるCreative形式 {#creative-creative-formats}

### 標準クリエイティブの形式

次のクリエイティブタイプを [ サポートされているクリエイティブサイズ ](creative-sizes.md) で追加および管理できます。

>[!IMPORTANT]
>
>広告エクスペリエンスにHTML5、フレキシブル HTML5、またはサードパーティのクリエイティブを使用する場合でも、使用するクリエイティブサイズごとに画像クリエイティブを追加する必要があります。
>
>各エクスペリエンスには、エクスペリエンスに割り当てられるクリエイティブサイズごとにデフォルトの画像クリエイティブが必要です。 デフォルトの画像クリエイティブは、ブラウザーがJavaScriptに対応していない場合や、遅延のために広告サーバーが広告をパーソナライズできない場合に使用されます。

#### 柔軟なHTML5

柔軟なHTML5 クリエイティブは、HTML5 のすべての画像とその他の属性を標準のHTML タグとして持つクリエイティブで、クリエイティブライブラリ内または個々のエクスペリエンス内で [!DNL Creative] 内で直接編集できます（元のクリエイティブのバリエーションを作成します）。 柔軟なHTML5 クリエイティブは、Interactive Advertising Bureau （IAB）テクノロジーラボラトリーの標準である [ 広告ポートフォリオ ](https://flexibleads.iabtechlab.com/)<!-- Change to https://iabtechlab.com/standards/iab-new-ad-portfolio-guidelines/ if the broken page isn't fixed --> を使用します。広告フォーマットのサイズは（固定ではなく）柔軟で、広告の縦横比とサイズ範囲に基づいており、デバイスやパブリッシャーサイトをまたいで解像度を維持する広告です。

柔軟な HTML5 クリエイティブを ZIP ファイルとしてアップロード<!-- either --><!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point -->。詳しくは、[ フレキシブル HTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

<!-- Will flattening the view be possible later?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

オプションで、フレキシブル HTML5 クリエイティブで指定した属性のデフォルト値を変更できます。 後で、特定のエクスペリエンス内の属性にカスタム値を指定して、親クリエイティブのバリエーションを作成できます。

#### HTML5 クリエイティブ

すべての属性と画像を指定したシンプルまたは静的なHTML5 クリエイティブを ZIP ファイルとしてアップロードできます。 属性を編集したり、画像を追加したりすることはできません。代わりに、新しい ZIP ファイルをアップロードして、新しいクリエイティブを追加してください。 シンプルな HTML5 クリエイティブと静的クリエイティブの [仕様](html5-creative-specification.md)をご覧ください。

#### クリエイティブ画像

イメージ クリエイティブは、GIF、JPEG、JPG または PNG 形式 に含めることができます。 デバイスまたはネットワークから画像をアップロード<!--LATER:   images from your Adobe Experience Manager accounts or --> できます。

各広告エクスペリエンスには、エクスペリエンスに割り当てられた各クリエイティブサイズに応じたデフォルトの画像クリエイティブが必要です。

#### 第三者クリエイティブ

サードパーティの広告サーバーでホストされているクリエイティブのJavaScript トラッキングタグを入力します。 スクリプトは広告サーバーによって異なります。次に例を示します。

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### 動的広告の形式

管理者ユーザーは、広告テンプレートの動的変数をフィードファイルの値にマッピングすることで、静的なHTML5 形式および動的なHTML5 形式のクリエイティブを動的に生成できます。 動的なクリエイティブには、従来のAdobe Advertising Dynamic Creative Optimization（DCO）エクスペリエンスからのクリエイティブが含まれる場合があります。

## [!UICONTROL Creative Libraries] ビュー

各ビューのカスタマイズについて詳しくは、「[ データビューのカスタマイズ ](/help/creative/introduction/customize-data-views.md)」を参照してください。

### [!UICONTROL Creative Libraries] のメインビュー

[!UICONTROL Creative Libraries] のメインビューには、すべてのクリエイティブライブラリが表示されます。 各ライブラリのデータには、ライブラリのバンドルが割り当てられたエクスペリエンスの数、バンドルの数、クリエイティブの数、クリエイティブサイズの数、デフォルトの言語ターゲットの数、作成日、ライブラリの要素の最終変更日が含まれます。 テーブルモードには、広告主用の列も含まれます。

#### 使用可能なアクション

* ライブラリの新規作成

* クリエイティブライブラリごとに、次の操作を行います。

   * ライブラリ名を編集

   * ライブラリを開いて、ライブラリに割り当てられたクリエイティブとバンドルを表示します

   * ライブラリの削除

### [!UICONTROL Creative Libraries]/[!UICONTROL Creatives] ビュー

#### [!UICONTROL Standard Ads]

「[!UICONTROL Standard Ads]」タブには、作成したすべての標準クリエイティブが表示されます。 各クリエイティブのデータには、クリエイティブサイズ、クリエイティブタイプおよび作成日が含まれます。 テーブルモードには、デフォルト言語の列とデフォルトのランディングページの列も含まれます。

##### 使用可能なアクション

* [ライブラリへの標準クリエイティブの追加](creative-add-standard.md)

* [標準クリエイティブの編集](creative-edit-standard.md)

* [標準クリエイティブのプレビュー](creative-preview.md)

* [標準バンドルに標準クリエイティブを追加し、標準バンドルから標準クリエイティブを削除します](creative-attach-detach-bundles.md)

* [標準クリエイティブの複製](creative-duplicate.md)

* [標準クリエイティブのダウンロード](creative-download.md)

* [標準クリエイティブを削除](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

「[!UICONTROL Dynamic Ads]」タブには、クリエイティブカタログに対して動的に作成されたすべての動的クリエイティブが表示されます。ただし、「[!UICONTROL Dynamic Ads]」タブから [ 手動で削除 ](creative-delete.md) した動的クリエイティブは表示されません。 カタログが最後に処理されて以降の動的なクリエイティブを [ 手動で複製 ](creative-duplicate.md) した場合、そのカタログのクリエイティブのリストには重複したクリエイティブも含まれます。

各クリエイティブのデータには、クリエイティブタイプ、クリエイティブサイズ、クリエイティブが属するカタログの数、および作成日が含まれます。 テーブルモードには、クリエイティブの生成に使用されたテンプレートの列とオファーカウントも含まれます。

>[!NOTE]
>
>カタログが処理されるたびに、そのカタログの既存のダイナミック クリエイティブのデータが更新されます。

##### 使用可能なアクション

動的なクリエイティブを作成および編集する機能は、現在、Adobe アカウントチームのみが使用できます。 ただし、すべてのユーザーが次の操作を行うことができます。

* [動的クリエイティブのプレビュー](creative-preview.md)

* [ダイナミック クリエイティブをダイナミック バンドルに追加し、ダイナミック バンドルからダイナミック クリエイティブを削除する](creative-attach-detach-bundles.md)

* [ダイナミック クリエイティブ複製](creative-duplicate.md)

* [ダイナミック クリエイティブ削除](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]表示

[!UICONTROL Bundles]表示には、すべての標準バンドルコンテナと動的バンドルコンテナが表示されます。各バンドルに含まれるクリエイティブのクリエイティブ名、クリエイティブサイズ、言語を確認できます。

#### 使用可能なアクション

* ライブラリへの標準バンドルと動的バンドルの追加

* バンドル内のクリエイティブのリストとプレビュー

* バンドル名を編集

* 標準バンドルに標準クリエイティブを追加し、標準バンドルから標準クリエイティブを削除します

* 重複するバンドル

* バンドルを削除

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリの管理 ](/help/creative/creative-libraries/creative-library-manage.md)
>* [ クリエイティブライブラリへの標準クリエイティブの追加 ](creative-add-standard.md)
>* [ クリエイティブバンドルの管理 ](bundle-manage.md)
>* [ データビューのカスタマイズ ](/help/creative/introduction/customize-data-views.md)
