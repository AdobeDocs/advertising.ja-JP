---
title: ' [!DNL Yandex]  アカウントに必要なバルクシートデータ'
description: ' [!DNL Yandex]  アカウントの必須ヘッダーフィールドとデータフィールドを一括シートで参照します。'
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/yargzmjV5ZvOef--zrF6oSNq-gVcu1z3UXSovFDcMwo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1940
ht-degree: 0%

---

# 付録 – [!DNL Yandex] アカウントに必要なバルクシート データ

[!DNL Yandex]件のキャンペーンデータを一括で作成および更新するには、[!DNL Yandex]件のアカウントに特化してフォーマットされたSearch、Social、およびCommerceのバルクシート ファイルを使用できます。 a） [必要なファイル形式で既存のアカウントの一括シートファイルを生成するか、b）手動で作成できます（サポートされているファイル形式に関する一般的な情報については、「](../bulksheet-download.md) サポートされている一括シートファイル形式[」を参照）。](bulksheet-file-formats.md)

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## 使用可能なデータフィールド

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>次の表は幅が広いです。 表示領域を拡大するには、左ペインの上部にある![左ペインを非表示](/help/dsp/assets/hide-left-pane.png "左ペインを非表示")および右ペインの上部にある![右ペインを隠す](/help/dsp/assets/hide-right-pane.png "右ペインを隠す")をクリックして、目次と右ペインを一時的に非表示にすることができます。 テーブルの下部にあるスクロールバーを使用して、コンテンツ全体を表示することもできます。

