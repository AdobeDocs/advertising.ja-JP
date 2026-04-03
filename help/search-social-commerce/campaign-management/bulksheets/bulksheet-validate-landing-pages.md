---
title: バルクシートファイルでのランディングページの検証
description: 単一アカウントのバルクシートファイルで宛先URLを検証する方法について説明します。
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/gHVP2daXHY2iS6uibwNj4IxQyFjQReIgR54As8nc9Y8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 532
ht-degree: 0%

---

# バルクシートファイルでのランディングページの検証

*宛先URLのみ*&#x200B;のアカウント

単一アカウントのバルクシートファイル内のすべての宛先URLのランディングページを検証できます。 無効なページを示すフレーズとURLを指定し、オプションでランディングページのリダイレクトをエラーとしてレポートできます。 Search, Social, &amp; Commerceは、指定した条件とランディングページが見つからない場合にチェックします（これにより、HTTP 404または「見つかりません」エラーが発生します）。

エラーが見つかった場合、Search, Social, &amp; Commerceは、元のバルクシート内のすべての行と、無効なランディングページを持つすべての行に対するエラーメッセージを含むバルクシート エラーファイルを作成します。 エラーは[!UICONTROL EF Errors]列に記録されます。 ファイル名規則は`<bulksheet name>__lpv_errors.<extension used for the bulksheet>`です。

後でファイルをダウンロードし、エラーを修正して修正したファイルをアップロードしてから、修正したファイルを広告ネットワークアカウントに投稿できます。

>[!NOTE]
>
>* この機能では、ベース URL/最終URL列の値は検証されません。
>* バルクシートファイルは、検証中やエラーが見つかった場合でも投稿することができます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. 検証する各ファイルの横にあるチェックボックスをオンにします。

1. データテーブルの上のツールバーで、**[!UICONTROL Validate URLs]**&#x200B;をクリックします。

1. ダイアログボックスで、フィールドに情報を入力し、**[!UICONTROL Apply]**&#x200B;をクリックします。

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** ランディングページの本文に、ページが無効であることを示すテキストが含まれています。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL Enter invalid landing pages(one per line):]** ランディングページとして無効なページのURL。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL User Agent:]** ランディングページの検証エージェントが、ランディングページが格納されているweb サーバーに対して識別される方法。 デフォルトはデフォルトで、エージェントによるビューは匿名の[!DNL Mozilla Firefox] ユーザーに属します。 Web サーバーが匿名[!DNL Mozilla Firefox] ユーザーからのリクエストをブロックする場合は、別のエージェントの名前を入力します。 例えば、[!DNL Googlebot]に対して、`Googlebot/2.1;+http://www.google.com/bot.html`と入力します。

   **[!UICONTROL Report redirects as errors]:** ランディングページが別のページにリダイレクトされる場合（ランディングページが見つからず、サイトに代替ページが表示される場合など）、ランディングページエラーファイルの[!UICONTROL ER Errors]列は、ランディングページがリダイレクトされるURLを示します。

タスクが開始されると、新しい行が[!UICONTROL Bulksheets view]に追加されます。 ファイルが作成されると、ファイルへのリンクを含むメール通知が送信されます。 収集されたデータ量によっては、メール通知に数分以上かかる場合があります。 ファイルをダウンロードして編集し、投稿のために再アップロードするか、ファイルをそのまま投稿できます。 ただし、ファイルの生成に失敗した場合は、エラーファイルが[!UICONTROL Bulksheet Management] ページに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 大きなファイルの検証には時間がかかります。
>* 複数のキャンペーンのバルクシートファイルには、最大500,000行のデータ行を含めることができます。 複数のキャンペーンのデータを生成し、結合データが500,000行を超える場合、データはキャンペーンごとに`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`などの名前の2つ以上のファイルに分割されます。

>[!MORELIKETHIS]
>
>* [ バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [ アップロードされたバルクシートとエラーファイルを削除](bulksheet-delete.md)
>* [ バルクシートの投稿またはエラーファイルの修正](bulksheet-post.md)
>* [進行中のバルクシート ジョブの停止](bulksheet-stop-job.md)
>* [ バルクシートまたは修正されたエラーファイルをアップロード ](bulksheet-upload.md)
>* [生成またはアップロードされたバルクシート ファイルを書き出す](bulksheet-export.md)
