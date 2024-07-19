---
title: アカウントに必須のバルクシート デ  [!DNL Yandex]  タ
description: アカウントのバルクシートで、必須のヘッダーフィールドとデータフィ  [!DNL Yandex]  ルドを参照します。
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
source-git-commit: e15cc54f09f905ee4d3b448d7e766c1513f12afb
workflow-type: tm+mt
source-wordcount: '1936'
ht-degree: 0%

---

# 付録 – [!DNL Yandex] アカウントに必須のバルクシートデータ

キャンペーンデータ [!DNL Yandex] 一括で作成および更新するには、[!DNL Yandex] アカウント用に特別にフォーマットされた検索、ソーシャル、Commerceのバルクシートファイルを使用できます。 a） [ 既存のアカウント用のバルクシートファイルを必要なファイル形式で生成する ](../bulksheet-download.md) または b）手動で作成できます（サポートされるファイル形式について詳しくは、「[ サポートされるバルクシートファイル形式 ](bulksheet-file-formats.md)」を参照してください）。

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
>次の表は幅が広いです。 必要に応じて、テーブルの下部にあるスクロールバーを使用して、コンテンツ全体を表示します。 オプションで、左側のウィンドウの上部にある ![ 左側のウィンドウを非表示にする ](/help/search-social-commerce/assets/hide-left-pane.png " 左側のウィンドウを非表示にする ") または右側のウィンドウの上部にある ![右側のウィンドウを非表示](/help/search-social-commerce/assets/hide-right-pane.png "右側のウィンドウを非表示") をクリックして、目次または右側のウィンドウを一時的に非表示にすることもできます。

