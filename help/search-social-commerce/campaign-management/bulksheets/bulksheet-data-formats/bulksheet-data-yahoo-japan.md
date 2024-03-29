---
title: のバルクシートデータ [!DNL Yahoo! Japan] アカウント
description: 次のフィールドについて、ダウンロードした一括送信シートのヘッダーフィールドとデータフィールドを参照します。 [!DNL Yahoo! Japan] アカウント。
exl-id: 78eb41ce-3854-454c-adf2-ba0339e2aef7
feature: Search Bulksheets
source-git-commit: e15cc54f09f905ee4d3b448d7e766c1513f12afb
workflow-type: tm+mt
source-wordcount: '2645'
ht-degree: 0%

---

# 付録 — のバルクシートデータ [!DNL Yahoo! Japan] アカウント

のデータをダウンロードできます。 [!DNL Yahoo! Japan] アカウントを一括でアップロードしているものの、広告ネットワークにバルクシートをアップロードまたは投稿できない。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Delivery Method,Mobile Bid Adjustment,Location,Location Type,Ad Group Name,Max CPC,Keyword,Match Type,First Page Bid, Quality Score,Ad Name (Yahoo JP),Creative Preferred Devices,Ad Title,Ad Title2,Description Line 1,Description Line 2,Creative Type,Display URL,Display Path 1,Display Path 2,Base URL/Final URL,Destination URL,Tracking Template,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Constraints,Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 使用可能なデータフィールド

>[!TIP]
>
>次の表は幅が広い。 必要に応じて、テーブルの下部にあるスクロールバーを使用して、すべてのコンテンツを表示します。 また、オプションで、目次や右側のウィンドウを一時的に非表示にするには、 ![左側のウィンドウを非表示にする](/help/search-social-commerce/assets/hide-left-pane.png "左側のウィンドウを非表示にする") 左側のウィンドウの上部に、または ![右側のウィンドウを非表示にする](/help/search-social-commerce/assets/hide-right-pane.png "右側のウィンドウを非表示にする") をクリックします。

