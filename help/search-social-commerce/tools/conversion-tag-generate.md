---
title: Adobe広告のコンバージョントラッキングタグの生成
description: コンバージョンイベントを追跡するAdobe広告コンバージョンタグを作成する方法について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Adobe広告のコンバージョントラッキングタグの生成

*Adobe広告コンバージョントラッキングのみを持つ広告主*

追跡する指標のセットごとに個別のコンバージョンタグを作成し、それぞれを挿入する Web ページのリストを広告主または代理店に提供します。

>[!NOTE]
>
>この機能では画像タグや [!DNL JavaScript] タグを広告主の Web ページに追加します。 タグは、Web ページを更新する際の広告主の通常の手順に従って追加する必要があります。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. 次を指定： [コンバージョンタグの設定](#conversion-tag-settings).

1. タグを生成します。

   * Web サイトで HTTP を使用している場合は、 **[!UICONTROL Generate Conversion Tag]**.

   * Web サイトがセキュアサーバー (HTTPS) 上で実行されている場合は、 **[!UICONTROL Generate Secure Conversion Tag]**.

1. ダイアログボックスからタグをコピーし、必要に応じて適切な Web ページに貼り付けます。

>[!NOTE]
>
>新しいコンバージョンタグの各指標は、 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]実装されていない場合や、実装されている Web ページがクリックを受け取っていない場合でも、有効です。 この動作は、手動で作成されたタグや他の場所で作成されたタグ ( [!UICONTROL Admin] > [!UICONTROL Transaction Properties] そのウェブページの 1 つがクリックを受け取るまで。 ただし、どの場合でも、明示的に使用可能にするまで、各指標は最初はポートフォリオの目標、レポート、表示から除外されます。 ただし、ポートフォリオの目標に指標を追加する前に、まず指標を使用可能にし、それらの指標をレポートに追加して、いつクリックを受け取ったかを確認することを検討してください。

## Adobe広告コンバージョンタグの設定 {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** 作成するタグのタイプ：

* *[!UICONTROL Image]:* Web ページに 1 ピクセル x 1 ピクセルの透明な画像（ピクセル）を表示するイメージタグを作成するには、エンドユーザーには表示されません。 ベストプラクティスは、サイトに JavaScript タグの使用に対するポリシーが設定されている場合にのみ画像タグを使用することです。

* *[!UICONTROL JavaScript]:* JavaScript タグを作成するには、以下を実行します。

タグタイプの違いについて詳しくは、[Adobe広告コンバージョンおよびページビュートラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** コンバージョンタグを含むページをエンドユーザーが表示した際にトラッキングされる 1 つ以上のトランザクションプロパティ（指標）。 リストに指標を追加するには、「[!UICONTROL Add new property]「 」フィールドで、 **[!UICONTROL Add]**.

複数の指標が追跡されている場合、アンパサンド (`&`) をタグ内に含めることができます。例： `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>このリストに追加された指標は、どこにも保存されず、クライアントの [!UICONTROL Transaction Properties] リスト [!UICONTROL Admin] タブをクリックします。 ただし、指標はクライアントの [!UICONTROL Transaction Properties] Adobe広告は、指標のデータを実際に収集すると、リストを自動的に自動的に作成します。この処理は、コンバージョンタグがページに実装され、エンドユーザーがそのページを開くトランザクションを完了したときに発生します。

**[!UICONTROL Include unique transaction IDs]:** （オプション）トランザクション ID プロパティ (`ev_transid=<transid>`) をタグ内に追加します。 このオプションはデフォルトで選択されています。

このオプションを選択した場合、広告主は `<transid>` （例えば、実際の注文 ID）トランザクションが完了し、それをAdobe広告に返すとき ( 例： `ev_transid=0123`. Adobe広告はトランザクション ID を使用して、同じトランザクション ID とプロパティ値を持つ重複トランザクションを排除します。 トランザクション ID にアンパサンド記号 (`&`) で始まります。これらはパラメーターの区切り文字として予約されています。 トランザクション ID は、 [の [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)：広告主のデータを含む Search、Social および Commerce 内のデータを検証するために使用できます。

データにトランザクションごとの一意の ID が含まれていない場合、Adobe広告はトランザクション時間に基づいて ID を生成します。

>[!NOTE]
>
>送信する場合 [トランザクション ID フィード](/help/search-social-commerce/tracking/feed-transaction-id.md) オフラインコンバージョンのコンバージョンデータを使用する場合、トランザクション ID(`ev_transid`) をクリックします。

**[!UICONTROL Page is inside FB app]:** 廃止

**[!UICONTROL Segment users]:** 廃止

**[!UICONTROL JS Version]:** ([!DNL JavaScript] タグのみ ) [!DNL JavaScript] タグを作成します。 *[!UICONTROL v2]* （デフォルト）または *[!UICONTROL v3]*.

参照：[Adobe広告コンバージョンおよびページビュートラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; を参照してください。

>[!MORELIKETHIS]
>
>* [Adobe広告のコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [トラッキングタグを作成およびデコードするツールについて](tracking-tools-about.md)
>* [コンバージョンおよびページビューのトラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [画像コンバージョントラッキングタグの形式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe広告の JavaScript コンバージョンマッピングタグ](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [広告主のトランザクションプロパティの管理について](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)

