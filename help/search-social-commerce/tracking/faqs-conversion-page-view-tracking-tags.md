---
title: Adobe Advertisingコンバージョンおよびページビュートラッキングタグに関する FAQ
description: Adobe Advertisingコンバージョンタグとページビュートラッキングタグの比較を参照してください。
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e9d55ba2f4b3ce8b1ac19c06fe8759a2f862c480
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Adobe Advertisingコンバージョンおよびページビュートラッキングタグに関する FAQ

以下は、Adobe Advertisingコンバージョントラッキングタグとページビューのトラッキングタグに当てはまります。

| | ECID を持つ JS タグ | JS バージョン 3 タグ | JS バージョン 2 タグ | 画像タグ |
| ---- | ---- | ---- | ---- | ---- |
| 別の JS バージョンと同じ web ページで使用できます | — | — | — | 該当なし |
| 同じ web ページ上で、同じ広告主ユーザー ID を持つ複数のタグを使用できるようにします | はい | はい | はい | — |
| 同じ web ページ上で、異なる広告主ユーザー ID を持つ複数のタグを使用できるようにします | はい | はい | — | — |
| Adobe Experience PlatformのAdobe Advertising拡張機能で使用され、Experience Platformを使用して生成された他のタグと互換性があります | はい | はい | — | — |
| Adobe AdvertisingのJavaScript コンバージョンマッピングタグで使用される場合、[!DNL Apple Safari] および [!DNL Mozilla Firefox] から発生するすべてのコンバージョンを追跡できます | はい | はい | はい | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* すべての新規実装では、JavaScript バージョン 3 が使用されます。
>* ECID を持つJavaScript タグは、[Adobe Experience Cloud ID （ECID）サービスと ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=ja) 従来の ef_id および gsurferid を使用してコンバージョンを測定します。 この最新のタグは、[ ファーストパーティExperience Cloud s_ecid cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html?lang=ja) を作成し、他のExperience Cloud製品とより緊密に統合できます。
>* JavaScript バージョン 2 のタグは、広告主の web ページにタグが既に実装されている場合にのみ使用します。
>* サイトで使用を禁止するポリシーがない限り、画像タグの代わりにJavaScript タグを使用することをお勧めします。
>* JavaScript タグは、Adobe Experience Cloudで作成されたオーディエンスをターゲットにする広告主や、Adobe Audience Managerで作成されたオーディエンスをターゲットにする広告主、またはAudience ManagerまたはAdobe AnalyticsからAdobe Experience Cloudに公開する広告主に必要です。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertisingコンバージョンタグを生成 ](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式 ](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式 ](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [ 画像変換トラッキングタグの形式 ](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
