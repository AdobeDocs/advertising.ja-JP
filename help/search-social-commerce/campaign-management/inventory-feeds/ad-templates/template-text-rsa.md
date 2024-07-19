---
title: 在庫フィードのテキスト広告とレスポンシブ検索広告テンプレート設定
description: 在庫フィードのテキスト広告およびレスポンシブ検索広告テンプレートの設定を参照してください。
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# 在庫フィードのテキスト広告とレスポンシブ検索広告テンプレート設定


*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名を指定するために予約されているので、すべての属性フィールドでテキストとして使用することはできません。`[ ] < > `
>* [!DNL Yandex templates] では、動的パラメーター `{param1}` と `{param2}` は URL でのみ使用でき、広告の説明では動的な価格挿入を使用できません。

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

**[!UICONTROL Map Only]:** （任意）すべての新規広告グループ（[!DNL Yandex] では使用できません）、キーワードおよび広告を、キャンペーンを作成するのではなく、既存のキャンペーンにマッピングします。 このオプションを有効にする場合は、マッピング方法を選択します。

キャンペーンレベルで [!UICONTROL Map Only] を使用するには、製品の分類に密接に結び付き、データフィードに簡単にマッピングできる既存のアカウント構造が必要です。

**[!UICONTROL Map Method]:** （キャンペーンで [!UICONTROL Map Only] が有効になっている場合）新しい広告グループ（[!DNL Yandex] では利用できません）、キーワードおよび広告を既存のキャンペーンにマッピングする方法：

* *[!UICONTROL Contains Anywhere]:* 指定した文字列を名前に含む既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Contains Exactly]:* 指定した文字列を名前に含む既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Exactly Matches]* （デフォルト）：同じ名前の既存のキャンペーンが存在する場合は、そのキャンペーンにデータを追加します。

一致するものが見つからない場合、キャンペーンのすべてのデータは無視されます。 複数のキャンペーンの一致が見つかった場合、キーワードと広告はそれらすべてにマッピングされます。

**[!UICONTROL Campaign Tracking Template]:** （最終/詳細 URL を持つアカウントのみ。任意）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込む、キャンペーンレベルのトラッキングテンプレート。 この値はアカウントレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレート（キーワードを最も詳細なレベルとして）はこの値を上書きします。

* キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、レコードを保存すると、検索、ソーシャルおよびCommerceにリダイレクトおよびトラッキングコードが自動的に追加されます。

