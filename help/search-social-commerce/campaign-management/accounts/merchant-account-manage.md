---
title: マーチャントアカウントの管理
description: マーチャントセンターアカウントのアカウント詳細を設定および管理する方法について説明します。
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# マーチャントアカウントの管理

*エージェンシーアカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

検索、ソーシャルおよびCommerceでは、広告主のMicrosoft マーチャントセンターまたはGoogle マーチャントセンターアカウントの商品データを毎日ダウンロードして表示できます。 さらに、検索、ソーシャル、Commerceでは、マーチャントアカウントの内容に基づいて広告制作を自動化できます。検索、ソーシャル、Commerceで商品データを直接操作するには、アカウントのアクセス資格情報と、アクセス *有効* を含む、対応するアカウントレコードを作成する必要があります。

>[!NOTE]
>
>販売者の口座レコードは削除できません。 アカウントの種類を *無効* に変更すると、アカウントへのアクセスを無効にすることができます。

## マーチャントアカウントの詳細を作成 {#create-merchant-account}

*エージェンシーアカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

商品データを表示し、マーチャントアカウントのトラッキングテンプレートを生成し、データに基づいて広告を作成するには、アカウントのアクセス資格情報と、アカウントへのアクセス権を持つ *有効* アカウントレコードを作成する必要があります。

>[!NOTE]
>
>マーチャントネットワーク上で実際のアカウントを作成するには、ネットワークの web サイトにアクセスします。

1. メインメニューで、「\> **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]****[!UICONTROL Products]** クリックし、「[!UICONTROL Accounts]」タブを開きます。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Create Account]**] をクリックします。

1. [ マーチャントアカウント設定 ](#merchant-account-settings) を指定します。

   1. [!UICONTROL Product Source] メニューで、マーチャントセンターを選択します。

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. （[!DNL Google Ads] アカウントの場合は必須、[!DNL Microsoft Advertising] アカウントの場合はオプション）検索、ソーシャルおよびCommerceが [[!DNL OAuth]  認証プロトコル ](https://oauth.net/2/) を使用してアカウントにアクセスできるようにします。

      1. （[!DNL Microsoft Advertising] アカウントのみ）「**[!UICONTROL oAuth]**」を選択します。

      1. 「**[!UICONTROL Enable Connection]**」をクリックします。

      1. （広告主のアカウントにログインしていない場合）広告主のアカウントにログインします。 ベストプラクティスは、マーチャントセンターアカウントへのコンテンツ API アクセスに資格情報を使用することです。

      1. アクセス/権限のリクエスト画面で、「」ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、**[!UICONTROL oAuth Token]** フィールドに貼り付けます。

      1. その他のアカウント設定を指定します。

1. 「**[!UICONTROL Save]**」をクリックします。

   アカウント内のすべての商品の属性データは、次の日次同期プロセス（ユーザーのローカルタイムゾーンで約 06:00）後、検索、ソーシャル、Commerceで利用できます。 その後、製品データを使用して、在庫フィードを使用して広告の作成を自動化できます。

## 販売者アカウントの詳細の編集 {#edit-merchant-account}

*エージェンシーアカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの資格情報を変更する場合、またはマーチャントアカウントのデータの取得と使用を停止する場合は、アカウントの詳細を編集します。

>[!NOTE]
>
>マーチャントネットワーク上の実際のアカウントを編集するには、ネットワークの web サイトに移動します。

1. メインメニューで、「\> **[!UICONTROL Search]\> [!UICONTROL Campaigns][!UICONTROL Products]** クリックし、「[!UICONTROL Accounts]」タブを開きます。

1. アカウント名の横の「![ 設定を表示/編集 ](/help/search-social-commerce/assets/settings.png " 設定を表示/編集 ")」をクリックします。

1. [ マーチャントアカウント設定 ](#merchant-account-settings) を編集します。

1. 「**[!UICONTROL Save]**」をクリックします。

>[!NOTE]
>
>検索、ソーシャル、Commerceでは、新しいアカウントデータをマーチャントネットワーク上のアカウントデータと同期させる必要があります。 これは、ユーザーのローカルタイムゾーンの 06:00 頃に 1 日に 1 回自動的に発生します。

## マーチャントアカウントへのアクセスの無効化 {#disable-merchant-account}

*エージェンシーアカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

マーチャントアカウントを無効にすると、検索、ソーシャル、Commerceはアカウントにログインしないので、更新された商品データを取得できません。 アカウントが有効になっている間に収集されたデータは引き続き保存され、製品データを使用して作成された既存の広告は、フィードテンプレートとフィードデータの設定に従って、更新、一時停止、削除されることはありません。

1. メインメニューで **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** をクリックし、「[!UICONTROL Accounts]」タブを開きます。

1. アカウント名の横の「![ 設定を表示/編集 ](/help/search-social-commerce/assets/settings.png " 設定を表示/編集 ")」をクリックします。

1. [!UICONTROL EF Account Type] を **[!UICONTROL Disabled]** に変更します。

1. 「**[!UICONTROL Save]**」をクリックします。

## マーチャントアカウントの設定 {#merchant-account-settings}

>[!NOTE]
>
>代理店アカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみが、マーチャントアカウント設定を構成できます。

**[!UICONTROL Product Source]:** マーチャントネットワーク。 既存のアカウントの値は変更できません。

**[!UICONTROL OAuth Token]:** （[!DNL Google Merchant Center] アカウントのみ） [[!DNL OAuth]  認証プロトコル ](https://oauth.net/2/) を使用してログインを認証するためのアカウントのトークン。

**[!UICONTROL Auth Type]:** （[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] のみ）次を使用してアカウントへのログインを許可するかどうか：

* *[!UICONTROL Client login]:* クライアントのログインを使用します。

* *[!UICONTROL oAuth]* （デフォルト）: [[!DNL OAuth]  認証プロトコル ](https://oauth.net/2/) を使用します。

**[!UICONTROL Access Key]:** （[!DNL Microsoft Merchant Center] のみ）使用する開発者アカウントのアクセスキー。

**[!UICONTROL Account Name]:** 検索、ソーシャル、Commerce内でアカウントに対して表示される名前。

**[!UICONTROL Login]:** アカウントのログイン名または ID。

**[!UICONTROL Password]:** アカウントのパスワード。

**[!UICONTROL Confirm Password]:** アカウントのパスワード。

**[!UICONTROL EF Account Type]:** 検索、ソーシャル、Commerceがアカウントにアクセスするかどうか：

* *[!UICONTROL Enabled]* （デフォルト）：検索、ソーシャル、Commerceは、アカウントにログインして商品データを取得できます。

* *[!UICONTROL Disabled]:* 検索、ソーシャル、Commerceはアカウントにログインしないため、更新された商品データを取得しません。 アカウントが有効になっている間に収集されたデータは引き続き保存され、製品データを使用して作成された既存の広告は、フィードテンプレートとフィードデータの設定に従って、更新、一時停止、削除されることはありません。

**[!UICONTROL Account ID]:** マーチャントアカウント ID。 指定したログイン情報を持つアカウントが 1 つだけの場合、この値はオプションです。

**[!UICONTROL Time Zone]:** 広告主のタイムゾーン。 広告主の検索、ソーシャル、Commerceのアカウント情報と同じタイムゾーンを使用します（アカウントの作成時に設定されます）。 既存のアカウントの値は変更できません。

>[!MORELIKETHIS]
>
>* [ 広告ネットワークアカウントについて ](ad-network-account-about.md)
>* [ 広告ネットワークアカウントの管理 ](ad-network-account-manage.md)
