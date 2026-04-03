---
title: 顧客データリストを使用した顧客一致オーディエンスの管理
description: 顧客データリストから [!DNL Google Ads] および [!DNL Microsoft Advertising] 顧客一致オーディエンスを作成および編集する方法について説明します。
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/XoDGbJAFowx-KX0hWQH4XoFrc0R2YiftT-mN6f4KWDE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 840
ht-degree: 0%

---

# 顧客データリストを使用して、[!DNL Google Ads]および[!DNL Microsoft Advertising]の顧客一致オーディエンスを管理します

顧客データリストから[!DNL Google Ads]および[!DNL Microsoft Advertising]の顧客一致オーディエンスを作成できます。 [!DNL Google Ads]人のオーディエンスから作成された[!DNL Microsoft Advertising]人のオーディエンスを除き、[!DNL Google Ads]人または[!DNL Adobe]人の顧客一致オーディエンスを更新することもできます。

## 顧客データリストからカスタマーマッチオーディエンスを作成する

顧客の一致のみ&#x200B;*[!DNL Google Ads]の対象となる[!DNL Microsoft Advertising]および* アカウント

顧客関係管理（CRM）システムから生成したデータファイルから、[!DNL Google Ads]または[!DNL Microsoft Advertising]の顧客データベースのリストを作成できます。

[!DNL Microsoft Advertising] アカウントの場合、ファイルに電子メールアドレスを含めることができます。 [!DNL Google Ads] アカウントの場合、ファイルには、電子メールアドレス、郵送先住所、電話番号、ユーザーID、またはCRMのモバイルデバイス IDを含めることができます。

>[!NOTE]
>
>Search, Social, &amp; Commerceには、[!DNL Adobe]または[!DNL Google Ads]のオーディエンスの作成または編集に使用した[!DNL Microsoft Advertising] セグメントからアップロードした顧客データは保存されません。

