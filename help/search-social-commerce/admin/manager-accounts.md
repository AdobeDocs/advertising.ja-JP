---
title: ad network manager アカウントの資格情報の管理
description: 管理者アカウントの資格情報を指定する方法  [!DNL Google Ads]  説明します。
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# ad network manager アカウントの資格情報の管理

*[!DNL Google Ads]アカウントのみ*

検索、ソーシャル、Commerceでクロスアカウントコンバージョンをアップロードする [!DNL Google Ads] Manager アカウントの資格情報を指定します。 この機能を使用するのは、a） [!DNL Adobe] 追跡されたクロスアカウントコンバージョン指標を [!DNL Google Ads] manager アカウントにアップロードする場合、または b） クロスアカウントコンバージョンを含むポートフォリオ目標をハイブリッド最適化のために [!DNL Google Ads] にアップロードする場合です。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

新しいマネージャーアカウントレコードの資格情報を追加したり、既存のマネージャーアカウントを再認証したりできます。

管理者アカウントの資格情報を追加すると、アカウント設定に、関連する管理者アカウント ID が読み取り専用として表示されます。 さらに、[!UICONTROL Campaigns]/[!UICONTROL Accounts] ビューのオプションの「[!UICONTROL Manager Account for Cross-Account Conversions]」列には、各子アカウントの管理者アカウント ID が表示され、管理者アカウントが認証されていない場合にエラーを示します。 [!UICONTROL Notification Center] には、マネージャーアカウントの資格情報がない場合（[[!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)）、またはマネージャーアカウント認証トークンの有効期限が切れる場合（[[!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)）に通知が含まれます。

## 新しいマネージャーアカウントの資格情報を追加するには

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Admin]/[!UICONTROL Manager Accounts]** をクリックします。

1. 「**[!UICONTROL Create new manager account]**」を選択します。

1. マネージャ・アカウントのログイン認証情報を入力します。

   **[!UICONTROL Manager Account ID]** と **[!UICONTROL Login Email]** は必須です。 検索、ソーシャル、Commerceでは、認証に使用するアカウントトークンが自動的にキャプチャおよび保存されます。

   必要に応じて、検索、ソーシャル、Commerce内の ID の **[!UICONTROL MCC Account Name]** とアカウント **[!UICONTROL Password]** を含めることができます。 暗号化する際にパスワードを入力して保存し、必要に応じてアカウントマネージャーがトークンを更新できるようにします。

1. 「**[!UICONTROL Authenticate]**」をクリックします。

1. 「**[!UICONTROL Save]**」をクリックします。

## 既存のマネージャ アカウントを再認証するには

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Admin]/[!UICONTROL Manager Accounts]** をクリックします。

1. 「**[!UICONTROL Reauthenticate existing manager account]**」を選択します。

1. マネージャーアカウントを選択します。

1. マネージャ・アカウントのログイン認証情報を入力します。

   **[!UICONTROL Manager Account ID]** と **ログインメール** は必須です。 検索、ソーシャル、Commerceでは、認証に使用するアカウントトークンが自動的にキャプチャおよび保存されます。

   必要に応じて、検索、ソーシャル、Commerce内の ID の **[!UICONTROL MCC Account Name]** とアカウント **[!UICONTROL Password]** を含めることができます。 暗号化する際にパスワードを入力して保存し、必要に応じてアカウントマネージャーがトークンを更新できるようにします。

1. 「**[!UICONTROL Authenticate]**」をクリックします。

1. 「**[!UICONTROL Save]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; 広告ネットワークへの目標のアップロードを有効にする &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [&#x200B; 検索、ソーシャル、Commerceで追跡されるコンバージョン指標のへのアップロード  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [&#x200B; 通知設定の編集 &#x200B;](/help/search-social-commerce/notifications/notification-edit.md)
