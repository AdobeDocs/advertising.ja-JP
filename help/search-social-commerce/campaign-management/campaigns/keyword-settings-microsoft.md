---
title: '[!DNL Microsoft Advertising] キーワード設定'
description: キーワードの設定  [!DNL Microsoft Advertising]  参照します。
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キーワードの設定

検索および表示ネットワークを使用するキャンペーンのキーワードを作成できます。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:**&#x200B;[!DNL Microsoft Advertising] 一致の構文とプレースホルダーを含むキーワード。 キーワードごとの最大長は 100 文字です。

最大 2000 個のキーワードを入力または貼り付けできます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* ネガティブキーワードは、[!UICONTROL Keywords] / [!UICONTROL Negatives] ビューや、広告グループおよびキャンペーン設定で作成できます。
>* [!DNL Microsoft Advertising] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード ID で新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ* または *一時停止*。 新しいキーワードのデフォルトは *アクティブ* です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダ

**[!UICONTROL Param2]:** キーワードのベース URL または広告のタイトル、説明、またはベース URL に [`{Param2}` 動的な置換文字列 &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/53079/0) が含まれる場合に、置換値として使用する文字列。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、タイトル 1 とタイトル 2 を組み合わせると、最大 76 文字になる場合があります）。

**[!UICONTROL Param3]:** キーワードのベース URL または広告のタイトル、説明、またはベース URL に [`{Param3}` 動的な置換文字列 &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/53079/0) が含まれる場合に、置換値として使用する文字列。 最大長は 70 文字ですが、これを使用する広告要素の最大長には注意が必要です（例えば、タイトル 1 とタイトル 2 を組み合わせると、最大 76 文字になる場合があります）。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

このフィールドには、オプションで `{Param2}` および `{Param3}` の動的置換変数を含めることができます。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
