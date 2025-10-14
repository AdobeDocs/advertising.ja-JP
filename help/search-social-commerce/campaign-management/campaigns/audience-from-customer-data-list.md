---
title: 顧客データリストを使用したカスタマーマッチオーディエンスの管理
description: 顧客データリストからオーディエンスを作成および編集  [!DNL Google Ads]  お  [!DNL Microsoft Advertising]  び顧客一致させる方法を説明します。
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 顧客データリストを使用した [!DNL Google Ads] および [!DNL Microsoft Advertising] 顧客マッチオーディエンスの管理

顧客データリストから [!DNL Google Ads] を作成し、顧客一致オーディエンスを [!DNL Microsoft Advertising] 成できます。 また、[!DNL Adobe] オーディエンスから作成されたオーディエンスを除く、任意の [!DNL Google Ads] または [!DNL Microsoft Advertising] のカスタマーマッチオーディエンス [!DNL Google Ads] 更新することもできます。

## 顧客データリストからの顧客一致オーディエンスの作成

カスタマーマッチの対象となる *[!DNL Google Ads]および [!DNL Microsoft Advertising] アカウントのみ*

顧客関係管理（CRM）システムから生成したデータファイルから、[!DNL Google Ads] または [!DNL Microsoft Advertising] の顧客データベースのリストを作成できます。

[!DNL Microsoft Advertising] アカウントの場合、ファイルにはメールアドレスを含めることができます。 [!DNL Google Ads] アカウントの場合、ファイルには、メールアドレス、住所または電話番号、ユーザー ID、CRM のモバイルデバイス ID を含めることができます。

>[!NOTE]
>
>検索、ソーシャル、Commerceには、アップロードした顧客データや、[!DNL Google Ads] ーザーまたは [!DNL Microsoft Advertising] オーディエンスの作成または編集に使用された [!DNL Adobe] セグメントの顧客データは格納されません。

