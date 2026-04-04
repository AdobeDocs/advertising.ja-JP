---
title: 在庫フィードのテキスト広告とレスポンシブ検索広告のテンプレート設定
description: 在庫フィードには、テキスト広告とレスポンシブ検索広告テンプレートの設定を参照します。
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/ECmtczHqzO5JyR--JWgKQYReKLTohbrJlvhbBGUNOLY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: b2ff290c2cee19c8acdc8001433189ea9bdbf83f
workflow-type: tm+mt
source-wordcount: 3352
ht-degree: 0%

---

# 在庫フィードのテキスト広告とレスポンシブ検索広告のテンプレート設定

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除操作のみ）、[!DNL Yandex] アカウントのみ*

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名を指定するために予約されているため、すべての属性フィールドのテキストとして使用できません：`[ ] < > `
>* [!DNL Yandex templates]では、動的パラメーター`{param1}`と`{param2}`はURLでのみ使用でき、広告説明では動的な価格挿入を使用できません。

## \[すべてのタブの上\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[左パネル\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** （オプション）すべての新しい広告グループ（[!DNL Yandex]では利用できません）、キーワード、および広告を、キャンペーンを作成するのではなく、既存のキャンペーンにマッピングします。 このオプションを有効にする場合は、マッピング方法を選択します。

キャンペーンレベルで[!UICONTROL Map Only]を使用するには、製品分類と密接に関連し、データフィードに簡単にマッピングできる既存のアカウント構造が必要です。

**[!UICONTROL Map Method]:** （[!UICONTROL Map Only]がキャンペーンに対して有効になっている場合）新しい広告グループ （[!DNL Yandex]では使用できない）、キーワード、広告を既存のキャンペーンにマッピングする方法：

* *[!UICONTROL Contains Anywhere]:*&#x200B;指定された文字列を含む名前の既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Contains Exactly]:*&#x200B;指定された文字列を含む名前の既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

* *[!UICONTROL Exactly Matches]* （既定値）：同じ名前の既存のキャンペーンが存在する場合、そのキャンペーンにデータを追加します。

一致するフィールドが見つからない場合、キャンペーンのすべてのデータは無視されます。 複数のキャンペーンの一致が見つかった場合、キーワードと広告はそれらすべてにマッピングされます。

**[!UICONTROL Campaign Tracking Template]:** （最終/詳細URLを持つアカウントのみ。オプション）すべてのランディングドメイン外リダイレクトとトラッキングパラメーターを指定し、最終的なURLをパラメーターに埋め込む、キャンペーンレベルのトラッキングテンプレート。 この値はアカウントレベルの設定よりも優先されますが、より詳細なレベル（キーワードが最も詳細なレベル）でテンプレートを追跡すると、この値よりも優先されます。

* キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceはリダイレクトコードとトラッキングコードを自動的に追加します。

