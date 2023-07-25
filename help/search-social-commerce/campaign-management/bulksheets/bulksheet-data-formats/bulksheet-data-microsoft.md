---
title: 次に必要なバルクシートデータ： [!DNL Microsoft Advertising] アカウント
description: 次のバルクシートで、必須ヘッダーフィールドとデータフィールドを参照します： [!DNL Microsoft Advertising] アカウント。
exl-id: a3090962-49df-46b0-89f8-98b633c3ea7a
source-git-commit: 9cdfe415c9ec2d7e7b65d5a46d208329d66ca14a
workflow-type: tm+mt
source-wordcount: '6888'
ht-degree: 0%

---

# 付録 — の必須バルクシートデータ [!DNL Microsoft Advertising] アカウント

作成および更新するには [!DNL Microsoft Advertising] キャンペーンデータを一括で使用する場合は、専用の形式の検索、ソーシャル、コマースのバルクシートファイルを使用できます。 [!DNL Microsoft Advertising] アカウント。 次のいずれかを実行できます。a) [既存のアカウントに対してバルクシートファイルを生成](../bulksheet-download.md) 必要なファイル形式で、または b) 手動で作成する ([サポートされるバルクシートファイル形式](bulksheet-file-formats.md)」を参照してください )。

各バルクシートには、ヘッダーフィールドと、 [実行する特定の操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) （広告の作成など）。 フィールドが必須でない場合は、ヘッダー行とデータ行から省略できます。 バルクシートファイルをアップロードすると、すべてのカスタム列が削除されます。

以下に、使用可能なすべてのデータフィールドの表と、個々のエンティティ（キャンペーン、キーワードなど）のデータの追加、編集、削除に必要なフィールドを示す追加テーブルを示します。

## すべての使用可能なデータフィールド {#bulksheet-fields-all-microsoft}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、[各アカウントコンポーネントの作成、編集または削除に必要なフィールド](#bulksheet-fields-per-component-microsoft).&quot;

