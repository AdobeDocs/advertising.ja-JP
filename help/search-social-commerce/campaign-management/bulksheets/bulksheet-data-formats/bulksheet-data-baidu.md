---
title: 次に必要なバルクシートデータ： [!DNL Baidu] アカウント
description: 次のバルクシートで、必須ヘッダーフィールドとデータフィールドを参照します： [!DNL Baidu] アカウント。
exl-id: 9680cb37-50d4-4b4b-b359-ac54267cd5e6
feature: Search Bulksheets
source-git-commit: e15cc54f09f905ee4d3b448d7e766c1513f12afb
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 0%

---

# 付録 — の必須バルクシートデータ [!DNL Baidu] アカウント

作成および更新するには [!DNL Baidu] キャンペーンデータを一括で使用する場合は、専用の形式の検索、ソーシャル、コマースのバルクシートファイルを使用できます。 [!DNL Baidu] アカウント。 次のいずれかを実行できます。a) [既存のアカウントに対してバルクシートファイルを生成します](../bulksheet-download.md) 必要なファイル形式で、または b) 手動で作成する ([サポートされるバルクシートファイル形式](bulksheet-file-formats.md)」を参照してください )。

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
>次の表は幅が広い。 必要に応じて、テーブルの下部にあるスクロールバーを使用して、すべてのコンテンツを表示します。 また、オプションで、目次や右側のウィンドウを一時的に非表示にするには、 ![左側のウィンドウを非表示にする](/help/search-social-commerce/assets/hide-left-pane.png "左側のウィンドウを非表示にする") 左側のウィンドウの上部に、または ![右側のウィンドウを非表示にする](/help/search-social-commerce/assets/hide-right-pane.png "右側のウィンドウを非表示にする") をクリックします。

