---
title: Adobe Advertisingのコンバージョン追跡タグを生成して実装する
description: Adobe Advertisingのコンバージョンタグを作成して、コンバージョンイベントをトラッキングする方法について説明します。
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Adobe Advertisingのコンバージョン追跡タグを生成して実装する

*Adobe Advertising コンバージョントラッキングのみを使用する広告主*

追跡する指標のセットごとに個別のコンバージョンタグを作成します。 Search、Social、Commerceでタグを生成するか、Adobe Experience Platform（旧Adobe Experience Platform Launch）のタグとAdobe Advertising拡張機能を使用してタグを生成できます。

<!--

## (New UI) Generate and implement a conversion-tracking tag within Search, Social, & Commerce

>[!NOTE]
>
>This feature doesn't add image tags or [!DNL JavaScript] tags to the advertiser's webpages. Provide the tags to the advertiser or agency with a list of webpages on which to insert each. The tags must be added according to the advertiser's normal procedure for updating webpages.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

1. In the main toolbar, click **[!UICONTROL Conversion Tag]**.

1. Specify the [conversion tag settings](#conversion-tag-settings).

1. Click **[!UICONTROL Generate]**.
   
1. Click **[!UICONTROL Copy]** to copy the tag to your clipboard. Give the tag to the advertiser or agency to implement.

>[!NOTE]
>
>Each metric in the new conversion tag is automatically listed in [!UICONTROL Admin] > [!UICONTROL Conversions], even if it isn't implemented or the webpages that it's on haven't received any clicks. This behavior is different from the behavior of metrics in tags created manually or elsewhere, which aren't listed in [!UICONTROL Admin] > [!UICONTROL Conversions] until one of the webpages that it's on has received a click. In all cases, however, each metric is initially excluded from portfolio objectives, reports, and views until you explicitly make them available. Before you add the metrics to portfolio objectives, consider first making the metrics available and adding them to reports to verify when they receive clicks.

### Adobe Advertising conversion tag settings {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** The type of tag to create:

* *[!UICONTROL JavaScript]:* To create a JavaScript tag.

* *[!UICONTROL Image]:* To create an image tag to display a 1-pixel x 1-pixel transparent image (pixel), which is invisible to end users, on the webpage. The best practice is to use image tags only when the site has a policy against using JavaScript tags.

For more information about the differences between the tag types, see "[FAQs about Adobe Advertising conversion and page view tracking tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)."

**[!UICONTROL Include unique transaction IDs]:** (Optional) Includes a transaction ID property (`ev_transid=<transid>`) in the tag. The option is selected by default.

When you select this option, the advertiser must generate a unique value for `<transid>` (for example, an actual order ID) when the transaction is complete and pass it back to Adobe Advertising, such as `ev_transid=0123`. Adobe Advertising uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. The transaction ID can't contain ampersand symbols (`&`), which are reserved as parameter separators. The transaction ID is included in [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), which you can use to validate data within Search, Social, & Commerce with the advertiser's data.

If the data doesn't include a unique ID per transaction, then Adobe Advertising still generates one based on transaction time.

>[!NOTE]
>
>If you send [transaction ID feeds](/help/search-social-commerce/tracking/feed-transaction-id.md) with conversion data for offline conversions, then you must submit the transaction ID (`ev_transid`) for the online part of the transaction in the feed data for offline parts of the transaction.

**[!UICONTROL JS Version]:** ([!DNL JavaScript] tags only) Which version of the [!DNL JavaScript] tag to create: *[!UICONTROL v2]* (the default) or *[!UICONTROL v3]*.

**[!UICONTROL Security]:** The security protocol for your website create: *[!UICONTROL Standard]* (for websites that use HTTP) or *[!UICONTROL Secure]* (for websites that use HTTPs).

**[!UICONTROL Properties]:** One or more conversion metrics to be tracked when an end user views a page containing the conversion tag. To add a metric to the list, enter the metric name in the "[!UICONTROL Property name]" field and click **[!UICONTROL Add]**.

When multiple metrics are tracked, they're joined by an ampersand (`&`) in the tag, such as `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrics added to this list aren't saved anywhere or integrated with the client's [!UICONTROL Conversions] list on the [!UICONTROL Admin] tab. However, metrics are added to the client's [!UICONTROL Conversions] list automatically once Adobe Advertising actually gathers data for a metric, which happens when the conversion tag is implemented on a page and an end user completes a transaction that opens that page.

-->
## &#x200B;<!-- (Legacy UI) --> Search, Social, &amp; Commerce内でコンバージョントラッキングタグを生成して実装します

>[!NOTE]
>
>この機能は、広告主のweb ページに画像タグまたは[!DNL JavaScript] タグを追加しません。 広告主または代理店に、各タグを挿入するweb ページのリストを提供します。 タグは、web ページを更新するための広告主の通常の手順に従って追加する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**&#x200B;をクリックします。

1. [&#x200B; コンバージョンタグ設定](#conversion-tag-settings)を指定します。

1. タグを生成：

   * Web サイトでHTTPを使用している場合は、**[!UICONTROL Generate Conversion Tag]**&#x200B;をクリックします。

   * Web サイトが安全なサーバー（HTTPS）で実行されている場合は、**[!UICONTROL Generate Secure Conversion Tag]**&#x200B;をクリックします。

1. ダイアログボックスからタグをコピーし、必要に応じて適切なweb ページに貼り付けます。

>[!NOTE]
>
>新しいコンバージョンタグの各指標は、実装されていない場合やweb ページでクリックが行われていない場合でも、[!UICONTROL Admin] > [!UICONTROL Conversions]に自動的に一覧表示されます。 この動作は、手動または他の場所で作成されたタグ内の指標の動作とは異なり、そのタグ内のweb ページの1つがクリックされるまで[!UICONTROL Admin] > [!UICONTROL Conversions]にリストされません。 ただし、いずれの場合も、明示的に使用可能になるまで、各指標は最初にポートフォリオ目標、レポート、ビューから除外されます。 ただし、指標をポートフォリオ目標に追加する前に、まず指標を使用可能にし、クリックを受け取ったタイミングを検証するためにレポートに追加することを検討してください。

### Adobe Advertising変換タグ設定 {#conversion-tag-settings}

**[!UICONTROL Tag Type]:**&#x200B;作成するタグの種類：

* *[!UICONTROL Image]:*&#x200B;画像タグを作成して、エンドユーザーには見えない1 ピクセル x 1 ピクセルの透明画像（ピクセル）をweb ページに表示します。 ベストプラクティスは、JavaScript タグの使用に対するポリシーがサイトにある場合にのみ、画像タグを使用することです。

* *[!UICONTROL JavaScript]:* JavaScript タグを作成するには。

タグタイプの違いについて詳しくは、「[Adobe Advertising コンバージョンとページビューのトラッキングタグに関するよくある質問](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。

**[!UICONTROL Tag Properties]:** エンドユーザーがコンバージョンタグを含むページを表示したときに追跡される1つ以上のコンバージョン指標。 リストに指標を追加するには、「[!UICONTROL Add new property]」フィールドに指標の名前を入力し、**[!UICONTROL Add]**&#x200B;をクリックします。

複数の指標が追跡されると、タグ内の`ev_Property1=<Property1>&ev_Property2=<Property2>`などのアンパサンド （`&`）によって結合されます。

>[!NOTE]
>
>このリストに追加された指標は、どこにも保存されないか、[!UICONTROL Admin] タブのクライアントの[!UICONTROL Conversions] リストと統合されていません。 ただし、Adobe Advertisingが実際に指標のデータを収集すると、指標がクライアントの[!UICONTROL Conversions] リストに自動的に追加されます。これは、コンバージョンタグがページに実装され、エンドユーザーがそのページを開くトランザクションを完了したときに発生します。

**[!UICONTROL Include unique transaction IDs]:** （オプション）トランザクション ID プロパティ （`ev_transid=<transid>`）がタグに含まれます。 このオプションはデフォルトで選択されています。

このオプションを選択すると、広告主は、トランザクションが完了したときに`<transid>`の一意の値（実際の注文IDなど）を生成し、`ev_transid=0123`などのAdobe Advertisingに渡す必要があります。 Adobe Advertisingでは、トランザクション IDを使用して、同じトランザクション IDとプロパティ値を持つ重複するトランザクションを削除します。 トランザクション IDに、パラメーター区切り記号として予約されているアンパサンド記号（`&`）を含めることはできません。 トランザクション IDは[the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)に含まれており、Search, Social, &amp; Commerce内のデータを広告主のデータで検証するために使用できます。

データにトランザクションごとに一意のIDが含まれていない場合でも、Adobe Advertisingはトランザクション時間に基づいて一意のIDを生成します。

>[!NOTE]
>
>オフライン コンバージョン用のコンバージョンデータを含む[&#x200B; トランザクション ID フィード &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id.md)を送信する場合、トランザクションのオフライン部分のフィード データ内のトランザクションのオンライン部分のトランザクション ID （`ev_transid`）を送信する必要があります。

**[!UICONTROL Page is inside FB app]:**&#x200B;が廃止されました

**[!UICONTROL Segment users]:**&#x200B;が廃止されました

**[!UICONTROL JS Version]:** （[!DNL JavaScript] タグのみ）作成する[!DNL JavaScript] タグのバージョン：*[!UICONTROL v2]* （デフォルト）または&#x200B;*[!UICONTROL v3]*。

「[Adobe Advertising コンバージョンとページビューのトラッキングタグに関するよくある質問](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。 違いに関する詳細については、こちらを参照してください。

## Adobe Experience PlatformタグとAdobe Advertising拡張機能を使用して、コンバージョントラッキングタグを実装する

Adobe Experience Platformのタグを使用して、検索、ソーシャル、Commerceのコンバージョントラッキングを設定できます。 Adobe CX Enterpriseをご利用のお客様は、同梱の付加価値機能としてタグを利用できます。

Experience Platform ユーザーインターフェイスまたはExperience Platform Data Collection ユーザーインターフェイスから、Search、Social、Commerceのコンバージョントラッキングタグを設定するには、次のタスクが必要です。 タグの設定の詳細と手順については、「[Tags overview](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)」および「[&#x200B; クイックスタートガイド &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start)」で始まるExperience Platform タグガイドを参照してください。

>[!PREREQUISITES]
>
>必要なタグ拡張機能をインストールするには、組織の管理者に対して、`manage_properties`権限を含むUIのデータ収集機能へのアクセス権を求めます。

1. [Data Collection UI](https://experience.adobe.com/#/data-collection/)から、Adobe Advertising [拡張機能](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview)をインストールします。

   1. 該当するプロパティから、拡張機能カタログを開き、**Adobe Advertising**&#x200B;を選択します。

   1. プルダウンメニューから、**SSC** （検索、ソーシャル、およびCommerce）を選択します。

   1. **SSC UserID** フィールドに、組織のSearch、Social、およびCommerce アカウントの数値ユーザーIDを入力します。

      ユーザーIDがわからない場合は、Adobe アカウントチームにお問い合わせください。

   1. **保存**&#x200B;をクリックします。

1. 新しいルール（例：「form_completes」）を作成して、Search, Social, &amp; Commerceのコンバージョンタグをトリガーします。

   1. 「イベント設定」セクションで、次の操作を行います。

      1. 次の値を選択します。

         **拡張機能：** `Core`

         **イベントタイプ：** `Library Loaded (Page Top)`

      1. 「**変更を保持**」をクリックします。

   1. 「条件設定」セクションで、次の操作を行います。

      1. 次の値を指定します。

         **ロジックの種類：** `Regular`

         **拡張機能：** `Core`

         **条件タイプ：** `Path Without Query String`

         **パスが次の場合はtrueを返します：** コンバージョンを追跡するパス（例：`/form_complete`）。

      1. 「**変更を保持**」をクリックします。

   1. 「アクション設定」セクションで、次の操作を行います。

      1. 次の値を指定します。

         **拡張機能：** `Adobe Advertising`

         **アクションの種類：** `AMO Measurement`

         **変換プロパティ名：**&#x200B;変換プロパティの名前（例：`form_completes`）。

         **値：** コンバージョンプロパティの数値（form_completesを追跡する`1`など）、または既存の[&#x200B; データ要素](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements)を選択します。

      1. 「**変更を保持**」をクリックします。

   1. ルールを保存します。

1. 変更を公開します。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [&#x200B; トラッキングタグを作成およびデコードするツールについて](tracking-tools-about.md)
>* コンバージョンとページビューのトラッキングタグに関する[FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)の形式
>* [JavaScript コンバージョントラッキングタグバージョン 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)の形式
>* [画像コンバージョントラッキングタグの形式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe Advertising JavaScript コンバージョンマッピングタグ &#x200B;](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