| フィールド | 説明 |
|----|----|
| [!UICONTROL Platform] | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 最大長は 128 文字です。 |
| [!UICONTROL Campaign Budget] | 日次または月次のキャンペーン予算。通貨記号と句読点の有無は問いません。 0.05 以上にする必要があります。 |
| [!UICONTROL Channel Type] | キャンペーンのターゲットにするチャネルのタイプ： <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i>または <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | （日次予算のみのキャンペーン）キャンペーンの広告を毎日どの程度の速さで表示するかを指定できます。<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新規キャンペーンのデフォルト）:広告インプレッションを 1 日にわたって広める。</li><li><i>[!UICONTROL Accelerated]:</i> 広告を可能な限り頻繁に表示して、予算に達します。 その結果、広告が 1 日後に表示されない場合があります。</li></ul> |
| [!UICONTROL Campaign Priority] | （買い物キャンペーンのみ）複数のキャンペーンが同じ製品を宣伝する場合に使用される優先順位： <i>[!UICONTROL Low]</i> （新しいキャンペーンのデフォルト） <i>[!UICONTROL Medium]</i>または <i>[!UICONTROL High]</i>.<br><br>同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークは、まずキャンペーンの優先順位を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンが同じ優先順位の場合、最も入札額の高いキャンペーンが適格になります。 |
| [!UICONTROL Merchant ID] | （マーチャントフィードにリンクされたショッピングキャンペーンおよびオーディエンスキャンペーンのみ）商品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。 |
| [!UICONTROL Sales Country] | ( 買い物キャンペーンのみ、既存のキャンペーンの読み取り専用 ) キャンペーンの製品が販売された国。 製品は対象国に関連付けられているので、この設定によってキャンペーンで広告される製品が決まります。 |
| [!UICONTROL Product Scope Filter] | （ショッピングネットワークを使用するキャンペーンのみ）商品広告をキャンペーン用に作成できる商品アカウント内の製品。 dimension=attribute の形式を使用して、製品をフィルタリングする製品次元と属性の組み合わせを 7 つまで入力できます。 複数のフィルターは「>>」区切り文字で区切ります。 使用可能な製品ディメンションのリストについては、[買い物キャンペーンの製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> 例：&quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> 既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL DSA Domain Name] | （タイプ a のキャンペーン） &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot;または b) &quot;<i>[!UICONTROL Search]</i>」と入力します。 [!DNL ExperimentId] element isn set) 動的検索広告をターゲットにする Web サイトのドメイン名。 最大長は 2,048 文字です。 ドメイン名に `www`の場合は、トリミングされて使用されません。<br><br>既存のキャンペーンでは、ドメインを編集することはできませんが、他のプロパティを更新するにはドメインを含める必要があります。 |
| [!UICONTROL DSA Domain Language] | （タイプ a のキャンペーン） &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot;または b) &quot;<i>[!UICONTROL Search]</i>」と入力します。 [!DNL ExperimentId] element isn set) 動的検索広告のターゲットにする Web サイトページの言語。 サポートされるドメイン言語は次のとおりです。 [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish]、および [!UICONTROL Swedish].<br><br>既存のキャンペーンでは、言語を編集することはできませんが、他のプロパティを更新するには言語を含める必要があります。 |
| [!UICONTROL Ad Group Name] | 広告グループを識別する一意の名前。 最大長は 128 文字です。 末尾の空白文字は保存されません（例えば、「Ad Group 1」は「Ad Group 1」として保存されます）。 |
| [!UICONTROL Ad Group Type] | ( 検索ネットワーク上のキャンペーン既存の広告グループの読み取り専用 ) 広告グループのタイプ： <i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ） <i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）および <i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告および既存の拡張テキスト広告のみ）。 キャンペーンタイプによっては、複数の広告グループタイプを含めることができます。 |
| [!UICONTROL Keyword] | （検索ネットワーク上のキャンペーンのみ）キーワード文字列。 最大長は 50 文字です。<br><br><b>メモ：</b><ul><li>広告グループまたはキャンペーンレベルでキーワードを除外するには、 [!UICONTROL Match Type] から `Negative`. 行に広告グループ名が含まれる場合、そのキーワードは広告グループに対して除外されます。 行に広告グループ名が含まれていない場合、このキーワードはキャンペーン全体に対して除外されます。</li><li>の変更 [!DNL Microsoft Advertising] キーワードは、既存のキーワードを削除し、新しいキーワード ID を持つ新しいキーワードを作成します。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。</li></ul> |
| プレースメント | 非推奨 |
| [!UICONTROL Audience] | 検索広告 (RLSA) のリマーケティングリストは、キャンペーンまたは広告グループのターゲットオーディエンスです。 |
| [!UICONTROL Target Type] | （RLSA ターゲットのみ）ターゲットのタイプ： <i>[!UICONTROL Inclusion]</i> または <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | 広告グループの動的検索ターゲット。 すべてのターゲットに対して、[!UICONTROL All Web Pages].&quot;<br><br>最大 3 つの動的検索条件をターゲットにするには、という形式を使用します。 `<category>=<target>`で、 &lt;category> には、以下の任意のカテゴリを含めることができます。 個々のカテゴリの複数のターゲットを「`[blank space] and [blank space]`」と入力し、複数のカテゴリを「`[blank space] and [blank space]`&quot;.<br><ul><li><i>カテゴリ：</i> 特定のGoogleコンテンツカテゴリを持つインデックス付きページの動的検索広告を表示する。</li><li><i>URL:</i> 特定の URL を持つインデックス付きページで、URL 内の任意の場所に値を含む動的検索広告を表示する。</li><li><i>ページタイトル：</i> ページタイトルに特定のテキストを含むインデックス付きページの動的検索広告を表示する。</li><li><i>ページコンテンツ：</i> 特定のコンテンツを含むインデックス付きページの動的検索広告を表示する。</li></ul>例：url=shoes.example.com および page title=footwear<br>例：すべてのウェブページ |
| [!UICONTROL Location] | キャンペーンまたは広告グループの広告を配置する地理的な場所。値では大文字と小文字が区別されません。 キャンペーンまたは広告グループの値を入力しない場合、すべてのロケーションがターゲットになります。 特定の場所をターゲットにするには、 [!DNL Microsoft Advertising] 場所コードの形式。 ロケーションリストをダウンロードするには、 [!DNL Microsoft Advertising] 開発者ポータル [!DNL Microsoft Advertising] advertising アカウント資格情報。 <b>注意：</b> 位置を除外するには、位置コードの前にマイナス記号 (`-`など ) `-United States`. |
| [!UICONTROL Location Type] | 場所のタイプ（市区町村、国、MetroArea、郵便番号、都道府県など）。 ロケーションリストをダウンロードするには、 [!DNL Microsoft Advertising] 開発者ポータル [!DNL Microsoft Advertising] advertising アカウント資格情報。 |
| [!UICONTROL Match Type] | （検索ネットワーク上のキャンペーンのみ）キーワード一致オプション。 これには、動的検索ターゲットまたは製品グループのキーワード一致オプションが含まれる場合があります。 次の値が含まれます。 <i>[!UICONTROL Broad]</i> （新しいキーワードのデフォルト） <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> （広告グループがコンテンツネットワークをターゲットにする場合、キーワードに対して自動的に設定されます）。 <i>[!UICONTROL Negative]</i> （コンテンツネットワーク上のキーワードを除外する場合） <i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索ターゲットのデフォルト） <i>[!UICONTROL Product Group]</i> （新しい製品グループのデフォルト）、または <i>[!UICONTROL Negative Product Group]</i> （製品グループを除外する場合）。  複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード ID の値が必要です。<br><br>Broad Match Modifier の場合は、「Broad」を選択し、 `+` 必要なキーワード内の任意の単語の前 (「`+red +shoes`&quot; &quot;&quot;red&quot;と&quot;shoes&quot;の両方が必要 )。<br><br>の一致タイプの変更 [!DNL Microsoft Advertising] キーワードで既存のキーワードが削除されない。 |
| [!UICONTROL Max CPC] | （検索ネットワーク上のキャンペーン）最大クリック単価 (CPC)。キーワード、製品グループ、動的検索のターゲットに基づいて広告クリックに支払われる最高の金額で、通貨記号や句読点の有無は問いません。  最適化されたポートフォリオ内の既存のキーワードおよび製品グループレコードの場合、更新は 1 日のみ有効で、次の最適化サイクルで上書きされます。 <b>注意：</b> 除外キーワードの入札は設定できません。 |
| [!UICONTROL Max Content CPC] | （2017 年に廃止されたコンテンツネットワークの前に作成された CPC キャンペーンのみ読み取り専用）最大コンテンツコストパークリック (CPC)。これは、表示ネットワークサイトから広告クリックに支払う最も高い金額で、金額記号や句読点は使用しない。 |
| [!UICONTROL Audience Target Method] | （オーディエンス広告グループ）次のいずれを実行するか。<ul><li><i>[!UICONTROL Target and Bid]:</i> 広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーに対してのみ広告を表示する。</li><li><i>[!UICONTROL Bid Only]:</i>ターゲットオーディエンスに関連付けられていないユーザーが他の広告グループレベルのターゲットを満たしている限り、広告を表示する。</li></ul> ただし、特定のオーディエンスに対して広告が表示される可能性を高めるには、それらのオーディエンスの入札額を高く設定します。 |
| [!UICONTROL Parent Product Groupings] | 親製品グループの階層。<br><br>例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | 製品グループ（「brand=acme」や「All Products」など）。<br><br><b>メモ：</b><ul><li>指定した製品グループが親製品グループ階層に存在しない場合、検索、ソーシャル、コマースは、必要な階層の任意の部分を作成します。</li><li>検索、ソーシャル、コマースでは、「[!UICONTROL All Products]「 」グループは、広告グループのデフォルトの入札に設定されたデフォルトの入札を持つショッピングキャンペーンで広告グループを作成する際に常に使用されます。 検索、ソーシャル、コマースでは、「[!UICONTROL Everything Else]「広告グループ階層の各レベルでの広告グループのデフォルト入札額を持つグループ。 これらのデフォルトグループを明示的に作成し、それらを除外したり、入札を変更したりできます。</li><li>各広告グループは、最大 8 層の製品グループ (「[!UICONTROL All Products]「それから他の七段。</li></ul> |
| [!UICONTROL Partition Type] | 製品グループのパーティションタイプ： <i>[!UICONTROL subdivision]</i> （子製品グループがある場合）または <i>[!UICONTROL unit]</i> （子製品グループがない場合）。 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | （拡張テキスト広告、マルチメディア広告、レスポンシブ検索広告のみ）広告のヘッドライン。 各広告タイトルフィールドの最大の長さは、30 文字または 15 文字で、動的テキスト（キーワードの値など）は含まれます。 `{Param2}` および `{Param3}` 動的な代替変数、広告のカスタマイズなど ) を使用できます。<br><br> レスポンシブ検索広告の場合、次の形式を使用して広告をカスタマイズします。「Default text」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。 `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>拡張テキスト広告の場合、広告タイトルと広告タイトル 2 が必要です。 [!UICONTROL Ad Title 3] はオプションです。 [!DNL Microsoft Advertising] 2022 年 8 月に非推奨となった拡張テキスト広告。レポートおよび削除のみ可能になりました。<br><br>マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告の場合 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] は必須で、その他の広告タイトルフィールドはすべてオプションです。<br><br>必須でないフィールドの既存の値を削除するには、 `[delete]` （括弧を含む）<br><br>拡張テキスト広告を除くすべての広告タイプで、広告コピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | （レスポンシブ検索広告のみ）（オプション）対応する広告タイトルを固定する位置： `[null]` （値なし。すべての位置の対象となる広告タイトルにします）、1、2 または 3。 例えば、 [!UICONTROL Ad Title Position] の値が 1 の場合、 [!UICONTROL Ad Title] は、位置 1 にのみ表示されます。 デフォルトでは、すべての広告タイトルは null です（値はありません）。 既存の値を削除するには、 `[delete]` （括弧を含む）<br><br><b>注意：</b> 複数の広告タイトルを同じ位置にピン留めできます。 広告ネットワークは、位置に固定された広告タイトルの 1 つを使用します。 位置 3 にピン留めされたタイトルは、広告と共に表示されない場合があります。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | （テキスト広告、動的検索広告、マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告、拡張キャンペーンレベルサイトリンクのみ）広告またはサイトリンクの本文。<br><br>サイトリンクの場合は、オプションで両方を使用します [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] を追加します。 各説明フィールドには、最大 35 文字の 1 バイト文字または 17 文字の 2 バイト文字を含めることができます。<br><br>広告の場合、各説明フィールドの最大長は、任意の動的テキスト（キーワードや広告のカスタマイズの値など）を含む 90 文字または 45 バイト文字です。<br><br>レスポンシブ検索広告の場合、次の形式を使用して広告をカスタマイズします。「デフォルトテキスト」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。 `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>テキスト広告および動的検索広告の場合、説明行 1 が必要で、 [!UICONTROL Description Line 2] はオプションです。<br><br>マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告の場合 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] が必要で、 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。<br><br>既存の値を削除するには、 `[delete]` （括弧を含む）<br><br><b>メモ：</b><ul><li>（標準テキスト広告）タイトルとテキストを組み合わせるには、3 語以上の単語を使用する必要があります。</li><li>（拡張テキスト広告）このフィールドには、オプションで {Param2} および {Param3} 動的な代替変数。 その場合、広告テキストの最大の長さは 300 シングルバイトまたは 150 ダブルバイト文字です。 [!DNL Microsoft Advertising] 2022 年 8 月に非推奨となった拡張テキスト広告。レポートおよび削除のみ可能になりました。</li><li>（動的検索広告）動的置換テキストは使用できません。</li><li>拡張テキスト広告を除くすべての広告タイプで、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索広告のみ）（オプション）対応する説明を固定する位置： `[null]` （値なし。すべての職階の対象となる説明）、1、2 または 3。 例えば、 [!UICONTROL Description 1 Position] の値が 1 の場合、[ 説明 1] は [ 位置 1] にのみ表示されます。 デフォルトでは、説明は位置にピン留めされません。<br><br>既存の値を削除するには、 `[delete]` （括弧を含む）<br><br><b>注意：</b> 複数の説明を同じ位置にピン留めできます。 広告ネットワークは、位置に固定された説明の 1 つを使用します。 位置 2 に固定された説明は、広告と共に表示されない場合があります。 |
| [!UICONTROL Business Name] | （マルチメディア広告のみ）ビジネス名（最大 25 文字）。 |
| [!UICONTROL Promotion Line] | （製品リスト広告のみ）検索結果の製品リストに含める一意のプロモーション行（「Free shipping now!」など）。 最大長は 45 文字です。<br><br>プロモーション行は、ページ上で広告が表示される場所に応じて、広告に関連した様々な場所（広告の下など）に表示される場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれる URL。<br><br>動的検索広告を拡張すると、広告ネットワークによって Web サイトドメインから動的にこの値が生成されるので、値を入力する必要はありません。<br><br>拡張テキスト広告およびレスポンシブ検索広告の場合、値を入力する必要はありません。 表示 URL は、最終的な URL のドメインから自動的に抽出されます。 オプションで、「パス 1」フィールドと「パス 2」フィールドを使用して URL をカスタマイズできます。<br><br><b>メモ：</b><ul><li>（最終 URL を持つアカウント）表示 URL と最終 URL のドメイン名が一致する必要があります。</li><li>[!DNL Microsoft Advertising] 2022 年 8 月に非推奨となった拡張テキスト広告。レポートおよび削除のみ可能になりました。</li></ul> |
| [!UICONTROL Display Path 1] | （拡張テキスト広告、動的検索広告、レスポンシブ検索広告のみ）最終 URL から自動的に抽出される表示 URL に追加されるテキスト。 各パスの前には、URL の前にスラッシュ (/) が付きます。 パスには、スラッシュ (/) や改行 (\n) 文字を含めることはできません。 各パスの最大長は 15 文字または 2 バイト文字 7 文字です。<br><br>広告カスタマイズ機能を挿入するには、次の形式を使用します。「デフォルトのテキスト」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。 `{CUSTOMIZER.Attribute name:Default text}`例： `{CUSTOMIZER.Discount:10%}`<br><br>例えば、 [!UICONTROL Display Path 1] が「契約」の場合、表示 URL は &lt;display url=&quot;&quot;>/deals(www.example.com/dealsなど )<br><br>[!DNL Microsoft Advertising] 2022 年 8 月に非推奨となった拡張テキスト広告。レポートおよび削除のみ可能になりました。 |
| [!UICONTROL Display Path 1] | （拡張テキスト広告、動的検索広告、レスポンシブ検索広告のみ）追加の表示パス。エントリを見る [!UICONTROL Display Path 1].<br><br>例：If [!UICONTROL Display Path 1] は「契約」で、 [!UICONTROL Display Path 2] が「local」の場合、表示 URL は &lt;<i>表示 URL</i>>/deals/local(www.example.com/deals/localなど ) |
| [!UICONTROL Start Date] | （拡張サイトリンクのみ）広告主のタイムゾーンと次のいずれかの形式で、サイトリンクに入札を配置できる最初の日付。m/d/yyyy、m/d/yy、m-d-yyyy、m-d-yyy のいずれかです。 新しい拡張サイトリンクのデフォルトは現在の日です。 <b>注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーンでのみ作成できます。また、サイトリンクを含まないキャンペーンでも作成できます。 |
| [!UICONTROL End Date] | 広告主のタイムゾーンと、次のいずれかの形式で、サイトリンクが広告と共に表示される最終日。m/d/yyyy、m/d/yy、m-d-yyyy、m-d-yyy のいずれかです。 新しいサイトリンクの場合、デフォルトはです。 `[blank]` （つまり、終了日はありません）。 |
| [!UICONTROL Call To Action] | 広告に含めるコールトゥアクション。 詳しくは、 [使用可能な値のリストの API リファレンス](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)を設定しますが、複数語の呼び出しを入力してアクションを実行する場合は、「BetNow」の代わりに「Bet Now」と入力します。 |
| [!UICONTROL Call To Action Language] | コールトゥアクションオプションの言語。 詳しくは、 [使用可能な言語のリストの API リファレンス](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | 広告のクリック時に検索エンジンユーザーが使用するランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 キーワードレベルのベース URL と最終 URL は、広告レベル以上の URL よりも優先されます。<br><br>既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Destination URL] | ( 情報を提供するために、生成された一括送信シートに含まれます。検索エンジンに投稿されない ) リンク先 URL のアカウントの場合、広告を広告主の Web サイト上のベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づいています。 検索エンジン固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。<br><br>最終 URL を持つアカウントの場合、この列には、ベース URL/最終 URL 列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | に代わるデータ `{custom_code}` 動的変数を設定できます。 トラッキング URL にカスタム値を挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告の形式は次のとおりです。 <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> （買い物広告）、または <i>[!UICONTROL Responsive Search Ad]</i>または <i>[!UICONTROL Text ad]</i>. 新しい広告のデフォルトは、 <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | 広告主のタイムゾーンと以下のいずれかの形式で、広告グループの入札を行う最初の日付。m/d/yyyy、m/d/yy、m-d-yyyy、m-d-yyy のいずれかです。 新しい広告グループの場合、デフォルトは現在の日付です。 |
| [!UICONTROL Ad Group End Date] | 広告主のタイムゾーンと、次のいずれかの形式で、広告グループに入札を配置できる最終日。m/d/yyyy、m/d/yy、m-d-yyyy、m-d-yyy のいずれかです。 新しい広告グループの場合、デフォルトは [空白] （つまり、終了日はありません）。 |
| [!UICONTROL Tracking Template] | （オプション）すべてのオフランディングドメインのリダイレクトおよびトラッキングパラメーターを指定し、最終的な URL をパラメーターに埋め込んだトラッキングテンプレート。 最も詳細なレベル（最も詳細なキーワードを含む）のトラッキングテンプレートは、より高いレベルのすべての値を上書きします。<br><br>Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、リダイレクトおよびトラッキングコードを自動的に追加します。<br><br>サードパーティのリダイレクトとトラッキングの場合は、値を入力します。<br><br>トラッキングテンプレートの最終 URL を示すパラメーターのリストについては、 [!DNL Microsoft Advertising] ドキュメント。<br><br> 既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Landing Page Suffix] | 情報を追跡するために、最終 URL の末尾に追加するパラメーター。 例： `param2=value1&param3=value2`<br><br>参照：[のクリック追跡形式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>下位レベルでの最終的な URL サフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、 [!DNL Microsoft Advertising] 編集者。 |
| ネットワークステータスの検索 | 検索ネットワークの様々な要素に広告グループの広告を配置するかどうかを指定します。<ul><li><i>すべて：</i> すべての Bing 検索ネットワークとシンジケート検索パートナーに広告を配置する。</li><li><i>OwnedAndOperatedOnly:</i>広告を Bing および Yahoo! web サイト。</li><li><i>SyndicateSearchOnly:</i> 広告を Bing および Yahoo! シンジケート検索パートナー。</li><li><i>オフ：</i> 広告をコンテンツネットワークにのみ配置する（検索ネットワークではなく）場合。</li></ul> 新しい広告グループの場合、デフォルトはオンです。 |
| [!UICONTROL Content Network Status] | 非推奨 |
| [!UICONTROL Languages] | 広告グループ内の広告のターゲット言語： [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish]または [!UICONTROL Swedish]. 新しいキャンペーンのデフォルトはです。 [!UICONTROL English].<br><br>この設定は、広告を表示できる国と地域を決定します。 キャンペーンのロケーションターゲットと互換性のある言語を必ず選択してください。 |
| [!UICONTROL Budget Type] | 予算が <i>[!UICONTROL Daily]</i> （デフォルト）または <i>[!UICONTROL Monthly]</i>.<br><br>注意：最適化されたポートフォリオにキャンペーンを割り当てると、この値は自動的にに設定されます。 [!UICONTROL Daily]. |
| [!UICONTROL Device] | キャンペーンまたは広告グループレベルで入札調整がおこなわれるデバイスタイプ。 <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>または <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | 指定したターゲットタイプの入札調整。 例えば、キーワードレベルの入札が 1 USD で、スマートフォンの入札調整が 50%の場合、スマートフォンの入札額は 1.50 USD になります。 デフォルトでは、すべてのターゲットはキーワードレベルの入札で入札されます。 有効な割合は次のとおりです。<ul><li>スマートフォンとタブレット：-100（デバイスタイプに入札しない）かつ —90 ～ 900</li><li>デスクトップ：0 ～ 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | 広告またはサイトリンクの表示を希望するデバイスタイプ： <i>[!UICONTROL All]</i> （デフォルト）または <i>[!UICONTROL Mobile]</i>. モバイルを指定すると、ネットワークはデスクトップユーザーやタブレットユーザーではなく、モバイルデバイスユーザーに対して広告またはサイトリンクを表示しようとします。 そうしないと、ネットワークは任意のデバイスタイプで広告またはサイトリンクを表示します。 <b>注意：</b> ネットワークでは、広告が優先デバイスタイプで表示されるとは限りません。 |
| [!UICONTROL Param2] | キーワードのベース URL または広告のタイトル、説明、またはベース URL に `{Param2}` 動的置換文字列。 最大長は 70 文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1 とタイトル 2 の組み合わせは最大 76 文字になります）。 既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Param3] | キーワードのベース URL または広告のタイトル、説明、またはベース URL に `{Param3}` 動的置換文字列。 最大長は 70 文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1 とタイトル 2 の組み合わせは最大 76 文字になります）。 既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Link Name] | サイトリンクのテキスト。 キャンペーン内で一意である必要があります。 Description1 と Description2 を指定した場合、サイトリンクテキストには最大 25 文字の 1 バイト文字または 12 文字の 2 バイト文字を含めることができます。そうしないと、サイトリンクテキストに最大 35 文字の 1 バイト文字または 17 文字の 2 バイト文字が含まれる場合があります。<br><br>[!DNL Microsoft Advertising] では、説明付きの 2 つ、4 つ、6 つの拡張サイトリンクが表示される場合があります。また、1 行に 4 つ、6 つのサイトリンクが表示され、説明なしで広告が表示される場合もあります。<br><br>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーンまたはサイトリンクを含まないキャンペーンでのみ作成できます。 |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトはです。 [!UICONTROL Active]. アクティブまたは一時停止したキャンペーンを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトはです。 [!UICONTROL Active]. アクティブな広告または一時停止した広告グループを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトはです。 [!UICONTROL Active]. アクティブまたは一時停止したキーワードを削除するには、値を入力します `Deleted`. <b>注意：</b> 複数の一致タイプを持つキーワードの追跡 URL を作成する場合は、各一致タイプのキーワードステータスが同じである必要があります。 |
| [!UICONTROL Placement Status] | 非推奨 |
| [!UICONTROL Ad Status] | 広告の表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> （既存の広告のみ）、 <i>[!UICONTROL Disapproved]</i> （編集不可）または <i>[!UICONTROL Paused]</i>. 新しい広告のデフォルトは、 [!UICONTROL Active]. アクティブな広告または一時停止した広告を削除するには、値を入力します `Deleted`. |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットのデフォルトはです。 [!UICONTROL Active]. アクティブなターゲットまたは一時停止したターゲットを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトはです。 [!UICONTROL Active]. アクティブなサイトリンクを削除するには、値を入力します。 `Deleted`. |
| [!UICONTROL Location Status] | ロケーションターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトはです。 [!UICONTROL Active]. アクティブな場所を削除するには、値を入力します `Deleted`. |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の製品グループのみ）。 新しい製品グループのデフォルトはです。 [!UICONTROL Active]. アクティブな製品グループを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Device Target Status] | キャンペーンまたは広告グループレベルのデバイスターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i>. 新しいキャンペーンおよび広告グループの場合、デフォルトはです。 [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | キャンペーンまたは広告グループレベルの RLSA ターゲットまたは (Google Ads のみ ) 除外のステータス。 <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットまたは除外のデフォルトは、 [!UICONTROL Active]. アクティブなターゲットまたは除外を削除するには、値を入力します `Deleted`. |
| \[ 広告主固有のラベル分類\] | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 エンティティごとに 1 つの分類のみを含めることができます（キャンペーン A の「色」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も精度の高い）レベルに適用されます。<br><br>分類名も分類値も、大文字と小文字を区別しません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられる制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><b>> 制約は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に「[!UICONTROL AMO ID]」と呼ばれます。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に「[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Placement ID] | 非推奨 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] キーワードを変更した場合にのみ必須です（行に a が含まれている場合を除く）キーワードを識別するのに十分なプロパティ列、または b)a &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] レスポンシブ検索広告の場合、広告データを編集または削除するには、広告 ID または AMO ID が必要です。 その他すべてのエンティティタイプの場合、AMO ID は、行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告ステータスを変更した場合にのみ必要です。[!UICONTROL AMO ID]&quot;.&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。</p><p><b>注意：</b> a) 広告プロパティの列（既存の広告のステータスを除く）または b) レスポンシブ検索広告のデータを編集する場合、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]をクリックした場合、新しい広告が作成され、既存の広告は変更されません。 </p> |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] サイトリンクを識別するのに十分なプロパティ列（a を含む場合を除く）または b) および&quot;[!UICONTROL AMO ID]&quot;.&quot; ただし、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]、およびプロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。</p><p><b>注意：</b> 既存のサイトリンクの「ステータス」以外のサイトリンクプロパティ列を編集し、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]をクリックした場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL Product Group ID] | 既存の製品グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に a が含まれている場合を除き、製品グループを変更または削除する場合にのみ必須です。a) 製品グループを識別するのに十分なプロパティ列、または b) および&quot;[!UICONTROL AMO ID]&quot;.&quot; |
| 場所 ID | 一意の [!DNL Microsoft Advertising] ロケーションターゲットの識別子。 ロケーションリストをダウンロードするには、 [!DNL Microsoft Advertising] 開発者ポータル [!DNL Microsoft Advertising] advertising アカウント資格情報。 ロケーションターゲットを変更または削除する場合にのみ必須です ( 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意の ID。 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルの RLSA ターゲットを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] ターゲットまたは除外を変更または削除する場合にのみ必須です ( 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL AMO ID] | （生成された一括送信シート内）同期されたAdobeに対してエンティティが生成した一意の識別子。 レスポンシブ検索広告の場合、広告 ID を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID はデータの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |
| [!UICONTROL EF Error Message] | （情報を提供するために、生成された一括送信シートに含まれます）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報を提供するために、生成された一括送信シートに含まれます）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL SE Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報を提供するために生成された一括送信シートに含まれます）広告が違反するGoogle広告ポリシーの名前とテキストを表示するためのプレースホルダーです。 |
| [!UICONTROL Retail Hash] | (Advanced Campaign Managementを使用して生成されたバルクシートの情報用に含まれます )Advanced (ACM) ビューを使用してアイテムが生成されたことを示す英数字のハッシュコード (f9639f40cdf56524b541e5dacf55a991 など )。 |

