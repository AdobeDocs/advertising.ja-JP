---
title: Creative Studioでのアセットの管理
description: Adobe Advertising Creativeの「Creative Studio Assets」タブで、アセットをアップロード、参照、管理する方法について説明します。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 292
ht-degree: 0%

---

# [!UICONTROL Creative Studio]のアセットの管理

*Beta機能*

画像、動画、オーディオ、フォントアセットをアップロードして広告テンプレートで参照し、広告生成セッション中にAI エージェントのチャットメッセージに添付できます。

## [!UICONTROL Creative Studio] > [!UICONTROL Assets] ビュー

「**[!UICONTROL Assets]**」タブには、既存のアセットがカード表示で一覧表示されます。

### 使用可能なアクション

<!--  * [Browse and search assets](#assets-search) -->

* [アセットのアップロード](#assets-upload)

* [アセット名の変更](#assets-rename)

* [アセットのダウンロード](#assets-download)

* [アセットの削除](#assets-delete)

<!--
Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.
-->

## アセットのアップロード {#assets-upload}

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. **[!UICONTROL Upload Assets]**&#x200B;をクリックします。

1. コンピューターまたはネットワークから1つ以上のファイルを選択します。

   次のファイルタイプがサポートされています。

   | タイプ | サポートされる形式 | 最大ファイルサイズ |
   | --- | --- | --- |
   | 画像 | JPG/JPEG、PNG、GIF、WebP、SVG | 10 MB |
   | ビデオ | MP4、MOV、AVI、WebM | 512 MB |
   | オーディオ | MP3、WAV、AAC、OGG | 50 MB |

   空のファイルとサポートされていないファイルタイプは、エラー通知で拒否されます。

   アセット名は、拡張子なしでアップロードされたファイル名として保存されます。 ファイル名のスペースと非ASCII文字はアンダースコアに置き換えられます（例えば、`My Logo.png`をアップロードすると、`My_Logo`という名前のアセットが作成されます）。 後でアセットの名前を変更することもできます。

<!--
(from Bob) Moved from above step. Content in your repo failed to publish, and I'm testing several possible issues. Comment syntax between steps is sometimes problematic.

Verified 2026-07-09 against creative-api TemplateMediaValidator.java (IMAGE_EXTENSIONS, VIDEO_EXTENSIONS, AUDIO_EXTENSIONS), which backs the /v1/creative/template-medias upload/initiate endpoint used by this tab. The Assets tab file input has no client-side accept restriction (TemplateBrowser.tsx) and relies entirely on this backend validator, so it is authoritative.


maybe later:

   | Fonts | TTF, OTF, WOFF, WOFF2 | 5 MB |
   
-->

## アセット名の編集 {#asset-rename}

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセットカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit name]**&#x200B;をクリックします。

1. アセット名を更新します。

   アセット名は最大512文字です。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

## アセットのダウンロード {#asset-download}

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセットカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Download]**&#x200B;をクリックします。

   アセットは、ブラウザーの通常の手順に従ってダウンロードされます。

## アセットの削除 {#asset-delete}

>[!NOTE]
>
>削除したアセットを再アクティブ化することはできません。

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセットカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising CreativeのCreative Studioについて](creative-studio-about.md)
>* [Creative Studioでテンプレートを管理](creative-studio-manage-templates.md)
>* [Creative Studioで標準広告を生成](creative-studio-manage-standard-ads.md)
