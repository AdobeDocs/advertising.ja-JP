---
title: ' [!DNL Last Event Service] で [!DNL Web SDK]JavaScript ライブラリを使用する'
description: ' [!DNL Analytics] [!DNL visitorAPI] ライブラリの使用から [!DNL Experience Platform] [!DNL Web SDK]実装の [!DNL Analytics for Advertising]  ライブラリに切り替える手順について説明します。'
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# Adobe Experience Platform [!DNL Last Event Service]での[!DNL Web SDK] JavaScript ライブラリの使用

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

組織でデータ収集に従来のAdobe Analytics `visitorAPI.js` ライブラリを使用している場合は、オプションで[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) ライブラリ （`alloy.js`）を使用して切り替えることができ、[!DNL Edge Network]を介して様々なExperience Cloud サービスと対話できます。

[!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript ライブラリは、そのまま、ビュースルーおよびクリックスルーのイベントを記録し、補足ID （`SDID`）を使用して関連するコンバージョンにそれらを合成します。 ただし、[!DNL Web SDK] ライブラリは[!DNL stitch ID]を提供していません。 [!DNL Web SDK]を[!DNL Analytics for Advertising]に使用するには、1） web ページで使用する[!DNL Last Event Service] タグを変更し、2）それに応じて[!DNL Web SDK] `sendEvent` コマンドを変更する必要があります。

## 手順1: [!DNL Last Event Service] タグを編集して`[!DNL StitchID]`を生成する

Web ページで使用する[!DNL Analytics for Advertising] [!DNL Last Event Service] タグで、ライブラリにバンドルされているランダム ID ジェネレーターを使用して`[!DNL StitchID]`を生成するコードを追加します。

**レガシータグ：**

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

## 手順2: [!DNL Web SDK]を使用して[!DNL StitchID]を[!DNL Analytics]のXDM データとして送信する

[!DNL Web SDK] `sendEvent` コマンド内に次のプロパティを挿入して、[!DNL StitchID]を[!DNL Experience Edge]に[!DNL Experience Data Model] （XDM） データとして[!DNL Analytics]に送信します。<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics]は値を`SDID`として使用します。

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
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [の [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)JavaScript コード
