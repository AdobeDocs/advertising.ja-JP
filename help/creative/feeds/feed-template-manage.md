---
title: フィードテンプレートの管理
description: フィードテンプレートの管理方法について説明します。
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# フィードテンプレートの管理

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

フィードテンプレートは、フィードファイル/カタログのフィールドをAdvertising Creative バックエンドのフィールドとマッピングします。 動的HTML5 広告（静的HTML5 広告ではない）では、動的広告を作成するためにフィードテンプレートが必要です。

複数の広告テンプレートでフィードテンプレートを使用できます。

## フィードテンプレートの作成

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]**/**[!UICONTROL Template]** をクリックします。

1. [&#x200B; フィードテンプレート設定 &#x200B;](#feed-template-settings) を指定します。

1. 「**[!UICONTROL Save]**」をクリックします。

## フィードテンプレートの編集

**メモ：** 編集できるのは、自分で作成したフィードテンプレートのみです。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Duplicate]** をクリックします。

1. 必要に応じて [&#x200B; フィードテンプレート設定 &#x200B;](#feed-template-settings) を編集します。

1. 「**[!UICONTROL Save]**」をクリックします。

## フィードテンプレートの表示

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL View]** をクリックします。

## フィードテンプレートの複製

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Duplicate]** をクリックします。

1. [!UICONTROL Duplicate Template] 画面で、一意の **[!UICONTROL Template Name]** を入力します。 他のユーザーが作成したテンプレートを複製する場合は、**[!UICONTROL Advertiser]** を選択します。 必要に応じて、オプションで他の [&#x200B; フィードテンプレート設定 &#x200B;](#feed-template-settings) を編集します。

1. 「**[!UICONTROL Save]**」をクリックします。

## フィードテンプレートのダウンロード

ダウンロードしたフィードテンプレートは、ZIP 形式のMicrosoft Excel スプレッドシート（XLSX）形式です。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Download]** をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## フィードテンプレート設定 {#feed-template-settings}

### [!UICONTROL General] 設定

**[!UICONTROL Template Name]:** 指定した広告主の一意のテンプレート名。

**[!UICONTROL Advertiser]:** テンプレートを使用できる広告主。

**[!UICONTROL Description]:** （任意）フィードテンプレートを使用しているすべてのユーザーに役立つ情報です。

### [!UICONTROL Field Mapping] 設定

フィードファイルの各フィールドをAdvertising Creative バックエンドのフィールドにマッピングします。 バックエンドフィールドとその必要な属性のリストについては [&#x200B; 「](/help/creative/appendix-available-feed-fields.md) 動的広告フィードファイルに使用できるフィールド」を参照してください。<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

少なくとも 1 つのフィード ファイル フィールドが&quot;[!UICONTROL Is Unique]&quot;としてマークされている必要があります。 フィールドマッピングを追加するには、「**[!UICONTROL +]**」をクリックします。 最後のフィールドマッピングを削除するには、「削 **[!UICONTROL +]**」をクリックします。

**[!UICONTROL Field Name]:** フィードファイルのフィールド。

**[!UICONTROL Description]:** （任意）フィードテンプレートを使用しているすべてのユーザーに役立つ情報です。

**[!UICONTROL Is Unique]:** フィールドが一意の ID （キー）であることを示します。 フィードテンプレートごとに少なくとも 1 つのフィールドが一意である必要があります。 このオプションを選択するには、ボタンをクリックして右に移動します。<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** Advertising Creative バックエンドの [&#x200B; フィールド &#x200B;](/help/creative/appendix-available-feed-fields.md) は、フィードファイルで指定された [!UICONTROL Field Name] にマッピングされます。

>[!MORELIKETHIS]
>
>* [&#x200B; 動的広告のワークフロー &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; アセットファイルの管理 &#x200B;](/help/creative/feeds/asset-manage.md)
>* [&#x200B; カタログの管理 &#x200B;](/help/creative/feeds/catalog-manage.md)
>* [&#x200B; カタログ処理ジョブのステータスのトラッキング &#x200B;](/help/creative/feeds/job-status-track.md)
>* [&#x200B; 動的広告テンプレートの管理 &#x200B;](/help/creative/ad-templates/ad-template-manage.md)
>* [&#x200B; クリエイティブライブラリへのダイナミッククリエイティブの追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md)
