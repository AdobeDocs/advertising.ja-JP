---
title: 顧客データリストを使用した顧客一致オーディエンスの管理
description: 作成および編集方法を学ぶ [!DNL Google Ads] および [!DNL Microsoft® Advertising] 顧客データリストからの顧客一致オーディエンス。
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] および [!DNL Microsoft® Advertising] 顧客データリストを使用した顧客マッチング

次の項目を作成できます。 [!DNL Google Ads] および [!DNL Microsoft® Advertising] 顧客データリストからの顧客一致オーディエンス。 また、 [!DNL Google Ads] または [!DNL Microsoft® Advertising] を除く顧客一致オーディエンス [!DNL Google Ads] から作成されたオーディエンス [!DNL Adobe] オーディエンス。

## 顧客データリストからの顧客一致オーディエンスの作成

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] カスタマーマッチの条件を満たすアカウント*

次の項目を作成できます。 [!DNL Google Ads] または [!DNL Microsoft® Advertising] 顧客関係管理 (CRM) システムから生成するデータファイルの顧客データベースのリスト。

の場合 [!DNL Microsoft® Advertising] アカウントには、ファイルに電子メールアドレスを含めることができます。 の場合 [!DNL Google Ads] アカウント、ファイルには、電子メールアドレス、郵送先住所、電話番号、ユーザー ID、CRM のモバイルデバイス ID などを含めることができます。

>[!NOTE]
>
>Search、Social、および Commerce では、アップロードした顧客データや [!DNL Adobe] 作成または編集に使用されるセグメント [!DNL Google Ads] または [!DNL Microsoft® Advertising] オーディエンス。

