---
title: モバイル広告設定
description: モバイル広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# モバイル広告設定

## [!UICONTROL Insert Ad Tag]

*新しいモバイルビデオ広告形式のみ*

**[!UICONTROL URL]** または **[!UICONTROL Ad Tag]**：クリエイティブアセットとトラッキングピクセルを含む、サードパーティの膨大な広告タグまたは広告タグ

**[!UICONTROL Ad Title]** または **[!UICONTROL Title]**:[!UICONTROL Ads] ビューおよびレポートで使用される広告の名前。

>[!TIP]
>
> VAST タグの有効性を確認するには、ブラウザーに貼り付けて **[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部に `<VAST>` を含む XML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]：モバイル表示広告

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付するとき、広告ビューおよびレポートで見つけやすい名前を使用します。 例えば、ユニットのタイプや主要な属性（Holiday Product Preview: 300x250 Gamer など）を記述します。

**\[Ad Source\]**: （読み取り専用） *[!UICONTROL 3rd party]*。

**[!UICONTROL Display Code]:** サードパーティのクリエイティブアセットの URL。 [timestamp] および [[timestamp]] パラメーターは、実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** サードパーティのクリエイティブアセットの URL で、必要な [Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md) が挿入されています（該当する場合）。

### [!UICONTROL Basic]：ビデオ広告

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付するとき、広告ビューおよびレポートで見つけやすい名前を使用します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 30sec Phone Preroll など）を記述します。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** 広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** 広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

**[!UICONTROL Player X]:** 広告単位の X 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Y]:** 広告単位の Y 座標。 デフォルト設定のままにします。

**[!UICONTROL Player Width]:** 広告ユニット全体の幅 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

これは **[!UICONTROL Width]** フィールドと同じです。

**[!UICONTROL Player Height]:** 広告単位全体の高さ。 このオプションは、選択した広告ユニットのタイプによってロックされる場合があります。

これは **[!UICONTROL Height]** フィールドと同じです。

**[!UICONTROL Show Controls]:** 広告のビデオコントロールを含める場所：*[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]* または *[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの比率（*[!UICONTROL Yes]*）を維持するか、使用可能なスペースを埋めるようにビデオをストレッチするか（*[!UICONTROL No]*）を選択します。

**[!UICONTROL Close Button Delay]:** （一部の広告タイプ）「閉じる」ボタンの表示を遅延させる秒数。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用） クリエイティブアセットとして入力したサードパーティの VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要な [Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md) が挿入されたクリエイティブアセットとして入力したサードパーティ VAST タグ（該当する場合）。

**[!UICONTROL Wmode]:** （一部の広告タイプ）ウィンドウモード：*[!UICONTROL window]*、*[!UICONTROL transparent]*、*[!UICONTROL opaque]*。

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。 **ヒント：** [!UICONTROL Ad Tools] ビューを使用して、プレースメント内の複数の広告に対して一度にサードパーティトラッキングピクセルを編集するには、「[ プレースメント内の広告にサードパーティトラッキングピクセルを添付する ](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)」を参照してください。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプには、*[!UICONTROL Impression]* または *[!UICONTROL Click-through]* で発生するピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、*[!UICONTROL HTML]*、*[!UICONTROL JavaScript URL]* のどれであるかを示します。

**[!UICONTROL Pixel URL or Code]:** ピクセル画像の URL を、指定した [!UICONTROL Pixel Type] に適した形式で指定します。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]* または *[!UICONTROL IAS]*。

### [!UICONTROL Sharing]

非推奨

>[!MORELIKETHIS]
>
>* [Ad Management について ](ad-about.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ 広告に関連付けられたプレースメントのリスト ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ 広告仕様 ](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
