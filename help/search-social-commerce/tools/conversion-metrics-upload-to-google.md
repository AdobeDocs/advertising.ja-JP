---
title: 検索、ソーシャル、Commerceで追跡したコンバージョン指標を [!DNL Google Ads]にアップロードします
description: 検索、ソーシャル、Commerceで追跡されたコンバージョン指標を [!DNL Google Ads]にアップロードする方法について説明します。
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
TQID: https://experienceleague.adobe.com/ayxUfDgkrnPz0s-pFAdkmvYy94Il5szQHl6lYg8DpF8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# 検索、ソーシャル、Commerceで追跡したコンバージョン指標を[!DNL Google Ads]にアップロードします

*件のアカウントを持つ[!DNL Google Ads]広告主とAdobe Advertising コンバージョンのトラッキングのみ*

Search, Social, &amp; Commerceでは、Adobe Advertising コンバージョン追跡サービスを使用する[!DNL Google Ads]件のキャンペーンで追跡するすべてのコンバージョン指標を、オプションで[!DNL Google Ads]にアップロードできます。 このオプションでは、ハイブリッド最適化でコンバージョンを利用することはできません。 Adobe コンバージョンをハイブリッド最適化に使用する場合は、「[広告ネットワークへの目標のアップロードを有効にする](objective-upload-to-networks.md)」を参照してください。

毎日のアップロードには、トラッキングされた`gclid`値、広告主レベルのアトリビューションモデルを使用して定義されたコンバージョン値、およびタイムスタンプが含まれます。 アトリビューションモデルが更新された場合、次のアップロードでは新しいモデルが使用されますが、過去のデータは新しいモデルを使用するように更新されません。

>[!NOTE]
>
>アップロードには、フィードファイルからAdobe Advertisingにアップロードされたコンバージョン指標は含まれません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**&#x200B;をクリックします。

1. **[!UICONTROL Upload Conversions to Google Ads]**&#x200B;の横にあるチェックボックスをオンにします。

1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う広告主。オプション）広告目的でデータをアップロードするためにEEAおよび英国のユーザーから同意を得た場合は、**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;の横にあるチェックボックスをオンにします

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （コンバージョンがマネージャーアカウントレベルで追跡されている場合） [&#x200B; マネージャーアカウントの資格情報](/help/search-social-commerce/admin/manager-accounts.md)を&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;に追加します。

>[!MORELIKETHIS]
>
>* [広告ネットワークへの目標のアップロードを有効にする](objective-upload-to-networks.md)
