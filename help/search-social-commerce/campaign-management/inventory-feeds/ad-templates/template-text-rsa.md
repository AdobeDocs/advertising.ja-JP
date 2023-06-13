---
title: 在庫フィード用のテキスト広告およびレスポンシブ検索広告テンプレート設定
description: 在庫フィードに対して、テキスト広告およびレスポンシブ検索広告テンプレートの設定を参照します。
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '3317'
ht-degree: 0%

---

# 在庫フィード用のテキスト広告およびレスポンシブ検索広告テンプレート設定


*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名の指定用に予約されているため、すべての属性フィールドのテキストとして使用することはできません。  `[ ] < > `
>* In [!DNL Yandex templates]に値を指定しない場合は、動的パラメーターを使用できます `{param1}` および `{param2}` は URL 内のみで、広告の説明に動的な価格挿入は使用できません。

## \[ すべてのタブの上\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[ 左パネル\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** （オプション）すべての新しい広告グループをマッピングします（以下では使用できません）。 [!DNL Yandex])、キーワードおよび広告を、キャンペーンを作成するのではなく、既存のキャンペーンに追加する必要があります。 このオプションを有効にする場合、マッピング方法を選択します。

使用 [!UICONTROL Map Only] キャンペーンレベルでは、製品の分類に密接に関連し、データフィードに簡単にマッピングできる既存のアカウント構造が必要です。

**[!UICONTROL Map Method]:** ( [!UICONTROL Map Only] がキャンペーンに対して有効になっている ) 新規の広告グループを使用する方法 ( [!DNL Yandex])、キーワードおよび広告は、既存のキャンペーンにマッピングされます。

* *[!UICONTROL Contains Anywhere]:* 指定した文字列を含む名前を持つ既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Contains Exactly]:* 指定した文字列を含む名前を持つ既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Exactly Matches]* （デフォルト）:同じ名前の既存のキャンペーンが存在する場合は、そのキャンペーンにデータを追加します。

一致するものが見つからない場合、キャンペーンのすべてのデータが無視されます。 複数のキャンペーンが一致する場合、キーワードと広告はすべてのキャンペーンにマッピングされます。

**[!UICONTROL Campaign Tracking Template]:** ( 最終/詳細 URL のみのアカウント。（オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込む、キャンペーンレベルのトラッキングテンプレート。 この値はアカウントレベルの設定より優先されますが、より詳細なレベル（最も詳細なキーワードを含む）でのトラッキングテンプレートは、この値よりも優先されます。

* Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、リダイレクトおよびトラッキングコードを自動的に追加します。

* 最終 URL を埋め込むには：

   * ([!DNL Google Ads] および [!DNL Microsoft® Advertising] のみ ) トラッキングテンプレートの最終 URL を示すパラメーターのリストについては、[!DNL Microsoft® Advertising] のみ ) [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799/2) または ([!DNL Google Ads] （のみ）「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] パラメーター」( [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] のみ ) パラメーターを使用する `!{unescapedurl}` をクリックして、ランディングページの URL を指定します。

   * オプションとして、URL パラメーターと、キャンペーンに定義されているカスタムパラメーターを、アンパサンド (&amp;) で区切って含めることができます。例えば、 `{lpurl}?matchtype={matchtype}&device={device}`.

* サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** ( 内 [!DNL Google Ads] および [!DNL Yandex] キャンペーン設定 ) 広告を配置するネットワーク：

