---
title: （新しいUI）広告ネットワークアカウントの管理
description: 広告ネットワーク APIを介して同期された広告ネットワークの新しいUIで、アカウントの詳細を設定および管理する方法について説明します。
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 0%

---

# （新しいUI） API接続による広告ネットワークアカウントの管理

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta機能*

<!-- Move out info about Naver into a separate page -->

以下は、Search、Social、およびCommerceが広告ネットワークのAPIを使用して同期する広告ネットワークアカウントを管理する手順です。

<!-- Move out info about Naver into a separate page -->

各広告ネットワークで使用できる機能について詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## 広告ネットワークアカウントの詳細の作成 {#create-account}

アカウントの同期を有効にするには、アカウントのアクセス資格情報と追跡オプションを含み、ステータスが&#x200B;*enabled*&#x200B;の対応するアカウントレコードを作成する必要があります。

>[!NOTE]
>
>広告ネットワークで実際のアカウントを作成するには、広告ネットワークのweb サイトに移動します。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. **[!UICONTROL Create Account]**&#x200B;をクリックします。

1. 広告ネットワークの名前をクリックし、**[!UICONTROL Next]**&#x200B;をクリックします。

1. （広告主の資格情報を使用して、広告ネットワークにログインします（[!DNL Yandex]を除くすべての広告ネットワーク）。 「このアカウントのアカウントトラッキング」オプションを選択します。 次に、右上の「**[!UICONTROL Next]**」をクリックします。

1. [&#x200B; アカウント設定](#account-settings-api)を指定します。

   1. 「**[!UICONTROL Select Accounts]**」タブで、一般的なアカウント設定を指定します。 [!DNL Yandex] アカウントの場合は、アカウントの資格情報を指定します。

   1. 「**[!UICONTROL Setup Tracking]**」タブをクリックし、トラッキング設定を入力します。

   1. （[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)を持つ広告主）「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、追跡およびレポートのキャンペーンアクティビティに使用するすべての[!DNL Analytics] レポートスイートを選択します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

   アカウント内のすべてのキャンペーンの最近のコストとクリックデータは、検索、ソーシャル、Commerceの時間単位で更新されます。 デフォルトでは、広告ネットワークに応じて、過去5～10日間データを利用できます。 ただし、必要に応じて、プロジェクト立ち上げチームは過去60日間までのデータを取得できます。

## 広告ネットワークアカウントの詳細を編集 {#edit-account}

アカウント設定を再認証して接続を更新したり、権限を更新したり、アカウントのアクティビティを有効または無効にしたり、アカウント全体のデフォルトのトラッキングパラメーターを変更したり、トラッキングとレポートに使用する[!DNL Analytics] レポートスイートを変更したりするには、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークのweb サイトに移動します。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [&#x200B; アカウント設定](#account-settings-api)を編集します。

   1. （オプション）「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （オプション）「**[!UICONTROL Setup Tracking]**」タブをクリックし、トラッキング設定を編集します。

   1. （オプション、[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)を持つ広告主）「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、[!DNL Analytics] レポートスイートを編集して、キャンペーンアクティビティの追跡とレポートに使用します。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. **[!UICONTROL Save]**&#x200B;をクリックします。

   >[!NOTE]
   >
   >Search, Social, &amp; Commerceは、新しいアカウントデータを広告ネットワーク上のアカウントデータと同期させる必要があります。 Search, Social, &amp; Commerceによって広告ネットワーク上の変化が検出されると、1日に1回、またはそれ以上の頻度で自動的に行われます。

## 広告ネットワークアカウントの再認証 {#reauthenticate}

アカウントの広告ネットワーク接続を更新したり、権限を更新したりするには、アカウントを再認証します。

1. （同じブラウザーアプリケーションで同じ広告ネットワークの別のアカウントにログインしている場合）広告主以外のアカウントからログアウトします。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. 「**[!UICONTROL Account Details]**」タブで「**[!UICONTROL Re authenticate]**」をクリックし、広告主の資格情報を使用して広告ネットワークにログインします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

広告ネットワークアカウントを有効にすると、Search, Social, &amp; Commerceは、キャンペーンデータをアカウントと（サポートされている場合）同期し、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。 広告ネットワークアカウントを無効にすると、Search、Social、およびCommerceは、アカウント上のすべてのアクティビティを停止します。 アカウントがアクティブな間に収集されたデータは引き続き保存されますが、キャンペーン管理ビューとレポートには、アカウントが無効になっている期間のデータは含まれません。 後でアカウントを再度有効にして、アカウントのアクティビティを再開できます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （[!UICONTROL Accounts] ビューから）:

      * （アカウントを有効にするには） アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Activate]**」をクリックします。

      * （アカウントを無効にするには） アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Pause]**」をクリックします。

   * （アカウント設定から）:

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

         * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. 「**[!UICONTROL Account Details]**」タブで「**[!UICONTROL Account enabled]**」をオフにします。

      1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 広告ネットワークアカウント設定 {#account-settings-api}

アカウント設定は広告ネットワークによって異なります。 以下のすべての設定が表示されない場合があります。

<!--
 When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details] タブ

