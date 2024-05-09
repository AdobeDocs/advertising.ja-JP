---
title: 使用， [!DNL Last Event Service] を使用した JavaScript ライブラリ [!DNL Web SDK]
description: の使用から切り替える手順を説明します [!DNL Analytics] [!DNL visitorAPI] のライブラリ [!DNL Experience Platform] [!DNL Web SDK] のライブラリ [!DNL Analytics for Advertising] 実装。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 使用， [!DNL Last Event Service] Adobe Experience Platformを使用した JavaScript ライブラリ [!DNL Web SDK]

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

組織で従来のAdobe Analyticsを使用している場合 `visitorAPI.js` データ収集用のライブラリ。オプションで、を使用してに切り替えることができます [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) ライブラリ （`alloy.js`を使用して、様々なExperience Cloudサービスを操作できます。 [!DNL Edge Network].

この [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript ライブラリは、そのまま、ビュースルーおよびクリックスルーイベントを記録し、追加の ID （`SDID`）に設定します。 この [!DNL Web SDK] ただし、ライブラリはを提供しません [!DNL stitch ID]. を使用するには [!DNL Web SDK] （用） [!DNL Analytics for Advertising]を変更する必要があります。1） [!DNL Last Event Service] web ページで使用するタグと 2） [!DNL Web SDK] `sendEvent` それに応じてコマンドを使用します。

## 手順 1：を編集する [!DNL Last Event Service] タグを使用してを生成 `[!DNL StitchID]`

が含まれる [!DNL Analytics for Advertising] [!DNL Last Event Service] web ページで使用するタグを付け、コードを追加して `[!DNL StitchID]` ライブラリにバンドルされているランダム ID ジェネレーターを使用します。

**従来のタグ :**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**新しいタグ：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## 手順 2：使用 [!DNL Web SDK] を送信 [!DNL StitchID] の XDM データとして [!DNL Analytics]

内に次のプロパティを挿入 [!DNL Web SDK] `sendEvent` を送信するコマンド [!DNL StitchID] 対象： [!DNL Experience Edge] as [!DNL Experience Data Model] （XDM）のデータ [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] この場合、値はとして使用されます `SDID`.

**追加するプロパティ：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**例：**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [の JavaScript コード [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
