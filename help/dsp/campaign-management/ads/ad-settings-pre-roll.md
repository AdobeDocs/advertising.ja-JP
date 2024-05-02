---
title: プリロール広告設定
description: プリロール広告で使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# プリロール広告設定

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
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] およびレポートで表示します。 例えば、ユニットの種類や主要な属性（ホリデー商品のプレビュー：30 秒のプリロールなど）を記述します。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** （標準およびスキップ可能なプリロール広告のみ）広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** （標準およびスキップ可能なプリロール広告のみ）広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Player X]:** 広告ユニットの X 座標です。 デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告ユニットの Y 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

このフィールドは **[!UICONTROL Width]** フィールド。

**[!UICONTROL Player Height]:** 広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

これは **[!UICONTROL Height]** フィールド。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*、または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率を維持するかどうか（*[!UICONTROL Yes]*）または、ビデオを引き伸ばして使用可能なスペースを埋めます（*[!UICONTROL No]*）に設定します。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要に応じて広告ソースとして入力したサードパーティの VAST タグ [Advertising DSP トラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入（該当する場合）。

**[!UICONTROL Wmode]:** （インタラクティブなプリロールのみ）期間モード： *[!UICONTROL window]*, *[!UICONTROL transparent]*、または *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** （インタラクティブなプリロールのみ）潜在的なインベントリの広告プレーヤーの形式。 *[!UICONTROL VPAID]* または *[!UICONTROL VPAID & VAST]*. ビューアビリティは常に VPAID について測定されますが、VPAID &amp; VAST にはビューアビリティ測定を許可しない在庫が含まれます。 ビューアビリティ指標がキャンペーンにとって重要な場合は、この違いを考慮してください。

**[!UICONTROL Clock Number]**:（インタラクティブなプリロールのみ。英国でのみ使用され、権限を持つユーザーのみが使用できます）適切な広告がブロードキャストされるようにするために使用される一意の識別子。 この設定が適用されない場合は、空白のままにします。

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプには、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*、または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定されたに適した形式のピクセル画像の URL [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー： *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*、または *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Ad Management について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられたプレースメントのリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告仕様](ad-specs.md)
>* [DSP マクロ](/help/dsp/campaign-management/macros.md)