**[!UICONTROL Account Name]:**&#x200B;検索、ソーシャル、およびCommerce内のアカウントに表示される名前。

>[!NOTE]
>
>Search、Social、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobe アカウントチームにマッピングを更新するように依頼します。

**[!DNL [Ad Network] アカウント &#x200B;]:** （アカウント作成中に表示）同期する広告ネットワークアカウント。

**[ログインの詳細]:** （Yandex アカウントのみ）使用するアカウント資格情報：

* **[!UICONTROL Login]:** アカウントへのAPI アクセスを有効にするログイン名またはID。

* **[!UICONTROL Password]:** アカウントのパスワード。

* **[!UICONTROL Access Key]:**&#x200B;使用する開発者アカウントのアクセス キー。

* **[!UICONTROL Application ID]:** アカウントに使用する開発者トークン。 同じトークンがすべての[!DNL Yandex] アカウントに使用されます。

* **[!UICONTROL Purse Campaign ID]:** （[!DNL Yandex] アカウント （共有アカウント設定が無効になっているアカウントのみ、オプション）アカウント内のすべての広告キャンペーンの支払いに使用されるキャンペーンの数値ID。

* **[!UICONTROL Finance Token]:** （[!DNL Yandex] アカウントで、共有アカウント設定が無効になっている場合のみ、オプション）金融関連のAPI呼び出しに使用する開発者トークン。例えば、ポートフォリオの最適化に必要に応じて、広告主のキャンペーン間でウォレットから資金を再配分する場合などに使用します。

**[!UICONTROL Network Account ID]:** （[!DNL Yandex]を除くすべての広告ネットワーク広告ネットワークによって割り当てられたアカウント ID。

>[!NOTE]
>
>Ad network manager アカウントは、ここではサポートされていません。 [!DNL Microsoft Advertising]のマネージャーアカウントを特定するには、「マスターアカウント ID」フィールドまたは「MCC アカウント」フィールドをそれぞれ使用します。 [&#x200B; マネージャーアカウント &#x200B;](/help/search-social-commerce/admin/manager-accounts.md)の資格情報を設定するには、[!UICONTROL Admin] \> [!UICONTROL Manager Accounts]に移動します。 [!DNL Google Ads] 

**[!UICONTROL Currency]:** （読み取り専用）アカウントに使用される通貨の略語。 この値は、レコードを保存すると、広告ネットワーク上のアカウントに設定された通貨で自動的に入力されます。

**[!UICONTROL Time Zone]:**&#x200B;広告主のタイムゾーン。 この値は、レコードを保存すると、広告主のSearch, Social, &amp; Commerce アカウント用に設定されたタイムゾーンで自動的に入力されます。

**[!UICONTROL Login]:** （読み取り専用） アカウントへのログインに使用したユーザーアカウント。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social, &amp; Commerceは、キャンペーンデータをアカウントと（サポートされている場合）同期し、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。

## [!UICONTROL Setup Tracking] タブ

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** トラッキングを有効にするかどうかをAdobe Advertising コンバージョントラッキングサービスを使用します。 この方法では、一意のクリックトラッキング IDを生成し、ユーザーをトラッキング目的でAdobe Advertising サーバーにリダイレクトしてから、クライアントのランディングページに送信します。 このメソッドには、オプションでカスタマイズできるデフォルトのトラッキングオプションがあり、各URLに追加するパラメーターを指定することもできます。

この機能を有効にするには、**[トラッキングを有効にする]**&#x200B;をオンにします。

>[!NOTE]
>
>* この設定を変更した場合は、アカウントのトラッキング URLを再生成する必要があります。
>* キャンペーンレベルのトラッキングオプションは、アカウントレベルの設定を上書きします。

**[!UICONTROL Tracking Type]:** （Search, Social, &amp; Commerce トラッキングが有効になっている場合）エンドユーザーを最終URLまたは宛先URLにリダイレクトする方法。 選択したオプションは、アカウントまたはキャンペーンのすべての入札単位に適用されます。 デフォルトのアカウントレベル設定は広告主のトラッキング設定から継承され、デフォルトのキャンペーンレベル設定はアカウント設定から継承されます。

* *[!UICONTROL Standard]:* エンドユーザーを指定されたURLにリダイレクトするだけです。

* *[!UICONTROL Token]:* エンドユーザーをURLにリダイレクトし、クリック用の検索、ソーシャル、およびCommerce ID （`ef_id`）をクエリ文字列パラメーターとして記録します。このパラメーターはトークンとして使用されます。 オフラインのトランザクションをレポートする場合、Search、Social、およびCommerceでAdobe Analyticsとデータを交換する場合、または[!DNL Apple Safari] ブラウザー内で発生するすべてのコンバージョンをトラッキングする場合は、このオプションを選択します。

>[!NOTE]
>
>* [!UICONTROL Standard]から[!UICONTROL Token]に切り替える場合、またはその逆の場合は、アカウントのトラッキング URLを再生成する必要があります。
>* アカウントレベルの設定は、キャンペーンレベルで上書きできます。

**[!UICONTROL Auto Update]:** （検索、ソーシャル、およびCommerce トラッキングが有効になっている場合）は、ブラウザーとサーバー間で互換性を保つためにトラッキング URLを標準化します。 Search, Social, &amp; Commerceは、次の同期中に、次の情報を自動的にアドネットワークにアップロードします。（a） トラッキングテンプレートのSearch, Social, &amp; Commerce トラッキングパラメーターと、最終的なURLに追加された同じパラメーター、または（b） Search, Social, &amp; Commerce トラッキングコードが埋め込まれた新しい宛先URL。 [Adobe AdvertisingとAdobe Analyticsの統合](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)およびサーバーサイド AMO ID （s_kwcid）設定を持つ広告主の場合、アップロードには[!DNL Google Ads] アカウントと[!DNL Microsoft Advertising] アカウントの[AMO ID パラメーター](/help/integrations/analytics/ids.md#amo-id)も含まれます。 デフォルトのアカウントレベル設定は、広告主のトラッキング設定から継承されます。 アカウントレベルの設定は、キャンペーンレベルで上書きできます。

トラッキング URLは、同期されていないエンティティ（つまり、追加された新しいエンティティとプロパティが変更された既存のエンティティ）に対してのみ毎日更新されます。 したがって、既存の広告主/アカウント/キャンペーンに対してこの設定を「無効」から「有効」に変更した場合、既に同期している既存のエンティティのトラッキング URLは更新されません。 既存の同期中のエンティティのURLにトラッキングを追加するには、Adobe アカウントチームに連絡し、1回限りの手動同期プロセスをリクエストしてください。 自動アップロードプロセスは、今後の変更を処理します。

**[!UICONTROL URL Encoding]:** （Search, Social, &amp; Commerce トラッキングが有効になっている場合、リンク先URLを持つアカウントのみ） エンドユーザーのアドレスバー内のベース URLをエンコードします（`=`ではなく`%3D`など）。

**[!UICONTROL Tracking Level]:** （Search, Social, &amp; Commerce トラッキングが有効になっている場合、アカウントレベルとキャンペーンレベルで利用可能です。並列トラッキングが有効になっている広告ネットワークには適用されません） クリックと収益をトラッキングするレベルは、リダイレクトを追加し（関連する場合）、関連するURLにパラメーターを追加することで追跡されます。

* *[!UICONTROL Keyword]:* キーワードレベルでのみデータを追跡します。 [!DNL Yandex]では利用できません。

* *[!UICONTROL Ad]:*&#x200B;広告レベルでのみデータを追跡します。 [!DNL Naver]では利用できません。

* *[!UICONTROL Keyword and Ad]:* キーワードレベルと広告レベルの両方でデータを追跡します。 [!DNL Naver]および[!DNL Yandex]では利用できません。

**[!UICONTROL Landing Page Suffix]** （[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的なURLの末尾に追加するパラメーター。企業が追跡する必要があるすべてのパラメーターを含めます。

例：`param1=value1&param2=value2`

Adobe Advertising クリック トラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック ID （[!DNL Microsoft Advertising]の`msclkid`; Googleの`gclid`）を含める必要があります。 Adobe Analyticsとの統合を持つアカウントでは、AMO ID パラメーター（`s_kwcid`で始まる）を使用する必要があります。 アカウントにサーバーサイド AMO ID実装がある場合、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、ここで手動で追加する必要があります。  [!DNL Google Ads][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-google.md)の[必要なサフィックス形式と [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)の必要なサフィックス形式を参照してください。

>[!NOTE]
>
>* このフィールドは、[!UICONTROL Auto Update] トラッキング設定で更新されません。
>* 下位レベルの最終URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

**アカウントトラッキング URL**: （[!DNL Google Ads]、[!DNL LY Ads]、および[!DNL Microsoft Advertising] アカウントのみ。オプション）アカウントのデフォルトのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最後のページ URLもパラメーターに埋め込みます。 例：リダイレクトを含める`{lpurl}?source={network}&id=5`または`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`。

* 最終的なURLを埋め込むには：

   * （[!DNL Google Ads]および[!DNL Microsoft Advertising]のみ）トラッキングテンプレートの最終的なURLを示すパラメーターのリストについては、[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/6305348)の「使用可能な[!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ」パラメーター（[!DNL Microsoft Advertising]のみ） [[!DNL Microsoft Advertising]  ドキュメント &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799)または（[!DNL Google Ads]のみ）を参照してください。

   * （[!DNL LY Ads]のみ） パラメーター`!{lpurl}`を使用して、ランディングページ URLを示します。

* 必要に応じて、URL パラメーターと、キャンペーン用に定義された任意のカスタムパラメーターを、アンパサンド（&amp;）で区切って含めることができます（`{lpurl}?matchtype={matchtype}&device={device}`）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

* キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合、レコードを保存すると、Search、Social、およびCommerceに独自のリダイレクトコードとトラッキングコードが自動的にプレフィックスされます。

>[!NOTE]
>
>* [!DNL Google Ads]の場合、並列追跡を有効にするソースからのクリックに代わらないマクロの使用を避けてください。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームは、カスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。
>* 最も詳細なレベルのトラッキングテンプレートは、より高いレベルのすべての値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンク、またはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 承認のために広告を再送信することなく、アカウントレベル、キャンペーンレベル、広告グループレベルでトラッキングテンプレートを更新できます。

## [!UICONTROL Setup Analytics] タブ

**[!UICONTROL Adobe Analytics Report Suite]:** （広告主と[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)、オプション） Search, Social, &amp; Commerceが広告ネットワークから収集したデータを送信する1つ以上のAnalytics レポートスイート（エンティティの分類やアカウントのクリックデータを含む）。 この機能は、サポートされている広告ネットワークでのみ使用できます。

レポートスイートにデータを表示するには、（a）アカウントにサーバーサイド AMO ID機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、広告主の[!DNL Analytics] アカウントは、Search、Social、およびCommerceからデータを受信するように設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントについて](../ad-network-account-about.md)
>* [&#x200B; マーチャント センターのアカウントの管理](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [&#x200B; アカウント  [!DNL Google Ads] のs_kwcid トラッキングコードを更新します](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
