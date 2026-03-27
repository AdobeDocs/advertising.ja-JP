---
title: ユニバーサルビデオ広告の設定
description: ユニバーサルビデオ広告で使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# ユニバーサルビデオ広告の設定

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオの配置にのみ添付できます。

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]:**&#x200B;広大なタグ URL。

**[!UICONTROL Title]:** [!UICONTROL Ads] ビューとレポートにあるファイルのタイトル。

>[!TIP]
>
> VAST タグの有効性を確認するには、そのタグをブラウザーに貼り付け、**[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部に`<VAST>`を含むXML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントタイプに対応します。

**[!UICONTROL Ad Name]:**&#x200B;広告名。 アセットタイトルはデフォルトで使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメント、[!UICONTROL Ads] ビュー、およびレポートに添付する際に見つけやすい名前を使用します。 例えば、ユニットのタイプと一部の主要属性（ホリデープロダクト プレビュー：30sec ユニバーサル ビデオなど）について説明します。

**[!UICONTROL Show Controls]:**&#x200B;広告のビデオコントロールを含める場所：*[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]*&#x200B;または&#x200B;*[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの縦横比（*[!UICONTROL Yes]*）を維持するか、ビデオを拡張して使用可能なスペース（*[!UICONTROL No]*）を埋めるか。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティ VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要な[Advertising DSP トラッキングマクロ &#x200B;](/help/dsp/campaign-management/macros.md)を挿入して広告ソースとして入力したサードパーティ VAST タグ（該当する場合）。

**[!UICONTROL Wmode]:** ウィンドウ モード：*[!UICONTROL window]*、*[!UICONTROL transparent]*、または&#x200B;*[!UICONTROL opaque]*。 この設定が適用されない場合は、空白のままにします。

**[!UICONTROL Video Format]:**&#x200B;潜在的なインベントリの広告プレーヤーの形式：*[!UICONTROL VPAID]*、*[!UICONTROL VPAID & VAST]*、または&#x200B;*[!UICONTROL VAST]*。 表示可能性は常に[!UICONTROL VPAID]に対して測定されますが、[!UICONTROL VPAID & VAST]には表示可能性の測定を許可しないインベントリが含まれています。 キャンペーンにおいてビューアビリティ指標が重要である場合、この違いを考慮する必要があります。

[!UICONTROL VAST]を使用すると、ビューアビリティの測定が許可されません。コネクテッド TVまたはインベントリをターゲットにする場合は、厳密にVAST形式のみを必要とします（通常はGoogle Ad Manager、Appnexus、SpotX、FreeWheelなどの供給元から）。 このオプションは、以前にStandard Pre-roll （VAST）またはPhone + Tablet Standard Pre-roll （VAST）プレースメント/広告と互換性があった在庫にも使用します。

**[!UICONTROL Clock Number]**: （英国でのみ使用されます。権限を持つユーザーのみが使用できます）適切な広告を確実にブロードキャストするために使用される一意の識別子。 この設定が適用されない場合は、空白のままにします。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; ユニバーサルビデオに関するFAQ](/help/dsp/campaign-management/faq-universal-video.md)
>* [Advertising DSPの広告管理について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられているプレースメントを一覧表示](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)
