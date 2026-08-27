---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---
# 最終的なURL サフィックス定義

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** （[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的なURLの末尾に追加するパラメーター。企業が追跡する必要があるすべてのパラメーターを含めます。 例：`param1=value1&param2=value2`

Adobe Advertising コンバージョントラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック識別子（[!DNL Microsoft Advertising]の場合は`msclkid`、[!DNL Google Ads]の場合は`gclid`）を含める必要があります。

Adobe Analytics統合を持つアカウントでは、[AMO ID](/help/integrations/analytics/ids.md) パラメーターを使用する必要があります。 アカウントにサーバーサイド AMO ID実装がある場合、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、ここで手動で追加する必要があります。  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)の[必要なサフィックス形式と [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)の[必要なサフィックス形式を参照してください。

>[!NOTE]
>
>* このフィールドは、[!UICONTROL Auto Upload] トラッキング設定で更新されません。
>* 下位レベルの最終URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