* *[!UICONTROL Search]:* スポンサー付き検索リストの入札を行う。

  ([!DNL Google Ads] （キャンペーン）次の項目のリストに入札を含める [!DNL Google Ads] 検索パートナーの横にあるチェックボックスを選択します。 **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* コンテンツ（ディスプレイ）のネットワークリストに配置の入札を配置する。 **注意：** テンプレートを使用して配置を作成することはできません。 このオプションを選択する場合、各広告グループに配置を作成し、次のいずれかを使用して、各広告グループに対してターゲットにするディスプレイネットワーク上のページを指定します。 <!-- insert link --> バルクシートまたは <!-- insert links --> 以下の広告グループとプレースメント設定 [!UICONTROL Search] > [!UICONTROL Campaigns] ビュー。

**[!UICONTROL Languages]:** ([!DNL Google Ads] 検索および表示ネットワークのみ ) キャンペーン内の広告に対する 1 つ以上のターゲット言語。

[!DNL Google Ads] は、ユーザーの [!DNL Google] 言語設定、検索クエリの言語、現在のページ、または [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** （最終/詳細 URL のアカウントのみ）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込む広告グループレベルのトラッキングテンプレート。

Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、リダイレクトおよびトラッキングコードを自動的に追加します。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページの URL を指定するには：

* Yahoo! Japan Ads アカウントでは、パラメーターを使用してください {lpurl}.

* Microsoft® Advertising およびGoogle Ads のアカウントで使用できるパラメーターについては、 [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799) または、「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] パラメーター」( [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348).

この値は、アカウントレベルとキャンペーンレベルの設定より優先されますが、より詳細なレベル（最も詳細なキーワードを含む）でのトラッキングテンプレートは、この値よりも優先されます。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** 指定した広告グループ ( またはキャンペーンのキーワード： [!DNL Yandex] アカウント ) です。静的テキスト、指定したファイル内の列、および修飾子の任意の組み合わせで構成できます。 列名と修飾子は、指定したフィードファイルがテンプレートを通じて伝播される際に、実際のデータに置き換えられます。

列名または修飾子グループを動的パラメータとして挿入するには、入力フィールドをクリックし、列リスト内の列名または [修飾子名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) を選択します。 同じキーワードに複数のキーワードまたは複数の一致タイプを指定するには、それぞれを別々の行に入力します。 キーワードの一致タイプを指定するには、列名の周囲で次の一致タイプ構文を使用します。

* の場合 [!DNL Google Ads], [!DNL Microsoft® Advertising]、および [!DNL Yahoo! Japan Ads] テンプレート：

   * 動的パラメーターの場合：部分一致= `[keyword]`、最初のキーワードの部分一致修飾子 ( [!UICONTROL Keyword] 列（+青いスエードの靴など） = `+[keyword]`、キーワード列の各キーワードの部分一致修飾子（+blue +suede +shoes など） = `+[keyword]+`, Phrase Match = `"[keyword]"`, Exact Match = `[[keyword]]`

   * 静的キーワードの場合：部分一致= `keyword`、部分一致修飾子= `+keyword`、またはフレーズ一致= `"keyword"`

     完全一致および標準一致構文を持つ静的キーワードは、角括弧 (`[]`) と同様に、動的パラメーターと同様に使用できます。

* の場合 [!DNL Yandex] テンプレート：

   * 動的パラメーターの場合：列名（例： ）を挿入します。 `[keyword]`. 一致タイプを示すには、 [[!DNL Yandex] — 固有の構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **注意：** 部分一致キーワードの場合は、次の構文を使用します。キーワード列の最初のキーワードの部分一致修飾子（+blue suede shoes など） = `+[keyword]`、キーワード列の各キーワードの部分一致修飾子（+blue +suede +shoes など） = `+[keyword]+`

   * 静的キーワードの場合：検索キーワードのみがサポートされます。 以下を使用： [[!DNL Yandex] — 固有の構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html) を設定します。 括弧 (`[]`) をクリックして、単語の順序がサポートされていないことを示します。

>[!NOTE]
>
>* 「キーワード」フィールドに複数の修飾子の値を手動で含めるには、キーワードパラメータの前または後の括弧内にコンマ区切りの値を含めます（両方の場所には含めません）。 例： `(cheap, discount, affordable)[product]` は、各製品に対して 3 つの異なる広告を生成します。
>* 一致タイプを指定しない場合、デフォルトの一致タイプ「broad」が使用されます。
* 負の一致はサポートされていません。
* Google部分一致修飾子は、一部の言語でフレーズ一致と同じ一致動作を示すようになりました。また、新しい部分一致修飾子キーワードを作成することはできません。 詳しくは、 [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/10286719) を参照してください。

**[!UICONTROL Map Only]:** 新しい広告を広告グループ ( または [!DNL Yandex] アカウント ) を検索する際に使用されます。 このオプションを有効にするには、チェックボックスをオンにします。 このオプションを有効にすると、指定したキーワードが存在するので、指定したキーワード内の Param 1 および Param 2 変数は適用されません。

**[!UICONTROL Keyword Final URL]:** ( 最終/詳細 URL を持つアカウント（オプション）広告をクリックしたときに広告ネットワークユーザーが取得するランディングページの URL。 これには表示 URL と同じドメインを含める必要があり、最終 URL のパラメーターは、広告クリック後のランディングページ URL のパラメーターと一致する必要があります。 ランディングページドメインまたはサブドメイン内ではリダイレクトが含まれる場合がありますが、ランディングページドメイン外ではリダイレクトされません。

次を使用する場合、 [!DNL Google Merchant Center] フィードに格納し、この値を「[!DNL Link]」列を挿入し、このフィールドにその列を挿入します。

>[!NOTE]
>
* テンプレートを通じて伝播されるデータを投稿する際にトラッキング URL を生成する場合、アカウントトラッキング設定に基づいて、トラッキングパラメーターがこの値に追加されます。
* ([!DNL Google Ads] アカウント ) マクロの使用は避けてください。マクロは、並列追跡を有効にするソースからのクリック数に置き換えられません。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

**[!UICONTROL Keyword Tracking Template]:** ( 最終/詳細 URL を持つアカウント（オプション）すべてのオフランディングドメインのリダイレクトおよびトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込むトラッキングテンプレート。 最も詳細なレベル（最も詳細なレベルのキーワードを含む）のトラッキングテンプレートは、他のすべてのレベルで値を上書きします。

* Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、リダイレクトおよびトラッキングコードを自動的に追加します。

* オプションで、サードパーティのリダイレクトとトラッキングを入力できます。

* ランディングページの URL を指定するには：

   * ([!DNL Google Ads] および [!DNL Microsoft® Advertising] のみ ) トラッキングテンプレートの最終 URL を示すパラメーターのリストについては、[!DNL Microsoft® Advertising] のみ ) [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799) または ([!DNL Google Ads] （のみ）「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] パラメーター」( [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] のみ ) パラメーターを使用する `!{lpurl}` をクリックして、ランディングページの URL を指定します。

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** ([!DNL Google Ads] templates のみ ) 指定したファイル内の、 [!DNL Google Ads] `{param1}` または `{param2}` 変数に含めることができます。この変数は、テンプレートから作成された広告の広告コピーまたは表示 URL に含めることができます。 動的パラメータを挿入するには、入力フィールドをクリックし、列リストで列名をクリックします。 フィードファイルがテンプレートを通じて伝播されると、列名が実際のデータに置き換えられます。

どちらかのパラメーターを使用する場合、新しいキーワードにのみパラメーターを適用するか、テンプレートから作成されなかった既存のキーワードの値も更新するかを選択できます。

* **[!UICONTROL Do Not Apply to Existing Keywords]** （デフォルト）:テンプレートを使用して作成された新しいキーワードのパラメータの値を挿入します。

* **[!UICONTROL Apply to Existing Keywords: Constant]:** フィードから新しいキーワードを作成するだけでなく、検索、ソーシャル、コマースでも、テンプレートを使用して作成されなかった、広告グループ内の既存のすべてのキーワードのパラメーターの値が更新されます。 これらのすべてのキーワードに使用する 1 つの数値を入力します。 テンプレートには少なくとも 1 つのキーワードが含まれている必要があります。

* **[!UICONTROL Apply to Existing Keywords: Min]:** フィードから新しいキーワードを作成するだけでなく、フィードファイルに小数点以下 1 桁までの数値が含まれ、カンマ、通貨記号、コード、その他の文字を含まない限り、広告グループ内の既存のキーワードの値も更新されます。 フィードファイル内のパラメーターの最小値は、既存のすべてのキーワードで使用されます。 例えば、フィードファイルに [!UICONTROL Param1] 21500と22000の値、 [!UICONTROL Param1] 既存のキーワードの値が21500に変更されます。 テンプレートには少なくとも 1 つのキーワードが含まれている必要があります。 **ヒント：** キーワードが同じ値を持つことが意味をなすように、広告グループに厳密なテーマを設定している場合にのみ、このオプションを使用します。

フィードファイルのデータフィールドは、最大 25 文字で、次の数字以外の文字を含む数値データのみで構成される場合があります。

* ([!UICONTROL Apply to Existing Keywords: Min]&quot;パラメータ ) 小数点以下 1 桁までです。

* ([!UICONTROL Apply to Existing Keywords: Min]&quot;パラメータ ):

   * 値の前後に通貨記号やコードを付けることができます。 例えば、£2.000,000 と 2000GBP が有効です。

   * 値には、コンマ (,) またはピリオド (.) を含めることができます を区切り文字として指定し、オプションでピリオド (.) を使用できます。 小数値の場合はコンマ (,)。 例えば、1,000.00 と 2.000,10 が有効です。

   * 値の前には、パーセント記号 (%)、プラス記号 (+)、マイナス記号 (-) を付けることができます。 例えば、20%、208+、-42.32 が有効です。

   * 2 つの数字をフォワードスラッシュで埋め込むことができます。 例えば、4/1 と 0.95/0.45 が有効です。

**[!UICONTROL Param 2]\[[!DNL Microsoft® Advertising] templates\]:** ([!DNL Microsoft® Advertising] templates のみ ) タイトル、テキスト、表示 URL または最終 URL に `{Param2}` 動的置換文字列。 最大長は 70 文字ですが、使用する広告要素の最大長に注意してください（例えば、広告タイトルは最大 25 文字までです）。

**[!UICONTROL Param 3]:** ([!DNL Microsoft® Advertising] templates のみ ) タイトル、テキスト、表示 URL または最終 URL に `{Param3}` 動的置換文字列。 最大長は 70 文字ですが、使用する広告要素の最大長に注意してください（例えば、広告タイトルは最大 25 文字までです）。

**[!UICONTROL Initial Bid (&lt;Match Type or Ad Type>)]:** 指定した一致タイプまたは広告タイプを持つ各キーワードの初期入札。

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンのみ ) 広告のタイプ： *[!UICONTROL Expanded Search Ads]* または *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** （オプション）すべての代替広告コピーフィールドに、元の広告コピーフィールドのテキストを事前入力します。

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）タイトル/ヘッドラインを含める必要がある広告の位置 ( 例：[!UICONTROL Pinned at position 1]&quot;) です。 デフォルトはです。 [!UICONTROL Unpinned].

各位置に少なくとも 1 つのタイトルを使用できる必要があります。 複数のタイトルを同じ位置に固定すると、最終的な広告には、指定した位置のタイトルの 1 つが常に含まれます。 位置 3 にピン留めされたタイトルは、広告と共に表示されない場合があります。

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** （レスポンシブ検索広告のみ）広告タイトル（ヘッドライン）。 各広告バリエーションには、少なくとも 3 つの広告タイトルと、最大 15 個の広告タイトルを含める必要があります。 広告ネットワークには、最大 3 つのヘッドラインを持つ広告が表示されます。 各タイトルの最大長は、任意の動的テキスト（キーワードの値や広告のカスタマイズ者など）を含む 30 文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** ( 既存のMicrosoft® Advertising 標準テキスト広告のみ。読み取り専用 ) 広告のタイトル（1 行目）。 Microsoft® Advertising は、標準テキスト広告の作成と編集を廃止しました。

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] および [!DNL Yahoo! Japan Ads] 拡張/拡張テキスト広告テンプレートのみ ) 広告のヘッドライン。 各行の最大長（動的パラメーターの置き換え後）は、30 文字または 2 バイト文字 15 文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] 拡張テキスト広告テンプレートのみ。（オプション）広告の 3 番目のヘッドライン。 （動的パラメーターの置き換え後の）最大長は 30 文字または 2 バイト文字 15 文字です。

**[!UICONTROL Title]:** ([!DNL Yandex] のみ ) 広告のタイトル（1 行目）。 最大 33 文字です。

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Microsoft® Advertising expanded text ads only) 広告のヘッドライン。 各行の最大長（動的パラメーターの置き換え後）は、30 文字または 2 バイト文字 15 文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Microsoft® Advertising 拡張テキスト広告のみ ) 広告の本文。 最大長（動的パラメーターが置き換えられた後）は、80 文字または 2 バイト文字（中国語、日本語、韓国語など）40 文字です。

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** 広告の本文。

