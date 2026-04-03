---
title: ' [!DNL Baidu]のクリックトラッキング形式'
description: ' [!DNL Baidu]  アカウントのクリックトラッキング形式について説明します。'
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
TQID: https://experienceleague.adobe.com/iV5-TNxdMov1LoPZzwP3RqkP93fp8A9TvAlY-2R-ZGo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# [!DNL Baidu]のスポンサー広告のクリックトラッキング形式

スポンサー広告には、次の基本宛先UR形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* `<campaignID>`は、数値キャンペーン IDの変数です。
>
>* `<the landing page>`は、エンドユーザーの宛先となるサイト上のURLを表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)
