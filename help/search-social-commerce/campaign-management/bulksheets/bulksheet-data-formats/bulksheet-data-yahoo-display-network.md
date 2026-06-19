---
title: ' [!DNL Yahoo DSP]  アカウントの一括シートデータ'
description: ' [!DNL Yahoo DSP]  アカウントのダウンロード済みバルクシートのヘッダーフィールドとデータフィールドを参照します。'
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/cqFcEzgFtjpBzPZEUYNnXjZSb-yRDytPCQm4hqX0R9w
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 525
ht-degree: 0%

---

# 付録 – [!DNL Yahoo DSP] アカウントの一括シートデータ

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

[!DNL Yahoo DSP] （旧[!DNL Yahoo! Display Network]）アカウントのデータを一括でダウンロードできますが、バルクシートを広告ネットワークにアップロードまたは投稿することはできません。

## 使用可能なデータフィールド

| フィールド | キャンペーン | 広告グループ | 広告 | 説明 |
|----|----|----|----|----|
| [!UICONTROL Platform] | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）広告プラットフォーム。 |
| [!UICONTROL Acct  Name] | 含まれる場合 | 含まれる場合 | 含まれる場合 | 広告ネットワークアカウントを識別する一意の名前。 |
| [!UICONTROL Campaign Name] | 含まれる場合 | 含まれる場合 | 含まれる場合 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Ad Group Name] | なし | 含まれる場合 | 含まれる場合 | 広告グループを識別する一意の名前。 |
| [!UICONTROL Ad Name] | なし | なし | 含まれる場合 | 広告グループ内の広告を識別する一意の名前。 最大長は50文字です。 |
| [!UICONTROL Ad Title] | なし | なし | 含まれる場合 | 広告の見出し。 |
| [!UICONTROL Description Line 1] | なし | なし | 含まれる場合 | 広告の本文の最初の行。 |
| [!UICONTROL Description Line 2] | なし | なし | 含まれる場合 | 広告の本文の2行目。 |
| [!UICONTROL Base URL/Final URL] | なし | なし | 含まれる場合 | 広告をクリックしたときにエンドユーザーが取得するランディングページのURL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 キーワードレベルのベース/最終URLは、広告レベル以上のURLを上書きします。 |
| [!UICONTROL Destination URL] | なし | なし | なし | （生成されたバルクシートに含まれ、広告ネットワークには投稿されません）宛先URLを持つアカウントの場合、この値は、広告を広告主のweb サイト上のベース URL/ランディングページにリンクするURLです（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイト経由で送信する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URLを生成した場合、この値は、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 広告ネットワーク固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。 |
| \[広告主固有ラベル分類\] | 含まれる場合 | 含まれる場合 | 含まれる場合 | （広告主固有のラベル分類の名前。例えば、「カラー」というラベル分類の「カラー」など）エンティティに関連付けられている指定された分類の値。 |
| [!UICONTROL Constraints] | 含まれる場合 | 含まれる場合 | なし | エンティティに割り当てられた制約。 |
| [!UICONTROL Campaign Status] | 含まれる場合 | なし | なし | キャンペーンの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、または<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Status] | なし | 含まれる場合 | なし | 広告グループの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、または<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Keyword Status] | なし | なし | 含まれる場合 | キーワードの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 |
| [!UICONTROL Campaign ID] | 含まれる場合 | 含まれる場合 | 含まれる場合 | 既存のキャンペーンを識別する一意のID。 |
| [!UICONTROL Ad Group ID] | なし | 含まれる場合 | 含まれる場合 | 既存の広告グループを識別する一意のID。 |
| [!UICONTROL Keyword ID] | なし | なし | 含まれる場合 | 既存のキーワードを識別する一意のID。 |
| [!UICONTROL AMO ID] | なし | なし | なし | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意のID。 |
| [!UICONTROL EF Error Message] | なし | なし | なし | （情報目的で生成されたバルクシートに含まれる）行のデータに関するSearch、Social、およびCommerceのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL EF Errors] ファイルに含まれます。 |

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシート ファイルのダウンロードと作成](../bulksheet-download.md)
