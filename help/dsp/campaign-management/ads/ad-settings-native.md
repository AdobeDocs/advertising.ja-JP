---
title: ネイティブのディスプレイ広告設定
description: ネイティブディスプレイ広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# ネイティブのディスプレイ広告設定

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。

**[!UICONTROL Ad Name]:** 広告名。 広告タイプはデフォルトで使用されますが、名前は変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、[!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 15sec Native など）を記述します。

**[!UICONTROL Native Creative]:** モバイルインベントリでの配信を最大化するための 1200 x 627 画像。 [**[!UICONTROL Browse]**] をクリックし、デバイスまたはネットワーク上のファイルを探して、[**[!UICONTROL Upload]**] をクリックします。

**[!UICONTROL Title]:** 視聴者を惹きつける人目を引くタイトル。

**[!UICONTROL Description]:** 広告の本文。 最大長は 100 文字です。

**[!UICONTROL Landing Page]:** ビューアが広告をクリックしたときに表示される URL。

**[!UICONTROL Final Landing Page]:** 必要な [!UICONTROL Landing Page]Advertising DSP トラッキングマクロ [&#x200B; が挿入された &#x200B;](/help/dsp/campaign-management/macros.md) URL （該当する場合）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 広告の広告主。

**[!UICONTROL Call to Action]:** （任意）この広告を表示した視聴者に実行させる手順。

**[!UICONTROL Advertiser Logo]:** （オプション）ブランド認知度を高めるために広告に含める 1:1 比のロゴ。 [**[!UICONTROL Browse]**] をクリックし、デバイスまたはネットワーク上のファイルを探して、[**[!UICONTROL Upload]**] をクリックします。

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。 **ヒント：** [!UICONTROL Ad Tools] ビューを使用して、プレースメント内の複数の広告に対して一度にサードパーティトラッキングピクセルを編集するには、「[&#x200B; プレースメント内の広告にサードパーティトラッキングピクセルを添付する &#x200B;](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)」を参照してください。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、*[!UICONTROL HTML]*、*[!UICONTROL JavaScript URL]* のどれであるかを示します。

**[!UICONTROL Pixel URL or Code]:** ピクセル画像の URL を、指定した [!UICONTROL Pixel Type] に適した形式で指定します。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]* または *[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [Ad Management について &#x200B;](ad-about.md)
>* [&#x200B; 単一の広告の作成 &#x200B;](ad-create.md)
>* [&#x200B; 広告に関連付けられたプレースメントのリスト &#x200B;](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [&#x200B; 広告仕様 &#x200B;](ad-specs.md)
>* [DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)
