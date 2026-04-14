---
title: 標準クリエイティブをクリエイティブライブラリに追加
description: 標準（動的でない）クリエイティブをクリエイティブライブラリに追加する方法について説明します。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
TQID: https://experienceleague.adobe.com/mgUcE-E6LAIFFU8S5WrUceCQ6ZMSGF9tFkqEfnuKKSQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 2ec4c13497ef6b5373a36b1f75111322a3ef26d0
workflow-type: tm+mt
source-wordcount: 1068
ht-degree: 0%

---

# 標準クリエイティブをクリエイティブライブラリに追加

標準のクリエイティブを[ クリエイティブライブラリ ](creative-library-manage.md)に追加して、標準の[広告エクスペリエンス ](/help/creative/experiences/experience-about.md)で使用します。

>[!NOTE]
>
> ユーザーターゲットが定義されていない広告エクスペリエンスに、個々のクリエイターを直接含めることができます。 クリエイティブを[ バンドル ](bundle-manage.md)でグループ化して、ターゲット広告エクスペリエンスに含めることもできます。

## HTMLの柔軟な広告をクリエイティブライブラリに追加 {#flexible-creative-add}

次のいずれかを実行できます。

* ZIP ファイルに独自の柔軟なクリエイティブをアップロードします。

* アカウントにアップロードされた定義済みの柔軟なクリエイティブテンプレートを、独自の柔軟なクリエイティブの出発点として使用します。

### 独自の柔軟なクリエイターをアップロード {#flexible-creative-upload}

複数の柔軟なクリエイティブユニットをアップロードできます。 柔軟なクリエイターはZIP形式で、最大2 MBです。 ファイルの要件については、[HTML5 クリエイティブ仕様](html5-creative-specification.md)を参照してください。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**&#x200B;をクリックします。

1. **[!UICONTROL Upload New]**&#x200B;をクリックします。

1. 次のいずれかの方法でZIP ファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * **[!UICONTROL Select a file]**&#x200B;をクリックして、デバイスまたはネットワーク上のファイルを検索します。

   [柔軟な広告仕様](#flexible-ad-spec)を参照してください。

1. 柔軟なクリエイティブファイルを追加または削除する：

   * ファイルを追加するには、左上の「![追加](/help/creative/assets/create.png "追加")」をクリックし、デバイスまたはネットワーク上でファイルを見つけます。

   * ファイルを削除するには、そのファイルの横にあるチェックボックスの選択を解除します。

1. （オプション）クリエイティブをプレビューするには、画像の上にある![ プレビュー](/help/creative/assets/preview.png " プレビュー")をクリックします。

1. [ フレキシブル HTML5の広告設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)を指定します。

   デフォルトでは、アップロードしたばかりのクリエイティブがすべて選択されます。 1つの値のみを持つ設定は、選択したすべてのクリエイティブに適用されます。一部の設定では、個々の値を指定できます。 特定のクリエイティブの設定を入力するには、該当しない各クリエイティブの横にあるチェックボックスをオフにします。

1. **[!UICONTROL Create]**&#x200B;をクリック

### テンプレートを使用した柔軟なクリエイティブの追加 {#flexible-creative-use-template}

アカウントにアップロードされた柔軟なクリエイティブテンプレートを使用して、定義済みのサイズの広告を作成できます。 使用するテンプレートを選択したら、クリックタグと属性を編集します。

<!--
Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).
-->

<!--
 Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**&#x200B;をクリックします。

1. **[!UICONTROL Browse System Flexible Templates]**&#x200B;をクリックします。

1. （オプション）テンプレートをプレビューするには、テンプレート名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Preview]**&#x200B;をクリックします。

   オプションでテンプレートをダウンロードできます。テンプレート名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Download]**」をクリックします。

1. テンプレート名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Use Selected]**」をクリックします。

1. [ フレキシブル HTML5 クリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)を編集して、言語を指定し、独自のクリックタグ、画像、その他の属性を含めます。

   クリエイティブの最大ファイルサイズは、圧縮されると2 MBになります。<!-- Still true? -->

1. 独自の柔軟なクリエイティブファイルを追加または削除します。

   * デバイスまたはネットワークからファイルを追加するには、左上の「![追加](/help/creative/assets/create.png "追加")」をクリックして、ファイルを見つけます。 クリエイティブの横にあるチェックボックスをオンにし、他のクリエイティブの横にあるチェックボックスをオフにし、[柔軟なHTML5 クリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)を編集して、言語を指定し、独自のクリックタグ、画像、その他の属性を含めます。

   * ファイルを削除するには、そのファイルの横にあるチェックボックスの選択を解除します。

1. （オプション）クリエイティブをプレビューするには、画像の上にある![ プレビュー](/help/creative/assets/preview.png " プレビュー")をクリックします。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## 標準ディスプレイクリエイティブをクリエイティブライブラリに追加する

通常のディスプレイクリエイティブには、Adobe Experience ManagerやAdobe GenStudio for Performance Marketingから読み込んだクリエイティブを含む、画像やHTML5のクリエイティブが含まれます。

