---
title: Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について
description: サポートされる広告ネットワークのクリック追跡形式について説明します。
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について

Adobe Advertisingコンバージョントラッキングサービスを使用する広告アカウントおよびキャンペーンのトラッキングテンプレート、ランディングページサフィックス（最終的な URL サフィックス）および宛先 URL は、次のフォーマットになります。

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

ここで、

* `http://pixel.everesttech.net` は、ユーザーをAdobe Advertisingの pixel サーバーにリダイレクトします。

* `<advertiser_ID>` は、Adobe Advertising内で広告主に割り当てられた一意のユーザー ID に対する変数です。

* 次の `<token passing parameter>` ずれかの変数です。

   * `cq?` または `rq` は、トークン受け渡しが有効であることを示します。

   * `c?` または `r` は、トークン受け渡しが無効であることを示します。

* 指定した広告ネットワークの数値 ID の変数 `<ad network ID>` す。例えば、[!DNL Google Ads] の場合は *3*、[!DNL Microsoft Advertising] の場合は *10*、[!DNL Meta] の場合は *45*、[!DNL Yahoo! Display Network] の場合は *86*、[!DNL Naver] の場合は *87*、[!DNL Baidu] の場合は *88*、** [!DNL Yandex] ** [!DNL Yahoo! Japan Ads] ** [!DNL Yahoo Native] ** [!DNL Pinterest] 9000 for

* `<tracking ID>` は、アカウント内で一意のキーワード、広告またはプレースメントを識別する、システム生成トラッキング ID 文字列の変数です。 文字列は広告ネットワークによって異なります。

* `<the landing page>` は、エンドユーザーが誘導されるサイト上の URL を表す変数です。 宛先 URL を持つアカウントの場合、この値は URL になります。 トラッキングテンプレートを使用するアカウントの場合、この値は最終的な URL を表すパラメーター（`{lpurl}` など）になります。

[[!DNL Baidu] formats](formats-click-tracking-baidu.md)、[[!DNL Google Ads] formats](formats-click-tracking-google.md)、[[!DNL Microsoft Advertising] formats](formats-click-tracking-microsoft.md)、[[!DNL Naver] formats](formats-click-tracking-naver.md)、[[!DNL Yahoo! Display Network] formats](formats-click-tracking-yahoo-display-network.md)、[[!DNL Yahoo! Japan Ads] formats](formats-click-tracking-yahoo-japan.md) および [[!DNL Yandex] formats](formats-click-tracking-yandex.md) については、それぞれのページを参照してください。

>[!MORELIKETHIS]
>
>* [ スポンサー付き広告のクリック追跡形式  [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [ のクリック追跡形式  [!DNL Google Ads]](formats-click-tracking-google.md)
>* [ のクリック追跡形式  [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [ スポンサー付き広告のクリック追跡形式  [!DNL Naver]](formats-click-tracking-naver.md)
>* [ スポンサー付き広告のクリック追跡形式  [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [ スポンサー付き広告のクリック追跡形式  [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [ スポンサー付き広告のクリック追跡形式  [!DNL Yandex]](formats-click-tracking-yandex.md)
