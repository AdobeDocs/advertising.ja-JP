---
title: トラッキング URLに使用できるマクロ
description: ランディングページのURL、トラッキング URL、サードパーティのクリエイティブに追加できるマクロを参照します。
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# トラッキング URLに使用できるマクロ

<!-- More feature metadata???  -->

サードパーティクリエイティブ、エクスペリエンスのサードパーティトラッキング URL、独自の使用のためにランディングページ URLに、次のマクロのいずれかを含めることができます。

利用可能なマクロの一部、またはそれに相当するマクロは、自動的にエクスペリエンスタグに含まれます。

<!--
 Later: 

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

| マクロ | 説明 | Advertising DSPのエクスペリエンスタグは自動的に生成されますか？ |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | DSPからキャンペーン IDを追跡およびレポートします | はい |
| `${TM_SITE_ID_NUM}` | DSPからサイト IDを追跡およびレポートします | はい |
| `${TM_PLACEMENT_ID_NUM}` | DSPからプレースメント IDを追跡およびレポートします | はい |
| `${TM_AD_ID_NUM}` | DSPから広告IDを追跡してレポートします | はい |
| `${TM_CREATIVE_ID_NUM}` | DSPからクリエイティブ IDをトラッキングおよびレポートします | 該当なし |
| `${TM_SESSION_ID}` | DSPからインプレッション IDを追跡およびレポートします。 値が返されない場合は、Advertising Creativeによって値が生成されます。 | はい |
| `${TM_ACC_EXPERIENCE_ID}` | Advertising Creative エクスペリエンス IDのトラッキングとレポート | — |
| `${TM_ACC_CREATIVE_ID}` | Advertising Creativeのクリエイティブ IDをトラッキングおよびレポートします | — |
| `${TM_RANDOM}` | 1 ～ 1000000の間の乱数 | — |
| `${TM_TIMESTAMP}` | UNIX® タイムスタンプ （秒単位） | — |
| `${TM_CLICK_URL_URLENC}` | （URL エンコーディングを必要とするベンダーからのサードパーティ広告の場合）エンコードされたクリックリダイレクト URL。広告サーバーが広告クリックを追跡およびカウントできるようにします。 ユーザーが広告をクリックすると、マクロがアクティブになり、クリックはレポート用に記録され、カウントされます。 | はい |

>[!MORELIKETHIS]
>
>* [標準クリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [標準クリエイティブ設定](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [ ターゲット設定](/help/creative/experiences/experience-settings-targeting.md)
>*[ ターゲティングされていないエクスペリエンス設定](/help/creative/experiences/experience-settings-no-targeting.md)