* 最終的な URL を埋め込むには：

   * （[!DNL Google Ads] および [!DNL Microsoft Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799/2) の「使用可能なトラッキングパラメーター」の節の（[!DNL Microsoft Advertising] のみ） [[!DNL Microsoft Advertising]  ドキュメント [[!DNL Google Ads]  または（[!DNL Google Ads] のみ） [!DNL ValueTrack] 「トラッキングテンプレートのみ」パラメーターを参照してください ](https://support.google.com/google-ads/answer/6305348)

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーター `!{unescapedurl}` を使用して、ランディングページの URL を指定します。

   * オプションで、URL パラメーターと、キャンペーンに定義されたカスタムパラメーターをアンパサンド（&amp;）で区切ったもの（`{lpurl}?matchtype={matchtype}&device={device}` など）を含めることができます。

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

**[!UICONTROL Networks]:** （[!DNL Google Ads] および [!DNL Yandex] キャンペーン設定）広告を配置するネットワーク：

* *[!UICONTROL Search]:* スポンサー付き検索リストの入札を行う。

  （[!DNL Google Ads] キャンペーン）検索パートナーのリストに入札を含め [!DNL Google Ads] には、**[!UICONTROL Search partners]** の横にあるチェックボックスを選択します。

* *[!UICONTROL Content]:* コンテンツ（ディスプレイ）ネットワークリストにプレースメントの入札を配置します。 **メモ：** テンプレートを使用してプレースメントを作成することはできません。 このオプションを選択する場合は、各広告グループにプレースメントを作成し、バルクシートまたは <!-- insert links --> の広告グループとプレースメント設定を使用して、表示ネットワーク上で各広告グループのターゲット <!-- insert link --> するページを [!UICONTROL Search] > [!UICONTROL Campaigns] ビューで指定します。

**[!UICONTROL Languages]:** （[!DNL Google Ads] search and display networks only） キャンペーンの広告の 1 つ以上のターゲット言語。

ユーザーの言語 [!DNL Google Ads]、ユーザーの [!DNL Google] 言語設定または検索クエリの言語、現在のページ、[!DNL Google Display Network] ージ上で最近閲覧されたページなどから特定されます。

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

キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、レコードを保存すると、検索、ソーシャルおよびCommerceにリダイレクトおよびトラッキングコードが自動的に追加されます。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページの URL を指定するには：

* Yahoo！の場合 日本の広告アカウント、パラメーター {lpurl} を使用します。

* Microsoft AdvertisingおよびGoogle Ads アカウントで使用できるパラメーターについては、[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799) または「ドキュメント」の「使用できる [!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ [[!DNL Google Ads]  パラメーターを参照してください ](https://support.google.com/google-ads/answer/6305348)。

この値は、アカウントレベルおよびキャンペーンレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレート（キーワードを最も詳細なレベルとして）はこの値を上書きします。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** 指定した広告グループ（または [!DNL Yandex] アカウントのキャンペーン）のキーワード。静的テキスト、指定したファイル内の列、修飾子を任意に組み合わせて構成できます。 指定したフィードファイルがテンプレートによって伝播される際に、列名と修飾子は実際のデータに置き換えられます。

列名またはモディファイヤ グループを動的パラメータとして挿入するには、入力フィールド内をクリックし、列リスト内の列名または [ モディファイヤ ] リスト内の [ モディファイヤ名 ](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) をクリックします。 同じキーワードに対して複数のキーワードまたは複数の一致タイプを指定するには、別々の行に入力します。 キーワード一致タイプを指定するには、列名の前後に次の一致タイプ構文を使用します。

* [!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] のテンプレートの場合：

   * 動的パラメーターの場合：部分一致= `[keyword]`、[!UICONTROL Keyword] 列の最初の語句の部分一致モディファイヤ（+blue suede shoes など） = `+[keyword]`、キーワード列の各語句の部分一致モディファイヤ（+blue +suede +shoes など） = `+[keyword]+`、語句の一致= `"[keyword]"`、完全一致= `[[keyword]]`

   * 静的キーワードの場合：部分一致= `keyword`、部分一致の修飾子= `+keyword`、またはフレーズ一致= `"keyword"`

     静的キーワードは、動的パラメーターと同様に角括弧（`[]`）で囲まれているため、完全一致および標準一致の構文を使用してここに入力することはできません。

* [!DNL Yandex] テンプレートの場合：

   * 動的パラメーターの場合：列名（`[keyword]` など）を挿入します。 一致タイプを示すには、[[!DNL Yandex] 固有の構文 ](https://yandex.com/support/direct/keywords/symbols-and-operators.html) を使用します。 **注：** 部分一致用語の場合は、次の構文を使用します。キーワード列の最初の用語に対する部分一致修飾子（+blue suede shoes など） = `+[keyword]`、キーワード列の各用語に対する部分一致修飾子（+blue +suede +shoes など） = `+[keyword]+`

   * 静的キーワードの場合：検索キーワードのみがサポートされます。 キーワードには [[!DNL Yandex] 固有 ](https://yandex.com/support/direct/keywords/symbols-and-operators.html) 構文を使用します。 単語の順序を示す角括弧（`[]`）はサポートされていません。

>[!NOTE]
>
>* キーワードパラメーターの前または後にコンマ区切りの値を括弧で囲むことで、「キーワード」フィールドに複数の修飾子値を手動で含めることができます（両方の場所にはできません）。 例えば、`(cheap, discount, affordable)[product]` は製品ごとに 3 つの異なる広告を生成します。
>* 一致タイプを指定しない場合、デフォルトの一致タイプ「broad」が使用されます。
>* 負の一致はサポートされていません。
>* Googleの部分一致修飾子は、一部の言語のフレーズ一致と同じ一致動作を持つようになり、新しい部分一致修飾子のキーワードを作成できません。 詳しくは、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/10286719) を参照してください。

**[!UICONTROL Map Only]:** 新しいキーワードを作成するのではなく、指定したキーワードが含まれる広告グループ（または [!DNL Yandex] アカウントのキャンペーン）に新しい広告を追加します。 このオプションを有効にするには、チェックボックスをオンにします。 このオプションを有効にすると、キーワードが存在するので、指定したキーワード内の Param 1 および Param 2 変数は適用されません。

**[!UICONTROL Keyword Final URL]:** （最終/詳細 URL のあるアカウント。任意）広告をクリックした際に、広告ネットワークユーザーが取得するランディングページの URL。 表示 URL と同じドメインを含め、最終的な URL のパラメーターは、広告クリック後にランディングページ URL のパラメーターと一致する必要があります。 ランディングページのドメインまたはサブドメイン内のリダイレクトを含めることができますが、ランディングページのドメイン外のリダイレクトを含めることはできません。

[!DNL Google Merchant Center] フィードを使用してこの値を「[!DNL Link]」列に含める場合は、その列をこのフィールドに挿入します。

>[!NOTE]
>
>* テンプレートを通じて伝播されたデータを POST する際にトラッキング URL を生成すると、アカウントのトラッキング設定に基づいて、トラッキングパラメーターがこの値に付加されます。
>* （[!DNL Google Ads] アカウント）並列トラッキングを有効にするソースからのクリックに置き換えられないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

**[!UICONTROL Keyword Tracking Template]:** （最終/詳細 URL を持つアカウント。任意）トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、パラメーターに最終 URL を埋め込みます。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、他のすべてのレベルの値を上書きします。

* キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、レコードを保存すると、検索、ソーシャルおよびCommerceにリダイレクトおよびトラッキングコードが自動的に追加されます。

* オプションで、サードパーティのリダイレクトとトラッキングを入力できます。

* ランディングページの URL を指定するには：

   * （[!DNL Google Ads] および [!DNL Microsoft Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799) の「使用可能なトラッキングパラメーター」の節の（[!DNL Microsoft Advertising] のみ） [[!DNL Microsoft Advertising]  ドキュメント [[!DNL Google Ads]  または（[!DNL Google Ads] のみ） [!DNL ValueTrack] 「トラッキングテンプレートのみ」パラメーターを参照してください ](https://support.google.com/google-ads/answer/6305348)

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーター `!{lpurl}` を使用して、ランディングページの URL を指定します。

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** （[!DNL Google Ads] templates のみ） [!DNL Google Ads] `{param1}` または `{param2}` 変数を表す、指定されたファイル内の列。これは、テンプレートから作成された任意の広告の広告コピーまたは表示 URL に含めることができます。 動的パラメーターを挿入するには、入力フィールドをクリックしてから、列リストで列名をクリックします。 フィードファイルがテンプレートを通じて伝播される際に、列名が実際のデータに置き換えられます。

どちらのパラメーターを使用する場合でも、そのパラメーターを新しいキーワードにのみ適用するか、テンプレートから作成されなかった既存のキーワードの値も更新するかを選択できます。

* **[!UICONTROL Do Not Apply to Existing Keywords]** （デフォルト）：テンプレートを使用して作成された新しいキーワードに対して、パラメーターの値を挿入するだけです。

* **[!UICONTROL Apply to Existing Keywords: Constant]:** フィード、検索、ソーシャル、Commerceから新しいキーワードを作成する以外に、テンプレートを使用して作成されなかった広告グループ内の既存のすべてのキーワードのパラメーターの値も更新されます。 これらのキーワードすべてに使用する単一の数値を入力します。 テンプレートには少なくとも 1 つのキーワードが含まれている必要があります。

* **[!UICONTROL Apply to Existing Keywords: Min]:** フィードファイルにパラメーターの数値が含まれ、小数点が 1 つまで、コンマ、通貨記号、コードまたはその他の文字が含まれていない場合、フィード、検索、ソーシャルおよびCommerceから新しいキーワードを作成できるだけでなく、テンプレートを使用して作成されなかった広告グループ内の既存のすべてのキーワードのパラメーター値も更新されます。 フィードファイル内のパラメーターの最小値は、既存のすべてのキーワードに使用されます。 例えば、フィードファイルの [!UICONTROL Param1] 値が 21500 と 22000 の場合、既存のキーワードの [!UICONTROL Param1] 値は 21500 に変更されます。 テンプレートには少なくとも 1 つのキーワードが含まれている必要があります。 **ヒント：** このオプションは、厳密なテーマの広告グループがある場合にのみ使用して、キーワードが同じ値を持つことは理にかなっています。

フィードファイルのデータフィールドは最大 25 文字で、次の非数値文字を含む数値データのみで構成される場合があります。

* （「[!UICONTROL Apply to Existing Keywords: Min]」パラメーターを使用する場合）小数点 1 つまで。

* （「[!UICONTROL Apply to Existing Keywords: Min]」パラメーターを使用しない場合）:

   * 値の先頭または末尾に通貨記号またはコードを付けることができます。 例えば、£2.000,00 および 2000GBP は有効です。

   * 値には、コンマ（,）またはピリオド（.）を含めることができます 区切り記号として使用します（オプションでピリオド（.）も使用できます） 分数の場合はコンマ （,）を使用します。 例えば、1,000.00 と 2.000,10 は有効です。

   * 値の前にはパーセント記号（%）、プラス記号（+）、マイナス記号（–）を付けることができます。 例えば、20%、208+、-42.32 は有効です。

   * 2 つの数値をスラッシュで埋め込むことができます。 例えば、4/1 と 0.95/0.45 は有効です。

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] templates\]:** （[!DNL Microsoft Advertising] templates のみ） タイトル、テキスト、表示 URL、または最終 URL に `{Param2}` の動的置換文字列が含まれる場合に、広告の置換値として使用する文字列。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、広告のタイトルには最大 25 文字まで含めることができます）。

**[!UICONTROL Param 3]:** （[!DNL Microsoft Advertising] テンプレートのみ） タイトル、テキスト、表示 URL または最終 URL に `{Param3}` の動的置換文字列が含まれる場合に、広告の置換値として使用する文字列。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、広告のタイトルには最大 25 文字まで含めることができます）。

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** 指定した一致タイプまたは広告タイプの各キーワードの初期入札。

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** （[!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンのみ）広告のタイプ：*[!UICONTROL Expanded Search Ads]* または *[!UICONTROL Responsive Search Ads]*。

**[!UICONTROL Prefill]:** （オプション）すべての代替広告コピーフィールドに、元の広告コピーフィールドからのテキストを事前に入力します。

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）タイトル/ヘッドラインを含める必要がある広告の位置（「[!UICONTROL Pinned at position 1]」など）。 デフォルトは [!UICONTROL Unpinned] です。

各職位に対して少なくとも 1 つのタイトルを使用できる必要があります。 複数のタイトルを同じ位置に固定した場合、最終的な広告には常に、指定した位置にこれらのタイトルの 1 つが含まれます。 位置 3 にピン留めされたタイトルは、広告では表示されない場合があります。

**[!UICONTROL Headline 1]**、**[!UICONTROL Headline 2]**、**[!UICONTROL Headline 3]:** （レスポンシブ検索広告のみ）広告タイトル（ヘッドライン）。 各広告バリエーションには、少なくとも 3 つの広告タイトル、最大 15 の広告タイトルを含める必要があります。 広告ネットワークには、最大 3 つのヘッドラインを持つ広告が表示されます。 各タイトルの最大長は 30 文字で、ダイナミックテキスト（キーワードの値や広告カスタマイズ機能など）も含まれます。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** （既存のMicrosoft Advertising標準テキスト広告のみ。読み取り専用）広告のタイトルまたは最初の行。 Microsoft Advertisingでは、標準テキスト広告の作成と編集が非推奨（廃止予定）になりました。

**[!UICONTROL Headline 1]**、**[!UICONTROL Headline 2]:** （[!DNL Google Ads] および [!DNL Yahoo! Japan Ads] の拡張/拡張テキスト広告テンプレートのみ）広告のヘッドライン。 動的パラメーターを置き換えた後の各行の最大長は、30 文字または 15 個のダブルバイト文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** （拡張テキスト広告テンプレートの [!DNL Google Ads] み、オプション）広告の 3 つ目のヘッドライン。 動的パラメーターを置き換えた後の最大長は、30 文字または 15 文字の 2 バイト文字です。

**[!UICONTROL Title]:** （[!DNL Yandex] のみ）広告のタイトル、または最初の行。 最大 33 文字です。

**[!UICONTROL Title Part 1]**、**[!UICONTROL Title Part 2]:** （Microsoft Advertising拡張テキスト広告のみ）広告の見出し。 動的パラメーターを置き換えた後の各行の最大長は、30 文字または 15 個のダブルバイト文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** （Microsoft Advertising拡張テキスト広告のみ）広告の本文。 動的パラメーターを置き換えた後の最大長は、80 文字または 40 文字の 2 バイト文字（中国語、日本語、韓国語など）です。

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** 広告の本文。

* （Google Ads expanded text ad templates）最大長（動的パラメーターが置き換えられた後）は 90 文字または 45 文字のダブルバイト文字です。

* （Yahoo! 日本の広告テンプレート）最大長（動的パラメーターが置き換えられた後）は、80 文字または 40 文字の全角文字です。

* （Yandex テンプレート）最大長（動的パラメータが置き換えられた後）は 75 文字であり、1 つの単語は 22 文字を超えることはできません。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）説明を含める必要がある広告の位置（「[!UICONTROL Pinned at position 1]」など）。 デフォルトは [!UICONTROL Unpinned] です。 各職位に対して少なくとも 1 つの説明を使用できる必要があります。

複数の説明を同じ位置にピン留めする場合、最終的な広告には常に、指定した位置にこれらの説明の 1 つが含まれます。 位置 2 にピン留めされた説明は、広告では表示されない場合があります。

**[!UICONTROL Description 1]**、**[!UICONTROL Description 2]:** （レスポンシブ検索広告のみ）広告の説明。 各広告バリエーションには、少なくとも 2 つ、最大 4 つの広告の説明を含める必要があります。 広告ネットワークには、最大 2 つの説明を持つ広告が表示されます。少なくとも 2 つ入力します。 各説明の最大長は 90 文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** （Googleで拡張されたテキスト広告テンプレートのみ。オプション）広告の 2 行目。 動的パラメーターを置き換えた後の最大長は、90 文字または 45 文字の 2 バイト文字です。

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**、**[!UICONTROL Display Path 2]:** （展開されたテキストとレスポンシブ検索広告のみ。オプション）ベース URL の後に連続して含める 1 つまたは 2 つの URL パス。 製品やサービスに関する詳細を広告で説明する必要があります。 例えば、ベース URL www.example.comに「Shoes」の [!UICONTROL Display Path 1] と「Outdoor」の [!UICONTROL Display Path 2] を追加した場合、URL はwww.example.com/Shoes/Outdoorになります。 各フィールドの最大長（動的パラメーターを置き換えた後）は 15 文字または 7 つの 2 バイト文字です。

レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイザーを挿入します。`Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]:`{CUSTOMIZER.AdCustomizerName:Default text}` （`{CUSTOMIZER.Discount:10%}` など）

* [!DNL Microsoft Advertising]:`{CUSTOMIZER.Attribute name:Default text}` （`{CUSTOMIZER.Discount:10%}` など）

**[!UICONTROL Display URL]:** （既存の [!DNL Microsoft Advertising] および [!DNL Yahoo! Japan Ads] 標準テキスト広告のみ。読み取り専用）広告に表示される URL。

[!DNL Microsoft Advertising] および [!DNL Yahoo! Japan Ads] は、標準テキスト広告の作成と編集を非推奨（廃止予定）としました。

**[!UICONTROL Base URL]:** （宛先 URL を持つアカウントのみ）ユーザーが取得されるページ。 サードパーティのリダイレクトやトラッキングコードを含めることができます。 Adobe Advertisingコンバージョントラッキングサービスを使用し、キャンペーン設定に [!UICONTROL EF Redirect] の使用と広告レベルでのトラッキングの追加が含まれる場合、検索、ソーシャル、Commerceでは独自のリダイレクトとトラッキングコードが広告に自動的に追加されます。

列名または修飾グループを動的パラメータとして挿入するには、入力フィールド内をクリックし、列リスト内の列名または [!UICONTROL Modifiers] 名リスト内の [ 修飾子名 ](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) をクリックします。

**[!UICONTROL Final URL]:** （最終/高度な URL を持つアカウント）ユーザーが広告をクリックした際に取得されるランディングページの URL。 表示 URL と同じドメインを含め、最終的な URL のパラメーターは、広告クリック後にランディングページ URL のパラメーターと一致する必要があります。 ランディングページのドメインまたはサブドメイン内のリダイレクトを含めることができますが、ランディングページのドメイン外のリダイレクトを含めることはできません。

[!DNL Google Merchant] Center フィードを使用してこの値を「[!UICONTROL Link]」列に含める場合は、その列をこのフィールドに挿入します。

>[!NOTE]
>
>* テンプレートを通じて伝播されたデータを POST する際にトラッキング URL を生成すると、アカウントトラッキング設定に基づいてトラッキングパラメーターがこの値に付加されます。
>* （[!DNL Google Ads] アカウント）並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

**[!UICONTROL Tracking Template]:** （最終/詳細 URL を持つアカウント。任意）トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、パラメーターに最終 URL を埋め込みます。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、他のすべてのレベルの値を上書きします。

キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、レコードを保存すると、検索、ソーシャルおよびCommerceにリダイレクトおよびトラッキングコードが自動的に追加されます。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページの URL を指定するには：

* Yahoo！の場合 日本の広告アカウント、パラメーター {lpurl} を使用します。

* Microsoft AdvertisingおよびGoogle Ads アカウントで使用できるパラメーターについては、[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799) または「ドキュメント」の「使用できる [!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ [[!DNL Google Ads]  パラメーターを参照してください ](https://support.google.com/google-ads/answer/6305348)。

**\[ 元の広告フィールドの下の代替広告フィールド\]:** （オプション）広告の代替の広告コピーセット。元の広告コピー内のいずれかの行が、伝播中に動的パラメーターがデータに入力された際に許可される最大長を超える場合に使用できます。

>[!NOTE]
>
>* 「[!UICONTROL Prefill]」オプションを選択した場合、代替フィールドには元のフィールドが事前入力され、必要に応じて編集できます。
>* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替ヘッドラインまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせる際には、代替の広告コピーが理にかなっていることを確認してください。
>* 元の広告コピーが検索エンジンの長さの要件を満たしている場合、代替広告コピーは破棄されます。

**\[Component\] [!UICONTROL Ad Label Classifications] > \[Label Classification and Value\]:** （オプション）テンプレートを使用して作成または編集する広告バリエーションに割り当てる、既存のラベル分類の値（最大 5 つ）。 ラベル分類を割り当てるキャンペーンコンポーネントごとに、次の操作を行います。

1. チェックボックスをクリックします。

1. 広告バリエーションテンプレートのラベル分類値を設定します。

   * コンポーネントに割り当てるラベル分類および値ごとに、次の操作を行います。

      1. 「**[!UICONTROL Add Label Classification]**」をクリックします。

      1. 既存のラベル分類を選択し、既存の値を選択するか、新しい値を入力します。

         各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

         ラベル分類値の動的パラメータとして列名を挿入するには、入力フィールド （2 番目のフィールド）をクリックし、列リストで列名をクリックします。

         キャンペーンコンポーネントごとに、分類ごとに 1 つの値のみを含めることができます。 例えば、キャンペーンのカラーは「赤」とすることができますが、カラーは「赤」や「カラー」は「青」にはできません。

         * 既存のラベル分類値を変更するには、新しい値を選択または入力します。

         * 既存のラベル分類値を削除するには、値の横の **[!UICONTROL X]** をクリックします。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [ 在庫フィードを使用した広告管理の自動化について ](../inventory-feeds-about.md)
>* [ 修飾子の管理 ](../modifiers-manage.md)
>* [ 在庫データフィードファイルの管理 ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [ テンプレートを使用したフィードデータの伝播 ](../feed-data-propagate.md)
>* [ 在庫フィードから広告ネットワークへのキャンペーンデータの投稿 ](../propagated-data-post.md)
