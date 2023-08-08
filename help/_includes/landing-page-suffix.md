---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# GGL および MS アカウント設定の「ランディングページサフィックス」フィールド、キャンペーン設定、一部の広告設定

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ、オプション ) 情報を追跡するために最終的な URL の末尾に追加するパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターが含まれます。 例： `param1=value1&param2=value2`

Adobe Advertisingコンバージョントラッキングを使用するアカウントには、広告ネットワークのクリック識別子 (`gclid` 対象： [!DNL Google Ads] または `msclkid` 対象： [!DNL Microsoft Advertising]) をサフィックスに追加します。

Adobe Analytics統合のアカウントでは、 s_kwcid パラメーターを使用する必要があります。 アカウントにサーバー側の s_kwcid 実装がある場合、ユーザーが広告をクリックすると、パラメーターが自動的に追加されます。それ以外の場合は、ここに手動で追加する必要があります。 詳しくは、 [Google Ads に必要なサフィックス形式](/help/search-social-commerce/tracking/formats-click-tracking-google.md) および [Microsoft Advertising に必要なサフィックス形式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**メモ：**

* このフィールドは、 [!UICONTROL Auto Upload] トラッキング設定。

* 下位レベルでのランディングページのサフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
