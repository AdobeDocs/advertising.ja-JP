---
title: Sync [!DNL Adobe] audiences
description: オーディエンスのメタデータ、階層データおよび一意のオーディエンスデータを同期する方法  [!DNL Adobe]  説明します。
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# オーディエンス [!DNL Adobe] 同期

クライアント管理者および管理者専用の *[!DNL Direct Access]ール*

*Adobe AdvertisingとAdobe Audience ManagerまたはAdobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

検索、ソーシャルおよびCommerceを使用して、すべての広告主または代理店の [!DNL Adobe] オーディエンスのすべてのメタデータ、階層データおよび一意のオーディエンスデータを、[!UICONTROL Campaigns]/[!UICONTROL Audiences] ビューに取り込むことができます。 この情報には、次のデータが含まれます。

* Adobe Audience Manager セグメント

* Adobe Experience Cloudに公開されるAdobe Analytics セグメント

* Adobe Experience Cloud [!DNL Audience Library] を使用して作成されたセグメント

条件を満たすには、広告主または代理店が [Adobe Experience Platform ID サービスを実装し ](https://experienceleague.adobe.com/docs/id-service/using/home.html) その組織 ID （旧称：[!DNL IMS Org ID]）を提供する必要があります。

最初の同期には約 24 時間かかります。 その後、データは 1 秒から 2 秒の遅延でリアルタイムに同期されます。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Audience Manager Setup]** をクリックします。

1. 広告主のAdobe Experience Cloud アカウントの一意の組織 ID を入力し、「**[!UICONTROL Submit]**」をクリックします。

   広告主の組織 ID がわからない場合は、[!UICONTROL Admin] > [!UICONTROL Manage Client] の広告主の設定の「**[!UICONTROL IMS Org ID]**」フィールドで検索します。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて ](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Adobe Experience Cloud ソリューションおよびサービスとの統合 ](/help/search-social-commerce/introduction/integrations.md)
