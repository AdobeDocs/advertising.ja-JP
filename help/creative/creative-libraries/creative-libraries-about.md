---
title: クリエイティブライブラリについて
description: 広告エクスペリエンスのクリエイティブの管理について説明します。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 24846adba9ff856571d117261f44aff408e70c50
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# クリエイティブライブラリについて

クリエイティブライブラリを使用すると、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成できます。各ライブラリには、一連のクリエイティブと、1 つのユニットとしてエクスペリエンスに追加できるクリエイティブのグループである *クリエイティブバンドル* が含まれます。

ライブラリには、次のものが含まれます。

* **個々のクリエイティブ：** ユーザーのターゲットを定義していない広告エクスペリエンスに個々のクリエイティブを直接含めることができます。 また、クリエイティブを使用してバンドルを作成し、ターゲット設定した [ 広告エクスペリエンス ](/help/creative/experiences/experience-about.md) に含めることもできます。

   * **標準クリエイティブ：** クリエイティブは [ 様々な形式 ](#creative-creative-formats) でアップロードおよび管理できます。 各クリエイティブに対して、クリエイティブを関連付ける各広告のデフォルトの言語と、ユーザーがクリエイティブを含む広告をクリックすると開くデフォルトのランディングページを指定します。 オプションで、[!DNL Creative] ディメンションの使用を含める場合、[!UICONTROL Custom Creative Report] 内の様々なビュー内のフィルターとして、および [!UICONTROL Creative Label] の列値として使用するラベルを指定できます。

   * **動的クリエイティブ：** 広告テンプレート内の動的変数をフィードファイルの値にマッピングすることで、動的に生成されたクリエイティブを作成できます。 すべてのユーザーは、既存の動的広告をプレビュー、複製および削除できます。

* **クリエイティブバンドル：** 定義済みのユーザターゲットを持つ複数のエクスペリエンスで使用するために、クリエイティブをバンドルにグループ化します。 標準のディスプレイ広告で構成される *標準のディスプレイバンドル*、標準のビデオ広告で構成される *標準のビデオバンドル*、動的に生成されたディスプレイ広告で構成される *動的なディスプレイバンドル* を作成できます。

## サポートされるCreative形式 {#creative-creative-formats}

### 標準クリエイティブの形式

次のクリエイティブタイプを [ サポートされているクリエイティブサイズ ](creative-sizes.md) で追加および管理できます。

>[!IMPORTANT]
>
>* 標準のディスプレイ広告エクスペリエンスにHTML5、フレキシブル HTML5、またはサードパーティのクリエイティブを使用する場合でも、使用するクリエイティブサイズごとに画像クリエイティブを追加する必要があります。
>* 標準のディスプレイエクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブサイズごとにデフォルトの画像クリエイティブが必要です。 デフォルトの画像クリエイティブは、ブラウザーがJavaScriptに対応していない場合や、遅延のために広告サーバーが広告をパーソナライズできない場合に使用されます。
>* 標準のビデオエクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブ期間ごとにデフォルトのビデオクリエイティブが必要です。<!-- when is it used? -->

#### 柔軟なHTML5

柔軟なHTML5 クリエイティブは、HTML5 のすべての画像とその他の属性を標準のHTML タグとして持つクリエイティブで、クリエイティブライブラリ内または個々のエクスペリエンス内で [!DNL Creative] 内で直接編集できます（元のクリエイティブのバリエーションを作成します）。 DSPでは、フレキシブル HTML5 のクリエイティブは、1 つの特定の広告サイズ（ピクセル単位）に対応しています。 オプションで、フレキシブル HTML5 クリエイティブで指定した属性のデフォルト値を変更できます。 後で、特定のエクスペリエンス内の属性にカスタム値を指定して、親クリエイティブのバリエーションを作成できます。

柔軟なHTML5 クリエイティブを ZIP ファイルとしてアップロードするか、アカウントで使用可能なテンプレートの 1 つを出発点として使用できます。 詳しくは、[ フレキシブル HTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

#### 標準の表示クリエイティブ

標準のディスプレイ広告には、次のものが含まれます。

* HTML5 のクリエイティブがローカルまたはAdobe GenStudio for Performance Marketingからアップロードされている。
* ローカルまたはAdobe Experience Managerからアップロードされた画像ファイル。

##### HTML5 クリエイティブ

* **GenStudio エクスペリエンス：** [GenStudio for Performance Marketingの ](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences) ディスプレイ広告エクスペリエンス [ からすべての広告のバリエーションをHTML5 クリエイティブとして読み込む ](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) とができます。 外部リンクはローカル参照に変換されます。 HTMLのコンテンツのサイズは最大 20 MB で、個々の画像のサイズは最大 50 MB です。

  この機能を使用するには、GenStudio アカウントとAdvertising Creative アカウントの両方が同じ組織 ID を使用する必要があり、ユーザーはGenStudioにアクセスするための権限を持っている必要があります。

  GenStudio エクスペリエンスを読み込んだら、読み込んだクリエイティブのメタデータ（名前、言語、タグ）を編集できますが、クリエイティブコンテンツを編集することはできません。 GenStudio内でGenStudioのエクスペリエンスを編集する場合は、最新バージョンを使用する [!DNL Creative] めに、エクスペリエンスを再度読み込みます。

* **アップロードされたファイル：** すべての属性と画像が指定されたシンプルまたは静的なHTML5 クリエイティブを ZIP ファイルとしてアップロードすることもできます。 属性を編集したり、画像を追加したりすることはできません。代わりに、新しい ZIP ファイルをアップロードして、新しいクリエイティブを追加してください。 [ シンプルで静的なHTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

##### 画像クリエイティブ

GIF、JPEG、JPG、PNG 形式の画像クリエイティブを含めることができます。 Adobe Experience Manager アカウントから承認済みの画像を、またはデバイスやネットワークから画像をアップロードできます。

標準のディスプレイ広告エクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブサイズごとにデフォルトの画像クリエイティブが必要です。

#### サードパーティクリエイティブ

サードパーティの広告サーバーでホストされているクリエイティブのJavaScript トラッキングタグを入力します。 スクリプトは広告サーバーによって異なります。次に例を示します。

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### ビデオクリエイティブ {#creative-video-specs}

デバイスやネットワークから、web、モバイル、接続テレビ用のファーストパーティビデオクリエイティブをアップロードできます。 標準のビデオ広告エクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブ期間ごとにデフォルトのビデオクリエイティブが必要です。 DSPでは、すべてのビデオクリエイティブを自動的に VAST 2.0 タグにトランスコードして、プレビューできます。 ま [!UICONTROL Tag Manager]、任意のビデオ広告エクスペリエンスタグに対して、オプションで [DSP固有のトランスコーディングを適用 ](/help/creative/experiences/experience-tag-video-transcoding.md) できます。

次のビデオクリエイティブの要件を参照してください。 **注意：** ビデオエクスペリエンスをAdvertising DSPにアップロードする場合は、DSPの [ 高精細ビデオAssetsの要件 ](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets) も参照してください。この要件は制限される場合があります。

**ファイルタイプ：** .mov、.mp4、.webm

**ファイルサイズ：** 最大 512 MB

**ビデオの縦横比：** 16:9、4:3

**ビデオ解像度：** 360p の場合は 640 x 360、720p の場合は 1280 x 720、1080p の場合は 1920 x 1080

**ビデオ長：** 最大 90 秒

**ビットレート：** 360p の場合は 600～1200 kbps、720p の場合は 1500～2500 kbps、1080p の場合は 3000～5000+ kbps

**ビデオフレームレート：** 23.98 FPS。 追加のフレームレートは、地域またはパブリッシャーの要件に応じて受け入れることができます

**ビデオコーデック：** H.264 （業界標準）、AV1、H.265

**音声形式：** ACC （業界標準/MP4）、Opus （WebM/AV1）

**オーディオビットレート：** 16～512 kbps

**音声サンプルレート：** 44100～48000 Hz

**音声レート：** 44.1kHz または 48kHz

**Audio Other:** アップロードするファイルは、ノンインターレースおよび混在のファイルであり、オーディオトラックを含んでいる必要があります。 音声がない場合がありますが、音声トラックをビデオファイルに含める必要があります。

### 動的広告の形式

広告テンプレートの動的変数をフィードファイルの値にマッピングすることで、静的HTML5 形式および動的HTML5 形式でクリエイティブを動的に生成できます。 動的なクリエイティブには、従来のAdobe Advertising Dynamic Creative Optimization（DCO）エクスペリエンスから移行したクリエイティブが含まれる場合があります。

## [!UICONTROL Creative Libraries] ビュー

各ビューのカスタマイズについて詳しくは、「[ データビューのカスタマイズ ](/help/creative/introduction/customize-data-views.md)」を参照してください。

### [!UICONTROL Creative Libraries] のメインビュー

[!UICONTROL Creative Libraries] のメインビューには、すべてのクリエイティブライブラリが表示されます。 各ライブラリのデータには、ライブラリのバンドルが割り当てられたエクスペリエンスの数、バンドルの数、クリエイティブの数、クリエイティブサイズの数、デフォルトの言語ターゲットの数、作成日、ライブラリの要素の最終変更日が含まれます。 テーブルモードには、広告主用の列も含まれます。

カードモードの場合、&lt; および > ボタンを使用して、複数のクリエイティブでライブラリ内の画像をスクロールできます。

#### 使用可能なアクション

* [新しいライブラリの作成](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* クリエイティブライブラリごとに、次の手順を実行します。

   * [ライブラリ名の編集](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [ライブラリを開いて、ライブラリに割り当てられたクリエイティブとバンドルを表示します](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [ライブラリの削除](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### [!UICONTROL Creative Libraries]/[!UICONTROL Creatives] ビュー

#### [!UICONTROL Standard Ads]

「[!UICONTROL Standard Ads]」タブには、作成したすべての標準クリエイティブが表示されます。 各クリエイティブのデータには、クリエイティブサイズ、クリエイティブタイプ、作成日が含まれます。 テーブルモードには、デフォルト言語の列とデフォルトのランディングページの列も含まれます。

##### 使用可能なアクション

* [ライブラリへの標準クリエイティブの追加](creative-add-standard.md)

* [標準クリエイティブの編集](creative-edit-standard.md)

* [標準クリエイティブのプレビュー](creative-preview.md)

* [標準ディスプレイのバンドルに標準クリエイティブを追加し、標準ディスプレイのバンドルから標準クリエイティブを削除します](creative-attach-detach-bundles.md)

* [標準ビデオバンドルにビデオクリエイティブを追加し、標準ビデオバンドルからビデオクリエイティブを削除します](creative-attach-detach-bundles.md)

* [標準クリエイティブの複製](creative-duplicate.md)

* [標準クリエイティブのダウンロード](creative-download.md)

* [標準クリエイティブを削除](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

「[!UICONTROL Dynamic Ads]」タブには、クリエイティブカタログに対して動的に作成されたすべての動的クリエイティブが表示されます。ただし、「[」タブから ](creative-delete.md) 手動で削除 [!UICONTROL Dynamic Ads] した動的クリエイティブは表示されません。 [ 手動で複製 ](creative-duplicate.md) 動的なクリエイティブ <!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed --> を作成した場合、そのカタログのクリエイティブのリストには重複したクリエイティブも含まれます。

各クリエイティブのデータには、クリエイティブタイプ、クリエイティブサイズ、クリエイティブが属するカタログの数、作成日が含まれます。 テーブルモードには、クリエイティブの生成時に使用した広告テンプレートの列とオファー数も含まれます。

>[!NOTE]
>
>カタログが処理されるたびに、そのカタログの既存の動的クリエイティブのデータが更新されます。<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### 使用可能なアクション

* [ライブラリへのダイナミッククリエイティブの追加](creative-add-dynamic.md)

* [動的クリエイティブの編集](creative-edit-dynamic.md)

* [動的クリエイティブのプレビュー](creative-preview.md)

* [動的ディスプレイバンドルに動的クリエイティブを追加し、動的ディスプレイバンドルから動的クリエイティブを削除します](creative-attach-detach-bundles.md)

* [動的クリエイティブの複製](creative-duplicate.md)

* [動的クリエイティブの削除](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries]/[!UICONTROL Bundles] ビュー

[!UICONTROL Bundles] ビューには、標準および動的バンドルコンテナがすべて表示されます。 各バンドルに含まれているクリエイティブの名前、クリエイティブのサイズ、言語を確認できます。 カードモードの場合、&lt; および > ボタンを使用して、複数のクリエイティブでバンドル内の画像をスクロールできます。

#### 使用可能なアクション

* 標準ディスプレイ、標準ビデオ、動的ディスプレイのバンドルをライブラリに追加します

* バンドル内のクリエイティブのリストとプレビュー

* バンドル名を編集

* 標準表示バンドルに標準表示クリエイティブを追加し、標準表示バンドルから標準表示クリエイティブを削除します

* 標準ビデオバンドルに標準ビデオクリエイティブを追加し、標準ビデオバンドルから標準ビデオクリエイティブを削除します

* 重複するバンドル

* バンドルを削除

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリの管理 ](/help/creative/creative-libraries/creative-library-manage.md)
>* [ クリエイティブライブラリへの標準クリエイティブの追加 ](creative-add-standard.md)
>* [ クリエイティブバンドルの管理 ](bundle-manage.md)
>* [ データビューのカスタマイズ ](/help/creative/introduction/customize-data-views.md)
