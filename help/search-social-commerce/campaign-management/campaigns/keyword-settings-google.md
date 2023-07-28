---
title: '''[!DNL Google Ads] キーワード設定'
description: 次の設定を参照してください： [!DNL Google Ads] キーワード。
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] キーワード設定

検索ネットワークとディスプレイネットワークを使用するキャンペーン用のキーワードを作成できます。

詳しくは、 Google Ads ヘルプを参照してください。 [アカウントごとのキーワード制限](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード（任意を含む） [!DNL Google Ads] キーワードとプレースホルダーの構文を一致させます。 [!DNL Google Ads] アカウントには次の属性を持つキーワードが必要です。

* 1 つのキーワードの最大長は 80 文字で、10 語以下です。
* キーワードには、文字、数字、および次の特殊文字のみを含めることができます：スペース `# $ & _ - " [] ' + . / :`

最大 2000 個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、複数のキーワードを複数の行に入力します。

>[!NOTE]
>
>* 除外キーワードは、 [!UICONTROL Keywords] > [!UICONTROL Negatives] 広告グループとキャンペーンの設定で「 」と「 」を表示します。
>* の変更 [!DNL Google Ads] キーワードまたは一致タイプは、既存のキーワードを削除し、新しいキーワードを作成します。

**[!UICONTROL Status]:** キーワードの表示ステータス： *アクティブ* または *一時停止*. 新しいキーワードのデフォルトはです。 *アクティブ*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダー

**[!UICONTROL Param1]:** ベース URL またはトラッキングテンプレートに次が含まれる場合に、置換値として使用する文字列 [の `{param1}`](https://support.google.com/google-ads/answer/6305348) 動的置換文字列。

**[!UICONTROL Param2]:** ベース URL またはトラッキングテンプレートに次が含まれる場合に、置換値として使用する文字列 [の `{param2}`](https://support.google.com/google-ads/answer/6305348) 動的置換文字列。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
