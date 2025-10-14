---
title: 動的広告テンプレートの管理
description: xxxx について説明します。
feature: Creative Templates
source-git-commit: ed0fe4849c1db933f1c68a49fc848acd7c74af5b
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# 動的広告テンプレートの管理

目的の広告フォーマットで圧縮したHTML5 ファイルをアップロードして、広告タイプ（静的HTML5 または動的HTML5）と広告サイズの組み合わせごとに個別の広告テンプレートを作成します。 動的なHTML5 広告の場合は、広告属性 <!-- more clarification? --> を含むファイルもアップロードします。

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## 動的広告テンプレートの作成

>[!NOTE]
>
>また、[&#x200B; クリエイティブライブラリにダイナミッククリエイティブを追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) する際に、動的広告テンプレートをアップロードすることもできます。 作成した広告テンプレートは、後で使用するために [!UICONTROL Ad Templates] ビュー内で使用できるようになります。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Ad Templates]** をクリックします。

1. 右上のをクリック **[!UICONTROL Create Ad Template]** ます

1. [ad テンプレート設定を指定してください &#x200B;](#ad-template-settings)

1. 「**[!UICONTROL Create]**」をクリックします。

## 動的広告テンプレートの編集

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Ad Templates]** をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Edit]** をクリックします。

1. [&#x200B; 広告テンプレート設定 &#x200B;](#ad-template-settings) を編集します。

1. 「**[!UICONTROL Save]**」をクリックします。

## 動的広告テンプレートのダウンロード

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Ad Templates]** をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Download]** をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## 動的広告テンプレートの削除

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Ad Templates]** をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Delete]** をクリックします。

1. 確認メッセージで、「**[!UICONTROL Delete]**.<!-- Confirm -->」をクリックします。

## 広告テンプレートからの動的広告の作成

>[!NOTE]
>
>また、クリエイティブライブラリ内から [&#x200B; クリエイティブライブラリにダイナミッククリエイティブを追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) することもできます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Ad Templates]** をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Create Dynamic Ad]** をクリックします。

   [!UICONTROL New Dynamic Ad] 画面では、「[!UICONTROL Ad Template Size]」、「[!UICONTROL Ad Template Type]」、「[!UICONTROL Ad Template]」フィールドが自動的に選択され、読み取り専用になります。

1. 動的広告設定を指定して [&#x200B; 動的広告を作成 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) します。

## 広告テンプレート設定 {#ad-template-settings}

### 広告テンプレートの詳細

**[!UICONTROL Advertiser]**: （既存のテンプレートの場合は読み取り専用）広告が生成される広告主。

**[!UICONTROL Ad Template Name]**：広告主の一意の広告テンプレート名。

**[!UICONTROL Ad Template Type]**: （既存のテンプレートの読み取り専用）広告テンプレートのフォーマット：*静的HTML5* または *動的HTML5*。

**[!UICONTROL Ad Template Size]**: （既存のテンプレートの場合は読み取り専用）テンプレートによって作成された広告のディメンション。

**[!UICONTROL Description]**:（任意）広告テンプレートを使用しているすべてのユーザーにとって役に立つ情報。

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### HTML5 zip

目的の広告フォーマットを持つ圧縮されたHTML5 ファイル。 既にファイルをアップロードしている場合は、ファイル名が表示されます。

[HTML5 クリエイティブの仕様 &#x200B;](/help/creative/creative-libraries/html5-creative-specification.md) を参照してください。

ファイルをアップロードするには：

1. 「**[!UICONTROL Upload HTML5 zip]**」をクリックします。

1. デバイスまたはネットワーク上でファイルを見つけます。

### （Dynamic HTML5 広告テンプレート）属性ファイル

<!-- EXPLAIN -->広告テンプレートの属性を含むファイル。 既にファイルをアップロードしている場合は、ファイル名が表示されます。

<!-- Add specs for this file type -->

ファイルをアップロードするには：

1. 「**[!UICONTROL Upload Attributes File]**」をクリックします。

1. デバイスまたはネットワーク上でファイルを見つけます。

>[!MORELIKETHIS]
>
>* [&#x200B; 動的広告のワークフロー &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; アセットファイルの管理 &#x200B;](/help/creative/feeds/asset-manage.md)
>* [&#x200B; フィードテンプレートの管理 &#x200B;](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; カタログの管理 &#x200B;](/help/creative/feeds/catalog-manage.md)
>* [&#x200B; クリエイティブライブラリへのダイナミッククリエイティブの追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md)

