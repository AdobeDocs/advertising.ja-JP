---
title: '"[!DNL Yandex] キーワード設定'
description: 次の設定を参照してください： [!DNL Yandex] キーワード。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] キーワード設定

Yandex キーワードは、検索とディスプレイ（コンテンツ）の両方のネットワークに使用されます。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワードフレーズ（任意を含む） [Yandex 一致タイプの構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html) （キーワード用） 各キーワードは、ストップワードを除く最大 7 語まで指定できます。

最大 2000 個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、複数のキーワードを複数の行に入力します。

>[!NOTE]
>
>* の変更 [!DNL Yandex] キーワードまたは一致タイプは、既存のキーワードを削除し、新しいキーワードを作成します。
>* 各 Yandex 広告グループには、最大 200 個のキーワードを含めることができます。


**[!UICONTROL Status]:** キーワードの表示ステータス： *アクティブ* または *一時停止*. 新しいキーワードのデフォルトはです。 *アクティブ*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダー

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** の値 `{param1}` および `{param2}` 代替変数。広告の表示にキーワードが使用された際に、広告およびサイトリンクのベース URL の {param1} および {param2} のインスタンスで置き換えられます。 最大長は 255 バイトです。

特殊文字は UTF-8 で自動的にエンコードされます。 例えば、関連する広告のベース URL が「http://www.example.com/{param1}」で、キーワードレベルの値が {param1} が「shoes/flats.html」の場合、広告はhttp://www.example.com/shoes%2Fflats.htmlになります。

>[!MORELIKETHIS]
>
>* [キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