* (Google Ads 拡張テキスト広告テンプレート )（動的パラメーターが置き換えられた後の）最大長は 90 文字または 45 ダブルバイト文字です。

* (Yahoo! Japan Ads テンプレート )（動的パラメーターが置き換えられた後の）最大長は、80 文字または 40 バイト文字です。

* （Yandex テンプレート）動的パラメーターの置き換え後の最大長は 75 文字で、1 単語に対して 22 文字以内にする必要があります。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）説明を含める必要がある広告の位置 (「[!UICONTROL Pinned at position 1]&quot;) です。 デフォルトはです。 [!UICONTROL Unpinned]. 各位置に対して、少なくとも 1 つの説明を使用できる必要があります。

複数の説明を同じ位置にピン留めすると、最終的な広告には、指定した位置にそれらの説明の 1 つが常に含まれます。 位置 2 に固定された説明は、広告と共に表示されない場合があります。

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** （レスポンシブ検索広告のみ）広告の説明。 各広告バリエーションには、広告の説明を少なくとも 2 つ、最大 4 つ含める必要があります。 広告ネットワークには、最大 2 つの説明を持つ広告が表示されます。少なくとも 2 つを入力してください。 各説明の最大の長さは、任意の動的テキスト（キーワードの値や広告のカスタマイズ子など）を含む 90 文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Googleの拡張テキスト広告テンプレートのみ )（オプション）広告の 2 行目。 （動的パラメーターの置き換え後の）最大長は 90 文字または 45 文字の 2 バイト文字です。

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** ( 拡張テキストおよびレスポンシブ検索広告のみ。（オプション）ベース URL の後に連続して含める 1 つまたは 2 つの URL パス。 広告内の製品やサービスについて、より詳細に説明する必要があります。 例えば、 [!UICONTROL Display Path 1] 「靴」と [!UICONTROL Display Path 2] の「Outdoor」をベース URL www.example.comに設定した場合、URL はwww.example.com/Shoes/Outdoorになります。 各フィールドの最大の長さ（動的パラメーターの置き換え後）は、15 文字または 2 バイト文字 7 文字です。

レスポンシブ検索広告の場合、次の形式を使用して広告をカスタマイズします。ここで、 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`例： `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}`例： `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** ( 既存 [!DNL Microsoft® Advertising] および [!DNL Yahoo! Japan Ads] 標準テキスト広告のみ；読み取り専用 ) 広告に表示される URL。

