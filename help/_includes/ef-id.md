---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

## ADOBE ADVERTISING EF ID

EF IDは、Adobe Advertisingがアクティビティを個々のブラウザーまたはデバイスレベルでオンラインクリックまたは広告露出に関連付けるために使用する一意のトークンです。 EF IDは、主に、[!DNL Analytics] データとCustomer Journey Analytics データをAdobe Advertisingに送信し、Adobe Advertising内でレポートと入札を最適化するためのキーとして機能します。

[!DNL Analytics]の場合、EF IDは[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=ja)または[!DNL rVar] （予約済み[!DNL eVar]）ディメンション（Adobe Advertising EF ID）に保存されます。

Customer Journey Analyticsの場合、EF IDは`trackingIdentities` オブジェクトの`conversionDetails` プロパティに格納されます。これは[the [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/ja/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)の一部です。

### EF ID形式 {#ef-id-formats}

「Adobe Analytics コンポーネントガイド」のEF ID ディメンション項目[の](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-ef-id#dimension-items)形式を参照してください。

>[!NOTE]
>
>EF IDでは、大文字と小文字が区別されます。 [!DNL Analytics]またはCustomer Journey Analyticsの実装でURL トラッキングが小文字に強制される場合、Adobe AdvertisingはEF IDを認識しません。 これはAdobe Advertisingの入札とレポートに影響しますが、[!DNL Analytics]またはCustomer Journey Analytics内のAdobe Advertising レポートには影響しません。

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
