---
title: 接続されたテレビ広告設定
description: 接続されたテレビ広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 接続されたテレビ広告設定

## [!UICONTROL Insert Ad Tag]

*新規広告のみ*

**[!UICONTROL URL]**：広大なタグ URL。

**[!UICONTROL Title]**: ファイルの名前。広告ビューおよびレポートで使用されます。

>[!TIP]
>
> VAST タグの有効性を確認するには、ブラウザーに貼り付けて **[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部に `<VAST>` を含む XML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を [!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 30sec CTV など）を記述します。

**[!UICONTROL Width | Ad Unit Width]:** 広告ユニット全体の幅 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Height | Ad Unit Height]:** 広告単位全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Player X]:** 広告単位の X 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告単位の Y 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

これは **[!UICONTROL Width]** フィールドと同じです。

**[!UICONTROL Player Height]:** 広告単位全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

これは **[!UICONTROL Height]** フィールドと同じです。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所：*[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]* または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率（*[!UICONTROL Yes]*）を維持するか、使用可能なスペースを埋めるようにビデオをストレッチするか（*[!UICONTROL No]*）を選択します。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要な [Advertising DSP トラッキングマクロ &#x200B;](/help/dsp/campaign-management/macros.md) が挿入された広告ソースとして入力したサードパーティ VAST タグ（該当する場合）。

**[!UICONTROL Clock Number]**: （英国でのみ使用され、権限を持つユーザーのみが使用できます）適切な広告がブロードキャストされることを保証するために使用される一意の ID。 この設定が適用されない場合は、空白のままにします。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Ad Management について &#x200B;](ad-about.md)
>* [&#x200B; 単一の広告の作成 &#x200B;](ad-create.md)
>* [&#x200B; 広告に関連付けられたプレースメントのリスト &#x200B;](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [&#x200B; 広告仕様 &#x200B;](ad-specs.md)
>* [DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)
