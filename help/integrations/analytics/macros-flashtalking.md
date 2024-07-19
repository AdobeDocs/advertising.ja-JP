---
title: タグに追加  [!DNL Analytics for Advertising]  マクロ  [!DNL Flashtalking]  追加
description: 広告タグにマクロを追加する理由  [!DNL Analytics for Advertising]  方法  [!DNL Flashtalking]  説明します
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# [!DNL Flashtalking] Ad タグへの [!DNL Analytics for Advertising] マクロの追加

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

*Advertising DSPにのみ適用*

Advertising DSP広告に [!DNL Flashtalking] の広告タグを使用する場合は、ランディングページの URL に Analytics for Advertising パラメーターを追加します。 パラメーターは、AMO ID （`s_kwcid`）および `ef_id` クエリ文字列パラメーターをランディングページの URL に記録するので、Adobe Advertisingは、広告のクリックデータをAdobe Analyticsに送信できます。

次のタイプの [!DNL Analytics for Advertising] 実装 [!DNL Flashtalking] ディスプレイ広告とビデオ広告にマクロを使用します。

* **Web サイトに実装された [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript コードを持つ広告主**:JavaScript コードは既に AMO ID （`s_kwcid`）とクエリ文字列パラメーター `ef_id` 記録しています。 ただし、サードパーティ cookie がサポートされていない場合に、マクロを使用すると、トラッキングが拡張されて、クリックベースの変換が含まれます。 ベストプラクティスは、JavaScript コードを通じて取得されないクリックスルーのデータをさらに取得するために、次のセクションのマクロを広告タグに追加することです。

>[!NOTE]
>
>JavaScript コードは、cookie が使用可能な状態でのクリックの追跡にのみ使用できるソリューションです。 Cookie が廃止されると、次のマクロの実装が必要になります。

* **Web サイトで [!DNL Analytics for Advertising] JavaScript コードを使用せず、代わりにクリックスルーデータのみの [!DNL Analytics] サーバーサイド転送に依存している広告主** （ビュースルーデータがない）:Adobe Advertisingで購入した広告から発生するオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## 広告タグの表示

[!DNL Flashtalking] の広告タグ設定で、`Clicktag` フィールドのクリックスルー URL の末尾に次のマクロを追加します。

```
[ftqs:[AdobeAMO]]
```

ベース URL の後の最初または唯一のクエリ文字列である場合は、`?` でベース URL から分離します。 ベース URL に複数のクエリ文字列が含まれる場合は、最初の文字列を `?` で始め、後続の各文字列を `&` で始めます。

例：

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## ビデオ広告タグ

[!DNL Flashtalking] の広告タグ設定で、`Clicktag` フィールドのクリックスルー URL の末尾に次のマクロを追加します。

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

ベース URL の後の最初または唯一のクエリ文字列である場合は、`?` でベース URL から分離します。 ベース URL に複数のクエリ文字列が含まれる場合は、最初の文字列を `?` で始め、後続の各文字列を `&` で始めます。

例：

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [ 使用Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad タグ ](/help/integrations/analytics/macros-google-campaign-manager.md)

