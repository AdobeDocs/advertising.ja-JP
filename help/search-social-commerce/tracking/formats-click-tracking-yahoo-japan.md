---
title: ' [!DNL Yahoo! Japan Ads]のクリックトラッキング形式'
description: ' [!DNL Yahoo! Japan Ads]  アカウントのクリックトラッキング形式について説明します。'
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ZFNzA0bfxKhlNW6fvPWMwBc4naT7rOhvym-wSpxvYXg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 0%

---

# [!DNL Yahoo! Japan Ads]のスポンサー広告のクリックトラッキング形式

スポンサー広告には、次の基本トラッキングテンプレート形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

または、[!DNL Yahoo! Japan Ads]でアカウントに自動タグ付けオプションが設定されている場合：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* `<the landing page>`は、エンドユーザーの宛先となるサイト上のURLを表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)
