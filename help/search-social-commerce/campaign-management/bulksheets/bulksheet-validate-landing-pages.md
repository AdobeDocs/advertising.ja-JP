---
title: バルクシートファイル内のランディングページの検証
description: 単一アカウントのバルクシートファイルで宛先 URL を検証する方法を説明します。
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# バルクシートファイル内のランディングページの検証

*宛先 URL を持つアカウントのみ*

単一アカウントのバルクシートファイルで、すべての宛先 URL のランディングページを検証できます。 無効なページを示す任意のフレーズや URL を指定でき、オプションで、ランディングページのリダイレクトをエラーとしてレポートできます。 検索、ソーシャル、Commerceは、指定した条件とランディングページの有無をチェックします（ランディングページが見つからない場合、HTTP 404 または「見つかりません」のエラーが発生します）。

エラーが見つかると、検索、ソーシャル、Commerceは、元のバルクシートのすべての行と、無効なランディングページを含むすべての行のエラーメッセージを含むバルクシートエラーファイルを作成します。 エラーは [!UICONTROL EF Errors] 列に記録されます。 ファイル名規則は `<bulksheet name>__lpv_errors.<extension used for the bulksheet>` です。

後でファイルをダウンロードし、エラーを修正して、修正したファイルをアップロードし、修正したファイルを広告ネットワークアカウントに投稿できます。

>[!NOTE]
>
>* この機能では、「ベース URL/最終 URL」列の値は検証されません。
>* バルクシートファイルは、検証中やエラーが見つかった場合でも投稿できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Bulksheets]** をクリックします。

1. 検証する各ファイルの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Validate URLs]**] をクリックします。

1. ダイアログボックスで、フィールドに情報を入力し、「**[!UICONTROL Apply]**」をクリックします。

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** ランディングページの本文に、ページが無効であることを示すテキストを挿入します。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL Enter invalid landing pages(one per line):]** ランディングページとして無効なページの URL。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL User Agent:]** ランディングページ検証エージェントがランディングページが存在する Web サーバーに対して識別される方法。 デフォルトはデフォルトです。この属性は、エージェントによって表示されるビューを匿名の [!DNL Mozilla Firefox] ユーザーに対して行います。 Web サーバーが匿名の [!DNL Mozilla Firefox] ユーザーからの要求をブロックする場合は、別のエージェントの名前を入力します。 例えば、[!DNL Googlebot] の場合は `Googlebot/2.1;+http://www.google.com/bot.html` と入力します。

   **[!UICONTROL Report redirects as errors]:** ランディングページが別のページにリダイレクトされる場合（ランディングページが見つからない場合やサイトに代替ページが表示される場合など）は、ランディングページエラーファイルの [!UICONTROL ER Errors] 列にランディングページのリダイレクト先の URL が示されます。

タスクが開始されると、新しい行が [!UICONTROL Bulksheets view] に追加されます。 ファイルが作成されると、ファイルへのリンクを含むメール通知が送信されます。 コンパイルされたデータの量に応じて、メール通知は数分以上かかる場合があります。 ファイルをダウンロードして編集し、投稿用に再度アップロードするか、そのまま投稿できます。 ただし、ファイルの生成に失敗した場合は、エラーファイルが [!UICONTROL Bulksheet Management] ページに一覧表示され、エラーファイルへのリンクが記載されたメール通知が送信されます。

>[!NOTE]
>
>* 大きなファイルの場合、検証に時間がかかります。
>* 複数のキャンペーン用のバルクシートファイルには、最大 500,000 個のデータ行を含めることができます。 複数のキャンペーンのデータを生成し、結合されたデータが 500,000 行を超える場合、データは Campaign によって、`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv` などの名前を持つ 2 つ以上のファイルに分割されます。

>[!MORELIKETHIS]
>
>* [ バルクシートを使用した Campaign データの管理について ](bulksheet-about.md)
>* [ アップロードしたバルクシートおよびエラーファイルの削除 ](bulksheet-delete.md)
>* [ ポストバルクシートまたは修正されたエラーファイル ](bulksheet-post.md)
>* [ 進行中のバルクシート ジョブの停止 ](bulksheet-stop-job.md)
>* [ バルクシートまたは修正されたエラーファイルのアップロード ](bulksheet-upload.md)
>* [ 生成またはアップロードされたバルクシートファイルのエクスポート ](bulksheet-export.md)
