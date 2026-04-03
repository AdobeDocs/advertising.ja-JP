---
title: コネクテッド TVの広告設定
description: コネクテッド TV広告で使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
TQID: https://experienceleague.adobe.com/EY3BI7GFcDtR9SmA-N9VY3pwEMPTA99GApcuReaLBeQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# コネクテッド TVの広告設定

## [!UICONTROL Insert Ad Tag]

*新しい広告のみ*

**[!UICONTROL URL]**：広大なタグ URL。

**[!UICONTROL Title]**：広告ビューとレポートで使用されるファイルの名前。

>[!TIP]
>
> VAST タグの有効性を確認するには、そのタグをブラウザーに貼り付け、**[!UICONTROL Enter]** キーを押します。 タグが有効な場合は、上部の近くに`<VAST>`を含むXML ファイルが表示されます。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントタイプに対応します。

**[!UICONTROL Ad Name]:**&#x200B;広告名。 アセットタイトルはデフォルトで使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメント、[!UICONTROL Ads] ビュー、およびレポートに添付する際に見つけやすい名前を使用します。 例えば、ユニットのタイプと一部の主要属性（ホリデープロダクト プレビュー：30sec CTVなど）について説明します。

**[!UICONTROL Width | Ad Unit Width]:**&#x200B;広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

**[!UICONTROL Height | Ad Unit Height]:**&#x200B;広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

**[!UICONTROL Player X]:**&#x200B;広告ユニットのX座標。 デフォルト設定を維持します。

**[!UICONTROL Player Y]:**&#x200B;広告単位のY座標。 デフォルト設定を維持します。

**[!UICONTROL Player Width]:**&#x200B;広告ユニット全体の幅。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

これは&#x200B;**[!UICONTROL Width]** フィールドと同じです。

**[!UICONTROL Player Height]:**&#x200B;広告ユニット全体の高さ。 このオプションは、選択した広告ユニットのタイプに応じてロックされる場合があります。

これは&#x200B;**[!UICONTROL Height]** フィールドと同じです。

**[!UICONTROL Show Controls]:**&#x200B;広告のビデオコントロールを含める場所：*[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]*&#x200B;または&#x200B;*[!UICONTROL None]* （デフォルト）。

**[!UICONTROL Preserve Aspect Ratio]:** ビデオの幅と高さの縦横比（*[!UICONTROL Yes]*）を維持するか、ビデオを拡張して使用可能なスペース（*[!UICONTROL No]*）を埋めるか。

**[!UICONTROL VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）広告ソースとして入力したサードパーティ VAST タグ。

**[!UICONTROL Final VAST Tag]:** （VAST タグを使用した広告のみ。読み取り専用）必要な[Advertising DSP トラッキングマクロ &#x200B;](/help/dsp/campaign-management/macros.md)を挿入して広告ソースとして入力したサードパーティ VAST タグ（該当する場合）。

**[!UICONTROL Clock Number]**: （英国でのみ使用されます。権限を持つユーザーのみが使用できます）適切な広告を確実にブロードキャストするために使用される一意の識別子。 この設定が適用されない場合は、空白のままにします。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Advertising DSPの広告管理について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられているプレースメントを一覧表示](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)
