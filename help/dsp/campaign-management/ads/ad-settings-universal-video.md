---
title: ユニバーサルビデオ広告設定
description: ユニバーサルビデオ広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# ユニバーサルビデオ広告設定

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオプレースメントにのみ添付できます。

## [!UICONTROL Insert Ad Tag]

*新規広告のみ*

**[!UICONTROL URL]:** 広大なタグ URL。

**[!UICONTROL Title]:** ファイルのタイトル。[!UICONTROL Ads] ビューおよびレポートに表示されます。

>[!TIP]
>
> VAST タグの有効性を確認するには、ブラウザーに貼り付けて **[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、`<VAST>` を含む XML ファイルが上部に表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を [!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットのタイプや主要な属性（Holiday Product Preview: 30sec Universal Video など）を記述します。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所：*[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]* または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率（*[!UICONTROL Yes]*）を維持するか、使用可能なスペースを埋めるようにビデオをストレッチするか（*[!UICONTROL No]*）を選択します。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要な [Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md) が挿入された広告ソースとして入力したサードパーティ VAST タグ（該当する場合）。

**[!UICONTROL Wmode]:** ウィンドウモード：*[!UICONTROL window]*、*[!UICONTROL transparent]* または *[!UICONTROL opaque]*。 この設定が適用されない場合は、空白のままにします。

**[!UICONTROL Video Format]:** 潜在的なインベントリの広告プレーヤーの形式：*[!UICONTROL VPAID]*、*[!UICONTROL VPAID & VAST]* または *[!UICONTROL VAST]*。 ビューアビリティは [!UICONTROL VPAID] に対して常に測定されますが、ビューアビリティの測定を許可しないインベントリは [!UICONTROL VPAID & VAST] に含まれます。 ビューアビリティ指標がキャンペーンにとって重要な場合は、この違いを考慮してください。

厳密に VAST フォーマットのみを必要とするコネクテッド TV や在庫（通常はGoogle Ad Manager、Appnexus、SpotX、Freewheel などの供給源から）をターゲットにする場合は、ビューアビリティ測定を許可しない [!UICONTROL VAST] を使用します。 また、以前は標準プレロール（VAST）または電話+ タブレット標準プレロール（VAST）のプレースメント/広告と互換性があったインベントリにも、このオプションを使用します。

**[!UICONTROL Clock Number]**: （英国でのみ使用され、権限を持つユーザーのみが使用できます）適切な広告がブロードキャストされることを保証するために使用される一意の ID。 この設定が適用されない場合は、空白のままにします。

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。 **ヒント：** [!UICONTROL Ad Tools] ビューを使用して、プレースメント内の複数の広告に対して一度にサードパーティトラッキングピクセルを編集するには、「[ プレースメント内の広告にサードパーティトラッキングピクセルを添付する ](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)」を参照してください。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプには、*[!UICONTROL Impression]* または *[!UICONTROL Click-through]* で発生するピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、*[!UICONTROL HTML]*、*[!UICONTROL JavaScript URL]* のどれであるかを示します。

**[!UICONTROL Pixel URL or Code]:** ピクセル画像の URL を、指定した [!UICONTROL Pixel Type] に適した形式で指定します。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]* または *[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [ ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
>* [Ad Management について ](ad-about.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ 広告に関連付けられたプレースメントのリスト ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ 広告仕様 ](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
