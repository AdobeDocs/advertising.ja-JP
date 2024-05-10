---
title: 在庫フィードのテキスト広告とレスポンシブ検索広告テンプレート設定
description: 在庫フィードのテキスト広告およびレスポンシブ検索広告テンプレートの設定を参照してください。
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# 在庫フィードのテキスト広告とレスポンシブ検索広告テンプレート設定


*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （削除アクションのみ）、 [!DNL Yandex] アカウントのみ*

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名を指定するために予約されているため、すべての属性フィールドでテキストとして使用することはできません。  `[ ] < > `
>* 対象： [!DNL Yandex templates]動的パラメーターを使用できます `{param1}` および `{param2}` URL 内のみで、広告の説明で動的な価格挿入を使用することはできません。

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

**[!UICONTROL Map Only]:** （任意）すべての新規広告グループをマッピングします（次の場合は使用できません： [!DNL Yandex]）、キーワードおよび広告（キャンペーンを作成するのではなく、既存のキャンペーンに対して行います。 このオプションを有効にする場合は、マッピング方法を選択します。

使用 [!UICONTROL Map Only] キャンペーンレベルでは、製品の分類に密接に結び付き、データフィードに簡単にマッピングできる既存のアカウント構造が必要です。

**[!UICONTROL Map Method]:** （条件 [!UICONTROL Map Only] がキャンペーンに対して有効になっている）新しい広告グループを作成する方法（では使用できません [!DNL Yandex]）、キーワードおよび広告は、既存のキャンペーンにマッピングされます。

* *[!UICONTROL Contains Anywhere]:* 指定した文字列を名前に含む既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Contains Exactly]:* 指定した文字列を名前に含む既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Exactly Matches]* （デフォルト）：同じ名前の既存のキャンペーンが存在する場合は、そのキャンペーンにデータを追加します。

一致するものが見つからない場合、キャンペーンのすべてのデータは無視されます。 複数のキャンペーンの一致が見つかった場合、キーワードと広告はそれらすべてにマッピングされます。

**[!UICONTROL Campaign Tracking Template]:** （最終/詳細 URL を持つアカウントのみ。オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、パラメーターに最終 URL を埋め込む、キャンペーンレベルのトラッキングテンプレート。 この値はアカウントレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレート（キーワードを最も詳細なレベルとして）はこの値を上書きします。

* キャンペーン設定に「」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキング[!UICONTROL EF Redirect]「」と「」に対して検査する値[!UICONTROL Auto Upload],&quot; レコードを保存すると、検索、ソーシャル、Commerceによって、リダイレクトおよびトラッキングコードが自動的に追加されます。

