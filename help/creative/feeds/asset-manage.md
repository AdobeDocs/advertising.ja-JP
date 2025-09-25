---
title: アセットファイルの管理
description: 広告主用のアセットファイルをアップロードおよび管理する方法について説明します。
feature: Creative Dynamic Creatives
source-git-commit: ed0fe4849c1db933f1c68a49fc848acd7c74af5b
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# アセットファイルの管理

Dynamic HTML5 広告には、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルとスプレッドシートで参照される画像アセットの両方が必要です（Adobe Experience Manager アセット参照を除く）。 静的HTML5 広告では、広告ごとに 1 つの画像アセットのみが必要です。

>[!NOTE]
>
> 各フィードファイルは、1 つのカタログにのみ使用できます。

## ファイル要件

* ダイナミック HTML5 広告：

   * Microsoft Excel スプレッドシート（XLSX）形式のフィードファイル。広告バリエーションごとに 1 つのヘッダー行と 1 つのデータ行があります。 各行に画像名またはAdobe Experience Managerへの参照を含めます。<!-- need spec of available column names that the user-created header names must map to; need to reference it in feed template topic too, so make it a separate file/appendix. -->

     アップロードする画像については、形式 `images/image_name` （`images/300x250_acme_logo.png` など）を使用して画像を参照し <!-- Verify.  Also need to include the spec for how to reference images in AEM --> す。

   * JPEG、JPGまたは PNG 形式の関連する画像アセット。<!-- NOT GIF still? And is this true: The maximum file size is two (2) MB. --> [ サポートされているクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md) を参照してください。

  単一の XLSX ファイル、単一の画像ファイル、または XLSX と画像ファイルの任意の組み合わせを含む単一の ZIP ファイルをアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 静的HTML5 広告：

   * JPG、JPEGまたは PNG 形式の広告ごとに 1 つの画像アセット。

     ZIP ファイルに 1 つの画像または複数の画像をアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## アセットファイルのアップロード

>[!NOTE]
>
>アセットファイルをアップロードする代わりに、[ クリエイティブライブラリにダイナミッククリエイティブを追加 ](/help/creative/creative-libraries/creative-add-dynamic.md) する際に、カタログを直接アップロードすることもできます。 ここで作成したカタログは、後で使用するために [!UICONTROL Catalogs] ビュー内で使用できます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]**/**[!UICONTROL Asset]** をクリックします。

1. アセットファイルを設定します。

   1. アセットファイルにアクセスできる広告主を選択します。

   1. 次のいずれかの方法でアセットファイルを指定します。

      * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

      * **[!UICONTROL Select a file]** をクリックして、デバイスまたはネットワーク上のファイルを探します。

   1. 「**[!UICONTROL Upload]**」をクリックします。

すべての ZIP ファイルは自動的に解凍されます。 スプレッドシートファイルをアップロードすると、そのファイルが「[!UICONTROL Feeds]」サブタブに表示されます。 画像ファイルをアップロードすると、画像ファイルが「[!UICONTROL Images]」サブタブに表示されます。

## アセットファイルのダウンロード

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセット行の上にカーソルを置き、**[!UICONTROL Download]** をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## アセットファイルの削除

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセット行の上にカーソルを置き、**[!UICONTROL Delete]** をクリックします。

>[!MORELIKETHIS]
>
>* [ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ フィードテンプレートの管理 ](/help/creative/feeds/feed-template-manage.md)
>* [ カタログの管理 ](/help/creative/feeds/catalog-manage.md)
>* [ 動的広告テンプレートの管理 ](/help/creative/ad-templates/ad-template-manage.md)
>* [ クリエイティブライブラリへのダイナミッククリエイティブの追加 ](/help/creative/creative-libraries/creative-add-dynamic.md)