| フィールド | キャンペーン | 広告グループ | キーワード | テキスト広告 | Sitelink | 説明 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Start Date] | 必須：作成 <br> オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンに対して入札を行うことができる最初の日付。広告主のタイムゾーンおよび次のいずれかのフォーマット（m/d/yyyy、m/d/yy、m-d-yyyy または m-d-yy）。 新しいキャンペーンのデフォルトは現在の日付です。 |
| [!UICONTROL Campaign Budget] | 必須：作成 <br> オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | 金銭的記号および句読点の有無に関わらず、キャンペーンのライフタイム支出制限。 |
| [!UICONTROL Delivery Method] | 必須：作成 <br> オプション：編集または削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの広告を毎日表示する速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを 1 日に配分します。</li><li><i>[!UICONTROL Accelerated]:</i> 予算に達するまでできるだけ頻繁に広告を表示します。 その結果、広告がその日の後半に表示されない場合があります。</li></ul> |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 必須 | 該当なし | 広告グループ。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | バナーのヘッドライン（広告）。 最大長は 33 文字です。1 つの単語に 23 文字を超える文字を含めることはできません。<br><br><b> メモ：</b> 広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Ad Description] | 該当なし | 該当なし | 該当なし | 必須 | 該当なし | バナーの本文（広告）。 最大長は 75 文字で、1 つの単語は 22 文字以下にする必要があります。<br><br><b> メモ：</b> 広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Base URL] | 該当なし | 該当なし | オプション | 必須 | 該当なし | エンドユーザーが広告をクリックした際に取得されるランディングページの URL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 最大長は、プロトコルを含めて 1024 文字です。<br><br> キーワードレベルのベース/最終 URL は、広告レベル以降の URL を上書きします。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報目的で生成されたバルクシートに含まれ、広告ネットワークに投稿されない）宛先 URL を持つアカウントの場合、この値は、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定およびキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。 |
| [!UICONTROL SiteLink Title] | 該当なし | 該当なし | 該当なし | 該当なし | 必須 | サイトリンクテキスト。 新しいサイトリンクの場合は、サイトリンク行にキャンペーン名を含めます。 広告グループレベルまたは広告レベルのサイトリンクには、それぞれ広告グループ名または広告のタイトルとテキストが含まれます。<br><br><b> メモ：</b> 最大 4 つのサイトリンクを設定できます。 |
| [!UICONTROL SiteLink Base URL] | 該当なし | 該当なし | 該当なし | 該当なし | 必須 | サイトリンクのベース URL。バナーのベース URL である必要があります。 「[!UICONTROL Base URL]」を参照してください。 |
| [!UICONTROL SiteLink Destination URL] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | サイトリンクの宛先 URL。バナーの宛先 URL にする必要があります。 「[!UICONTROL Destination URL]」を参照してください。 |
| [!UICONTROL Keyword] | オプション/なし | 該当なし | 必須 | 該当なし | 該当なし | フレーズ（キーワード文字列）。 広告には少なくとも 1 つのフレーズが必要です。 各キーワードには、ストップワードを除いて最大 7 つのワードを含めることができます。<br><br><b> 注：</b><ul><li>キャンペーンレベルでフレーズを除外するには、「[!UICONTROL Match Type]」を「[!UICONTROL Negative]」に設定します。</li><li>フレーズを変更すると、既存のフレーズが削除され、新しいフレーズが作成されます。</li><li>[!DNL Yandex] キーワード句または一致タイプを変更すると、既存のキーワード句が削除され、新しいキーワード句が作成されます。</li></ul> |
| [!UICONTROL Max CPC] | 該当なし | 必須：作成 <br> オプション：編集または削除 | オプション | 該当なし | 該当なし | 最大クリック単価（CPC）。これは、検索ネットワーク上のバナー（広告）クリックに対して支払う最高額で、金銭的な記号と句読点の有無は関係ありません。 広告グループとキーワードの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 |
| [!UICONTROL Match Type] | オプション/なし | 該当なし | オプション：作成 <br> 必須/オプション：編集または削除 | 該当なし | 該当なし | フレーズのキーワード照合オプション：<i>[!UICONTROL Content]</i> または <i>[!UICONTROL Search]</i>。 「[!UICONTROL Negative Keywords]」列を使用して負のキーワードを定義します。<br><br><b> 注意：</b>[!DNL Yandex] しいキーワード句または一致タイプを変更すると、既存のキーワード句が削除され、新しいキーワード句が作成されます。 |
| [!UICONTROL Search Network Status] | オプション | 該当なし | 該当なし | 該当なし | 該当なし | 検索ネットワークに広告を配置するかどうか：<i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>。 |
| コンテンツ ネットワークの状態 | オプション | 該当なし | 該当なし | 該当なし | 該当なし | [!DNL Yandex] 広告（ディスプレイ）ネットワークに広告を配置するかどうか：<i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>。 |
| [!UICONTROL Negative Keywords (Yandex)] | 該当なし | 該当なし | オプション | 該当なし | 該当なし | 広告グループ内のすべてのフレーズで共有され、先頭にマイナス記号が付く負のキーワード（フレーズ）（`-mykeyword` など）。 負のキーワードがフレーズ内のキーワードと一致する場合、負のキーワードはフレーズに適用されません。 |
| [!UICONTROL Param1 (Yandex)] | 該当なし | 該当なし | オプション | 該当なし | 該当なし | `{param1}` 代替変数の値。 最大 255 バイトを含めることができます。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Param2 (Yandex)] | 該当なし | 該当なし | オプション | 該当なし | 該当なし | `{param2}` 代替変数の値。 最大 255 バイトを含めることができます。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集 <br> 必須：削除 | 該当なし | 該当なし | 該当なし | 該当なし | キャンペーンの表示ステータス：<i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>、<i>[!UICONTROL stop]</i> （一時停止）。 新しいキャンペーンのデフォルトは <i>[!UICONTROL active]</i> です。<br><br><b> 注：</b><ul></li>キャンペーンがアクティブになっている場合は、削除できません。 代わりに、アーカイブします。</li><li>キャンペーンは、状況によっては自動的にアーカイブまたは削除されることがあります。</li><li>ステータスを手動で <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i> に設定したり、それらのステータスを変更したりすることはできません。</li></ul> |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集 <br> 必須：削除 | 該当なし | 該当なし | 該当なし | 広告グループの表示ステータス：<i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>、<i>[!UICONTROL stop]</i> （一時停止）。 新しい広告グループのデフォルトは <i>[!UICONTROL active]</i> です。<br><br><b> 注：</b><ul></li>アクティブになっていたことのある広告グループは削除できません。 代わりに、アーカイブします。</li><li>ステータスを手動で <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i> に設定したり、それらのステータスを変更したりすることはできません。</li></ul> |
| [!UICONTROL Ad Status] | 該当なし | 該当なし | 該当なし | オプション：作成または編集 <br> 必須：削除 | 該当なし | バナー（広告）の表示ステータス：<i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i> または <i>[!UICONTROL stop]</i> （一時停止） 新しいバナーのデフォルトは <i>[!UICONTROL active]</i> です。<br><br><b> メモ：手動でステータスを <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i> に設定したり、それらのステータスを変更したりすることはできません。 |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集 <br> 必須：削除 | 該当なし | 該当なし | フレーズ（キーワード）の表示ステータス：<i>[!UICONTROL active]</i>。 新しいフレーズのデフォルトは <i>[!UICONTROL active]</i> です。<br><br><b> メモ：手動でステータスを <i>[!UICONTROL disapproved]</i> または <i>[!UICONTROL pending]</i> に設定したり、それらのステータスを変更したりすることはできません。 |
| [!UICONTROL SiteLink Status] | 該当なし | 該当なし | 該当なし | 該当なし | オプション：作成または編集 <br> 必須：削除 | サイトリンクの表示ステータス：<i>[*UICONTROL Active]</i> または <i>[*UICONTROL Paused]</i> 新しいサイトリンクのデフォルトは <i>[*UICONTROL Active]</i> です。 |
| [!UICONTROL Campaign ID] | 該当なし：作成 <br> 必須/オプション：編集 <br> オプション：削除 | オプション | オプション | オプション | オプション | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にキャンペーンの AMO ID が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 該当なし | 該当なし：作成 <br> 必須/オプション：編集 <br> オプション：削除 | オプション | オプション | 該当なし | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に広告グループの AMO ID が含まれていない限り、広告グループ名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad ID] | 該当なし | 該当なし | 該当なし | なし：作成 <br> 必須/オプション：編集または削除 | 該当なし | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] キーワード名を変更する場合にのみ必須です。ただし、行に（a） キーワードを識別するのに十分なプロパティ列、または（b） AMO ID が含まれる場合を除きます。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 該当なし：作成 <br> 必須/オプション：編集 <br> 必須：削除 | 該当なし | 該当なし | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] キーワード名を変更する場合にのみ必須です。ただし、行に（a） キーワードを識別するのに十分なプロパティ列、または（b） AMO ID が含まれる場合を除きます。 |
| [!UICONTROL AMO ID] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （生成されたバルクシート内）同期されたエンティティの [!DNL Adobe] 生成された一意の ID。 レスポンシブ検索広告の場合、[!UICONTROL Ad ID] を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つその他すべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID でデータを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | オプション | 該当なし | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 エンティティごとに分類ごとに 1 つの値のみを含めることができます（キャンペーン A の「カラー」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加する新しいコンポーネントは、自動的にラベルに関連付けられます。 製品グループのラベル分類は、単位（最も詳細な単位）レベルで適用されます。<br><br> 分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | 該当なし | 該当なし | エンティティに割り当てられている制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br> 制約は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）行のデータに関する検索、ソーシャル、Commerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |

[^1]: Excel でファイルを開くと、大きな数値が指数表記（2115585666 の場合は 2.12E+09 など）に変換されます。 標準の表記で数字を表示するには、列の任意のセルを選択して、式バーの内側をクリックします。

>[!MORELIKETHIS]
>
>* [ 付録 – バルクシート エラー ](../bulksheet-errors.md)
>* [ バルクシートで実行できる操作 ](bulksheet-operations.md)
>* [ サポートされるバルクシート ファイル形式 ](bulksheet-file-formats.md)
>* [ バルクシートファイルのダウンロード/作成 ](../bulksheet-download.md)
>* [ のクリック追跡形式  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [ バルクシートファイルまたは修正されたエラーファイルのアップロード ](../bulksheet-upload.md)
