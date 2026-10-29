---
title: '[!DNL Google Ads] キーワード設定'
description: '[!DNL Google Ads] キーワードの設定を参照してください。'
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%
---
# [!DNL Google Ads] キーワード設定

検索ネットワークと表示ネットワークを使用するキャンペーンのキーワードを作成できます。

アカウントごとの[ キーワード制限](https://support.google.com/google-ads/answer/6372658)について、[!DNL Google Ads]のヘルプを参照してください。

## [!UICONTROL Basic Settings]

*新しいキーワードのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。

**[!UICONTROL Ad Group]:**&#x200B;広告グループ。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワードとプレースホルダーの[!DNL Google Ads]一致の構文を含むキーワード。 [!DNL Google Ads] アカウントには、次の属性を持つキーワードが必要です：

* キーワードあたりの最大長は80文字で、10文字以下です。

* キーワードには、文字、数字、および次の特殊文字のみを含めることができます：スペース `# $ & _ - " [] ' + . / :`

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* 負のキーワードは、[!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] タブおよび広告グループとキャンペーン設定で作成できます。
>* [!DNL Google Ads] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。

**[!UICONTROL Status]:** キーワードの表示ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。 新しいキーワードのデフォルトは&#x200B;*[!UICONTROL Active]*&#x200B;です。

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** ベース URLまたはトラッキングテンプレートに[動的な置換文字列`{param1}`](https://support.google.com/google-ads/answer/6305348)が含まれている場合に、置換値として使用する文字列。

**[!UICONTROL Param2]:** ベース URLまたはトラッキングテンプレートに[動的な置換文字列`{param2}`](https://support.google.com/google-ads/answer/6305348)が含まれている場合に、置換値として使用する文字列。

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [ キーワードの管理](keyword-manage.md)
