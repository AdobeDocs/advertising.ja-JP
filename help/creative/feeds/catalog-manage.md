---
title: フィード カタログの管理
description: フィード カタログの管理方法を説明します。
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
TQID: https://experienceleague.adobe.com/x-5tLvICnT97bjhgenM3iTBWRLKl3fbfA5UF8VlKrVw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 462
ht-degree: 0%

---

# フィード カタログの管理

処理されたフィード カタログは、指定されたフィード ファイルと指定されたフィード テンプレートから作成された潜在的な広告バリエーションのセットです。 動的なHTML5広告と動画広告は、静的なHTML5広告ではなく、動的な広告を作成するためにカタログが必要です。

広告のバリエーションを作成し、[動的な広告をクリエイティブライブラリに追加する](/help/creative/creative-libraries/creative-add-dynamic.md)前に、カタログを処理してください。 後でフィード ファイルを更新し、カタログを再処理して、新しい広告バリエーションのセットを作成できます。<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

各フィードファイルは、ビデオアセットで最大500行まで処理できます。

>[!TIP]
>
>ダイナミック ビデオを使用しているすべてのアカウントの場合、ベストプラクティスは[ ユニバーサル フィード テンプレート [!UICONTROL Adobe Creative Template]](feed-template-manage.md)をダウンロードし、アセット ファイルの各フィールドをAdvertising Creative バックエンドのフィールドにマッピングしてから、フィード テンプレートの名前を変更してアップロードすることです。 新しいフィードテンプレートとアセットファイルを使用して、カタログを作成します。

## カタログの作成 {#feed-catalog-create}

>[!NOTE]
>
>[動的なクリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-dynamic.md)すると、カタログを直接アップロードすることもできます。 そこで作成したカタログは、今後の使用のために[!UICONTROL Catalogs] ビュー内で使用できるようになります。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Catalog]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]** > **[!UICONTROL Template]**&#x200B;をクリックします。

1. 必要に応じて[ カタログ設定](#catalog-settings)を指定します。

1. **[!UICONTROL Next]**&#x200B;をクリックします。

1. カタログに作成できる潜在的な広告バリエーションを確認します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## カタログの編集

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Catalog]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. 必要に応じて[ カタログ設定](#catalog-settings)を編集します。

1. カタログに作成できる潜在的な広告バリエーションを確認します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## カタログの処理 {#feed-catalog-process}

カタログを処理することで、広告のバリエーションを利用して、動的なHTML 5広告を作成できるようになります。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Catalog]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Run Now]**&#x200B;をクリックします。

## アクティブなカタログを一時停止する

カタログを一時停止して非アクティブにします。<!-- Can you Activate it again? -->

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Pause]**&#x200B;をクリックします。

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## 一時停止したカタログのアクティブ化

<!-- Verify if this is available. -->

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Activate]**&#x200B;をクリックします。

## カタログのアーカイブ

カタログをアーカイブして削除します。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、**[!UICONTROL Archive]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Archive]**&#x200B;をクリックします。

## カタログ設定 {#catalog-settings}

**[!UICONTROL Advertiser]:** カタログを使用できる広告主。

**[!UICONTROL Asset]:** カタログの入力として使用するフィード ファイル。

**[!UICONTROL Catalog Name]:**&#x200B;指定された広告主の一意のカタログ名。 デフォルトでは、フィード ファイル名が使用され、ファイル拡張子も含まれます。これは、識別のベストプラクティスです。<!-- must it have a file extension? -->

**[!UICONTROL Template]:**&#x200B;指定したアセット/フィードファイルのフィールドをAdvertising Creative バックエンドのフィールドにマッピングするために使用するフィードテンプレート。

>[!MORELIKETHIS]
>
>* [ カタログ処理ジョブのステータスを追跡](/help/creative/feeds/job-status-track.md)
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ アセットファイルの管理](/help/creative/feeds/asset-manage.md)
>* [ フィード テンプレートの管理](/help/creative/feeds/feed-template-manage.md)
>* [動的広告テンプレートの管理](/help/creative/ad-templates/ad-template-manage.md)
>* [ クリエイティブライブラリに動的なクリエイティブを追加](/help/creative/creative-libraries/creative-add-dynamic.md)
