---
title: 顧客データリストを使用したカスタマーマッチオーディエンスの管理
description: を作成および編集する方法を説明します [!DNL Google Ads] および [!DNL Microsoft Advertising] 顧客データリストの顧客一致オーディエンス。
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] および [!DNL Microsoft Advertising] 顧客データリストを使用した顧客マッチオーディエンス

次を作成できます [!DNL Google Ads] および [!DNL Microsoft Advertising] 顧客データリストの顧客一致オーディエンス。 また、以下のいずれかを更新できます [!DNL Google Ads] または [!DNL Microsoft Advertising] 次を除く顧客一致オーディエンス [!DNL Google Ads] から作成されたオーディエンス [!DNL Adobe] オーディエンス。

## 顧客データリストからの顧客一致オーディエンスの作成

*[!DNL Google Ads]および [!DNL Microsoft Advertising] 顧客一致のみの対象となるアカウント*

以下を作成できます [!DNL Google Ads] または [!DNL Microsoft Advertising] 顧客関係管理（CRM）システムから生成したデータファイルに含まれる顧客データベースのリスト。

の場合 [!DNL Microsoft Advertising] アカウントの場合、このファイルにはメールアドレスを含めることができます。 の場合 [!DNL Google Ads] アカウント。ファイルには、メールアドレス、住所、電話番号、ユーザー ID、CRM のモバイルデバイス ID が含まれます。

>[!NOTE]
>
>検索、ソーシャル、Commerceには、アップロードまたはアップロード元の顧客データは格納されません [!DNL Adobe] の作成または編集に使用するセグメント [!DNL Google Ads] または [!DNL Microsoft Advertising] オーディエンス。

