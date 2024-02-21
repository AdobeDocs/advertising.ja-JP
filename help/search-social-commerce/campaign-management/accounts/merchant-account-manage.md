---
title: マーチャントアカウントの管理
description: マーチャントセンターアカウントのアカウント詳細を設定および管理する方法を説明します。
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: 35a27d075d5de7c3526cd6522376671954b608db
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# マーチャントアカウントの管理

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

検索、ソーシャル、コマースは、広告主のGoogleマーチャントセンターまたはMicrosoftマーチャントセンターアカウントの製品データを毎日ダウンロードおよび表示できます。 また、Search, Social, &amp; Commerce は、マーチャントアカウントの内容に基づいて広告の作成を自動化できます。Search, Social, &amp; Commerce で製品データを直接操作するには、アカウントのアクセス資格情報とアクセス権を含む対応するアカウントレコードを作成する必要があります *有効*.

>[!NOTE]
>
>マーチャントアカウントレコードは削除できません。 アカウントタイプを *無効*.

## マーチャントアカウントの詳細を作成 {#create-merchant-account}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

商人アカウントの製品データを表示し、トラッキングテンプレートを生成し、データに基づいて広告を作成するには、アカウントアクセス資格情報とアカウントへのアクセス権を含む対応するアカウントレコードを作成する必要があります *有効*.

>[!NOTE]
>
>マーチャントネットワーク上に実際のアカウントを作成するには、ネットワークの Web サイトにアクセスします。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**（が開きます） [!UICONTROL Accounts] タブをクリックします。

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Create Account]**.

1. 次を指定します。 [マーチャントアカウント設定](#merchant-account-settings):

   1. Adobe Analytics の [!UICONTROL Product Source] メニューで、「マーチャントセンター」を選択します。

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. ( 必須 [!DNL Google Ads] アカウント；オプション [!DNL Microsoft Advertising] アカウント ) 検索、ソーシャル、コマースで、 [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] アカウントのみ ) を選択します。 **[!UICONTROL oAuth]**.

      1. クリック **[!UICONTROL Enable Connection]**.

      1. （広告主のアカウントにログインしていない場合）広告主のアカウントにログインします。 ベストプラクティスは、Merchant Center アカウントへのコンテンツ API アクセス用の資格情報を使用することです。

      1. アクセス/権限をリクエスト画面で、「 」ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、 **[!UICONTROL oAuth Token]** フィールドに入力します。

      1. その他のアカウント設定を指定します。

1. クリック **[!UICONTROL Save]**.

   アカウント内のすべての製品の属性データは、次の日次同期プロセス（ユーザーのローカルタイムゾーンで約 06:00）の後、検索、ソーシャルおよびコマースで使用できます。 その後、製品データを使用して、在庫フィードを使用した広告作成を自動化できます。

## マーチャントアカウントの詳細を編集 {#edit-merchant-account}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの資格情報が変更された場合、またはマーチャントアカウントのデータの取得と使用を停止する場合は、アカウントの詳細を編集します。

>[!NOTE]
>
>マーチャントネットワーク上の実際のアカウントを編集するには、ネットワークの Web サイトに移動します。

1. メインメニューで、 **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**（が開きます） [!UICONTROL Accounts] タブをクリックします。

1. アカウント名の横にある ![設定を表示/編集](/help/search-social-commerce/assets/settings.png "設定を表示/編集").

1. を編集します。 [マーチャントアカウント設定](#merchant-account-settings).

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
>検索、ソーシャル、コマースでは、新しいアカウントデータをマーチャントネットワーク上のデータと同期する必要があります。 これは、ユーザーのローカルタイムゾーンの 1 日に 1 回、約 06:00 に自動的に発生します。

## マーチャントアカウントへのアクセスを無効にする {#disable-merchant-account}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

マーチャントアカウントを無効にすると、Search、Social、および Commerce はアカウントにログインしないので、更新された製品データを取得しません。 アカウントの有効化中に収集されたデータは、引き続き保存され、製品データを使用して作成された既存の広告は、フィードテンプレートおよびフィードデータの設定に従って更新、一時停止、削除されません。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** （が開きます） [!UICONTROL Accounts] タブをクリックします。

1. アカウント名の横にある ![設定を表示/編集](/help/search-social-commerce/assets/settings.png "設定を表示/編集").

1. 次を変更： [!UICONTROL EF Account Type] から **[!UICONTROL Disabled]**.

1. クリック **[!UICONTROL Save]**.

## マーチャントアカウント設定 {#merchant-account-settings}

>[!NOTE]
>
>代理店のアカウントマネージャーのみ、 [!DNL Adobe] アカウントマネージャーおよび管理者ユーザーロールは、マーチャントアカウント設定を構成できます。

**[!UICONTROL Product Source]:** マーチャントネットワーク。 既存のアカウントの値は変更できません。

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] アカウントのみ ) [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] （のみ）次を使用して、アカウントへのログインを承認するかどうかを指定します。

* *[!UICONTROL Client login]:* クライアントのログインを使用する場合。

* *[!UICONTROL oAuth]* （デフォルト）: [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] （のみ）使用する開発者アカウントのアクセスキー。

**[!UICONTROL Account Name]:** 検索、ソーシャル、コマース内のアカウントに表示される名前。

**[!UICONTROL Login]:** アカウントのログイン名または ID。

**[!UICONTROL Password]:** アカウントのパスワード。

**[!UICONTROL Confirm Password]:** アカウントのパスワード。

**[!UICONTROL EF Account Type]:** 検索、ソーシャル、コマースがアカウントにアクセスするかどうか：

* *[!UICONTROL Enabled]* （デフォルト）:Search、Social、および Commerce は、アカウントにログインして製品データを取得できます。

* *[!UICONTROL Disabled]:* Social、Commerce での検索は、アカウントにログインしないので、更新された製品データは取得されません。 アカウントの有効化中に収集されたデータは、引き続き保存され、製品データを使用して作成された既存の広告は、フィードテンプレートおよびフィードデータの設定に従って更新、一時停止、削除されません。

**[!UICONTROL Account ID]:** マーチャントアカウント ID。 指定したログイン情報を持つアカウントが 1 つだけの場合、この値はオプションです。

**[!UICONTROL Time Zone]:** 広告主のタイムゾーン。 広告主の検索、ソーシャル、コマースの各アカウント情報（アカウントの作成時に設定される）に設定されているのと同じタイムゾーンを使用します。 既存のアカウントの値は変更できません。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントについて](ad-network-account-about.md)
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
