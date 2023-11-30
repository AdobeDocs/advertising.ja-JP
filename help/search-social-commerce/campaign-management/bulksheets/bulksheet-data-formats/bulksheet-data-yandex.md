---
title: 次に必要なバルクシートデータ： [!DNL Yandex] アカウント
description: 次のバルクシートで、必須ヘッダーフィールドとデータフィールドを参照します： [!DNL Yandex] アカウント。
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
source-git-commit: e15cc54f09f905ee4d3b448d7e766c1513f12afb
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 0%

---

# 付録 — の必須バルクシートデータ [!DNL Yandex] アカウント

作成および更新するには [!DNL Yandex] キャンペーンデータを一括で使用する場合は、専用の形式の検索、ソーシャル、コマースのバルクシートファイルを使用できます。 [!DNL Yandex] アカウント。 次のいずれかを実行できます。a) [既存のアカウントに対してバルクシートファイルを生成します](../bulksheet-download.md) 必要なファイル形式で、または b) 手動で作成する ([サポートされるバルクシートファイル形式](bulksheet-file-formats.md)」を参照してください )。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 使用可能なデータフィールド

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>次の表は幅が広い。 必要に応じて、テーブルの下部にあるスクロールバーを使用して、すべてのコンテンツを表示します。 また、オプションで、目次や右側のウィンドウを一時的に非表示にするには、 ![左側のウィンドウを非表示にする](/help/search-social-commerce/assets/hide-left-pane.png "左側のウィンドウを非表示にする") 左側のウィンドウの上部に、または ![右側のウィンドウを非表示にする](/help/search-social-commerce/assets/hide-right-pane.png "右側のウィンドウを非表示にする") をクリックします。

