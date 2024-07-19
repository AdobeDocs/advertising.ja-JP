---
title: Adobe Campaign [!DNL Google Ads]  メールリストからカスタマーマッチオーディエンスを作成
description: 既存のAdobe Campaignのメールリストから  [!DNL Google Ads]  カスタマーマッチオーディエンスを作成する方法を説明します。
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Adobe Campaignのメールリストから [!DNL Google Ads] カスタマーマッチオーディエンスを作成

顧客一致の対象となるアカウントの *[!DNL Google Ads]定*

[!DNL Campaign] でアカウントリンクとワークフローを設定することで、Adobe Campaign内のメールリストから [!DNL Google Ads] しいカスタマーマッチオーディエンスを作成できます。

これを行うには、[!DNL Campaign] インスタンスにアクセスし、必要なワークフローを含む XML ファイルにアクセスする必要があります。このワークフローはAdobeアカウントチームから提供されます。 手順は、[!DNL Campaign] のバージョンによって異なる場合があります。 必要に応じて、Adobeアカウントチームが [!DNL Campaign] でのワークフローの設定を支援します。

1. Advertising検索、ソーシャル、Commerce提供の SFTP アカウントの資格情報を取得します。

1. [!DNL Campaign] で、Advertising検索、ソーシャル、Commerceへのメールリストの配信を設定します。

   1. [ 外部アカウント ](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) を作成して、検索、ソーシャル、Commerceで提供される SFTP アカウントにリンクします。

      1. 左側のメニューから **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]** に移動します。

      1. ![ アカウントを作成 ](/help/search-social-commerce/assets/campaign-create-account.png " アカウントを作成 ") をクリックします。

      1. 勘定科目のラベルを入力し、勘定科目のタイプとして「**[!UICONTROL SFTP]**」を選択します。

      1. [!DNL Adobe] SFTP サーバーの URL とポート番号、および広告主のフォルダー名、ユーザー名、パスワードを入力します。

      1. 「**[!UICONTROL Save]**」をクリックします。

   1. [!DNL Campaign Client] で、メールデータの送信に必要なワークフローを含むデータパッケージをインストールします。

      1. メニューバーで、**[!UICONTROL Tools]/ [!UICONTROL Advanced] /[!UICONTROL Import Package]** に移動します。

      1. 「**[!UICONTROL Install a package from a file]**」を選択し、「**[!UICONTROL Next]**」をクリックします。

      1. デバイスまたはネットワーク上のデータ パッケージ ファイル （`AMO_Workflow.xml`）を見つけ、[**[!UICONTROL Next]**] をクリックします。

      1. 「**[!UICONTROL Start]**」をクリックして、ワークフローがインストールされるのを待ちます。

   1. インストール済みのワークフローを編集し、オプションでデータクエリのフィルターを編集し、新しいオーディエンス名と外部 SFTP アカウントを識別します。

      1. **[!UICONTROL Administration]/[!UICONTROL Configuration]/[!UICONTROL Package management]/[!UICONTROL Installed packages]** に移動し、パッケージを開きます。

      1. （任意）データのフィルターを編集します。

         * ワークフローで、クエリ アクティビティ（ForkTransition 1 など）をダブルクリックします。

         * フィルター式を編集します。

         * 「**[!UICONTROL Finish]**」をクリックします。

      1. セグメントに次の名前を付けます。

         * ワークフローで、アクティビティ **[!UICONTROL Data extraction (File)]** をダブルクリックします。

         * 「**[!UICONTROL Data extraction (File)]**」タブの「**[!UICONTROL File name]**」フィールドに、拡張子が「`.added`」のセグメント名（PaidSubscribers.added など）を入力します。

           セグメント名は、既に存在してはいけません。 セグメント名では大文字と小文字が区別され、ASCII 文字で構成する必要がありますが、アンダースコアを含めることはできません（`_`）。

           ただし、セグメントを特定の [!DNL Google Ad] アカウントに追加する場合は、セグメント名にアンダースコアと [!UICONTROL User SE Account ID] （ネットワークのアカウント ID ではなく、[!DNL Google Ads] アカウントの検索、ソーシャル、Commerceの各 ID）を付加します。

           `_<User SE Account ID>`

           例：Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >これは、ファイル名にアンダースコアを使用できないというルールの例外です。

           そうでない場合は、広告主に対して検索、ソーシャル、Commerceで同期しているすべての [!DNL Google Ads] アカウントにセグメントが追加されます。

         * このオプションは選択し **[!UICONTROL Generate an outbound transition]** ままにします。

         * 「**[!UICONTROL Ok]**」をクリックします。

      1. データの送信先の外部アカウントを指定してください：

         * ワークフローで、アクティビティ **[!UICONTROL File Transfer]** をダブルクリックします。

         * 「**[!UICONTROL File Transfer]**」タブの「**[!UICONTROL Remote server]**」セクションで、**[!UICONTROL Use an external account]** すオプションを選択します。

         * 「**[!UICONTROL External account]**」フィールドで、手順 2 で作成した外部アカウントのラベルを選択します。

         * 「**[!UICONTROL Server folder]**」フィールドで、外部アカウントの「[!UICONTROL Account]」フィールドの値を選択します。

         * （オプション）「**[!UICONTROL Schedule]**」タブで、ファイル転送の別のスケジュールを指定します。

           デフォルトでは、ワークフローは 00:00 （午前 0 時）に実行され、すべてのレコードが処理されます。 待ち時間を最小限に抑えるには、ワークフローを 18:00 までに実行するようにスケジュールします。

         * 「**[!UICONTROL Ok]**」をクリックします。

検索、ソーシャル、Commerceは、30 分ごとに（広告主のタイムゾーンの NN:30 と NN:59 で） ディレクトリをチェックして、見つかったファイルを別の場所に移動し、データからオーディエンスを自動的に作成し、22:00 （午後 10 時）にGoogleにプッシュします。 検索、ソーシャル、Commerceでは、引き続き 30 分ごとにメールリストの更新（加算と減算）をチェックし、それに応じて毎日 22:00 に [!DNL Google Ads] でオーディエンスを更新します。

>[!NOTE]
>
>* 処理サイクルの間にファイルの複数のバージョンをアップロードした場合は、最新のファイルが使用されます。
>
>* 検索、ソーシャル、Commerceには、[!DNL Google Ads] ーザーオーディエンスの作成や編集に使用されるメールリストの顧客データは格納されません。
>
>* オ [!DNL Google Ads] ディエンスに対する更新の処理には時間がかかる場合があります。
>
>* [[!DNL Google Ads]  カスタマーマッチの仕組みと制限事項に関するドキュメント ](https://support.google.com/displayvideo/answer/9539301) を参照してください。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて ](audience-about.md)
>* [ オーディエ  [!DNL Google Ads]  スからの顧客一致オーディエ  [!DNL Adobe]  スの作成 ](google-audience-from-adobe-audience.md)
>* [ 顧客データリストを使用したカスタマーマッチオーディエンスの管理 ](audience-from-customer-data-list.md)
>* [ 動的リマーケティングオーディエンスの管理 ](audience-dynamic-remarketing-manage.md)
