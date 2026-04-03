---
title: '[!DNL Microsoft Advertising] キーワード設定'
description: ' [!DNL Microsoft Advertising]  キーワードの設定を参照してください。'
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/fA0ZDCw5Ici0wOfpd1kXdjbQA6DtUFxOSBEtrlJl4Oo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キーワード設定

検索ネットワークと表示ネットワークを使用するキャンペーンのキーワードを作成できます。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:**&#x200B;一致する構文とプレースホルダー[!DNL Microsoft Advertising]を含むキーワード。 キーワードごとの最大長は100文字です。

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* 負のキーワードは、[!UICONTROL Keywords] > [!UICONTROL Negatives] ビューと、広告グループおよびキャンペーン設定で作成できます。
>* [!DNL Microsoft Advertising] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード IDを持つ新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新しいキーワードのデフォルトは&#x200B;*Active*&#x200B;です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダー

**[!UICONTROL Param2]:** キーワードのベース URLまたは広告のタイトル、説明、ベース URLに[動的な置換文字列`{Param2}`が含まれている場合に、置換値として使用する文字列。](https://help.bingads.microsoft.com/#apex/3/en/53079/0) 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1とタイトル 2の組み合わせは最大76文字です）。

**[!UICONTROL Param3]:** キーワードのベース URLまたは広告のタイトル、説明、ベース URLに[動的な置換文字列`{Param3}`が含まれている場合に、置換値として使用する文字列。](https://help.bingads.microsoft.com/#apex/3/en/53079/0) 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1とタイトル 2の組み合わせは最大76文字です）。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

このフィールドには、オプションで`{Param2}`および`{Param3}`の動的代替変数を含めることができます。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
