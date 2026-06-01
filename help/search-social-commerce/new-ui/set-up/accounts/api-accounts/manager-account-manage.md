---
title: （新しいUI）Google Ads Manager アカウントの資格情報の管理
description: 新しいUIでGoogle Ads Manager アカウントの資格情報を設定および管理する方法について説明します。
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# （新しいUI） [!DNL Google Ads] マネージャーアカウントの資格情報の管理

*Beta機能*

*[!DNL Google Ads]アカウントのみ*

Search、Social、およびCommerceでクロスアカウントコンバージョンをアップロードする[!DNL Google Ads] マネージャーアカウントの資格情報を指定します。 この機能は、a）トラッキングされたクロスアカウントのコンバージョン指標を[!DNL Google Ads] マネージャーアカウントにアップロードする場合、またはb）クロスアカウントのコンバージョンを含むポートフォリオ目標を[!DNL Google Ads]にアップロードしてハイブリッド最適化を行う場合に使用します。[!DNL Adobe]

新しいマネージャーアカウントレコードの資格情報を追加したり、既存のマネージャーアカウントを再認証したりできます。

マネージャーアカウントの資格情報を追加すると、アカウント設定に関連するマネージャーアカウント IDが読み取り専用として表示されます。 [!UICONTROL Notification Center]には、マネージャーアカウントの資格情報が見つからない場合（例：[!UICONTROL Manager Account Missing Error]）、またはマネージャーアカウント認証トークンの有効期限が切れた場合（例：[!UICONTROL Manager Account Auth Error]）に[通知](/help/search-social-commerce/new-ui/notifications-manage.md)が含まれます。

## 新しいマネージャーアカウントの資格情報の追加 {#create-manager-account}

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**&#x200B;をクリックします。

1. **[!UICONTROL +]**&#x200B;をクリックします。

1. 広告ネットワークを選択し、**[!UICONTROL Next]**&#x200B;をクリックします。

1. [ マネージャーアカウント設定](#manager-account-settings)を指定します。

1. **[!UICONTROL Authenticate]**&#x200B;をクリックし、マネージャーアカウントの資格情報を使用してログインします。

   Search, Social, &amp; Commerceは、認証トークンを自動的に取得して保存します。

1. Search, Social, &amp; Commerceで、**[!UICONTROL Save]**&#x200B;をクリックします。

## マネージャーアカウントの詳細の編集 {#edit-manager-account}

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**&#x200B;をクリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、 （/help/search-social-commerce/assets/edit-new.png「編集」をクリック）をクリックします。

1. [ マネージャーアカウント設定](#manager-account-settings)を編集します。

1. **[!UICONTROL Re-Authenticate]**&#x200B;をクリックし、マネージャーアカウントの資格情報を使用してログインします。

   Search, Social, &amp; Commerceは、認証トークンを自動的に取得して保存します。

1. Search, Social, &amp; Commerceで、**[!UICONTROL Save]**&#x200B;をクリックします。

## マネージャーアカウントの再認証 {#reauthenticate-manager-account}

OAuth トークンが期限切れになったり、無効になったりすると、マネージャーアカウントを再認証します。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**&#x200B;をクリックします。

1. アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Reauthenticate]**&#x200B;をクリックします。

1. マネージャーアカウントの資格情報を使用してログインします。

   Search, Social, &amp; Commerceは、新しい認証トークンを自動的にキャプチャして保存します。

## マネージャーアカウント設定 {#manager-account-settings}

**[!UICONTROL Manager Account ID]:**&#x200B;広告ネットワーク上のマネージャーアカウントの一意のアカウント ID。

**[!UICONTROL Mnaager Account Name]:**&#x200B;検索、ソーシャル、およびCommerce内のマネージャーアカウントに表示する名前。

**[!UICONTROL Login Email]:** マネージャーアカウントのログインに関連付けられている電子メールアドレス。 認証に必要です。

**[!UICONTROL Password]:** （オプション） アカウントのパスワード。 暗号化して保存する際にパスワードを入力し、アカウントマネージャーが必要に応じてトークンを更新できるようにします。

>[!MORELIKETHIS]
>
>* [広告ネットワークへの目標のアップロードを有効にする](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [通知の管理](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
