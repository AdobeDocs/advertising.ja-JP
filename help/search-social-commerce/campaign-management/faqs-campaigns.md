---
title: キャンペーンに関するよくある質問
description: キャンペーン管理とキャンペーンデータビューに関する質問への回答を参照してください。
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/5I3xvxMaW-VmMn1UhxtTgt7O68vi--W38VNpV1fE6Rs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1585
ht-degree: 0%

---

# キャンペーン管理に関するよくある質問

## 一般情報

+++キャンペーンとコンポーネントをアカウント間で移動できますか？

一意のIDを持つキャンペーンまたはキャンペーンコンポーネントを、別のアカウント IDを持つアカウントに移動またはコピーしないでください。 これにより、データエラーが発生します。
+++

+++広告ネットワークからクリックデータが更新されるのはいつですか？

検索エンジンから前日のクリックデータを取得するプロセスは、広告主のタイムゾーンの06:00から始まります。

さらに、現在の日の検索ネットワーク上の[!DNL Google Ads]個のキャンペーンレベルのパフォーマンス指標は、広告主のタイムゾーンの08:00と16:00にプルされます。
+++

+++どのようなアクションがキーワードや広告の履歴を失うのか？

>[!NOTE]
>
>（ポートフォリオを持つ広告主） Search, Social, &amp; Commerceがデータを収集してモデルを作成する間、新しいキーワードとマッチタイプの組み合わせのパフォーマンスが不安定になることを期待しています。

**[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] ビュー、バルクシート投稿プロセス、および広告ネットワーク独自のエディターでのアクション：**

既存のキーワードまたは広告が削除され、次の場合に別のキーワードが作成されます。

* （[!DNL Baidu]、[!DNL Google Ads]、[!DNL Yandex]）キーワード名を編集します。

* （[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]） キーワードの一致タイプを変更しました。

* 広告グループ間でキーワードを移動します。

* （[!DNL Google Ads]件の動的検索広告、[!DNL Microsoft Advertising]件の拡張テキスト広告、およびその他のサポートされている広告ネットワーク上のすべての広告タイプ）広告コピー（見出し/タイトルまたは説明）または広告画像を編集します。

* 広告グループ間で広告を移動します。

**製品インベントリ フィード投稿プロセスのイベント：**

既存の広告またはキーワードが削除され、次の場合に別の広告またはキーワードが作成されます。

* フィードファイルには、広告バリエーションで使用される列の新しい値が含まれます。

* 広告のテンプレート設定は、前回の伝播以降に変更されました。

* 新しいフィードファイルには、a）以前のファイルにあったがb）以降に省略され、フィードデータの設定に従って一時停止または削除された広告またはキーワードの行が含まれます。

