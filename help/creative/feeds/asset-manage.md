---
title: アセットファイルの管理
description: 広告主用のアセットファイルをアップロードおよび管理する方法について説明します。
feature: Creative Dynamic Creatives
source-git-commit: af29637d42b9932933cd23a64d6a0e2b7084fa31
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# アセットファイルの管理

Dynamic HTML5 広告では、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルと、スプレッドシートで参照される画像アセットの両方が必要です。 静的HTML5 広告では、広告ごとに 1 つの画像アセットのみが必要です。


>[!NOTE]
>
> 各フィードファイルは、1 つのカタログにのみ使用できます。

## ファイル要件

* ダイナミック HTML5 広告：

   * 広告バリエーションごとに 1 つのヘッダー行と 1 つのデータ行を持つ、CSV、TSV またはMicrosoft Excel スプレッドシート（XLSX）形式のフィードファイル。 形式 `images/image_name` を使用して、各行に画像名を含めます（`images/300x250_acme_logo.png` など）。

     広告主固有のフィールド名は、[ 動的広告フィードファイルで使用可能なフィールド ](/help/creative/appendix-available-feed-fields.md) にマッピングする必要があります。

   * GIF、JPEG、JPGまたは PNG 形式の関連する画像アセット。<!-- Is this true: The maximum file size is two (2) MB. --> [ サポートされているクリエイティブサイズ ](/help/creative/creative-libraries/creative-sizes.md) を参照してください。

  単一の XLSX ファイル、単一の画像ファイル、または XLSX と画像ファイルの任意の組み合わせを含む単一の ZIP ファイルをアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 静的HTML5 広告：

   * GIF、JPG、JPEGまたは PNG 形式の広告ごとに 1 つの画像アセット。

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
>* [ 動的広告フィードファイルで使用可能なフィールド ](/help/creative/appendix-available-feed-fields.md)
>* [ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ フィードテンプレートの管理 ](/help/creative/feeds/feed-template-manage.md)
>* [ カタログの管理 ](/help/creative/feeds/catalog-manage.md)
>* [ 動的広告テンプレートの管理 ](/help/creative/ad-templates/ad-template-manage.md)
>* [ クリエイティブライブラリへのダイナミッククリエイティブの追加 ](/help/creative/creative-libraries/creative-add-dynamic.md)