| フィールド | Campaign | 広告グループ | キーワード | テキスト広告 | Sitelink | 説明 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Start Date] | 必須：作成<br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの入札を行う最初の日付。広告主のタイムゾーンと、m/d/yyyy、m/d/yyy、m-d-yyyy、m-d-yyyy のいずれかの形式で入札を行います。 新しいキャンペーンのデフォルトは現在の日です。 |
| [!UICONTROL Campaign Budget] | 必須：作成<br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンに対する全期間の支出制限（通貨記号と句読点の有無を問わず）。 |
| [!UICONTROL Delivery Method] | 必須：作成<br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの広告を 1 日に表示する速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを 1 日にわたって分散させます。</li><li><i>[!UICONTROL Accelerated]:</i> 広告を可能な限り頻繁に表示して、予算に達します。 その結果、広告が 1 日後に表示されない場合があります。</li></ul> |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 必須 | 該当なし | 広告グループ。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | バナー（広告）のヘッドライン。 最大長は 33 文字で、1 語に含めることができる文字数は 23 文字までです。<br><br><b>注意：</b> 広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Ad Description] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | バナーの本文（広告）。 最大長は 75 文字で、1 語に対して 22 文字以下にする必要があります。<br><br><b>注意：</b> 広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Base URL] | 該当なし | 該当なし | オプション | 必須 | 該当なし | 広告のクリック時に表示されるランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 最大長は、プロトコルを含む 1024 文字です。<br><br>キーワードレベルのベース/最終 URL は、広告レベル以上の URL に優先します。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （広告ネットワークに投稿されない、情報を目的として生成された一括送信シートに含まれます）宛先 URL のアカウントの場合、この値は広告主の Web サイト上のベース URL/ランディングページに広告をリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイト経由）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告のネットワーク固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。 |
| [!UICONTROL SiteLink Title] | 該当なし | 該当なし | 該当なし | 該当なし | 必須 | サイトリンクのテキスト。 新しいサイトリンクの場合は、サイトリンク行内にキャンペーン名を含めます。 広告グループレベルまたは広告レベルのサイトリンクの場合は、広告グループ名または広告タイトルとテキストもそれぞれ含めます。<br><br><b>注意：</b> 最大 4 つのサイトリンクを設定できます。 |
| [!UICONTROL SiteLink Base URL] | 該当なし | 該当なし | 該当なし | 該当なし | 必須 | サイトリンクのベース URL。バナーのベース URL にする必要があります。 参照：[!UICONTROL Base URL].&quot; |
| [!UICONTROL SiteLink Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | サイトリンクのリンク先 URL。バナーのリンク先 URL にする必要があります。 参照：[!UICONTROL Destination URL].&quot; |
| [!UICONTROL Keyword] | オプション/なし | 該当なし | 必須 | 該当なし | 該当なし | フレーズ（キーワード文字列）。 広告には 1 つ以上のフレーズが必要です。 各キーワードは、ストップワードを除く最大 7 語まで指定できます。<br><br><b>メモ：</b><ul><li>キャンペーンレベルで特定のフレーズを除外するには、 [!UICONTROL Match Type] から [!UICONTROL Negative].</li><li>フレーズを変更すると、既存のフレーズが削除され、新しいフレーズが作成されます。</li><li>の変更 [!DNL Yandex] キーワードフレーズまたは一致タイプは、既存のキーワードフレーズを削除し、新しいキーワードフレーズを作成します。</li></ul> |
| [!UICONTROL Max CPC] | 該当なし | 必須：作成<br>オプション：編集または削除 | オプション | 該当なし | 該当なし | 最大クリック単価 (CPC)。検索ネットワーク上でバナー（広告）をクリックする際に支払われる最も高い金額で、通貨記号や句読点の有無は問いません。 広告グループおよびキーワードの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 |
| [!UICONTROL Match Type] | オプション/なし | 該当なし | オプション：作成<br>必須/オプション：編集または削除 | 該当なし | 該当なし | フレーズのキーワード一致オプション： <i>[!UICONTROL Content]</i> または <i>[!UICONTROL Search]</i>. 「[!UICONTROL Negative Keywords]」列に表示されます。<br><br><b>注意：</b> の変更 [!DNL Yandex] キーワードフレーズまたは一致タイプは、既存のキーワードフレーズを削除し、新しいキーワードフレーズを作成します。 |
| [!UICONTROL Search Network Status] | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 検索ネットワークに広告を配置するかどうか： <i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>. |
| コンテンツネットワークステータス | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 広告を [!DNL Yandex] 広告（ディスプレイ）ネットワーク： <i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>. |
| [!UICONTROL Negative Keywords (Yandex)] | 該当なし | 該当なし | オプション | 該当なし | 該当なし | 広告グループ内のすべてのフレーズで共有される、マイナス記号 ( 例： `-mykeyword`) をクリックします。 フレーズ内のキーワードと除外キーワードが一致する場合、そのフレーズには除外キーワードは適用されません。 |
| [!UICONTROL Param1 (Yandex)] | 該当なし | 該当なし | オプション | 該当なし | 該当なし | の値 `{param1}` 代替変数。 最大 255 バイトを含めることができます。 既存の値を削除するには、 `[delete]` （括弧を含む）。 |
| [!UICONTROL Param2 (Yandex)] | 該当なし | 該当なし | オプション | 該当なし | 該当なし | の値  `{param2}` 代替変数。 最大 255 バイトを含めることができます。 既存の値を削除するには、 `[delete]` （括弧を含む）。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの表示ステータス： <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>または <i>[!UICONTROL stop]</i> （一時停止中）。 新しいキャンペーンのデフォルトはです。 <i>[!UICONTROL active]</i>.<br><br><b>メモ：</b><ul></li>キャンペーンがアクティブになったことがある場合は、そのキャンペーンを削除することはできません。 代わりに、アーカイブします。</li><li>キャンペーンは、状況によっては自動的にアーカイブまたは削除される場合があります。</li><li>ステータスを手動でに設定することはできません <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i>また、ステータスを変更することもできません。</li></ul> |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | 該当なし | 広告グループの表示ステータス： <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>または <i>[!UICONTROL stop]</i> （一時停止中）。 新しい広告グループのデフォルトはです。 <i>[!UICONTROL active]</i>.<br><br><b>メモ：</b><ul></li>広告グループがアクティブになったことがある場合、その広告グループは削除できません。 代わりに、アーカイブします。</li><li>ステータスを手動でに設定することはできません <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i>また、ステータスを変更することもできません。</li></ul> |
| [!UICONTROL Ad Status] | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | バナー（広告）の表示ステータス： <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>または <i>[!UICONTROL stop]</i> （一時停止中）。 新しいバナーのデフォルトはです。 <i>[!UICONTROL active]</i>.<br><br><b>注意：ステータスを手動でに設定することはできません。 <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i>また、ステータスを変更することもできません。 |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | フレーズの表示ステータス（キーワード）: <i>[!UICONTROL active]</i>. 新しいフレーズのデフォルトはです。 <i>[!UICONTROL active]</i>.<br><br><b>注意：ステータスを手動でに設定することはできません。 <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i>また、ステータスを変更することもできません。 |
| [!UICONTROL SiteLink Status] | 該当なし | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | サイトリンクの表示ステータス： <i>[*UICONTROL アクティブ]</i> または <i>[*UICONTROL 一時停止中]</i>. 新しいサイトリンクのデフォルトはです。 <i>[*UICONTROL アクティブ]</i>. |
| [!UICONTROL Campaign ID] | 該当なし：作成<br>必須/任意：編集<br>オプション：削除 | オプション | オプション | オプション | オプション | 既存のキャンペーンを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキャンペーンの AMO ID が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 該当なし | 該当なし：作成<br>必須/任意：編集<br>オプション：削除 | オプション | オプション | 該当なし | 既存の広告グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に広告グループの AMO ID が含まれていない限り、広告グループ名を変更した場合にのみ必要です。 |
| [!UICONTROL Ad ID] | 該当なし | 該当なし | 該当なし | 該当なし：作成<br>必須/オプション：編集または削除 | 該当なし | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキーワードを識別するのに十分なプロパティ列 (a) または b)AMO ID を含む十分なプロパティ列が含まれている場合にのみ必須です。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 該当なし：作成<br>必須/任意：編集<br>必須：削除 | 該当なし | 該当なし | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキーワードを識別するのに十分なプロパティ列 (a) または b)AMO ID を含む十分なプロパティ列が含まれている場合にのみ必須です。 |
| [!UICONTROL AMO ID] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （生成されたバルクシート内） [!DNL Adobe] — 同期されたエンティティに対して生成された一意の識別子。 レスポンシブ検索広告の場合、 [!UICONTROL Ad ID]. AMO ID を持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID はデータの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | オプション | 該当なし | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 エンティティごとに 1 つの分類のみを含めることができます（キャンペーン A の「色」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も精度の高い）レベルに適用されます。<br><br>分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | 該当なし | 該当なし | エンティティに割り当てられる制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br>制約は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）行のデータに関する検索、ソーシャル、コマースからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |

[^1]:Excel は、ファイルを開く際に大きな数値を科学的表記 (2115585666の 2.12E+09 など ) に変換します。 標準の表記で数字を表示するには、列内の任意のセルを選択し、数式バーの内側をクリックします。

>[!MORELIKETHIS]
>
>* [付録 — バルクシートエラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルをダウンロード/作成する](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正済みエラーファイルのアップロード](../bulksheet-upload.md)
