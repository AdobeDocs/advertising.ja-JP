---
title: '[!DNL Microsoft Advertising] キーワード設定'
description: '[!DNL Microsoft Advertising] キーワードの設定を参照してください。'
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] キーワード設定

検索ネットワークと表示ネットワークを使用するキャンペーンのキーワードを作成できます。

## [!UICONTROL Basic Settings]

*新しいキーワードのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。

**[!UICONTROL Ad Group]:**&#x200B;広告グループ。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:**&#x200B;一致する構文とプレースホルダー[!DNL Microsoft Advertising]を含むキーワード。 キーワードごとの最大長は100文字です。

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* 負のキーワードは、[!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] タブおよび広告グループとキャンペーン設定で作成できます。
>* [!DNL Microsoft Advertising] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード IDを持つ新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。 新しいキーワードのデフォルトは&#x200B;*[!UICONTROL Active]*&#x200B;です。

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** キーワードのベース URLまたは広告のタイトル、説明、ベース URLに[動的な置換文字列`{Param1}`が含まれている場合に、置換値として使用する文字列。](https://help.bingads.microsoft.com/#apex/3/en/53079/0) 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1とタイトル 2の組み合わせは最大76文字です）。

**[!UICONTROL Param2]:** キーワードのベース URLまたは広告のタイトル、説明、ベース URLに[動的な置換文字列`{Param2}`が含まれている場合に、置換値として使用する文字列。](https://help.bingads.microsoft.com/#apex/3/en/53079/0) 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1とタイトル 2の組み合わせは最大76文字です）。

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

このフィールドには、オプションで`{Param1}`および`{Param2}`の動的代替変数を含めることができます。

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理](keyword-manage.md)