[&#x200B; フィード データ設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)に応じて、次の場合に既存の広告またはキーワードが削除される場合があります。

* 新しいフィード ファイルには、既存の広告またはキーワードの行が含まれていません。

* 投稿されたフィード ファイルのコンポーネントの予定終了日が発生します。

* 品目の在庫レベルが、フィードデータ設定で指定された最小値を下回っています。
+++

+++（[!DNL Google Ads] キャンペーン）トラッキングされた[!DNL Google]個のコンバージョンの表示名の変更が元に戻されました。

Search、Social、およびCommerceでコンバージョン指標の表示名を変更すると、変更内容が[!DNL Google Ads]で設定された名前で上書きされます。 [!DNL Google Ads]内で名前を変更します。
+++

+++（Google Ads キャンペーン） ポートフォリオのキャンペーンに共有予算を使用できますか？

最良の結果を得るには、「[!DNL Google Ads]」に設定された最適化されたポートフォリオにあるキャンペーンを[!DNL Google Ads]の共有予算に[!UICONTROL Auto adjust campaign budget limits]件を追加しないでください。 この場合、[!DNL Google Ads]がSearch, Social, &amp; Commerceに最適化されたキャンペーン予算を上書きするため、入札が非効率になる可能性があります。
+++

+++（[!DNL Google Ads] キャンペーン） モバイルユーザーとモバイルユーザー以外のユーザーを異なるランディングページに送信できますか？

[!DNL Google Ads] [!DNL ValueTrack] パラメーター`{ifmobile}`および`{ifnotmobile}`を使用して、サイトに適用できる2つの方法のいずれかでランディングページのドメイン名を決定できます。

* `{ifmobile:m}{ifnotmobile:www}`を使用して、モバイル指定をホストサーバーとして含めます。

  例えば、`http://{ifmobile:m}{ifnotmobile:www}.example.com`はモバイルユーザーをm.example.comに、モバイル以外のユーザーをwww.example.comに移動します。

* `{ifmobile:mobi}{ifnotmobile:com}`を使用して、モバイル指定を最上位ドメインとして含めます。

  例えば、`http://www.example.{ifmobile:mobi}{ifnotmobile:com}`はモバイルユーザーをwww.example.mobiに、非モバイルユーザーをwww.example.comに移動します。

いずれの場合も、Search、Social、およびCommerce トラッキングを含むベース URLには、エンコードされていない`{}` タグと、ベース URLに追加された追加パラメーターが含まれます。

>[!NOTE]
>
>ifnotmobileおよびifmobile パラメーターの値として完全なURLを使用しないでください。URLの変数部分（「m」と「www」、「mobi」と「com」など）のみを使用してください。

+++

+++（検索ネットワーク上の[!DNL Google Ads] キャンペーン）今日のデータは何ですか？

現在の日の検索ネットワーク上の[!DNL Google Ads]個のキャンペーンレベルのパフォーマンス指標が、広告主のタイムゾーンの08:00と16:00にプルされます。

[!UICONTROL Campaigns] > [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] ビューと[!UICONTROL Campaigns] > [!UICONTROL Optimization] ビューの両方の[!UICONTROL Portfolios] タブで、[!UICONTROL Today]または現在の日付を含むカスタム日付範囲についてレポートする場合、データには最近同期されたデータが含まれます。

>[!NOTE]
>
>クリック数、インプレッション数、コンバージョン数などのデータは、3時間遅れになり、次のデータ取得まで完了しません。

+++

+++トラッキングテンプレートとランディングページの接尾辞の違いは何ですか？

ランディングページのサフィックスは、並列トラッキングをサポートする広告ネットワークにのみ使用します。 Search, Social, &amp; Commerceでは、トラッキングテンプレートとランディングページのサフィックスの両方に広告ネットワークのクリック識別子を含める必要がありますが、トラッキングテンプレートには追加のトラッキングパラメーターが含まれています。

ユーザーが広告をクリックしたときにトラッキングテンプレートとランディングページのサフィックスが読み込まれる方法について詳しくは、[&#x200B; パラレルトラッキングサポート &#x200B;](#parallel-tracking)に関する次のFAQを参照してください。

+++

+++（[!DNL Google Ads]および[!DNL Microsoft Advertising]） Search、Social、およびCommerceは、[!DNL Google Ads]または[!DNL Microsoft Advertising]の広告の並行トラッキングをサポートしていますか？{#parallel-tracking}

パラレルトラッキングは、広告から最終的なURLに顧客を直接送信します。これには、最終的なURL サフィックスや「ランディングページサフィックス」から追加されたパラメーターが含まれます。 トラッキングテンプレートのURL （クリック測定用の追加パラメーターを含む）は、バックグラウンドで個別に読み込まれます。その結果、ランディングページがより迅速に読み込まれます。

Search, Social, &amp; Commerceでは、広告ネットワークのクリック識別子（`msclkid`は[!DNL Microsoft Advertising]、`gclid`は[!DNL Google Ads]）を使用して、検索キャンペーンとショッピングキャンペーンを並行して追跡できます。 ランディングページ URLに追加される[&#x200B; アカウントレベル &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings)または[&#x200B; キャンペーンレベル &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix]を使用して、並列追跡をサポートするブラウザーからの子広告のクリックを追跡します。 [!DNL final URL suffix][の [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必要なサフィックス形式と[の [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必要なサフィックス形式を参照してください。

ユーザーが並列トラッキングをサポートしていないブラウザーで広告を表示する場合、広告ネットワークは代わりにシーケンシャルトラッキングを使用します。顧客はまずトラッキングテンプレート URLに送信され、中間追跡サーバーに顧客をリダイレクトしてから最終的なURL （ランディングページサフィックスに追加のパラメーターを含む場合がある）にリダイレクトされます。 広告ネットワークアカウントのすべてのトラッキングテンプレートには、[!UICONTROL Landing Page Suffix]で使用するのと同じクリック識別子パラメーターを含める必要があります。 [の [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) トラッキングテンプレート形式と[の [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) トラッキングテンプレート形式を参照してください。
+++

+++広告のトラッキング URLに「`&EV_HASH={<hash>}`」が含まれているのはなぜですか？

Search, Social, &amp; Commerce ピクセルリダイレクトを使用し、キーワードレベルおよびクリエイティブレベルのトラッキングを使用するアカウントの[商品インベントリフィード &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)を使用して広告をアップロードすると、Search, Social, &amp; Commerceは、広告のトラッキングテンプレートまたは宛先URLにハッシュパラメーターと値を追加して、インベントリフィード機能を使用して作成されたことを識別します。
+++

## 在庫フィード

+++（商品の在庫フィード）古い広告や、在庫レベルが指定された最小値未満の商品の広告を一時停止または削除しますか？

広告主のビジネス要件によって異なります。

広告を一時停止すると、同じ広告を再送信するか、在庫レベルが最小値を超えると、広告が再度有効になります。 これにより、広告の履歴を保持できます。

広告を削除して再送信すると、新しい広告が作成され、新しい広告の履歴データを蓄積する必要があります。 しかし、削除した広告を再送信することを想定していない場合、過去のデータがあることは重要ではありません。
+++

+++（製品在庫フィード）広告テンプレートを削除してから新しい同一の広告テンプレートを作成した場合、次のフィード ファイルで欠落している項目が一時停止されますか（フィード ファイル設定が一時停止するように設定されている場合）?

次のフィードファイルに行項目が欠落していて、以前に以前のフィードファイルを介して新しいテンプレートからそれらの行項目を投稿したことがない場合、欠落している行項目は「欠落」として認識されないため、作成されません。 これを回避するには、新しいテンプレートを通じて前のフィードファイルを伝播し、新しいファイルからデータを伝播して転記する前にデータを転記します。
+++

+++（商品の在庫フィード）広告の品質スコアに影響を与えることなく、商品の価格を更新できますか？

[!DNL Google Ads] キャンペーンの場合、はい：[!DNL Google Ads] `{Param 1}`変数と`{Param 2}`変数を使用すると、広告を削除および再作成することなく、つまり品質スコアに影響を与えることなく、広告バリエーションに数値を動的に挿入できます。

価格データに`{Param 1}`または`{Param 2}`変数を使用するには、データファイルの価格列を適切なフィード テンプレートの変数にマッピングし、その変数を広告バリエーション テンプレートに含めます。

例えば、列が「価格」と呼ばれる場合、広告を作成するフィードテンプレートを開き、**[!UICONTROL Param 1]**&#x200B;の横にある入力フィールドをクリックし、**[!UICONTROL Price]** リストの[!UICONTROL Feeds/Available Columns]列をクリックします。この列では、`[Price]`が[!UICONTROL Param 1]の値として挿入されます。 次に、フィード テンプレートの下部にある広告バリエーション テンプレートに`{param1:default text}`を挿入します。フィード ファイルのパラメーター列が広告行に対して空の場合に使用する「デフォルト テキスト」はテキストです。

データを送信する場合、[!UICONTROL Param1]列と[!UICONTROL Param2]列のデータフィールドには、数値データ、通貨記号と通貨コード、および次の非数値文字を含む、最大25文字を含めることができます：`, . % + - /`
+++

+++在庫フィードから生成されたキャンペーンには、孤立したトランザクションが多く含まれています。

[&#x200B; フィードデータ設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)が様々な状況で広告を削除するように設定されている場合、広告をクリックした後に発生するコンバージョンの遅延は、[孤立トランザクション &#x200B;](/help/search-social-commerce/glossary.md#o-p)の原因となる可能性があります。 広告を削除する代わりに、広告を一時停止することをお勧めします。 広告がまだ長い間収益を受け取っていない場合は、バルクシートまたは広告管理ビューを使用して広告を削除できます。
+++

## アカウントおよびキャンペーン関連のパフォーマンスの問題

+++キャンペーンの予算を上回ったり下回ったりしているキャンペーンもあります。

* これは、「[!UICONTROL Auto adjust campaign budget limits]」オプションで設定された最適化されたポートフォリオでは通常です。 このオプションを有効にすると、各キャンペーンの予算の&#x200B;*N*&#x200B;倍まで費やすことができます。ここで、*N*&#x200B;は「[!UICONTROL Multiple]」設定の値です。 このオプションにより、最適化機能は、必要に応じて個々のキャンペーンの支出を調整しながら、ポートフォリオ全体をその目標に合わせて誘導することができます。
* [!DNL Google Ads]件のキャンペーンで共有予算が使用されている場合、[!DNL Google Ads]は、必要に応じて個々のキャンペーンの支出を調整して、共有予算全体を費やします。
+++
