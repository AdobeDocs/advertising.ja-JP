---
title: ' [!DNL Yandex] のクリック追跡形式'
description: アカウントのクリック追跡形式について説明  [!DNL Yandex]  ます。
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# [!DNL Yandex] でのスポンサー付き広告のクリック追跡形式

スポンサー付き広告には、次のベース宛先 UR 形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* `<the landing page>` は、エンドユーザーが誘導されるサイト上の URL を表す変数です。
>
>* `source_type` は一致するタイプです。
>
>* 広告 `source` 検索サイトとコンテンツベースのサイトのどちらで表示されたかを示します。
>
>* `position` は、ブロック内の広告の位置番号です。 検索以外のトラフィックの場合、値は「0」です。
>
>* `position_type` は、広告が [!DNL Yandex] に表示されたブロックです。 指定可能な値：「premium」（上部ブロック）、「other」（右側のブロック）、または「none」（検索トラフィック以外）。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について &#x200B;](formats-click-tracking-about.md)
>* [AMO ID 形式 &#x200B;](/help/integrations/analytics/ids.md#amo-id-formats)
