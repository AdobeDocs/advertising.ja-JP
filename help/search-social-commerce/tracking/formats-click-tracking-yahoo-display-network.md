---
title: のクリック追跡形式 [!DNL Yahoo! Display Network]
description: のクリック追跡形式について説明します。 [!DNL Yahoo! Display Network] アカウント。
exl-id: 62ea592c-9138-4a8e-9616-c8f2475fea26
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# 以下のスポンサー付き広告のクリック追跡形式： [!DNL Yahoo! Display Network]

以下のベースリンク先 URL 形式は、スポンサー付き広告に適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
>* `<the landing page>` は、エンドユーザーのリダイレクト先となるサイト上の URL を表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリック追跡 URL の形式について](formats-click-tracking-about.md)
>* [AMO ID の形式](/help/integrations/analytics/ids.md#amo-id-formats)