[!DNL Microsoft® Advertising] および [!DNL Yahoo! Japan Ads] 標準テキスト広告の作成と編集を廃止しました。

**[!UICONTROL Base URL]:** （リンク先 URL のアカウントのみ）ユーザーが移動するページ。 サードパーティのリダイレクトやトラッキングコードを含めることができます。 Adobe Advertisingコンバージョントラッキングサービスを使用し、キャンペーン設定に [!UICONTROL EF Redirect] 広告レベルでトラッキングを追加すると、検索、ソーシャル、コマースによって、独自のリダイレクトとトラッキングコードが広告に自動的に追加されます。

列名または修飾子グループを動的パラメータとして挿入するには、入力フィールドをクリックし、列リスト内の列名または [修飾子名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) 内 [!UICONTROL Modifiers] リスト。

**[!UICONTROL Final URL]:** （最終/詳細 URL のアカウント）ユーザーが広告をクリックしたときに取得されるランディングページの URL。 これには表示 URL と同じドメインを含める必要があり、最終 URL のパラメーターは、広告クリック後のランディングページ URL のパラメーターと一致する必要があります。 ランディングページドメインまたはサブドメイン内ではリダイレクトが含まれる場合がありますが、ランディングページドメイン外ではリダイレクトされません。

次を使用する場合、 [!DNL Google Merchant] フィードを中央揃えにし、この値を「[!UICONTROL Link]」列を挿入し、このフィールドにその列を挿入します。

