---
title: フィードカタログの管理
description: フィードカタログの管理方法について説明します。
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# フィードカタログの管理

処理済みのフィードカタログは、指定したフィードファイルと指定したフィードテンプレートから作成された、潜在的な広告バリエーションのセットです。 動的HTML5 広告（静的HTML5 広告ではない）を作成するには、カタログが必要です。

広告のバリエーションを作成し [&#x200B; クリエイティブライブラリに動的広告を追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) する前に、カタログを処理します。 後でフィードファイルを更新し、カタログを再処理して、新しい広告バリエーションのセットを作成できます。<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

## カタログの作成 {#feed-catalog-create}

>[!NOTE]
>
>[&#x200B; クリエイティブライブラリにダイナミッククリエイティブを追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) する際に、カタログを直接アップロードすることもできます。 ここで作成したカタログは、後で使用するために [!UICONTROL Catalogs] ビュー内で使用できます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Catalog]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]**/**[!UICONTROL Template]** をクリックします。

1. 必要に応じて [&#x200B; カタログ設定 &#x200B;](#catalog-settings) を指定します。

1. 「**[!UICONTROL Next]**」をクリックします。

1. カタログに対して作成できる潜在的な広告バリエーションを確認します。

1. 「**[!UICONTROL Save]**」をクリックします。

## カタログを編集

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Catalog]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Edit]** をクリックします。

1. 必要に応じて [&#x200B; カタログ設定 &#x200B;](#catalog-settings) を編集します。

1. カタログに対して作成できる潜在的な広告バリエーションを確認します。

1. 「**[!UICONTROL Save]**」をクリックします。

## カタログを処理 {#feed-catalog-process}

カタログを処理すると、広告のバリエーションを使用して動的なHTML5 広告を作成できます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Catalog]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Run Now]** をクリックします。

## アクティブなカタログを一時停止

カタログを一時停止して非アクティブにします。<!-- Can you Activate it again? -->

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Pause]** をクリックします。

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## 一時停止したカタログのアクティブ化

<!-- Verify if this is available. -->

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Activate]** をクリックします。

## カタログのアーカイブ

カタログをアーカイブして削除します。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Feeds]** をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. カーソルをテンプレートの行の上に置き、**[!UICONTROL Archive]** をクリックします。

1. 確認メッセージで、「**[!UICONTROL Archive]**」をクリックします。

## カタログ設定 {#catalog-settings}

**[!UICONTROL Advertiser]:** カタログを使用できる広告主。

**[!UICONTROL Asset]:** カタログの入力として使用するフィードファイル。

**[!UICONTROL Catalog Name]:** 指定した広告主の一意のカタログ名。 デフォルトでは、識別のベストプラクティスとなるファイル拡張子を含んだフィードファイル名が使用されます。<!-- must it have a file extension? -->

**[!UICONTROL Template]:** 指定されたアセット/フィードファイルのフィールドをAdvertising Creative バックエンドのフィールドにマッピングするために使用するフィードテンプレート。

>[!MORELIKETHIS]
>
>* [&#x200B; カタログ処理ジョブのステータスのトラッキング &#x200B;](/help/creative/feeds/job-status-track.md)
>* [&#x200B; 動的広告のワークフロー &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; アセットファイルの管理 &#x200B;](/help/creative/feeds/asset-manage.md)
>* [&#x200B; フィードテンプレートの管理 &#x200B;](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; 動的広告テンプレートの管理 &#x200B;](/help/creative/ad-templates/ad-template-manage.md)
>* [&#x200B; クリエイティブライブラリへのダイナミッククリエイティブの追加 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md)