<table style="table-layout:auto">

[^1]: [!DNL Excel] は、ファイルを開くときに大きな数を科学的表記 (2115585666の 2.12E+09 など ) に変換します。 標準の表記で数字を表示するには、列内の任意のセルを選択し、数式バーの内側をクリックします。

## 各アカウントコンポーネントの作成、編集または削除に必要なフィールド {#bulksheet-fields-per-component-microsoft}

以下のセクションでは、特定のアカウントエンティティに関連するフィールドについて説明します。

>[!NOTE]
>
>1 つのフィールドをアクションに適用できない場合、そのフィールドに入力された値は無視されます。

### Campaign フィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | キャンペーンを作成するために必要です。 | キャンペーンに対する 1 日の支出制限。通貨記号や句読点の有無は問いません。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Channel Type] | キャンペーンを作成するために必要です。 |
| [!UICONTROL Delivery Method] | オプション |
| [!UICONTROL Campaign Priority] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Merchant ID] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Sales Country] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Product Scope Filter] | （買い物キャンペーン）オプション |
| [!UICONTROL DSA Domain Name] | タイプ a のキャンペーンを作成するために必要 ) &quot;[!UICONTROL DynamicSearchAds]&quot;または b) &quot;[!UICONTROL Search]」と入力します。 [!DNL ExperimentId] 要素が設定されていない ) |
| [!UICONTROL DSA Domain Language] | タイプ a のキャンペーンを作成するために必要 ) &quot;[!UICONTROL DynamicSearchAds]&quot;または b) &quot;[!UICONTROL Search]」と入力します。 [!DNL ExperimentId] 要素が設定されていない ) |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Landing Page Suffix] | <p>オプション |
| [!UICONTROL Budget Type] | キャンペーンを作成するために必要です。 |
| [!UICONTROL Device] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Campaign Status] | キャンペーンを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | 行に「[!UICONTROL AMO ID]」と呼ばれます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 広告グループフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Group Type] | 広告グループを作成するために必要です。 |
| [!UICONTROL Audience Target Method] | オーディエンス広告グループを作成する場合にのみ必要です。 |
| [!UICONTROL Ad Group Start Date] | オプション |
| [!UICONTROL Ad Group End Date] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Search Network Status] | （検索ネットワーク上のキャンペーンのみ）オプション |
| [!UICONTROL Languages] | オプション |
| [!UICONTROL Device] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Status] | 広告グループを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Ad Group ID] | 行に「[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キーワードフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
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
| [!UICONTROL Keyword Status] | キーワードを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Keyword ID] | キーワードを編集または削除する場合にのみ必須です（ただし、行に a が含まれている場合を除く）。キーワードを識別するのに十分なプロパティ列、または b)a &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 動的検索広告フィールド

