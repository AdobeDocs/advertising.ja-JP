---
title: バルクシートファイルのダウンロードと作成
description: 広告ネットワークのアカウントデータをダウンロードしてバルクシートファイルを作成する方法を説明します。
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# バルクシートファイルのダウンロードと作成

1 つ以上のアカウントに対してカスタム設定を使用して、バルクシートを作成できます [サポートされる広告ネットワーク](bulksheet-about.md#bulksheet-functionality-by-network). バルクシートには、検索、ソーシャル、Commerce内のデータが含まれます。

同期されたキャンペーンの場合は、データをダウンロードする前に広告ネットワークと同期して、広告ネットワーク側での最近のデータ変更が含まれていることを確認するオプションがあります。 すべての広告ネットワークについて、オプションで、ファイルに含める新しいクリック追跡 URL を生成できます。

>[!NOTE]
>
>以下の手順でも可能です [キャンペーン管理ビューで表示される列に基づいてバルクシートファイルを作成](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. メインメニューで、 **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. ツールバーで、 **[!UICONTROL Download Bulksheet]**.

1. を指定 [バルクシート設定](#bulksheet-download-settings):

1. 日 **[!UICONTROL Selections]** タブをクリックし、フィールドに情報を入力または選択します。

1. （任意） **[!UICONTROL Rows and Columns]** タブで、バルクシートに行を含めるアカウントコンポーネントとコンポーネントステータスを指定し、選択した各コンポーネントに含める列を指定します。

   使用可能なバルクシート行のリストについては、「」を参照してください[広告ネットワーク別バルクシート行](#bulksheet-rows-by-ad-network).」と入力します。

1. （任意） **[!UICONTROL Filters]** タブをクリックし、バルクシートに含める特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、プレースメントおよびその他のエンティティの条件を指定します。

   1. パラメーター（エンティティ名または ID、または広告、キーワード、プレースメントの任意の要素）を選択し、演算子を選択してから、該当する値を入力します。 例えば、のヘッドラインに「shoes」を含む広告のみを返すには、次のようにします [!DNL Google Ads] アカウント、選択 *見出し*&#x200B;を選択 *[!UICONTROL contains]*&#x200B;を入力し、 `shoes` 入力フィールドに移動します。

   1. （追加のフィルターを適用するには）追加のフィルターごとに、 **[!UICONTROL +Add Filter]**&#x200B;を選択 **[!UICONTROL AND]** または **[!UICONTROL OR]**&#x200B;を選択し、広告要素またはキーワード、および演算子を選択してから、該当する値を入力します。

1. クリック **[!UICONTROL Download]**.

タスクが開始されると、ウィンドウには通知が表示されますが、開いたままなので、必要に応じて追加のバルクシートを引き続き作成できます。 選択した新しいアカウントに適用できる、指定したフィルターと除外は保持されます。 タスクが開始されると、ファイルがバルクシート ビューに一覧表示されます。 ファイルを作成すると、そのファイルへのリンクが記載されたメール通知が届きます。コンパイルするデータの量によっては、通知に数分以上かかることがあります。 ただし、ファイルの生成に失敗すると、エラーファイルがバルクシート ビューに表示され、エラーファイルへのリンクを含むメール通知が届きます。

## バルクシートダウンロード設定 {#bulksheet-download-settings}

| タブ | パラメーター | 説明 |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | データをアップロードするアカウント、キャンペーンまたは広告グループ：<ul><li>アカウントとそのすべてのキャンペーンおよび広告グループを選択するには、アカウント名の横にあるチェックボックスをオンにし、>> をクリックしてに移動します [!UICONTROL Selected Filters] 列。</li><li>個々のキャンペーンまたは広告グループを選択するには、アカウントの横のをクリックして展開し、（必要に応じて）「キャンペーンの次へ」をクリックして展開し、キャンペーンまたは広告グループ名の横にあるチェックボックスを選択して、「>>」をクリックし、キャンペーンを「 [!UICONTROL Selected Filters] 列。 例えば、アカウント 1 のキャンペーン 1 のデータのみを取得するには、アカウント 1 を展開し、キャンペーン 1 の横にあるチェックボックスをオンにしてに移動します [!UICONTROL Selected Filters] 列。</li></ul><b>メモ：</b><ul><li>1 つのバルクシートを複数の広告ネットワーク内の複数のアカウントに適用できます。 広告ネットワーク固有の列は、バルクシート内で、広告ネットワーク名でラベル付けされます（「携帯電話会社（Google広告）」など）。</li><li>項目のコンポーネントの種類を確認するには、その上にカーソルを置きます。</li><li>キャンペーンの場合、広告ネットワーク名の最初の文字は、アカウント名の後の括弧内に含まれます（ [!DNL Google Ads] アカウント）。</li><li>デフォルトでは、アクティブで有効なアカウントとそのアクティブなコンポーネントのみが表示されます。 一時停止および削除されたコンポーネントを表示するには、をクリックします。 ![下矢印キー](/help/search-social-commerce/assets/arrow-down-expand.png "下矢印キー") 次の [!UICONTROL Show] を選択し**す。[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | （任意） トラッキングテンプレートを使用するアカウントのトラッキングテンプレートとランディングページサフィックス（該当する広告ネットワークの場合）、またはトラッキングコードが埋め込まれた宛先 URL （キーワード、広告、配置、サイトリンクの場合）を宛先 URL を使用するアカウントに含めます [!DNL Google Ads] バルクシートの製品グループ。 デフォルトでは、このオプションが選択されています。<br><br>このオプションを選択すると、のパラメーターに従って URL が生成されます [!UICONTROL Campaign Tracking] アカウント設定またはキャンペーン設定の「」セクション。 デフォルトでは、トラッキング URL が既に存在する場合、新しい URL が必要ない限り（キーワード一致タイプ、広告テキスト、アカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。<br><br><b>メモ：</b><ul><li>Adobe Advertising主が広告コンバージョントラッキングを使用し、関連するアカウントがトラッキング URL を自動生成してアップロードするように設定されていない場合、ベース URL が変更されたときは新しいトラッキング URL を生成する必要があります。</li><li>このオプションを選択しない場合でも、後でファイルをアップロードまたは投稿するときにトラッキング URL を生成できます。</li></ul> |
| | [!UICONTROL Perform Pre-sync] | （任意）は、検索、ソーシャル、Commerceに対し、そのファイルを指定したキャンペーンと同期してすべてのデータが同じであることを確認するように指示します。 デフォルトでは、このオプションは選択されていません。<br><b>注意：</b> 検索、ソーシャル、Commerceは、1 日に 1 回、広告ネットワーク上で新しいキャンペーンを検出するたびに、また検索、ソーシャル、Commerce内からキャンペーンデータを変更するたびに、自動的に広告ネットワークと同期します。 キャンペーンまたはアカウントデータに対する最近の変更が広告ネットワークで直接行われた、または広告ネットワークのデスクトップエディターを使用して行われたと思われる場合は、このオプションを選択します。 このオプションを選択すると、バルクシートの作成に時間がかかります。 |
| | [!UICONTROL Bulksheet Name] | 新しいバルクシートの名前とファイルの種類。 デフォルトでは、ファイルはタブ区切り値の形式で作成され、次のいずれかの名前が付けられます。<ul><li>（広告ネットワークのすべてのアカウント用） `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（単一アカウントの場合） `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（複数アカウントの場合） `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>ファイルの名前は変更できます。 名前に次の文字を含めることはできません： `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>必要に応じて、ファイルタイプを変更します。 次のオプションがあります *[!UICONTROL .tsv]* （タブ区切り値の場合）、 *[!UICONTROL .txt]* （Unicode 準拠 ASCII テキストの場合）、 *[!UICONTROL .csv]* （コンマ区切り値の場合）、 *[!UICONTROL .zip]* （圧縮された ZIP 形式の場合、TSV ファイルに解凍されます）。<br><br><b>ヒント：</b> 国際化対応の文字を含むバルクシートの場合は、TSV 形式または TXT 形式を使用します。 |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | エントリごとに 1 つのデータ行を持つバルクシートに含めるエンティティと、それに対応するステータス。 例えば、アクティブなキャンペーンを含める場合、バルクシートにはアクティブなキャンペーンごとに 1 行が含まれます。 選択したステータスを持つ、選択したエンティティのみが含まれます。 デフォルトは、指定された広告ネットワークに基づいて事前に選択されています。 デフォルトでは、選択したエンティティのアクティブなインスタンスのみが含まれます。 使用可能なバルクシート行のリストについては、「」を参照してください[広告ネットワーク別バルクシート行](#bulksheet-rows-by-ad-network).」と入力します。<br><br>エンティティを追加または削除するには、エンティティの横にあるチェックボックスをオンまたはオフにします。 エンティティのステータスを追加または削除するには、「ステータス」 メニューの横にあるをクリックし、エンティティの横にあるチェックボックスをオンまたはオフにします。 |
| | [!UICONTROL Cascading Status Hierarchy] | AND 操作を使用して、子エンティティの範囲を、指定された親エンティティのステータスを持つエンティティにフィルタリングします。 例えば、「アクティブなキャンペーン」、「アクティブな広告グループ」、および「アクティブなキーワード」を選択した場合、バルクシートにはアクティブなキャンペーンのアクティブな広告グループのアクティブなキーワードのみが含まれます。<br><br>このオプションを選択しない場合、親ステータスは考慮されず、フィルターは OR 操作を使用します。 例えば、「アクティブなキャンペーン」、「アクティブな広告グループ」および「アクティブなキーワード」を選択した場合、バルクシートには、親キャンペーンのステータスに関係なく、すべてのアクティブなキャンペーン、すべてのアクティブな広告グループ、親キャンペーンと広告グループのステータスに関係なく、すべてのアクティブなキーワードが含まれます。 |
| | [!UICONTROL Bulksheet Columns] | ダウンロードしたバルクシートファイルに含める列：<ul><li>*[!UICONTROL AMO ID]*: （「の場合」に必須[!UICONTROL SE ID]&#39;&#39;が選択されていません）次を含む [!DNL Adobe] – 各エンティティ/行に対して生成された一意の id。 検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、広告ネットワークには投稿しません。 後で、を使用してエンティティのデータを編集できます [!UICONTROL AMO ID] エンティティ ID や親エンティティ ID ではなく、識別子として使用します。</li><li>*[!UICONTROL SE ID]*: （「の場合」に必須[!UICONTROL AMO ID]&#39;&#39;が選択されていない）は、含まれている各列とその親エンティティの広告ネットワークの一意の ID を含みます。 後で、を使用して任意のエンティティのデータを編集する場合 [!UICONTROL SE ID] 識別子として、親エンティティの行（とその行を含む）も含める必要があります [!UICONTROL SE ID] 値）。</li><li>*[!UICONTROL Platform]*：が含まれます [!UICONTROL Platform column] 各行の先頭に、広告プラットフォームを示します（「Baidu」など）。</li><li>*[!UICONTROL Acct Name]*: （「の場合」に必須[!UICONTROL AMO ID]``が選択されていません）各エンティティ/行の広告ネットワークアカウント名が含まれます。</li><li>\[ 含める列\]：すべての列、なし、または選択した各エンティティに関連する選択した列のみを [!UICONTROL Bulksheet Rows] セクション。 エンティティに関連する個々の列を表示するには、をクリックします ![右矢印](/help/search-social-commerce/assets/compressed-item.png "右矢印") エンティティ名の隣。 デフォルトでは、選択した各エンティティ行に関連するすべての列が含まれます。 任意のエンティティの横または個々の列の横にあるチェックボックスの選択を解除して、バルクシートから除外します。</li></ul><br><br><b>ヒント：</b> バルクシート ファイルの各行でアイテムを識別するのに十分な列を含めてください。 例えば、にキーワード行を含めるとします [!UICONTROL Bulksheet Rows] セレクターを使用しますが、キーワード関連の列はすべて除外されます。 結果のバルクシートには、キーワードインスタンスごとに 1 行が含まれます。 ただし、キーワード関連の列は含まれず（AMO ID や SE ID も含まれない）、特定の行に関連するキーワードインスタンスを識別できず、適切な ID 列と値を手動で追加しない限り、バルクシートを使用してデータを更新できません。 |
| [!UICONTROL Filters] | | バルクシートに含める特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、プレースメントの条件：<ol><li>パラメーター（エンティティ名または ID、またはクリエイティブ、キーワード、プレースメントの任意の要素）を選択し、演算子を選択してから、該当する値を入力します。<br>例えば、のヘッドラインに「shoes」を含む広告のみを返すには、次のようにします [!DNL Google Ads] アカウント、選択 *[!UICONTROL Headline]*&#x200B;を選択 *[!UICONTROL contains]*&#x200B;を入力し、 `shoes` 入力フィールドに移動します。</li><li>（追加のフィルターを適用するには）追加のフィルターごとに、 **[!UICONTROL +Add Filter]**&#x200B;を選択 **[!UICONTROL AND]** または **[!UICONTROL OR]**&#x200B;を選択し、広告要素またはキーワード、および演算子を選択してから、該当する値を入力します。</li></ul> |

## 広告ネットワーク別バルクシート行 {#bulksheet-rows-by-ad-network}

| バルクシート行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | ヤンデックス | 備考 |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Adgroup] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Creative] *または* [!UICONTROL Creative (except RSA)] | はい | はい | はい | — | — | はい | はい | はい | はい | （[!DNL Google  Ads]）で利用可能なレスポンシブ検索広告以外のすべての広告タイプに使用します [!UICONTROL Responsive Search Ad] 行。 |
| [!UICONTROL Responsive Search Ad] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | はい | はい | はい | はい | はい | — | はい | はい | はい | 負でないキーワードにのみ使用します。 キャンペーンレベルまたは広告グループレベルで作成されたネガティブキーワードを表示するには、 [!UICONTROL Campaign Negative Keyword] または [!UICONTROL Adgroup Negative Keyword] 行（使用可能な場合）。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | はい | — | — | — | — | — |
| [!UICONTROL Placement] | — | はい | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | はい | はい | — | — | — | — | — | — | 広告グループの動的検索ターゲットに使用します。 |
| [!UICONTROL Shopping Product Group] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | はい | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Campaign Negative Keyword] | はい | はい | はい | — | — | — | はい | はい | — | キャンペーンレベルまたは広告グループレベルでのみ作成されたネガティブキーワードに使用します。 負でないキーワードを表示するには、を使用します。 [!UICONTROL Keyword] 行（使用可能な場合）。 |
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
>* [バルクシートを使用した Campaign データの管理について](bulksheet-about.md)
>* [バルクシートまたは修正されたエラーファイルの投稿](bulksheet-post.md)
>* [バルクシートファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシートファイルのエクスポート](bulksheet-export.md)
