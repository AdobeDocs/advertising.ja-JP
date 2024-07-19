---
title: '[!DNL Baidu] キーワード設定'
description: キーワードの設定  [!DNL Baidu]  参照します。
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu] キーワードの設定

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード。 キーワードごとの最大長は、30 個の 1 バイト文字または 15 個の 2 バイト文字です

最大 2000 個のキーワードを入力または貼り付けできます。 複数のキーワードをコンマで区切るか、別々の行に入力します。 次の構文を使用します。

* 部分一致の `keyword`
* フレーズ一致の `"keyword"`
* 完全一致の `[keyword]`

>[!NOTE]
>
>* [!DNL Baidu] では、広告グループごとにキーワードごとに 1 つの一致タイプのみを使用できます。 例えば、広告グループ 1 に `"keyword"` と `[keyword]` の両方を含めることはできません。
>* ネガティブキーワードは、[!UICONTROL Keywords] / [!UICONTROL Negatives] ビューや、広告グループおよびキャンペーン設定で作成できます。
>* [!DNL Baidu] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード ID で新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ* または *一時停止*。 新しいキーワードのデフォルトは *アクティブ* です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL オプション

**[!UICONTROL Base URL]:** （キーワードレベルのトラッキングのみを使用するキャンペーン。オプション）ユーザーが広告をクリックした際に取得されるランディングページの URL。 これには以下が含まれます
サードパーティのリダイレクトとトラッキングコード。 値を入力すると、広告のベース URL が上書きされます。

レコードを保存すると、ベース URL には、キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。

Adobe Advertisingコンバージョントラッキングサービスを使用し、キャンペーン設定に [!UICONTROL EF Redirect] の使用とキーワードレベルでのトラッキングの追加が含まれる場合、検索、ソーシャル、Commerceには独自のクリック追跡コードが自動的に追加されます。

>[!MORELIKETHIS]
>
>* [ キーワードの管理 ](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
