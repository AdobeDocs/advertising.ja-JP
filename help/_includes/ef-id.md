---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

EF ID は、Adobe Advertisingがアクティビティをオンラインクリックや個々のブラウザーまたはデバイスレベルでの広告表示に関連付けるために使用する一意のトークンです。 EF ID は、主に、Adobe Advertising内のレポートと入札最適化のために、[!DNL Analytics] データとCustomer Journey Analytics データをAdobe Advertisingに送信するためのキーとして機能します。

[!DNL Analytics] の場合、EF ID は [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または [!DNL rVar] （予約 [!DNL eVar]）ディメンション（Adobe Advertising EF ID）に保存されます。

Customer Journey Analyticsの場合、EF ID は、`trackingIdentities` の一部である `conversionDetails` オブジェクトの [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] プロパティに格納されます。