>[!NOTE]
>
>サポートを作成できません。

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] 説明を編集するために必要です。 <b>注意：</b> この広告タイプで広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display Path 1] | フィールドの編集に必要です。 |
| [!UICONTROL Display Path 2] | フィールドの編集に必要です。 |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告のステータスを変更した場合にのみ必須です。b) または b)[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 製品（買い物）広告フィールド

ショッピング広告の作成について詳しくは、[実装方法 [!DNL Microsoft Advertising] ショッピングキャンペーン](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
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
| [!UICONTROL Ad ID] | 行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告のステータスを変更した場合にのみ必須です。b) または b)[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### レスポンシブ（マルチメディア）広告フィールド

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | レスポンシブ広告の場合 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] 広告を作成するにはが必要です。他の広告タイトルフィールドはすべてオプションです。 必須でないフィールドの既存の値を削除するには、 `[delete]` （括弧を含む） <b>注意：</b> この広告タイプで広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] 広告を作成する必要があり、 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。 <b>注意：</b> この広告タイプで広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Business Name] | 広告を作成または削除するために必要です。 |
| [!UICONTROL Call To Action] | 広告を作成するために必要です。 |
| [!UICONTROL Call To Action Language] | 広告を作成するために必要です。 |
| [!UICONTROL Base URL/Final URL] | 広告を作成するために必要です。 |
| [!UICONTROL Creative Type] | （オプション） |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告のステータスを変更した場合にのみ必須です。b) または b)[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### レスポンシブ検索広告フィールド

この広告タイプでは、[!UICONTROL Responsive Search Ad]」行を [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | レスポンシブ検索広告の場合、 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] 広告を作成するにはが必要です。その他の広告タイトルフィールドはすべてオプションです。 必須でないフィールドの既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] 広告を作成するにはが必要で、 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | オプション |
| [!UICONTROL Display Path 1] | オプション |
| [!UICONTROL Display Path 2] | オプション |
| [!UICONTROL Base URL/Final URL] | 広告を作成するために必要です。 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | 広告 ID を含めない限り、広告の編集または削除に必要です。 |