1. 顧客データを含んだファイルを必要な形式で生成します。

   姓名、メールアドレスおよび電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> の場合 [!DNL Google Ads] オーディエンス。詳しくは、 [!DNL Google Ads] のドキュメント[ハッシュ化されたデータのアップロードに関する形式ガイドライン](https://support.google.com/google-ads/answer/7476159)」を参照して、許可された連絡先情報のフィールドと要件を確認してください。 の場合 [!DNL Microsoft Advertising] オーディエンス。詳しくは、 [!DNL Microsoft Advertising] のドキュメント [顧客一致リストの準備]（https://help.ads.microsoft.com/#apex/ads/en/56921. オプションで、 [!DNL Microsoft Excel] 連絡先情報のテンプレート。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. データ テーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. オーディエンス情報を指定します。

   1. が含まれる [!UICONTROL Data Source] メニュー、選択 **[!UICONTROL Customer List]**.

   1. を入力 **[!UICONTROL Audience Name]**.

   1. ファイルをアップロードします。

      1. 「」を選択します [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*、または *[!UICONTROL Mobile Device IDs]*.

         「ユーザー ID」オプションは、次の場合にのみ使用できます [!DNL Google Ads] 米国の広告主で～を選んだ人 [ユーザー ID セグメント](https://support.google.com/google-ads/answer/9199250)

      1. （モバイルデバイス ID リストのみ）を選択します **[!UICONTROL OS Type]** （*[!UICONTROL Android™]* または *[!UICONTROL iOS]*）、を入力します。 **[!UICONTROL App ID]**.

         アプリ ID は、アプリケーションがGoogle PlayまたはApple App Storeに接続できるようにするためにモバイルオペレーティングシステムで使用される一意の ID です。

         * （[!DNL Android™] apps） [!DNL Android™] 内のパッケージ名 [!DNL Google Play]、「」で識別`id=<package_name>`.」と入力します。

           例えば、https://play.google.com/store/apps/details?id=com.example.gameでは、パッケージ名は com.example.game です。

         * （[!DNL iOS] apps）内のアプリケーション ID [!DNL iTunes App Store]、「」で識別`<idNNNNNNNNN>`」に設定する必要があります。 次でも利用できます [!DNL iOS Developer Console].

           例えば、https://itunes.apple.com/us/app/id284882215では、ID は id284882215 です。

         開発チームが以下にアクセスできます [!UICONTROL App ID] （該当するプラットフォーム用）。

      1. が含まれる [!UICONTROL Select File] フィールド、クリック **[!UICONTROL Choose File]** そして、ネットワークまたはデバイス上のファイルを選択します。

      1. の条件に同意することを示すチェックボックスを選択します [!DNL Adobe] および広告ネットワークプライバシーポリシー。

      1. （作成する広告主） [!DNL Google Ads] 欧州経済領域（EEA）または英国（UK）でビジネスを行うオーディエンス（任意） EEA および英国のユーザーから、広告目的でデータをアップロードすることに同意を収集した場合は、の横にあるチェックボックスを選択します **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] は、同意ステータスが未指定の EEA および英国のユーザーに関するデータを無視します。 これにより、データの不一致とパフォーマンスの問題が発生する可能性があります。

      1. クリック **[!UICONTROL Upload File]**.

   1. 次の数を指定 **[!UICONTROL Membership Days]**：ユーザーの cookie がオーディエンスに残る日数です。

   広告がユーザーに関連すると予想される時間の長さを使用します。 値を入力しない限り、顧客リストに有効期限はありません。

1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>* 広告ネットワークは、ファイルを処理するのに最大 24 時間かかる場合があります。
>* 参照： [[!DNL Google Ads] カスタマーマッチの仕組みと制限に関するドキュメント](https://support.google.com/displayvideo/answer/9539301).

## 顧客データリストを使用した顧客一致オーディエンスの編集

以下のいずれかを更新できます [!DNL Google Ads] または [!DNL Microsoft Advertising] 次を除く顧客一致オーディエンス [!DNL Google Ads] から作成されたオーディエンス [!DNL Adobe] オーディエンス。 データをアップロードして、オーディエンスの既存のデータを追加、削除または置き換えることができます。

データは、元の顧客リストと同じタイプ（特定のモバイルオペレーティングシステム上の特定のアプリのメールアドレス、住所、電話番号、ユーザー ID、モバイルデバイス ID）である必要があります。

1. 既存のデータタイプに必要な形式の顧客データを含んだファイルを生成します。

姓名、メールアドレスおよび電話番号は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> の場合 [!DNL Google Ads] オーディエンス。詳しくは、 [!DNL Google Ads] のドキュメント[ハッシュ化されたデータのアップロードに関する形式ガイドライン](https://support.google.com/google-ads/answer/7476159)」を参照して、許可された連絡先情報のフィールドと要件を確認してください。 の場合 [!DNL Microsoft Advertising] オーディエンス。詳しくは、 [!DNL Microsoft Advertising] のドキュメント [顧客一致リストの準備]（https://help.ads.microsoft.com/#apex/ads/en/56921. オプションで、 [!DNL Microsoft Excel] 連絡先情報のテンプレート。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 編集するオーディエンスの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png).

1. アクションを選択します。 *[!UICONTROL Add]* （既存のデータが存在する場合を除き、アップロードしたデータを既存のデータに追加します）。 *[!UICONTROL Delete]* （既存のデータが存在する場合に、そのデータからアップロードされたデータを削除する）、 *[!UICONTROL Replace]* （既存のデータをすべて削除し、アップロードしたデータに置き換える場合）。

1. ファイルをアップロードします。

   1. が含まれる [!UICONTROL Select File] フィールド、クリック **[!UICONTROL Choose File]** そして、ネットワークまたはデバイス上のファイルを選択します。

   1. の条件に同意することを示すチェックボックスを選択します [!DNL Adobe] および広告ネットワークプライバシーポリシー。

   1. クリック **[!UICONTROL Upload File]**.

1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>広告ネットワークでは、オーディエンスに対する更新を処理するのに時間がかかる場合があります。

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [作成 [!DNL Google Ads] のカスタマーマッチオーディエンス [!DNL Adobe] オーディエンス](google-audience-from-adobe-audience.md)
>* [を作成 [!DNL Google Ads] Adobe Campaign メールリストからのカスタマーマッチオーディエンス](google-audience-from-campaign-email-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
