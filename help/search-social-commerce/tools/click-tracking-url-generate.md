---
title: クリックの追跡 URL の生成
description: 検索、ソーシャル、Commerceのクリックトラッキング URL を手動で生成する方法を説明します。
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: 0da23a2756fc7ed4d2ef8fb739d94a91ac6400ba
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# URL トラッキング ツールを使用した、検索、ソーシャル、Commerceのクリックトラッキング URL の生成

*Adobe Advertisingコンバージョントラッキングのみを使用する広告主*

クリックトラッキング URL を手動で生成および実装する必要がある場合について詳しくは、「」を参照してください[クリックの追跡 URL を生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).」と入力します。

>[!NOTE]
>
>この機能では、関連する広告アカウントにトラッキングテンプレートまたは宛先 URL を実装しません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. リストから広告ネットワークアカウントを選択します。

   （[!DNL Google Ads] キーワード、テキスト、モバイルアプリのインストール、動的検索広告、プレースメント、サイトリンク、製品グループ） トラッキングテンプレートフィールドのトラッキングタグが表示されます。 アカウントレベルの追加パラメーターは含まれません。 手順 4 に進みます。

   その他のすべてのタイプのタグの場合は、情報を入力してタグを生成します。

1. （必要に応じて）タグを生成します。

   1. 次のいずれかの方法で、要求に応じてサイトリンクまたは製品名を使用してランディングページを指定します。

      * フルパスとファイル名を入力するか、をクリックして、情報を含むファイルを指定します **[!UICONTROL Browse]** をクリックして、デバイスまたはネットワーク上のファイルを探します。 ファイルは、次の形式で、行ごとに 1 つの項目を持つタブ区切りのテキストファイルである必要があります。

         * （クリエイティブ、標準広告） `**landing_page**`

           ここで、 `landing_page` は、有効なランディングページの URL またはベース URL です。

           例：http://www.example.com/travel.html

         * （[!DNL Microsoft® Advertising] sitelinks） `sitelink <tab> ** <tab> landing_page`

           ここで、 `sitelink` はサイトリンク名で、 `landing_page` は、有効なランディングページの URL またはベース URL です。

           例： `Careers <tab> ** <tab> http://www.example.com/careers.html`

           ファイルには、最大 10,000 行を含めることができます。

         * （[!DNL Google Merchant Center] 製品グループと [DNL Microsoft® Advertising] 製品広告） `product name <tab> ** <tab> landing_page`

           ここで、 `product name` は製品名で、 `landing_page` は、有効なランディングページの URL またはベース URL です。

           例： `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           ファイルには、最大 10,000 行を含めることができます。

      * 入力フィールドに、次の形式で 1 行に 1 項目を入力します。

         * （クリエイティブ、標準広告） `landing_page`

           ここで、 `landing_page` は、有効なランディングページの URL またはベース URL です。

           例：http://www.example.com/travel.html

         * （[!DNL Microsoft® Advertising] sitelinks） `sitelink**landing_page`

           ここで、 `sitelink` はサイトリンク名で、 `landing_page` は、有効なランディングページの URL またはベース URL です。

           例： `Careers**http://www.example.com/careers.html`

         * （[!DNL Google Merchant Center] 製品グループと [!DNL Microsoft® Advertising] 製品広告） `product name**landing_page`

           ここで、 `product name` は製品名で、 `landing_page` は、有効なランディングページの URL またはベース URL です。

           例：Acme PR208**http://www.example.com/travel.html

   1. クリック **[!UICONTROL Generate Tracking URLs]**.

1. （オプション）画面または出力ページから URL （「http」または「https」で始まる）をコピーして、検索またはソーシャルアカウントに実装します。

宛先 URL を持つアカウントの場合、適切な値を入力します [!UICONTROL Base URL] フィールド。

最終的な URL を持つアカウントの場合は、画面上の適切な値を入力します [!UICONTROL Tracking Template] フィールド。 の後に最終 URL のパラメーターを追加する必要があります `&url=` パラメーター（例： `{lpurl}`）に設定します。 の場合 [!DNL Yahoo! Japan Ads] アカウント、パラメーターを使用します `{lpurl}`. のリスト用 [!DNL Google Ads] および [!DNL Microsoft® Advertising] トラッキングテンプレートで最終的な URL を示すパラメーターについては、を参照してください。 [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/6305348) （「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーターを参照。 [!DNL ValueTrack] パラメーター&quot;）と [[!DNL Microsoft® Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [トラッキングタグを作成およびデコードするツールについて](tracking-tools-about.md)
>* [クリックの追跡 URL を生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [検索、ソーシャル、Commerceのクリックトラッキング URL のデコード](click-tracking-url-decode.md)
