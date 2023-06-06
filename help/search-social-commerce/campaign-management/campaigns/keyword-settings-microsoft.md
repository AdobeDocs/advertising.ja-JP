---
title: '"[!DNL Microsoft Advertising] キーワード設定'
description: 次の設定を参照してください： [!DNL Microsoft Advertising] キーワード。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キーワード設定

検索ネットワークとディスプレイネットワークを使用するキャンペーン用のキーワードを作成できます。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード（任意を含む） [!DNL Microsoft Advertising] 構文とプレースホルダーを一致させます。 キーワードごとの最大長は 100 文字です。

最大 2000 個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、複数のキーワードを複数の行に入力します。

>[!NOTE]
>
>* 除外キーワードは、 [!UICONTROL Keywords] > [!UICONTROL Negatives] 広告グループとキャンペーンの設定で「 」と「 」を表示します。
>* の変更 [!DNL Microsoft Advertising] キーワードは、既存のキーワードを削除し、新しいキーワード ID を持つ新しいキーワードを作成します。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。


**[!UICONTROL Status]:** キーワードの表示ステータス： *アクティブ* または *一時停止*. 新しいキーワードのデフォルトはです。 *アクティブ*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダー

**[!UICONTROL Param2]:** キーワードのベース URL または広告のタイトル、説明、またはベース URL にが含まれる場合に、置換値として使用する文字列 [の `{Param2}` 動的置換文字列](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 最大長は 70 文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1 とタイトル 2 の組み合わせは最大 76 文字になります）。

**[!UICONTROL Param3]:** キーワードのベース URL または広告のタイトル、説明、またはベース URL にが含まれる場合に、置換値として使用する文字列 [の `{Param3}` 動的置換文字列](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 最大長は 70 文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1 とタイトル 2 の組み合わせは最大 76 文字になります）。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

このフィールドには、オプションで `{Param2}` および `{Param3}` 動的な代替変数。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

