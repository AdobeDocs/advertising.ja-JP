---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID は、一意の各広告の組み合わせを細かいレベルで追跡し、[!DNL Analytics] とCustomer Journey Analyticsのデータ分類や、Adobe Advertisingからの広告指標（インプレッション数、クリック数、コストなど）の取り込みに使用されます。

[!DNL Analytics]:AMO ID は、[eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション（AMO ID）に保存されます。

Customer Journey Analyticsの場合、AMO ID は、`trackingCode` の一部である `conversionDetails` オブジェクトの [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] プロパティに保存されます。

AMO ID は `s_kwcid` とも呼ばれ、「[!DNL squid]」と発音されることがあります。
