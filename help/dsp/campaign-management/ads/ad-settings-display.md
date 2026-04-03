---
title: 広告設定の表示
description: ディスプレイ広告で使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
TQID: https://experienceleague.adobe.com/bcuGR2fzcwjvPcWisdQZBbU8vcaZhgW2qZPAXjV5ndM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# 広告設定の表示

次の設定は、標準ディスプレイ広告用です。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントタイプに対応します。 デフォルトは&#x200B;*[!UICONTROL Display]*&#x200B;です。

**[!UICONTROL Ad Name]:**&#x200B;広告名。 アセットタイトルはデフォルトで使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメント、[!UICONTROL Ads] ビュー、およびレポートに添付する際に見つけやすい名前を使用します。 例えば、ユニットのタイプと一部の主要属性（ホリデープロダクト プレビュー：300x250 ゲーマーなど）を説明します。

**\[Ad Source\]**: （読み取り専用） *[!UICONTROL 3rd party]*。

**[!UICONTROL This is an expandable Banner]:** （サードパーティ広告のみ）広告が拡張可能なバナー広告であることを示します。 関連する拡張設定によって購入する在庫が決まりますので、広告行動を反映したものにしましょう。

**[!UICONTROL Expansion Method]:** （サードパーティの拡張可能なバナー広告のみ）バナーが&#x200B;*[!UICONTROL Click]*&#x200B;または&#x200B;*[!UICONTROL Rollover]*&#x200B;に展開されるかどうか。

**[!UICONTROL Expansion Directions]:** （サードパーティの拡張可能なバナー広告のみ）広告が展開される方向：*[!UICONTROL Up]*、*[!UICONTROL Down]*、*[!UICONTROL Left]*、または&#x200B;*[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]:** （サードパーティの拡張可能なバナー広告のみ）広告を利用できる認定ベンダー：*[!UICONTROL DCM]* （[!DNL Google DoubleClick for Advertisers]）、*[!UICONTROL Flashtalking]*、*[!UICONTROL Sizmek]*、または&#x200B;*[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]:** （サードパーティ広告のみ） サードパーティのクリエイティブアセットのURL。 [timestamp]および[[timestamp]]のパラメーターはすべて、実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** （サードパーティ広告のみ）必要な[Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md)が挿入されたサードパーティのクリエイティブアセットのURL （該当する場合）。

**[!UICONTROL Ad Size]:**&#x200B;広告の幅と高さ。 [ サポートされている標準ディスプレイ広告サイズ ](ad-specs.md)である必要があります。 広告をアップロードする前に広告サイズを手動で入力するか、[!UICONTROL Display Code]を入力します。 広告サイズを入力しない場合、アップロードされた広告または広告タグのサイズは、自動的に読み取り専用として入力されます。

>[!IMPORTANT]
>
> 「幅」フィールドと「高さ」フィールドで宣言された広告サイズは、入札依頼と一致します。 広告のディメンションが宣言された広告サイズと一致しない場合、配信の問題が発生する可能性があります。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Advertising DSPの広告管理について](ad-about.md)
>* [単一の広告を作成](ad-create.md)
>* [広告に関連付けられているプレースメントを一覧表示](ad-list-placements.md)
>* [広告の仕様](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