1. 顧客データを含んだファイルを必要な形式で生成します。

   姓名、メールアドレスおよび電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> [!DNL Google Ads] オーディエンスの場合、許可された連絡先情報のフィールドと要件のリストについては、「[&#x200B; ハッシュ化されたデータをアップロードするためのフォーマットガイドライン &#x200B;](https://support.google.com/google-ads/answer/7476159)」に関する [!DNL Google Ads] のドキュメントを参照してください。 [!DNL Microsoft Advertising] のオーディエンスについては、[!DNL Microsoft Advertising] 顧客一致リストの準備 [&#x200B; に関するドキュメントを参照してください &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/56921)。 必要に応じて、連絡先情報の [!DNL Microsoft Excel] テンプレートをダウンロードできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![&#x200B; 作成 &#x200B;](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワークとアカウント名を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. オーディエンス情報を指定します。

   1. [!UICONTROL Data Source] メニューで、「**[!UICONTROL Customer List]**」を選択します。

   1. **[!UICONTROL Audience Name]** を入力します。

   1. ファイルをアップロードします。

      1. *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*、*[!UICONTROL User IDs]*、*[!UICONTROL Mobile Device IDs]* のい [!UICONTROL Data Upload Type] れかを選択します。

         「ユーザー ID」オプションは、[&#x200B; ユーザー ID セグメント &#x200B;](https://support.google.com/google-ads/answer/9199250) をオプトインした米国の [!DNL Google Ads] の広告主のみが使用できます

      1. （モバイルデバイス ID リストのみ） **[!UICONTROL OS Type]** （*[!UICONTROL Android™]* または *[!UICONTROL iOS]*）を選択し、**[!UICONTROL App ID]** を入力します。

         アプリ ID は、アプリケーションがGoogle PlayまたはApple App Storeに接続できるようにするためにモバイルオペレーティングシステムで使用される一意の ID です。

         * （[!DNL Android™] apps） [!DNL Google Play] 内の [!DNL Android™] パッケージ名。「`id=<package_name>`」で識別されます。

           例えば、`https://play.google.com/store/apps/details?id=com.example.game` では、パッケージ名は com.example.game です。

         * （[!DNL iOS] アプリ） [!DNL iTunes App Store] 内のアプリケーション ID。URL の末尾に「`<idNNNNNNNNN>`」が付きます。 また、[!DNL iOS Developer Console] でも利用できます。

           例えば、`https://itunes.apple.com/us/app/id284882215` では、ID は id284882215 です。

         開発チームが、関連するプラットフォームの [!UICONTROL App ID] にアクセスできます。

      1. [!UICONTROL Select File] フィールドで **[!UICONTROL Choose File]** をクリックし、ネットワークまたはデバイス上のファイルを選択します。

      1. [!DNL Adobe] および広告ネットワークのプライバシーポリシーの条項に同意することを示すチェックボックスをオンにします。

      1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う [!DNL Google Ads] オーディエンスを作成する広告主。オプション） EEA および英国のユーザーから、広告目的でデータをアップロードすることに同意する場合は、**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]** の横にあるチェックボックスを選択します

      [!DNL Google Ads] は、同意ステータスが未指定の EEA および英国のユーザーに関するデータを無視します。 これにより、データの不一致とパフォーマンスの問題が発生する可能性があります。

      1. 「**[!UICONTROL Upload File]**」をクリックします。

   1. **[!UICONTROL Membership Days]** 数を指定します。これは、ユーザーの Cookie がオーディエンスに残る日数です。

   広告がユーザーに関連すると予想される時間の長さを使用します。 値を入力しない限り、顧客リストに有効期限はありません。

1. 「**[!UICONTROL Post]**」をクリックします。

>[!NOTE]
>
>* 広告ネットワークは、ファイルを処理するのに最大 24 時間かかる場合があります。
>* [[!DNL Google Ads]  カスタマーマッチの仕組みと制限事項に関するドキュメント &#x200B;](https://support.google.com/displayvideo/answer/9539301) を参照してください。

## 顧客データリストを使用した顧客一致オーディエンスの編集

[!DNL Adobe] オーディエンスから作成されたオーディエンスを除く、任意の [!DNL Google Ads] または [!DNL Microsoft Advertising] のカスタマーマッチオーディエンス [!DNL Google Ads] 更新できます。 データをアップロードして、オーディエンスの既存のデータを追加、削除または置き換えることができます。

データは、元の顧客リストと同じタイプ（特定のモバイルオペレーティングシステム上の特定のアプリのメールアドレス、住所、電話番号、ユーザー ID、モバイルデバイス ID）である必要があります。

1. 既存のデータタイプに必要な形式の顧客データを含んだファイルを生成します。

姓名、メールアドレスおよび電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> [!DNL Google Ads] オーディエンスの場合、許可された連絡先情報のフィールドと要件のリストについては、「[&#x200B; ハッシュ化されたデータをアップロードするためのフォーマットガイドライン &#x200B;](https://support.google.com/google-ads/answer/7476159)」に関する [!DNL Google Ads] のドキュメントを参照してください。 [!DNL Microsoft Advertising] オーディエンスについては、[ 顧客一致リストの準備 ] （https://help.ads.microsoft.com/#apex/ads/en/56921）に関する [!DNL Microsoft Advertising] ドキュメントを参照してください。 必要に応じて、連絡先情報の [!DNL Microsoft Excel] テンプレートをダウンロードできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** をクリックします。

1. 編集するオーディエンスの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[![&#x200B; 編集 &#x200B;](/help/search-social-commerce/assets/edit.png)] をクリックします。

1. アクション（*[!UICONTROL Add]* （既存のデータが存在する場合を除いて、アップロードしたデータを既存のデータに追加する場合）、*[!UICONTROL Delete]* （既存のデータが存在する場合に、アップロードしたデータを既存のデータから削除する場合）、*[!UICONTROL Replace]* （既存のデータをすべて削除し、アップロードしたデータに置き換える場合）を選択します。

1. ファイルをアップロードします。

   1. [!UICONTROL Select File] フィールドで **[!UICONTROL Choose File]** をクリックし、ネットワークまたはデバイス上のファイルを選択します。

   1. [!DNL Adobe] および広告ネットワークのプライバシーポリシーの条項に同意することを示すチェックボックスをオンにします。

   1. 「**[!UICONTROL Upload File]**」をクリックします。

1. 「**[!UICONTROL Post]**」をクリックします。

>[!NOTE]
>
>広告ネットワークでは、オーディエンスに対する更新を処理するのに時間がかかる場合があります。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスについて &#x200B;](audience-about.md)
>* [&#x200B; オーディエ  [!DNL Google Ads]  スからの顧客一致オーディエ  [!DNL Adobe]  スの作成 &#x200B;](google-audience-from-adobe-audience.md)
>* [Adobe Campaign [!DNL Google Ads]  メールリストからカスタマーマッチオーディエンスを作成 &#x200B;](google-audience-from-campaign-email-list.md)
>* [&#x200B; 動的リマーケティングオーディエンスの管理 &#x200B;](audience-dynamic-remarketing-manage.md)
