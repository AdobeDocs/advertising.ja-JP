---
title: クリック追跡 URL を生成
description: 検索、ソーシャル、コマースのクリック追跡 URL を手動で生成する方法を説明します。
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# トラッキング URL ツールを使用して、検索、ソーシャル、およびコマースのクリックトラッキング URL を生成します

*Adobe広告コンバージョントラッキングのみを持つ広告主*

クリック追跡 URL を手動で生成して実装する必要があるタイミングについて詳しくは、[クリック追跡 URL を生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>この機能では、関連する広告アカウントにトラッキングテンプレートまたはリンク先 URL は実装されません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. リストから広告ネットワークアカウントを選択します。

   ([!DNL Google Ads] キーワード；テキスト、モバイルアプリのインストール、動的検索広告。配置；sitelinks;および製品グループ ) トラッキングテンプレートフィールドのトラッキングタグが表示されます。 アカウントレベルの追加パラメーターは含まれていません。 手順 4 に進みます。

   その他のタグタイプの場合は、タグを生成するための情報を入力します。

1. （必要に応じて）タグを生成します。

   1. 次のいずれかの方法で、リクエストに応じて、ランディングページにサイトリンクまたは製品名を指定します。

      * フルパスとファイル名を入力するか、 **[!UICONTROL Browse]** をクリックして、お使いのデバイスまたはネットワーク上でファイルを見つけます。 ファイルは、次の形式で、1 行に 1 つの項目を含むタブ区切りのテキストファイルである必要があります。

         * （クリエイティブ、標準広告） `**landing_page**`

           場所 `landing_page` は、有効なランディングページ URL またはベース URL です。

           例：http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           場所 `sitelink` はサイトリンク名で、 `landing_page` は、有効なランディングページ URL またはベース URL です。

           例： `Careers <tab> ** <tab> http://www.example.com/careers.html`

           ファイルには、最大 10,000 行を含めることができます。

         * ([!DNL Google Merchant Center] 製品グループと [Microsoft® Advertising] 製品広告 ) `product name <tab> ** <tab> landing_page`

           場所 `product name` は製品名で、 `landing_page` は、有効なランディングページ URL またはベース URL です。

           例： `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           ファイルには、最大 10,000 行を含めることができます。

      * 入力フィールドに、次の形式で 1 行に 1 項目ずつ入力します。

         * （クリエイティブ、標準広告） `landing_page`

           場所 `landing_page` は、有効なランディングページ URL またはベース URL です。

           例：http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink**landing_page`

           場所 `sitelink` はサイトリンク名で、 `landing_page` は、有効なランディングページ URL またはベース URL です。

           例： `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] 製品グループと [!DNL Microsoft® Advertising] 製品広告 ) `product name**landing_page`

           場所 `product name` は製品名で、 `landing_page` は、有効なランディングページ URL またはベース URL です。

           例：Acme PR208**http://www.example.com/travel.html

   1. クリック **[!UICONTROL Generate Tracking URLs]**.

1. （オプション）画面または出力ページから URL（「http」または「https」で始まる）をコピーし、検索またはソーシャルアカウントに実装します。

リンク先 URL のアカウントの場合は、該当する [!UICONTROL Base URL] フィールド。

最終的な URL を持つアカウントの場合は、該当する [!UICONTROL Tracking Template] フィールドに入力します。 最終 URL の、 `&url=` パラメータ ( `{lpurl}`) をクリックします。 の場合 [!DNL Yahoo! Japan Ads] アカウントの場合は、パラメーターを使用します。 `{lpurl}`. のリスト [!DNL Google Ads] および [!DNL Microsoft® Advertising] トラッキングテンプレートの最終 URL を示すパラメーターについては、 [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348) ( 使用可能 [!DNL ValueTrack] パラメータ」) および [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [トラッキングタグを作成およびデコードするツールについて](tracking-tools-about.md)
>* [クリック追跡 URL を生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [検索、ソーシャル、コマースのクリック追跡 URL のデコード](click-tracking-url-decode.md)
