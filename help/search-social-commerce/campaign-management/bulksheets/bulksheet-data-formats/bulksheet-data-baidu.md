---
title: に必要なバルクシート データ [!DNL Baidu] アカウント
description: のバルクシートの必須のヘッダーフィールドおよびデータフィールドを参照します。 [!DNL Baidu] アカウント。
exl-id: 9680cb37-50d4-4b4b-b359-ac54267cd5e6
feature: Search Bulksheets
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 0%

---

# 付録 – に必要なバルクシートデータ [!DNL Baidu] アカウント

を作成および更新するには [!DNL Baidu] campaign データを一括で使用すると、用に特別にフォーマットされた検索、ソーシャル、Commerceのバルクシートファイルを使用できます [!DNL Baidu] アカウント。 次のいずれかを実行できます [既存のアカウントの一括シートファイルを生成](../bulksheet-download.md) 必要なファイル形式または b）で手動作成（「」を参照）。[サポートされるバルクシート ファイル形式](bulksheet-file-formats.md)サポートされるファイル形式の一般情報については、「」を参照してください。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Location,Excluded IPs (Baidu), Ad Serving (Baidu),Ad Group Name,Max CPC,Keyword,Match Type,Ad Title,Description Line 1,Description Line 2,Display URL,Base URL,Destination URL,Custom URL Param,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 使用可能なデータフィールド

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>次の表は幅が広いです。 必要に応じて、テーブルの下部にあるスクロールバーを使用して、コンテンツ全体を表示します。 オプションで、をクリックして目次または右側のウィンドウ枠を一時的に非表示にすることもできます。 ![左側のウィンドウを非表示](/help/search-social-commerce/assets/hide-left-pane.png "左側のウィンドウを非表示") 左側のウィンドウの上部、または ![右側のウィンドウを非表示](/help/search-social-commerce/assets/hide-right-pane.png "右側のウィンドウを非表示") 右側のパネルの上部

