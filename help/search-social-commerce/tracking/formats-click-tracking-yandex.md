---
title: ' [!DNL Yandex]のクリックトラッキング形式'
description: ' [!DNL Yandex]  アカウントのクリックトラッキング形式について説明します。'
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# [!DNL Yandex]のスポンサー広告のクリックトラッキング形式

スポンサー広告には、次の基本宛先UR形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* `<the landing page>`は、エンドユーザーの宛先となるサイト上のURLを表す変数です。
>
>* `source_type`は一致タイプです。
>
>* `source`は、広告が検索用サイトとコンテンツベースのサイトのどちらに表示されたかです。
>
>* `position`は、ブロック内の広告の位置番号です。 検索以外のトラフィックの場合、値は「0」です。
>
>* `position_type`は、[!DNL Yandex]に広告が表示されたブロックです。 使用可能な値は、「premium」（上ブロック）、「other」（右ブロック）、「none」（検索トラフィック以外）です。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
