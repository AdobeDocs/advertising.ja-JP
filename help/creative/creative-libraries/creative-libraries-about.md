---
title: クリエイティブライブラリについて
description: 広告体験のためのクリエイティブの管理について詳しく見る。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
TQID: https://experienceleague.adobe.com/rvm3BAkRlgbJKdpHNoN5oH9sOhqGwOA-3I-XIol0RXc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1586
ht-degree: 0%

---

# クリエイティブライブラリについて

クリエイティブライブラリでは、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成できます。各ライブラリには、一連のクリエイターと&#x200B;*クリエイティブバンドル*&#x200B;が含まれており、これらは1つのユニットとしてエクスペリエンスに追加できるクリエイターのグループです。

ライブラリには、次のものが含まれます。

* **個々のクリエイター：** ユーザーターゲットが定義されていない広告エクスペリエンス内で、個々のクリエイターを直接含めることができます。 クリエイティブを使用してバンドルを作成し、対象となる[広告エクスペリエンス &#x200B;](/help/creative/experiences/experience-about.md)に含めることもできます。

   * **標準クリエイティブ：** [様々な形式](#creative-creative-formats)でクリエイティブをアップロードおよび管理できます。 各クリエイティブについて、クリエイティブを関連付ける各広告のデフォルトの言語と、ユーザーがクリエイティブを含む広告をクリックしたときに開くデフォルトのランディングページを指定します。 [!DNL Creative]内の様々なビュー内のフィルターとして使用するラベルと、[!UICONTROL Custom Creative Report] ディメンションを使用する場合は[!UICONTROL Creative Label]の列値として使用するラベルをオプションで指定できます。

   * **動的なクリエイティブ：**&#x200B;広告テンプレートの動的変数をフィードファイルの値にマッピングすることで、動的に生成されたクリエイティブを作成できます。 すべてのユーザーは、既存の動的広告をプレビュー、複製、削除できます。

* **クリエイティブバンドル：** クリエイターをバンドルにグループ化して、定義されたユーザーターゲットを持つ複数のエクスペリエンスで使用します。 標準ディスプレイ広告で構成される&#x200B;*標準ディスプレイバンドル*、標準ビデオ広告で構成される&#x200B;*標準ビデオバンドル*、動的に生成されるディスプレイ広告で構成される&#x200B;*動的ディスプレイバンドル*、動的に生成されるビデオ広告で構成される&#x200B;*動的ビデオバンドル*&#x200B;を作成できます。

## サポートされているクリエイティブ形式 {#creative-creative-formats}

### 標準的なクリエイティブの形式

[&#x200B; サポートされるクリエイティブサイズ &#x200B;](creative-sizes.md)で、次のクリエイティブタイプを追加および管理できます。

>[!IMPORTANT]
>
>* 標準的なディスプレイ広告エクスペリエンスにHTML5、Flexible HTML5、サードパーティ製のクリエイティブを使用する場合でも、使用する各クリエイティブサイズに合わせて画像クリエイティブも追加する必要があります。
>* 標準的な表示エクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブサイズごとに、デフォルトの画像クリエイティブが必要です。 デフォルトの画像クリエイターは、ブラウザーがJavaScriptに対応していない場合や、広告サーバーが遅延のために広告をパーソナライズできない場合に使用されます。
>* 標準ビデオ エクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブ期間ごとに、デフォルトのビデオ クリエイティブが必要です。<!-- when is it used? -->

#### 柔軟なHTML5

柔軟なHTML5 クリエイターは、すべての画像とその他の属性を標準のHTML タグとして持つHTML5 クリエイターです。このタグは、[!DNL Creative]内で、クリエイティブライブラリ内または個々のエクスペリエンス内（元のクリエイティブのバリエーションを作成）で直接編集できます。 DSPでは、HTML5の柔軟なクリエイティブツールが、特定の広告サイズ（ピクセル単位）に対応しています。 オプションで、フレキシブル HTML5 クリエイティブで指定された属性のデフォルト値を変更できます。 その後、特定のエクスペリエンス内の属性にカスタム値を指定して、親クリエイティブのバリエーションを作成できます。

柔軟性の高いHTML 5のクリエイティブをZIP ファイルとしてアップロードするか、アカウントで利用可能なテンプレートのいずれかをベースとして使用できます。 柔軟性に優れたHTML 5 クリエイティブの[仕様](html5-creative-specification.md)を参照してください。

#### 標準の表示クリエイティブ

標準的なディスプレイ広告には次のものが含まれます。

* HTML5のクリエイティブをローカルまたはAdobe GenStudio for Performance Marketingからアップロードします。
* ローカルまたはAdobe Experience Managerからアップロードされた画像ファイル。

##### HTML5のクリエイティブ

* **GenStudio エクスペリエンス：** [GenStudio for Performance Marketing](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences)の[&#x200B; ディスプレイ広告エクスペリエンス &#x200B;](https://experienceleague.adobe.com/ja/docs/genstudio-for-performance-marketing/user-guide/home)からすべての広告バリエーションを個々のHTML5 クリエイターとして読み込むことができます。 外部リンクはローカル参照に変換されます。 HTML コンテンツは最大20 MB、個々の画像は最大50 MBです。

  GenStudio エクスペリエンスを読み込むと、読み込んだクリエイティブのメタデータ（名前、言語、タグ）は編集できますが、クリエイティブコンテンツは編集できません。 GenStudio内でGenStudio エクスペリエンスを編集する場合は、[!DNL Creative]でエクスペリエンスを再インポートして最新バージョンを使用します。

  >[!NOTE]
  >
  >この機能を使用するには、GenStudio アカウントとAdvertising Creative アカウントの両方で同じ組織IDを使用し、ユーザーがGenStudioにアクセスするための権限を持っている必要があります。

* **アップロードしたファイル：**&#x200B;すべての属性と画像を指定したシンプルまたは静的なHTML5 クリエイティブをZIP ファイルとしてアップロードすることもできます。 属性を編集したり画像を追加したりすることはできません。代わりに、新しいクリエイティブを追加するために新しいZIP ファイルをアップロードしてください。 シンプルで静的なHTML5 クリエイター[については、](html5-creative-specification.md)仕様を参照してください。

##### 画像クリエイター

GIF、JPEG、JPG、またはPNG形式で画像クリエイティブを含めることができます。 承認済みの画像は、Adobe Experience Manager アカウントからアップロードすることも、デバイスやネットワークからアップロードすることもできます。

標準的なディスプレイ広告エクスペリエンスごとに、エクスペリエンスに割り当てられたクリエイティブサイズごとに、デフォルトの画像クリエイティブが必要です。

#### サードパーティのクリエイティブ

そこで、JavaScriptのトラッキングタグの出番です。 スクリプトは広告サーバーによって異なります。次に例を示します。

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### 動画クリエイター {#creative-video-specs}

web、モバイル、コネクテッド TV用の1st パーティビデオのクリエイティブを、デバイスやネットワークからアップロードできます。 各動画広告エクスペリエンスには、エクスペリエンスに割り当てられたクリエイティブ期間ごとに、デフォルトの動画クリエイティブが必要です。 DSPでは、すべてのビデオクリエイティブがVAST 2.0 タグとして自動的にトランスコードされるので、プレビューできます。 [!UICONTROL Tag Manager]では、オプションで[DSP固有のトランスコーディング &#x200B;](/help/creative/experiences/experience-tag-video-transcoding.md)を任意のビデオ広告エクスペリエンスタグに適用できます。

次のビデオクリエイティブ要件を参照してください。 **注：** ビデオ エクスペリエンスをAdvertising DSPにアップロードする場合は、[DSPの高精細ビデオの要件](https://experienceleague.adobe.com/ja/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets)も参照してください。これは、より制限されている可能性があります。

**ファイルの種類：** .mov、.mp4、.webm

**ファイルサイズ：**&#x200B;最大512 MB

**ビデオ縦横比：** 16:9、4:3

**ビデオ解像度：** 640x360 （360p）、1280x720 （720p）、1920x1080 （1080p）

**ビデオの長さ：**&#x200B;最大90秒

**ビットレート：** 360pでは600 ～ 1200 kbps、720pでは1500 ～ 2500 kbps、1080pでは3000 ～ 5000+ kbps

**ビデオフレームレート：** 23.98 FPS 地域またはパブリッシャーの要件に基づいて、追加のフレームレートを受け入れることができます

**ビデオコーデック：** H.264 （業界標準）、AV1、H.265

**オーディオ形式：** ACC （業界標準/MP4）、Opus （WebM/AV1）

**音声ビットレート：** 16 ～ 512 kbps

**オーディオサンプルレート：** 44100-48000 Hz

**音声レート：** 44.1kHzまたは48 kHz

**オーディオその他：** アップロードするファイルは、インターレースなし、混在、オーディオトラックが含まれている必要があります。 音声が聞こえない場合もありますが、ビデオファイルにオーディオトラックを含める必要があります。

### 動的広告用のフォーマット

広告テンプレートの動的変数をフィードファイルの値にマッピングすることで、ディスプレイまたはビデオのクリエイティブを動的に生成できます。 動的なクリエイターには、従来のAdobe Advertising Dynamic Creative Optimization（DCO）エクスペリエンスから移行されたクリエイターが含まれる場合があります。

#### 動的な表示クリエイティブ

ダイナミック表示のクリエイティブは、GIF、JPG、JPEG、またはPNG形式の画像を含むHTML 5形式です。

#### 動的な動画クリエイティブ

ダイナミック動画クリエイティブには、通常の動画クリエイティブと同じ仕様の動画ファイルが含まれます。 「[&#x200B; ビデオクリエイティブ &#x200B;](#creative-video-specs)」を参照してください。

サポートされている広告フォーマットには、開始カード、終了カード、トップオーバーレイ、ボトムオーバーレイ、L字型などがあります。

## [!UICONTROL Creative Libraries] ビュー

各ビューのカスタマイズについて詳しくは、「[&#x200B; データビューのカスタマイズ &#x200B;](/help/creative/introduction/customize-data-views.md)」を参照してください。

### [!UICONTROL Creative Libraries] メインビュー

[!UICONTROL Creative Libraries] メインビューには、すべてのクリエイティブライブラリが表示されます。 各ライブラリのデータには、ライブラリのバンドルが割り当てられるエクスペリエンスの数、バンドルの数、クリエイティブの数、クリエイティブサイズの数、デフォルトの言語ターゲットの数、作成日、ライブラリの任意の要素に対する最終変更日が含まれます。 テーブルモードには、広告主用の列も含まれます。

カードモードの場合は、&lt; ボタンと> ボタンを使用して、複数のクリエイターでライブラリ内の画像をスクロールできます。

#### 使用可能なアクション

* [新しいライブラリを作成](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* 各クリエイティブライブラリについて：

   * [ライブラリ名の編集](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [ライブラリを開き、ライブラリに割り当てられたクリエイティブとバンドルを表示します](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [ライブラリの削除](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] ビュー

#### [!UICONTROL Standard Ads]

「[!UICONTROL Standard Ads]」タブには、作成したすべての標準クリエイティブが表示されます。 各クリエイティブのデータには、クリエイティブサイズ、クリエイティブタイプ、作成日が含まれます。 テーブルモードには、デフォルト言語とデフォルトのランディングページの列も含まれます。

##### 使用可能なアクション

* [標準クリエイティブをライブラリに追加](creative-add-standard.md)

* [標準クリエイティブの編集](creative-edit-standard.md)

* [標準クリエイティブのプレビュー](creative-preview.md)

* [標準クリエイターを標準ディスプレイバンドルに追加し、標準クリエイターを標準ディスプレイバンドルから削除する](creative-attach-detach-bundles.md)

* [ビデオクリエイティブを標準ビデオバンドルに追加し、標準ビデオバンドルからビデオクリエイティブを削除する](creative-attach-detach-bundles.md)

* [標準クリエイティブの複製](creative-duplicate.md)

* [標準のクリエイティブをダウンロード](creative-download.md)

* [標準クリエイティブの削除](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

「[!UICONTROL Dynamic Ads]」タブには、クリエイティブカタログ用に動的に作成されたすべての動的クリエイターが表示されます。ただし、[&#x200B; タブから](creative-delete.md)手動で[!UICONTROL Dynamic Ads]削除した動的クリエイターは表示されません。 動的なクリエイティブ [を](creative-duplicate.md)手動で<!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed -->複製した場合、そのカタログのクリエイターのリストには、複製されたクリエイターも含まれます。

各クリエイティブのデータには、クリエイティブタイプ、クリエイティブサイズ、クリエイティブが属するカタログ数、作成日が含まれます。 テーブルモードには、クリエイティブが生成された広告テンプレートとオファー数の列も含まれます。

>[!NOTE]
>
>カタログが処理されるたびに、そのカタログの既存の動的クリエイターのデータが更新されます。<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### 使用可能なアクション

* [ライブラリへの動的クリエイターの追加](creative-add-dynamic.md)

* [ダイナミッククリエイティブの編集](creative-edit-dynamic.md)

* [動的なクリエイティブのプレビュー](creative-preview.md)

* [動的なクリエイターを動的なディスプレイバンドルに追加し、動的なクリエイターを動的なディスプレイバンドルから削除する](creative-attach-detach-bundles.md)

* [動的なクリエイティブの複製](creative-duplicate.md)

* [動的なクリエイティブの削除](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] ビュー

[!UICONTROL Bundles] ビューには、すべての標準バンドルコンテナと動的バンドルコンテナが表示されます。 各バンドルに含まれるクリエイティブのクリエイティブ名、クリエイティブサイズ、言語を確認できます。 カードモードの場合は、&lt; ボタンと> ボタンを使用して、複数のクリエイターを含むバンドル内の画像をスクロールできます。

#### 使用可能なアクション

* 標準ディスプレイ、標準ビデオ、および動的ディスプレイバンドルをライブラリに追加する

* バンドル内のクリエイティブのリストとプレビュー

* バンドル名の編集

* 標準ディスプレイクリエイティブを標準ディスプレイバンドルに追加し、標準ディスプレイクリエイティブを標準ディスプレイバンドルから削除する

* 標準ビデオバンドルに標準ビデオクリエイティブを追加し、標準ビデオバンドルから標準ビデオクリエイティブを削除します

* 重複したバンドル

* バンドルの削除

>[!MORELIKETHIS]
>
>* [&#x200B; クリエイティブライブラリの管理](/help/creative/creative-libraries/creative-library-manage.md)
>* [標準クリエイティブをライブラリに追加](creative-add-standard.md)
>* [&#x200B; クリエイティブバンドルの管理](bundle-manage.md)
>* [&#x200B; データビューのカスタマイズ &#x200B;](/help/creative/introduction/customize-data-views.md)
