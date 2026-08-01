---
title: '[!DNL Microsoft Advertising]件のレスポンシブ広告の設定'
description: ' [!DNL Microsoft Advertising]  レスポンシブ広告の設定を参照してください。'
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 0%

---

# [!DNL Microsoft Advertising]個のレスポンシブ （オーディエンス）広告の設定

レスポンシブ広告の形式は、[!DNL Microsoft Audience Network]の画像ベース、ビデオベース、コネクテッド TV ビデオベースのオーディエンス広告で利用できます。 広告ネットワークは、最も効果的な広告要素の組み合わせを使用して、レスポンシブ広告を動的に組み立てます。

## [!UICONTROL Basic Settings]

*新しい広告のみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。

**[!UICONTROL Ad Group]:**&#x200B;広告グループ。

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### 動画広告

**[!UICONTROL Videos]:** 1つのビデオ広告のURL。

**[!UICONTROL Status]:**&#x200B;広告ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。

### 画像広告）

>[!NOTE]
>
>広告ネットワークは、加盟店の商品情報と広告グループレベルのユーザーターゲティングを使用して、加盟店センターのストアにリンクされたオーディエンスキャンペーンの広告を自動的に作成します。 手動で広告を作成する必要はありません。

**[!UICONTROL Images]:**&#x200B;広告用のJPEGまたはPNG画像は最大15枚です。 1.91:1の縦横比を持つ画像を少なくとも1つ含めます。 [ オーディエンスと画像](https://help.ads.microsoft.com/#apex/ads/en/56912/0)の許可された縦横比とディメンションを参照してください。

オーディエンス広告の場合、[!DNL Microsoft Advertising]はこの画像をすべての可能な縦横比で自動的に切り抜きます。

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** ビジネス名（最大25文字）。 呼び出し専用の広告フォーマットで使用できます。

**[!UICONTROL Short Headlines]:**&#x200B;少なくとも3つ、最大15個の短い見出し。各見出しに1語以上30文字以内を使用してください。

**[!UICONTROL Long Headlines]:**&#x200B;少なくとも3つ、最大5つの長い見出し（各90文字まで）。

**[!UICONTROL Ad Text]:**&#x200B;少なくとも2文字、最大4文字の説明で、1語以上および90文字以下の説明が含まれています。

**[!UICONTROL Status]:**&#x200B;広告ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [広告の管理](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