* 最終的なURLを埋め込むには：

   * （[!DNL Google Ads]および[!DNL Microsoft Advertising]のみ）トラッキングテンプレートの最終的なURLを示すパラメーターのリストについては、[!DNL Microsoft Advertising] ドキュメント [[!DNL Microsoft Advertising] の「使用可能な](https://help.ads.microsoft.com/#apex/3/en/56799/2) パラメーター」の節の「トラッキングテンプレートのみ」パラメーター（[!DNL Google Ads]のみ） [!DNL ValueTrack] ドキュメント [[!DNL Google Ads] または（](https://support.google.com/google-ads/answer/6305348)のみ）を参照してください。

   * （[!DNL Yahoo! Japan Ads]のみ） パラメーター`!{unescapedurl}`を使用して、ランディングページ URLを示します。

   * 必要に応じて、URL パラメーターと、キャンペーン用に定義された任意のカスタムパラメーターを、アンパサンド（&amp;）で区切って含めることができます（`{lpurl}?matchtype={matchtype}&device={device}`）。

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

**[!UICONTROL Networks]:** （[!DNL Google Ads]および[!DNL Yandex] キャンペーン設定）広告を配置するネットワーク：

* *[!UICONTROL Search]:* スポンサー付き検索リストの入札を行います。

  （[!DNL Google Ads] キャンペーン） [!DNL Google Ads]件の検索パートナーのリストに入札を含めるには、**[!UICONTROL Search partners]**&#x200B;の横にあるチェックボックスを選択します。

* *[!UICONTROL Content]:* コンテンツ （ディスプレイ） ネットワーク リスト上のプレースメントに入札を配置します。 **メモ：** テンプレートを使用してプレースメントを作成することはできません。 このオプションを選択すると、各広告グループのプレースメントを作成し、[!UICONTROL Search] > [!UICONTROL Campaigns] ビューで、バルクシートまたは広告グループとプレースメント設定を使用して、各広告グループにターゲットとするディスプレイネットワーク上のページを指定します。

<!-- insert links above -->

**[!UICONTROL Languages]:** （[!DNL Google Ads]検索および表示ネットワークのみ）キャンペーン内の広告の1つ以上のターゲット言語。

[!DNL Google Ads]は、ユーザーの[!DNL Google]言語設定または検索クエリの言語、現在のページ、または[!DNL Google Display Network]で最近閲覧したページから、ユーザーの言語を決定します。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:** （[!DNL Google Ads]および[!DNL Microsoft Advertising] キャンペーンのみ。欧州連合（EU）内のオーディエンスをターゲットとするキャンペーンに適用されます）このキャンペーンに、EU規則2024/90に基づいて欧州連合で配信される広告の要件に従った政治的広告が含まれているかどうか：*[!UICONTROL Yes]*&#x200B;または&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** （最終/詳細URLを持つアカウントのみ）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的なURLをパラメーターに埋め込む、広告グループレベルのトラッキングテンプレート。

キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceはリダイレクトコードとトラッキングコードを自動的に追加します。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページ URLを指定するには：

* Yahoo! 日本の広告アカウントです。パラメーター{lpurl}を使用してください。

* [!DNL Microsoft Advertising]および[!DNL Google Ads] アカウントで使用できるパラメーターについては、[[!DNL Microsoft Advertising]  ドキュメント &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799)の「使用可能な[!DNL ValueTrack] パラメーター」の節の[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/6305348)または「トラッキングテンプレートのみ」パラメーターを参照してください。

この値は、アカウントレベルとキャンペーンレベルの設定よりも優先されますが、より詳細なレベル（キーワードが最も詳細なレベル）でテンプレートを追跡すると、この値よりも優先されます。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

指定された広告グループ （または&#x200B;**[!UICONTROL Keywords]アカウントのキャンペーン）の**:[!DNL Yandex] キーワード。静的テキスト、指定されたファイル内の列、および修飾子の任意の組み合わせで構成できます。 指定したフィードファイルがテンプレートを通じて伝播されると、列名と修飾子は実際のデータに置き換えられます。

列名または修飾子グループを動的パラメーターとして挿入するには、入力フィールドをクリックし、列リストの列名または修飾子リストの[修飾子名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)をクリックします。 同じキーワードに複数のキーワードまたは複数の一致タイプを指定するには、それらを別々の行に入力します。 キーワード一致タイプを指定するには、列名の周りに次の一致タイプ構文を使用します。

* [!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]のテンプレートの場合：

   * 動的パラメーターの場合：`[keyword]`列の最初の用語のBroad Match = [!UICONTROL Keyword]、Broad Match Modifier （+blue suede shoesなど） = `+[keyword]`、キーワード列の各用語のBroad Match Modifier （+blue +suede +shoesなど） = `+[keyword]+`、フレーズ Match = `"[keyword]"`、完全一致= `[[keyword]]`

   * 静的キーワードの場合：Broad Match = `keyword`、Broad Match Modifier = `+keyword`、またはPhrase Match = `"keyword"`

     完全一致と標準一致の構文を使用して静的キーワードを入力することはできません。動的パラメーターと同様に、括弧（`[]`）で囲まれています。

* [!DNL Yandex] テンプレートの場合：

   * 動的パラメーターの場合：`[keyword]`などの列名を挿入します。 一致するタイプを示すには、[[!DNL Yandex]固有の構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html)を使用します。 **注意：**&#x200B;幅広い一致の用語については、次の構文を使用します。キーワード列の最初の用語のBroad Match Modifier （+blue suede shoesなど） = `+[keyword]`、キーワード列の各用語のBroad Match Modifier （+blue +suede +shoesなど） = `+[keyword]+`

   * 静的キーワードの場合：検索キーワードのみがサポートされます。 キーワードには[[!DNL Yandex]固有の構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html)を使用します。 単語の順序を示す角かっこ（`[]`）はサポートされていません。

>[!NOTE]
>
>* キーワードパラメーターの前または後の括弧内にコンマ区切りの値を囲むことで、「キーワード」フィールドに複数の修飾子値を手動で含めることができます（両方の場所にはありません）。 例えば、`(cheap, discount, affordable)[product]`は、各製品に対して3つの個別の広告を生成します。
>* 一致タイプを指定しない場合、デフォルトの一致タイプ「broad」が使用されます。
>* 負の一致はサポートされていません。
>* Googleの部分一致モディファイアは、一部の言語でフレーズ一致と同じマッチング動作を持つようになり、新しい部分一致モディファイアのキーワードを作成できません。 詳しくは、[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/10286719)を参照してください。

**[!UICONTROL Map Only]:**&#x200B;新しいキーワードを作成するのではなく、指定されたキーワードが見つかった広告グループ （または[!DNL Yandex] アカウントのキャンペーン）に新しい広告を追加します。 このオプションを有効にするには、チェックボックスをオンにします。 このオプションを有効にすると、キーワードが存在するため、指定したキーワードのパラメーター1変数とパラメーター2変数は適用されません。

**[!UICONTROL Keyword Final URL]:** （最終/詳細URLを持つアカウント。オプション）広告ネットワークユーザーが広告をクリックしたときに取得されるランディングページ URL。 表示URLと同じドメインを含める必要があり、最終的なURLのパラメーターは、広告のクリック後にランディングページ URLのパラメーターと一致する必要があります。 ランディングページドメインまたはサブドメイン内にリダイレクトを含めることができますが、ランディングページドメイン外にリダイレクトを含めることはできません。

[!DNL Google Merchant Center] フィードを使用し、この値を「[!DNL Link]」列に含める場合は、その列をこのフィールドに挿入します。

>[!NOTE]
>
>* テンプレートを通じて伝播されたデータを投稿するときにトラッキング URLを生成する場合、トラッキングパラメーターは、アカウントのトラッキング設定に基づいてこの値に追加されます。
>* （[!DNL Google Ads] アカウント）並列追跡を有効にするソースからのクリックに代わらないマクロの使用を避けます。 広告主がマクロを使用する必要がある場合は、Adobe アカウントチームがカスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。

**[!UICONTROL Keyword Tracking Template]:** （最終/詳細URLを持つアカウント。オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終URLをパラメーターに埋め込むトラッキングテンプレート。 最も詳細なレベル（キーワードが最も詳細）のトラッキングテンプレートは、他のすべてのレベルの値を上書きします。

* キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceはリダイレクトコードとトラッキングコードを自動的に追加します。

* オプションで、サードパーティのリダイレクトとトラッキングを入力できます。

* ランディングページ URLを指定するには：

   * （[!DNL Google Ads]および[!DNL Microsoft Advertising]のみ）トラッキングテンプレートの最終的なURLを示すパラメーターのリストについては、[!DNL Microsoft Advertising] ドキュメント [[!DNL Microsoft Advertising] の「使用可能な](https://help.ads.microsoft.com/#apex/3/en/56799) パラメーター」の節の「トラッキングテンプレートのみ」パラメーター（[!DNL Google Ads]のみ） [!DNL ValueTrack] ドキュメント [[!DNL Google Ads] または（](https://support.google.com/google-ads/answer/6305348)のみ）を参照してください。

   * （[!DNL Yahoo! Japan Ads]のみ） パラメーター`!{lpurl}`を使用して、ランディングページ URLを示します。

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\]:** （[!DNL Google Ads] templatesのみ）指定されたファイルの列で、[!DNL Google Ads] `{param1}`または`{param2}`変数を表します。この変数は、テンプレートから作成された任意の広告の広告コピーまたは表示URLに含めることができます。 動的パラメーターを挿入するには、入力フィールドのをクリックし、列リストの列名をクリックします。 フィードファイルがテンプレートを通じて伝播されると、列名は実際のデータに置き換えられます。

いずれかのパラメーターを使用する場合は、パラメーターを新しいキーワードにのみ適用するか、テンプレートから作成されていない既存のキーワードの値も更新するオプションがあります。

* **[!UICONTROL Do Not Apply to Existing Keywords]** （既定値）: テンプレートを使用して作成された新しいキーワードのパラメーターの値を単純に挿入します。

* **[!UICONTROL Apply to Existing Keywords: Constant]:** フィードから新しいキーワードを作成するだけでなく、Search, Social, &amp; Commerceでは、テンプレートを使用して作成されなかった広告グループ内のすべての既存のキーワードのパラメーターの値も更新されます。 すべてのキーワードに使用される1つの数値を入力します。 テンプレートには少なくとも1つのキーワードを含める必要があります。

* **[!UICONTROL Apply to Existing Keywords: Min]:** フィードから新しいキーワードを作成することに加えて、Search, Social, &amp; Commerceでは、フィード ファイルに最大10進数ポイント、通貨記号またはコード、またはその他の任意の文字を含まないパラメーターの数値が含まれている限り、テンプレートを使用して作成されなかった広告グループ内のすべての既存キーワードのパラメーターの値も更新されます。 フィードファイル内のパラメーターの最小値は、既存のすべてのキーワードに使用されます。 例えば、フィードファイルの値が[!UICONTROL Param1]個の21500と22000の場合、既存のキーワードの[!UICONTROL Param1]個の値は21500に変更されます。 テンプレートには少なくとも1つのキーワードを含める必要があります。 **ヒント：**&#x200B;このオプションは、キーワードが同じ値を持つことが理にかなるように、厳密にテーマ設定された広告グループがある場合にのみ使用してください。

フィードファイルのデータフィールドは最大25文字で、次の非数値文字の数値データのみで構成される場合があります。

* （「[!UICONTROL Apply to Existing Keywords: Min]」パラメーターを使用する場合）小数点以下1点までです。

* （「[!UICONTROL Apply to Existing Keywords: Min]」パラメーターを使用しない場合）:

   * 値の前に通貨記号またはコードを追加できます。 例えば、£2.000,00と2000GBPは有効です。

   * 値には、区切り記号としてコンマ（,）またはピリオド（。）を含めることができ、オプションのピリオド（。）または分数の値にはコンマ（,）を含めることができます。 例えば、1,000.00と2.000,10は有効です。

   * 値の前にパーセント記号（%）、プラス記号（+）、マイナス記号（ – ）を付けることもできます。 例えば、20%、208+、-42.32は有効です。

   * 2つの数字をスラッシュで埋め込むことができます。 例えば、4/1と0.95/0.45は有効です。

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] templates\]:** （[!DNL Microsoft Advertising] テンプレートのみ）タイトル、テキスト、表示URL、または最終的なURLに`{Param2}`動的な置換文字列が含まれている場合に、広告の置換値として使用する文字列。 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、広告タイトルには最大25文字が含まれる場合があります）。

