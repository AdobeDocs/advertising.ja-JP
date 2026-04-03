---
title: Adobe Campaignのメールリストから [!DNL Google Ads] 顧客マッチオーディエンスを作成
description: 既存のAdobe Campaign メールリストから [!DNL Google Ads]  カスタマッチオーディエンスを作成する方法を説明します。
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tEiqvHt1QzxhstsKGUsvKGgwm1JYIkv7mGr-Z8kPd0g
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# Adobe Campaignのメールリストから[!DNL Google Ads]の顧客マッチオーディエンスを作成する

顧客の一致のみ&#x200B;*[!DNL Google Ads]の対象となる* アカウント

アカウントリンクとワークフローを[!DNL Google Ads]に設定することで、Adobe Campaign内のメールリストから[!DNL Campaign]の顧客マッチオーディエンスを作成できます。

そのためには、[!DNL Campaign] インスタンスにアクセスし、必要なワークフローを含むXML ファイルにアクセスする必要があります。これには、Adobe アカウントチームから提供されます。 手順は、[!DNL Campaign]のバージョンによって異なる場合があります。 必要に応じて、Adobe アカウントチームが[!DNL Campaign]でのワークフローの設定を支援します。

1. Advertising Search、Social、およびCommerceが提供するSFTP アカウントの資格情報を取得します。

1. [!DNL Campaign]で、Advertising Search、Social、およびCommerceへのメールリストの配信を設定します。

   1. Search, Social, &amp; Commerceが提供するSFTP アカウントをリンクする[外部アカウント ](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html)を作成します。

      1. 左側のメニューから、**\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**&#x200B;に移動します。

      1. 「![ アカウントを作成](/help/search-social-commerce/assets/campaign-create-account.png " アカウントを作成")」をクリックします。

      1. アカウントのラベルを入力し、アカウントタイプとして「**[!UICONTROL SFTP]**」を選択します。

      1. [!DNL Adobe] SFTP サーバーのURLとポート番号、および広告主のフォルダー名、ユーザー名とパスワードを入力します。

      1. **[!UICONTROL Save]**&#x200B;をクリックします。

   1. [!DNL Campaign Client]で、電子メール データの送信に必要なワークフローを含むデータ パッケージをインストールします。

      1. メニューバーから、**[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**&#x200B;に移動します。

      1. **[!UICONTROL Install a package from a file]**&#x200B;を選択し、**[!UICONTROL Next]**&#x200B;をクリックします。

      1. デバイスまたはネットワーク上のデータパッケージファイル （`AMO_Workflow.xml`）を見つけて、**[!UICONTROL Next]**&#x200B;をクリックします。

      1. **[!UICONTROL Start]**&#x200B;をクリックし、ワークフローがインストールされるのを待ちます。

   1. インストールされているワークフローを編集して、データクエリのフィルターをオプションで編集し、新しいオーディエンス名と外部SFTP アカウントを特定します。

      1. **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]**&#x200B;に移動し、パッケージを開きます。

      1. （オプション）データのフィルターのいずれかを編集します。

         * ワークフローで、クエリアクティビティ（ForkTransition 1など）をダブルクリックします。

         * フィルター式を編集します。

         * **[!UICONTROL Finish]**&#x200B;をクリックします。

      1. セグメントに名前を付けます。

         * ワークフローで、アクティビティ **[!UICONTROL Data extraction (File)]**&#x200B;をダブルクリックします。

         * 「**[!UICONTROL Data extraction (File)]**」タブの&#x200B;**[!UICONTROL File name]** フィールドに、セグメント名を拡張子「`.added`」で入力します（PaidSubscribers.addedなど）。

           セグメント名が既に存在しない必要があります。 セグメント名では大文字と小文字が区別され、ASCII文字で構成する必要がありますが、アンダースコア（`_`）を含めることはできません。

           ただし、セグメントを特定の[!DNL Google Ad] アカウントに追加する場合は、セグメント名にアンダースコアと[!UICONTROL User SE Account ID]を付けます（ネットワークのアカウント IDではなく、[!DNL Google Ads] アカウントの検索、ソーシャル、およびCommerceのID）。

           `_<User SE Account ID>`

           例：Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >これは、ファイル名のアンダースコアを禁止するルールの例外です。

           それ以外の場合は、Search、Social、およびCommerceが広告主向けに同期しているすべての[!DNL Google Ads] アカウントにセグメントが追加されます。

         * オプションを&#x200B;**[!UICONTROL Generate an outbound transition]**&#x200B;に選択したままにします。

         * **[!UICONTROL Ok]**&#x200B;をクリックします。

      1. データを送信する外部アカウントを指定します。

         * ワークフローで、アクティビティ **[!UICONTROL File Transfer]**&#x200B;をダブルクリックします。

         * 「**[!UICONTROL File Transfer]**」タブの「**[!UICONTROL Remote server]**」セクションで、「**[!UICONTROL Use an external account]**」オプションを選択します。

         * **[!UICONTROL External account]** フィールドで、手順2で作成した外部アカウントのラベルを選択します。

         * **[!UICONTROL Server folder]** フィールドで、外部アカウントの[!UICONTROL Account] フィールドの値を選択します。

         * （オプション）「**[!UICONTROL Schedule]**」タブで、ファイル転送の別のスケジュールを指定します。

           デフォルトでは、ワークフローは00:00 （真夜中）に実行され、すべてのレコードが処理されます。 待ち時間を最小限に抑えるには、ワークフローを18:00までに実行するようにスケジュールします。

         * **[!UICONTROL Ok]**&#x200B;をクリックします。

Search, Social, &amp; Commerceは、30分ごとに（広告主のタイムゾーンのNN:30とNN:59で）ディレクトリをチェックし、見つかったファイルを別の場所に移動し、データからオーディエンスを自動的に作成し、22:00 （午後10時）にGoogleにプッシュします。 Search, Social, &amp; Commerceでは、30分ごとにメールリストの更新（追加と減算）を確認し続け、毎日22[!DNL Google Ads]に応じて:00のオーディエンスを更新します。

>[!NOTE]
>
>* 処理サイクル間で複数のバージョンのファイルをアップロードする場合は、最新のファイルが使用されます。
>
>* Search, Social, &amp; Commerceには、[!DNL Google Ads] オーディエンスの作成または編集に使用したメールリストの顧客データは保存されません。
>
>* [!DNL Google Ads]は、オーディエンスの更新を処理するのに時間がかかる場合があります。
>
>* 顧客の一致の仕組みと制限に関する[[!DNL Google Ads]  ドキュメント ](https://support.google.com/displayvideo/answer/9539301)を参照してください。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて](audience-about.md)
>* [顧客マッチオーディエンスを [!DNL Google Ads]  オーディエンス  [!DNL Adobe] から](google-audience-from-adobe-audience.md)作成
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
