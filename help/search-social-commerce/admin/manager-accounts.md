---
title: Ad Network Manager アカウントの資格情報の管理
description: の資格情報の入力方法を説明します [!DNL Google Ads] 管理者アカウント
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# Ad Network Manager アカウントの資格情報の管理

*ベータ版機能*

*[!DNL Google Ads]アカウントのみ*

の資格情報を入力します。 [!DNL Google Ads] 検索、ソーシャル、コマースでクロスアカウントコンバージョンをアップロードするマネージャーアカウント。 ( ) アップロードする場合は、この機能を使用します。 [!DNL Adobe] — トラッキングされたアカウント間のコンバージョン指標から [!DNL Google Ads] マネージャーアカウントまたは b) 次の項目にクロスアカウントコンバージョンを含むポートフォリオ目標をアップロード [!DNL Google Ads] ハイブリッド最適化の場合。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

新しいマネージャーアカウントレコードの資格情報を追加したり、既存のマネージャーアカウントを再認証したりできます。

管理者アカウントの資格情報を追加すると、アカウント設定に、関連する管理者アカウント ID が読み取り専用として表示されます。 また、オプションの[!UICONTROL Manager Account for Cross-Account Conversions]」列 [!UICONTROL Campaigns] > [!UICONTROL Accounts] 「表示」には、各子アカウントの manager アカウント ID が表示され、manager アカウントが認証されていない場合にエラーが表示されます。 [!UICONTROL Notification Center] 管理者アカウントの資格情報が見つからない場合の通知 ([の [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) または Manager アカウント認証トークンの有効期限 ([の [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)) をクリックします。

## 新しいマネージャーアカウントの資格情報を追加するには

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 選択 **[!UICONTROL Create new manager account]**.

1. マネージャーアカウントのログイン資格情報を入力します。

   この **[!UICONTROL Manager Account ID]** および **[!UICONTROL Login Email]** が必要です。 検索、ソーシャル、コマースでは、認証に使用するアカウントトークンを自動的にキャプチャして保存します。

   オプションで、 **[!UICONTROL MCC Account Name]** 検索、ソーシャル、コマースおよびアカウント内での識別 **[!UICONTROL Password]**. アカウントマネージャーが必要に応じてトークンを更新できるように、暗号化して保存するパスワードを入力します。

1. クリック **[!UICONTROL Authenticate]**.

1. クリック **[!UICONTROL Save]**.

## 既存の Manager アカウントを再認証するには

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 選択 **[!UICONTROL Reauthenticate existing manager account]**.

1. マネージャーアカウントを選択します。

1. マネージャーアカウントのログイン資格情報を入力します。

   この **[!UICONTROL Manager Account ID]** および **ログインメール** が必要です。 検索、ソーシャル、コマースでは、認証に使用するアカウントトークンを自動的にキャプチャして保存します。

   オプションで、 **[!UICONTROL MCC Account Name]** 検索、ソーシャル、コマースおよびアカウント内での識別 **[!UICONTROL Password]**. アカウントマネージャーが必要に応じてトークンを更新できるように、暗号化して保存するパスワードを入力します。

1. クリック **[!UICONTROL Authenticate]**.

1. クリック **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [広告ネットワークへの目標のアップロードを有効にする](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [コンバージョン指標のアップロード先 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [通知設定を編集](/help/search-social-commerce/notifications/notification-edit.md)

