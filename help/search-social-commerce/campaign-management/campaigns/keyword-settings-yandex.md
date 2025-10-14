---
title: '[!DNL Yandex] キーワード設定'
description: キーワードの設定  [!DNL Yandex]  参照します。
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# [!DNL Yandex] キーワードの設定

Yandex キーワードは、検索と表示（コンテンツ）ネットワークの両方に使用されます。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワードのキーワード フレーズ。キーワードの [Yandex match type syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) を含みます。 各キーワードには、ストップワードを除いて最大 7 つのワードを含めることができます。

最大 2000 個のキーワードを入力または貼り付けできます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* [!DNL Yandex] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。
>* 各 Yandex の広告グループには、最大 200 のキーワードを含めることができます。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ* または *一時停止*。 新しいキーワードのデフォルトは *アクティブ* です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダ

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** `{param1}` および `{param2}` 代替変数の値。キーワードを使用して広告を表示した場合に、広告およびサイトリンクのベース URL にある {param1} および {param2} のインスタンスを置き換えます。 最大長は 255 バイトです。

特殊文字は UTF-8 で自動的にエンコードされます。 例えば、関連付けられている広告のベース URL が「http://www.example.com/」で、キーワードレベルの値が {param1}shoes/flats.html」の場合、広告は {param1} http://www.example.com/shoes%2Fflats.htmlにリダイレクトされます。

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