1. 必要な形式の顧客データを含むファイルを生成します。

   姓と名、電子メールアドレスおよび電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> の場合 [!DNL Google Ads] オーディエンスについては、 [!DNL Google Ads] ドキュメント (「 」)[ハッシュ化されたデータをアップロードする際の書式設定のガイドライン](https://support.google.com/google-ads/answer/7476159)」をクリックします。 の場合 [!DNL Microsoft® Advertising] オーディエンスについては、 [!DNL Microsoft® Advertising] に関するドキュメント [カスタマーマッチリストの準備](https://help.ads.microsoft.com/#apex/ads/en/56921. オプションで、 [!DNL Microsoft® Excel] 連絡先情報のテンプレート。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. オーディエンス情報を指定します。

   1. Adobe Analytics の [!UICONTROL Data Source] メニュー、選択 **[!UICONTROL Customer List]**.

   1. 次を入力します。 **[!UICONTROL Audience Name]**.

   1. ファイルをアップロードします。

      1. を選択します。 [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*&#x200B;または *[!UICONTROL Mobile Device IDs]*.

         「ユーザー ID 」オプションを使用できるのは、次の場合のみです。 [!DNL Google Ads] ～に対してオプトインしている米国の広告主 [ユーザー ID セグメント](https://support.google.com/google-ads/answer/9199250)

      1. （モバイルデバイス ID リストのみ） **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* または *[!UICONTROL iOS]*) をクリックし、 **[!UICONTROL App ID]**.

         アプリ ID は、モバイルオペレーティングシステムがアプリケーションがGoogle PlayまたはApple App Storeに接続する際に使用する一意の識別子です。

         * ([!DNL Android™] apps) [!DNL Android™] 内のパッケージ名 [!DNL Google Play]（で識別）`id=<package_name>`.&quot;

           例えば、https://play.google.com/store/apps/details?id=com.example.gameでは、パッケージ名は com.example.game です。

         * ([!DNL iOS] apps) 内のアプリケーション ID [!DNL iTunes App Store]（で識別）`<idNNNNNNNNN>`」という名前に変更されます。 また、 [!DNL iOS Developer Console].

           例えば、https://itunes.apple.com/us/app/id284882215では、ID はid284882215です。

         開発チームが [!UICONTROL App ID] 関連するプラットフォーム用。

      1. Adobe Analytics の [!UICONTROL Select File] 「 」フィールドで、「 **[!UICONTROL Choose File]** お使いのネットワークまたはデバイス上のファイルを選択します。

      1. 「 」チェックボックスを選択して、の利用条件に同意したことを示します。 [!DNL Adobe] および広告ネットワークのプライバシーポリシー。

      1. ( 広告主の作成 [!DNL Google Ads] 欧州経済圏 (EEA) または英国 (UK) でビジネスを行うオーディエンス（オプション）EEA および UK ユーザーから広告用にデータをアップロードする同意を収集している場合は、の横のチェックボックスをオンにします。 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] は、同意ステータスが未指定の EEA および UK ユーザーのデータをすべて無視します。 これは、データに相違が生じ、パフォーマンスに問題が生じる可能性があります。

      1. クリック **[!UICONTROL Upload File]**.

   1. 次の数を指定： **[!UICONTROL Membership Days]**：ユーザーの Cookie がオーディエンスに残る日数です。

   広告がユーザーに関連すると予想される時間の長さを使用します。 値を入力しない限り、顧客リストは期限切れになりません。

1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>* 広告ネットワークがファイルを処理するのに最大 24 時間かかる場合があります。
>* 詳しくは、 [[!DNL Google Ads] カスタマーマッチの仕組みと制限に関するドキュメント](https://support.google.com/displayvideo/answer/9539301).

## 顧客データリストを使用した顧客一致オーディエンスの編集

任意の [!DNL Google Ads] または [!DNL Microsoft® Advertising] を除く顧客一致オーディエンス [!DNL Google Ads] から作成されたオーディエンス [!DNL Adobe] オーディエンス。 データをアップロードして、そのオーディエンスの既存のデータを追加、削除またはすべて置き換えることができます。

データは、元の顧客リスト（電子メールアドレス、郵送先住所、電話番号、ユーザー ID、またはモバイルオペレーティングシステム上の特定のアプリのモバイルデバイス ID）と同じタイプである必要があります。

1. 既存のデータタイプに必要な形式の顧客データを含むファイルを生成します。

姓と名、電子メールアドレスおよび電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> の場合 [!DNL Google Ads] オーディエンスについては、 [!DNL Google Ads] ドキュメント (「 」)[ハッシュ化されたデータをアップロードする際の書式設定のガイドライン](https://support.google.com/google-ads/answer/7476159)」をクリックします。 の場合 [!DNL Microsoft® Advertising] オーディエンスについては、 [!DNL Microsoft® Advertising] に関するドキュメント [カスタマーマッチリストの準備](https://help.ads.microsoft.com/#apex/ads/en/56921. オプションで、 [!DNL Microsoft® Excel] 連絡先情報のテンプレート。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 編集するオーディエンスの横にあるチェックボックスを選択します。

1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png).

1. アクションを選択します。 *[!UICONTROL Add]* （既に存在する場合を除き、アップロードしたデータを既存のデータに追加） *[!UICONTROL Delete]* （既存のデータからアップロードされたデータが既に存在する場合にそのデータを削除）、または *[!UICONTROL Replace]* （既存のすべてのデータを削除し、アップロードされたデータに置き換える）

1. ファイルをアップロードします。

   1. Adobe Analytics の [!UICONTROL Select File] 「 」フィールドで、「 **[!UICONTROL Choose File]** お使いのネットワークまたはデバイス上のファイルを選択します。

   1. 「 」チェックボックスを選択して、の利用条件に同意したことを示します。 [!DNL Adobe] および広告ネットワークのプライバシーポリシー。

   1. クリック **[!UICONTROL Upload File]**.

1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>広告ネットワークは、オーディエンスの更新を処理するのに時間がかかる場合があります。

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [の作成 [!DNL Google Ads] Adobe Campaign電子メールリストからの顧客一致オーディエンス](google-audience-from-campaign-email-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
