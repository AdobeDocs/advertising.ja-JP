---
title: Adobe Advertisingコンバージョントラッキングサービスのクリック追跡 URL の形式について
description: サポートされる広告ネットワークのクリック追跡形式について説明します。
exl-id: 12148caf-fde6-4ac2-b8b4-222409895dd7
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Adobe Advertisingコンバージョントラッキングサービスのクリック追跡 URL の形式について

Adobe Advertisingコンバージョントラッキングサービスを使用する広告アカウントおよびキャンペーンのトラッキングテンプレート、ランディングページのサフィックス（最終 URL のサフィックス）、リンク先 URL の形式は次のとおりです。

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

場所：

* `http://pixel.everesttech.net` ユーザーをAdobe Advertisingpixel サーバにリダイレクトします。

* `<advertiser_ID>` は、Adobe Advertising内の広告主に割り当てられた一意のユーザー ID の変数です。

* `<token passing parameter>` は、次のいずれかの変数です。

   * `cq?` または `rq` はトークンの受け渡しが有効であることを示します。

   * `c?` または `r` はトークンの受け渡しが無効であることを示します。

* `<ad network ID>` は、指定した広告ネットワークの数値 ID の変数です。次に例を示します。 *3* 対象： [!DNL Google Ads], *10* 対象： [!DNL Microsoft Advertising], *45* 対象： [!DNL Meta], *86* 対象： [!DNL Yahoo! Display Network], *87* 対象： [!DNL Naver], *88* 対象： [!DNL Baidu], *90* 対象： [!DNL Yandex], *94* 対象： [!DNL Yahoo! Japan Ads], *105* 対象： [!DNL Yahoo Native] （非推奨）、または *106* 対象： [!DNL Pinterest] （非推奨）。

* `<tracking ID>` は、アカウント内で一意のキーワード、広告、プレースメントを識別する、システム生成のトラッキング ID 文字列用の変数です。 文字列は、広告ネットワークによって異なります。

* `<the landing page>` は、エンドユーザーのリダイレクト先となるサイト上の URL を表す変数です。 宛先 URL のアカウントの場合、この値は URL です。 トラッキングテンプレートを持つアカウントの場合、この値はパラメーター ( `{lpurl}`) の持続性を 1 回の訪問期間で指定します。

次を示す別のページを参照してください： [[!DNL Baidu] 形式](formats-click-tracking-baidu.md), [[!DNL Google Ads] 形式](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] 形式](formats-click-tracking-microsoft.md), [[!DNL Naver] 形式](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] 形式](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] 形式](formats-click-tracking-yahoo-japan.md)、および [[!DNL Yandex] 形式](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [以下のスポンサー付き広告のクリック追跡形式： [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [のクリック追跡形式 [!DNL Google Ads]](formats-click-tracking-google.md)
>* [のクリック追跡形式 [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [以下のスポンサー付き広告のクリック追跡形式： [!DNL Naver]](formats-click-tracking-naver.md)
>* [以下のスポンサー付き広告のクリック追跡形式： [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [以下のスポンサー付き広告のクリック追跡形式： [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [以下のスポンサー付き広告のクリック追跡形式： [!DNL Yandex]](formats-click-tracking-yandex.md)
