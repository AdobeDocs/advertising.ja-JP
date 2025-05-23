---
title: クリエイティブライブラリへの標準クリエイティブの追加
description: クリエイティブライブラリに標準（非ダイナミック）クリエイティブを追加する方法を説明します。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 38ba8473eae3df204f618eac1f20e605e57ece5a
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# クリエイティブライブラリへの標準クリエイティブの追加

*クローズドベータ版*

[ad experience](/help/creative/experiences/experience-about.md) で使用するクリエイティブを [ クリエイティブライブラリ ](creative-library-manage.md) に追加します。

>[!NOTE]
>
> ユーザーのターゲットが定義されていない広告エクスペリエンスに、個々のクリエイティブを直接含めることができます。 また、クリエイティブを [ バンドル ](bundle-manage.md) にグループ化して、ターゲット設定された広告エクスペリエンスに含めることもできます。

## クリエイティブライブラリへの柔軟なHTML広告の追加 {#flexible-creative-add}

次のいずれかを実行できます。

* 独自のフレキシブルクリエイティブを ZIP ファイルにアップロードします。

* アカウントにアップロードした事前定義済みのフレキシブルクリエイティブテンプレートを、独自のフレキシブルクリエイティブの出発点として使用します。

### 独自の柔軟なクリエイティブをアップロード {#flexible-creative-upload}

複数の柔軟なクリエイティブユニットをアップロードできます。 柔軟なクリエイティブは、ZIP 形式で、最大 2 MB にする必要があります。 ファイル要件については、[HTML5 クリエイティブの仕様 ](html5-creative-specification.md) を参照してください。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、「**[!UICONTROL Standard Ads]**」サブタブをクリックします。

1. **[!UICONTROL Create]**/**[!UICONTROL Creative]**/**[!UICONTROL Flexible]** をクリックします。

1. 「**[!UICONTROL Upload New]**」をクリックします。

1. 次のいずれかの方法で ZIP ファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * **[!UICONTROL select a file]** をクリックして、デバイスまたはネットワーク上のファイルを探します。

   [ フレキシブル広告仕様 ](#flexible-ad-spec) を参照してください。

1. 柔軟なクリエイティブファイルを追加または削除します。

   * ファイルを追加するには、左上の ![ 追加 ](/help/creative/assets/create.png " 追加 ") をクリックし、デバイスまたはネットワーク上のファイルを探します。

   * ファイルを削除するには、横にあるチェックボックスの選択を解除します。

1. [ フレキシブル HTML5 広告の設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) を指定します。

   デフォルトでは、アップロードしたばかりのクリエイティブがすべて選択されます。 値が 1 つだけの設定は、選択したすべてのクリエイティブに適用されます。一部の設定では、個々の値を指定できます。 特定のクリエイティブの設定を入力するには、適用できない各クリエイティブの横にあるチェックボックスの選択を解除します。

1. **[!UICONTROL Create]** をクリック

### テンプレートを使用した柔軟なクリエイティブの追加 {#flexible-creative-use-template}

アカウントにアップロードされた任意の柔軟なクリエイティブテンプレートを使用して、事前に定義されたサイズの広告を作成できます。 使用するテンプレートを選択したら、クリックのタグと属性を編集します。&lt;!— テンプレートのダウンロード機能を追加する場合は、最後の文をこの文に置き換えます。a\）使用するテンプレートを選択して、クリックのタグと属性を編集するか、b\） [ テンプレートを ZIP ファイルとしてダウンロード ](#download-flexible-creative-template)、コンテンツをオフラインで編集して独自のクリエイティブを作成してから [ 編集したファイルを新しいクリエイティブとしてアップロード ](flexible-creative-upload)。>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、「**[!UICONTROL Standard Ads]**」サブタブをクリックします。

1. **[!UICONTROL Create]**/**[!UICONTROL Creative]**/**[!UICONTROL Flexible]** をクリックします。

1. 「**[!UICONTROL Browse System Flexible Templates]**」をクリックします。

<!-- Not options as of 5/22/25:

1. In the left panel, select the creative size to see all available templates for that size.

1. Select the template:

   * In card view, click **[!UICONTROL ...]** next to the template name, and then click **[!UICONTROL Use Selected]**.
     
   * In table view, hold the cursor over the row and click **[!UICONTROL Use Selected]**.
-->

1. （オプション）テンプレートをプレビューするには、テンプレート名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Preview]**」をクリックします。

   オプションで、テンプレートをダウンロードできます

1. テンプレート名の横の「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Use Selected]**」をクリックします。

1. [ フレキシブル HTML5 クリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) を編集して、言語を指定し、独自のクリックタグ、画像、その他の属性を含めます。

   クリエイティブの最大ファイルサイズは、圧縮されると、2 MB になります。<!-- Still true? -->

