---
title: バルクシートファイル内のランディングページの検証
description: 単一アカウントのバルクシートファイルで宛先 URL を検証する方法について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# バルクシートファイル内のランディングページの検証

*宛先 URL のみのアカウント*

単一アカウントの一括送信シートファイルで、すべての宛先 URL のランディングページを検証できます。 無効なページを示すフレーズや URL を指定したり、オプションでランディングページのリダイレクトをエラーとしてレポートしたりできます。 検索、ソーシャル、コマースは、指定した条件および見つからないランディングページをチェックします（HTTP 404、または「見つかりません」エラーが発生します）。

エラーが見つかると、Search、Social、および Commerce は、元のバルクシートのすべての行と、無効なランディングページを持つすべての行のエラーメッセージを含むバルクシートエラーファイルを作成します。 エラーは、 [!UICONTROL EF Errors] 列。 ファイル名の命名規則は次のとおりです。 `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

後でファイルをダウンロードし、エラーを修正して、修正したファイルをアップロードして、修正したファイルを広告ネットワークアカウントに投稿できます。

>[!NOTE]
>
>* この機能では、「ベース URL/最終 URL 」列の値は検証されません。
>* バルクシートファイルは、検証中、またはエラーが見つかった場合にも投稿できます。


1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. 検証する各ファイルの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Validate URLs]**.

1. ダイアログボックスで、フィールドに情報を入力し、 **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** ランディングページの本文に含まれる、ページが無効であることを示すテキスト。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL Enter invalid landing pages(one per line):]** ランディングページとして無効なページの URL。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL User Agent:]** ランディングページの検証エージェントを、ランディングページが存在する Web サーバーに対して識別する方法。 デフォルトはです。これは、エージェントによって表示されるを匿名に属性付けします。 [!DNL Mozilla Firefox] ユーザー。 Web サーバーが匿名からの要求をブロックする場合 [!DNL Mozilla Firefox] ユーザー」を選択し、別のエージェントの名前を入力します。 例： [!DNL Googlebot]を入力して、 `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** ランディングページが別のページにリダイレクトされる場合（例えば、ランディングページが見つからず、サイトに代替ページが表示される場合）、 [!UICONTROL ER Errors] ランディングページのエラーファイルの列は、ランディングページのリダイレクト先の URL を示します。

タスクが開始されると、新しい行が [!UICONTROL Bulksheets view]. ファイルを作成すると、そのファイルへのリンクを含む電子メール通知が送信されます。 コンパイルされたデータの量に応じて、電子メール通知には数分以上かかる場合があります。 ファイルをダウンロードして編集し、投稿用に再度アップロードするか、そのまま投稿することができます。 ただし、ファイルの生成に失敗した場合は、エラーファイルが [!UICONTROL Bulksheet Management] ページに送信され、エラーファイルへのリンクが記載された電子メール通知が送信されます。

>[!NOTE]
>
>* サイズの大きいファイルの検証に時間がかかります。
>* 複数のキャンペーン用のバルクシートファイルには、最大 500,000 行のデータ行を含めることができます。 複数のキャンペーンのデータを生成し、結合されたデータが 500,000 行を超える場合、データはキャンペーンごとに 2 つ以上のファイル ( `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`など。


>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [アップロードしたバルクシートとエラーファイルを削除](bulksheet-delete.md)
>* [バルクシートの投稿または修正されたエラーファイル](bulksheet-post.md)
>* [進行中のバルクシートジョブを停止します](bulksheet-stop-job.md)
>* [バルクシートまたは修正済みエラーファイルのアップロード](bulksheet-upload.md)
>* [生成またはアップロードされたバルクシートファイルのエクスポート](bulksheet-export.md)