* 画像のクリエイティブは、GIF、JPEG、JPG、PNG形式で作成できます。 最大ファイルサイズは2 MBです。 [ サポートされているクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md)を参照してください。

* 一度に複数のExperience Manager アセット、複数のGenStudio エクスペリエンス、または1つのタイプ（シンプルまたは静的）の複数のローカル HTML 5 クリエイターを追加できます。 HTML5のクリエイティブについては、[HTML5広告の仕様](/help/creative/creative-libraries/html5-creative-specification.md)を参照してください。

<!--
 Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>また、[柔軟なHTML5 クリエイター](#flexible-creative-add)を追加することもできます。これは、[!DNL Creative]内で直接編集できる標準のHTML タグとしてすべての属性を持つHTML5 クリエイターです。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Standard Display]**&#x200B;をクリックします。

1. クリエイターを指定します。

   * ローカル画像またはHTML5 アセットの場合は、次のいずれかの操作を行います。

      * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

      * **[!UICONTROL Select a file]**&#x200B;をクリックして、デバイスまたはネットワーク上のファイルを検索します。

   * DSP アカウント [に接続された](/help/creative/creative-libraries/aem-assets-configure.md)Experience Manager ライブラリ内の承認済み画像の場合は、次の操作を行います。

      1. **[!UICONTROL AEM Asset Library]**&#x200B;をクリックします。

      1. （Experience Manager アカウントにまだログインしていない場合） Experience Manager アカウントにログインします。

      1. [!UICONTROL Assets]または[!UICONTROL Collections] ビューでファイルを見つけて選択し、右上の&#x200B;**[!UICONTROL Select]**&#x200B;をクリックします。

         <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * GenStudio エクスペリエンスの場合は、次の操作を行います。

      1. **[!UICONTROL GenStudio Library]**&#x200B;をクリックします。

      1. （GenStudio アカウントにまだログインしていない場合） GenStudio アカウントにログインします。

         ディスプレイ広告エクスペリエンスはデフォルトで表示されます。 必要に応じて、キャンペーンやその他の属性によってエクスペリエンスをフィルタリングすることもできます。

      1. ディスプレイ広告エクスペリエンスを見つけて選択し、右上の「**[!UICONTROL Select]**」をクリックします。

     選択したエクスペリエンスの各クリエイティブのバリエーションは、個別のHTML5 クリエイティブとして読み込まれます。

1. クリエイターを追加または削除する：

   * 画像を追加するには、左上の「![追加](/help/creative/assets/create.png "追加")」をクリックし、デバイスまたはネットワーク上でファイルを見つけます。

   * 画像を削除するには、その画像の横にあるチェックボックスの選択を解除します。

1. [HTML5 クリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)または[画像クリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)を指定します。

   デフォルトでは、アップロードしたばかりのクリエイティブエクスペリエンスまたはGenStudio エクスペリエンスがすべて選択され、指定した設定は選択したすべての項目に適用されます。 1つだけの値を持つ設定は、選択したすべての項目に適用されます。 特定のクリエイティブまたはGenStudio エクスペリエンスの設定を入力するには、該当しない各クリエイティブまたはエクスペリエンスの選択を解除します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## クリエイティブライブラリへのサードパーティクリエイティブの追加 {#creative-add-third-party}

[!DNL Creative]は、ほとんどのサードパーティ広告サーバーでホストされているクリエイターに対して、JavaScript トラッキングタグをサポートしています。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**&#x200B;をクリックします。

1. [ サードパーティのクリエイティブ設定](#creative-settings-third-party)で、クリエイティブのJavaScript タグとその他の設定を指定します。

   使用可能な[ マクロ ](/help/creative/creative-macros.md)のいずれかをJavaScript タグにコピーして貼り付けることができます。

1. **[!UICONTROL Create]**&#x200B;をクリック

## クリエイティブライブラリへのビデオクリエイティブの追加

[ ビデオクリエイティブの仕様](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs)と[ サポートされているクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md)を参照してください。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**&#x200B;をクリックします。

1. 次のいずれかの方法でビデオファイルを指定します。

   * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

   * **[!UICONTROL Select a file]**&#x200B;をクリックして、デバイスまたはネットワーク上のファイルを検索します。

1. [ ビデオクリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video)を指定します。

   デフォルトでは、アップロードしたクリエイティブが選択され、指定した設定は選択したクリエイティブに適用されます。<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. **[!UICONTROL Create]**&#x200B;をクリック

>[!MORELIKETHIS]
>
>* [標準クリエイティブの編集](/help/creative/creative-libraries/creative-edit-standard.md)
>* [標準クリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md)
>* [ クリエイティブの変更ログを表示](/help/creative/creative-libraries/creative-view-change-log.md)
>* [URLのトラッキングに使用できるマクロ ](/help/creative/creative-macros.md)
>* [ サポートされているクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md)
>* [ クリエイティブをプレビュー](/help/creative/creative-libraries/creative-preview.md)
>* [ バンドルからクリエイティブを添付および分離](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [ クリエイティブライブラリについて](/help/creative/creative-libraries/creative-libraries-about.md)
>* [ クリエイティブライブラリの管理](/help/creative/creative-libraries/creative-library-manage.md)
