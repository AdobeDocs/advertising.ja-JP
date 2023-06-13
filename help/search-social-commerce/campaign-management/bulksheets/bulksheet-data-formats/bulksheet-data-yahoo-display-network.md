---
title: のバルクシートデータ [!DNL Yahoo! Display Network] アカウント
description: 次のフィールドについて、ダウンロードした一括送信シートのヘッダーフィールドとデータフィールドを参照します。 [!DNL Yahoo! Display Network] アカウント。
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 付録 — のバルクシートデータ [!DNL Yahoo! Display Network] アカウント

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

のデータをダウンロードできます [!DNL Yahoo! Display Network] アカウントを一括でアップロードしているものの、広告ネットワークにバルクシートをアップロードまたは投稿できない。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## 使用可能なデータフィールド

| フィールド | Campaign | 広告グループ | 広告 | 説明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 |
| [!UICONTROL Acct  Name] | 含まれる場合 | 含まれる場合 | 含まれる場合 | 広告ネットワークアカウントを識別する一意の名前。 |
| [!UICONTROL Campaign Name] | 含まれる場合 | 含まれる場合 | 含まれる場合 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Ad Group Name] | 該当なし | 含まれる場合 | 含まれる場合 | 広告グループを識別する一意の名前。 |
| [!UICONTROL Ad Name] | 該当なし | 該当なし | 含まれる場合 | 広告グループ内の広告を識別する一意の名前。 最大長は 50 文字です。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 含まれる場合 | 広告のヘッドライン。 |
| [!UICONTROL Description Line 1] | 該当なし | 該当なし | 含まれる場合 | 広告の本文の最初の行。 |
| [!UICONTROL Description Line 2] | 該当なし | 該当なし | 含まれる場合 | 広告の本文の 2 行目。 |
| [!UICONTROL Base URL/Final URL] | 該当なし | 該当なし | 含まれる場合 | 広告のクリック時に表示されるランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 キーワードレベルのベース/最終 URL は、広告レベル以上の URL に優先します。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | ( 情報を提供するために、生成された一括送信シートに含まれます。広告ネットワークに投稿されない ) リンク先 URL のアカウントの場合、この値は広告主の Web サイト上のベース URL/ランディングページに広告をリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを介します）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告のネットワーク固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。 |
| \[ 広告主固有のラベル分類\] | 含まれる場合 | 含まれる場合 | 含まれる場合 | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 |
| [!UICONTROL Constraints] | 含まれる場合 | 含まれる場合 | 該当なし | エンティティに割り当てられる制約。 |
| [!UICONTROL Campaign Status] | 含まれる場合 | 該当なし | 該当なし | キャンペーンの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | 該当なし | 含まれる場合 | 該当なし | 広告グループの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | 含まれる場合 | キーワードの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 |
| [!UICONTROL Campaign ID] | 含まれる場合 | 含まれる場合 | 含まれる場合 | 既存のキャンペーンを識別する一意の ID。 |
| [!UICONTROL Ad Group ID] | 該当なし | 含まれる場合 | 含まれる場合 | 既存の広告グループを識別する一意の ID。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 含まれる場合 | 既存のキーワードを識別する一意の ID。 |
| [!UICONTROL AMO ID] | 該当なし | 該当なし | 該当なし | （生成された一括送信シート内）同期されたAdobeに対してエンティティが生成した一意の識別子。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | （情報を目的として生成された一括送信シートに含まれます）行のデータに関する検索、ソーシャル、コマースからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL EF Errors] ファイル。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [バルクシートファイルのダウンロード/作成](../bulksheet-download.md)
