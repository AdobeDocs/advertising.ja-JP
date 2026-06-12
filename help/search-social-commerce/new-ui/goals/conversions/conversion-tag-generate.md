---
title: （新しいUI） Adobe Advertising コンバージョントラッキングタグの生成と実装
description: Adobe Advertisingのコンバージョンタグを作成して、コンバージョンイベントをトラッキングする方法について説明します。
feature: Search Tools, Search Tracking
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---

# （新しいUI） Adobe Advertising コンバージョントラッキングタグの生成と実装

*Adobe Advertising コンバージョントラッキングのみを使用する広告主*

追跡する指標のセットごとに個別のコンバージョンタグを作成します。 Search、Social、Commerceでタグを生成するか、Adobe Experience Platform（旧Adobe Experience Platform Launch）のタグとAdobe Advertising拡張機能を使用してタグを生成できます。

## Search, Social, &amp; Commerce内でコンバージョントラッキングタグを生成する

>[!NOTE]
>
>この機能は、広告主のweb ページに画像タグまたは[!DNL JavaScript] タグを追加しません。 広告主または代理店に、各タグを挿入するweb ページのリストを提供します。 タグは、web ページを更新するための広告主の通常の手順に従って追加する必要があります。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

1. メインツールバーで、**[!UICONTROL Conversion Tag]**&#x200B;をクリックします。

1. [&#x200B; コンバージョンタグ設定](#conversion-tag-settings)を指定します。

1. **[!UICONTROL Generate]**&#x200B;をクリックします。

1. タグをクリップボードにコピーするには、**[!UICONTROL Copy]**&#x200B;をクリックします。 実装する広告主または代理店にタグを付与します。

>[!NOTE]
>
>新しいコンバージョンタグの各指標は、実装されていない場合やweb ページでクリックが行われていない場合でも、[!UICONTROL Admin] > [!UICONTROL Conversions]に自動的に一覧表示されます。 この動作は、手動または他の場所で作成されたタグ内の指標の動作とは異なり、そのタグのweb ページの1つがクリックされるまで[!UICONTROL Admin] > [!UICONTROL Conversions]にリストされません。 ただし、いずれの場合も、明示的に使用可能になるまで、各指標は最初にポートフォリオ目標、レポート、ビューから除外されます。 指標をポートフォリオ目標に追加する前に、まず指標を使用可能にし、クリックを受け取ったタイミングを検証するためにレポートに追加することを検討してください。

### Adobe Advertising変換タグ設定 {#conversion-tag-settings}

**[!UICONTROL Tag Type]:**&#x200B;作成するタグの種類：

* *[!UICONTROL JavaScript]:* JavaScript タグを作成するには。

* *[!UICONTROL Image]:*&#x200B;画像タグを作成して、エンドユーザーには見えない1 ピクセル x 1 ピクセルの透明画像（ピクセル）をweb ページに表示します。 ベストプラクティスは、JavaScript タグの使用に対するポリシーがサイトにある場合にのみ、画像タグを使用することです。

タグタイプの違いについて詳しくは、「[Adobe Advertising コンバージョンとページビューのトラッキングタグに関するよくある質問](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。

**[!UICONTROL Include unique transaction IDs]:** （オプション）トランザクション ID プロパティ （`ev_transid=<transid>`）がタグに含まれます。 このオプションはデフォルトで選択されています。

このオプションを選択すると、広告主は、トランザクションが完了したときに`<transid>`の一意の値（実際の注文IDなど）を生成し、`ev_transid=0123`などのAdobe Advertisingに渡す必要があります。 Adobe Advertisingでは、トランザクション IDを使用して、同じトランザクション IDとプロパティ値を持つ重複するトランザクションを削除します。 トランザクション IDに、パラメーター区切り記号として予約されているアンパサンド記号（`&`）を含めることはできません。 トランザクション IDは[the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)に含まれており、Search, Social, &amp; Commerce内のデータを広告主のデータで検証するために使用できます。

データにトランザクションごとに一意のIDが含まれていない場合でも、Adobe Advertisingはトランザクション時間に基づいて一意のIDを生成します。

>[!NOTE]
>
>オフライン コンバージョン用のコンバージョンデータを含む[&#x200B; トランザクション ID フィード &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id.md)を送信する場合、トランザクションのオフライン部分のフィード データ内のトランザクションのオンライン部分のトランザクション ID （`ev_transid`）を送信する必要があります。

**[!UICONTROL JS Version]:** （[!DNL JavaScript] タグのみ）作成する[!DNL JavaScript] タグのバージョン：*[!UICONTROL v2]* （デフォルト）または&#x200B;*[!UICONTROL v3]*。

**[!UICONTROL Security]:** Web サイトのセキュリティプロトコルは、次の通りです：*[!UICONTROL Standard]* （HTTPを使用するWeb サイトの場合）または&#x200B;*[!UICONTROL Secure]* （HTTPを使用するWeb サイトの場合）。

**[!UICONTROL Properties]:** エンドユーザーがコンバージョンタグを含むページを表示したときに追跡される1つ以上のコンバージョン指標。 リストに指標を追加するには、「[!UICONTROL Property name]」フィールドに指標の名前を入力し、**[!UICONTROL Add]**&#x200B;をクリックします。

複数の指標が追跡されると、タグ内の`ev_Property1=<Property1>&ev_Property2=<Property2>`などのアンパサンド （`&`）によって結合されます。

>[!NOTE]
>
>このリストに追加された指標は、どこにも保存されないか、[!UICONTROL Admin] タブのクライアントの[!UICONTROL Conversions] リストと統合されていません。 ただし、Adobe Advertisingが実際に指標のデータを収集すると、指標がクライアントの[!UICONTROL Conversions] リストに自動的に追加されます。これは、コンバージョンタグがページに実装され、エンドユーザーがそのページを開くトランザクションを完了したときに発生します。

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
>* [JavaScript コンバージョントラッキングタグバージョン 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)の形式
>* [JavaScript コンバージョントラッキングタグバージョン 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)の形式
>* [画像コンバージョントラッキングタグの形式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe Advertising JavaScript コンバージョンマッピングタグ &#x200B;](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
