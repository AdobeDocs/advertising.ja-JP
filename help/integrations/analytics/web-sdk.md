---
title: の使用 [!DNL Last Event Service] を使用した JavaScript ライブラリ [!DNL Web SDK]
description: を使用してから切り替える手順を説明します。 [!DNL Analytics] [!DNL visitorAPI] ライブラリを [!DNL Experience Platform] [!DNL Web SDK] のライブラリ [!DNL Analytics for Advertising] 実装。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 687f146b27765d59f172284e4cff7ab5c0e57b50
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# の使用 [!DNL Last Event Service] Adobe Experience Platformを使用した JavaScript ライブラリ [!DNL Web SDK]

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

組織で従来のAdobe Analyticsを使用している場合 `visitorAPI.js` データ収集用のライブラリでは、オプションで、 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) ライブラリ (`alloy.js`) を使用して、 [!DNL Edge Network].

The [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript ライブラリは、そのまま、追加の ID(`SDID`) をクリックします。 The [!DNL Web SDK] ただし、ライブラリでは [!DNL stitch ID]. 次の手順で [!DNL Web SDK] 対象： [!DNL Analytics for Advertising]を変更する場合は、1) [!DNL Last Event Service] のタグを Web ページで使用し、2) を使用して、 [!DNL Web SDK] `sendEvent` 適切にコマンドを実行します。

## 手順 1: [!DNL Last Event Service] タグを生成して `[!DNL StitchID]`

Adobe Analytics の [!DNL Analytics for Advertising] [!DNL Last Event Service] タグを追加して、 `[!DNL StitchID]` ライブラリにバンドルされているランダム ID ジェネレーターを使用する。

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
          stitchId = AdCloudEvent('IMS ORG Id''rsid').generateRandomId();
</script>
```

## 手順 2：使用 [!DNL Web SDK] を送信し、 [!DNL StitchID] を XDM データとして使用 [!DNL Analytics]

次のプロパティを [!DNL Web SDK] `sendEvent` コマンドを使用して [!DNL StitchID] から [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) データ [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] は、値を `SDID`.

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
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [用 JavaScript コード [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
