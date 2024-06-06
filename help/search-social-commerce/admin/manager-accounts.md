---
title: ad network manager アカウントの資格情報の管理
description: の資格情報を指定する方法を説明します [!DNL Google Ads] manager accounts.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# ad network manager アカウントの資格情報の管理

*[!DNL Google Ads]アカウントのみ*

の資格情報を指定 [!DNL Google Ads] 検索、ソーシャル、Commerceでクロスアカウントコンバージョンをアップロードする Manager アカウント。 （を使用して）アップロードする場合は、この機能を使用します [!DNL Adobe] – 追跡される、へのクロスアカウントコンバージョン指標 [!DNL Google Ads] 管理者アカウントまたは b）へのクロスアカウントコンバージョンを含むポートフォリオ目標のアップロード [!DNL Google Ads] ハイブリッド最適化の場合。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

新しいマネージャーアカウントレコードの資格情報を追加したり、既存のマネージャーアカウントを再認証したりできます。

管理者アカウントの資格情報を追加すると、アカウント設定に、関連する管理者アカウント ID が読み取り専用として表示されます。 さらに、オプションの「[!UICONTROL Manager Account for Cross-Account Conversions]列（ [!UICONTROL Campaigns] > [!UICONTROL Accounts] ビューには、子アカウントごとのマネージャーアカウント ID と、マネージャーアカウントが認証されていない場合のエラーが表示されます。 [!UICONTROL Notification Center] マネージャーアカウントの資格情報がない場合の通知を含めます（[この [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)）または manager アカウント認証トークンの有効期限が切れた場合（[この [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)）に設定します。

## 新しいマネージャーアカウントの資格情報を追加するには

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. を選択 **[!UICONTROL Create new manager account]**.

1. マネージャ・アカウントのログイン認証情報を入力します。

   この **[!UICONTROL Manager Account ID]** および **[!UICONTROL Login Email]** は必須です。 検索、ソーシャル、Commerceでは、認証に使用するアカウントトークンが自動的にキャプチャおよび保存されます。

   オプションで、次を含めることができます **[!UICONTROL MCC Account Name]** 検索、ソーシャル、Commerce内およびアカウント内の識別用 **[!UICONTROL Password]**. 暗号化する際にパスワードを入力して保存し、必要に応じてアカウントマネージャーがトークンを更新できるようにします。

1. クリック **[!UICONTROL Authenticate]**.

1. クリック **[!UICONTROL Save]**.

## 既存のマネージャ アカウントを再認証するには

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. を選択 **[!UICONTROL Reauthenticate existing manager account]**.

1. マネージャーアカウントを選択します。

1. マネージャ・アカウントのログイン認証情報を入力します。

   この **[!UICONTROL Manager Account ID]** および **Login Email** は必須です。 検索、ソーシャル、Commerceでは、認証に使用するアカウントトークンが自動的にキャプチャおよび保存されます。

   オプションで、次を含めることができます **[!UICONTROL MCC Account Name]** 検索、ソーシャル、Commerce内およびアカウント内の識別用 **[!UICONTROL Password]**. 暗号化する際にパスワードを入力して保存し、必要に応じてアカウントマネージャーがトークンを更新できるようにします。

1. クリック **[!UICONTROL Authenticate]**.

1. クリック **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [広告ネットワークへの目標のアップロードを有効にする](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [へのコンバージョン指標のアップロード [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [通知設定の編集](/help/search-social-commerce/notifications/notification-edit.md)
