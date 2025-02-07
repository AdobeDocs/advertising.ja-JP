---
title: URL を追跡するために使用可能なマクロ
description: ランディングページの URL のトラッキング URL およびサードパーティのクリエイティブに追加できるマクロを参照します。
feature: Creative Experiences, Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# URL を追跡するために使用可能なマクロ

*クローズドベータ版*

<!-- More feature metadata??? -->

サードパーティクリエイティブ、エクスペリエンスのサードパーティトラッキング URL、独自に使用するランディングページ URL には、次のマクロを含めることができます。

使用可能なマクロの一部、またはそれに相当するものが、エクスペリエンスタグに自動的に含まれます。

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| マクロ | 説明 | Advertising DSPの Experience Tags で自動的に実行しますか？ |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | DSPからキャンペーン ID をトラッキングしレポートします | はい |
| `${TM_SITE_ID_NUM}` | DSPからサイト ID をトラッキングしレポートします | はい |
| `${TM_PLACEMENT_ID_NUM}` | DSPからプレースメント ID を追跡およびレポートします | はい |
| `${TM_AD_ID_NUM}` | DSPからの広告 ID を追跡してレポートします | はい |
| `${TM_CREATIVE_ID_NUM}` | DSPからクリエイティブ ID をトラッキングしレポートします | 該当なし |
| `${TM_SESSION_ID}` | DSPからインプレッション ID をトラッキングしレポートします。 値が返されない場合、Advertising Creativeによって値が生成されます。 | はい |
| `${TM_ACC_EXPERIENCE_ID}` | Advertising Creativeエクスペリエンス ID をトラッキングしレポートします | — |
| `${TM_ACC_CREATIVE_ID}` | Advertising Creativeのクリエイティブ ID をトラッキングしレポートします | — |
| `${TM_RANDOM}` | 1 ～ 1000000 の乱数 | — |
| `${TM_TIMESTAMP}` | Unix タイムスタンプ （秒） | — |
| `${TM_CLICK_URL_URLENC}` | （URL エンコーディングを必要とするベンダーからのサードパーティ広告の場合） エンコードされたクリックリダイレクト URL を使用すると、広告サーバーは広告のクリックを追跡およびカウントできます。 広告が配信され、ユーザーが広告をクリックすると、マクロがアクティブ化され、クリックが記録され、レポート目的でカウントされます。 | はい |

>[!MORELIKETHIS]
>
>* 
>* 
