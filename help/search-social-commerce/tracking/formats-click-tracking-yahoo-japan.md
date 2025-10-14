---
title: ' [!DNL Yahoo! Japan Ads] のクリック追跡形式'
description: アカウントのクリック追跡形式について説明  [!DNL Yahoo! Japan Ads]  ます。
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# [!DNL Yahoo! Japan Ads] でのスポンサー付き広告のクリック追跡形式

スポンサー付き広告には、次の基本トラッキングテンプレート形式が適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

または、[!DNL Yahoo! Japan Ads] のアカウントに自動タグ付けオプションが設定されている場合は、次のようになります。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* `<the landing page>` は、エンドユーザーが誘導されるサイト上の URL を表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について &#x200B;](formats-click-tracking-about.md)
>* [AMO ID 形式 &#x200B;](/help/integrations/analytics/ids.md#amo-id-formats)