**[!UICONTROL Param 3]:** （[!DNL Microsoft Advertising] テンプレートのみ）タイトル、テキスト、表示URL、または最終URLに`{Param3}`動的な置換文字列が含まれている場合に、広告の置換値として使用する文字列。 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、広告タイトルには最大25文字が含まれる場合があります）。

**[!UICONTROL Initial Bid (&lt;Match Type or Ad Type>)]:**&#x200B;指定された一致タイプまたは広告タイプの各キーワードの初期入札。

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** （[!DNL Google Ads]および[!DNL Microsoft Advertising] キャンペーンのみ）広告の種類：*[!UICONTROL Expanded Search Ads]*&#x200B;または&#x200B;*[!UICONTROL Responsive Search Ads]*。

**[!UICONTROL Prefill]:** （オプション）すべての代替の広告コピーフィールドに、元の広告コピーフィールドのテキストが事前入力されます。

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）タイトルまたは見出しを含める必要がある広告位置（「[!UICONTROL Pinned at position 1]」など）。 デフォルトは[!UICONTROL Unpinned]です。

各位置に少なくとも1つのタイトルが用意されている必要があります。 複数のタイトルを同じ位置にピン留めすると、最終的な広告には、常に指定された位置にそれらのタイトルのいずれかが含まれます。 3番目にピン留めされたタイトルは、広告で表示されない場合があります。

