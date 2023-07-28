---
title: Adobe Advertisingコンバージョンおよびページビュートラッキングタグに関する FAQ
description: Adobe Advertisingコンバージョンとページビュートラッキングタグの比較を参照してください。
exl-id: 5eb414a7-2f96-47de-b157-a17851653206
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Adobe Advertisingコンバージョンおよびページビュートラッキングタグに関する FAQ

以下が、Adobe Advertisingコンバージョントラッキングタグとページビュートラッキングタグに適用されます。

| | ECID を使用した JS タグ | JS バージョン 3 タグ | JS バージョン 2 タグ | 画像タグ |
| ---- | ---- | ---- | ---- | ---- |
| 別の JS バージョンと同じ Web ページで使用できます | — | — | — | 該当なし |
| 同じ Web ページで同じ広告主ユーザー ID を持つ複数のタグを使用できます | はい | はい | はい | — |
| 同じ Web ページで異なる広告主のユーザー ID を持つ複数のタグを使用できます | はい | はい | いいえ | いいえ |
| Adobe Experience PlatformのAdobe Advertising拡張機能で使用され、Experience Platformを使用して生成された他のタグとの互換性があります。 | はい | はい | — | — |
| 発生するすべてのコンバージョンを許可します [!DNL Apple Safari] および [!DNL Mozilla Firefox] を JavaScript コンバージョンマッピングタグと共に使用した場合にAdobe Advertisingする | はい | はい | はい | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* すべての新しい実装で JavaScript バージョン 3 が使用されます。
>* ECID を持つ JavaScript タグは、 [Adobe Experience Cloud ID(ECID) サービス](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) コンバージョンを測定する従来の ef_id および gsurferid。 この最新のタグは、 [ファーストパーティExperience Clouds_ecid の cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) とは、他のExperience Cloud製品とのより緊密な統合を提供します。
>* 広告主の Web ページに既にタグが実装されている場合にのみ、JavaScript Version 2 タグを使用します。
>* サイトで使用に対するポリシーが設定されていない限り、ベストプラクティスは画像タグではなく JavaScript タグを使用することです。
>* Adobe Experience Cloudで作成されたオーディエンス、Adobe Audience Managerで作成されたオーディエンス、Audience ManagerまたはAdobe AnalyticsからAdobe Experience Cloudに公開されたオーディエンスをターゲットにする広告主には、JavaScript タグが必要です。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertisingコンバージョンタグの生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [画像コンバージョントラッキングタグの形式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
