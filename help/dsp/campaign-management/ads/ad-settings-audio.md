---
title: オーディオ広告設定
description: オーディオ広告に使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# オーディオ広告設定

## [!UICONTROL Insert Ad Tag]

*新規広告のみ*

**[!UICONTROL URL]**：広大なタグ URL。

**[!UICONTROL Title]**: ファイルの名前。[!UICONTROL Ads] ビューおよびレポートで使用されます。

>[!TIP]
>
> VAST タグの有効性を確認するには、ブラウザーに貼り付けて **[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部に `<VAST>` を含む XML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。 デフォルト値は *[!UICONTROL Audio]* です。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を [!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 30sec Audio など）を記述します。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。 選択した広告ユニットに応じて、自動的に [!UICONTROL 15] または [!UICONTROL 30] に設定されます。

このフィールドは、アカウントの権限に応じて、表示される場合とされない場合があります。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ）サードパーティの広告ソースの URL。 VAST タグにはオーディオメディアファイルのみが含まれていることを確認してください。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ）必要な [Advertising DSP トラッキングマクロが挿入されたサードパーティの広告ソースの URL](/help/dsp/campaign-management/macros.md) 該当する場合）。

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ） Adobeを通じて請求される事前交渉済みの料金、または交渉し、ベンダーを通じて請求される料金の 1 つ。 評価を追加するには、Adobe アカウントチームにお問い合わせください。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Ad Management について ](ad-about.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ 広告に関連付けられたプレースメントのリスト ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ 広告仕様 ](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
