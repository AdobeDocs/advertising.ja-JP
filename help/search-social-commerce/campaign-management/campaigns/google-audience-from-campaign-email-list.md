---
title: の作成 [!DNL Google Ads] Adobe Campaign電子メールリストからの顧客一致オーディエンス
description: を作成する方法を学ぶ [!DNL Google Ads] 既存のAdobe Campaign電子メールリストの顧客一致オーディエンス。
exl-id: 967580fc-52c3-42f5-8d60-18cb83bc714a
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# の作成 [!DNL Google Ads] Adobe Campaign電子メールリストからの顧客一致オーディエンス

*[!DNL Google Ads]カスタマーマッチの条件を満たすアカウント*

次の項目を作成できます。 [!DNL Google Ads] Adobe Campaign内の電子メールリストからの顧客一致オーディエンス ( [!DNL Campaign].

これをおこなうには、 [!DNL Campaign] インスタンスと、必要なワークフローを含む XML ファイル (Adobeアカウントチームから提供される )。 手順は、 [!DNL Campaign]. 必要に応じて、Adobeアカウントチームが [!DNL Campaign].

1. 広告検索、ソーシャルおよびコマースで指定された SFTP アカウントの資格情報を取得します。

1. In [!DNL Campaign]、Advertising Search、Social、および Commerce への電子メールリストの配信を設定します。

   1. の作成 [外部アカウント](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) Search、Social および Commerce が提供する SFTP アカウントをリンクするには：

      1. 左のメニューから、に移動します。 **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. クリック ![アカウントを作成](/help/search-social-commerce/assets/campaign-create-account.png "アカウントを作成").

      1. アカウントのラベルを入力し、「 」を選択します。 **[!UICONTROL SFTP]** をアカウントタイプとして設定します。

      1. の URL とポート番号を入力します。 [!DNL Adobe] SFTP サーバーと、広告主のフォルダー名、ユーザー名、パスワード。

      1. クリック **[!UICONTROL Save]**.

   1. In [!DNL Campaign Client]、電子メールデータの送信に必要なワークフローを含むデータパッケージをインストールします。

      1. メニューバーから、に移動します。 **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. 選択 **[!UICONTROL Install a package from a file]**&#x200B;をクリックし、 **[!UICONTROL Next]**.

      1. データパッケージファイル (`AMO_Workflow.xml`) をクリックし、 **[!UICONTROL Next]**.

      1. クリック **[!UICONTROL Start]** ワークフローがインストールされるまで待ちます。

   1. インストール済みのワークフローを編集し、オプションでデータクエリのフィルターを編集し、新しいオーディエンス名と外部 SFTP アカウントを特定します。

      1. に移動します。 **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** パッケージを開きます。

      1. （オプション）データの次のいずれかのフィルターを編集します。

         * ワークフローで、クエリアクティビティ（ ForkTransition 1 など）をダブルクリックします。

         * フィルター式を編集します。

         * クリック **[!UICONTROL Finish]**.

      1. セグメントに次の名前を付けます。

         * ワークフローで、「 」アクティビティをダブルクリックします。 **[!UICONTROL Data extraction (File)]**.

         * をに設定します。 **[!UICONTROL Data extraction (File)]** タブ、 **[!UICONTROL File name]** 「 」フィールドに、拡張子「 」を持つセグメント名を入力します。`.added`&quot; （PaidSubscribers.added など）

           セグメント名が存在していない必要があります。 セグメント名では大文字と小文字が区別されます。また、ASCII 文字で構成する必要がありますが、アンダースコア (`_`) をクリックします。

           ただし、特定の [!DNL Google Ad] アカウントを作成し、セグメント名にアンダースコアと [!UICONTROL User SE Account ID] ( 検索、Social および Commerce の ID は、 [!DNL Google Ads] アカウント（ネットワークのアカウント ID ではなく）:

           `_<User SE Account ID>`

           例： Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >これは、ファイル名でアンダースコアを禁止するルールの例外です。

           それ以外の場合、セグメントはすべての [!DNL Google Ads] 広告主に対して検索、ソーシャル、コマースを同期するアカウント。

         * オプションは次のままにします。 **[!UICONTROL Generate an outbound transition]** 選択済み

         * クリック **[!UICONTROL Ok]**.

      1. データの送信先の外部アカウントを指定します。

         * ワークフローで、「 」アクティビティをダブルクリックします。 **[!UICONTROL File Transfer]**.

         * をに設定します。 **[!UICONTROL File Transfer]** タブ、 **[!UICONTROL Remote server]** セクションで、次のオプションを選択します。 **[!UICONTROL Use an external account]**.

         * Adobe Analytics の **[!UICONTROL External account]** 「 」フィールドで、手順 2 で作成した外部アカウントのラベルを選択します。

         * Adobe Analytics の **[!UICONTROL Server folder]** フィールドで、 [!UICONTROL Account] 外部アカウントのフィールド。

         * （オプション） **[!UICONTROL Schedule]** タブで、別のファイル転送スケジュールを指定します。

           デフォルトでは、ワークフローは 0 時（午前 0 時）に実行され、すべてのレコードが処理されます。 待ち時間を最小限に抑えるには、ワークフローの実行スケジュールを 18:00 以下に設定します。

         * クリック **[!UICONTROL Ok]**.

Social、Commerce は、30 分ごとにディレクトリをチェックし（広告主のタイムゾーンの NN:30 と NN:59）、見つけたファイルを別の場所に移動し、データからオーディエンスを自動的に作成し、22:00（午後 10 時）にGoogleにプッシュします。 検索、ソーシャル、コマースは、30 分ごとに電子メールリストの更新（追加と引き算）を引き続き確認し、 [!DNL Google Ads] 毎日 22:00 になります。

>[!NOTE]
>
>* 処理サイクルの間に 1 つのファイルの複数のバージョンをアップロードする場合は、最新のファイルが使用されます。
>
>* 検索、ソーシャル、コマースでは、電子メールリストの顧客データは保存されず、 [!DNL Google Ads] オーディエンス。
>
>* [!DNL Google Ads] オーディエンスの更新を処理するのに時間がかかる場合があります。
>
>* 詳しくは、 [[!DNL Google Ads] カスタマーマッチの仕組みと制限に関するドキュメント](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
