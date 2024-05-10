---
title: '''[!DNL Microsoft Advertising] キーワード設定'
description: の設定を参照します [!DNL Microsoft Advertising] キーワード。
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キーワード設定

検索および表示ネットワークを使用するキャンペーンのキーワードを作成できます。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード （いずれか） [!DNL Microsoft Advertising] 構文とプレースホルダーを一致させます。 キーワードごとの最大長は 100 文字です。

最大 2000 個のキーワードを入力または貼り付けできます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* からネガティブキーワードを作成できます [!UICONTROL Keywords] > [!UICONTROL Negatives] 広告グループとキャンペーンの設定にとを表示します。
>* 変更， [!DNL Microsoft Advertising] keyword 既存のキーワードを削除し、新しいキーワード ID で新しいキーワードを作成します。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス： *アクティブ* または *一時停止*. 新しいキーワードのデフォルトは *アクティブ*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダ

**[!UICONTROL Param2]:** キーワードのベース URL または広告のタイトル、説明、ベース URL に「」が含まれる場合に、置換値として使用する文字列 [この `{Param2}` 動的置換文字列](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、タイトル 1 とタイトル 2 を組み合わせると、最大 76 文字になる場合があります）。

**[!UICONTROL Param3]:** キーワードのベース URL または広告のタイトル、説明、ベース URL に「」が含まれる場合に、置換値として使用する文字列 [この `{Param3}` 動的置換文字列](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、タイトル 1 とタイトル 2 を組み合わせると、最大 76 文字になる場合があります）。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

このフィールドには、オプションで `{Param2}` および `{Param3}` 動的代替変数。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
