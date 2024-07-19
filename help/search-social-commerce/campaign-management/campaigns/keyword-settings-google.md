---
title: '[!DNL Google Ads] キーワード設定'
description: キーワードの設定  [!DNL Google Ads]  参照します。
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# [!DNL Google Ads] キーワードの設定

検索および表示ネットワークを使用するキャンペーンのキーワードを作成できます。

[ アカウントごとのキーワード制限 ](https://support.google.com/google-ads/answer/6372658) について詳しくは、Google Ads のヘルプを参照してください。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワードとプレースホルダーの [!DNL Google Ads] 一致構文を含むキーワード。 [!DNL Google Ads] アカウントには、次の属性を持つキーワードが必要です。

* キーワードごとの最大長は 80 文字、10 語以内です。
* キーワードには、文字、数字、および次の特殊文字のみを含めることができます。スペース `# $ & _ - " [] ' + . / :`

最大 2000 個のキーワードを入力または貼り付けできます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* ネガティブキーワードは、[!UICONTROL Keywords] / [!UICONTROL Negatives] ビューや、広告グループおよびキャンペーン設定で作成できます。
>* [!DNL Google Ads] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ* または *一時停止*。 新しいキーワードのデフォルトは *アクティブ* です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダ

**[!UICONTROL Param1]:** ベース URL またはトラッキングテンプレートに [`{param1}`](https://support.google.com/google-ads/answer/6305348) の動的置換文字列が含まれる場合に、置換値として使用する文字列。

**[!UICONTROL Param2]:** ベース URL またはトラッキングテンプレートに [`{param2}`](https://support.google.com/google-ads/answer/6305348) の動的置換文字列が含まれる場合に、置換値として使用する文字列。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [ キーワードの管理 ](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
