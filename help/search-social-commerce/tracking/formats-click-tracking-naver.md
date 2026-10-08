---
title: '[!DNL Naver]のクリックトラッキング形式'
description: '[!DNL Naver] アカウントのクリックトラッキング形式について説明します。'
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
TQID: 'https://experienceleague.adobe.com/c1zAy1aKgr4MRpyiitdmO4VxP7kfKfFWHzYk88lvX2w'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2206c6aa-b5c2-51b3-88e0-706d57048fe4
    internal-label: Search Tracking
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '104'
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
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`<advertiser_ID>`の後の`cq?`を`c?`に置き換えます。
>
>* `<the landing page>`は、エンドユーザーの宛先となるサイト上のURLを表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)
