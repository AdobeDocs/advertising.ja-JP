---
title: アセットファイルの管理
description: 広告主用のアセットファイルをアップロードおよび管理する方法について説明します。
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# アセットファイルの管理

Dynamic HTML5 広告には、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルとスプレッドシートで参照される画像アセットの両方が必要です（Adobe Experience Manager アセット参照を除く）。 静的HTML5 広告では、広告ごとに 1 つの画像アセットのみが必要です。


>[!NOTE]
>
> 各フィードファイルは、1 つのカタログにのみ使用できます。

## ファイル要件

* ダイナミック HTML5 広告：

   * 広告バリエーションごとに 1 つのヘッダー行と 1 つのデータ行を持つ、CSV、TSV またはMicrosoft Excel スプレッドシート（XLSX）形式のフィードファイル。 形式 `images/image_name` を使用して、各行に画像名を含めます（`images/300x250_acme_logo.png` など）。

     広告主固有のフィールド名は、[&#x200B; 動的広告フィードファイルで使用可能なフィールド &#x200B;](/help/creative/appendix-available-feed-fields.md) にマッピングする必要があります。

   * GIF、JPEG、JPGまたは PNG 形式の関連する画像アセット。<!-- Is this true: The maximum file size is two (2) MB. --> [&#x200B; サポートされているクリエイティブサイズ &#x200B;](/help/creative/creative-libraries/creative-sizes.md) を参照してください。

   * （オプション） MP4 または WEBM 形式のビデオアセット

  アップロードできるのは、1 つの XLSX ファイル、1 つの画像またはビデオファイル、または XLSX、画像およびビデオファイルの任意の組み合わせを含む 1 つの ZIP ファイルです。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 静的HTML5 広告：

   * GIF、JPG、JPEGまたは PNG 形式の広告ごとに 1 つの画像アセット。

     ZIP ファイルに 1 つの画像または複数の画像をアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## アセットファイルのアップロード

>[!NOTE]
>
>アセットファイルをアップロードする代わりに、[&#x200B; クリエイティブライブラリにダイナミッククリエイティブを追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) する際に、カタログを直接アップロードすることもできます。 ここで作成したカタログは、後で使用するために [!UICONTROL Catalogs] ビュー内で使用できます。

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
>* [&#x200B; 動的広告フィードファイルで使用可能なフィールド &#x200B;](/help/creative/appendix-available-feed-fields.md)
>* [&#x200B; 動的広告のワークフロー &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; フィードテンプレートの管理 &#x200B;](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; カタログの管理 &#x200B;](/help/creative/feeds/catalog-manage.md)
>* [&#x200B; 動的広告テンプレートの管理 &#x200B;](/help/creative/ad-templates/ad-template-manage.md)
>* [&#x200B; クリエイティブライブラリへのダイナミッククリエイティブの追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md)