1. 顧客データを含むファイルを必要な形式で生成します。

   氏名、メールアドレス、電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> [!DNL Google Ads]人のオーディエンスについては、許可されている連絡先情報フィールドと要件のリストについては、「[!DNL Google Ads] ハッシュ化されたデータのアップロードに関する書式設定ガイドライン [」の](https://support.google.com/google-ads/answer/7476159)のドキュメントを参照してください。 [!DNL Microsoft Advertising]人のオーディエンスについては、[!DNL Microsoft Advertising]顧客マッチリストの準備[に関する](https://help.ads.microsoft.com/#apex/ads/en/56921)のドキュメントを参照してください。 必要に応じて、連絡先情報の[!DNL Microsoft Excel] テンプレートをダウンロードできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワークとアカウント名を選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. オーディエンス情報を指定します。

   1. [!UICONTROL Data Source] メニューで、**[!UICONTROL Customer List]**&#x200B;を選択します。

   1. **[!UICONTROL Audience Name]**&#x200B;を入力します。

   1. ファイルをアップロードします。

      1. [!UICONTROL Data Upload Type]を選択します：*[!UICONTROL Emails, Phones, and/or Mailing Addresses]*、*[!UICONTROL User IDs]*、または&#x200B;*[!UICONTROL Mobile Device IDs]*。

         ユーザーID オプションは、[!DNL Google Ads] ユーザーID セグメント [にオプトインしている米国の](https://support.google.com/google-ads/answer/9199250)広告主のみが利用できます

      1. （モバイルデバイス ID リストのみ） **[!UICONTROL OS Type]** （*[!UICONTROL Android™]*&#x200B;または&#x200B;*[!UICONTROL iOS]*）を選択し、**[!UICONTROL App ID]**&#x200B;を入力します。

         アプリ IDは、モバイルオペレーティングシステムがアプリケーションをGoogle PlayまたはApple App Storeに接続するために使用する一意のIDです。

         * （[!DNL Android™] アプリ）「[!DNL Android™]」によって識別される[!DNL Google Play]内の`id=<package_name>` パッケージ名。

           例えば、`https://play.google.com/store/apps/details?id=com.example.game`では、パッケージ名はcom.example.gameです。

         * （[!DNL iOS] アプリ） [!DNL iTunes App Store]内のアプリケーション ID。URLの末尾に「`<idNNNNNNNNN>`」が表示されます。 [!DNL iOS Developer Console]でも利用できます。

           例えば、`https://itunes.apple.com/us/app/id284882215`では、IDはID284882215です。

         開発チームは、関連するプラットフォームの[!UICONTROL App ID]にアクセスできます。

      1. [!UICONTROL Select File] フィールドで、**[!UICONTROL Choose File]**&#x200B;をクリックし、ネットワークまたはデバイス上のファイルを選択します。

      1. 「[!DNL Adobe]」および広告ネットワークのプライバシーポリシーの条件に同意することを示すチェックボックスをオンにします。

      1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う[!DNL Google Ads]人のオーディエンスを作成する広告主。オプション）広告目的でデータをアップロードするEEAおよび英国のユーザーの同意を得た場合は、**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;の横にあるチェックボックスをオンにします

      [!DNL Google Ads]は、未指定の同意ステータスを持つEEAおよび英国ユーザーのデータを無視します。 これにより、データの不整合やパフォーマンスの問題につながる可能性があります。

      1. **[!UICONTROL Upload File]**&#x200B;をクリックします。

   1. ユーザーのCookieがオーディエンスに滞在する日数である&#x200B;**[!UICONTROL Membership Days]**&#x200B;の数を指定します。

   広告がユーザーに適していると期待される期間を使用します。 値を入力しない限り、顧客リストの有効期限は切れません。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!NOTE]
>
>* 広告ネットワークがファイルを処理するのに最大24時間かかる場合があります。
>* 顧客の一致の仕組みと制限に関する[[!DNL Google Ads]  ドキュメント ](https://support.google.com/displayvideo/answer/9539301)を参照してください。

## 顧客データリストを使用した顧客マッチオーディエンスの編集

[!DNL Google Ads]人のオーディエンスから作成された[!DNL Microsoft Advertising]人のオーディエンスを除き、[!DNL Google Ads]人または[!DNL Adobe]人の顧客一致オーディエンスを更新できます。 オーディエンスの既存のすべてのデータを追加、削除、置き換えるためにデータをアップロードできます。

データは、元の顧客リストと同じタイプ（特定のモバイルオペレーティングシステム上の特定のアプリのメールアドレス、郵送先住所、電話番号、ユーザーID、モバイルデバイス ID）である必要があります。

1. 既存のデータタイプに必要な形式の顧客データを含むファイルを生成します。

氏名、メールアドレス、電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> [!DNL Google Ads]人のオーディエンスについては、許可されている連絡先情報フィールドと要件のリストについては、「[!DNL Google Ads] ハッシュ化されたデータのアップロードに関する書式設定ガイドライン [」の](https://support.google.com/google-ads/answer/7476159)のドキュメントを参照してください。 [!DNL Microsoft Advertising]人のオーディエンスについては、[!DNL Microsoft Advertising]顧客マッチリストの準備[ （https://help.ads.microsoft.com/#apex/ads/en/56921）に関する]のドキュメントを参照してください。 必要に応じて、連絡先情報の[!DNL Microsoft Excel] テンプレートをダウンロードできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**&#x200B;をクリックします。

1. 編集するオーディエンスの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png)をクリックします。

1. アクションを選択します：*[!UICONTROL Add]* （アップロードされたデータを既存のデータに追加する場合は除く）、*[!UICONTROL Delete]* （アップロードされたデータを既存のデータから削除する場合は既に存在する場合）、または&#x200B;*[!UICONTROL Replace]* （既存のすべてのデータを削除し、アップロードされたデータに置き換える場合）。

1. ファイルをアップロードします。

   1. [!UICONTROL Select File] フィールドで、**[!UICONTROL Choose File]**&#x200B;をクリックし、ネットワークまたはデバイス上のファイルを選択します。

   1. 「[!DNL Adobe]」および広告ネットワークのプライバシーポリシーの条件に同意することを示すチェックボックスをオンにします。

   1. **[!UICONTROL Upload File]**&#x200B;をクリックします。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!NOTE]
>
>広告ネットワークがオーディエンスの更新処理に時間がかかる場合があります。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて](audience-about.md)
>* [顧客マッチオーディエンスを [!DNL Google Ads]  オーディエンス  [!DNL Adobe] から](google-audience-from-adobe-audience.md)作成
>* [Adobe Campaignのメールリストから [!DNL Google Ads] 顧客マッチオーディエンスを作成](google-audience-from-campaign-email-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
