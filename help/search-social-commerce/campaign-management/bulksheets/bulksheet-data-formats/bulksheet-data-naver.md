---
title: 次に必要なバルクシートデータ： [!DNL Naver] アカウント
description: 次のバルクシートで、必須ヘッダーフィールドとデータフィールドを参照します： [!DNL Naver] アカウント。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---

# 付録 — の必須バルクシートデータ [!DNL Naver] アカウント

を [!DNL Naver] アカウントを検索、ソーシャル、コマースの [!DNL Naver]検索、ソーシャル、コマースにアップロードします。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 使用可能なデータフィールド

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| フィールド | Campaign | 広告グループ | キーワード | 説明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 広告グループを識別する一意の名前。 |
| [!UICONTROL Keyword] | 該当なし | 該当なし | 必須 | キーワード文字列。 |
| [!UICONTROL Base URL] | 該当なし | 該当なし | オプション | 広告のクリック時に表示されるランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。<br><br>キーワードレベルのベース/最終 URL は、広告レベル以上の URL に優先します。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | ( 情報を提供するために、生成された一括送信シートに含まれます。広告ネットワークに投稿されない ) リンク先 URL のアカウントの場合、この値は広告主の Web サイト上のベース URL/ランディングページに広告をリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを介します）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告のネットワーク固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。<br><br>最終 URL を持つアカウントの場合、この列には [!UICONTROL Base URL/Final URL column]. |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 エンティティごとに 1 つの分類のみを含めることができます（キャンペーン A の「色」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も精度の高い）レベルに適用されます。<br><br>分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | エンティティに割り当てられる制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br>制約は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br>必須：削除 | 該当なし | 該当なし | キャンペーンの表示ステータス：*[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブなキャンペーンまたは一時停止したキャンペーンを削除するには、値&quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集<br>必須：削除 | 該当なし | 広告グループの表示ステータス：*[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブな広告または一時停止した広告グループを削除するには、値&quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集<br>必須：削除 | キーワードの表示ステータス：*[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブまたは一時停止したキーワードを削除するには、値&quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | 該当なし：作成<br>必須/任意：編集または削除 | オプション | オプション | 既存のキャンペーンを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキャンペーンの AMO ID が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 該当なし | 該当なし：作成<br>必須/任意：編集または削除 | オプション | 既存の広告グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に広告グループの AMO ID が含まれていない限り、広告グループ名を変更した場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 該当なし：作成<br>必須/任意：編集<br>必須：削除 | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行にキーワードを識別するのに十分なプロパティ列 (a) または b)AMO ID を含む十分なプロパティ列が含まれている場合にのみ必要です。 |
| [!UICONTROL AMO ID] | 該当なし：作成<br>オプション：編集または削除 | 該当なし：作成<br>オプション：編集または削除 | 該当なし：作成<br>オプション：編集または削除 | （生成されたバルクシート内） [!DNL Adobe] — 同期されたエンティティに対して生成された一意の識別子。 レスポンシブ検索広告の場合、 [!UICONTROL Ad ID]. AMO ID を持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID はデータの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | （情報を目的として生成された一括送信シートに含まれます）行のデータに関する検索、ソーシャル、コマースからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | 該当なし | 該当なし | 該当なし | （情報を提供するために、生成された一括送信シートに含まれます）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL SE Errors] ファイル。 この値は広告ネットワークに投稿されません。 |

<table style="table-layout:auto">

[^1]:Excel は、ファイルを開くときに大きな数値を科学的表記 (2115585666の 2.12E+09 など ) に変換します。 標準の表記で数字を表示するには、列内の任意のセルを選択し、数式バーの内側をクリックします。

>[!MORELIKETHIS]
>
>* [付録 — バルクシートエラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルのダウンロード/作成](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正済みエラーファイルのアップロード](../bulksheet-upload.md)
>* [実装方法 [!DNL Naver] トラッキング専用アカウント](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)