| フィールド | キャンペーン | 広告グループ | キーワード | テキスト広告 | Sitelink | 説明 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | なし | なし | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティのAMO IDが含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | 必須/オプション | （情報目的で生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティのAMO IDが含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Start Date] | 必須：作成<br> オプション：編集または削除 | なし | なし | なし | なし | 広告主のタイムゾーンで、m/d/yyyy、m/d/yy、m-d-yyyy、またはm-d-yyのいずれかの形式で、キャンペーンに入札を配置できる最初の日付。 新しいキャンペーンのデフォルトは現在の日付です。 |
| [!UICONTROL Campaign Budget] | 必須：作成<br> オプション：編集または削除 | なし | なし | なし | なし | キャンペーンの生涯支出制限。金銭的な記号と句読点の有無にかかわらず適用されます。 |
| [!UICONTROL Delivery Method] | 必須：作成<br> オプション：編集または削除 | なし | なし | なし | なし | キャンペーンの広告を毎日表示する速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを一日中広げます。</li><li><i>[!UICONTROL Accelerated]:</i>予算に達するまで、広告を可能な限り頻繁に表示します。 その結果、広告が後で表示されない場合があります。</li></ul> |
| [!UICONTROL Ad Group Name] | なし | 必須 | 必須 | 必須 | なし | 広告グループ。 |
| [!UICONTROL Ad Title] | なし | なし | なし | 必須 | なし | バナー（ad）の見出し。 最大長は33文字で、1つの単語に23文字を超えることはできません。<br><br><b> メモ：</b>広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Ad Description] | なし | なし | なし | 必須 | なし | バナー（ad）の本文。 最大長は75文字で、1つの単語は22文字を超えることはできません。<br><br><b> メモ：</b>広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Base URL] | なし | なし | オプション | 必須 | なし | 広告をクリックしたときにエンドユーザーが取得するランディングページのURL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 最大長は、プロトコルを含めて1024文字です。<br><br> キーワードレベルのベース/最終URLは、広告レベル以上のURLを上書きします。 |
| [!UICONTROL Destination URL] | なし | なし | なし | なし | なし | （生成されたバルクシートに含まれ、広告ネットワークには投稿されません）宛先URLを持つアカウントの場合、この値は、広告を広告主のweb サイト上のベース URL/ランディングページにリンクするURLです（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイト経由で送信する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URLを生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。 |
| [!UICONTROL SiteLink Title] | なし | なし | なし | なし | 必須 | サイトリンクのテキスト： 新しいサイトリンクの場合は、サイトリンクの行内にキャンペーン名を含めます。 広告グループレベルまたは広告レベルのサイトリンクの場合は、それぞれ広告グループ名または広告タイトルとテキストも含めます。<br><br><b>注：</b> サイトリンクは4つまで指定できます。 |
| [!UICONTROL SiteLink Base URL] | なし | なし | なし | なし | 必須 | サイトリンクのベース URL。バナーのベース URLでなければなりません。 「[!UICONTROL Base URL]」を参照してください。 |
| [!UICONTROL SiteLink Destination URL] | なし | なし | なし | なし | なし | サイトリンクの宛先URL。バナーの宛先URLである必要があります。 「[!UICONTROL Destination URL]」を参照してください。 |
| [!UICONTROL Keyword] | オプション / n/a | なし | 必須 | なし | なし | フレーズ（キーワード文字列）。 広告には少なくとも1つのフレーズが必要です。 各キーワードには、ストップワードを除く最大7つの単語を含めることができます。<br><br><b> メモ：</b><ul><li>キャンペーンレベルでフレーズを除外するには、[!UICONTROL Match Type]を[!UICONTROL Negative]に設定します。</li><li>フレーズを変更すると、既存のフレーズが削除され、新しいフレーズが作成されます。</li><li>[!DNL Yandex] キーワードフレーズまたは一致タイプを変更すると、既存のキーワードフレーズが削除され、新しいキーワードフレーズが作成されます。</li></ul> |
| [!UICONTROL Max CPC] | なし | 必須：作成<br> オプション：編集または削除 | オプション | なし | なし | クリック単価（CPC）の上限。バナー（広告）のクリックに対する支払い額が最も高くなります。検索ネットワークでは、金銭記号と句読点の有無にかかわらず、クリック単価が最も高くなります。 広告グループとキーワードの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 |
| [!UICONTROL Match Type] | オプション / n/a | なし | オプション：Create<br>必須/オプション：編集または削除 | なし | なし | 語句のキーワードマッチングオプション：<i>[!UICONTROL Content]</i>または<i>[!UICONTROL Search]</i>。 「[!UICONTROL Negative Keywords]」列を使用して、負のキーワードを定義します。<br><br><b>注意：</b> [!DNL Yandex] キーワードフレーズまたは一致タイプを変更すると、既存のキーワードフレーズが削除され、新しいキーワードフレーズが作成されます。 |
| [!UICONTROL Search Network Status] | オプション | なし | なし | なし | なし | 検索ネットワークに広告を配置するかどうか：<i>[!UICONTROL Yes]</i> （既定）または<i>[!UICONTROL No]</i>。 |
| コンテンツネットワークステータス | オプション | なし | なし | なし | なし | [!DNL Yandex]広告（ディスプレイ）ネットワークに広告を配置するかどうか：<i>[!UICONTROL Yes]</i> （デフォルト）または<i>[!UICONTROL No]</i>。 |
| [!UICONTROL Negative Keywords (Yandex)] | なし | なし | オプション | なし | なし | 広告グループ内のすべてのフレーズで共有され、その前にマイナス記号（`-mykeyword`など）が付いたネガティブキーワード（フレーズ）。 負のキーワードがフレーズ内のキーワードと一致する場合、負のキーワードはフレーズに適用されません。 |
| [!UICONTROL Param1 (Yandex)] | なし | なし | オプション | なし | なし | `{param1}`代用変数の値。 最大255 バイトまで含めることができます。 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Param2 (Yandex)] | なし | なし | オプション | なし | なし | `{param2}`代用変数の値。 最大255 バイトまで含めることができます。 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br>必須：削除 | なし | なし | なし | なし | キャンペーンの表示ステータス：<i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>または<i>[!UICONTROL stop]</i> （一時停止）。 新規キャンペーンのデフォルトは<i>[!UICONTROL active]</i>です。<br><br><b> メモ：</b><ul></li>施策がアクティブになったことがある場合、削除することはできません。 アーカイブ化しましょう。</li><li>キャンペーンは、状況によっては自動的にアーカイブまたは削除されることがあります。</li><li>ステータスを<i>[!UICONTROL disapproved]</i>または<i>[!UICONTROL pending]</i>に手動で設定したり、ステータスを変更したりすることはできません。</li></ul> |
| [!UICONTROL Ad Group Status] | なし | オプション：作成または編集<br>必須：削除 | なし | なし | なし | 広告グループの表示ステータス：<i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>または<i>[!UICONTROL stop]</i> （一時停止）。 新規広告グループのデフォルトは<i>[!UICONTROL active]</i>です。<br><br><b> メモ：</b><ul></li>広告グループがアクティブになったことがある場合、削除することはできません。 アーカイブ化しましょう。</li><li>ステータスを<i>[!UICONTROL disapproved]</i>または<i>[!UICONTROL pending]</i>に手動で設定したり、ステータスを変更したりすることはできません。</li></ul> |
| [!UICONTROL Ad Status] | なし | なし | なし | オプション：作成または編集<br>必須：削除 | なし | バナー（広告）の表示ステータス：<i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>または<i>[!UICONTROL stop]</i> （一時停止）。 新しいバナーのデフォルトは<i>[!UICONTROL active]</i>です。<br><br><b>注意：ステータスを手動で<i>[!UICONTROL disapproved]</i>または<i>[!UICONTROL pending]</i>に設定したり、ステータスを変更したりすることはできません。 |
| [!UICONTROL Keyword Status] | なし | なし | オプション：作成または編集<br>必須：削除 | なし | なし | 語句（キーワード）の表示ステータス：<i>[!UICONTROL active]</i>。 新規フレーズのデフォルトは<i>[!UICONTROL active]</i>です。<br><br><b>注意：ステータスを手動で<i>[!UICONTROL disapproved]</i>または<i>[!UICONTROL pending]</i>に設定したり、ステータスを変更したりすることはできません。 |
| [!UICONTROL SiteLink Status] | なし | なし | なし | なし | オプション：作成または編集<br>必須：削除 | サイトリンクの表示ステータス：<i>[*UICONTROL Active]</i>または<i>[*UICONTROL Paused]</i>。 新しいサイトリンクのデフォルトは<i>[*UICONTROL Active]</i>です。 |
| [!UICONTROL Campaign ID] | なし：作成<br>必須/オプション：編集<br> オプション：削除 | オプション | オプション | オプション | オプション | 既存のキャンペーンを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にキャンペーンのAMO IDが含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | なし | なし：作成<br>必須/オプション：編集<br> オプション：削除 | オプション | オプション | なし | 既存の広告グループを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行に広告グループのAMO IDが含まれていない限り、広告グループ名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad ID] | なし | なし | なし | なし：作成<br>必須/オプション：編集または削除 | なし | 既存のキーワードを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にa）キーワードを識別するのに十分なプロパティ列またはb） AMO IDが含まれていない限り、キーワード名を変更する場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | なし | なし | なし：作成<br>必須/オプション：編集<br>必須：削除 | なし | なし | 既存のキーワードを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にa）キーワードを識別するのに十分なプロパティ列またはb） AMO IDが含まれていない限り、キーワード名を変更する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | なし | なし | なし | なし | なし | （生成されたバルクシート内）同期されたエンティティに対して[!DNL Adobe]が生成した一意のID。 レスポンシブ検索広告の場合、[!UICONTROL Ad ID]を含まない限り、AMO IDは広告の編集または削除に必要です。 AMO IDを持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ IDと親エンティティ IDを含めない限り、AMO IDがデータの編集または削除に必要です。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |
| \[広告主固有ラベル分類\] | オプション | オプション | オプション | オプション | なし | （広告主固有のラベル分類の名前。例えば、「カラー」というラベル分類の「カラー」など）エンティティに関連付けられている指定された分類の値。 エンティティごとに分類ごとに1つの値のみを含めることができます（キャンペーン Aの「カラー」ラベル分類の「赤」など）。 最大長は100文字で、値にはASCII文字と非ASCII文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も詳細）レベルに適用されます。<br><br>分類名と分類値は、大文字と小文字を区別しません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | なし | なし | エンティティに割り当てられた制約。 エンティティごとに割り当てることができる制約は1つだけです。<br><br>制約は子エンティティによって継承されるので、継承された値を上書きしない限り、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL EF Error Message] | なし | なし | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）行のデータに関するSearch、Social、およびCommerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |

[^1]: ファイルを開くと、Excelは大きな数値を科学表記法（2115585666の場合は2.12E+09など）に変換します。 標準表記法で数値を表示するには、列内の任意のセルを選択し、数式バー内をクリックします。

>[!MORELIKETHIS]
>
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [ バルクシートで実行できる操作](bulksheet-operations.md)
>* [ サポートされているバルクシート ファイル形式](bulksheet-file-formats.md)
>* [ バルクシート ファイルのダウンロードと作成](../bulksheet-download.md)
>* [の [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md) クリックトラッキング形式
>* [ バルクシート ファイルをアップロードするか、エラーファイルを修正](../bulksheet-upload.md)
