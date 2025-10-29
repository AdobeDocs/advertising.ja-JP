---
title: 広告設定を表示
description: ディスプレイ広告に使用できる広告設定の説明を参照してください。
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 広告設定を表示

標準のディスプレイ広告の設定は次のとおりです。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （読み取り専用）作成する広告タイプ。広告を添付できるプレースメントのタイプに対応します。 デフォルト値は *[!UICONTROL Display]* です。

**[!UICONTROL Ad Name]:** 広告名。 デフォルトではアセットタイトルが使用されますが、名前を変更できます。

>[!TIP]
>
> 広告をプレースメントに添付する際に見つけやすい名前を [!UICONTROL Ads] ビューおよびレポートで使用します。 例えば、ユニットのタイプや主要な属性（Holiday Product Preview: 300x250 Gamer など）を記述します。

**\[Ad Source\]**: （読み取り専用） *[!UICONTROL 3rd party]*。

**[!UICONTROL This is an expandable Banner]:** （サードパーティ広告のみ）広告が拡張可能なバナー広告であることを示します。 関連する拡張設定によって、購入する在庫が決まるので、広告の行動が反映されていることを確認します。

**[!UICONTROL Expansion Method]:** （サードパーティ製の展開可能なバナー広告のみ）バナーが *[!UICONTROL Click]* または *[!UICONTROL Rollover]* に展開するかどうか。

**[!UICONTROL Expansion Directions]:** （サードパーティ製の展開可能なバナー広告のみ）広告の展開方向：*[!UICONTROL Up]*、*[!UICONTROL Down]*、*[!UICONTROL Left]*、*[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]:** （サードパーティ製の拡張可能なバナー広告のみ）広告が使用可能な認定ベンダー：*[!UICONTROL DCM]* （[!DNL Google DoubleClick for Advertisers]）、*[!UICONTROL Flashtalking]*、*[!UICONTROL Sizmek]*、*[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットの URL。 [timestamp] および [[timestamp]] パラメーターは、実際の値に置き換えられます。

**[!UICONTROL Final Display Code]:** （サードパーティ広告のみ）サードパーティのクリエイティブアセットの URL で、必要な [Advertising DSP トラッキングマクロ ](/help/dsp/campaign-management/macros.md) が挿入されています（該当する場合）。

**[!UICONTROL Ad Size]:** 広告の幅と高さ。 [ サポートされている標準表示広告サイズ ](ad-specs.md) である必要があります。 広告をアップロードする前または [!UICONTROL Display Code] を入力する前に、広告サイズを手動で入力できます。 広告サイズを入力しない場合、アップロードされた広告または広告タグの寸法は自動的に読み取り専用として入力されます。

>[!IMPORTANT]
>
> 幅と高さのフィールドで宣言された広告サイズは、受信入札リクエストと一致します。 広告のディメンションが宣言済みの広告サイズと一致しない場合、配信の問題が発生する可能性があります。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [Ad Management について ](ad-about.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ 広告に関連付けられたプレースメントのリスト ](ad-list-placements.md)
>* [ 広告仕様 ](ad-specs.md)
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
