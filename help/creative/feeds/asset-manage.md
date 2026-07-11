---
title: アセットファイルの管理
description: 広告主向けのアセットファイルをアップロードおよび管理する方法について説明します。
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
TQID: https://experienceleague.adobe.com/U8KSnvef-wUsj6AzRuPUdPpf1xHjZp3Ae7zxXnMfMUc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d32c0462696cdd11b4e4a184bed683c611d018c0
workflow-type: tm+mt
source-wordcount: 617
ht-degree: 0%

---

# アセットファイルの管理

* ダイナミック HTML5広告には、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルと、スプレッドシートで参照される実際の画像アセットが必要です。

* 静的なHTML5の広告では、1つの広告につき1つの画像アセットしか必要ありません。

* ビデオ広告には、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルと、スプレッドシートで参照される実際のビデオアセットが必要です。

>[!NOTE]
>
> 各フィードファイルは1つのカタログにのみ使用できます。

## ファイル要件

最大データ行：200万

最大ファイルサイズ：2 GB

* ダイナミックHTML5広告：

   * CSV、TSV、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイル。各広告バリエーションに1つのヘッダー行と1つのデータ行が含まれている。 `images/image_name`形式（`images/300x250_acme_logo.png`など）を使用して、各行に画像名を含めます。

     広告主固有のフィールド名は、動的な広告フィード ファイル [&#128279;](/help/creative/appendix-available-feed-fields.md)の利用可能なフィールドにマッピングする必要があります。

   * GIF、JPEG、JPG、またはPNG形式の関連する画像アセット。 最大ファイルサイズは10 MBです。 [&#x200B; サポートされているクリエイティブサイズ &#x200B;](/help/creative/creative-libraries/creative-sizes.md)を参照してください。

  1つのXLSX ファイル、1つの画像ファイル、またはXLSXと画像ファイルの任意の組み合わせを含む1つのZIP ファイルをアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 静的なHTML5広告：

   * GIF、JPG、JPEG、PNG形式の広告ごとに1つの画像アセット。

     1つの画像または複数の画像を1つのZIP ファイルにアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* ダイナミック動画広告：

   * CSV、TSV、Microsoft Excel スプレッドシート（XLSX）形式のフィードファイル。各広告バリエーションに1つのヘッダー行と1つのデータ行が含まれている。 `videos/image_name`形式（`videos/300x250_acme_logo.png`など）を使用して、各行にビデオ名を含めます。 ZIP ファイルは、最大512 MB、最大500行までです。

     広告主固有のフィールド名は、動的な広告フィード ファイル [&#128279;](/help/creative/appendix-available-feed-fields.md)の利用可能なフィールドにマッピングする必要があります。

     ダイナミック ビデオを使用しているすべてのアカウントの場合、ベストプラクティスは、アセット ファイルと[&#x200B; ユニバーサル フィード テンプレート [!UICONTROL Adobe Creative Template]](feed-template-manage.md)のコピーを使用してカタログ [&#128279;](catalog-manage.md)を作成し、アセット ファイルの各フィールドをAdvertising Creative バックエンドのフィールドにマッピングすることです。

   * 関連するビデオアセットをMP4、MOV、またはWEBM形式で保存します。 対応している広告テンプレートには、開始カード、終了カード、上オーバーレイ、下オーバーレイ、L字型などがあります。 各ビデオのデュレーションは1 ～ 90秒の間である必要があります。 [&#x200B; サポートされているクリエイティブサイズ &#x200B;](/help/creative/creative-libraries/creative-sizes.md)を参照してください。

  1つのXLSX ファイル、1つの画像ファイル、またはXLSXとビデオ ファイルの任意の組み合わせを含む1つのZIP ファイルをアップロードできます。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## アセットファイルのアップロード

>[!NOTE]
>
>アセットファイルをアップロードする代わりに、[動的なクリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-dynamic.md)するときに、カタログを直接アップロードすることもできます。 そこで作成したカタログは、今後の使用のために[!UICONTROL Catalogs] ビュー内で使用できるようになります。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]** > **[!UICONTROL Asset]**&#x200B;をクリックします。

1. アセットファイルを設定します。

   1. アセットファイルにアクセスできる広告主を選択します。

   1. 次のいずれかの方法でアセットファイルを指定します。

      * デバイスまたはネットワーク上のファイルをボックスにドラッグ&amp;ドロップします。

      * **[!UICONTROL Select a file]**&#x200B;をクリックして、デバイスまたはネットワーク上のファイルを見つけます。

   1. **[!UICONTROL Upload]**&#x200B;をクリックします。

すべてのZIP ファイルは自動的に解凍されます。 スプレッドシート ファイルをアップロードすると、そのファイルは[!UICONTROL Feeds] サブタブに一覧表示されます。 画像ファイルをアップロードすると、その画像ファイルは[!UICONTROL Images] サブタブに一覧表示されます。

## アセットファイルのダウンロード

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセット行の上にカーソルを置き、**[!UICONTROL Download]**&#x200B;をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## アセットファイルの削除

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Assets]**」タブをクリックします。

1. アセット行の上にカーソルを置き、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [動的な広告フィード ファイルの使用可能なフィールド &#x200B;](/help/creative/appendix-available-feed-fields.md)
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; フィード テンプレートの管理](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; カタログの管理](/help/creative/feeds/catalog-manage.md)
>* [動的広告テンプレートの管理](/help/creative/ad-templates/ad-template-manage.md)
>* [&#x200B; クリエイティブライブラリに動的なクリエイティブを追加](/help/creative/creative-libraries/creative-add-dynamic.md)