**[!UICONTROL Headline 1]**、**[!UICONTROL Headline 2]**、**[!UICONTROL Headline 3]:** （レスポンシブ検索広告のみ）広告タイトル（見出し）。 各広告バリエーションには、少なくとも3つ、最大15個の広告タイトルを含める必要があります。 広告ネットワークには、最大3つの見出しの広告が表示されます。 各タイトルの最大長は、動的テキスト（キーワードや広告カスタマイザーの値など）を含めて30文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** （既存のMicrosoft Advertising標準テキスト広告のみ。読み取り専用）広告のタイトルまたは1行目。 Microsoft Advertisingでは、標準テキスト広告の作成および編集が非推奨になりました。

**[!UICONTROL Headline 1]**、**[!UICONTROL Headline 2]:** （[!DNL Google Ads]および[!DNL Yahoo! Japan Ads]件の拡張/拡張テキスト広告テンプレートのみ）広告の見出し。 各行の最大長（動的パラメーターを置き換えた後）は、30文字または15文字の2 バイト文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** （[!DNL Google Ads]件の拡張テキスト広告テンプレートのみ。オプション）広告の3番目の見出し。 最大長（動的パラメーターを置き換えた後）は、30文字または2 バイト文字15文字です。

**[!UICONTROL Title]:** （[!DNL Yandex]のみ）広告のタイトルまたは最初の行。 最大は33文字です。