>[!NOTE]
>
* テンプレートを通じて伝播されるデータを投稿する際にトラッキング URL を生成する場合、アカウントトラッキング設定に基づいてトラッキングパラメーターがこの値に追加されます。
* ([!DNL Google Ads] アカウント ) マクロの使用は避けてください。マクロは、並列追跡を有効にするソースからのクリック数に置き換えられません。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

**[!UICONTROL Tracking Template]:** ( 最終/詳細 URL を持つアカウント（オプション）すべてのオフランディングドメインのリダイレクトおよびトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込むトラッキングテンプレート。 最も詳細なレベル（最も詳細なレベルのキーワードを含む）のトラッキングテンプレートは、他のすべてのレベルで値を上書きします。

Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、リダイレクトおよびトラッキングコードを自動的に追加します。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページの URL を指定するには：

* Yahoo! Japan Ads アカウントでは、パラメーターを使用してください {lpurl}.

* Microsoft® Advertising およびGoogle Ads のアカウントで使用できるパラメーターについては、 [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799) または、「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] パラメーター」( [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348).

**\[ 元の広告フィールドの下の代替広告フィールド\]:** （オプション）広告の代替広告コピー。元の広告コピーの行のいずれかが、伝播中に動的パラメーターにデータが入力された後で許容される最大長を超えた場合に使用できます。

>[!NOTE]
>
* この [!UICONTROL Prefill] 「 」オプションを選択した場合、代替フィールドには元のフィールドが事前に入力され、必要に応じて編集できます。
* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成される広告バリエーションは、別のヘッドラインまたはタイトルと元の説明を使用します。 したがって、元の広告コピーと組み合わせると、代替広告コピーが意味を持つようにします。
* 元の広告コピーが検索エンジンの長さの要件を満たす場合、代替広告コピーは破棄されます。

**\[ コンポーネント\] [!UICONTROL Ad Label Classifications] > \[ ラベルの分類と値\]:** （オプション）テンプレートを使用して作成または編集される広告バリエーションに割り当てる、最大 5 つの既存のラベル分類の値。 ラベル分類を割り当てるキャンペーンコンポーネントごとに、次の操作を行います。

1. チェックボックスをクリックします。

1. 広告バリエーションテンプレートのラベル分類値を設定します。

   * コンポーネントに割り当てるラベルの分類と値ごとに、次の操作を行います。

      1. クリック **[!UICONTROL Add Label Classification]**.

      1. 既存のラベル分類を選択し、既存の値を選択するか、新しい値を入力します。

         各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

         ラベル分類値の動的パラメータとして列名を挿入するには、入力フィールド（2 番目のフィールド）をクリックし、列リストで列名をクリックします。

         キャンペーンコンポーネントごとに、分類ごとに 1 つの値のみを含めることができます。 例えば、キャンペーンの色は赤に設定できますが、色は赤に、色は青に設定できません。

         * 既存のラベル分類値を変更するには、「 」を選択するか、新しい値を入力します。

         * 既存のラベル分類値を削除するには、 **[!UICONTROL X]** 値の横にある

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
* [在庫フィードを使用した広告管理の自動化について](../inventory-feeds-about.md)
* [修飾子の管理](../modifiers-manage.md)
* [在庫データフィードファイルの管理](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
* [テンプレートを通じてフィードデータを伝達](../feed-data-propagate.md)
* [在庫フィードから広告ネットワークへのキャンペーンデータの投稿](../propagated-data-post.md)
