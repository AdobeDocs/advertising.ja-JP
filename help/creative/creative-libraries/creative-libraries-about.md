---
title: クリエイティブライブラリについて
description: 広告エクスペリエンスで使用するクリエイティブの管理について説明します。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 0%

---

# クリエイティブライブラリについて

*クローズドベータ版機能*

クリエイティブライブラリを使用すると、広告エクスペリエンスで使用するすべてのクリエイティブを管理できます。 複数のライブラリを作成できます。各ライブラリには、一連のクリエイティブと、1 つのユニットとしてエクスペリエンスに追加できるクリエイティブのグループである *クリエイティブバンドル* が含まれます。

ライブラリには、次のものが含まれます。

* **個々のクリエイティブ：** ユーザーのターゲットを定義していない広告エクスペリエンスに個々のクリエイティブを直接含めることができます。 また、クリエイティブを使用してバンドルを作成し、ターゲット設定した [ 広告エクスペリエンス ](/help/creative/experiences/experience-about.md) に含めることもできます。

   * **標準クリエイティブ：** クリエイティブは [ 様々な形式 ](#creative-creative-formats) でアップロードおよび管理できます。 各クリエイティブに対して、クリエイティブに関連付ける各広告のデフォルトの言語、ユーザーがクリエイティブを含む広告をクリックすると開くデフォルトのランディングページ、[!DNL Creative] 内の様々なビューでフィルターとして使用するオプションのラベルを指定します。

   * **動的クリエイティブ：** （Adobe AdvertisingDCO のお客様のみ）管理者ユーザーは、広告テンプレート内の動的変数をフィードファイル内の値にマッピングすることで、動的に生成されたクリエイティブを作成できます。 すべてのユーザーは、既存の動的広告をプレビュー、複製および削除できます。

* **クリエイティブバンドル：** 定義済みのユーザターゲットを持つ複数のエクスペリエンスで使用するために、クリエイティブをバンドルにグループ化します。 標準広告で構成される *標準バンドル* と、動的に生成された広告で構成される *動的バンドル* を作成できます。

## サポートされるクリエイティブ形式 {#creative-creative-formats}

### 標準クリエイティブの形式

次のクリエイティブタイプを [ サポートされているクリエイティブサイズ ](creative-sizes.md) で追加および管理できます。

>[!IMPORTANT]
>
>広告エクスペリエンスに HTMl5、フレキシブルHTML5、またはサードパーティのクリエイティブを使用する場合でも、使用するクリエイティブサイズごとに画像クリエイティブを追加する必要があります。
>
>各エクスペリエンスには、エクスペリエンスに割り当てられるクリエイティブサイズごとにデフォルトの画像クリエイティブが必要です。 デフォルトの画像クリエイティブは、ブラウザーがJavaScriptに対応していない場合や、遅延のために広告サーバーが広告をパーソナライズできない場合に使用されます。

#### 柔軟なHTML5

フレキシブルHTML5 クリエイティブは、すべての画像とその他の属性を標準のHTMLタグとして持つHTML5 のクリエイティブで、クリエイティブライブラリ内または個々のエクスペリエンス内で [!DNL Creative] 内で直接編集できます（元のクリエイティブのバリエーションを作成します）。 柔軟なHTML5 クリエイティブは、インタラクティブAdvertisingビューロー（IAB）テクノロジーラボの [ 広告ポートフォリオ ](https://flexibleads.iabtechlab.com/) の標準を使用しています。広告フォーマットのサイズは固定ではなく柔軟で、広告の縦横比とサイズ範囲に基づいており、デバイスやパブリッシャーサイトをまたいで解像度を維持する広告です。

また、フレキシブルHTML5 のクリエイティブを ZIP ファイル <!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point --> としてアップロードすること <!-- either --> できます。 [ フレキシブルHTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

<!-- Will flattening the view be possible in the MVP?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

オプションで、フレキシブルHTML5 クリエイティブで指定した属性のデフォルト値を変更できます。 後で、特定のエクスペリエンス内の属性にカスタム値を指定して、親クリエイティブのバリエーションを作成できます。

#### HTML5 クリエイティブ

すべての属性と画像を指定したシンプルまたは静的なHTML5 のクリエイティブを ZIP ファイルとしてアップロードできます。 属性を編集したり、画像を追加したりすることはできません。代わりに、新しい ZIP ファイルをアップロードして、新しいクリエイティブを追加してください。 [ シンプルで静的なHTML5 のクリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

#### 画像クリエイティブ

画像クリエイティブは、GIF、JPEG、JPGまたは PNG 形式で含めることができます。 デバイスまたはネットワークから <!--LATER:   images from your Adobe Experience Manager accounts or --> の画像をアップロードできます。

各広告エクスペリエンスには、エクスペリエンスに割り当てられるクリエイティブサイズごとにデフォルトの画像クリエイティブが必要です。

#### サードパーティクリエイティブ

サードパーティの広告サーバーでホストされているクリエイティブのJavaScript トラッキングタグを入力します。 スクリプトは広告サーバーによって異なります。次に例を示します。

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### 動的広告の形式

アドアドテンプレート内の動的HTMLをフィードファイル内の値にマッピングすることで、静的HTML5 形式および動的変数 5 形式で動的に生成されたクリエイティブを作成できます。 これには、従来のAdobe AdvertisingDynamic Creative Optimization（DCO）エクスペリエンスからのクリエイティブが含まれる場合があります。

## [!UICONTROL Creative Libraries] ビュー

各ビューのカスタマイズについて詳しくは、「[ データビューのカスタマイズ ](/help/creative/introduction/customize-data-views.md)」を参照してください。

### [!UICONTROL Creative Libraries] のメインビュー

[!UICONTROL Creative Libraries] のメインビューには、すべてのクリエイティブライブラリが表示されます。 各ライブラリのデータには、ライブラリのバンドルが割り当てられたエクスペリエンスの数、バンドルの数、クリエイティブの数、クリエイティブサイズの数、デフォルトの言語ターゲットの数、作成日、ライブラリの要素の最終変更日が含まれます。 テーブルモードには、広告主用の列も含まれます。

#### 使用可能なアクション

* ライブラリの新規作成

* クリエイティブライブラリごとに、次の手順を実行します。

   * ライブラリ名を編集

   * ライブラリを開いて、ライブラリに割り当てられたクリエイティブとバンドルを表示します

   * ライブラリの削除

### [!UICONTROL Creative Libraries]/[!UICONTROL Creatives] ビュー

#### [!UICONTROL Standard Ads]

「[!UICONTROL Standard Ads]」タブには、作成したすべての標準クリエイティブが表示されます。 各クリエイティブのデータには、クリエイティブサイズ、クリエイティブタイプ、作成日が含まれます。 テーブルモードには、デフォルト言語の列とデフォルトのランディングページの列も含まれます。

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

「[!UICONTROL Dynamic Ads]」タブには、クリエイティブカタログに対して動的に作成されたすべての動的クリエイティブが表示されます。ただし、「[!UICONTROL Dynamic Ads]」タブから [ 手動で削除 ](creative-delete.md) した動的クリエイティブは表示されません。 カタログが最後に処理されて以降に動的なクリエイティブを [ 手動で複製 ](creative-duplicate.md) した場合、そのカタログのクリエイティブのリストには、重複したクリエイティブも含まれます。

各クリエイティブのデータには、クリエイティブタイプ、クリエイティブサイズ、クリエイティブが属するカタログの数、作成日が含まれます。 テーブルモードには、クリエイティブの生成時に使用したテンプレートの列とオファー数も含まれます。

>[!NOTE]
>
>カタログが処理されるたびに、そのカタログの既存の動的クリエイティブのデータが更新されます。

##### 使用可能なアクション

動的なクリエイティブを作成および編集する機能は、現在、Adobeアカウントチームのみが使用できます。 ただし、すべてのユーザーが次の操作を行うことができます。

* [動的クリエイティブのプレビュー](creative-preview.md)

* [ダイナミックバンドルにダイナミッククリエイティブを追加し、ダイナミックバンドルからダイナミッククリエイティブを削除](creative-attach-detach-bundles.md)

* [動的クリエイティブの複製](creative-duplicate.md)

* [動的クリエイティブの削除](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries]/[!UICONTROL Bundles] ビュー

[!UICONTROL Bundles] ビューには、標準および動的バンドルコンテナがすべて表示されます。 各バンドルに含まれているクリエイティブの名前、クリエイティブのサイズ、言語を確認できます。

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
