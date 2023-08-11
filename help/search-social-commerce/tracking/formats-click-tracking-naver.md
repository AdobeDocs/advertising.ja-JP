---
title: のクリック追跡形式 [!DNL Naver]
description: のクリック追跡形式について説明します。 [!DNL Naver] アカウント。
exl-id: ff243eb5-d768-4e5c-b5b3-015fe22c9d5a
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 以下のスポンサー付き広告のクリック追跡形式： [!DNL Naver]

以下のベースリンク先 URL 形式は、スポンサー付き広告に適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
* `<the landing page>` は、エンドユーザーのリダイレクト先となるサイト上の URL を表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリック追跡 URL の形式について](formats-click-tracking-about.md)
>* [AMO ID トラッキングコードの形式](amo-id-tracking-parameter.md)
