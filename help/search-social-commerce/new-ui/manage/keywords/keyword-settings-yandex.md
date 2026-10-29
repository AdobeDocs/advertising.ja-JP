---
title: '[!DNL Yandex] キーワード設定'
description: '[!DNL Yandex] キーワードの設定を参照してください。'
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
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex] キーワード設定

検索ネットワークと表示（コンテンツ）ネットワークの両方に[!DNL Yandex] キーワードが使用されます。

## [!UICONTROL Basic Settings]

*新しいキーワードのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。

**[!UICONTROL Ad Group]:**&#x200B;広告グループ。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード用の[[!DNL Yandex] 一致タイプ構文](https://yandex.com/support/direct/keywords/symbols-and-operators.html)を含むキーワードフレーズ。 各キーワードには、ストップワードを除く最大7つの単語を含めることができます。

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* [!DNL Yandex] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。
>* 各[!DNL Yandex]広告グループには、最大200個のキーワードを含めることができます。

**[!UICONTROL Status]:** キーワードの表示ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。 新しいキーワードのデフォルトは&#x200B;*[!UICONTROL Active]*&#x200B;です。

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>特殊文字はUTF-8で自動的にエンコードされます。 例えば、関連付けられた広告のベース URLが`http://www.example.com/{param1}`で、キーワードレベルの値`{param1}`が`shoes/flats.html`の場合、広告は`http://www.example.com/shoes%2Fflats.html`につながります。

**[!UICONTROL Param1]:**&#x200B;広告の表示にキーワードを使用する場合、ベース URLに広告およびサイトリンクの`{param1}`動的な置換文字列が含まれている場合に、置換値として使用する文字列。 最大長は255 バイトです。

**[!UICONTROL Param2]:**&#x200B;広告の表示にキーワードを使用する場合、ベース URLに広告およびサイトリンクの`{param2}`動的な置換文字列が含まれている場合に、置換値として使用する文字列。 最大長は255 バイトです。

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理](keyword-manage.md)