| フィールド | Campaign | 広告グループ | キーワード | テキスト広告 | キャンペーンの場所のターゲット | 説明 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | 広告ネットワークアカウントを識別する一意の名前。 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | 必須：作成<br><br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンに対する 1 日の支出制限。通貨記号や句読点の有無は問いません。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Delivery Method] | 必須：作成<br><br>オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの広告を 1 日に表示する速度：<ul><li>*[!UICONTROL Standard (Distributed)]* （新しいキャンペーンのデフォルト）：広告インプレッションを 1 日にわたって分散させます。</li><li>*[!UICONTROL Accelerated]:* 広告を可能な限り頻繁に表示して、予算に達します。 その結果、広告が 1 日後に表示されない場合があります。</li></ul> |
| [!UICONTROL Mobile Bid Adjustment] | オプション | オプション | 該当なし | 該当なし | 該当なし | モバイルデバイスで広告の入札をおこなうかどうか、キャンペーンレベルまたは広告グループレベルで指定します。<ul><li>既存のモバイル入札の調整を使用する場合は、空白のままにします。</li><li>モバイルデバイスで広告を入札しない場合は、 `-100`.</li><li>デスクトップおよびタブレットデバイスで広告と同じ入札額を使用してモバイルデバイスで広告を入札するには、次のように入力します（0%の差異）。 `0`. 新規キャンペーンの場合は、この設定を空白にすることもできます。</li><li>異なる入札を使用しているモバイルデバイス上の広告に対する入札を行うには、入札の増減に使用する割合を入力します。 値は、 `-90` から `300`.</li></ul>キャンペーンレベルでデバイスを除外する場合、広告グループレベルで除外を上書きすることはできません。<br><br><b>メモ：</b><ul><li>広告グループはキャンペーンレベルの設定を継承しますが、上書きすることができます。</li><li>最適化されたポートフォリオにキャンペーンを割り当てると、最適化機能によって、ポートフォリオの目的を満たすのに役立つ基本キーワードレベルの入札額が自動的に決定されます。 次に、広告ネットワークは、モバイル広告に指定されたとおりに入札額を調整します。</li><li>最適化されたポートフォリオにキャンペーンまたは広告グループを割り当てる場合：<ul><li>最適化機能は、ポートフォリオの目的を満たすのに役立つ、基本キーワードレベルの入札を自動的に決定します。 次に、検索ネットワークは、モバイル広告に対して指定された入札額を調整します。</li><li>ポートフォリオが「[!UICONTROL Auto-optimize Bid Adjustment Values]「」の場合、最適化機能は、計算する理想的な値がポートフォリオ設定で指定された最小値と最大値に該当し、広告グループがモバイル広告の入札を除外しない限り、広告グループレベルで入札調整を変更します。</li></ul></li></ul> |
| [!UICONTROL Location] | 該当なし | 該当なし | 該当なし | 該当なし | オプション | キャンペーンの広告を配置する地理的な場所。 市区町村の場合は、「&lt;」の形式を使用します。<i>市区町村</i>>, &lt;</i>都道府県</i>>」（東京の足立など） 場所を除外するには、場所の前にマイナス記号 (`-`) をクリックします。 キャンペーンに特定の値を入力しない場合、すべての場所がターゲットになります。 |
| [!UICONTROL Location Type] | 該当なし | 該当なし | 該当なし | 該当なし | 必須/オプション | （特定の場所をターゲットにする場合に必須）指定した場所のタイプがの場合、 [!UICONTROL Prefecture] または [!UICONTROL City]. |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 必須 | 該当なし | キャンペーン内で一意の広告グループ名。 最大長は 50 文字です。 |
| [!UICONTROL Max CPC] | 該当なし | オプション | オプション | 該当なし | 該当なし | 最大クリック単価 (CPC)。検索ネットワーク上での広告クリックに対して支払われる最も高い金額で、通貨記号や句読点の有無は問いません。 広告グループおよびキーワードの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 |
| [!UICONTROL Keyword] | オプション/なし | オプション/なし | 必須 | 該当なし | 該当なし | キーワード文字列。 [!DNL Yahoo! Japan] キーワードと一致タイプは可変です。つまり、既存のキーワードを削除せずに編集できます。<br><br>広告グループまたはキャンペーンレベルでキーワードを除外するには、 [!UICONTROL Match Type] を「ネガティブ」に変更します。 行に広告グループ名が含まれる場合、そのキーワードは広告グループに対して除外されます。 行に広告グループ名が含まれていない場合、キーワードはキャンペーン全体に対して除外されます。 |
| [!UICONTROL Match Type] | オプション/なし | オプション/なし | オプション：作成<br><br>必須/オプション：編集または削除 | 該当なし | 該当なし | キーワードのキーワード一致オプション： *[!UICONTROL Broad]* （新しいキーワードのデフォルト）、 *[!UICONTROL Exact]*, *[!UICONTROL Phrase]*, *[!UICONTROL Negative Broad]または *[!UICONTROL Negative Exact]*. キャンペーンレベルまたは広告グループレベルで除外キーワードを定義する。 [!DNL Yahoo! Japan] キーワードと一致タイプは可変です。つまり、既存のキーワードを削除せずに編集できます。<br><br>一致タイプまたはキーワード ID の値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。 |
| [!UICONTROL First Page Bid] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）検索結果の最初のページに広告を配置するために必要な入札。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Quality Score] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）広告ネットワークがキーワードに割り当てた現在の品質スコア。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Ad Name (Yahoo JP)] | 該当なし | 該当なし | 該当なし | オプション：作成<br><br>必須/オプション：編集または削除 | 該当なし | 広告グループ内の広告画像を識別する一意の名前。 最大長は 50 文字です。 を使用しない限り必須 [!UICONTROL AMO ID] または [!UICONTROL Ad ID] 行の。 |
| [!UICONTROL Creative Preferred Devices] | 該当なし | 該当なし | 該当なし | オプション | 該当なし | 広告の表示を希望するデバイスタイプ： *[!UICONTROL All]* （デフォルト）または *[!UICONTROL Mobile]*. の場合 [!UICONTROL Mobile]を使用すると、広告ネットワークは、デスクトップユーザーやタブレットユーザーではなく、モバイルデバイスユーザーに対して広告の表示を試みます。 それ以外の場合は、広告が任意のデバイスタイプで表示されます。<br><br>管理者と [!DNL Adobe] アカウントマネージャーユーザーは、この設定を編集できます。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告のヘッドライン。 最大の長さは、1 バイト文字 30 文字または 2 バイト文字 15 文字です。 広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Ad Title 2] | 該当なし | 該当なし | 該当なし | 必須/なし | 該当なし | （拡張テキスト広告のみ）2 番目のヘッドライン。 最大長は 30 文字または 2 バイト文字 15 文字です。 広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Description Line 1] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | 広告の本文。 拡張テキスト広告の場合、最大の長さは 80 シングルバイトまたは 40 ダブルバイト文字です。 広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Description Line 2] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | （標準テキスト広告のみ）広告本文の 2 行目。 最大の長さは、1 バイト文字で 38 文字、または 2 バイト文字で 19 文字です。 広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 <b>注意：</b> [!DNL Yahoo! Japan Ads] では、標準テキスト広告の作成と編集ができなくなりました。 |
| [!UICONTROL Creative Type] | 該当なし | 該当なし | 該当なし | オプション | 該当なし | 広告の形式は次のとおりです。<ul><li>*[!UICONTROL Text]* （新しい広告のデフォルト）：コンピューター、タブレット、スマートフォンに表示される可能性のあるテキスト広告。</li><li>*[!UICONTROL Mobile]:* 廃止されました。</li></ul> |
| [!UICONTROL Display URL] | 該当なし | 該当なし | 該当なし | 必須/なし：作成<br><br>オプション/該当なし：編集または削除 | 該当なし | （既存の標準テキスト広告のみ、読み取り専用）広告に表示される URL。 最大の長さは、1 バイト文字で 255 文字、または 2 バイト文字で 127 文字です。 また、表示 URL とランディングページ URL のドメインは同じである必要があります。 <b>注意：</b> [!DNL Yahoo! Japan Ads] では、標準テキストおよび拡張テキスト広告の作成と編集を廃止しました。 |
| [!UICONTROL Display Path 1], [!UICONTROL Display Path 2] | 該当なし | 該当なし | 該当なし | オプション/なし | 該当なし | （拡張テキスト広告のみ、オプション）最終 URL から自動的に抽出される表示 URL に追加されるテキスト。 URL の前にスラッシュ (`/`) をクリックします。 パスにスラッシュ (`/`) または改行 (`\n`) 文字を使用します。 最大長は 15 文字または 2 バイト文字 7 文字です。<br><br>広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。<ul><li>[!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`</li><li>[!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`</li></ul>例えば、 [!UICONTROL Display Path 1] が「掘り出し物」の場合、表示 URL は `&lt;display URL&gt;/deals`www.example.com/dealsなど。 |
| [!UICONTROL Base URL/Final URL] | 該当なし | 該当なし | オプション | 必須 | 該当なし | 広告のクリック時に表示されるランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 キーワードレベルのベース/最終 URL は、広告レベル以上の URL に優先します。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （広告ネットワークに投稿されない、情報を目的として生成された一括送信シートに含まれます）宛先 URL のアカウントの場合、この URL は広告主の Web サイト上のベース URL/ランディングページに広告をリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする場合もあります）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づいています。 広告のネットワーク固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。<br><br>最終 URL を持つアカウントの場合、この列には「ベース URL/最終 URL」列と同じ値が表示されます。<br><br>キーワードまたはプレースメントレベルのリンク先 URL は、広告レベルの URL を上書きします。 |
| [!UICONTROL Tracking Template] | オプション | オプション | オプション | オプション | オプション | （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 パラメーターの使用 `!{lpurl}` をクリックして、ランディングページの URL を指定します。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。<br><br>オプションで、サードパーティのリダイレクトとトラッキングを追加できます。<br><br>Adobe Advertisingコンバージョントラッキングの場合。これは、キャンペーン設定で「[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。<br><br>最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br><br>必須：削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの表示ステータス： *[!UICONTROL Active]* （新しいキャンペーンのデフォルト） *[!UICONTROL Paused]*, *[!UICONTROL Ended]* （既存のキャンペーンのみ）または *[!UICONTROL Deleted]* （既存のキャンペーンのみ）。 |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集<br><br>必須：削除 | 該当なし | 該当なし | 該当なし | 広告グループの表示ステータス：  *[!UICONTROL Active]*, *[!UICONTROL Paused]*&#x200B;または *[!UICONTROL Deleted]* （既存の広告グループのみ）。 新しい広告グループのデフォルトはです。 [!UICONTROL Active]. アクティブな広告または一時停止した広告グループを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集<br><br>必須：削除 | 該当なし | 該当なし | キーワードの表示ステータス： *[!UICONTROL Active]*, *[!UICONTROL Deleted]* （既存のキーワードのみ）、 *[!UICONTROL Disapproved]* （編集不可） *[!UICONTROL Paused]* （既存のキーワードのみ）または *[!UICONTROL Pending]* （編集不可） 新しいキーワードのデフォルトはです。 [!UICONTROL Active]. キーワードを削除するには、値を入力します。 `Deleted`. |
| [!UICONTROL Ad Status] | 該当なし | 該当なし | 該当なし | オプション：作成または編集<br><br>必須：削除 | 該当なし | 広告の表示ステータス： *[!UICONTROL Active]* （新しい広告のデフォルト） *[!UICONTROL Deleted]* （既存の広告のみ）、 *[!UICONTROL Disapproved]* （編集不可） *[!UICONTROL Paused]*&#x200B;または *[!UICONTROL Pending]* （編集不可） 新しい広告のデフォルトは、 [!UICONTROL Active]. 広告を削除するには、値を入力します `Deleted`. |
| [!UICONTROL Location Status] | 該当なし | 該当なし | 該当なし | 該当なし | オプション | ロケーションターゲットのステータス： *[!UICONTROL Active]* または *[!UICONTROL Deleted]* （既存の場所のみ）。 新しい場所のデフォルトはです。 [!UICONTROL Active]. アクティブな場所を削除するには、値を入力します `Deleted`. |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | オプション | オプション | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 エンティティごとに 1 つの分類のみを含めることができます（キャンペーン A の「色」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 <br><br>分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | オプション | 該当なし | エンティティに割り当てられる制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br>制約は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 該当なし：作成<br><br>必須/オプション：編集または削除 | オプション | オプション | オプション | 該当なし | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、前に一重引用符 (`'`) をクリックします。[^1] キャンペーン名を変更した場合にのみ必須です ( 行に「[!UICONTROL AMO ID]」と呼ばれます。 |
| [!UICONTROL Ad Group ID] | 該当なし | 該当なし：作成<br><br>必須/オプション：編集または削除 | オプション | オプション | 該当なし | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、前に一重引用符 (`'`) をクリックします。[^1] 広告グループ名を変更した場合にのみ必須です ( 行に「[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 該当なし：作成<br><br>必須/任意：編集<br><br>必須：削除 | 該当なし | 該当なし | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、前に一重引用符 (`'`) をクリックします。[^1] キーワードを編集または削除する場合にのみ必須です（ただし、行に a が含まれている場合を除く）。キーワードを識別するのに十分なプロパティ列、または b)a &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL Ad ID] | 該当なし | 該当なし | 該当なし | 該当なし：作成<br><br>必須/オプション：編集または削除 | 該当なし | 既存の広告を識別する一意の ID。 CSV および TSV ファイルでは、前に一重引用符 (`'`) をクリックします。[^1] レスポンシブ検索広告の場合は、 [!UICONTROL Ad ID] または [!UICONTROL AMO ID] は、広告データの編集または削除に必要です。 その他のエンティティタイプの場合、 [!UICONTROL AMO ID] は、広告のステータスを変更する場合にのみ必要です（行に a を含む場合を除く）広告を識別するのに十分な広告プロパティ列または b)「[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。<br><br><b>注意：</b> を編集する場合、以下を除く広告プロパティの列 [!UICONTROL Status] （既存の広告または b）レスポンシブ検索広告のデータの場合 ) を選択し、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]をクリックした場合、新しい広告が作成され、既存の広告は変更されません。 |
| [!UICONTROL AMO ID] | 該当なし：作成<br><br>オプション：編集または削除 | 該当なし：作成<br><br>オプション：編集または削除 | 該当なし：作成<br><br>オプション：編集または削除 | 該当なし：作成<br><br>オプション：編集または削除 | 該当なし | （生成されたバルクシート内） [!DNL Adobe] — 同期されたエンティティに対して生成された一意の識別子。 レスポンシブ検索広告の場合、 [!UICONTROL AMO ID] を含めない限り、広告を編集または削除するにはが必要です。 [!UICONTROL Ad ID]. を使用して他のすべてのエンティティタイプのデータを編集するには [!UICONTROL AMO ID]、 [!UICONTROL AMO ID] エンティティ ID と親エンティティ ID を含めない限り、はデータの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |
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
