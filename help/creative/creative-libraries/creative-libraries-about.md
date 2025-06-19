---
title: クリエイティブライブラリについて
description: 広告エクスペリエンスのクリエイティブの管理について説明します。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 9782471837db19d14839027ea7a576484863bb69
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# クリエイティブライブラリについて

*クローズドベータ版機能*

クリエイティブライブラリを使用すると、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成できます。各ライブラリには、一連のクリエイティブと、1 つのユニットとしてエクスペリエンスに追加できるクリエイティブのグループである *クリエイティブバンドル* が含まれます。

ライブラリには、次のものが含まれます。

* **個々のクリエイティブ：** ユーザーのターゲットを定義していない広告エクスペリエンスに個々のクリエイティブを直接含めることができます。 また、クリエイティブを使用してバンドルを作成し、ターゲット設定した [ 広告エクスペリエンス ](/help/creative/experiences/experience-about.md) に含めることもできます。

   * **標準クリエイティブ：** クリエイティブは [ 様々な形式 ](#creative-creative-formats) でアップロードおよび管理できます。 各クリエイティブに対して、クリエイティブを関連付ける各広告のデフォルトの言語と、クリエイティブが含まれる広告をユーザーがクリックすると開くデフォルトのランディングページを指定します。 オプションで、[!UICONTROL Creative Label] ディメンションの使用を含める場合、[!DNL Creative] 内の様々なビュー内のフィルターとして、および [!UICONTROL Custom Creative Report] の列値として使用するラベルを指定できます。

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

柔軟なHTML5 クリエイティブは、HTML5 のすべての画像とその他の属性を標準のHTML タグとして持つクリエイティブで、クリエイティブライブラリ内または個々のエクスペリエンス内で [!DNL Creative] 内で直接編集できます（元のクリエイティブのバリエーションを作成します）。 DSPでは、フレキシブル HTML5 のクリエイティブは、1 つの特定の広告サイズ（ピクセル単位）に対応しています。 オプションで、フレキシブル HTML5 クリエイティブで指定した属性のデフォルト値を変更できます。 後で、特定のエクスペリエンス内の属性にカスタム値を指定して、親クリエイティブのバリエーションを作成できます。

柔軟なHTML5 クリエイティブを ZIP ファイルとしてアップロードするか、アカウントで使用可能なテンプレートの 1 つを出発点として使用できます。 詳しくは、[ フレキシブル HTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

#### HTML5 クリエイティブ

すべての属性と画像を指定したシンプルまたは静的なHTML5 クリエイティブを ZIP ファイルとしてアップロードできます。 属性を編集したり、画像を追加したりすることはできません。代わりに、新しい ZIP ファイルをアップロードして、新しいクリエイティブを追加してください。 [ シンプルで静的なHTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

#### 画像クリエイティブ

GIF、JPEG、JPG、PNG 形式の画像クリエイティブを含めることができます。 Adobe Experience Manager アカウントから承認済みの画像を、またはデバイスやネットワークから画像をアップロードできます。

各広告エクスペリエンスには、エクスペリエンスに割り当てられるクリエイティブサイズごとにデフォルトの画像クリエイティブが必要です。

#### サードパーティクリエイティブ

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

* [標準バンドルに標準クリエイティブを追加し、標準バンドルから標準クリエイティブを削除します](creative-attach-detach-bundles.md)

* [標準クリエイティブの複製](creative-duplicate.md)

* [標準クリエイティブのダウンロード](creative-download.md)

* [標準クリエイティブを削除](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

「[!UICONTROL Dynamic Ads]」タブには、クリエイティブカタログに対して動的に作成されたすべての動的クリエイティブが表示されます。ただし、「[!UICONTROL Dynamic Ads]」タブから [ 手動で削除 ](creative-delete.md) した動的クリエイティブは表示されません。 カタログが最後に処理されて以降の動的なクリエイティブを [ 手動で複製 ](creative-duplicate.md) した場合、そのカタログのクリエイティブのリストには重複したクリエイティブも含まれます。

各クリエイティブのデータには、クリエイティブタイプ、クリエイティブサイズ、クリエイティブが属するカタログの数、作成日が含まれます。 テーブルモードには、クリエイティブの生成時に使用したテンプレートの列とオファー数も含まれます。

>[!NOTE]
>
>カタログが処理されるたびに、そのカタログの既存の動的クリエイティブのデータが更新されます。

##### 使用可能なアクション

動的なクリエイティブを作成および編集する機能は、現在、Adobe アカウントチームのみが使用できます。 ただし、すべてのユーザーが次の操作を行うことができます。

* [動的クリエイティブのプレビュー](creative-preview.md)

* [ダイナミックバンドルにダイナミッククリエイティブを追加し、ダイナミックバンドルからダイナミッククリエイティブを削除](creative-attach-detach-bundles.md)

* [動的クリエイティブの複製](creative-duplicate.md)

* [動的クリエイティブの削除](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries]/[!UICONTROL Bundles] ビュー

[!UICONTROL Bundles] ビューには、標準および動的バンドルコンテナがすべて表示されます。 各バンドルに含まれているクリエイティブの名前、クリエイティブのサイズ、言語を確認できます。 カードモードの場合、&lt; および > ボタンを使用して、複数のクリエイティブでバンドル内の画像をスクロールできます。

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