| フィールド | Campaign | 広告グループ | キーワード | テキスト広告 | 場所のターゲット | 説明 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | R/O | 必須/オプション | 必須/オプション | 必須/オプション | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | 必須：作成<br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンに対する 1 日の支出制限。通貨記号や句読点の有無は問いません。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Location] | 該当なし | 該当なし | 該当なし | 該当なし | 必須 | キャンペーンの広告を配置する地理的な場所。 場所を除外するには、場所の前にマイナス記号 (`-`) をクリックします。 キャンペーンに特定の値を入力しない場合、すべての場所がターゲットになります。 |
| [!UICONTROL Excluded IPs (Baidu)] | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 広告を表示しない Web サイトの IP アドレス。 複数の値を指定する場合はコンマで区切ります。 |
| [!UICONTROL Ad Serving (Baidu)] | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 広告グループ内でお互いに関連してアクティブな広告を配信する頻度：<ul><li><i>回転</i> （新しいキャンペーンのデフォルト）：各広告が広告オークションにほぼ同じ回数入力され、検索、ソーシャル、コマースがクリックスルー率だけでなくコンバージョンも広告にスコアを付けることができます。</li><li><i>最適化：</i> 広告ネットワークは、高いクリックスルー率と高い品質スコアを組み合わせた広告を優先します。 これらの広告は、より頻繁に広告オークションに入り、時間の経過と共に単一の広告が優先されます。 この結果は、ビジネス目標や最適化目標と矛盾する場合があります。</li></ul> |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 必須 | 該当なし | 広告グループを識別する一意の名前。 |
| [!UICONTROL Max CPC] | 該当なし | O | O | 該当なし | 該当なし | 最大クリック単価 (CPC)。検索ネットワークでの広告クリックに対して支払う最も高い金額です。通貨記号や句読点の有無は問いません。 広告グループおよびキーワードの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 |
| [!UICONTROL Keyword] | オプション/なし | オプション/なし | 必須 | 該当なし | 該当なし | キーワード文字列。<br><br>広告グループまたはキャンペーンレベルでキーワードを除外するには、 [!UICONTROL Match Type] から [!UICONTROL Negative]. 行に広告グループ名が含まれる場合、そのキーワードは広告グループに対して除外されます。 行に広告グループ名が含まれていない場合、このキーワードはキャンペーン全体に対して除外されます。<br><br><b>注意：</b>Baidu キーワードを変更すると、既存のキーワードが削除され、新しいキーワード ID を持つ新しいキーワードが作成されます。 ただし、既存のキーワードを削除せずに、一致タイプを変更できます。 |
| [!UICONTROL Match Type] | オプション/なし | オプション/なし | オプション：作成<br>必須/オプション：編集または削除 | 該当なし | 該当なし | キーワードのキーワード一致オプション： <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Negative Broad]</i>または <i>[!UICONTROL Negative Exact]</i>. キャンペーンレベルまたは広告グループレベルで除外キーワードを定義する。<br><br>新しいキーワードの場合、デフォルトはです。 <i>[!UICONTROL Broad]</i>. 一致タイプまたはキーワード ID の値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。<br><br><b>注意：</b>一致タイプは、 [!DNL Baidu] キーワードを使用して、既存のキーワードを削除することはできません。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告のヘッドライン。 最大の長さは、2 バイト文字で 14 文字、または 1 バイト文字で 28 文字です。<br><br><b>注意：</b> 広告のコピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Description Line 1] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告の本文の最初の行。 最小の長さは、2 バイト文字 4 文字または 1 バイト文字 8 文字で、最大の長さは 20 ダブルバイト文字または 40 シングルバイト文字です。<br><br><b>注意：</b> 広告のコピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Description Line 2] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告の本文の 2 行目。 最小の長さは、2 バイト文字 4 文字または 1 バイト文字 8 文字で、最大の長さは 20 ダブルバイト文字または 40 シングルバイト文字です。<br><br><b>注意：</b> 広告のコピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Display URL] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告に表示される URL。 最大長は 35 文字です。 |
| [!UICONTROL Base URL] | 該当なし | 該当なし | オプション | 必須 | 該当なし | 広告のクリック時に表示されるランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。<br><br>キーワードレベルのベース/最終 URL は、広告レベル以上の URL に優先します。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （広告ネットワークに投稿されない、情報を目的として生成された一括送信シートに含まれます）宛先 URL のアカウントの場合、この値は広告主の Web サイト上のベース URL/ランディングページに広告をリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイト経由）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告のネットワーク固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。<br><br>最終 URL を持つアカウントの場合、この列には [!UICONTROL Base URL/Final URL column]. |
| [!UICONTROL Custom URL Param] | 該当なし | 該当なし | オプション | オプション | 該当なし | に代わるデータ `{custom_code}` 動的変数を設定できます。 トラッキング URL にカスタム値を挿入するには、 [!UICONTROL Generate Tracking URLs] オプション。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブなキャンペーンまたは一時停止したキャンペーンを削除するには、値&quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | 該当なし | 広告グループの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブな広告または一時停止した広告グループを削除するには、値&quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | キーワードの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）、 <i>[!UICONTROL Inactive]</i> （編集不可） <i>[!UICONTROL Paused]</i> （既存のキーワードのみ）または <i>[!UICONTROL Pending]</i>（編集不可） 新しいキーワードのデフォルトはです。 <i>[!UICONTROL Active]</i>.<br><br>キーワードを削除するには、値を入力します。 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 広告の表示ステータス： <i>[!UICONTROL Active]</i>（新しい広告のデフォルト） <i>[!UICONTROL Deleted]</i> （既存の広告のみ）、 <i>[!UICONTROL Disapproved]</i> （編集不可） <i>[!UICONTROL Inactive]</i> （編集不可） <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Pending (not editable)]</i>.<br><br>広告を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | 該当なし | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | ロケーションターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted] （既存の場所のみ）。 新しい場所のデフォルトはです。 <i>[!UICONTROL Active]. アクティブな場所を削除するには、値を入力します <i>[!UICONTROL Deleted]. |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | オプション | 該当なし | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 エンティティごとに 1 つの分類のみを含めることができます（キャンペーン A の「色」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 <br><br>分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | 該当なし | 該当なし | エンティティに割り当てられる制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br>制約は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 該当なし：作成<br>必須/オプション：編集および削除 | オプション | オプション | オプション | 該当なし | 既存のキャンペーンを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキャンペーンの AMO ID が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 該当なし | 該当なし：作成<br>必須/オプション：編集および削除 | オプション | オプション | 該当なし | 既存の広告グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に広告グループの AMO ID が含まれていない限り、広告グループ名を変更した場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 該当なし：作成<br>必須/オプション：編集および削除 | 該当なし | 該当なし | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキーワードを識別するのに十分なプロパティ列 (a) または b)AMO ID を含む十分なプロパティ列が含まれている場合にのみ必須です。 |
| [!UICONTROL Ad ID] | 該当なし | 該当なし | 該当なし | 該当なし：作成<br>必須/オプション：編集および削除 | 該当なし | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキーワードを識別するのに十分なプロパティ列 (a) または b)AMO ID を含む十分なプロパティ列が含まれている場合にのみ必須です。 |
| [!UICONTROL AMO ID] | 該当なし：作成<br>オプション：編集および削除 | 該当なし：作成<br>オプション：編集および削除 | 該当なし：作成<br>オプション：編集および削除 | 該当なし：作成<br>オプション：編集および削除 | 該当なし：作成<br>オプション：編集および削除 | （生成されたバルクシート内） [!DNL Adobe] — 同期されたエンティティに対して生成された一意の識別子。 レスポンシブ検索広告の場合、 [!UICONTROL Ad ID]. AMO ID を持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID はデータの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）行のデータに関する検索、ソーシャル、コマースからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL SE Errors] ファイル。 この値は広告ネットワークに投稿されません。 |

[^1]:Excel は、ファイルを開く際に大きな数値を科学的表記 (2115585666の 2.12E+09 など ) に変換します。 標準の表記で数字を表示するには、列内の任意のセルを選択し、数式バーの内側をクリックします。

>[!MORELIKETHIS]
>
>* [付録 — バルクシートエラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルをダウンロード/作成する](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正済みエラーファイルのアップロード](../bulksheet-upload.md)
