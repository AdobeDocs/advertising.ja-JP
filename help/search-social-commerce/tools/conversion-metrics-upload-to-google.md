---
title: 検索、ソーシャル、Commerceで追跡されるコンバージョン指標の  [!DNL Google Ads] へのアップロード
description: 検索、ソーシャル、Commerceで追跡するコンバージョン指標を  [!DNL Google Ads] にアップロードする方法を説明します。
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 検索、ソーシャル、Commerceで追跡されるコンバージョン指標の [!DNL Google Ads] へのアップロード

*[!DNL Google Ads] アカウントとAdobe Advertisingコンバージョントラッキングのみを使用する広告主*

検索、ソーシャル、Commerceは、オプションで、Adobe Advertisingコンバージョントラッキングサービスを使用するキャンペーンで追跡するすべてのコンバージョン指標を [!DNL Google Ads] にアップロードで [!DNL Google Ads] ます。 このオプションでは、コンバージョンをハイブリッド最適化で使用することはできません。 Adobeコンバージョンをハイブリッド最適化に使用する場合は、「[ 広告ネットワークへの目標のアップロードの有効化 ](objective-upload-to-networks.md) を参照してください。

毎日のアップロードには、トラッキングされる `gclid` 値、広告主レベルのアトリビューションモデルを使用して定義されたコンバージョン値、タイムスタンプが含まれます。 アトリビューションモデルが更新された場合、次のアップロードでは新しいモデルが使用されますが、過去のデータは新しいモデルを使用するように更新されません。

>[!NOTE]
>
>このアップロードには、フィードファイルからAdobe Advertisingにアップロードされたコンバージョン指標は含まれません。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Tools]/[!UICONTROL Conversion Upload Setup]** をクリックします。

1. 「**[!UICONTROL Upload Conversions to Google Ads]**」の横にあるチェックボックスをオンにします。

1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う広告主。任意） EEA および英国のユーザーから、広告目的でデータをアップロードすることに対する同意を収集した場合は、**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]** の横にあるチェックボックスを選択します

1. 「**[!UICONTROL Save]**」をクリックします。

1. （コンバージョンが管理者アカウントレベルで追跡されている場合） [ 管理者アカウントの資格情報を追加 ](/help/search-social-commerce/admin/manager-accounts.md)**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Manager Accounts]** で行います。

>[!MORELIKETHIS]
>
>* [ 広告ネットワークへの目標のアップロードを有効にする ](objective-upload-to-networks.md)
