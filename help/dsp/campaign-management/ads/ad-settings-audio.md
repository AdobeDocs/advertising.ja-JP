---
title: オーディオ広告設定
description: オーディオ広告に使用可能な広告設定の説明を参照してください。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# オーディオ広告設定

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]**：広大なタグ URL。

**[!UICONTROL Title]**：で使用されるファイルの名前 [!UICONTROL Ads] とレポートを表示します。

>[!TIP]
>
> VAST タグの有効性を確認するには、それをブラウザーに貼り付けて、 **[!UICONTROL Enter]** キー。 タグが有効な場合、を含む XML ファイルが表示されます `<VAST>` 上部の近く。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。 デフォルト値は *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を、 [!UICONTROL Ads] およびレポートで表示します。 例えば、ユニットの種類や主要な属性（Holiday Product Preview: 30sec Audio など）を記述します。

**[!UICONTROL Ad Duration]:** オーディオファイルの長さ。 自動で次のいずれかに設定されます [!UICONTROL 15] または [!UICONTROL 30]選択した広告ユニットに応じて異なります。

このフィールドは、アカウントの権限に応じて、表示される場合とされない場合があります。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ）サードパーティの広告ソースの URL。 VAST タグにはオーディオメディアファイルのみが含まれていることを確認してください。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用する広告のみ）必要なサードパーティ広告ソースの URL [Advertising DSP トラッキングマクロ](/help/dsp/campaign-management/macros.md) 挿入（該当する場合）。

**[!UICONTROL Select Rate]:** （権限を持つユーザーのみ） ベンダーを通じて請求される事前交渉されたレート、またはAdobeを通じて交渉し、請求されるレートの 1 つ。 料金を追加するには、Adobeアカウントチームにお問い合わせください。

### ピクセル

プレースメントの既存のイベントトラッキングピクセルはすべて自動的に添付されます。 個々の広告のトラッキングのニーズに基づいて、既存のピクセルを分離し、必要に応じて新しいピクセルを作成できます。

次の設定は、作成または編集する各ピクセルに適用されます。

**[!UICONTROL Integration Event]:** 発生するピクセルをトリガーするイベント。 この広告タイプには、 *[!UICONTROL Impression]* または *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*、または *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 指定したピクセルタイプに適した形式のピクセル画像の URL。

**[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

**[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*、または *[!UICONTROL IAS]*..

>[!MORELIKETHIS]
>
>* [Ad Management について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられたプレースメントのリスト](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告仕様](ad-specs.md)
>* [DSP マクロ](/help/dsp/campaign-management/macros.md)
