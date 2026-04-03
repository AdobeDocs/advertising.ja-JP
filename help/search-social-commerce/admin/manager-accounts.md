---
title: ad network manager アカウントの資格情報の管理
description: ' [!DNL Google Ads] manager アカウントに資格情報を提供する方法について説明します。'
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
TQID: https://experienceleague.adobe.com/NHgpx-F19gX8jsOIPijPzNlGVhBje-CVsj4jjlV1OR0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 0%

---

# ad network manager アカウントの資格情報の管理

*[!DNL Google Ads]アカウントのみ*

Search、Social、およびCommerceでクロスアカウントコンバージョンをアップロードする[!DNL Google Ads] マネージャーアカウントの資格情報を指定します。 この機能は、a）トラッキングされたクロスアカウントのコンバージョン指標を[!DNL Adobe] マネージャーアカウントにアップロードする場合、またはb）クロスアカウントのコンバージョンを含むポートフォリオ目標を[!DNL Google Ads]にアップロードしてハイブリッド最適化を行う場合に使用します。[!DNL Google Ads]

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

新しいマネージャーアカウントレコードの資格情報を追加したり、既存のマネージャーアカウントを再認証したりできます。

マネージャーアカウントの資格情報を追加すると、アカウント設定に関連するマネージャーアカウント IDが読み取り専用として表示されます。 さらに、[!UICONTROL Manager Account for Cross-Account Conversions] > [!UICONTROL Campaigns] ビューのオプションの「[!UICONTROL Accounts]」列には、各子アカウントのマネージャーアカウント IDが表示され、マネージャーアカウントが認証されていない場合のエラーが示されます。 [!UICONTROL Notification Center]には、マネージャーアカウントの資格情報が見つからない場合（[個の[!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)）またはマネージャーアカウント認証トークンの有効期限（[個の[!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)）に通知が含まれます。

## 新しいマネージャーアカウントの資格情報を追加するには

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;をクリックします。

1. **[!UICONTROL Create new manager account]**&#x200B;を選択します。

1. マネージャーアカウントのログイン資格情報を入力します。

   **[!UICONTROL Manager Account ID]**&#x200B;と&#x200B;**[!UICONTROL Login Email]**&#x200B;は必須です。 Search, Social, &amp; Commerceは、認証に使用するアカウントトークンを自動的に取得して保存します。

   オプションで、Search, Social, &amp; Commerce内のID用に&#x200B;**[!UICONTROL MCC Account Name]**&#x200B;とアカウント **[!UICONTROL Password]**&#x200B;を含めることができます。 暗号化して保存する際にパスワードを入力し、アカウントマネージャーが必要に応じてトークンを更新できるようにします。

1. **[!UICONTROL Authenticate]**&#x200B;をクリックします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 既存のマネージャーアカウントを再認証するには

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;をクリックします。

1. **[!UICONTROL Reauthenticate existing manager account]**&#x200B;を選択します。

1. マネージャーアカウントを選択します。

1. マネージャーアカウントのログイン資格情報を入力します。

   **[!UICONTROL Manager Account ID]**&#x200B;と&#x200B;**ログイン電子メール**&#x200B;が必要です。 Search, Social, &amp; Commerceは、認証に使用するアカウントトークンを自動的に取得して保存します。

   オプションで、Search, Social, &amp; Commerce内のID用に&#x200B;**[!UICONTROL MCC Account Name]**&#x200B;とアカウント **[!UICONTROL Password]**&#x200B;を含めることができます。 暗号化して保存する際にパスワードを入力し、アカウントマネージャーが必要に応じてトークンを更新できるようにします。

1. **[!UICONTROL Authenticate]**&#x200B;をクリックします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [広告ネットワークへの目標のアップロードを有効にする](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [検索、ソーシャル、Commerceで追跡したコンバージョン指標を [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)にアップロード
>* [通知設定を編集](/help/search-social-commerce/notifications/notification-edit.md)
