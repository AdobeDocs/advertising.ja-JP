---
title: '''[!DNL Baidu] キーワード設定'
description: 次の設定を参照してください： [!DNL Baidu] キーワード。
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] キーワード設定

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード。 1 つのキーワードの最大長は、1 バイト文字 30 文字または 2 バイト文字 15 文字です

最大 2000 個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、複数のキーワードを複数の行に入力します。 次の構文を使用します。

* `keyword` 幅広い一致を求めて
* `"keyword"` （フレーズ一致の場合）
* `[keyword]` 完全一致

>[!NOTE]
>
>* [!DNL Baidu] では、広告グループごとに 1 つのキーワードにつき 1 つの一致タイプのみを使用できます。 例えば、広告グループ 1 に `"keyword"` および `[keyword]`.
>* 除外キーワードは、 [!UICONTROL Keywords] > [!UICONTROL Negatives] 広告グループとキャンペーンの設定で「 」と「 」を表示します。
>* の変更 [!DNL Baidu] キーワードは、既存のキーワードを削除し、新しいキーワード ID を持つ新しいキーワードを作成します。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス： *アクティブ* または *一時停止*. 新しいキーワードのデフォルトはです。 *アクティブ*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL オプション

**[!UICONTROL Base URL]:** （キーワードレベルのトラッキングのみを含むキャンペーン、オプション）ユーザーが広告をクリックしたときに表示されるランディングページの URL。 サードパーティのリダイレクトやトラッキングコードを含めることができます。 値を入力すると、広告のベース URL よりも優先されます。

レコードを保存すると、ベース URL にはキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。

Adobe Advertisingコンバージョントラッキングサービスを使用し、キャンペーン設定で [!UICONTROL EF Redirect] キーワードレベルで追跡を追加すると、検索、ソーシャル、コマースによって、独自のクリック追跡コードが自動的に追加されます。

>[!MORELIKETHIS]
>
>* [キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
