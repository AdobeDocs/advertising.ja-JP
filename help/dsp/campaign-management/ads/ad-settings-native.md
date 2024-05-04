---
title: ネイティブのディスプレイ広告設定
description: ネイティブディスプレイ広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# ネイティブのディスプレイ広告設定

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 広告タイプはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] およびレポートで表示します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 15sec Native など）を記述します。

**[!UICONTROL Native Creative]:** モバイルインベントリでの配信を最大化する 1200 x 627 画像。 クリック **[!UICONTROL Browse]** デバイスまたはネットワーク上のファイルを探し、 **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** 視聴者を引き付ける目を引くタイトル。

**[!UICONTROL Description]:** 広告の本文。 最大長は 100 文字です。

**[!UICONTROL Landing Page]:** 広告をクリックしたときにビューアが表示される URL。

**[!UICONTROL Final Landing Page]:** この [!UICONTROL Landing Page] 必要なを含む URL [Advertising DSP トラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入（該当する場合）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 広告の広告主。

**[!UICONTROL Call to Action]:** （任意）閲覧者がこの広告を表示したときに実行する手順。

**[!UICONTROL Advertiser Logo]:** （オプション）ブランド認知度を高めるために広告に含める 1:1 の比率のロゴ。 クリック **[!UICONTROL Browse]** デバイスまたはネットワーク上のファイルを探し、 **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。 **ヒント：** を使用して、プレースメント内の複数の広告に対するサードパーティトラッキングピクセルを一度に編集するには [!UICONTROL Ad Tools] 表示、「」を参照[プレースメントの広告にサードパーティのトラッキングピクセルを添付](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).」と入力します。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプでの唯一のオプションは次のとおりです。 *[!UICONTROL Impression]*.

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
