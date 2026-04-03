---
title: ' [!DNL Analytics for Advertising]  マクロを [!DNL Flashtalking] 広告タグに追加'
description: ' [!DNL Analytics for Advertising] 広告タグに [!DNL Flashtalking]  マクロを追加する理由と方法について説明します'
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
TQID: https://experienceleague.adobe.com/fgmEHPEGMS9vA6P3QDeZMT7MBBTRDtnQcz-qMbMDw3Y
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 429
ht-degree: 0%

---

# [!DNL Analytics for Advertising]個のマクロを[!DNL Flashtalking]個の広告タグに追加

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

*[!DNL Flashtalking]さんとの直接的なパートナーシップを持たない組織のみ*

*Advertising DSPにのみ適用*

Advertising DSP広告に[!DNL Flashtalking]の広告タグを使用する場合は、ランディングページのURLにトラッキングパラメーターを追加する必要があります。 [!DNL Flashtalking]とAdvertising DSPのパートナーシップを使用するには、Analytics for Advertising パラメーターをランディングページ URLに追加します。 パラメーターは、ランディングページ URLのAMO ID （`s_kwcid`）と`ef_id` クエリ文字列パラメーターを記録し、Adobe Advertisingが広告のクリックデータをAdobe Analyticsに送信できるようにします。

>[!NOTE]
>
>組織が[!DNL Flashtalking]と直接パートナーシップを締結している場合、この手順は必要ありません。 代わりに、[!DNL Flashtalking] アカウントにログインし、[!DNL Flashtalking]https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros[の](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) サポートドキュメントに従って、`s_kwcid`および`ef_id` トラッキングパラメーターを追跡するためにデータパスマクロを使用します。

次の種類の[!DNL Flashtalking]実装では、[!DNL Analytics for Advertising]件のディスプレイ広告とビデオ広告にマクロを使用します。

* **Web サイトに実装された[!DNL Adobe] [!DNL Analytics for Advertising] JavaScript コードを持つ広告主**: JavaScript コードには、AMO ID （`s_kwcid`）と`ef_id` クエリ文字列パラメーターが既に記録されています。 ただし、マクロを使用すると、サードパーティのCookieがサポートされていない場合に、トラッキングを拡張してクリックベースのコンバージョンを含めることができます。 ベストプラクティスは、次のセクションのマクロを広告タグに追加して、JavaScript コードでキャプチャされないクリックスルーのデータを取り込むことです。

  >[!NOTE]
  >
  >JavaScript コードは、Cookieがまだ利用可能な間のみクリックを追跡するためのソリューションです。 Cookieが廃止されると、次のマクロを実装する必要があります。

* **Web サイトで[!DNL Analytics for Advertising] JavaScript コードを使用せず、代わりに[!DNL Analytics] サーバーサイド転送によるクリックスルー情報の提供のみ** （ビュースルーデータなし）を利用している広告主：Adobe Advertisingを通じて購入した広告からクリック活動を報告するには、次のマクロが必要です。

## 広告タグの表示

[!DNL Flashtalking]広告タグの設定内で、`Clicktag` フィールドのクリックスルーURLの末尾に次のマクロを追加します。

```
[ftqs:[AdobeAMO]]
```

ベース URLの後の最初または唯一のクエリ文字列である場合は、ベース URLから`?`を付けて分離します。 ベース URLに複数のクエリ文字列が含まれる場合は、最初の文字列を`?`、後続の各文字列を`&`で開始します。

例：

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## 動画広告タグ

[!DNL Flashtalking]広告タグの設定内で、`Clicktag` フィールドのクリックスルーURLの末尾に次のマクロを追加します。

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

ベース URLの後の最初または唯一のクエリ文字列である場合は、ベース URLから`?`を付けて分離します。 ベース URLに複数のクエリ文字列が含まれる場合は、最初の文字列を`?`、後続の各文字列を`&`で開始します。

例：

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [様が使用している [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID
>* [追加 [!DNL Analytics for Advertising]  マクロを [!DNL Google Campaign Manager 360] 広告タグ &#x200B;](/help/integrations/analytics/macros-google-campaign-manager.md)に追加

