---
title: オーディオ広告の設定
description: オーディオ広告で使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
TQID: https://experienceleague.adobe.com/rP0SJspXvqzivctnNqe7b35mbL-ARZlGzC3cLAS-uwA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 0%

---

# オーディオ広告の設定

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]**：広大なタグ URL。

**[!UICONTROL Title]**: [!UICONTROL Ads] ビューとレポートで使用されるファイルの名前。

>[!TIP]
>
> VAST タグの有効性を確認するには、そのタグをブラウザーに貼り付け、**[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部の近くに`<VAST>`を含むXML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントタイプに対応します。 デフォルトは&#x200B;*[!UICONTROL Audio]*&#x200B;です。

**[!UICONTROL Ad Name]:**&#x200B;広告名。 アセットタイトルはデフォルトで使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメント、[!UICONTROL Ads] ビュー、およびレポートに添付する際に見つけやすい名前を使用します。 例えば、ユニットのタイプと一部の主要属性（ホリデープロダクト プレビュー：30sec オーディオなど）を説明します。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。 選択した広告ユニットに応じて、[!UICONTROL 15]または[!UICONTROL 30]のいずれかに自動的に設定されます。

このフィールドは、アカウントの権限に応じて表示される場合とされない場合があります。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ）サードパーティ広告ソースのURL。 VAST タグにオーディオメディアファイルのみが含まれていることを確認します。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ）必要な[Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md)が挿入されたサードパーティ広告ソースのURL （該当する場合）。

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ） Adobeを通じて請求された事前交渉済み料金、または交渉した料金のうち、ベンダーを通じて請求された料金。 料金を追加するには、Adobe アカウントチームにお問い合わせください。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Advertising DSPの広告管理について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられているプレースメントを一覧表示](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
