---
title: アカウントのバルクシ  [!DNL Yahoo! Display Network]  ト データ
description: ダウンロードしたアカウント用バルクシートのヘッダーフィールド  [!DNL Yahoo! Display Network]  データフィールドを参照します。
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# 付録 – [!DNL Yahoo! Display Network] アカウントのバルクシート データ

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

[!DNL Yahoo! Display Network] アカウントのデータを一括でダウンロードできますが、広告ネットワークにバルクシートをアップロードまたは投稿することはできません。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## 使用可能なデータフィールド

| フィールド | キャンペーン | 広告グループ | 広告 | 説明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 |
| [!UICONTROL Acct  Name] | 含める場合 | 含める場合 | 含める場合 | 広告ネットワークアカウントを識別する一意の名前。 |
| [!UICONTROL Campaign Name] | 含める場合 | 含める場合 | 含める場合 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Ad Group Name] | 該当なし | 含める場合 | 含める場合 | 広告グループを識別する一意の名前。 |
| [!UICONTROL Ad Name] | 該当なし | 該当なし | 含める場合 | 広告グループ内の広告を識別する一意の名前。 最大長は 50 文字です。 |
| [!UICONTROL Ad Title] | 該当なし | 該当なし | 含める場合 | 広告の見出し。 |
| [!UICONTROL Description Line 1] | 該当なし | 該当なし | 含める場合 | 広告の本文の最初のライン。 |
| [!UICONTROL Description Line 2] | 該当なし | 該当なし | 含める場合 | 広告の本文の 2 行目。 |
| [!UICONTROL Base URL/Final URL] | 該当なし | 該当なし | 含める場合 | エンドユーザーが広告をクリックした際に取得されるランディングページの URL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 キーワードレベルのベース/最終 URL は、広告レベル以降の URL を上書きします。 |
| [!UICONTROL Destination URL] | 該当なし | 該当なし | 該当なし | （情報目的で生成されたバルクシートに含まれ、広告ネットワークに投稿されない）宛先 URL を持つアカウントの場合、この値は、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、この値は、アカウント設定およびキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。 |
| \[ 広告主固有のラベル分類\] | 含める場合 | 含める場合 | 含める場合 | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 |
| [!UICONTROL Constraints] | 含める場合 | 含める場合 | 該当なし | エンティティに割り当てられている制約。 |
| [!UICONTROL Campaign Status] | 含める場合 | 該当なし | 該当なし | キャンペーンの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Status] | 該当なし | 含める場合 | 該当なし | 広告グループの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Keyword Status] | 該当なし | 該当なし | 含める場合 | キーワードの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 |
| [!UICONTROL Campaign ID] | 含める場合 | 含める場合 | 含める場合 | 既存のキャンペーンを識別する一意の ID。 |
| [!UICONTROL Ad Group ID] | 該当なし | 含める場合 | 含める場合 | 既存の広告グループを識別する一意の ID。 |
| [!UICONTROL Keyword ID] | 該当なし | 該当なし | 含める場合 | 既存のキーワードを識別する一意の ID。 |
| [!UICONTROL AMO ID] | 該当なし | 該当なし | 該当なし | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意の ID。 |
| [!UICONTROL EF Error Message] | 該当なし | 該当なし | 該当なし | （情報提供のために生成されたバルクシートに含まれる）行のデータに関する検索、ソーシャル、Commerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL EF Errors] ファイルに含まれます。 |

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートファイルのダウンロード/作成 &#x200B;](../bulksheet-download.md)
