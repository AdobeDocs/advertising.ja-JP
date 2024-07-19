---
title: アカウントに必須のバルクシート デ  [!DNL Naver]  タ
description: アカウントのバルクシートで、必須のヘッダーフィールドとデータフィ  [!DNL Naver]  ルドを参照します。
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# 付録 – [!DNL Naver] アカウントに必須のバルクシートデータ

[!DNL Naver] 内にバルクシートファイルを生成し、検索、ソーシャル、Commerceにアップロードすることで、検索、ソーシャル、Commerceに [!DNL Naver] アカウントを入力します。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 使用可能なデータフィールド

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| フィールド | キャンペーン | 広告グループ | キーワード | 説明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティの AMO ID が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Ad Group Name] | 該当なし | 必須 | 必須 | 広告グループを識別する一意の名前。 |
| [!UICONTROL Keyword] | 該当なし | 該当なし | 必須 | キーワード文字列。 |
| [!UICONTROL Base URL] | 該当なし | 該当なし | オプション | エンドユーザーが広告をクリックした際に取得されるランディングページの URL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。<br><br> キーワードレベルのベース/最終 URL は、広告レベル以降の URL を上書きします。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | （情報目的で生成されたバルクシートに含まれ、広告ネットワークに投稿されない）宛先 URL を持つアカウントの場合、この値は、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定およびキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br> 最終 URL を持つアカウントの場合、この列には [!UICONTROL Base URL/Final URL column] と同じ値が表示されます。 |
| \[ 広告主固有のラベル分類\] | オプション | オプション | オプション | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 エンティティごとに分類ごとに 1 つの値のみを含めることができます（キャンペーン A の「カラー」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加する新しいコンポーネントは、自動的にラベルに関連付けられます。 製品グループのラベル分類は、単位（最も詳細な単位）レベルで適用されます。<br><br> 分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | エンティティに割り当てられている制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><br> 制約は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集 <br> 必須：削除 | 該当なし | 該当なし | キャンペーンの表示ステータス：*[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i> または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブまたは一時停止されたキャンペーンを削除するには、値「[!UICONTROL Deleted]」を入力します。 |
| [!UICONTROL Ad Group Status] | 該当なし | オプション：作成または編集 <br> 必須：削除 | 該当なし | 広告グループの表示ステータス：*[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i> または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブまたは一時停止された広告グループを削除するには、値「[!UICONTROL Deleted]」を入力します。 |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | オプション：作成または編集 <br> 必須：削除 | キーワードの表示ステータス：*[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i> または <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブまたは一時停止されたキーワードを削除するには、値「[!UICONTROL Deleted]」を入力します。 |
| [!UICONTROL Campaign ID] | なし：作成 <br> 必須/オプション：編集または削除 | オプション | オプション | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にキャンペーンの AMO ID が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 該当なし | なし：作成 <br> 必須/オプション：編集または削除 | オプション | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に広告グループの AMO ID が含まれていない限り、広告グループ名を変更する場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 該当なし：作成 <br> 必須/オプション：編集 <br> 必須：削除 | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] キーワード名を変更する場合にのみ必須です。ただし、行に（a） キーワードを識別するのに十分なプロパティ列、または（b） AMO ID が含まれる場合を除きます。 |
| [!UICONTROL AMO ID] | なし：作成 <br> オプション：編集または削除 | なし：作成 <br> オプション：編集または削除 | なし：作成 <br> オプション：編集または削除 | （生成されたバルクシート内）同期されたエンティティの [!DNL Adobe] 生成された一意の ID。 レスポンシブ検索広告の場合、[!UICONTROL Ad ID] を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つその他すべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID でデータを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）行のデータに関する検索、ソーシャル、Commerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL SE Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |

[^1]: Excel でファイルを開くと、大きな数値が指数表記（2115585666 の場合は 2.12E+09 など）に変換されます。 標準の表記で数字を表示するには、列の任意のセルを選択して、式バーの内側をクリックします。

>[!MORELIKETHIS]
>
>* [ 付録 – バルクシート エラー ](../bulksheet-errors.md)
>* [ バルクシートで実行できる操作 ](bulksheet-operations.md)
>* [ サポートされるバルクシート ファイル形式 ](bulksheet-file-formats.md)
>* [ バルクシートファイルのダウンロード/作成 ](../bulksheet-download.md)
>* [ のクリック追跡形式  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [ バルクシートファイルまたは修正されたエラーファイルのアップロード ](../bulksheet-upload.md)
>* [ 実装  [!DNL Naver]  トラッキング専用アカウント ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
