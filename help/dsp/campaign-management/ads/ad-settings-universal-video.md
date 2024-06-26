---
title: ユニバーサルビデオ広告設定
description: ユニバーサルビデオ広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# ユニバーサルビデオ広告設定

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオプレースメントにのみ添付できます。

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]:** 広大なタグ URL。

**[!UICONTROL Title]:** ファイルのタイトル。これは、 [!UICONTROL Ads] とレポートを表示します。

>[!TIP]
>
> VAST タグの有効性を確認するには、それをブラウザーに貼り付けて、 **[!UICONTROL Enter]** キー。 タグが有効な場合、を含む XML ファイルが表示されます `<VAST>` 上部の近く。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] およびレポートで表示します。 例えば、ユニットのタイプや主要な属性（Holiday Product Preview: 30sec Universal Video など）を記述します。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*、または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率を維持するかどうか（*[!UICONTROL Yes]*）または、ビデオを引き伸ばして使用可能なスペースを埋めます（*[!UICONTROL No]*）に設定します。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要に応じて広告ソースとして入力したサードパーティの VAST タグ [Advertising DSP トラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入（該当する場合）。

**[!UICONTROL Wmode]:** ウィンドウモード： *[!UICONTROL window]*, *[!UICONTROL transparent]*、または *[!UICONTROL opaque]*. この設定が適用されない場合は、空白のままにします。

**[!UICONTROL Video Format]:** 潜在的なインベントリの広告プレーヤーの形式： *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*、または *[!UICONTROL VAST]*. ビューアビリティは、常に次の項目について測定されます。 [!UICONTROL VPAID]しかし、 [!UICONTROL VPAID & VAST] ビューアビリティ測定を許可しない在庫を含みます。 ビューアビリティ指標がキャンペーンにとって重要な場合は、この違いを考慮してください。

使用方法 [!UICONTROL VAST]（通常、Google Ad Manager、Appnexus、SpotX、Freewheel などの供給源からの） VAST フォーマットのみを必要とする接続されたテレビや在庫をターゲットにする場合、ビューアビリティの測定はできません。 また、以前は標準プレロール（VAST）または電話+ タブレット標準プレロール（VAST）のプレースメント/広告と互換性があったインベントリにも、このオプションを使用します。

**[!UICONTROL Clock Number]**:（英国でのみ使用され、権限を持つユーザーのみが使用できます）適切な広告がブロードキャストされるようにするために使用される一意の ID。 この設定が適用されない場合は、空白のままにします。

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。 **ヒント：** を使用して、プレースメント内の複数の広告に対するサードパーティトラッキングピクセルを一度に編集するには [!UICONTROL Ad Tools] 表示、「」を参照[プレースメントの広告にサードパーティのトラッキングピクセルを添付](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).」と入力します。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプには、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*、または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定されたに適した形式のピクセル画像の URL [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*、または *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
>* [Ad Management について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられたプレースメントのリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告仕様](ad-specs.md)
>* [DSP マクロ](/help/dsp/campaign-management/macros.md)
