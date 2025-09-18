---
title: オーディオ広告設定
description: オーディオ広告に使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# オーディオ広告設定

## [!UICONTROL Insert Ad Tag]

*新規広告のみ*

**[!UICONTROL URL]**：広大なタグ URL。

**[!UICONTROL Title]**: ファイルの名前。[!UICONTROL Ads] ビューおよびレポートで使用されます。

>[!TIP]
>
> VAST タグの有効性を確認するには、ブラウザーに貼り付けて **[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部に `<VAST>` を含む XML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。 デフォルト値は *[!UICONTROL Audio]* です。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を [!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 30sec Audio など）を記述します。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。 選択した広告ユニットに応じて、自動的に [!UICONTROL 15] または [!UICONTROL 30] に設定されます。

このフィールドは、アカウントの権限に応じて、表示される場合とされない場合があります。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ）サードパーティの広告ソースの URL。 VAST タグにはオーディオメディアファイルのみが含まれていることを確認してください。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ）必要な [Advertising DSP トラッキングマクロが挿入されたサードパーティの広告ソースの URL](/help/dsp/campaign-management/macros.md) 該当する場合）。

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ） Adobeを通じて請求される事前交渉済みの料金、または交渉し、ベンダーを通じて請求される料金の 1 つ。 評価を追加するには、Adobe アカウントチームにお問い合わせください。

### [!UICONTROL Pixel]

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。 **ヒント：** [!UICONTROL Ad Tools] ビューを使用して、プレースメント内の複数の広告に対して一度にサードパーティトラッキングピクセルを編集するには、「[ プレースメント内の広告にサードパーティトラッキングピクセルを添付する ](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)」を参照してください。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプには、*[!UICONTROL Impression]* または *[!UICONTROL Click-through]* で発生するピクセルを使用します。

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、*[!UICONTROL HTML]*、*[!UICONTROL JavaScript URL]* のどれであるかを示します。

**[!UICONTROL Pixel URL or Code]:** ピクセル画像の URL。指定したピクセルタイプに適した形式です。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*、*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [Ad Management について ](ad-about.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ 広告に関連付けられたプレースメントのリスト ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ 広告仕様 ](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
