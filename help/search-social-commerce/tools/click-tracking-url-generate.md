---
title: クリックの追跡 URL の生成
description: 検索、ソーシャル、Commerceのクリックトラッキング URL を手動で生成する方法を説明します。
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# URL トラッキング ツールを使用した、検索、ソーシャル、Commerceのクリックトラッキング URL の生成

*Adobe Advertisingコンバージョントラッキングのみを使用する広告主*

クリックトラッキング URL を手動で生成および実装する必要がある場合について詳しくは、「[ クリックトラッキング URL を生成するタイミングと方法 ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) を参照してください。

>[!NOTE]
>
>この機能では、関連する広告アカウントにトラッキングテンプレートまたは宛先 URL を実装しません。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Tools]/[!UICONTROL Tracking URL]** をクリックします。

1. リストから広告ネットワークアカウントを選択します。

   （キーワード、テキスト、モバイルアプリのインストール、動的検索広告、プレースメント、サイトリンク、製品グループな [!DNL Google Ads]）トラッキングテンプレートフィールドのトラッキングタグが表示されます。 アカウントレベルの追加パラメーターは含まれません。 手順 4 に進みます。

   その他のすべてのタイプのタグの場合は、情報を入力してタグを生成します。

1. （必要に応じて）タグを生成します。

   1. 次のいずれかの方法で、要求に応じてサイトリンクまたは製品名を使用してランディングページを指定します。

      * フルパスとファイル名を入力するか、**[!UICONTROL Browse]** をクリックしてデバイスまたはネットワーク上のファイルを探すことにより、情報を含むファイルを指定します。 ファイルは、次の形式で、行ごとに 1 つの項目を持つタブ区切りのテキストファイルである必要があります。

         * （クリエイティブ、標準広告） `**landing_page**`

           ここで、`landing_page` は有効なランディングページの URL またはベース URL です。

           例：http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising] sitelinks） `sitelink <tab> ** <tab> landing_page`

           ここで、`sitelink` はサイトリンク名で、`landing_page` は有効なランディングページの URL またはベース URL です。

           例：`Careers <tab> ** <tab> http://www.example.com/careers.html`

           ファイルには、最大 10,000 行を含めることができます。

         * （[!DNL Google Merchant Center] 製品グループと [!DNL Microsoft Advertising] 製品広告） `product name <tab> ** <tab> landing_page`

           `product name` は製品名で、`landing_page` は有効なランディングページの URL またはベース URL です。

           例：`Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           ファイルには、最大 10,000 行を含めることができます。

      * 入力フィールドに、次の形式で 1 行に 1 項目を入力します。

         * （クリエイティブ、標準広告） `landing_page`

           ここで、`landing_page` は有効なランディングページの URL またはベース URL です。

           例：http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising] sitelinks） `sitelink**landing_page`

           ここで、`sitelink` はサイトリンク名で、`landing_page` は有効なランディングページの URL またはベース URL です。

           例：`Careers**http://www.example.com/careers.html`

         * （[!DNL Google Merchant Center] 製品グループと [!DNL Microsoft Advertising] 製品広告） `product name**landing_page`

           `product name` は製品名で、`landing_page` は有効なランディングページの URL またはベース URL です。

           例：Acme PR208**http://www.example.com/travel.html

   1. 「**[!UICONTROL Generate Tracking URLs]**」をクリックします。

1. （オプション）画面または出力ページから URL （「http」または「https」で始まる）をコピーして、検索またはソーシャルアカウントに実装します。

宛先 URL を持つアカウントの場合、適切な [!UICONTROL Base URL] フィールドに値を入力します。

最終的な URL を持つアカウントの場合は、適切な [!UICONTROL Tracking Template] フィールドに画面上の値を入力します。 最終的な URL のパラメーターを `&url=` パラメーターの後に追加する必要があります（`{lpurl}` など）。 [!DNL Yahoo! Japan Ads] アカウントの場合は、パラメーター `{lpurl}` を使用します。 トラッキングテンプレートで最終的な URL を示す [!DNL Google Ads] および [!DNL Microsoft Advertising] パラメーターのリストについては、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/6305348) （「使用可能な [!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ」パラメーターを参照）および [[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799/2) を参照してください。

>[!MORELIKETHIS]
>
>* [ トラッキングタグを作成およびデコードするツールについて ](tracking-tools-about.md)
>* [ クリックトラッキング URL を生成するタイミングと方法 ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [ 検索、ソーシャル、Commerceのクリックトラッキング URL のデコード ](click-tracking-url-decode.md)
