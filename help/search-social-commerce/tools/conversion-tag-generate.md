---
title: Adobe Advertisingのコンバージョントラッキングタグを生成して実装する
description: Adobe Advertising コンバージョンタグを作成してコンバージョンイベントをトラッキングする方法について説明します。
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: 96c22e44dc4335b1896f82478985fe976d9a75b9
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Adobe Advertisingのコンバージョントラッキングタグを生成して実装する

*Adobe Advertisingのコンバージョントラッキングのみを使用する広告主*

追跡する指標のセットごとに個別のコンバージョンタグを作成します。 タグは、検索、ソーシャル、Commerceで生成することも、Adobe Experience Platform（旧称：Adobe Experience Platform Launch）のタグを使用して生成することもできます。

## 検索、ソーシャル、Commerce内でのコンバージョントラッキングタグの生成と実装

>[!NOTE]
>
>この機能では、広告主の web ページに画像タグや [!DNL JavaScript] タグを追加しません。 広告主または代理店に、それぞれ挿入する web ページのリストをタグに提供します。 Web ページを更新する際は、広告主の通常の手順に従ってタグを追加する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Conversion Tags]** をクリックします。

1. [&#x200B; 変換タグ設定 &#x200B;](#conversion-tag-settings) を指定します。

1. タグを生成します。

   * Web サイトで HTTP を使用している場合は、「**[!UICONTROL Generate Conversion Tag]**」をクリックします。

   * Web サイトが安全なサーバー（HTTPS）で実行されている場合は、「**[!UICONTROL Generate Secure Conversion Tag]**」をクリックします。

1. ダイアログボックスからタグをコピーし、必要に応じて適切な Web ページに貼り付けます。

>[!NOTE]
>
>新しいコンバージョンタグの各指標は、実装されていない場合や閲覧している web ページがクリックを受け取っていない場合でも、[!UICONTROL Admin]/[!UICONTROL Conversions] に自動的にリストされます。 この動作は、手動または他の場所で作成されたタグの指標の動作とは異なります。タグの動作は、そのタグが含まれる web ページの 1 つがクリックを受け取るまで [!UICONTROL Admin] > [!UICONTROL Conversions] に表示されません。 ただし、どの場合でも、各指標は、明示的に使用可能になるまで、最初はポートフォリオ目標、レポートおよびビューから除外されます。 ただし、ポートフォリオ目標に指標を追加する前に、最初に指標を使用可能にしてレポートに追加し、クリックを受け取ったときに検証することを検討してください。

### Adobe Advertising コンバージョンタグの設定 {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** 作成するタグのタイプ。

* *[!UICONTROL Image]:* 画像タグを作成して、エンドユーザーに表示されない 1 ピクセル x 1 ピクセルの透明な画像（ピクセル）を web ページに表示できるようにします。 ベストプラクティスは、サイトでJavaScript タグの使用に対するポリシーが設定されている場合にのみ、画像タグを使用することです。

* *[!UICONTROL JavaScript]:* JavaScript タグを作成する場合。

タグタイプの違いについて詳しくは、「[Adobe Advertising コンバージョンタグとページビュートラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。

**[!UICONTROL Tag Properties]:** エンドユーザーがコンバージョンタグを含んだページを表示する際に追跡される 1 つ以上のコンバージョン指標。 リストに指標を追加するには、「[!UICONTROL Add new property]」フィールドに指標名を入力し、「**[!UICONTROL Add]**」をクリックします。

複数の指標がトラッキングされる場合、指標は、タグ内でアンパサンド（`&`）によって結合されます（例：`ev_Property1=<Property1>&ev_Property2=<Property2>`）。

>[!NOTE]
>
>このリストに追加された指標は、どこにも保存されず、「[!UICONTROL Conversions]」タブのクライアントの [!UICONTROL Admin] リストと統合されません。 ただし、Adobe Advertisingが指標のデータを実際に収集すると、指標がクライアントの [!UICONTROL Conversions] リストに自動的に追加されます。これは、コンバージョンタグがページに実装され、エンドユーザーがそのページを開くトランザクションを完了した場合に発生します。

**[!UICONTROL Include unique transaction IDs]:** （任意）トランザクション ID プロパティ（`ev_transid=<transid>`）をタグに含めます。 このオプションはデフォルトで選択されています。

このオプションを選択すると、広告主は、取引が完了したときに `<transid>` に一意の値（実際の注文 ID など）を生成し、それを `ev_transid=0123` などのAdobe Advertisingに返す必要があります。 Adobe Advertisingでは、トランザクション ID を使用して、同じトランザクション ID とプロパティ値を持つ重複トランザクションを排除します。 トランザクション ID には、パラメーター区切り記号として予約されているアンパサンド記号（`&`）を含めることはできません。 取引 ID は [the [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) に含まれており、これを使用して、広告主のデータで検索、ソーシャル、Commerce内のデータを検証できます。

データにトランザクションごとの一意の ID が含まれていない場合、Adobe Advertisingでは、トランザクション時間に基づいて一意の ID を生成します。

>[!NOTE]
>
>オフライン変換のコンバージョンデータを使用して [&#x200B; トランザクション ID フィード &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id.md) を送信する場合は、トランザクションのオフライン部分用のフィードデータに含まれているトランザクションのオンライン部分のトランザクション ID （`ev_transid`）を送信する必要があります。

**[!UICONTROL Page is inside FB app]:** 古い

**[!UICONTROL Segment users]:** 古い

**[!UICONTROL JS Version]:** （[!DNL JavaScript] タグのみ）作成する [!DNL JavaScript] タグのバージョンは、*[!UICONTROL v2]* （デフォルト）または *[!UICONTROL v3]* です。

[Adobe Advertising コンバージョンタグとページビュートラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。 違いについて詳しくは、を参照してください。

## Adobe Experience Platform タグを使用したコンバージョントラッキングタグの実装

Adobe Experience Platformのタグを使用して、検索、ソーシャル、Commerceのコンバージョントラッキングを設定できます。 タグは、Adobe Experience Cloudのお客様が、付属の付加価値機能として利用できます。

Experience Platform ユーザーインターフェイスまたはExperience Platform Data Collection ユーザーインターフェイスから、検索、ソーシャル、Commerceのコンバージョントラッキングタグを設定するには、次のタスクが必要です。 タグの設定の詳細と手順については、「[&#x200B; タグの概要 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)」および「[&#x200B; クイックスタートガイド &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start)」で始まる、Experience Platformのタグガイドを参照してください。

>[!PREREQUISITES]
>
>必要なタグ拡張機能をインストールするには、UI のデータ収集機能（`manage_properties` 権限を含む）へのアクセス権を組織の管理者に問い合わせます。

1. [&#x200B; データ収集 UI](https://experience.adobe.com/#/data-collection/) から、Adobe Advertising[&#x200B; 拡張機能 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview) をインストールします。

   1. 該当するプロパティから、拡張機能カタログを開き、「**Adobe Advertising**」を選択します。

   1. プルダウンメニューから **SSC** （検索、ソーシャル、Commerceの場合）を選択します。

   1. **SSC ユーザー ID** フィールドに、組織の検索、ソーシャル、Commerceのアカウントの数値ユーザー ID を入力します。

      ユーザー ID が不明な場合は、Adobe アカウントチームにお問い合わせください。

   1. **保存** をクリックします。

1. 検索、ソーシャル、Commerceのコンバージョンタグをトリガーにする新しいルール（例：「form_completes」）を作成します。

   1. 「イベント設定」セクションで、

      1. 次の値を選択します。

         **拡張機能：** `Core`

         **イベントタイプ：** `Library Loaded (Page Top)`

      1. 「**変更を保持**」をクリックします。

   1. 「条件の設定」セクションで、

      1. 次の値を指定します。

         **論理タイプ：** `Regular`

         **拡張機能：** `Core`

         **条件の種類：** `Path Without Query String`

         **パスが次の値に等しい場合、true を返します：** 変換を追跡するパス（例：`/form_complete`）。

      1. 「**変更を保持**」をクリックします。

   1. アクションの設定セクションで、

      1. 次の値を指定します。

         **拡張機能：** `Adobe Advertising`

         **アクションの種類：** `AMO Measurement`

         **コンバージョンプロパティ名：** コンバージョンプロパティの名前（例：`form_completes`）。

         **Value:** コンバージョンプロパティの数値（例：form_completes を追跡する `1`）、または既存の [data 要素 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) を選択します。

      1. 「**変更を保持**」をクリックします。

   1. ルールを保存します。

1. 変更内容を公開します。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [&#x200B; トラッキングタグを作成およびデコードするツールについて &#x200B;](tracking-tools-about.md)
>* [&#x200B; コンバージョンおよびページビューのトラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [&#x200B; 画像変換トラッキングタグの形式 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe Advertising JavaScript コンバージョンマッピングタグ &#x200B;](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [&#x200B; 広告主のコンバージョン指標の管理について &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
