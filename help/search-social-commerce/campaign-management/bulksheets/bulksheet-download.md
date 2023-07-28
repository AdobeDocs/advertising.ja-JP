---
title: バルクシートファイルをダウンロード/作成する
description: 広告ネットワークのアカウントデータをダウンロードして、バルクシートファイルを作成する方法を説明します。
exl-id: 42558276-b930-49de-90a0-445433ee66b9
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1756'
ht-degree: 0%

---

# バルクシートファイルをダウンロード/作成する

1 つ以上のアカウントに対して 1 つ以上のカスタム設定を使用して、一括送信シートを作成できます [サポートされる広告ネットワーク](bulksheet-about.md#bulksheet-functionality-by-network). バルクシートには、検索、ソーシャル、コマース内のデータが含まれます。

同期されたキャンペーンの場合は、オプションで、データをダウンロードする前に広告ネットワークと同期して、広告ネットワーク側での最新のデータの変更が確実に含まれるようにすることができます。 すべての広告ネットワークについて、オプションで、ファイルに含める新しいクリック追跡 URL を生成できます。

>[!NOTE]
>
>また、 [キャンペーン管理ビューの表示される列に基づいてバルクシートファイルを作成する](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. メインメニューで、 **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. ツールバーで、 **[!UICONTROL Download Bulksheet]**.

1. 次を指定します。 [bulksheet 設定](#bulksheet-download-settings):

1. 次の日： **[!UICONTROL Selections]** 「 」タブで、「 」フィールドに情報を入力または選択します。

1. （オプション） **[!UICONTROL Rows and Columns]** タブで、バルクシートに行を含めるアカウントコンポーネントとコンポーネントステータスを指定し、選択した各コンポーネントに含める列を指定します。

   使用可能なバルクシート行の一覧については、[広告ネットワーク別のバルクシート行](#bulksheet-rows-by-ad-network).&quot;

1. （オプション） **[!UICONTROL Filters]** 」タブをクリックし、バルクシートに含める特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、プレースメントおよびその他のエンティティの条件を指定します。

   1. パラメーター（エンティティ名、ID、または広告、キーワード、プレースメントの任意の要素）を選択し、演算子を選択して、適切な値を入力します。 例えば、 [!DNL Google Ads] アカウント、選択 *見出し*&#x200B;を選択します。 *[!UICONTROL contains]*&#x200B;を入力し、 `shoes` を入力フィールドに入力します。

   1. （追加のフィルターを適用する場合）追加のフィルターごとに、 **[!UICONTROL +Add Filter]**&#x200B;を選択します。 **[!UICONTROL AND]** または **[!UICONTROL OR]**、広告要素またはキーワードと演算子を選択し、適切な値を入力します。

1. クリック **[!UICONTROL Download]**.

タスクが開始すると、ウィンドウに通知が表示されますが、ウィンドウは開いたままなので、必要に応じて追加のバルクシートを作成し続けることができます。 選択した新規アカウントに適用できる、指定したフィルターと除外はすべて保持されます。 タスクが開始されると、ファイルが Bulksheets ビューに一覧表示されます。 ファイルが作成されると、そのファイルへのリンクが記載された電子メール通知が届きます。コンパイルされるデータの量によっては、通知に数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルが Bulksheets ビューに表示され、エラーファイルへのリンクを含む電子メール通知が届きます。

## Bulksheet のダウンロード設定 {#bulksheet-download-settings}

| タブ | パラメーター | 説明 |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | データのアップロード先となるアカウント、キャンペーンまたは広告グループ：<ul><li>アカウントとそのすべてのキャンペーンおよび広告グループを選択するには、アカウント名の横にあるチェックボックスを選択し、 /> をクリックして、 [!UICONTROL Selected Filters] 列。</li><li>個々のキャンペーンまたは広告グループを選択するには、アカウントの横にある「 」をクリックして展開し、（必要に応じて）キャンペーンの横にある「 」をクリックして展開し、キャンペーンまたは広告グループ名の横にあるチェックボックスを選択して、「>>」をクリックして [!UICONTROL Selected Filters] 列。 例えば、アカウント 1 のキャンペーン 1 のデータのみを取得するには、「アカウント 1」を展開し、「キャンペーン 1」の横のチェックボックスをオンにして、次に [!UICONTROL Selected Filters] 列。</li></ul><b>メモ：</b><ul><li>1 つの一括送信シートは、複数の広告ネットワーク内の複数のアカウントに適用される場合があります。 広告ネットワーク固有の列には、広告ネットワーク名 (「携帯電話会社 (Google広告 )」など ) の付いたラベルが一括送信シートで付けられます。</li><li>項目の種類を確認するには、その上にカーソルを置きます。</li><li>キャンペーンの場合、広告ネットワーク名の最初の文字は、アカウント名の後の括弧内にあります ( 例： [!DNL Google Ads] アカウント )。</li><li>デフォルトでは、アクティブで有効なアカウントとそのアクティブなコンポーネントのみが表示されます。 一時停止および削除されたコンポーネントを表示するには、 ![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印") 次の [!UICONTROL Show] を選択し、「**[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | （オプション）トラッキングテンプレートを持つアカウント、またはリンク先 URL のアカウント、キーワード、広告、プレースメント、サイトリンク、 [!DNL Google Ads] bulksheet の製品グループです。 デフォルトでは、このオプションが選択されています。<br><br>このオプションを選択すると、 [!UICONTROL Campaign Tracking] 」セクションに追加されます。 デフォルトでは、トラッキング URL が既に存在する場合、新しい URL が必要な場合（キーワードの一致タイプ、広告テキスト、アカウントのトラッキングパラメーターが変更された場合など）以外は再生成されません。<br><br><b>メモ：</b><ul><li>広告主がAdobe Advertisingコンバージョントラッキングを使用し、トラッキング URL を自動的に生成してアップロードするようにアカウントが設定されていない場合、ベース URL が変更されたときに新しいトラッキング URL を生成する必要があります。</li><li>このオプションを選択しない場合でも、後でファイルのアップロード時または投稿時にトラッキング URL を生成できます。</li></ul> |
| | [!UICONTROL Perform Pre-sync] | （オプション）Search, Social, &amp; Commerce に対し、指定されたキャンペーンとファイルを同期してすべてのデータが同じであることを確認するよう指示します。 デフォルトでは、このオプションは選択されていません。<br><b>注意：</b> Social、Commerce は、広告ネットワーク上で新しいキャンペーンを検出するたびに、Search、Social、および Commerce 内でキャンペーンデータを変更するたびに、1 日 1 回広告ネットワークと自動的に同期します。 キャンペーンまたはアカウントデータに対する最近の変更が、広告ネットワークで直接行われた、または広告ネットワークのデスクトップエディターを使用して行われたと考える場合に、このオプションを選択します。 このオプションを選択すると、バルクシートの作成に時間がかかります。 |
| | [!UICONTROL Bulksheet Name] | 新しいバルクシートの名前とファイルタイプ。 デフォルトでは、ファイルはタブ区切りの値形式で作成され、次のいずれかの名前が付けられます。<ul><li>（広告ネットワークのすべてのアカウントの場合） `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（単一アカウントの場合） `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（複数のアカウントの場合） `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>ファイルの名前は変更できます。 名前に次の文字を含めることはできません。 `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>必要に応じて、ファイルタイプを変更します。 オプションは次のとおりです。 *[!UICONTROL .tsv]* （タブ区切り値の場合）、 *[!UICONTROL .txt]* （Unicode 準拠の ASCII テキストの場合）、 *[!UICONTROL .csv]* （コンマ区切り値の場合）または *[!UICONTROL .zip]* （圧縮 ZIP 形式の場合。TSV ファイルに解凍します）。<br><br><b>ヒント：</b> 国際文字を含むバルクシートの場合は、TSV または TXT 形式を使用します。 |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | バルクシートに含めるエンティティとそれに対応するステータス。エントリごとに 1 つのデータ行が含まれます。 例えば、アクティブなキャンペーンを含めると、バルクシートにはアクティブなキャンペーンごとに 1 行が含まれます。 選択したステータスを持つ選択したエンティティのみが含まれます。 デフォルトは、指定した広告ネットワークに基づいて事前に選択されています。 デフォルトでは、選択したエンティティのアクティブなインスタンスのみが含まれます。 使用可能なバルクシート行の一覧については、[広告ネットワーク別のバルクシート行](#bulksheet-rows-by-ad-network).&quot;<br><br>エンティティを追加または削除するには、エンティティの横にあるチェックボックスをそれぞれオンまたはオフにします。 エンティティのステータスを追加または削除するには、ステータスメニューの横のをクリックし、エンティティの横にあるチェックボックスをそれぞれオンまたはオフにします。 |
| | [!UICONTROL Cascading Status Hierarchy] | AND 演算子を使用して、子エンティティの範囲を、指定された親エンティティのステータスを持つエンティティにフィルターします。 例えば、「アクティブなキャンペーン」、「アクティブな広告グループ」、「アクティブなキーワード」を選択した場合、一括送信シートにはアクティブなキャンペーン内のアクティブな広告グループ内のアクティブなキーワードのみが含まれます。<br><br>このオプションを選択しない場合、親ステータスは考慮されず、フィルターで OR 演算子が使用されます。 例えば、「Active Campaign」、「Active Adgroup」および「Active Keyword」を選択した場合、親キャンペーンのステータスに関係なく、すべてのアクティブな広告グループと、親キャンペーンと広告グループのステータスに関係なく、すべてのアクティブなキーワードが一括送信シートに含まれます。 |
| | [!UICONTROL Bulksheet Columns] | ダウンロードした一括送信シートファイルに含める列：<ul><li>*[!UICONTROL AMO ID]*: （&quot;の場合は必須）[!UICONTROL SE ID]&quot;が選択されていない ) [!DNL Adobe] — 各エンティティ/行に対して生成される一意の ID。 検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには投稿しません。 後で、 [!UICONTROL AMO ID] エンティティ ID や親エンティティ ID ではなく、を識別子として使用するようになりました。</li><li>*[!UICONTROL SE ID]*: （&quot;の場合は必須）[!UICONTROL AMO ID]」が選択されていない場合 ) 含まれる各列とその親エンティティに対する広告ネットワークの一意の識別子を含めます。 後で、 [!UICONTROL SE ID] を識別子として指定する場合は、親エンティティの行（親エンティティの行を含む）も含める必要があります [!UICONTROL SE ID] の値 ) を参照してください。</li><li>*[!UICONTROL Platform]*：を含みます。 [!UICONTROL Platform column] 各行の先頭に、広告プラットフォーム（「Baidu」など）を示します。</li><li>*[!UICONTROL Acct Name]*: （&quot;の場合は必須）[!UICONTROL AMO ID]」が選択されていない場合 ) 各エンティティや行の広告ネットワークアカウント名が含まれます。</li><li>\[ 含める列\]：選択した各エンティティに関連するすべての列、なし列または選択した列のみを [!UICONTROL Bulksheet Rows] 」セクションに入力します。 エンティティに関連する個々の列を表示するには、 ![右向き矢印](/help/search-social-commerce/assets/compressed-item.png "右向き矢印") エンティティ名の横に表示されます。 デフォルトでは、選択したエンティティ行ごとに、すべての関連する列が含まれます。 エンティティの横または個々の列の横にあるチェックボックスの選択を解除して、バルクシートから除外します。</li></ul><br><br><b>ヒント：</b> bulksheet ファイルの各行の項目を識別するのに適した列を含めてください。 例えば、 [!UICONTROL Bulksheet Rows] セレクターを使用することもできますが、キーワード関連の列はすべて除外されます。 結果の一括送信シートには、各キーワードインスタンスに対して 1 つの行が含まれます。 ただし、キーワード関連の列は含まれないので（AMO ID や SE ID も含まれない）、特定の行に関連するキーワードインスタンスを識別できず、適切な ID 列と値を手動で追加しない限り、一括シートを使用してデータを更新できません。 |
| [!UICONTROL Filters] | | バルクシートに含める特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、プレースメントの条件：<ol><li>パラメーター（エンティティ名、ID、またはクリエイティブ、キーワード、プレースメントの任意の要素）を選択し、演算子を選択して、適切な値を入力します。<br>例えば、 [!DNL Google Ads] アカウント、選択 *[!UICONTROL Headline]*&#x200B;を選択します。 *[!UICONTROL contains]*&#x200B;を入力し、 `shoes` を入力フィールドに入力します。</li><li>（追加のフィルターを適用する場合）追加のフィルターごとに、 **[!UICONTROL +Add Filter]**&#x200B;を選択します。 **[!UICONTROL AND]** または **[!UICONTROL OR]**、広告要素またはキーワードと演算子を選択し、適切な値を入力します。</li></ul> |

## 広告ネットワーク別のバルクシート行 {#bulksheet-rows-by-ad-network}

| Bulksheet 行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | メモ |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Adgroup] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Creative] *または* [!UICONTROL Creative (except RSA)] | はい | はい | はい | — | — | はい | はい | はい | はい | ([!DNL Google  Ads]) で使用できるレスポンシブ検索広告を除く、すべての広告タイプに使用します。レスポンシブ検索広告は、 [!UICONTROL Responsive Search Ad] 行。 |
| [!UICONTROL Responsive Search Ad] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | はい | はい | はい | はい | はい | — | はい | はい | はい | 除外以外のキーワードに対してのみ使用します。 キャンペーンまたは広告グループレベルで作成された除外キーワードを確認するには、 [!UICONTROL Campaign Negative Keyword] または [!UICONTROL Adgroup Negative Keyword] 行が使用可能な場合は表示されます。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | はい | — | — | — | — | — |
| [!UICONTROL Placement] | — | はい | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | はい | はい | — | — | — | — | — | — | 広告グループの動的検索ターゲットに使用します。 |
| [!UICONTROL Shopping Product Group] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | はい | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Campaign Negative Keyword] | はい | はい | はい | — | — | — | はい | はい | — | キャンペーンまたは広告グループレベルで作成された除外キーワードに対してのみ使用します。 除外されないキーワードを表示するには、 [!UICONTROL Keyword] 行が使用可能な場合は表示されます。 |
| [!UICONTROL Campaign Negative Website] | — | はい | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Adgroup Site Link] | — | はい | — | — | — | — | — | はい | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | はい | — |
| [!UICONTROL Adgroup Negative Keyword] | はい | はい | はい | — | — | — | はい | はい | — | — |
| [!UICONTROL Adgroup Negative Website] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | はい | はい | はい | — | — | — | はい | はい | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Campaign Device Target] | — | はい | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Adgroup Device Target] | — | はい | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Campaign RLSA Target] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | はい | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | はい | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [バルクシートの投稿または修正されたエラーファイル](bulksheet-post.md)
>* [バルクシートファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシートファイルのエクスポート](bulksheet-export.md)
