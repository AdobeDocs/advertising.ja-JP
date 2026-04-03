---
title: 加盟店アカウントの管理
description: Merchant Center アカウントのアカウント詳細を設定および管理する方法について説明します。
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/u5LpCPL1I8lLHD9n1cDT1rEPvCcultnuhIVcn7IqxnY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 789
ht-degree: 0%

---

# 加盟店アカウントの管理

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

Search, Social, &amp; Commerceは、広告主のGoogle Merchant CenterまたはMicrosoft Merchant Centerの各アカウントの商品データを毎日ダウンロードして表示できます。 さらに、Search, Social, &amp; Commerceでは、加盟店アカウントの内容に基づいて広告作成を自動的に行うことができます。Search, Social, &amp; Commerceで商品データを直接操作するには、アカウントのアクセス資格情報を含み、アクセス *が有効になっている対応するアカウントレコードを作成する必要があります*。

>[!NOTE]
>
>加盟店アカウントレコードを削除することはできません。 アカウントの種類を&#x200B;*disabled*&#x200B;に変更すると、アカウントへのアクセスを無効にできます。

## 加盟店アカウント詳細の作成 {#create-merchant-account}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

商品データを表示してマーチャント アカウントのトラッキングテンプレートを生成し、データに基づいて広告を作成するには、アカウントのアクセス資格情報とアカウント *のアクセス権を含む対応するアカウントレコードを作成する必要があります。*

>[!NOTE]
>
>加盟店ネットワークで実際のアカウントを作成するには、ネットワークのweb サイトに移動します。

1. メインメニューで「**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**」をクリックすると、「[!UICONTROL Accounts]」タブが開きます。

1. データテーブルの上のツールバーで、**[!UICONTROL Create Account]**&#x200B;をクリックします。

1. [加盟店アカウント設定](#merchant-account-settings)を指定します。

   1. [!UICONTROL Product Source] メニューで、マーチャント センターを選択します。

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. （[!DNL Google Ads] アカウントに必要。オプションは[!DNL Microsoft Advertising] アカウントに対して必要）検索、ソーシャル、およびCommerceが[[!DNL OAuth] 認証プロトコル &#x200B;](https://oauth.net/2/)を使用してアカウントにアクセスできるようにします。

      1. （[!DNL Microsoft Advertising] アカウントのみ）「**[!UICONTROL oAuth]**」を選択します。

      1. **[!UICONTROL Enable Connection]**&#x200B;をクリックします。

      1. （広告主のアカウントにログインしていない場合）広告主のアカウントにログインします。 ベストプラクティスは、Merchant Center アカウントへのコンテンツ API アクセスに資格情報を使用することです。

      1. アクセス/権限のリクエスト画面で、ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、その文字列を&#x200B;**[!UICONTROL oAuth Token]** フィールドに貼り付けます。

      1. その他のアカウント設定を指定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

   アカウント内のすべての商品の属性データは、次の日次の同期プロセス（ユーザーのローカルタイムゾーンで約06:00）の後、検索、ソーシャル、およびCommerceで利用できます。 その後、商品データを使用して、在庫フィードを使用した広告作成を自動化できます。

## 加盟店アカウントの詳細を編集 {#edit-merchant-account}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの資格情報が変更された場合、または加盟店アカウントのデータの取得と使用を停止する場合は、アカウントの詳細を編集します。

>[!NOTE]
>
>加盟店ネットワークで実際のアカウントを編集するには、ネットワークのweb サイトに移動します。

1. メインメニューで「**[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**」をクリックすると、「[!UICONTROL Accounts]」タブが開きます。

1. アカウント名の横にある「![設定の表示/編集](/help/search-social-commerce/assets/settings.png "設定の表示/編集")」をクリックします。

1. [加盟店アカウント設定](#merchant-account-settings)を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!NOTE]
>
>Search, Social, &amp; Commerceは、新しいアカウントデータと加盟店ネットワーク上のアカウントデータを同期する必要があります。 これは、ユーザーのローカルタイムゾーンの約06:00で1日1回自動的に発生します。

## 加盟店アカウントへのアクセスを無効にする {#disable-merchant-account}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

加盟店アカウントを無効にすると、Search, Social, &amp; Commerceはアカウントにログインしないため、更新された商品データを取得できません。 アカウントが有効になっている間に収集されたデータは引き続き保存され、製品データを使用して作成された既存の広告は、フィードテンプレートとフィードデータの設定に従って更新、一時停止、または削除されません。

1. メインメニューで「**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**」をクリックすると、「[!UICONTROL Accounts]」タブが開きます。

1. アカウント名の横にある「![設定の表示/編集](/help/search-social-commerce/assets/settings.png "設定の表示/編集")」をクリックします。

1. [!UICONTROL EF Account Type]を&#x200B;**[!UICONTROL Disabled]**&#x200B;に変更します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 加盟店アカウント設定 {#merchant-account-settings}

>[!NOTE]
>
>販売者アカウント設定を設定できるのは、代理店アカウントマネージャー、[!DNL Adobe] アカウントマネージャー、および管理者ユーザーの役割のみです。

**[!UICONTROL Product Source]:** マーチャント ネットワーク。 既存のアカウントの値は変更できません。

**[!UICONTROL OAuth Token]:** （[!DNL Google Merchant Center] アカウントのみ） アカウントのトークンは、[[!DNL OAuth] 認証プロトコル &#x200B;](https://oauth.net/2/)を使用してログインを認証します。

**[!UICONTROL Auth Type]:** （[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]のみ）次を使用してアカウントへのログインを許可するかどうか：

* *[!UICONTROL Client login]:* クライアントのログインを使用します。

* *[!UICONTROL oAuth]* （デフォルト）: [[!DNL OAuth] 認証プロトコル &#x200B;](https://oauth.net/2/)を使用するには。

**[!UICONTROL Access Key]:** （[!DNL Microsoft Merchant Center]のみ）開発者アカウントが使用するアクセスキー。

**[!UICONTROL Account Name]:** Search, Social, &amp; Commerce内のアカウントに表示される名前。

**[!UICONTROL Login]:** アカウントのログイン名またはID。

**[!UICONTROL Password]:** アカウントのパスワード。

**[!UICONTROL Confirm Password]:** アカウントのパスワード。

**[!UICONTROL EF Account Type]:** Search、Social、およびCommerceがアカウントにアクセスするかどうか：

* *[!UICONTROL Enabled]* （デフォルト）:Search、Social、およびCommerceは、アカウントにログインして商品データを取得できます。

* *[!UICONTROL Disabled]:* Search, Social, &amp; Commerceはアカウントにログインしないため、更新された商品データを取得できません。 アカウントが有効になっている間に収集されたデータは引き続き保存され、製品データを使用して作成された既存の広告は、フィードテンプレートとフィードデータの設定に従って更新、一時停止、または削除されません。

**[!UICONTROL Account ID]:** マーチャント アカウント ID。 指定されたログイン情報を持つアカウントが1つしかない場合、この値はオプションです。

**[!UICONTROL Time Zone]:**&#x200B;広告主のタイムゾーン。 広告主のSearch, Social, &amp; Commerce アカウント情報（アカウントの作成時に設定されます）に設定されているのと同じタイムゾーンを使用します。 既存のアカウントの値は変更できません。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントについて](ad-network-account-about.md)
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
