---
title: ' [!DNL Naver]のクリックトラッキング形式'
description: ' [!DNL Naver]  アカウントのクリックトラッキング形式について説明します。'
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# [!DNL Naver]のスポンサー広告のクリックトラッキング形式

スポンサー広告には、次の基本宛先UR形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
* `<the landing page>`は、エンドユーザーの宛先となるサイト上のURLを表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
