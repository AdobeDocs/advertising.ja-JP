---
title: のクリック追跡形式 [!DNL Naver]
description: のクリック追跡形式について説明します。 [!DNL Naver] アカウント。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
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
>* `<advertiser_ID>` は、広告主の広告内の一意の ID 用の変数です。Adobe広告内では一意の ID が使用されます。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 後 `<advertiser_ID>` と `c?`.
>

* `<the landing page>` は、エンドユーザーのリダイレクト先となるサイト上の URL を表す変数です。

>[!MORELIKETHIS]
>
>* [Adobe広告コンバージョントラッキングサービスのクリック追跡 URL の形式について](formats-click-tracking-about.md)
>* [s\_kwcid トラッキングコードの形式](skwcid-tracking-parameter.md)