1. 「**[!UICONTROL Create]**」をクリックします。

## クリエイティブライブラリへのHTML5 クリエイティブの追加

一度に 1 つのタイプ（シンプルまたは静的）の複数のHTML5 クリエイティブを追加できます。

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>また、[ 柔軟なHTML5 クリエイティブを追加 ](#flexible-creative-add) することもできます。これは、[!DNL Creative] 内で直接編集できる標準のHTML タグとしてすべての属性を持つHTML5 クリエイティブです。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、「**[!UICONTROL Standard Ads]**」サブタブをクリックします。

1. **[!UICONTROL Create]**/**[!UICONTROL Creative]**/**[!UICONTROL HTML5]** をクリックします。

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. 次のいずれかの方法でファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * **[!UICONTROL select a file]** をクリックして、デバイスまたはネットワーク上のファイルを探します。

   [HTML5 広告の仕様 ](/help/creative/creative-libraries/html5-creative-specification.md) を参照してください。

1. [HTML5 広告の設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5) を指定してください。

デフォルトでは、アップロードしたばかりのクリエイティブがすべて選択されます。 値が 1 つだけの設定は、選択したすべてのクリエイティブに適用されます。一部の設定では、個々の値を指定できます。 特定のクリエイティブの設定を入力するには、適用できない各クリエイティブの横にあるチェックボックスの選択を解除します。

1. **[!UICONTROL Create]** をクリック

## クリエイティブライブラリへの画像クリエイティブの追加

画像クリエイティブは、GIF、JPEG、JPG、PNG のいずれかの形式になります。 最大ファイルサイズは 2 MB です。 [ サポートされるクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md) を参照してください。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、「**[!UICONTROL Standard Ads]**」サブタブをクリックします。

1. **[!UICONTROL Create]**/**[!UICONTROL Creative]**/**[!UICONTROL Image]** をクリックします。

1. 画像を指定します。

   * ローカル画像アセットの場合は、次のいずれかの操作を行います。

      * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

      * [**[!UICONTROL select a file]**] をクリックして、デバイスまたはネットワーク上のファイルを検索します。

   * Adobe Experience Manager ライブラリ内の画像の場合、次の操作を行います。

      1. 「**[!UICONTROL AEM Asset Library]**」をクリックします。

      1. Experience Manager アカウントにログインします。

      1. [!UICONTROL Assets] ビューまたは [!UICONTROL Collections] ビューでファイルを見つけて選択し、右上の [**[!UICONTROL Select]**] をクリックします。

1. 画像の追加または削除：

   * 画像を追加するには、左上の ![ 追加 ](/help/creative/assets/create.png " 追加 ") をクリックし、デバイスまたはネットワーク上のファイルを探します。

   * 画像を削除するには、横にあるチェックボックスの選択を解除します。

1. [ 画像クリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image) を指定します。

   デフォルトでは、アップロードしたクリエイティブがすべて選択され、指定した設定は選択したすべてのクリエイティブに適用されます。 値が 1 つだけの設定は、選択したすべてのクリエイティブに適用されます。 特定のクリエイティブの設定を入力するには、適用できない各クリエイティブの選択を解除します。

1. **[!UICONTROL Create]** をクリック

## クリエイティブライブラリへのサードパーティクリエイティブの追加 {#creative-add-third-party}

[!DNL Creative] は、ほとんどのサードパーティの広告サーバーでホストされているクリエイティブに対してJavaScriptのトラッキングタグをサポートしています。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、「**[!UICONTROL Standard Ads]**」サブタブをクリックします。

1. **[!UICONTROL Create]**/**[!UICONTROL Creative]**/**[!UICONTROL 3rd Party]** をクリックします。

1. [ サードパーティのクリエイティブ設定 ](#creative-settings-third-party) で、JavaScript タグとその他のクリエイティブ設定を指定します。

   任意の [ 使用可能なマクロ ](/help/creative/creative-macros.md) をコピーして、JavaScriptのタグに貼り付けることができます。

1. **[!UICONTROL Create]** をクリック

>[!MORELIKETHIS]
>
>* [ 標準クリエイティブを編集 ](/help/creative/creative-libraries/creative-edit-standard.md)
>* [ 標準のクリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md)
>* [URL をトラッキングするために使用可能なマクロ ](/help/creative/creative-macros.md)
>* [ サポートされるクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md)
>* [ クリエイティブのプレビュー ](/help/creative/creative-libraries/creative-preview.md)
>* [ クリエイティブをバンドルに添付して分離する ](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [ クリエイティブライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md)
>* [ クリエイティブライブラリの管理 ](/help/creative/creative-libraries/creative-library-manage.md)
