---
title: '[!DNL Yandex] キーワード設定'
description: ' [!DNL Yandex]  キーワードの設定を参照してください。'
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/-PRiQ9myH0XNYF8pc2OVBuLOK-8BpxzqruOP2hzPW0I
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# [!DNL Yandex] キーワード設定

Yandex キーワードは、検索ネットワークとディスプレイ（コンテンツ）ネットワークの両方に使用されます。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード用の[Yandex一致タイプ構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html)を含むキーワードフレーズ。 各キーワードには、ストップワードを除く最大7つの単語を含めることができます。

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* [!DNL Yandex] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。
>* Yandex広告グループには、最大200個のキーワードを含めることができます。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新しいキーワードのデフォルトは&#x200B;*Active*&#x200B;です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダー

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** キーワードを使用して広告を表示する際に、広告とサイトリンクのベース URLの`{param1}`と`{param2}`の任意のインスタンスに置き換えられる{param1}と{param2}の代用変数の値。 最大長は255 バイトです。

特殊文字はUTF-8で自動的にエンコードされます。 例えば、関連付けられた広告のベース URLが「http://www.example.com/{param1}」で、キーワードレベルの値{param1}が「shoes/flats.html」の場合、広告はhttp://www.example.com/shoes%2Fflats.htmlに導きます。

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
