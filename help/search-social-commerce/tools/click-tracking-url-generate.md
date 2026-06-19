---
title: クリックトラッキング URLの生成
description: Search, Social, & Commerceのクリックトラッキング URLを手動で生成する方法について説明します。
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
TQID: https://experienceleague.adobe.com/RqD0SAUXXlSNvMUJFgrjspFoGjpJHmx0ThZGAHFFdi0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 484
ht-degree: 0%

---

# トラッキング URL ツールを使用して、検索、ソーシャル、Commerceのクリックトラッキング URLを生成します

*Adobe Advertising コンバージョントラッキングのみを使用する広告主*

クリックトラッキング URLを手動で生成して実装する必要がある場合について詳しくは、「[いつ、どのようにクリックトラッキング URLを生成するか](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)」を参照してください。

>[!NOTE]
>
>この機能は、関連する広告アカウントにトラッキングテンプレートまたは宛先URLを実装しません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**&#x200B;をクリックします。

1. リストから広告ネットワークアカウントを選択します。

   （[!DNL Google Ads] キーワード、テキスト、モバイルアプリのインストール、動的検索広告、プレースメント、サイトリンク、製品グループ）トラッキングテンプレートフィールドのトラッキングタグが表示されます。 アカウントレベルの追加パラメーターは含まれていません。 手順4に進みます。

   その他のすべてのタイプのタグに対して、タグを生成するための情報を入力します。

1. （必要に応じて）タグを生成します。

   1. 次のいずれかの方法で、ランディングページをサイトリンクまたは製品名を指定します。

      * 完全なパスとファイル名を入力するか、**[!UICONTROL Browse]**&#x200B;をクリックしてデバイスまたはネットワーク上のファイルを検索して、情報を含むファイルを指定します。 ファイルは、次の形式の行ごとに1つの項目を持つタブ区切りのテキストファイルである必要があります。

         * （クリエイティブ、標準広告） `**landing_page**`

           ここで、`landing_page`は有効なランディングページ URLまたはベース URLです。

           例：http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising] サイトリンク） `sitelink <tab> ** <tab> landing_page`

           ここで、`sitelink`はサイトリンク名、`landing_page`は有効なランディングページ URLまたはベース URLです。

           例：`Careers <tab> ** <tab> http://www.example.com/careers.html`

           ファイルには最大10,000行を含めることができます。

         * （[!DNL Google Merchant Center]個の製品グループと[!DNL Microsoft Advertising]個の製品広告） `product name <tab> ** <tab> landing_page`

           ここで、`product name`は製品名、`landing_page`は有効なランディングページ URLまたはベース URLです。

           例：`Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           ファイルには最大10,000行を含めることができます。

      * 入力フィールドに、1行につき1つの項目を次の形式で入力します。

         * （クリエイティブ、標準広告） `landing_page`

           ここで、`landing_page`は有効なランディングページ URLまたはベース URLです。

           例：http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising] サイトリンク） `sitelink**landing_page`

           ここで、`sitelink`はサイトリンク名、`landing_page`は有効なランディングページ URLまたはベース URLです。

           例：`Careers**http://www.example.com/careers.html`

         * （[!DNL Google Merchant Center]個の製品グループと[!DNL Microsoft Advertising]個の製品広告） `product name**landing_page`

           ここで、`product name`は製品名、`landing_page`は有効なランディングページ URLまたはベース URLです。

           例：Acme PR208**http://www.example.com/travel.html

   1. **[!UICONTROL Generate Tracking URLs]**&#x200B;をクリックします。

1. （オプション）画面または出力ページからURL （「http」または「https」で始まる）をコピーし、検索またはソーシャルアカウントに実装します。

宛先URLを持つアカウントの場合は、適切な[!UICONTROL Base URL] フィールドに値を入力します。

最終的なURLを持つアカウントの場合は、適切な[!UICONTROL Tracking Template] フィールドに画面上の値を入力します。 `&url=` パラメーター（`{lpurl}`など）の後に、最終的なURLのパラメーターを追加する必要があります。 [!DNL LY Ads] アカウントの場合は、パラメーター`{lpurl}`を使用します。 トラッキングテンプレートの最終的なURLを示す[!DNL Google Ads]および[!DNL Microsoft Advertising] パラメーターのリストについては、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/6305348) （「使用可能な[!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ」パラメーターを参照）および[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799/2)を参照してください。

>[!MORELIKETHIS]
>
>* [ トラッキングタグを作成およびデコードするツールについて](tracking-tools-about.md)
>* [ クリックトラッキング URLを生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [検索、ソーシャル、Commerceのクリックトラッキング URLをデコード ](click-tracking-url-decode.md)
