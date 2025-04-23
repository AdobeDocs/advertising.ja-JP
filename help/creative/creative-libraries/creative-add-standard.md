---
title: クリエイティブライブラリへの標準クリエイティブの追加
description: クリエイティブライブラリに標準（非ダイナミック）クリエイティブを追加する方法を説明します。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 1ab83cfe82bde4a7b1a32cf3773cdce4738af497
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# クリエイティブライブラリへの標準クリエイティブの追加

*クローズドベータ版*

[ad experience](/help/creative/experiences/experience-about.md) で使用するクリエイティブを [ クリエイティブライブラリ ](creative-library-manage.md) に追加します。

>[!NOTE]
>
> ユーザーのターゲットが定義されていない広告エクスペリエンスに、個々のクリエイティブを直接含めることができます。 また、クリエイティブを [ バンドル ](bundle-manage.md) にグループ化して、ターゲット設定された広告エクスペリエンスに含めることもできます。

## クリエイティブライブラリへの柔軟なHTML広告の追加 {#flexible-creative-add}

<!-- Later:
You can do either of the following: 

* Upload your own flexible creatives in ZIP files.

* Use any of the predefined flexible creative templates as a starting point for your own flexible creative.

### Upload your own flexible creatives {#flexible-creative-upload}

-->

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

<!-- In a later phase:

### Add flexible creatives using a template {#flexible-creative-use-template}

You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads. Once you select a template to use, you'll edit the click tags and attributes.<!-- Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).>

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click the **[!UICONTROL Standard Ads]** subtab.

1. Click **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Browse System Flexible Templates]**.



[The following are old instructions; see how this works in the new UI]


1. In the left panel, select the creative size to see all available templates for that size.

1. Under the template name, click **[!UICONTROL Use This Creative]**.

1. Edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to include your own click tags, images, and other attributes.

   The maximum file size of the creative, once it's zipped, is 2 MB.[Will saving the creative zip it??]

1. (Optional) Once you've made your changes, click []()[add image] to preview the new creative. 

1. Click **[!UICONTROL Save]**.

-->

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

1. 次のいずれかの方法でファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * **[!UICONTROL select a file]** をクリックして、デバイスまたはネットワーク上のファイルを探します。
<!--  Verify wording and workflow and add when available:

   * Click **[!UICONTROL AEM Asset Library]** to locate a file in your Adobe Experience Manager library.
-->

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
