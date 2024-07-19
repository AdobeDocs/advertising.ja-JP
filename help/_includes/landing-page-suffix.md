---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# GGL および MS アカウント設定、キャンペーン設定、一部の広告設定のランディングページサフィックス フィールド

**[!UICONTROL Landing Page Suffix]:** （[!DNL Google Ads] アカウントおよび [!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的な URL の末尾に追加するすべてのパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターを含めます。 例：`param1=value1&param2=value2`

Adobe Advertisingコンバージョントラッキングを使用するアカウントでは、アドネットワークのクリック識別子（[!DNL Google Ads] の場合は `gclid`、[!DNL Microsoft Advertising] の場合は `msclkid`）をサフィックスに含める必要があります。

Adobe Analytics統合を使用するアカウントでは、s_kwcid パラメーターを使用する必要があります。 アカウントにサーバー側の s_kwcid 実装がある場合は、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 詳しくは、[Google Advertisingに必要なサフィックス形式 ](/help/search-social-commerce/tracking/formats-click-tracking-google.md) および [Microsoft Ads に必要なサフィックス形式 ](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) を参照してください。

**注：**

* このフィールドは、[!UICONTROL Auto Upload] トラッキング設定によって更新されません。

* 下位レベルのランディングページのサフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
