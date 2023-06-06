---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# 最終 URL サフィックスの定義

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ（オプション）情報を追跡するために最終 URL の末尾に追加するパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターを含めます。 例：`param1=value1&param2=value2`

Adobe広告コンバージョントラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック識別子 (`msclkid` 対象 [!DNL Microsoft Advertising]; `gclid` 対象 [!DNL Google Ads]) をクリックします。

Adobe Analytics統合のアカウントでは、 s_kwcid パラメーターを使用する必要があります。 アカウントにサーバー側の s_kwcid 実装がある場合、ユーザーが広告をクリックすると、パラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 詳しくは、 [必要なサフィックス形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) および [必要なサフィックス形式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* このフィールドは [!UICONTROL Auto Upload] トラッキング設定。
>* 下位レベルでの最終的な URL サフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

