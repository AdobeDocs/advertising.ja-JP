---
title: ' [!DNL Naver]  アカウントに必要なバルクシートデータ'
description: ' [!DNL Naver]  アカウントの必須ヘッダーフィールドとデータフィールドを一括シートで参照します。'
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/w87Fs-VxlSzJr-eakgPsqVVeHuufeytp3pMQ8n9LCMg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 998
ht-degree: 0%

---

# 付録 – [!DNL Naver] アカウントに必要なバルクシート データ

Search, Social, &amp; Commerceに[!DNL Naver] アカウントを設定するには、[!DNL Naver]内にバルクシート ファイルを作成し、それをSearch, Social, &amp; Commerceにアップロードします。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## 使用可能なデータフィールド

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| フィールド | キャンペーン | 広告グループ | キーワード | 説明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティのAMO IDが含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 必須/オプション | 必須/オプション | 必須/オプション | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティのAMO IDが含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 | 必須 | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Ad Group Name] | なし | 必須 | 必須 | 広告グループを識別する一意の名前。 |
| [!UICONTROL Keyword] | なし | なし | 必須 | キーワード文字列。 |
| [!UICONTROL Base URL] | なし | なし | オプション | 広告をクリックしたときにエンドユーザーが取得するランディングページのURL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。<br><br> キーワードレベルのベース/最終URLは、広告レベル以上のURLを上書きします。 |
| [!UICONTROL Destination URL] | なし | なし | なし | （生成されたバルクシートに含まれ、広告ネットワークには投稿されません）宛先URLを持つアカウントの場合、この値は、広告を広告主のweb サイト上のベース URL/ランディングページにリンクするURLです（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイト経由で送信する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URLを生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br>最終URLを持つアカウントの場合、この列は[!UICONTROL Base URL/Final URL column]と同じ値を示します。 |
| \[広告主固有ラベル分類\] | オプション | オプション | オプション | （広告主固有のラベル分類の名前。例えば、「カラー」というラベル分類の「カラー」など）エンティティに関連付けられている指定された分類の値。 エンティティごとに分類ごとに1つの値のみを含めることができます（キャンペーン Aの「カラー」ラベル分類の「赤」など）。 最大長は100文字で、値にはASCII文字と非ASCII文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も詳細）レベルに適用されます。<br><br>分類名と分類値は、大文字と小文字を区別しません。 |
| [!UICONTROL Constraints] | オプション | オプション | オプション | エンティティに割り当てられた制約。 エンティティごとに割り当てることができる制約は1つだけです。<br><br>制約は子エンティティによって継承されるので、継承された値を上書きしない限り、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign Status] | オプション：作成または編集<br>必須：削除 | なし | なし | キャンペーンの表示ステータス：*[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新規キャンペーンのデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブまたは一時停止したキャンペーンを削除するには、値「[!UICONTROL Deleted]」を入力します。 |
| [!UICONTROL Ad Group Status] | なし | オプション：作成または編集<br>必須：削除 | なし | 広告グループの表示ステータス : *[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新規広告グループのデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブな広告グループまたは一時停止した広告グループを削除するには、値「[!UICONTROL Deleted]」を入力します。 |
| [!UICONTROL Keyword Status] | なし | なし | オプション：作成または編集<br>必須：削除 | キーワードの表示ステータス : *[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブなキーワードまたは一時停止したキーワードを削除するには、値「[!UICONTROL Deleted]」を入力します。 |
| [!UICONTROL Campaign ID] | なし：作成<br>必須/オプション：編集または削除 | オプション | オプション | 既存のキャンペーンを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にキャンペーンのAMO IDが含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | なし | なし：作成<br>必須/オプション：編集または削除 | オプション | 既存の広告グループを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行に広告グループのAMO IDが含まれていない限り、広告グループ名を変更する場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | なし | なし | なし：作成<br>必須/オプション：編集<br>必須：削除 | 既存のキーワードを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にa）キーワードを識別するのに十分なプロパティ列またはb） AMO IDが含まれていない限り、キーワード名を変更する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | なし：作成<br> オプション：編集または削除 | なし：作成<br> オプション：編集または削除 | なし：作成<br> オプション：編集または削除 | （生成されたバルクシート内）同期されたエンティティに対して[!DNL Adobe]が生成した一意のID。 レスポンシブ検索広告の場合、[!UICONTROL Ad ID]を含まない限り、AMO IDは広告の編集または削除に必要です。 AMO IDを持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ IDと親エンティティ IDを含めない限り、AMO IDがデータの編集または削除に必要です。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |
| [!UICONTROL EF Error Message] | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）行のデータに関するSearch、Social、およびCommerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL SE Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |

[^1]: ファイルを開くと、Excelは大きな数値を科学表記法（2115585666の場合は2.12E+09など）に変換します。 標準表記法で数値を表示するには、列内の任意のセルを選択し、数式バー内をクリックします。

>[!MORELIKETHIS]
>
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [&#x200B; バルクシートで実行できる操作](bulksheet-operations.md)
>* [&#x200B; サポートされているバルクシート ファイル形式](bulksheet-file-formats.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](../bulksheet-download.md)
>* [の [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md) クリックトラッキング形式
>* [&#x200B; バルクシート ファイルをアップロードするか、エラーファイルを修正](../bulksheet-upload.md)
>* [&#x200B; トラッキング専用アカウントを実装 [!DNL Naver] します](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
