---
title: のクリック追跡形式 [!DNL Yandex]
description: のクリック追跡形式について説明します。 [!DNL Yandex] アカウント。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# 以下のスポンサー付き広告のクリック追跡形式： [!DNL Yandex]

以下のベースリンク先 URL 形式は、スポンサー付き広告に適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、広告主の広告内の一意の ID 用の変数です。Adobe広告内では一意の ID が使用されます。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 後 `<advertiser_ID>` と `c?`.
>
>* `<the landing page>` は、エンドユーザーのリダイレクト先となるサイト上の URL を表す変数です。
>
>* `source_type`  は一致タイプです。
>
>* `source` は、広告が検索またはコンテンツベースのサイトに表示されたかどうかを示します。
>
>* `position` は、ブロック内の広告の位置番号です。 検索以外のトラフィックの場合、値は「0」です。
>
>* `position_type` は、広告が表示されたブロックです [!DNL Yandex]. 可能な値：「premium」（トップブロック）、「その他」（右ブロック）、「なし」（検索以外のトラフィック）のいずれかです。


>[!MORELIKETHIS]
>
>* [Adobe広告コンバージョントラッキングサービスのクリック追跡 URL の形式について](formats-click-tracking-about.md)
>* [s\_kwcid トラッキングコードの形式](skwcid-tracking-parameter.md)