### テキスト広告フィールド

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

>[!NOTE]
>
>拡張テキスト広告は非推奨になりました。 既存のテキスト広告のみを削除できます。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | 読み取り専用 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] 読み取り専用 |
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
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | 広告 ID を含めない限り、データの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 動的検索ターゲット（自動ターゲット）フィールド

>[!NOTE]
>
>サポートを作成できません。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Auto Target Expression] | 必須。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Target Status] | ターゲットの削除に必要 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 買い物製品グループのフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Match Type] | 製品グループを作成するために必要です。 |
| [!UICONTROL Max CPC] | 製品グループを作成するために必要です。 |
| [!UICONTROL Parent Product Groupings] | 必須 |
| [!UICONTROL Product Grouping] | 必須 |
| [!UICONTROL Partition Type] | 製品グループを作成するために必要です。 |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Product Group Status] | 製品グループの削除にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Product Group ID] | 行に a が含まれている場合を除き、製品グループを変更または削除する場合にのみ必須です。a) 製品グループを識別するのに十分なプロパティ列、または b) および&quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キャンペーンレベルのサイトリンクフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| 説明行 1 | オプション |
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
| [!UICONTROL Sitelink ID] | サイトリンクを識別するのに十分なプロパティ列（a を含む場合を除く）または b) および&quot;[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]  およびプロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。<br><br><b>注意：</b> 既存のサイトリンクの「ステータス」以外のサイトリンクプロパティ列を編集し、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]をクリックした場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 場所のターゲットフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | ターゲットの作成に必要 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | ロケーションターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | キャンペーン ID を含めない限り、データの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスターゲットフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットを削除するために必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必須です。 キャンペーンレベルのデバイスターゲットには適用されません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション広告グループレベルのデバイスターゲットにのみ適用できます。 |
| [!UICONTROL AMO ID] | デバイスターゲット ID を含めない限り、データの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キャンペーンレベルおよび広告グループレベルの RLSA ターゲットフィールド

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-microsoft).&quot;

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットの場合は必須です。 キャンペーンレベルのターゲットには適用されません。 |
| [!UICONTROL Audience] | 新しいターゲットを作成するために必要です。 |
| [!UICONTROL Target Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL RLSA Target Status] | ターゲットを削除するために必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション広告グループレベルのターゲットにのみ適用できます。 |
| [!UICONTROL RLSA Target ID] | ターゲットを変更または削除する場合にのみ必要です ( 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL AMO ID] | RLSA ターゲット ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

>[!MORELIKETHIS]
>
>* [付録 — バルクシートエラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルのダウンロード/作成](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正済みエラーファイルのアップロード](../bulksheet-upload.md)