* 最終的な URL を埋め込むには：

   * （[!DNL Google Ads] および [!DNL Microsoft® Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（[!DNL Microsoft® Advertising] のみ） [[!DNL Microsoft® Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/56799/2) または（[!DNL Google Ads] のみ）「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] のパラメーター [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/6305348).

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーターを使用します `!{unescapedurl}` ランディングページの URL を指定します。

   * オプションで、次のような URL パラメーターと、キャンペーンに定義されたカスタムパラメーターをアンパサンド（&amp;）で区切って含めることができます `{lpurl}?matchtype={matchtype}&device={device}`.

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

**[!UICONTROL Networks]:** （中） [!DNL Google Ads] および [!DNL Yandex] （キャンペーン設定）広告を配置するネットワーク：

* *[!UICONTROL Search]:* スポンサー付き検索リストの入札を行う。

  （[!DNL Google Ads] キャンペーン）のリストに入札を含めます。 [!DNL Google Ads] パートナーを検索するには、の横にあるチェックボックスをオンにします。 **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* コンテンツ（ディスプレイ）ネットワークリスト上のプレースメントの入札を行う。 **注意：** テンプレートを使用してプレースメントを作成することはできません。 このオプションを選択する場合は、次のいずれかを使用して、各広告グループにプレースメントを作成し、各広告グループに対してターゲットにする表示ネットワーク上のページを指定します <!-- insert link --> バルクシートまたは <!-- insert links --> での広告グループとプレースメントの設定 [!UICONTROL Search] > [!UICONTROL Campaigns] ビュー。

**[!UICONTROL Languages]:** （[!DNL Google Ads] （ネットワークの検索と表示のみ）キャンペーン内の広告の 1 つ以上のターゲット言語。

[!DNL Google Ads] ユーザーの言語をユーザーの言語から決定します [!DNL Google] 検索クエリ、現在のページ、または最近表示されたページの言語設定または言語 [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** （最終/詳細 URL を持つアカウントのみ）広告グループレベルトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込みます。

キャンペーン設定に「」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキング[!UICONTROL EF Redirect]「」と「」に対して検査する値[!UICONTROL Auto Upload],&quot; レコードを保存すると、検索、ソーシャル、Commerceによって、リダイレクトおよびトラッキングコードが自動的に追加されます。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページの URL を指定するには：

* Yahoo！の場合 日本広告アカウント、パラメーターを使用 {lpurl}.

* Microsoft® Advertising およびGoogle Ads アカウントで使用できるパラメーターについては、を参照してください。 [[!DNL Microsoft® Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/56799) または「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] のパラメーター [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/6305348).

この値は、アカウントレベルおよびキャンペーンレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレート（キーワードを最も詳細なレベルとして）はこの値を上書きします。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** 指定した広告グループ（または次のキャンペーン： [!DNL Yandex] accounts）。静的テキスト、指定したファイル内の列、修飾子を任意に組み合わせて構成できます。 指定したフィードファイルがテンプレートによって伝播される際に、列名と修飾子は実際のデータに置き換えられます。

列名またはモディファイヤ グループを動的パラメータとして挿入するには、入力フィールドをクリックし、列リストまたは列の名前をクリックします [モディファイヤ名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) [ モディファイヤ ] リストで、次の操作を行います。 同じキーワードに対して複数のキーワードまたは複数の一致タイプを指定するには、別々の行に入力します。 キーワード一致タイプを指定するには、列名の前後に次の一致タイプ構文を使用します。

* の場合 [!DNL Google Ads], [!DNL Microsoft® Advertising]、および [!DNL Yahoo! Japan Ads] テンプレート：

   * 動的パラメーターの場合：部分一致= `[keyword]`、最初の語句の部分一致の修飾子。 [!UICONTROL Keyword] 列（+青いスエードの靴など） = `+[keyword]`、キーワード列の各用語の部分一致の修飾子（+blue +suede +shoes など） = `+[keyword]+`、フレーズ一致= `"[keyword]"`、完全一致= `[[keyword]]`

   * 静的キーワードの場合：部分一致= `keyword`、部分一致の修飾子= `+keyword`、または語句の一致= `"keyword"`

     完全一致および標準一致の構文で静的キーワードは角かっこ（`[]`）を使用する場合も、動的パラメーターと同様に使用できます。

* の場合 [!DNL Yandex] テンプレート：

   * 動的パラメーターの場合：次のような列名を挿入します `[keyword]`. 一致するタイプを指定するには、を使用します [[!DNL Yandex]固有の構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **注意：** 部分一致の用語については、次の構文を使用します。キーワード列の最初の用語に対する部分一致の修飾子（+青いスエード靴など） = `+[keyword]`、キーワード列の各用語の部分一致の修飾子（+blue +suede +shoes など） = `+[keyword]+`

   * 静的キーワードの場合：検索キーワードのみがサポートされます。 の使用 [[!DNL Yandex]固有の構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html) をキーワードに使用します。 角括弧（`[]`）を指定して、単語の順序がサポートされていないことを示します。

>[!NOTE]
>
>* キーワードパラメーターの前または後にコンマ区切りの値を括弧で囲むことで、「キーワード」フィールドに複数の修飾子値を手動で含めることができます（両方の場所にはできません）。 例： `(cheap, discount, affordable)[product]` は、各製品に対して 3 つの個別の広告を生成します。
>* 一致タイプを指定しない場合、デフォルトの一致タイプ「broad」が使用されます。
>* 負の一致はサポートされていません。
>* Googleの部分一致修飾子は、一部の言語のフレーズ一致と同じ一致動作を持つようになり、新しい部分一致修飾子のキーワードを作成できません。 を参照してください。 [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/10286719) を参照してください。

**[!UICONTROL Map Only]:** 広告グループ（またはキャンペーンに対する新しい広告を追加 [!DNL Yandex] accounts）に含まれるキーワードです。新しいキーワードを作成する代わりに指定したキーワードを検索します。 このオプションを有効にするには、チェックボックスをオンにします。 このオプションを有効にすると、キーワードが存在するので、指定したキーワード内の Param 1 および Param 2 変数は適用されません。

**[!UICONTROL Keyword Final URL]:** （最終/詳細 URL のあるアカウント。任意）広告をクリックした際に、広告ネットワークユーザーが取得するランディングページの URL。 表示 URL と同じドメインを含め、最終的な URL のパラメーターは、広告クリック後にランディングページ URL のパラメーターと一致する必要があります。 ランディングページのドメインまたはサブドメイン内のリダイレクトを含めることができますが、ランディングページのドメイン外のリダイレクトを含めることはできません。

を使用する場合 [!DNL Google Merchant Center] フィードし、この値を「」に含めます[!DNL Link]」列を選択して、その列をこのフィールドに挿入します。

>[!NOTE]
>
>* テンプレートを通じて伝播されたデータを POST する際にトラッキング URL を生成すると、アカウントのトラッキング設定に基づいて、トラッキングパラメーターがこの値に付加されます。
>* （[!DNL Google Ads] アカウント）並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

**[!UICONTROL Keyword Tracking Template]:** （最終/詳細 URL を持つアカウント。オプション）トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、パラメーターに最終 URL を埋め込みます。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、他のすべてのレベルの値を上書きします。

* キャンペーン設定に「」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキング[!UICONTROL EF Redirect]「」と「」に対して検査する値[!UICONTROL Auto Upload],&quot; レコードを保存すると、検索、ソーシャル、Commerceによって、リダイレクトおよびトラッキングコードが自動的に追加されます。

* オプションで、サードパーティのリダイレクトとトラッキングを入力できます。

* ランディングページの URL を指定するには：

   * （[!DNL Google Ads] および [!DNL Microsoft® Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（[!DNL Microsoft® Advertising] のみ） [[!DNL Microsoft® Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/56799) または（[!DNL Google Ads] のみ）「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] のパラメーター [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/6305348).

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーターを使用します `!{lpurl}` ランディングページの URL を指定します。

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] テンプレート\]:** （[!DNL Google Ads] （テンプレートのみ）指定したファイルの列で、 [!DNL Google Ads] `{param1}` または `{param2}` テンプレートから作成された任意の広告の広告コピーまたは表示 URL に含めることができる変数。 動的パラメーターを挿入するには、入力フィールドをクリックしてから、列リストで列名をクリックします。 フィードファイルがテンプレートを通じて伝播される際に、列名が実際のデータに置き換えられます。

どちらのパラメーターを使用する場合でも、そのパラメーターを新しいキーワードにのみ適用するか、テンプレートから作成されなかった既存のキーワードの値も更新するかを選択できます。

* **[!UICONTROL Do Not Apply to Existing Keywords]** （デフォルト）：テンプレートを使用して作成された新しいキーワードに対して、パラメーターの値を挿入するだけです。

* **[!UICONTROL Apply to Existing Keywords: Constant]:** フィード、検索、ソーシャル、Commerceから新しいキーワードを作成する以外にも、テンプレートを使用して作成されなかった広告グループ内の既存のすべてのキーワードのパラメーターの値も更新されます。 これらのキーワードすべてに使用する単一の数値を入力します。 テンプレートには少なくとも 1 つのキーワードが含まれている必要があります。

* **[!UICONTROL Apply to Existing Keywords: Min]:** フィードファイルにパラメーターの数値が含まれ、小数点が 1 つまで、コンマ、通貨記号、コードまたはその他の文字が使用されていない場合、フィード、検索、ソーシャルおよびCommerceから新しいキーワードを作成する以外に、テンプレートを使用して作成されなかった広告グループ内の既存のすべてのキーワードのパラメーターの値も更新されます。 フィードファイル内のパラメーターの最小値は、既存のすべてのキーワードに使用されます。 例えば、フィードファイルに [!UICONTROL Param1] 21500 と 22000 の値、さらに [!UICONTROL Param1] 既存のキーワードの値は 21500 に変更されます。 テンプレートには少なくとも 1 つのキーワードが含まれている必要があります。 **ヒント：** このオプションは、厳密なテーマの広告グループがある場合にのみ使用して、キーワードの値が同じであることを意味するようにします。

フィードファイルのデータフィールドは最大 25 文字で、次の非数値文字を含む数値データのみで構成される場合があります。

* （「[!UICONTROL Apply to Existing Keywords: Min]`` パラメータ）小数点 1 点まで入力してください。

* （「[!UICONTROL Apply to Existing Keywords: Min]`` パラメータ）:

   * 値の先頭または末尾に通貨記号またはコードを付けることができます。 例えば、£2.000,00 および 2000GBP は有効です。

   * 値には、コンマ（,）またはピリオド（.）を含めることができます 区切り記号として使用します（オプションでピリオド（.）も使用できます） 分数の場合はコンマ （,）を使用します。 例えば、1,000.00 と 2.000,10 は有効です。

   * 値の前にはパーセント記号（%）、プラス記号（+）、マイナス記号（–）を付けることができます。 例えば、20%、208+、-42.32 は有効です。

   * 2 つの数値をスラッシュで埋め込むことができます。 例えば、4/1 と 0.95/0.45 は有効です。

**[!UICONTROL Param 2]\[[!DNL Microsoft® Advertising] テンプレート\]:** （[!DNL Microsoft® Advertising] （テンプレートのみ）タイトル、テキスト、表示 URL または最終 URL に次の値が含まれる場合に、広告の置換値として使用する文字列 `{Param2}` 動的置換文字列。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、広告のタイトルには最大 25 文字まで含めることができます）。

**[!UICONTROL Param 3]:** （[!DNL Microsoft® Advertising] （テンプレートのみ）タイトル、テキスト、表示 URL または最終 URL に次の値が含まれる場合に、広告の置換値として使用する文字列 `{Param3}` 動的置換文字列。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、広告のタイトルには最大 25 文字まで含めることができます）。

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** 指定した一致タイプまたは広告タイプの各キーワードの初期入札。

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** （[!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンのみ）広告のタイプ： *[!UICONTROL Expanded Search Ads]* または *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** （オプション）すべての代替広告コピーフィールドに、元の広告コピーフィールドからのテキストを事前に入力します。

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）タイトル/ヘッドラインを含める必要がある広告の位置（例：「」）[!UICONTROL Pinned at position 1]``）に含まれます。 デフォルトはです [!UICONTROL Unpinned].

各職位に対して少なくとも 1 つのタイトルを使用できる必要があります。 複数のタイトルを同じ位置に固定した場合、最終的な広告には常に、指定した位置にこれらのタイトルの 1 つが含まれます。 位置 3 にピン留めされたタイトルは、広告では表示されない場合があります。

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** （レスポンシブ検索広告のみ）広告タイトル（ヘッドライン）。 各広告バリエーションには、少なくとも 3 つの広告タイトル、最大 15 の広告タイトルを含める必要があります。 広告ネットワークには、最大 3 つのヘッドラインを持つ広告が表示されます。 各タイトルの最大長は 30 文字で、ダイナミックテキスト（キーワードの値や広告カスタマイズ機能など）も含まれます。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** （既存のMicrosoft®Advertising 標準テキスト広告のみ。読み取り専用）広告のタイトルまたは最初の行。 Microsoft® Advertising では、標準テキスト広告の作成と編集を廃止しました。

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** （[!DNL Google Ads] および [!DNL Yahoo! Japan Ads] 拡張/拡張テキスト広告テンプレートのみ）広告のヘッドライン。 動的パラメーターを置き換えた後の各行の最大長は、30 文字または 15 個のダブルバイト文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** （[!DNL Google Ads] 展開されたテキスト広告テンプレートのみ（任意）広告の 3 つ目のヘッドライン。 動的パラメーターを置き換えた後の最大長は、30 文字または 15 文字の 2 バイト文字です。

**[!UICONTROL Title]:** （[!DNL Yandex] のみ）広告のタイトル、または最初の行。 最大 33 文字です。

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** （Microsoft®Advertising 拡張テキスト広告のみ）広告のヘッドライン。 動的パラメーターを置き換えた後の各行の最大長は、30 文字または 15 個のダブルバイト文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** （Microsoft®Advertising 拡張テキスト広告のみ）広告の本文。 動的パラメーターを置き換えた後の最大長は、80 文字または 40 文字の 2 バイト文字（中国語、日本語、韓国語など）です。

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** 広告の本文。

* （Google Ads expanded text ad templates）最大長（動的パラメーターが置き換えられた後）は 90 文字または 45 文字のダブルバイト文字です。

* （Yahoo! 日本の広告テンプレート）最大長（動的パラメーターが置き換えられた後）は、80 文字または 40 文字の全角文字です。

* （Yandex テンプレート）最大長（動的パラメータが置き換えられた後）は 75 文字であり、1 つの単語は 22 文字を超えることはできません。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）説明を含める必要がある広告の位置（「[!UICONTROL Pinned at position 1]``）に含まれます。 デフォルトはです [!UICONTROL Unpinned]. 各職位に対して少なくとも 1 つの説明を使用できる必要があります。

複数の説明を同じ位置にピン留めする場合、最終的な広告には常に、指定した位置にこれらの説明の 1 つが含まれます。 位置 2 にピン留めされた説明は、広告では表示されない場合があります。

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** （レスポンシブ検索広告のみ）広告の説明。 各広告バリエーションには、少なくとも 2 つ、最大 4 つの広告の説明を含める必要があります。 広告ネットワークには、最大 2 つの説明を持つ広告が表示されます。少なくとも 2 つ入力します。 各説明の最大長は 90 文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** （Googleで展開されたテキスト広告テンプレートのみ。オプション）広告の 2 行目。 動的パラメーターを置き換えた後の最大長は、90 文字または 45 文字の 2 バイト文字です。

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** （展開されたテキストとレスポンシブ検索広告のみ。オプション）ベース URL の後に連続して含める 1 つまたは 2 つの URL パス。 製品やサービスに関する詳細を広告で説明する必要があります。 例えば、 [!UICONTROL Display Path 1] 「Shoes」と [!UICONTROL Display Path 2] 「Outdoor」のベース URL www.example.comへの URL は、www.example.com/Shoes/Outdoorです。 各フィールドの最大長（動的パラメーターを置き換えた後）は 15 文字または 7 つの 2 バイト文字です。

レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイズ機能を挿入します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`（例：） `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}`（例：） `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** （既存 [!DNL Microsoft® Advertising] および [!DNL Yahoo! Japan Ads] 標準テキスト広告のみ。読み取り専用）広告に表示される URL。

[!DNL Microsoft® Advertising] および [!DNL Yahoo! Japan Ads] 標準テキスト広告の作成と編集を非推奨（廃止予定）にしました。

**[!UICONTROL Base URL]:** （宛先 URL を持つアカウントのみ）ユーザーが取得されるページ。 サードパーティのリダイレクトやトラッキングコードを含めることができます。 Adobe Advertisingコンバージョントラッキングサービスを使用する場合、およびキャンペーン設定に以下の使用が含まれる場合： [!UICONTROL EF Redirect] 広告レベルでトラッキングを追加すると、検索、ソーシャル、Commerceでは、独自のリダイレクトとトラッキングコードが広告に自動的に追加されます。

列名またはモディファイヤ グループを動的パラメータとして挿入するには、入力フィールドをクリックし、列リストまたは列の名前をクリックします [モディファイヤ名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) が含まれる [!UICONTROL Modifiers] リスト。

**[!UICONTROL Final URL]:** （最終/詳細 URL のあるアカウント）ユーザーが広告をクリックした際に取得されるランディングページの URL。 表示 URL と同じドメインを含め、最終的な URL のパラメーターは、広告クリック後にランディングページ URL のパラメーターと一致する必要があります。 ランディングページのドメインまたはサブドメイン内のリダイレクトを含めることができますが、ランディングページのドメイン外のリダイレクトを含めることはできません。

を使用する場合 [!DNL Google Merchant] フィードを中央に配置し、この値を「[!UICONTROL Link]」列を選択して、その列をこのフィールドに挿入します。

>[!NOTE]
>
>* テンプレートを通じて伝播されたデータを POST する際にトラッキング URL を生成すると、アカウントトラッキング設定に基づいてトラッキングパラメーターがこの値に付加されます。
>* （[!DNL Google Ads] アカウント）並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

**[!UICONTROL Tracking Template]:** （最終/詳細 URL を持つアカウント。オプション）トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、パラメーターに最終 URL を埋め込みます。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、他のすべてのレベルの値を上書きします。

キャンペーン設定に「」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキング[!UICONTROL EF Redirect]「」と「」に対して検査する値[!UICONTROL Auto Upload],&quot; レコードを保存すると、検索、ソーシャル、Commerceによって、リダイレクトおよびトラッキングコードが自動的に追加されます。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページの URL を指定するには：

* Yahoo！の場合 日本広告アカウント、パラメーターを使用 {lpurl}.

* Microsoft® Advertising およびGoogle Ads アカウントで使用できるパラメーターについては、を参照してください。 [[!DNL Microsoft® Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/56799) または「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] のパラメーター [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/6305348).

**\[ 元の広告フィールドの下の代替広告フィールド\]:** （オプション）広告の広告コピーの代替セット。元の広告コピーのいずれかの行が、伝播中に動的パラメーターがデータに入力された後に許可される最大長を超える場合に使用できます。

>[!NOTE]
>
>* 次の場合 [!UICONTROL Prefill] オプションを選択すると、代替フィールドに元のフィールドが事前入力され、必要に応じて編集できます。
>* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替ヘッドラインまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせる際には、代替の広告コピーが理にかなっていることを確認してください。
>* 元の広告コピーが検索エンジンの長さの要件を満たしている場合、代替広告コピーは破棄されます。

**\[ コンポーネント\] [!UICONTROL Ad Label Classifications] > \[ ラベルの分類と値\]:** （任意）テンプレートを使用して作成または編集する広告バリエーションに割り当てる、最大 5 つの既存のラベル分類の値。 ラベル分類を割り当てるキャンペーンコンポーネントごとに、次の操作を行います。

1. チェックボックスをクリックします。

1. 広告バリエーションテンプレートのラベル分類値を設定します。

   * コンポーネントに割り当てるラベル分類および値ごとに、次の操作を行います。

      1. クリック **[!UICONTROL Add Label Classification]**.

      1. 既存のラベル分類を選択し、既存の値を選択するか、新しい値を入力します。

         各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

         ラベル分類値の動的パラメータとして列名を挿入するには、入力フィールド （2 番目のフィールド）をクリックし、列リストで列名をクリックします。

         キャンペーンコンポーネントごとに、分類ごとに 1 つの値のみを含めることができます。 例えば、キャンペーンのカラーは「赤」とすることができますが、カラーは「赤」や「カラー」は「青」にはできません。

         * 既存のラベル分類値を変更するには、新しい値を選択または入力します。

         * 既存のラベル分類値を削除するには、をクリックします **[!UICONTROL X]** 値の横。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [在庫フィードを使用した広告管理の自動化について](../inventory-feeds-about.md)
>* [修飾子の管理](../modifiers-manage.md)
>* [在庫データフィードファイルの管理](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [テンプレートを使用したフィードデータの伝播](../feed-data-propagate.md)
>* [在庫フィードから広告ネットワークへのキャンペーンデータの投稿](../propagated-data-post.md)
