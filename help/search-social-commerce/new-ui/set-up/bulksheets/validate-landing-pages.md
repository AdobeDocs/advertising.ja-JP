---
title: （新しいUI）バルクシートファイルでのランディングページの検証
description: 新しい検索、ソーシャル、およびCommerce UIで、シングルアカウントのバルクシートファイル内のリンク先URLを検証する方法について説明します。
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f916f47a40729ff39ac1456e3b3ad93e1045e9a9
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# （新しいUI）バルクシートファイルでのランディングページの検証

*宛先URLのみ*&#x200B;のアカウント

単一アカウントのバルクシートファイル内のすべての宛先URLのランディングページを検証できます。 無効なページを示すフレーズとURLを指定し、オプションでランディングページのリダイレクトをエラーとしてレポートできます。 Search, Social, &amp; Commerceは、指定した条件とランディングページが見つからない場合にチェックします（これにより、HTTP 404または「見つかりません」エラーが発生します）。

エラーが見つかった場合、Search, Social, &amp; Commerceは、元のバルクシートのすべての行と、無効なランディングページを含むすべての行のエラーメッセージを含むバルクシートのエラーファイルを作成します。 エラーは[!UICONTROL EF Errors]列に記録されます。 ファイル名規則は`<bulksheet name>__lpv_errors.<extension used for the bulksheet>`です。

後でファイルをダウンロードし、エラーを修正して修正したファイルをアップロードしてから、修正したファイルを広告ネットワークアカウントに投稿できます。

>[!NOTE]
>
>* この機能では、ベース URL/最終URL列の値は検証されません。
>* バルクシートファイルは、検証中やエラーが見つかった場合でも投稿することができます。

>[!IMPORTANT]
>
>ランディングページ検証における非ASCII文字のサポートは、一時的に停止されました。 ランディングページのURLに非ASCII文字が含まれる場合は、テクニカルサポートにお問い合わせください。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. 検証する各ファイルの横にあるチェックボックスをオンにします。

   >[!NOTE]
   >
   >現在進行中ではない単一アカウント EF バルクシートのみを検証できます。 複数アカウントのバルクシートまたは現在処理中のバルクシートを選択すると、これらのファイルは除外されます。

1. アクションバーで、**[!UICONTROL Validate URLs]**&#x200B;をクリックします。

1. ダイアログで、フィールドに情報を入力し、**[!UICONTROL Apply]**&#x200B;をクリックします。

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** ランディングページの本文のテキスト。ページが無効であることを示します。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL Enter invalid landing pages (one per line):]** ランディングページとして無効なページのURL。 複数の値を指定するには、別々の行に入力します。

   **[!UICONTROL User Agent:]** ランディングページの検証エージェントが、ランディングページが格納されているweb サーバーに対して識別される方法。 デフォルトは`default`で、エージェントによるビューを匿名の[!DNL Mozilla Firefox] ユーザーに属性します。 Web サーバーが匿名[!DNL Mozilla Firefox] ユーザーからのリクエストをブロックする場合は、別のエージェントの名前を入力します。 例えば、[!DNL Googlebot]に対して、`Googlebot/2.1;+http://www.google.com/bot.html`と入力します。

   **[!UICONTROL Report redirects as errors]:** ランディングページが別のページにリダイレクトされる場合（ランディングページが見つからず、サイトに代替ページが表示される場合など）、ランディングページエラーファイルの[!UICONTROL EF Errors]列は、ランディングページがリダイレクトされるURLを示します。

タスクが開始されると、新しい行が[!UICONTROL Bulksheets] ビューに追加されます。 バルクシートのメール通知が[!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md)内で[有効になっている場合、ファイルの作成時に、ファイルへのリンクを含むメール通知が送信されます。 収集されたデータ量によっては、メール通知に数分以上かかる場合があります。 ファイルをダウンロードして編集し、投稿のために再アップロードするか、ファイルをそのまま投稿できます。

>[!NOTE]
>
>* 大きなファイルの検証には時間がかかります。
>* 複数のキャンペーンのバルクシートファイルには、最大500,000行のデータ行を含めることができます。 複数のキャンペーンのデータを生成し、結合データが500,000行を超える場合、データはキャンペーンごとに`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`などの名前の2つ以上のファイルに分割されます。

>[!MORELIKETHIS]
>
>* [ （新しいUI）バルクシートを使用したキャンペーンデータの管理について](about.md)
>* [ （新しいUI） バルクシートまたは修正されたエラーファイルをアップロード ](upload.md)
>* [ （新しいUI）バルクシートの投稿またはエラーファイルの修正](post.md)
>* [ （新しいUI） アップロードされたバルクシートとエラーファイルを削除](delete.md)
>* [ （新しいUI）進行中のバルクシート ジョブを停止](stop-job.md)
