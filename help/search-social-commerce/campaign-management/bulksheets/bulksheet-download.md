---
title: バルクシートファイルのダウンロード/作成
description: 広告ネットワークのアカウントデータをダウンロードして、バルクシートファイルを作成する方法について説明します。
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/2naHFI92HnVZ7Vi1gRnTtBtI1PbfTmfkeLQGRJJCSgs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1759
ht-degree: 0%

---

# バルクシートファイルのダウンロード/作成

1つ以上の[ サポートされている広告ネットワーク ](bulksheet-about.md#bulksheet-functionality-by-network)で、1つ以上のアカウントのカスタム設定を使用してバルクシートを作成できます。 Bulksheetsには、Search, Social, &amp; Commerce内のデータが含まれます。

同期済みキャンペーンの場合は、データをダウンロードする前にオプションで広告ネットワークと同期して、広告ネットワーク側の最近のデータ変更を確実に含めることができます。 すべての広告ネットワークに対して、オプションで、ファイルに含める新しいクリックトラッキング URLを生成できます。

>[!NOTE]
>
>キャンペーン管理ビューで表示されている列に基づいてバルクシート ファイルを[作成することもできます](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. ツールバーで、**[!UICONTROL Download Bulksheet]**&#x200B;をクリックします。

1. [ バルクシート設定](#bulksheet-download-settings)を指定します。

1. 「**[!UICONTROL Selections]**」タブで、フィールドに情報を入力または選択します。

1. （オプション）「**[!UICONTROL Rows and Columns]**」タブをクリックし、バルクシートに行を含めるアカウントコンポーネントとコンポーネントステータスを指定し、選択した各コンポーネントに含める列を指定します。

   使用可能なバルクシート行のリストについては、「[広告ネットワーク別バルクシート行](#bulksheet-rows-by-ad-network)」を参照してください。

1. （オプション）「**[!UICONTROL Filters]**」タブをクリックし、バルクシートに含める特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、プレースメント、その他のエンティティの条件を指定します。

   1. パラメーター（エンティティ名またはID、または広告、キーワード、プレースメントの任意の要素）を選択し、演算子を選択して、該当する値を入力します。 例えば、[!DNL Google Ads] アカウントの見出しに「靴」が付いた広告のみを返すには、*見出し*&#x200B;を選択し、*[!UICONTROL contains]*&#x200B;を選択して、入力フィールドに`shoes`と入力します。

   1. （追加のフィルターを適用するには）追加の各フィルターについて、**[!UICONTROL +Add Filter]**&#x200B;をクリックし、**[!UICONTROL AND]**&#x200B;または&#x200B;**[!UICONTROL OR]**&#x200B;を選択し、広告要素またはキーワードと演算子を選択して、該当する値を入力します。

1. **[!UICONTROL Download]**&#x200B;をクリックします。

タスクが開始されると、ウィンドウに通知が表示されますが、開いたままなので、必要に応じて追加のバルクシートを作成し続けることができます。 選択した新規顧客に適用できる、指定したフィルターと除外事項は保持されます。 タスクが開始されると、ファイルが一括処理ビューに表示されます。 ファイルを作成すると、ファイルへのリンクが記載されたメール通知が届きます。編集するデータ量によっては、通知に数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルが一括処理ビューに表示され、エラーファイルへのリンクを含むメール通知が届きます。

## バルクシートのダウンロード設定 {#bulksheet-download-settings}

| Tab | パラメーター | 説明 |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | データをアップロードするアカウント、キャンペーン、または広告グループ：<ul><li>アカウントとそのすべてのキャンペーンおよび広告グループを選択するには、アカウント名の横にあるチェックボックスを選択し、>>をクリックして[!UICONTROL Selected Filters]列に移動します。</li><li>個々のキャンペーンまたは広告グループを選択するには、アカウントの横にあるをクリックして展開し（必要に応じて）、キャンペーンの横にあるをクリックして展開し、キャンペーンまたは広告グループ名の横にあるチェックボックスを選択し、>>をクリックして[!UICONTROL Selected Filters]列に移動します。 例えば、アカウント 1のキャンペーン 1のデータのみを取得するには、アカウント 1を展開し、キャンペーン 1の横にあるチェックボックスを選択して、[!UICONTROL Selected Filters]列に移動します。</li></ul><b> メモ：</b><ul><li>単一のバルクシートが、複数の広告ネットワーク内の複数のアカウントに適用される場合があります。 広告ネットワーク固有の列には、広告ネットワーク名（「Mobile Carriers （Google Ads）」など）が付いたバルクシートでラベル付けされます。</li><li>項目の種類を確認するには、項目の上にカーソルを置きます。</li><li>キャンペーンの場合、広告ネットワーク名の最初の文字は、アカウント名の後に括弧で囲まれます（[!DNL Google Ads] アカウントの「Acme Realty （G）」など）。</li><li>デフォルトでは、アクティブなアカウントと有効なアカウントとそのアクティブなコンポーネントのみが一覧表示されます。 一時停止および削除されたコンポーネントを表示するには、![の横にある](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")下向き矢印[!UICONTROL Show]をクリックし、[!UICONTROL All]**選択します。 |
| | [!UICONTROL Generate Tracking URLs] | （オプション）トラッキングテンプレートを含むアカウントにトラッキングテンプレートとランディングページのサフィックス（該当する広告ネットワークの場合）、またはターゲット URLを含むアカウントにトラッキングコードが埋め込まれた宛先URL （キーワード、広告、プレースメント、サイトリンク、およびバルクシートの[!DNL Google Ads]製品グループ）を含みます。 デフォルトでは、このオプションが選択されています。<br><br>このオプションを選択すると、アカウント設定またはキャンペーン設定の[!UICONTROL Campaign Tracking] セクションのパラメーターに従ってURLが生成されます。 デフォルトでは、トラッキング URLが既に存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードの一致タイプ、広告テキスト、アカウントのトラッキングパラメーターが変更された場合など）。<br><br><b> メモ：</b><ul><li>広告主がAdobe Advertising コンバージョントラッキングを使用しており、関連するアカウントがトラッキング URLを自動生成してアップロードするように設定されていない場合は、ベース URLが変更されたときに新しいトラッキング URLを生成する必要があります。</li><li>このオプションを選択しない場合でも、後でファイルをアップロードまたは投稿するときにトラッキング URLを生成できます。</li></ul> |
| | [!UICONTROL Perform Pre-sync] | （オプション）すべてのデータが同じであることを確認するために、Search、Social、Commerceで指定されたキャンペーンとファイルを同期するように指示します。 デフォルトでは、このオプションは選択されていません。<br><b>注：</b>検索、ソーシャル、Commerceは、1日1回、広告ネットワーク上で新しいキャンペーンを検出するたびに、検索、ソーシャル、Commerce内からキャンペーンデータを変更するたびに、広告ネットワークと自動的に同期します。 広告ネットワークまたは広告ネットワークのデスクトップエディターを使用して、キャンペーンやアカウントのデータに対する最近の変更が直接行われたと思われる場合は、このオプションを選択します。 このオプションを選択すると、一括作成に時間がかかります。 |
| | [!UICONTROL Bulksheet Name] | 新しいバルクシートの名前とファイルタイプ。 デフォルトでは、ファイルはタブ区切りの値フォーマットで作成され、次のいずれかの名前が付けられます。<ul><li>（広告ネットワークのすべてのアカウントに対して） `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（単一アカウントの場合） `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（複数のアカウントの場合） `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`。</li></ul>ファイルの名前を変更できます。 名前に次の文字を含めることはできません：`# % & * \| \ : : < > . ? or /`。<br><br>必要に応じて、ファイルの種類を変更します。 オプションには、*[!UICONTROL .tsv]* （タブ区切り値の場合）、*[!UICONTROL .txt]* （Unicode準拠のASCII テキストの場合）、*[!UICONTROL .csv]* （コンマ区切り値の場合）、または&#x200B;*[!UICONTROL .zip]* （圧縮されたZIP形式の場合、TSV ファイルに展開）が含まれます。<br><br><b> ヒント：</b>国際文字を含むバルクシートには、TSVまたはTXT形式を使用します。 |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | バルクシートに含めるエンティティとそれに対応するステータス（エントリごとに1つのデータ行）。 例えば、アクティブなキャンペーンを含める場合、バルクシートにはアクティブなキャンペーンごとに1行が含まれます。 選択したステータスを持つ選択したエンティティのみが含まれます。 デフォルトは、指定した広告ネットワークに基づいて事前に選択されています。 デフォルトでは、選択したエンティティのアクティブなインスタンスのみが含まれます。 使用可能なバルクシート行のリストについては、「[広告ネットワーク別バルクシート行](#bulksheet-rows-by-ad-network)」を参照してください。<br><br> エンティティを追加または削除するには、エンティティの横にあるチェックボックスをそれぞれ選択またはオフにします。 エンティティのステータスを追加または削除するには、ステータスメニューの横にあるをクリックし、エンティティの横にあるチェックボックスをそれぞれ選択またはオフにします。 |
| | [!UICONTROL Cascading Status Hierarchy] | AND操作を使用して、指定された親エンティティのステータスを持つ子エンティティの範囲をフィルタリングします。 例えば、「Active Campaign」、「Active Adgroup」、「Active Keyword」を選択した場合、バルクシートには、アクティブなキャンペーンのアクティブな広告グループ内のアクティブなキーワードのみが含まれます。<br><br>このオプションを選択しない場合、親ステータスは考慮されず、フィルターはOR操作を使用します。 例えば、「Active Campaign」、「Active Adgroup」、「Active Keyword」を選択すると、親キャンペーンのステータスに関係なく、すべてのアクティブなキャンペーン、すべてのアクティブな広告グループ、および親キャンペーンと広告グループのステータスに関係なく、すべてのアクティブなキーワードが一括シートに含まれます。 |
| | [!UICONTROL Bulksheet Columns] | ダウンロードしたバルクシートファイルに含める列：<ul><li>*[!UICONTROL AMO ID]*: （「[!UICONTROL SE ID]」が選択されていない場合は必須）各エンティティ/行に[!DNL Adobe]が生成した一意のIDが含まれます。 Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、広告ネットワークには投稿しません。 後で、エンティティ IDと親エンティティ IDではなく、[!UICONTROL AMO ID]を識別子として使用して、エンティティのデータを編集できます。</li><li>*[!UICONTROL SE ID]*: （「[!UICONTROL AMO ID]」が選択されていない場合は必須）含まれる各列とその親エンティティに対する広告ネットワークの一意のIDが含まれます。 後で、[!UICONTROL SE ID]を識別子として使用して任意のエンティティのデータを編集する場合は、親エンティティの行（[!UICONTROL SE ID]の値を含む）も含める必要があります。</li><li>*[!UICONTROL Platform]*：広告プラットフォーム（「Baidu」など）を示すために、各行の先頭に[!UICONTROL Platform column]が含まれます。</li><li>*[!UICONTROL Acct Name]*: （「[!UICONTROL AMO ID]」が選択されていない場合は必須）各エンティティ/行の広告ネットワークアカウント名が含まれます。</li><li>\[含める列\]: [!UICONTROL Bulksheet Rows] セクションで選択した各エンティティに関連するすべての列、なし、または選択した列のみを含めるには。 エンティティに関連する個々の列を表示するには、エンティティ名の横にある![右矢印](/help/search-social-commerce/assets/compressed-item.png "右矢印")をクリックします。 デフォルトでは、選択した各エンティティ行に関連するすべての列が含まれます。 任意のエンティティの横または任意の個々の列の横にあるチェックボックスの選択を解除して、バルクシートから除外します。</li></ul><br><br><b> ヒント：</b> バルクシート ファイルの各行に項目を識別するための適切な列を含めるようにしてください。 例えば、[!UICONTROL Bulksheet Rows] セレクターごとにキーワード行を含めても、キーワードに関連するすべての列を除外するとします。 結果のバルクシートには、キーワードインスタンスごとに1行が含まれます。 ただし、AMO IDやSE IDを含むキーワード関連の列は含まれていないため、特定の行に関連するキーワードインスタンスを特定できず、適切なID列と値を手動で追加しない限り、バルクシートを使用してデータを更新することはできません。 |
| [!UICONTROL Filters] | | 特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、またはバルクシートに含める配置の条件：<ol><li>パラメーター（エンティティ名またはID、またはクリエイティブ、キーワード、またはプレースメントの任意の要素）を選択し、演算子を選択して、該当する値を入力します。<br>例えば、[!DNL Google Ads] アカウントの見出しに「靴」が付いた広告のみを返すには、*[!UICONTROL Headline]*&#x200B;を選択し、*[!UICONTROL contains]*&#x200B;を選択して、入力フィールドに`shoes`と入力します。</li><li>（追加のフィルターを適用するには）追加の各フィルターについて、**[!UICONTROL +Add Filter]**&#x200B;をクリックし、**[!UICONTROL AND]**&#x200B;または&#x200B;**[!UICONTROL OR]**&#x200B;を選択し、広告要素またはキーワードと演算子を選択して、該当する値を入力します。</li></ul> |

## 広告ネットワーク別のバルクシート行 {#bulksheet-rows-by-ad-network}

| バルクシート行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | メモ |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Adgroup] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Creative] *または* [!UICONTROL Creative (except RSA)] | はい | はい | はい | — | — | はい | はい | はい | はい | （[!DNL Google  Ads]） [!UICONTROL Responsive Search Ad]行にあるレスポンシブ検索広告を除くすべての広告タイプで使用します。 |
| [!UICONTROL Responsive Search Ad] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | はい | はい | はい | はい | はい | — | はい | はい | はい | 非負のキーワードにのみ使用します。 キャンペーンまたは広告グループレベルで作成された否定的なキーワードを表示するには、使用可能な場合は[!UICONTROL Campaign Negative Keyword]行または[!UICONTROL Adgroup Negative Keyword]行を使用します。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | はい | — | — | — | — | — |
| [!UICONTROL Placement] | — | はい | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | はい | はい | — | — | — | — | — | — | 広告グループの動的検索ターゲットに使用します。 |
| [!UICONTROL Shopping Product Group] | — | はい | はい | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | はい | はい | — | — | — | — | はい | — | — |
| [!UICONTROL Campaign Negative Keyword] | はい | はい | はい | — | — | — | はい | はい | — | キャンペーンまたは広告グループレベルで作成されたネガティブキーワードにのみ使用します。 負でないキーワードを表示するには、使用可能な場合は[!UICONTROL Keyword]行を使用します。 |
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
>* [ バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [ バルクシートの投稿またはエラーファイルの修正](bulksheet-post.md)
>* [ バルクシート ファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシート ファイルを書き出す](bulksheet-export.md)
