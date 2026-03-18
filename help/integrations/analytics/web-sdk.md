---
title: ' [!DNL Last Event Service]  での  [!DNL Web SDK]JavaScript ライブラリの使用'
description: 実装の  [!DNL Analytics] [!DNL visitorAPI] ライブラリの使用から  [!DNL Experience Platform] [!DNL Web SDK] ライブラリに切り替える手順  [!DNL Analytics for Advertising]  説明します。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Adobe Experience Platform [!DNL Last Event Service] での [!DNL Web SDK] JavaScript ライブラリの使用

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

組織がデータ収集に従来のAdobe Analytics `visitorAPI.js` ライブラリを使用している場合は、[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja) ライブラリ（`alloy.js`）の使用に切り替えることができます。これにより、[!DNL Edge Network] を通じて様々なExperience Cloud サービスを操作できます。

[!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript ライブラリは、そのまま、ビュースルーイベントとクリックスルーイベントを記録し、追加の ID （`SDID`）を使用して関連コンバージョンにステッチします。 ただし、[!DNL Web SDK] ライブラリは [!DNL stitch ID] を提供しません。 [!DNL Web SDK] に [!DNL Analytics for Advertising] を使用するには、1） Web ページで使用する [!DNL Last Event Service] タグと、2） [!DNL Web SDK] `sendEvent` コマンドを適宜変更する必要があります。

## 手順 1:[!DNL Last Event Service] タグを編集して `[!DNL StitchID]` を生成する

Web ページで使用する [!DNL Analytics for Advertising] [!DNL Last Event Service] タグに、ライブラリにバンドルされているランダム ID ジェネレーターを使用して `[!DNL StitchID]` を生成するコードを追加します。

**従来のタグ：**

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

## 手順 2:[!DNL Web SDK] を使用して、[!DNL StitchID] を [!DNL Analytics] の XDM データとして送信する

[!DNL Web SDK] `sendEvent` コマンド内に次のプロパティを挿入し、[!DNL StitchID].[!DNL Experience Edge] の [!DNL Experience Data Model] as [!DNL Analytics] <!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> （XDM）データに送信します。 [!DNL Analytics] はこの値を `SDID` として使用します。

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
>* [&#x200B; 概要  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) のJavaScript コード
