---
title: クリエイティブライブラリへの標準クリエイティブの追加
description: クリエイティブライブラリに標準（非ダイナミック）クリエイティブを追加する方法を説明します。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 24846adba9ff856571d117261f44aff408e70c50
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# クリエイティブライブラリへの標準クリエイティブの追加

標準の [&#x200B; 広告エクスペリエンス &#x200B;](creative-library-manage.md) で使用するには、標準のクリエイティブを [&#x200B; クリエイティブライブラリ &#x200B;](/help/creative/experiences/experience-about.md) に追加します。

>[!NOTE]
>
> ユーザーのターゲットが定義されていない広告エクスペリエンスに、個々のクリエイティブを直接含めることができます。 また、クリエイティブを [&#x200B; バンドル &#x200B;](bundle-manage.md) にグループ化して、ターゲット設定された広告エクスペリエンスに含めることもできます。

## クリエイティブライブラリへの柔軟なHTML広告の追加 {#flexible-creative-add}

次のいずれかを実行できます。

* 独自のフレキシブルクリエイティブを ZIP ファイルにアップロードします。

* アカウントにアップロードした事前定義済みのフレキシブルクリエイティブテンプレートを、独自のフレキシブルクリエイティブの出発点として使用します。

### 独自の柔軟なクリエイティブをアップロード {#flexible-creative-upload}

複数の柔軟なクリエイティブユニットをアップロードできます。 柔軟なクリエイティブは、ZIP 形式で、最大 2 MB にする必要があります。 ファイル要件については、[HTML5 クリエイティブの仕様 &#x200B;](html5-creative-specification.md) を参照してください。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL Flexible]** をクリックします。

1. 「**[!UICONTROL Upload New]**」をクリックします。

1. 次のいずれかの方法で ZIP ファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * **[!UICONTROL Select a file]** をクリックして、デバイスまたはネットワーク上のファイルを探します。

   [&#x200B; フレキシブル広告仕様 &#x200B;](#flexible-ad-spec) を参照してください。

1. 柔軟なクリエイティブファイルを追加または削除します。

   * ファイルを追加するには、左上の ![&#x200B; 追加 &#x200B;](/help/creative/assets/create.png " 追加 ") をクリックし、デバイスまたはネットワーク上のファイルを探します。

   * ファイルを削除するには、横にあるチェックボックスの選択を解除します。

1. （任意）クリエイティブをプレビューするには、画像の上の ![&#x200B; プレビュー &#x200B;](/help/creative/assets/preview.png " プレビュー ") をクリックします。

1. [&#x200B; フレキシブル HTML5 広告の設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) を指定します。

   デフォルトでは、アップロードしたばかりのクリエイティブがすべて選択されます。 値が 1 つだけの設定は、選択したすべてのクリエイティブに適用されます。一部の設定では、個々の値を指定できます。 特定のクリエイティブの設定を入力するには、適用できない各クリエイティブの横にあるチェックボックスの選択を解除します。

1. **[!UICONTROL Create]** をクリック

### テンプレートを使用した柔軟なクリエイティブの追加 {#flexible-creative-use-template}

アカウントにアップロードされた任意の柔軟なクリエイティブテンプレートを使用して、事前定義済みのサイズの広告を作成できます。 使用するテンプレートを選択したら、クリックのタグと属性を編集します。&lt;!— テンプレートのダウンロード機能を追加する場合は、最後の文をこの文に置き換えます。a\）使用するテンプレートを選択して、クリックのタグと属性を編集するか、b\） [&#x200B; テンプレートを ZIP ファイルとしてダウンロード &#x200B;](#download-flexible-creative-template)、コンテンツをオフラインで編集して独自のクリエイティブを作成してから [ 編集したファイルを新しいクリエイティブとしてアップロード ] (flexible-creative-upload)。>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL Flexible]** をクリックします。

1. 「**[!UICONTROL Browse System Flexible Templates]**」をクリックします。

1. （オプション）テンプレートをプレビューするには、テンプレート名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Preview]**」をクリックします。

   必要に応じて、テンプレートをダウンロードできます。テンプレート名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Download]**」をクリックします。

1. テンプレート名の横の「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Use Selected]**」をクリックします。

1. [&#x200B; フレキシブル HTML5 クリエイティブ設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) を編集して、言語を指定し、独自のクリックタグ、画像、その他の属性を含めます。

   クリエイティブの最大ファイルサイズは、圧縮されると、2 MB になります。<!-- Still true? -->

1. 独自の柔軟なクリエイティブファイルを追加または削除します。

   * デバイスまたはネットワークからファイルを追加するには、左上の ![&#x200B; 追加 &#x200B;](/help/creative/assets/create.png " 追加 ") をクリックしてファイルを探します。 クリエイティブの横にあるチェックボックスをオンにし、他のクリエイティブの横にあるチェックボックスの選択を解除して、[&#x200B; フレキシブル HTML5 クリエイティブ設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) を編集し、言語を指定し、独自のクリックタグ、画像、その他の属性を含めます。

   * ファイルを削除するには、横にあるチェックボックスの選択を解除します。

1. （任意）クリエイティブをプレビューするには、画像の上の ![&#x200B; プレビュー &#x200B;](/help/creative/assets/preview.png " プレビュー ") をクリックします。

1. 「**[!UICONTROL Create]**」をクリックします。

## クリエイティブライブラリへの標準ディスプレイクリエイティブの追加

標準の表示クリエイティブには、画像クリエイティブや、Adobe Experience ManagerやAdobe GenStudio for Performance Marketingから読み込んだクリエイティブを含むHTML5 クリエイティブが含まれます。

* 画像クリエイティブは、GIF、JPEG、JPG、PNG のいずれかの形式になります。 最大ファイルサイズは 2 MB です。 [&#x200B; サポートされるクリエイティブサイズ &#x200B;](/help/creative/creative-libraries/creative-sizes.md) を参照してください。

* 複数のExperience Manager アセット、複数のGenStudio エクスペリエンスまたは複数のローカル HTML5 クリエイティブを一度に 1 つのタイプ（シンプルまたは静的）で追加できます。 HTML5 のクリエイティブについては、[HTML5 広告仕様 &#x200B;](/help/creative/creative-libraries/html5-creative-specification.md) を参照してください。

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>また、[&#x200B; 柔軟なHTML5 クリエイティブを追加 &#x200B;](#flexible-creative-add) することもできます。これは、[!DNL Creative] 内で直接編集できる標準のHTML タグとしてすべての属性を持つHTML5 クリエイティブです。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL Standard Display]** をクリックします。

1. クリエイティブを指定します。

   * ローカル画像またはHTML5 アセットの場合は、次のいずれかを行います。

      * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

      * [**[!UICONTROL Select a file]**] をクリックして、デバイスまたはネットワーク上のファイルを検索します。

   * DSP アカウントに接続された [Experience Manager ライブラリの承認済み画像の場合 &#x200B;](/help/creative/creative-libraries/aem-assets-configure.md)、次の操作を行います。

      1. 「**[!UICONTROL AEM Asset Library]**」をクリックします。

      1. （Experience Manager アカウントにまだログインしていない場合） Experience Manager アカウントにログインします。

      1. [!UICONTROL Assets] ビューまたは [!UICONTROL Collections] ビューでファイルを見つけて選択し、右上の [**[!UICONTROL Select]**] をクリックします。

         <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * GenStudio エクスペリエンスの場合、次の操作を行います。

      1. 「**[!UICONTROL GenStudio Library]**」をクリックします。

      1. （GenStudio アカウントにまだログインしていない場合） GenStudio アカウントにログインします。

         ディスプレイ広告エクスペリエンスは、デフォルトで表示されます。 オプションで、必要に応じてキャンペーンやその他の属性でエクスペリエンスをフィルタリングできます。

      1. ディスプレイ広告エクスペリエンスを探して選択し、右上の「**[!UICONTROL Select]**」をクリックします。

         <!-- Each creative variant in the experience will be imported as a separate HTML5 creative. -->

1. クリエイティブを追加または削除：

   * 画像を追加するには、左上の ![&#x200B; 追加 &#x200B;](/help/creative/assets/create.png " 追加 ") をクリックし、デバイスまたはネットワーク上のファイルを探します。

   * 画像を削除するには、横にあるチェックボックスの選択を解除します。

1. [HTML5 クリエイティブ設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5) または [&#x200B; 画像クリエイティブ設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image) を指定します。

   デフォルトでは、アップロードしたクリエイティブがすべて選択され、指定した設定は選択したすべてのクリエイティブに適用されます。 値が 1 つだけの設定は、選択したすべてのクリエイティブに適用されます。 特定のクリエイティブの設定を入力するには、適用できない各クリエイティブの選択を解除します。

1. **[!UICONTROL Create]** または **[!UICONTROL Import]** をクリックします。

## クリエイティブライブラリへのサードパーティクリエイティブの追加 {#creative-add-third-party}

[!DNL Creative] は、ほとんどのサードパーティの広告サーバーでホストされているクリエイティブに対してJavaScriptのトラッキングタグをサポートしています。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL 3rd Party]** をクリックします。

1. [&#x200B; サードパーティのクリエイティブ設定 &#x200B;](#creative-settings-third-party) で、JavaScript タグとその他のクリエイティブ設定を指定します。

   任意の [&#x200B; 使用可能なマクロ &#x200B;](/help/creative/creative-macros.md) をコピーして、JavaScriptのタグに貼り付けることができます。

1. **[!UICONTROL Create]** をクリック

## クリエイティブライブラリへのビデオクリエイティブの追加

詳しくは、[&#x200B; ビデオクリエイティブの仕様 &#x200B;](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs) および [&#x200B; サポートされるクリエイティブサイズ &#x200B;](/help/creative/creative-libraries/creative-sizes.md) を参照してください。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL Video]** をクリックします。

1. 次のいずれかの方法でビデオファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * [**[!UICONTROL Select a file]**] をクリックして、デバイスまたはネットワーク上のファイルを検索します。

1. [&#x200B; ビデオクリエイティブ設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video) を指定します。

   デフォルトでは、アップロードしたクリエイティブが選択され、指定した設定は選択したクリエイティブに適用されます。<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. **[!UICONTROL Create]** をクリック

>[!MORELIKETHIS]
>
>* [&#x200B; 標準クリエイティブを編集 &#x200B;](/help/creative/creative-libraries/creative-edit-standard.md)
>* [&#x200B; 標準のクリエイティブ設定 &#x200B;](/help/creative/creative-libraries/creative-settings-standard.md)
>* [URL をトラッキングするために使用可能なマクロ &#x200B;](/help/creative/creative-macros.md)
>* [&#x200B; サポートされるクリエイティブサイズ &#x200B;](/help/creative/creative-libraries/creative-sizes.md)
>* [&#x200B; クリエイティブのプレビュー &#x200B;](/help/creative/creative-libraries/creative-preview.md)
>* [&#x200B; クリエイティブをバンドルに添付して分離する &#x200B;](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [&#x200B; クリエイティブライブラリについて &#x200B;](/help/creative/creative-libraries/creative-libraries-about.md)
>* [&#x200B; クリエイティブライブラリの管理 &#x200B;](/help/creative/creative-libraries/creative-library-manage.md)