**[!UICONTROL Title Part 1]**、**[!UICONTROL Title Part 2]:** （Microsoft Advertisingの拡張テキスト広告のみ）広告の見出し。 各行の最大長（動的パラメーターを置き換えた後）は、30文字または15文字の2 バイト文字です。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** （Microsoft Advertising拡張テキスト広告のみ）広告の本文。 最大長（動的パラメーターを置き換えた後）は、80文字または2 バイト文字（中国語、日本語、韓国語など） 40文字です。

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:**&#x200B;広告の本文。

* （Google Ads expanded text ad templates）最大長（動的パラメーターを置き換えた後）は、90文字または45文字の2 バイトです。

* （Yahoo! 日本広告テンプレート）最大長（動的パラメーターを置き換えた後）は、80文字または40文字の2 バイトです。

* （Yandex テンプレート）最大長（動的なパラメーターを置き換えた後）は75文字で、1つの単語を22文字を超えることはできません。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** （レスポンシブ検索広告のみ）説明を含める必要がある広告位置（「[!UICONTROL Pinned at position 1]」など）。 デフォルトは[!UICONTROL Unpinned]です。 各位置に少なくとも1つの説明を用意する必要があります。

複数の説明を同じ位置に固定する場合、最終広告には常に、指定した位置にそれらの説明のいずれかが含まれます。 位置2にピン留めされた説明は、広告で表示されない場合があります。

**[!UICONTROL Description 1]**、**[!UICONTROL Description 2]:** （レスポンシブ検索広告のみ）広告の説明。 各広告バリエーションには、少なくとも2つ、最大4つの広告説明を含める必要があります。 広告ネットワークには、最大2つの説明を含む広告が表示されます。少なくとも2つ入力してください。 各説明の最大長は90文字で、動的テキスト（キーワードや広告カスタマイザーの値など）を含みます。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** （Googleで拡張されたテキストとテンプレートのみ。オプション）広告の2行目。 最大長（動的パラメーターを置き換えた後）は、90文字または45文字の2 バイト文字です。

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**、**[!UICONTROL Display Path 2]:** （拡張テキストおよびレスポンシブ検索広告のみ。オプション）基本URLの後に連続して含める1つまたは2つのURL パス。 広告で商品やサービスをより詳しく説明する必要があります。 例えば、「Shoes」の[!UICONTROL Display Path 1]と「Outdoor」の[!UICONTROL Display Path 2]をベース URL www.example.comに追加すると、URLはwww.example.com/Shoes/Outdoorになります。 各フィールドの最大長（動的パラメーターが置き換えられた後）は、15文字または7文字の2 バイト文字です。

レスポンシブ検索広告の場合は、次の形式を使用して広告カスタマイザーを挿入します。フィード ファイルに有効な値が含まれていない場合に挿入するオプション値は`Default text`です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}` （例：`{CUSTOMIZER.Discount:10%}`）

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}` （例：`{CUSTOMIZER.Discount:10%}`）

**[!UICONTROL Display URL]:** （既存の[!DNL Microsoft Advertising]および[!DNL Yahoo! Japan Ads]標準テキスト広告のみ。読み取り専用）広告に表示されるURL。

標準テキスト広告の作成と編集は、[!DNL Microsoft Advertising]および[!DNL Yahoo! Japan Ads]によって非推奨（廃止予定）となりました。

**[!UICONTROL Base URL]:** （宛先URLを持つアカウントのみ）ユーザーが取得されるページ。 これには、サードパーティのリダイレクトとトラッキングコードを含めることができます。 Adobe Advertising コンバージョントラッキングサービスを使用しており、キャンペーン設定に[!UICONTROL EF Redirect]を使用して広告レベルでトラッキングを追加する場合、Search, Social, &amp; Commerceは自動的に独自のリダイレクトとトラッキングコードを広告に追加します。

