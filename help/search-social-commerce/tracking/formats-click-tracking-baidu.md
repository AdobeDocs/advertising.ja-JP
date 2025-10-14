---
title: ' [!DNL Baidu] のクリック追跡形式'
description: アカウントのクリック追跡形式について説明  [!DNL Baidu]  ます。
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# [!DNL Baidu] でのスポンサー付き広告のクリック追跡形式

スポンサー付き広告には、次のベース宛先 UR 形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* `<campaignID>` は、数値キャンペーン ID の変数です。
>
>* `<the landing page>` は、エンドユーザーが誘導されるサイト上の URL を表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について &#x200B;](formats-click-tracking-about.md)
>* [AMO ID 形式 &#x200B;](/help/integrations/analytics/ids.md#amo-id-formats)
