---
title: プリロール広告設定
description: プリロール広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# プリロール広告設定

## [!UICONTROL Insert Ad Tag]

*新規広告のみ*

**[!UICONTROL URL]:** 広大なタグ URL。

**[!UICONTROL Title]:** ファイルのタイトル。[!UICONTROL Ads] ビューおよびレポートに表示されます。

>[!TIP]
>
> VAST タグの有効性を確認するには、ブラウザーに貼り付けて **[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部に `<VAST>` を含む XML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を [!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットの種類や主要な属性（ホリデー商品のプレビュー：30 秒のプリロールなど）を記述します。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** （標準およびスキップ可能なプリロール広告のみ）広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** （標準およびスキップ可能なプリロール広告のみ）広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Player X]:** 広告単位の X 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告単位の Y 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

このフィールドは **[!UICONTROL Width]** フィールドと同じです。

**[!UICONTROL Player Height]:** 広告単位全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

これは **[!UICONTROL Height]** フィールドと同じです。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所：*[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]* または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率（*[!UICONTROL Yes]*）を維持するか、使用可能なスペースを埋めるようにビデオをストレッチするか（*[!UICONTROL No]*）を選択します。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要な [Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md) が挿入された広告ソースとして入力したサードパーティ VAST タグ（該当する場合）。

**[!UICONTROL Wmode]:** （インタラクティブなプリロールのみ）ウィンドウモード：*[!UICONTROL window]*、*[!UICONTROL transparent]* または *[!UICONTROL opaque]*。

**[!UICONTROL Video Format]:** （インタラクティブなプリロールのみ）潜在的なインベントリの広告プレーヤーの形式：*[!UICONTROL VPAID]* または *[!UICONTROL VPAID & VAST]*。 ビューアビリティは常に VPAID について測定されますが、VPAID &amp; VAST にはビューアビリティ測定を許可しない在庫が含まれます。 ビューアビリティ指標がキャンペーンにとって重要な場合は、この違いを考慮してください。

**[!UICONTROL Clock Number]**: （インタラクティブなプリロールのみ。英国でのみ使用され、権限を持つユーザーのみが使用できます）適切な広告がブロードキャストされることを保証するために使用される一意の ID。 この設定が適用されない場合は、空白のままにします。

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
