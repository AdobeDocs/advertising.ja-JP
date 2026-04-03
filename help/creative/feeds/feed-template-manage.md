---
title: フィード テンプレートの管理
description: フィードテンプレートの管理方法を説明します。
feature: Creative Dynamic Creatives
exl-id: 63f8af87-639c-45c8-b17f-99ce19594d35
TQID: https://experienceleague.adobe.com/5bEvYLuXmwYHifo--x98vtfZ7-tVsLcRq5LGSLilFvM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 476
ht-degree: 0%

---

# フィード テンプレートの管理

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

フィードテンプレートは、フィードファイル/カタログのフィールドをAdvertising Creative バックエンドのフィールドにマッピングします。 動的なHTML5広告と動画広告は静的なHTML5広告ではなく、動的な広告を作成するにはフィードテンプレートが必要です。 オプションで、ユニバーサルフィードのテンプレートをダウンロードして入力できます（小売キャンペーンの場合は[!UICONTROL Retail]、任意のキャンペーンタイプの場合は[!UICONTROL Adobe Creative Template]）。

複数の広告テンプレートを含むフィード テンプレートを使用できます。

>[!TIP]
>
>ダイナミック ビデオを使用しているすべてのアカウントの場合、ベストプラクティスは[&#x200B; ユニバーサル フィード テンプレート [!UICONTROL Adobe Creative Template]](feed-template-manage.md)をダウンロードし、アセット ファイルの各フィールドをAdvertising Creative バックエンドのフィールドにマッピングしてから、フィード テンプレートの名前を変更してアップロードすることです。 新しいフィード テンプレートとアセット ファイルを使用して、[&#x200B; カタログを作成](catalog-manage.md)します。

## フィードテンプレートの作成

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]** > **[!UICONTROL Template]**&#x200B;をクリックします。

1. [&#x200B; フィード テンプレート設定](#feed-template-settings)を指定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## フィードテンプレートの編集

**注：**&#x200B;編集できるのは、作成したフィード テンプレートのみです。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Duplicate]**&#x200B;をクリックします。

1. 必要に応じて、[&#x200B; フィードテンプレート設定](#feed-template-settings)を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## フィードテンプレートの表示

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL View]**&#x200B;をクリックします。

## フィードテンプレートの複製

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Duplicate]**&#x200B;をクリックします。

1. [!UICONTROL Duplicate Template]画面で、一意の&#x200B;**[!UICONTROL Template Name]**&#x200B;を入力します。 他のユーザーが作成したテンプレートを複製する場合は、**[!UICONTROL Advertiser]**&#x200B;を選択します。 必要に応じて、他の[&#x200B; フィードテンプレート設定](#feed-template-settings)をオプションで編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## フィードテンプレートをダウンロード

ダウンロードしたフィードテンプレートは、圧縮されたMicrosoft Excel スプレッドシート（XLSX）形式です。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Download]**&#x200B;をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## フィードテンプレート設定 {#feed-template-settings}

### [!UICONTROL General]設定

**[!UICONTROL Template Name]:**&#x200B;指定された広告主の一意のテンプレート名。

**[!UICONTROL Advertiser]:** テンプレートを使用できる広告主。

**[!UICONTROL Description]:** （オプション）フィード テンプレートを使用しているすべてのユーザーに役立つ情報。

### [!UICONTROL Field Mapping]設定

フィードファイルの各フィールドをAdvertising Creative バックエンドのフィールドにマッピングします。 バックエンドフィールドと必要な属性のリストについては、「[動的な広告フィードファイルの使用可能なフィールド &#x200B;](/help/creative/appendix-available-feed-fields.md)」を参照してください。<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

1つ以上のフィード ファイル フィールドに&quot;[!UICONTROL Is Unique]&quot;というマークを付ける必要があります。 フィールドマッピングを追加するには、**[!UICONTROL +]**&#x200B;をクリックします。 最後のフィールドマッピングを削除するには、**[!UICONTROL +]**&#x200B;をクリックします。

**[!UICONTROL Field Name]:** フィード ファイルのフィールド。

**[!UICONTROL Description]:** （オプション）フィード テンプレートを使用しているユーザーに役立つ情報です。

**[!UICONTROL Is Unique]:** フィールドが一意のID （キー）であることを示します。 フィード テンプレートごとに少なくとも1つのフィールドは一意である必要があります。 このオプションを選択するには、ボタンをクリックして右に移動します。<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** フィード ファイルの指定された[にマッピングするAdvertising Creative バックエンド &#x200B;](/help/creative/appendix-available-feed-fields.md)の[!UICONTROL Field Name] フィールド。

>[!MORELIKETHIS]
>
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; アセットファイルの管理](/help/creative/feeds/asset-manage.md)
>* [&#x200B; カタログの管理](/help/creative/feeds/catalog-manage.md)
>* [&#x200B; カタログ処理ジョブのステータスを追跡](/help/creative/feeds/job-status-track.md)
>* [動的広告テンプレートの管理](/help/creative/ad-templates/ad-template-manage.md)
>* [&#x200B; クリエイティブライブラリに動的なクリエイティブを追加](/help/creative/creative-libraries/creative-add-dynamic.md)