| フィールド | キャンペーン | 広告グループ | キーワード | テキスト広告 | 場所のターゲット | 説明 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | R/O | 必須/オプション | 必須/オプション | 必須/オプション | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | 必須：作成<br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの 1 日あたりの支出制限（金銭記号および句読点の有無は問わない）。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Location] | 該当なし | 該当なし | 該当なし | 該当なし | 必須 | キャンペーンの広告を配置する地理的な場所。 場所を除外するには、場所の先頭にマイナス記号（`-`）に設定します。 キャンペーンに特定の値を入力しない場合は、すべての場所がターゲットになります。 |
| [!UICONTROL Excluded IPs (Baidu)] | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 広告を表示してはいけない web サイトの IP アドレス。 複数の値をコンマで区切ります。 |
| [!UICONTROL Ad Serving (Baidu)] | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 広告グループ内でアクティブな広告を相互に関連させて配信する頻度：<ul><li><i>回転</i> （新しいキャンペーンのデフォルト）：各広告がほぼ同じ回数だけ広告オークションにエントリするため、検索、ソーシャル、Commerceで、クリックスルー率だけでなくコンバージョン数でも広告をスコアリングできます。</li><li><i>最適化：</i> 広告ネットワークは、高いクリックスルー率と高い品質スコアを組み合わせた広告を優先します。 これらの広告はより頻繁に広告オークションに入り、時間の経過とともに単一の広告が好まれます。 この結果は、ビジネス目標や最適化目標と一致しない場合があります。</li></ul> |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 必須 | 該当なし | 広告グループを識別する一意の名前。 |
| [!UICONTROL Max CPC] | 該当なし | O | O | 該当なし | 該当なし | 最大クリック単価（CPC）。これは、金銭的な記号や句読点の有無にかかわらず、検索ネットワーク上の広告クリックに対して支払う最高額です。 広告グループとキーワードの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 |
| [!UICONTROL Keyword] | オプション/なし | オプション/なし | 必須 | 該当なし | 該当なし | キーワード文字列。<br><br>広告グループまたはキャンペーンレベルでキーワードを除外するには、 [!UICONTROL Match Type] 対象： [!UICONTROL Negative]. 行に広告グループ名が含まれている場合、キーワードはその広告グループから除外されます。 行に広告グループ名が含まれていない場合、キーワードはキャンペーン全体で除外されます。<br><br><b>注意：</b>Baidu キーワードを変更すると、既存のキーワードが削除され、新しいキーワード ID で新しいキーワードが作成されます。 ただし、既存のキーワードを削除することなく、一致のタイプを変更できます。 |
| [!UICONTROL Match Type] | オプション/なし | オプション/なし | オプション：作成<br>必須/オプション：編集または削除 | 該当なし | 該当なし | キーワードの「キーワード一致」オプション： <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Negative Broad]</i>、または <i>[!UICONTROL Negative Exact]</i>. キャンペーンレベルまたは広告グループレベルでネガティブキーワードを定義します。<br><br>新しいキーワードの場合、デフォルトはです。 <i>[!UICONTROL Broad]</i>. 一致タイプまたはキーワード ID の値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。<br><br><b>注意：</b>の一致のタイプを変更できます [!DNL Baidu] 既存のキーワードを削除しないキーワード。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告の見出し。 最大長は 14 個の 2 バイトまたは 28 個の 1 バイト文字です。<br><br><b>注意：</b> 広告コピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Description Line 1] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告の本文の最初のライン。 最小の長さは 4 つの 2 バイト文字または 8 つの 1 バイト文字で、最大の長さは 20 つの 2 バイト文字または 40 つの 1 バイト文字です。<br><br><b>注意：</b> 広告コピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Description Line 2] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告の本文の 2 行目。 最小の長さは 4 つの 2 バイト文字または 8 つの 1 バイト文字で、最大の長さは 20 つの 2 バイト文字または 40 つの 1 バイト文字です。<br><br><b>注意：</b> 広告コピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Display URL] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告に表示される URL。 最大長は 35 個のシングルバイト文字です。 |
| [!UICONTROL Base URL] | 該当なし | 該当なし | オプション | 必須 | 該当なし | エンドユーザーが広告をクリックした際に取得されるランディングページの URL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。<br><br>キーワードレベルのベース/最終 URL は、広告レベル以降の URL を上書きします。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報目的で生成されたバルクシートに含まれ、広告ネットワークに投稿されない）宛先 URL を持つアカウントの場合、この値は、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定およびキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br>最終的な URL を持つアカウントの場合、この列には次の値が表示されます [!UICONTROL Base URL/Final URL column]. |
| [!UICONTROL Custom URL Param] | 該当なし | 該当なし | オプション | オプション | 該当なし | に置き換えるデータ `{custom_code}` 動的変数：変数が検索アカウントまたはキャンペーン設定のトラッキングパラメーターに含まれる場合。 トラッキング URL にカスタム値を挿入するには、 [!UICONTROL Generate Tracking URLs] オプション。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新規キャンペーンのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブまたは一時停止されたキャンペーンを削除するには、値「」を入力します[!UICONTROL Deleted]」と入力します。 |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | 該当なし | 広告グループの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ） 新しい広告グループのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブまたは一時停止されている広告グループを削除するには、値「」を入力します[!UICONTROL Deleted]」と入力します。 |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | キーワードの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）、 <i>[!UICONTROL Inactive]</i> （編集不可）、 <i>[!UICONTROL Paused]</i> （既存のキーワードのみ）、 <i>[!UICONTROL Pending]</i>（編集不可）。 新しいキーワードのデフォルトは <i>[!UICONTROL Active]</i>.<br><br>キーワードを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 広告の表示ステータス： <i>[!UICONTROL Active]</i>（新規広告のデフォルト）、 <i>[!UICONTROL Deleted]</i> （既存の広告のみ） <i>[!UICONTROL Disapproved]</i> （編集不可）、 <i>[!UICONTROL Inactive]</i> （編集不可）、 <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Pending (not editable)]</i>.<br><br>広告を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | 該当なし | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 場所ターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted] （既存の場所のみ）。 新しい場所のデフォルトはです <i>[!UICONTROL Active]. アクティブな位置を削除するには、値を入力します <i>[!UICONTROL Deleted]. |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | オプション | 該当なし | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 エンティティごとに分類ごとに 1 つの値のみを含めることができます（キャンペーン A の「カラー」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加する新しいコンポーネントは、自動的にラベルに関連付けられます。 <br><br>分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | 該当なし | 該当なし | エンティティに割り当てられている制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br>制約は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | なし：作成<br>必須/オプション：編集と削除 | オプション | オプション | オプション | 該当なし | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にキャンペーンの AMO ID が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 該当なし | なし：作成<br>必須/オプション：編集と削除 | オプション | オプション | 該当なし | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に広告グループの AMO ID が含まれていない限り、広告グループ名を変更した場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | なし：作成<br>必須/オプション：編集と削除 | 該当なし | 該当なし | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に a） キーワードを識別するのに十分なプロパティ列、または b） AMO ID が含まれていない限り、キーワード名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad ID] | 該当なし | 該当なし | 該当なし | なし：作成<br>必須/オプション：編集と削除 | 該当なし | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に a） キーワードを識別するのに十分なプロパティ列、または b） AMO ID が含まれていない限り、キーワード名を変更する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | なし：作成<br>オプション：編集と削除 | なし：作成<br>オプション：編集と削除 | なし：作成<br>オプション：編集と削除 | なし：作成<br>オプション：編集と削除 | なし：作成<br>オプション：編集と削除 | （生成されたバルクシート内） [!DNL Adobe] – 同期されたエンティティに対して生成された一意の id。 レスポンシブ検索広告の場合、を含めない限り、広告を編集または削除するには AMO ID が必要です [!UICONTROL Ad ID]. AMO ID を持つその他すべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID でデータを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）行のデータに関する検索、ソーシャル、Commerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは次に含まれます [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは次に含まれます [!UICONTROL SE Errors] ファイル。 この値は広告ネットワークに投稿されません。 |

[^1]:Excel でファイルを開くと、大きな数値が指数表記（2115585666 の場合は 2.12E+09 など）に変換されます。 標準の表記で数字を表示するには、列の任意のセルを選択して、式バーの内側をクリックします。

>[!MORELIKETHIS]
>
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルのダウンロードと作成](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正されたエラーファイルのアップロード](../bulksheet-upload.md)