列名または修飾子グループを動的パラメーターとして挿入するには、入力フィールドをクリックし、列リストの列名または[&#x200B; リストの](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)修飾子名[!UICONTROL Modifiers]をクリックします。

**[!UICONTROL Final URL]:** （最終/詳細URLを持つアカウント） ユーザーが広告をクリックしたときに取得されるランディングページ URL。 表示URLと同じドメインを含める必要があり、最終的なURLのパラメーターは、広告のクリック後にランディングページ URLのパラメーターと一致する必要があります。 ランディングページドメインまたはサブドメイン内にリダイレクトを含めることができますが、ランディングページドメイン外にリダイレクトを含めることはできません。

[!DNL Google Merchant] Center フィードを使用し、この値を&quot;[!UICONTROL Link]&quot;列に含める場合は、その列をこのフィールドに挿入します。

>[!NOTE]
>
>* テンプレートを通じて伝播されたデータを投稿する際にトラッキング URLを生成すると、アカウントトラッキング設定に基づいて、トラッキングパラメーターがこの値に追加されます。
>* （[!DNL Google Ads] アカウント）並列追跡を有効にするソースからのクリックに代わらないマクロの使用を避けます。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームは、カスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。

**[!UICONTROL Tracking Template]:** （最終/詳細URLを持つアカウント。オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終URLをパラメーターに埋め込むトラッキングテンプレート。 最も詳細なレベル（キーワードが最も詳細）のトラッキングテンプレートは、他のすべてのレベルの値を上書きします。

キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceはリダイレクトコードとトラッキングコードを自動的に追加します。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 ランディングページ URLを指定するには：

* Yahoo! 日本の広告アカウントです。パラメーター{lpurl}を使用してください。

* [!DNL Microsoft Advertising]および[!DNL Google Ads] アカウントで使用できるパラメーターについては、[[!DNL Microsoft Advertising]  ドキュメント &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799)の「使用可能な[!DNL ValueTrack] パラメーター」の節の[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/6305348)または「トラッキングテンプレートのみ」パラメーターを参照してください。

**\[元の広告フィールドの下の代替広告フィールド\]:** （オプション）広告の代替の広告コピーのセット。この広告コピーの代替セットは、元の広告コピー内の行のいずれかが、配信中に動的パラメーターにデータを入力した後に許可される最大長を超えた場合に使用できます。

>[!NOTE]
>
>* 「[!UICONTROL Prefill]」オプションが選択されている場合、代替フィールドには元のフィールドが事前入力され、必要に応じて編集できます。
>* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元の見出しまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替の見出しまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせると、代替の広告コピーが意味のあるものであることを確認してください。
>* 元の広告コピーが検索エンジンの長さ要件を満たしている場合、代替の広告コピーは破棄されます。

**\[ コンポーネント\] [!UICONTROL Ad Label Classifications] > \[ ラベル分類と値\]:** （オプション）既存のラベル分類を5つまで指定して、テンプレートを使用して作成または編集された広告バリエーションに割り当てることができます。 ラベル分類を割り当てる各キャンペーンコンポーネントについて：

1. チェックボックスをクリックします。

1. 広告バリエーション テンプレートのラベル分類値を設定します。

   * コンポーネントに割り当てる各ラベル分類と値について、次の操作を行います。

      1. **[!UICONTROL Add Label Classification]**&#x200B;をクリックします。

      1. 既存のラベル分類を選択し、既存の値を選択するか、新しい値を入力します。

         各値の最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

         ラベル分類値の動的パラメーターとして列名を挿入するには、入力フィールド（2番目のフィールド）をクリックし、列リストの列名をクリックします。

         キャンペーンコンポーネントごとに、分類ごとに1つの値のみを含めることができます。 例えば、キャンペーンにColor=Redを指定できますが、Color=RedとColor=Blueは指定できません。

         * 既存のラベル分類値を変更するには、新しい値を選択または入力します。

         * 既存のラベル分類値を削除するには、値の横にある&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。

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
>* [&#x200B; テンプレートを通じてフィード データを伝達](../feed-data-propagate.md)
>* [在庫フィードのキャンペーンデータを広告ネットワークに投稿](../propagated-data-post.md)
