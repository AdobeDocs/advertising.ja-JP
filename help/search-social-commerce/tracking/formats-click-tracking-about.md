---
title: Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について
description: サポートされている広告ネットワークのクリックトラッキング形式について説明します。
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について

Adobe Advertising コンバージョントラッキングサービスを使用する広告アカウントおよびキャンペーンのトラッキングテンプレート、ランディングページサフィックス（最終URL サフィックス）、および宛先URLは、次のフォーマットになります。

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

どこで：

* `http://pixel.everesttech.net`は、ユーザーをAdobe Advertising ピクセルサーバーにリダイレクトします。

* `<advertiser_ID>`は、Adobe Advertising内の広告主に割り当てられた一意のユーザーIDの変数です。

* `<token passing parameter>`は次のいずれかの変数です：

   * `cq?`または`rq`は、トークンの渡しが有効であることを示します。

   * `c?`または`r`は、トークンの渡しが無効であることを示します。

* `<ad network ID>`は、指定された広告ネットワークの数値IDの変数です。[!DNL Google Ads]の&#x200B;*3*、[!DNL Microsoft Advertising]の&#x200B;*10*、[!DNL Meta]の&#x200B;*45*、[!DNL Yahoo! Display Network]のの&#x200B;*86*、[!DNL Naver]の&#x200B;*87*、[!DNL Baidu]の&#x200B;*88*、*90*、[!DNL Yandex] [!DNL LY Ads]の&#x200B;*94* （旧称[!DNL Yahoo! Japan Ads]）、[!DNL Yahoo Native]の&#x200B;*105* （非推奨）、[!DNL Pinterest]の&#x200B;*106* （非推奨）。

* `<tracking ID>`は、アカウント内で一意のキーワード、広告、またはプレースメントを識別する、システム生成トラッキング ID文字列の変数です。 文字列は広告ネットワークによって異なります。

* `<the landing page>`は、エンドユーザーの宛先となるサイト上のURLを表す変数です。 宛先URLを持つアカウントの場合、この値はURLです。 トラッキングテンプレートを持つアカウントの場合、この値は最終的なURLを表すパラメーター（`{lpurl}`など）です。

[[!DNL Baidu] 形式](formats-click-tracking-baidu.md)、[[!DNL Google Ads] 形式](formats-click-tracking-google.md)、[[!DNL Microsoft Advertising] 形式](formats-click-tracking-microsoft.md)、[[!DNL Naver] 形式](formats-click-tracking-naver.md)、[[!DNL Yahoo! Display Network] 形式](formats-click-tracking-yahoo-display-network.md)、[[!DNL Yahoo! Japan Ads] 形式](formats-click-tracking-yahoo-japan.md)および[[!DNL Yandex] 形式](formats-click-tracking-yandex.md)を示す個別のページを参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; スポンサー広告のクリックトラッキング形式（ [!DNL Baidu]](formats-click-tracking-baidu.md)）
>*  [!DNL Google Ads][&#128279;](formats-click-tracking-google.md)の クリックトラッキング形式
>* [&#x200B; スポンサー広告のクリックトラッキング形式（ [!DNL LY Ads]](formats-click-tracking-yahoo-japan.md)）
>*  [!DNL Microsoft Advertising][&#128279;](formats-click-tracking-microsoft.md)の クリックトラッキング形式
>* [&#x200B; スポンサー広告のクリックトラッキング形式（ [!DNL Naver]](formats-click-tracking-naver.md)）
>* [&#x200B; スポンサー広告のクリックトラッキング形式（ [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)）
>* [&#x200B; スポンサー広告のクリックトラッキング形式（ [!DNL Yandex]](formats-click-tracking-yandex.md)）
