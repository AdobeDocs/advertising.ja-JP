---
title: '[!DNL Google Ads] キーワード設定'
description: ' [!DNL Google Ads]  キーワードの設定を参照してください。'
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/XwutnbHVQrg8mfimzVjv-Px6OeUsOWzT7-347-ff2C0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# [!DNL Google Ads] キーワード設定

検索ネットワークと表示ネットワークを使用するキャンペーンのキーワードを作成できます。

アカウントごとの[ キーワード制限](https://support.google.com/google-ads/answer/6372658)について、Google Ads ヘルプを参照してください。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワードとプレースホルダーの[!DNL Google Ads]一致の構文を含むキーワード。 [!DNL Google Ads] アカウントには、次の属性を持つキーワードが必要です：

* キーワードあたりの最大長は80文字で、10文字以下です。
* キーワードには、文字、数字、および次の特殊文字のみを含めることができます：スペース `# $ & _ - " [] ' + . / :`

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

>[!NOTE]
>
>* 負のキーワードは、[!UICONTROL Keywords] > [!UICONTROL Negatives] ビューと、広告グループおよびキャンペーン設定で作成できます。
>* [!DNL Google Ads] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新しいキーワードのデフォルトは&#x200B;*Active*&#x200B;です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## プレースホルダー

**[!UICONTROL Param1]:** ベース URLまたはトラッキングテンプレートに[動的な置換文字列`{param1}`](https://support.google.com/google-ads/answer/6305348)が含まれている場合に、置換値として使用する文字列。

**[!UICONTROL Param2]:** ベース URLまたはトラッキングテンプレートに[動的な置換文字列`{param2}`](https://support.google.com/google-ads/answer/6305348)が含まれている場合に、置換値として使用する文字列。

## URL オプション

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [ キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
