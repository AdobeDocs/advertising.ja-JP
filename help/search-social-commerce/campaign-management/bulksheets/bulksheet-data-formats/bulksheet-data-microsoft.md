---
title: アカウントに必須のバルクシート デ  [!DNL Microsoft Advertising]  タ
description: アカウントのバルクシートで、必須のヘッダーフィールドとデータフィ  [!DNL Microsoft Advertising]  ルドを参照します。
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# 付録 – [!DNL Microsoft Advertising] アカウントに必須のバルクシートデータ

キャンペーンデータ [!DNL Microsoft Advertising] 一括で作成および更新するには、[!DNL Microsoft Advertising] アカウント用に特別にフォーマットされた検索、ソーシャル、Commerceのバルクシートファイルを使用できます。 a） [ 既存のアカウント用のバルクシートファイルを必要なファイル形式で生成する ](../bulksheet-download.md) または b）手動で作成できます（サポートされるファイル形式について詳しくは、「[ サポートされるバルクシートファイル形式 ](bulksheet-file-formats.md)」を参照してください）。

各バルクシートには、ヘッダーフィールドと、[ 実行する特定の操作 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) に必要な対応するデータフィールド（広告の作成など）を含める必要があります。 フィールドが不要な場合は、ヘッダー行とデータ行から省略できます。 バルクシートファイルをアップロードすると、すべてのカスタム列が削除されます。

次の表は、使用可能なすべてのデータフィールドと、個々のエンティティ（キャンペーンやキーワードなど）のデータを追加、編集または削除するために必要なフィールドを示す追加のテーブルです。

## すべての使用可能なデータフィールド {#bulksheet-fields-all-microsoft}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、[ 各アカウントコンポーネントの作成、編集、削除に必要なフィールド ](#bulksheet-fields-per-component-microsoft) を参照してください。

