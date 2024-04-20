---
title: Append [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ
description: 追加の理由と方法を説明します [!DNL Analytics for Advertising] に対するマクロ [!DNL Flashtalking] 広告タグ
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 7b31fb7939f44aa99826bea3f183897683189eae
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Append [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

*Advertising DSPにのみ適用されます*

から広告タグを使用する場合 [!DNL Flashtalking] advertising DSP広告の場合、ランディングページ URL に Analytics for Advertising パラメーターを追加します。 パラメーターのレコード AMO ID （`s_kwcid`）および `ef_id` ランディングページ URL のクエリ文字列パラメーターで、Adobe Advertisingが広告のクリックデータをAdobe Analyticsに送信できるようにします。

にマクロを使用する [!DNL Flashtalking] 次のタイプのディスプレイおよびビデオ広告 [!DNL Analytics for Advertising] 実装：

* **を使用した広告主 [!DNL Adobe] [!DNL Analytics for Advertising] Web サイトに実装されている JavaScript コード**:JavaScript コードは既に AMO ID （`s_kwcid`）および `ef_id` クエリ文字列パラメーター。 ただし、サードパーティ cookie がサポートされていない場合に、マクロを使用すると、トラッキングが拡張されて、クリックベースの変換が含まれます。 ベストプラクティスは、JavaScript コードでは取得できない追加のクリックスルーデータを取得するために、広告タグに次のセクションのマクロを追加することです。

>[!NOTE]
>
>JavaScript コードは、Cookie が使用可能な場合にのみクリックを追跡するソリューションです。 Cookie が廃止されると、次のマクロの実装が必要になります。

* **Web サイトでを使用しない広告主 [!DNL Analytics for Advertising] JavaScript コードを使用し、代わりにに依存します [!DNL Analytics] クリックスルーデータのみのサーバーサイド転送** （ビュースルーデータなし）:Adobe Advertisingで購入した広告に基づくオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## 広告タグの表示

内 [!DNL Flashtalking] タグ設定を追加するには、のクリックスルー URL の末尾に次のマクロを追加します。 `Clicktag` フィールド :

```
[ftqs:[AdobeAMO]]
```

これはベース URL の後の最初または唯一のクエリ文字列で、次のようにベース URL から分離します `?`. ベース URL に複数のクエリ文字列が含まれる場合は、最初の文字列をで始めます `?` 後続の各文字列にはが付いています。 `&`.

例：

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## ビデオ広告タグ

内 [!DNL Flashtalking] タグ設定を追加するには、のクリックスルー URL の末尾に次のマクロを追加します。 `Clicktag` フィールド :

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

これはベース URL の後の最初または唯一のクエリ文字列で、次のようにベース URL から分離します `?`. ベース URL に複数のクエリ文字列が含まれる場合は、最初の文字列をで始めます `?` 後続の各文字列にはが付いています。 `&`.

例：

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [が使用するAdobe Advertising ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ](/help/integrations/analytics/macros-google-campaign-manager.md)

