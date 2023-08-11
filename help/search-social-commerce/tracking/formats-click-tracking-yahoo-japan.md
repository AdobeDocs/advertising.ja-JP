---
title: のクリック追跡形式 [!DNL Yahoo! Japan Ads]
description: のクリック追跡形式について説明します。 [!DNL Yahoo! Japan Ads] アカウント。
exl-id: 4584f2c4-8090-4931-bd44-0df42f350755
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 以下のスポンサー付き広告のクリック追跡形式： [!DNL Yahoo! Japan Ads]

以下のベーストラッキングテンプレート形式は、スポンサー付き広告に適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

または、自動タグ付けオプションが [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

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
>* [AMO ID トラッキングコードの形式](amo-id-tracking-parameter.md)