| フィールド | 説明 |
|----|----|
| [!UICONTROL Platform] | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 最大長は 128 文字です。 |
| [!UICONTROL Campaign Budget] | 通貨記号および句読点を含む、または含まない、毎日または毎月のキャンペーン予算。 0.05 未満にすることはできません。 |
| [!UICONTROL Channel Type] | キャンペーンがターゲットとするチャネルのタイプ（<i>[!UICONTROL Audience]</i>、<i>[!UICONTROL DynamicSearchAds]</i>、<i>[!UICONTROL Search]</i>、<i>[!UICONTROL Shopping]</i>）。 |
| [!UICONTROL Delivery Method] | （日次予算のあるキャンペーンのみ）キャンペーンの広告を毎日表示する間隔：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを 1 日に配分します。</li><li><i>[!UICONTROL Accelerated]:</i> 予算に達するまでできるだけ頻繁に広告を表示します。 その結果、広告がその日の後半に表示されない場合があります。</li></ul> |
| [!UICONTROL Campaign Priority] | （ショッピングキャンペーンのみ）複数のキャンペーンが同じ製品を広告する場合に使用されるキャンペーンの優先度。<i>[!UICONTROL Low]</i> （新しいキャンペーンのデフォルト）、<i>[!UICONTROL Medium]</i> または <i>[!UICONTROL High]</i> です。<br><br> 同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークはまずキャンペーンの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を判断します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。 |
| [!UICONTROL Merchant ID] | （マーチャントフィードにリンクされたショッピングキャンペーンおよびオーディエンスキャンペーンのみ）商品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。 |
| [!UICONTROL Sales Country] | （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）キャンペーンの商品が販売される国。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。 |
| [!UICONTROL Product Scope Filter] | （ショッピングネットワークを使用したキャンペーンのみ）キャンペーンに対して商品広告を作成できる、マーチャントアカウント内の商品。 dimension=attribute のフォーマットを使用して、製品をフィルタする製品次元と属性の組合せを最大 7 つ入力できます。 複数のフィルターを「>>」区切り文字で区切ります。 使用可能な製品ディメンションのリストについては、「[ ショッピングキャンペーン製品フィルター ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)」を参照してください。<br><br>: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL DSA Domain Name] | （タイプ a のキャンペーン）「<i>[!UICONTROL DynamicSearchAds]</i>」または b）「<i>[!UICONTROL Search]</i>」（[!DNL ExperimentId] 要素が設定されていない場合）。動的検索広告のターゲットとする web サイトのドメイン名。 最大長は 2,048 文字です。 ドメイン名に `www` が含まれている場合は、切り取られ、使用されません。<br><br> 既存のキャンペーンの場合、ドメインは編集できませんが、他のプロパティを更新するにはドメインを含める必要があります。 |
| [!UICONTROL DSA Domain Language] | （タイプ a）「<i>[!UICONTROL DynamicSearchAds]</i>」または b）「<i>[!UICONTROL Search]</i>」（[!DNL ExperimentId] 要素が設定されていない場合）。動的検索広告のターゲットとする web サイトページの言語。 サポートされているドメイン言語は、[!UICONTROL Dutch]、[!UICONTROL English]、[!UICONTROL French]、[!UICONTROL German]、[!UICONTROL Italian]、[!UICONTROL Spanish] および [!UICONTROL Swedish] です。<br><br> 既存のキャンペーンの場合、言語は編集できませんが、他のプロパティを更新するには言語を含める必要があります。 |
| [!UICONTROL Ad Group Name] | 広告グループを識別する一意の名前。 最大長は 128 文字です。 末尾の空白文字は保存されません（例：「広告グループ 1」は「広告グループ 1」として保存されます）。 |
| [!UICONTROL Ad Group Type] | （検索ネットワーク上のキャンペーン、既存の広告グループは読み取り専用）広告グループタイプ：<i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ）、<i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）、<i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告および既存の拡張テキスト広告のみ）。 一部のキャンペーンタイプには、複数の広告グループタイプを含めることができます。 |
| [!UICONTROL Keyword] | （検索ネットワーク上のキャンペーンのみ）キーワード文字列。 最大長は 50 文字です。<br><br><b> 注：</b><ul><li>広告グループレベルまたはキャンペーンレベルでキーワードを除外するには、[!UICONTROL Match Type] を `Negative` に設定します。 行に広告グループ名が含まれている場合、その広告グループ用のキーワードは除外されます。 行に広告グループ名が含まれていない場合、キーワードはキャンペーン全体で除外されます。</li><li>[!DNL Microsoft Advertising] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード ID で新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。</li></ul> |
| プレースメント | 非推奨 |
| [!UICONTROL Audience] | 検索広告（RLSA）用のリマーケティングリストは、キャンペーンまたは広告グループのターゲットオーディエンスを表します。 |
| [!UICONTROL Target Type] | （RLSA ターゲットのみ）ターゲット・タイプ：<i>[!UICONTROL Inclusion]</i> または <i>[!UICONTROL Exclusion]</i>。 |
| [!UICONTROL Auto Target Expression] | 広告グループの動的検索ターゲット。 すべてのターゲットに「[!UICONTROL All Web Pages]」を使用します。<br><br> 最大 3 つの動的検索条件をターゲットにするには、形式 `<category>=<target>` を使用します。&lt;category> には、以下のいずれかのカテゴリを含めることができます。 個々のカテゴリの複数のターゲットを「`[blank space] and [blank space]`」で結合し、複数のカテゴリを「`[blank space] and [blank space]`」で結合します。<br><ul><li><i> カテゴリ：</i> 特定のGoogle コンテンツカテゴリを持つインデックス付きページの動的検索広告を表示します。</li><li><i>URL:</i> 特定の URL を持つインデックス付きページの動的検索広告を表示します。この値は、URL 内の任意の場所に含めることができます。</li><li><i> ページタイトル：</i> ページタイトルに特定のテキストを含むインデックス付きページの動的検索広告を表示します。</li><li><i> ページコンテンツ：</i> 特定のコンテンツを含むインデックス付きページの動的検索広告を表示します。</li></ul>例：url=shoes.example.com and page title=footwear<br> 例：すべての web ページ |
| [!UICONTROL Location] | キャンペーンまたは広告グループの広告を配置する地理的な場所。値では大文字と小文字が区別されません。 キャンペーンまたは広告グループに値を入力しない場合、すべての場所がターゲットになります。 特定の場所をターゲットにするには、[!DNL Microsoft Advertising] の場所コード形式を使用して場所を入力します。 場所のリストをダウンロードするには、[!DNL Microsoft Advertising] advertising アカウントの資格情報を使用して [!DNL Microsoft Advertising] 開発者ポータルにログインします。 <b> 注意：</b> 場所を除外するには、場所コードの前にマイナス記号（`-`）を付けます（`-United States` など）。 |
| [!UICONTROL Location Type] | 場所のタイプ（市区町村、国、メトロ地域、郵便番号、都道府県など）。 場所のリストをダウンロードするには、[!DNL Microsoft Advertising] advertising アカウントの資格情報を使用して [!DNL Microsoft Advertising] 開発者ポータルにログインします。 |
| [!UICONTROL Match Type] | （検索ネットワーク上のキャンペーンのみ）キーワード照合オプション。 これには、動的検索ターゲットまたは製品グループのキーワード照合オプションが含まれる場合があります。 値には、<i>[!UICONTROL Broad]</i> （新しいキーワードのデフォルト）、<i>[!UICONTROL Exact]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Content]</i> （広告グループがコンテンツネットワークをターゲットとしている場合にキーワードに対して自動的に設定される）、<i>[!UICONTROL Negative]</i> （コンテンツネットワーク上のキーワードを除外する）、<i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索のターゲットのデフォルト）、<i>[!UICONTROL Product Group]</i> （新しい製品グループのデフォルト）、<i>[!UICONTROL Negative Product Group]</i> （製品グループを除外する）があります。  複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード ID の値が必要です。<br><br> 部分一致の修飾子の場合は、「部分一致」を選択し、必要なキーワード内の単語の前に `+` を挿入します（「赤」と「靴」の両方を必要とする場合は「`+red +shoes`」など）。<br><br>[!DNL Microsoft Advertising] キーワードの一致タイプを変更しても、既存のキーワードは削除されません。 |
| [!UICONTROL Max CPC] | （検索ネットワーク上のキャンペーン）最大クリック単価（CPC）。キーワード、製品グループ、動的検索目標に基づいて、金銭記号と句読点の有無にかかわらず広告クリックに対して支払う最高額です。  最適化されたポートフォリオ内の既存のキーワードおよび製品グループのレコードの場合、更新は 1 日のみ有効であり、次の最適化サイクルで上書きされます。 <b> メモ：</b> 負のキーワードに対して入札を設定することはできません。 |
| [!UICONTROL Max Content CPC] | （2017 年にコンテンツネットワークが廃止される前に作成された CPC キャンペーンのみ読み取り専用） 1 回あたりの最大コンテンツコスト（CPC）。金銭的な記号や句読点の有無にかかわらず、ディスプレイネットワークサイトから広告クリックに支払う最高額です。 |
| [!UICONTROL Audience Target Method] | （オーディエンス広告グループ）次のようにします。<ul><li><i>[!UICONTROL Target and Bid]:</i> ターゲットオーディエンスに関連付けられているユーザーで、その広告グループの他のターゲットも満たしているユーザーにのみ広告を表示します。</li><li><i>[!UICONTROL Bid Only]:</i> 他の広告グループレベルのターゲットを満たす限り、ターゲットオーディエンスに関連付けられていないユーザーにも広告を表示する場合。</li></ul> ただし、特定のオーディエンスに対してより高い入札を設定すると、それらのオーディエンスに広告が表示される可能性が高くなります。 |
| [!UICONTROL Parent Product Groupings] | 親商品グループの階層。<br><br> 例：`All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | 製品グループ（「brand=acme」や「すべての製品」など）。<br><br><b> 注：</b><ul><li>指定した商品グループが親商品グループ階層に存在しない場合、検索、ソーシャル、Commerceでは、必要な階層の部分が作成されます。</li><li>デフォルトの入札額を広告グループのデフォルトの入札額に設定して買い物キャンペーンで広告グループを作成すると、検索、ソーシャル、Commerceでは常に自動的に「[!UICONTROL All Products]」グループが作成されます。 検索、ソーシャル、Commerceでは、商品グループ階層の各レベルに広告グループのデフォルト入札を使用して、自動的に「[!UICONTROL Everything Else]」グループが作成されます。 これらのデフォルトグループを明示的に作成して、除外するか、入札を変更することができます。</li><li>各広告グループには、「[!UICONTROL All Products]」と 7 つのその他の層を含む、最大 8 つの製品グループ層を含めることができます。</li></ul> |
| [!UICONTROL Partition Type] | 製品グループのパーティション タイプ：<i>[!UICONTROL subdivision]</i> （子製品グループがある場合）または <i>[!UICONTROL unit]</i> （子製品グループがない場合）。 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | （拡張されたテキスト広告、マルチメディア広告、レスポンシブ広告およびレスポンシブ検索広告のみ）広告のヘッドライン。 各広告タイトルフィールドの最大長は、任意の動的テキストを含む 30 文字または 15 個の 2 バイト文字です（キーワードの値、`{Param2}` と `{Param3}` の動的置換変数、広告カスタマイズ機能など）。<br><br> レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイザーを挿入します。「デフォルトのテキスト」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。`{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br> 展開されたテキスト広告の場合、広告タイトルと広告タイトル 2 は必須で、[!UICONTROL Ad Title 3] はオプションです。 2022 年 8 月 [!DNL Microsoft Advertising] 廃止された拡張テキスト広告は、レポートおよび削除のみができるようになりました。<br><br> マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告の場合、[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]、[!UICONTROL Ad Title 3] は必須で、その他の広告タイトルフィールドはすべてオプションです。<br><br> 必須以外のフィールドに既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。<br><br> 拡張テキスト広告を除くすべての広告タイプで、広告コピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | （レスポンシブ検索広告のみ。オプション）対応する広告タイトルをピン留めする位置：`[null]` （値なし。これは、広告タイトルをすべての位置に対して適格にします）、1、2、または 3。 例えば、[!UICONTROL Ad Title Position] の値が 1 の場合、[!UICONTROL Ad Title] は位置 1 にのみ表示されます。 デフォルトでは、すべての広告タイトルが null です（値がありません）。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。<br><br><b> メモ：</b> 複数の広告タイトルを同じ位置にピン留めできます。 広告ネットワークは、位置にピン留めされた広告タイトルの 1 つを使用する。 位置 3 にピン留めされたタイトルは、広告では表示されない場合があります。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | （テキスト広告、動的検索広告、マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告、拡張キャンペーンレベルのサイトリンクのみ）広告またはサイトリンクの本文。<br><br> サイトリンクの場合、オプションで [!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] の両方を使用して、広告ネットワークがリンクテキストの下に表示する追加のテキストを含めます。 各説明フィールドには、最大 35 個のシングルバイト文字または 17 個のダブルバイト文字を含めることができます。<br><br> 広告の場合、各説明フィールドの最大長は 90 文字または 45 文字の 2 バイト文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。<br><br> レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイズ機能を挿入します。「デフォルトのテキスト」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。`{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br> テキスト広告と動的検索広告の場合、説明行 1 は必須で、「[!UICONTROL Description Line 2]」はオプションです。<br><br> マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告の場合は、[!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] が必要で、[!UICONTROL Description Line 3] と [!UICONTROL Description Line 4] はオプションです。<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。<br><br><b> 注：</b><ul><li>（標準テキスト広告）タイトルとテキストの組み合わせは、少なくとも 3 単語である必要があります。</li><li>（拡張テキスト広告）このフィールドには、オプションで {Param2} および {Param3} の動的置換変数を含めることができます。 この場合、広告テキストの最大長は 300 個の 1 バイト文字または 150 個の 2 バイト文字になります。 2022 年 8 月 [!DNL Microsoft Advertising] 廃止された拡張テキスト広告は、レポートおよび削除のみができるようになりました。</li><li>（動的検索広告）動的置換テキストは使用できません。</li><li>拡張テキスト広告を除くすべての広告タイプで、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索広告のみ。オプション）対応する説明をピン留めする位置：`[null]` （値なし。これは、説明をすべての位置に対して適格にします）、1、2、または 3。 例えば、[!UICONTROL Description 1 Position] の値が 1 の場合、説明 1 は位置 1 にのみ表示されます。 デフォルトでは、説明は位置にピン留めされません。<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。<br><br><b> 注：</b> 複数の説明を同じ位置にピン留めできます。 広告ネットワークは、位置にピン留めされた説明の 1 つを使用します。 位置 2 にピン留めされた説明は、広告では表示されない場合があります。 |
| [!UICONTROL Business Name] | （マルチメディア広告のみ）最大 25 文字のビジネス名。 |
| [!UICONTROL Promotion Line] | （商品リスト広告のみ）検索結果に商品リストに含まれる一意のプロモーションライン（「今すぐ送料無料」など）。 最大長は 45 文字です。<br><br> プロモーションラインは、広告がページ上のどこに表示されるかに応じて、広告に対して異なる場所（広告の下など）に表示される場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれる URL。<br><br> 拡張された動的検索広告の場合、広告ネットワークは、web サイトドメインから動的にこの値を生成するので、値を入力する必要はありません。<br><br> 拡張テキスト広告とレスポンシブ検索広告の場合は、値を入力する必要はありません。 最終的な URL のドメインから、表示 URL が自動的に抽出されます。 オプションで、「パス 1」および「パス 2」フィールドを使用して URL をカスタマイズできます。<br><br><b> 注：</b><ul><li>（最終的な URL を持つアカウント）表示 URL と最終的な URL のドメイン名は一致する必要があります。</li><li>2022 年 8 月 [!DNL Microsoft Advertising] 廃止された拡張テキスト広告は、レポートおよび削除のみができるようになりました。</li></ul> |
| [!UICONTROL Display Path 1] | （拡張テキスト広告、動的検索広告、レスポンシブ検索広告のみ）最終的な URL から自動的に抽出された、表示 URL に追加されるテキスト。 URL 内の各パスの前には、スラッシュ（/）が付きます。 パスにスラッシュ （/）や改行（\n）を含めることはできません。 各パスの最大長は 15 文字または 7 つの 2 バイト文字です。<br><br> 広告カスタマイズ機能を挿入するには、次の形式を使用します。ここで、「Default text」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。`{CUSTOMIZER.Attribute name:Default text}` 例：`{CUSTOMIZER.Discount:10%}`<br><br>[!UICONTROL Display Path 1] が「deals」の場合、表示 URL は &lt; ディスプレイ URL>/deals （www.example.com/dealsなど）になります。2022 年 8 月 <br><br>[!DNL Microsoft Advertising] 廃止された拡張テキスト広告は、レポートおよび削除のみができるようになりました。 |
| [!UICONTROL Display Path 1] | （拡張されたテキスト広告、動的検索広告、レスポンシブ検索広告のみ）追加の表示パス。[!UICONTROL Display Path 1] しくはエントリを参照してください。<br><br> 例：[!UICONTROL Display Path 1] が「deals」で、[!UICONTROL Display Path 2] が「local」の場合、表示 URL は &lt;<i>display URL</i>>/deals/local （www.example.com/deals/localなど）になります。 |
| [!UICONTROL Start Date] | （拡張サイトリンクのみ）広告主のタイムゾーンおよび次のいずれかの形式（m/d/yyyy、m/d/yy、m-d-yyyy または m-d-yy）でサイトリンクの入札を行うことができる最初の日付。 新しい拡張サイトリンクのデフォルトは現在の日付です。 <b> 注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクがあるキャンペーンにのみ作成するか、サイトリンクを作成しないキャンペーンに作成できます。 |
| [!UICONTROL End Date] | 広告と共にサイトリンクを表示できる最後の日付。広告主のタイムゾーンで、m/d/yyyy、m/d/yy、m-d-yyyy または m-d-yy のいずれかの形式です。 新しいサイトリンクの場合、デフォルトは `[blank]` （終了日なし）です。 |
| [!UICONTROL Call To Action] | 広告に含めるcall to action。 使用可能な値のリストについては [API リファレンス ](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction) を参照してください。ただし、アクションに対する複数のワードの呼び出しをバルクシートに複数のワードとして入力します（「BetNow」ではなく「Bet Now」など）。 |
| [!UICONTROL Call To Action Language] | call to action オプションの言語です。 使用可能な言語のリストについては、[API リファレンス ](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename) を参照してください。 |
| [!UICONTROL Base URL/Final URL] | 広告をクリックした際に検索エンジンユーザーが取得されるランディングページの URL （キャンペーンまたはアカウントに設定されている追加パラメーターを含む）。 キーワードレベルのベース URL/最終 URL が、広告レベル以降の URL を上書きします。<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Destination URL] | （情報目的で生成されたバルクシートに含まれ、検索エンジンに投稿されない）宛先 URL を持つアカウントの場合、これは、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 検索エンジン固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br> 最終 URL を持つアカウントの場合、この列には「ベース URL/最終 URL」列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | 検索アカウントまたはキャンペーン設定のトラッキングパラメーターに変数が含まれる場合、`{custom_code}` の動的変数に置き換わるデータです。 トラッキング URL にカスタム値を挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告の形式：<i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i> （ショッピング広告）、<i>[!UICONTROL Responsive Search Ad]</i>、<i>[!UICONTROL Text ad]</i>。 新規広告のデフォルトは <i>[!UICONTROL Text ad]</i> です。 |
| [!UICONTROL Ad Group Start Date] | 広告グループに対して入札を行うことができる最初の日付。広告主のタイムゾーンおよび次のいずれかの形式です：m/d/yyyy、m/d/yy、m-d-yyyy または m-d-yy。 新しい広告グループの場合、デフォルトは現在の日付です。 |
| [!UICONTROL Ad Group End Date] | 広告グループに入札を配置できる最終日付。広告主のタイムゾーンおよび次のいずれかの形式です：m/d/yyyy、m/d/yy、m-d-yyyy または m-d-yy。 新しい広告グループの場合、デフォルトは [ 空白 ] （終了日なし）です。 |
| [!UICONTROL Tracking Template] | （任意）トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL をパラメーターに埋め込みます。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、それより上のすべてのレベルの値を上書きします。<br><br> キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキングの場合、レコードを保存すると、検索、ソーシャルおよびCommerceによってリダイレクトコードとトラッキングコードが自動的に追加されます。<br><br> サードパーティのリダイレクトおよびトラッキングの場合は、値を入力します。<br><br> トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、[!DNL Microsoft Advertising] ドキュメントを参照してください。<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Landing Page Suffix] | 情報を追跡するために最終的な URL の末尾に追加するパラメーター。 例：`param2=value1&param3=value2`<br><br> 「[ のクリック追跡形式  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) を参照。<br><br> 下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下にサフィックスを設定するには、[!DNL Microsoft Advertising] エディターを使用します。 |
| ネットワーク状態の検索 | 広告グループの広告を検索ネットワークの様々な要素に配置するかどうか：<ul><li><i> すべて：</i> すべての Bing 検索ネットワークおよび同時配信の検索パートナーに広告を配信します。</li><li><i>OwnedAndOperatedOnly:</i>Bing および Yahoo にのみ広告を配置します web サイト。</li><li><i>SyndicatedSearchOnly:</i> Bing および Yahoo にのみ広告を配置します。 同時配信の検索パートナー</li><li><i> オフ：</i> 広告をコンテンツネットワークにのみ配置します（検索ネットワークには配置しません）。</li></ul> 新しい広告グループの場合、デフォルトはオンです。 |
| [!UICONTROL Content Network Status] | 非推奨 |
| [!UICONTROL Languages] | 広告グループの広告のターゲット言語：[!UICONTROL English]、[!UICONTROL French]、[!UICONTROL Finnish]、[!UICONTROL German]、[!UICONTROL Norwegian]、[!UICONTROL Spanish] または [!UICONTROL Swedish]。 新しいキャンペーンのデフォルトは [!UICONTROL English] です。<br><br> この設定は、広告を表示できる国と地域を決定します。 キャンペーンの場所ターゲットと互換性のある言語を選択してください。 |
| [!UICONTROL Budget Type] | 予算が <i>[!UICONTROL Daily]</i> （デフォルト）か <i>[!UICONTROL Monthly]</i> か。<br><br> メモ：最適化されたポートフォリオにキャンペーンを割り当てると、この値は自動的に [!UICONTROL Daily] に設定されます。 |
| [!UICONTROL Device] | キャンペーンレベルまたは広告グループレベルで入札調整が行われるデバイスタイプ：<i>[!UICONTROL smartphone]</i>、<i>[!UICONTROL tablet]</i>、<i>[!UICONTROL desktop]</i>。 |
| [!UICONTROL Bid Adjustment] | 指定したターゲット タイプの入札調整。 例えば、キーワードレベルの入札が 1 USD で、スマートフォンの入札調整額が 50% の場合、スマートフォンの入札は 1.50 USD になります。 デフォルトでは、すべてのターゲットはキーワードレベルの入札で入札されます。 有効な割合は次のとおりです。<ul><li>スマートフォンとタブレット：-100 （デバイスタイプに入札しない）、および–90～900</li><li>デスクトップ：0 ～ 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | 広告またはサイトリンクを表示するデバイスのタイプ：<i>[!UICONTROL All]</i> （デフォルト）または <i>[!UICONTROL Mobile]</i>。 Mobile が指定されている場合、ネットワークはデスクトップまたはタブレットユーザーではなく、モバイルデバイスユーザーに広告またはサイトリンクを表示しようと試みます。 それ以外の場合、ネットワークは任意のデバイスタイプで広告またはサイトリンクを表示します。 <b> 注意：</b> ネットワークでは、優先デバイスタイプで広告が表示されるとは保証されません。 |
| [!UICONTROL Param2] | キーワードのベース URL または広告のタイトル、説明またはベース URL に `{Param2}` の動的置換文字列が含まれる場合に、置換値として使用する文字列です。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、タイトル 1 とタイトル 2 を組み合わせると、最大 76 文字になる場合があります）。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Param3] | キーワードのベース URL または広告のタイトル、説明またはベース URL に `{Param3}` の動的置換文字列が含まれる場合に、置換値として使用する文字列です。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、タイトル 1 とタイトル 2 を組み合わせると、最大 76 文字になる場合があります）。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Link Name] | サイトリンクテキスト。 キャンペーン内で一意である必要があります。 Description1 と Description2 を指定した場合、サイトリンク テキストには最大 25 個の 1 バイト文字または 12 個の 2 バイト文字を含めることができます。それ以外の場合、サイトリンク テキストには最大 35 個の 1 バイト文字または 17 個の 2 バイト文字を含めることができます。説明を含む 2、4、6 個の拡張サイトリンクを表示する <br><br>[!DNL Microsoft Advertising]、説明を含まない 4 または 6 個の拡張サイトリンクを 1 行に広告と共に表示することもできます。<br><br> 新しい拡張サイトリンクは、既存の拡張サイトリンクがあるキャンペーンでのみ、またはサイトリンクがないキャンペーンで作成できます。 |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止されたキャンペーンを削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止されている広告グループを削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止したキーワードを削除するには、値 `Deleted` を入力します。 <b> 注意：</b> 複数の一致タイプを持つキーワードのトラッキング URL を作成する場合、各一致タイプのキーワードのステータスは同じである必要があります。 |
| [!UICONTROL Placement Status] | 非推奨 |
| [!UICONTROL Ad Status] | 広告の表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告のみ）、<i>[!UICONTROL Disapproved]</i> （編集不可）、<i>[!UICONTROL Paused]</i>。 新規広告のデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止された広告を削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i> または <i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットのデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止したターゲットを削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトは [!UICONTROL Active] です。 アクティブなサイトリンクを削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Location Status] | 場所ターゲットのステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトは [!UICONTROL Active] です。 アクティブな位置を削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の製品グループのみ）。 新製品グループのデフォルトは [!UICONTROL Active] です。 アクティブな製品グループを削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Device Target Status] | キャンペーンレベルまたは広告グループレベルデバイスターゲットのステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i>。 新規キャンペーンおよび広告グループの場合、デフォルトは [!UICONTROL Active] です。 |
| [!UICONTROL RLSA Target Status] | キャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは（Google広告のみ）除外のステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットまたは除外のデフォルトは [!UICONTROL Active] です。 アクティブなターゲットまたは除外を削除するには、値 `Deleted` を入力します。 |
| \[ 広告主固有のラベル分類\] | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 エンティティごとに分類ごとに 1 つの値のみを含めることができます（キャンペーン A の「カラー」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加する新しいコンポーネントは、自動的にラベルに関連付けられます。 製品グループのラベル分類は、単位（最も詳細な単位）レベルで適用されます。<br><br> 分類名も分類値も、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられている制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><b>> 制約は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にキャンペーンの「[!UICONTROL AMO ID]」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に広告グループの「[!UICONTROL AMO ID]」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Placement ID] | 非推奨 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に a） キーワードを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれていない限り、キーワードを変更する場合にのみ必要です。 |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] レスポンシブ検索広告の場合、広告データを編集または削除するには広告 ID または AMO ID が必要です。 その他のすべてのエンティティタイプでは、AMO ID が必要となるのは、広告ステータスを変更した場合のみです。ただし、行に（a）広告を識別するのに十分な広告プロパティ列、または（b）「[!UICONTROL AMO ID]」が含まれる場合を除きます。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、一方の広告のステータスのみが変更されます。</p><p><b> メモ：</b> 編集する場合、a）既存の広告のステータスを除く広告プロパティ列、または b）レスポンシブ検索広告のデータが含まれ、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も指定されていない場合、新しい広告が作成され、既存の広告は変更されません。 </p> |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] サイトリンクを変更または削除した場合にのみ必要です。ただし、行に a） サイトリンクを識別するのに十分なプロパティ列、または b） 「[!UICONTROL AMO ID]」が含まれる場合を除きます。 ただし、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含まれず、プロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。</p><p><b> 注意：</b> 既存のサイトリンクの [ 状態 ] 以外のサイトリンク プロパティの列を編集し、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含めない場合は、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL Product Group ID] | 既存の商品グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 製品グループを変更または削除する場合にのみ必要です。ただし、行に a）製品グループを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれる場合を除きます。 |
| 場所 ID | 場所ターゲットの一意の [!DNL Microsoft Advertising] ID。 場所のリストをダウンロードするには、[!DNL Microsoft Advertising] advertising アカウントの資格情報を使用して [!DNL Microsoft Advertising] 開発者ポータルにログインします。 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、場所ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意の ID。 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、自動ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルの RLSA ターゲットを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットまたは除外を変更または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意の ID。 レスポンシブ検索広告の場合、広告 ID を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つその他すべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID でデータを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |
| [!UICONTROL EF Error Message] | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL SE Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報提供のために生成されたバルクシートに含まれる）広告が違反したGoogle広告ポリシーの名前とテキストを表示するプレースホルダー。 |
| [!UICONTROL Retail Hash] | （詳細キャンペーン管理を使用して生成されたバルクシートに含まれる、情報提供の目的で）項目が詳細（ACM）ビューを使用して生成されたことを示す英数字のハッシュコード（f9639f40cdf56524b541e5dacf55a991 など）。 |

[^1]:[!DNL Excel] は、ファイルを開いたときに、大きな数値を指数表記（2115585666 の場合は 2.12E+09 など）に変換します。 標準の表記で数字を表示するには、列の任意のセルを選択して、式バーの内側をクリックします。

## 各アカウントコンポーネントを作成、編集または削除するために必要なフィールド {#bulksheet-fields-per-component-microsoft}

以下の節には、特定のアカウントエンティティに関連するフィールドが含まれます。

>[!NOTE]
>
>フィールドがアクションに適用できない場合、フィールドに入力された値は無視されます。

### キャンペーンフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須。 アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | キャンペーンの作成に必要です。 キャンペーンの 1 日あたりの支出制限（金銭記号および句読点の有無は問わない）。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Channel Type] | キャンペーンの作成に必要です。 |
| [!UICONTROL Delivery Method] | オプション |
| [!UICONTROL Campaign Priority] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Merchant ID] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Sales Country] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Product Scope Filter] | （ショッピングキャンペーン）任意 |
| [!UICONTROL DSA Domain Name] | タイプ a）「[!UICONTROL DynamicSearchAds]」または b）「[!UICONTROL Search]」（[!DNL ExperimentId] 要素が設定されていない場合）のキャンペーンを作成するために必要です。 |
| [!UICONTROL DSA Domain Language] | タイプ a）「[!UICONTROL DynamicSearchAds]」または b）「[!UICONTROL Search]」（[!DNL ExperimentId] 要素が設定されていない場合）のキャンペーンを作成するために必要です。 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Landing Page Suffix] | <p>オプション |
| [!UICONTROL Budget Type] | キャンペーンの作成に必要です。 |
| [!UICONTROL Device] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Campaign Status] | キャンペーンを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | キャンペーン名を変更した場合にのみ必要です。ただし、行にキャンペーンの「[!UICONTROL AMO ID]」が含まれる場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 広告グループフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Group Type] | 広告グループを作成するために必要です。 |
| [!UICONTROL Audience Target Method] | オーディエンスとグループの作成にのみ必要です。 |
| [!UICONTROL Ad Group Start Date] | オプション |
| [!UICONTROL Ad Group End Date] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Search Network Status] | （検索ネットワーク上のキャンペーンのみ）任意 |
| [!UICONTROL Languages] | オプション |
| [!UICONTROL Device] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Status] | 広告グループを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Ad Group ID] | 広告グループ名を変更した場合にのみ必要です。ただし、行に広告グループの「[!UICONTROL AMO ID]」が含まれている場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キーワードフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Keyword] | 必須 |
| [!UICONTROL Match Type] | 複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード ID の値が必要です。 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Param1] | オプション |
| [!UICONTROL Param2] | オプション |
| [!UICONTROL Keyword Status] | キーワードを削除する場合にのみ必須です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Keyword ID] | 行に a） キーワードを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれていない限り、キーワードを編集または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 動的検索広告フィールド

>[!NOTE]
>
>作成サポートは利用できません。

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 説明を編集するために必要です。 <b> メモ：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display Path 1] | フィールドの編集に必要です。 |
| [!UICONTROL Display Path 2] | フィールドの編集に必要です。 |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告ステータスを変更した場合にのみ必要です。ただし、行に a&amp;rpar；広告を識別するのに十分な広告プロパティ列または b&amp;rpar;「[!UICONTROL AMO ID]」が含まれている場合は除きます。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 製品（買い物）広告フィールド

ショッピング広告の作成の詳細は、「[ ショッピング・キャンペーン  [!DNL Microsoft Advertising]  実装 ](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html)」を参照してください。

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Promotion Line] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列、または（b）「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ必要です。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### レスポンシブ（マルチメディア）広告フィールド

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | レスポンシブ広告の場合、広告を作成するには [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]、[!UICONTROL Ad Title 3] が必要で、その他の広告タイトルフィールドはオプションです。 必須以外のフィールドに既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 <b> メモ：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 広告を作成するには [!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] が必要で、[!UICONTROL Description Line 3] と [!UICONTROL Description Line 4] はオプションです。 <b> メモ：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Business Name] | 広告を作成または削除するために必要です。 |
| [!UICONTROL Call To Action] | 広告の作成に必要です。 |
| [!UICONTROL Call To Action Language] | 広告の作成に必要です。 |
| [!UICONTROL Base URL/Final URL] | 広告の作成に必要です。 |
| [!UICONTROL Creative Type] | （オプション） |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列、または（b）「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ必要です。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### レスポンシブ検索広告フィールド

この広告タイプの場合は、[!UICONTROL Responsive Search Ad] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | レスポンシブ検索広告の場合、広告を作成するには [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]、[!UICONTROL Ad Title 3] が必要で、その他の広告タイトルフィールドはオプションです。 必須以外のフィールドに既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、広告を作成するには [!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] が必要で、[!UICONTROL Description Line 3] と [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | オプション |
| [!UICONTROL Display Path 1] | オプション |
| [!UICONTROL Display Path 2] | オプション |
| [!UICONTROL Base URL/Final URL] | 広告の作成に必要です。 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID]」が含まれていない場合、広告を編集または削除する必要があります。 |
| [!UICONTROL AMO ID] | 広告 ID を含めない場合、広告を編集または削除する必要があります。 |

### テキストとフィールド

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

>[!NOTE]
>
>拡張テキスト広告は非推奨（廃止予定）となりました。 既存のテキスト広告のみを削除できます。

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | 読み取り専用 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 読み取り専用 |
| [!UICONTROL Display URL] | 読み取り専用 |
| [!UICONTROL Display Path 1] | 読み取り専用 |
| [!UICONTROL Display Path 2] | 読み取り専用 |
| [!UICONTROL Base URL/Final URL] | 読み取り専用 |
| [!UICONTROL Custom URL Param] | 読み取り専用 |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Tracking Template] | 読み取り専用 |
| [!UICONTROL Creative Preferred Devices] | 読み取り専用 |
| [!UICONTROL Ad Status] | 必須 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | 広告 ID を含めない限り、データを編集または削除するために必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 動的検索のターゲット（自動ターゲット）フィールド

>[!NOTE]
>
>作成サポートは利用できません。

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Auto Target Expression] | 必須。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Target Status] | ターゲットの削除が必要です |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、自動ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### ショッピング製品グループ フィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Match Type] | 製品グループを作成するために必要です。 |
| [!UICONTROL Max CPC] | 製品グループを作成するために必要です。 |
| [!UICONTROL Parent Product Groupings] | 必須 |
| [!UICONTROL Product Grouping] | 必須 |
| [!UICONTROL Partition Type] | 製品グループを作成するために必要です。 |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Product Group Status] | 製品グループを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Product Group ID] | 製品グループを変更または削除した場合にのみ必要です。ただし、行に a）製品グループを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれる場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キャンペーンレベルのサイトリンクフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| 説明ライン 1 | オプション |
| [!UICONTROL Description Line 2] | オプション |
| [!UICONTROL Start Date] | オプション |
| [!UICONTROL End Date] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Link Name] | 必須 |
| [!UICONTROL Sitelink Status] | サイトリンクを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Sitelink ID] | 行に a） サイトリンクを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれていない限り、サイトリンクを変更または削除する場合にのみ必要です。 ただし、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含まれず、プロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。<br><br><b> 注意：</b> 既存のサイトリンクのステータスを除くサイトリンクプロパティの列を編集し、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含めない場合は、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 場所のターゲットフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | ターゲットの作成に必要 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | 場所のターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | キャンペーン ID を含めない場合は、データの編集または削除に必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスのターゲットフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットを削除するために必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必要。 キャンペーンレベルのデバイスターゲットには適用されません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのデバイスターゲットにのみ適用できます。 |
| [!UICONTROL AMO ID] | デバイスターゲット ID を含めない限り、データの編集または削除に必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キャンペーンレベルおよび広告グループレベルの RLSA ターゲットフィールド

各データ・フィールドの説明は、「[ 使用可能なすべてのデータ・フィールド ](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットに必要です。 キャンペーンレベルのターゲットには適用されません。 |
| [!UICONTROL Audience] | 新しいターゲットの作成に必要です。 |
| [!UICONTROL Target Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL RLSA Target Status] | ターゲットの削除に必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのターゲットにのみ適用されます。 |
| [!UICONTROL RLSA Target ID] | 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | RLSA ターゲット ID を含めない限り、データを編集または削除するために必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

>[!MORELIKETHIS]
>
>* [ 付録 – バルクシート エラー ](../bulksheet-errors.md)
>* [ バルクシートで実行できる操作 ](bulksheet-operations.md)
>* [ サポートされるバルクシート ファイル形式 ](bulksheet-file-formats.md)
>* [ バルクシートファイルのダウンロード/作成 ](../bulksheet-download.md)
>* [ のクリック追跡形式  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [ バルクシートファイルまたは修正されたエラーファイルのアップロード ](../bulksheet-upload.md)
