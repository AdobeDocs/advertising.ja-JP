---
title: ADOBE ADVERTISINGのコンバージョンおよびページビューのトラッキングタグに関するFAQ
description: Adobe Advertisingのコンバージョンタグとページビューのトラッキングタグの比較を参照してください。
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ckLRjqXGTShwM2TTyULRKjPwL5RYVWkiVVSkwMmvxE8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# ADOBE ADVERTISINGのコンバージョンおよびページビューのトラッキングタグに関するFAQ

以下は、Adobe Advertising コンバージョントラッキングタグおよびページビュートラッキングタグに適用されます。

| | ECIDを持つJS タグ | JS バージョン 3 タグ | JS バージョン 2 タグ | 画像タグ |
| ---- | ---- | ---- | ---- | ---- |
| 他のJS バージョンと同じweb ページで使用できます | — | — | — | なし |
| 同じweb ページで、同じ広告主ユーザーIDを持つ複数のタグを使用できるようにします | はい | はい | はい | — |
| 同じweb ページで、異なる広告主ユーザーIDを持つ複数のタグを使用できます | はい | はい | — | — |
| Adobe Experience PlatformのAdobe Advertising拡張機能で使用され、Experience Platformを使用して生成された他のタグと互換性があります | はい | はい | — | — |
| Adobe Advertising JavaScript コンバージョンマッピングタグで使用する場合、[!DNL Apple Safari]および[!DNL Mozilla Firefox]に由来するすべてのコンバージョンを追跡できるようにします | はい | はい | はい | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* 新しい実装では、すべてJavaScript バージョン 3を使用します。
>* ECIDを持つJavaScript タグは、[Adobe Experience Cloud ID （ECID） サービス ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html)と、従来のef_idおよびgsurferidを使用して、コンバージョンを測定します。 この最新のタグは、[ ファーストパーティ Experience Cloud s_ecid Cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html)を作成し、他のExperience Cloud製品との緊密な統合を提供します。
>* JavaScript バージョン 2のタグは、広告主のweb ページにタグが既に実装されている場合にのみ使用します。
>* ベストプラクティスは、サイトが画像タグの使用に対するポリシーを持っていない限り、画像タグの代わりにJavaScript タグを使用することです。
>* JavaScript タグは、Adobe Experience Cloudで作成されたオーディエンス、Adobe Audience Managerで作成されたオーディエンス、Audience ManagerまたはAdobe AnalyticsからAdobe Experience Cloudに公開されたオーディエンスをターゲットにする広告主に必要です。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertising コンバージョンタグを生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)の形式
>* [JavaScript コンバージョントラッキングタグバージョン 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)の形式
>* [画像コンバージョントラッキングタグの形式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!--
 add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
