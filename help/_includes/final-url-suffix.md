---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# 最終的な URL サフィックスの定義

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** （[!DNL Google Ads] アカウントおよび [!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的な URL の末尾に追加するすべてのパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターを含めます。 例：`param1=value1&param2=value2`

Adobe Advertisingコンバージョントラッキングを使用するアカウントの場合、サフィックスには、広告ネットワークのクリック識別情報（[!DNL Microsoft Advertising] の場合は `msclkid`、[!DNL Google Ads] の場合は `gclid`）を含める必要があります。

Adobe Analytics連携を持つアカウントでは、[AMO ID](/help/integrations/analytics/ids.md) パラメーターを使用する必要があります。 アカウントにサーバーサイド AMO ID 実装がある場合は、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 [ に必要なサフィックス形式  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)、および [ に必要なサフィックス形式  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) を参照してください。

>[!NOTE]
>
>* このフィールドは、[!UICONTROL Auto Upload] トラッキング設定によって更新されません。
>* 下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
