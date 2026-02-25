---
title: （新しい UI）広告ネットワークアカウントの管理
description: 広告ネットワーク API を介して同期された広告ネットワークの新しい UI でアカウントの詳細を設定および管理する方法について説明します。
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# （新しい UI） API 接続を使用した広告ネットワークアカウントの管理

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta機能*

<!-- Move out info about Naver into a separate page -->

次に、広告ネットワークの API を使用して検索、ソーシャル、Commerceで同期する広告ネットワークアカウントの管理手順を示します。

<!-- Move out info about Naver into a separate page -->

各広告ネットワークで使用できる機能について詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## 広告ネットワークアカウントの詳細を作成 {#create-account}

アカウントの同期を有効にするには、対応するアカウントレコードを作成する必要があります。これには、アカウントのアクセス資格情報とトラッキングオプションが含まれ、ステータスが *有効* になっている必要があります。

>[!NOTE]
>
>広告ネットワーク上に実際のアカウントを作成するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 「**[!UICONTROL Create Account]**」をクリックします。

1. 広告ネットワークの名前をクリックし、[**[!UICONTROL Next]**] をクリックします。

1. （[!DNL Yandex] 以外のすべての広告ネットワーク）広告主の資格情報を使用して広告ネットワークにログインします。 「このアカウントのアカウントトラッキング」オプションを選択します。 次に、右上のをクリック **[!UICONTROL Next]** ます。

1. [&#x200B; アカウント設定 &#x200B;](#account-settings-api) を指定します。

   1. 「**[!UICONTROL Select Accounts]**」タブで、一般的なアカウント設定を指定します。 [!DNL Yandex] アカウントの場合は、アカウント資格情報を指定します。

   1. 「**[!UICONTROL Setup Tracking]**」タブをクリックし、トラッキング設定を入力します。

   1. （[[!DNL Adobe Analytics for Advertising]  統合 &#x200B;](/help/integrations/analytics/overview.md)）を使用する広告主 **[!UICONTROL Set up Adobe Analytics]** タブをクリックし、キャンペーンアクティビティのトラッキングとレポートに使用するすべての [!DNL Analytics] レポートスイートを選択します。

1. 「**[!UICONTROL Save]**」をクリックします。

   アカウント内のすべてのキャンペーンに関する最近のコストとクリックデータは、検索、ソーシャル、Commerce（毎時）内で更新されます。 デフォルトでは、広告ネットワークに応じて、過去 5～10 日間データを利用できます。 ただし、必要に応じて、プロジェクトのローンチチームは最大 60 日間データを取得できます。

## 広告ネットワークアカウントの詳細の編集 {#edit-account}

アカウント設定を再認証して接続または更新の権限を更新するには、アカウントのアクティビティを有効または無効にするか、アカウント全体のデフォルトのトラッキングパラメーターを変更するか、トラッキングとレポートに使用する [!DNL Analytics] レポートスイートを変更してから、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

1. [&#x200B; アカウント設定 &#x200B;](#account-settings-api) の編集：

   1. （オプション）「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （任意）「**[!UICONTROL Setup Tracking]**」タブをクリックし、トラッキング設定を編集します。

   1. （任意。[[!DNL Adobe Analytics for Advertising]  統合 &#x200B;](/help/integrations/analytics/overview.md)）を使用する広告主。「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、キャンペーンアクティビティのトラッキングとレポートに使用する [!DNL Analytics] レポートスイートを編集します。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 「**[!UICONTROL Save]**」をクリックします。

   >[!NOTE]
   >
   >検索、ソーシャル、Commerceでは、新しいアカウントデータを広告ネットワーク上のアカウントデータと同期する必要があります。 これは、1 日に 1 回か、検索、ソーシャル、Commerceが広告ネットワーク上の変更を検出した場合により多く発生します。

## 広告ネットワークアカウントの再認証 {#reauthenticate}

広告ネットワーク接続を更新するか、アカウントの権限を更新するには、アカウントを再認証します。

1. （同じブラウザーアプリケーションで、同じ広告ネットワークの別のアカウントにログインしている場合）広告主以外のアカウントからログアウトします。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

1. 「**[!UICONTROL Account Details]**」タブで「**[!UICONTROL Re authenticate]**」をクリックし、広告主の資格情報を使用して広告ネットワークにログインします。

1. 「**[!UICONTROL Save]**」をクリックします。

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

広告ネットワークアカウントを有効にすると、検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。 広告ネットワークアカウントを無効にすると、検索、ソーシャルおよびCommerceは、アカウント上のすべてのアクティビティを停止します。 アカウントがアクティブだった間に収集されたデータは引き続き保存されますが、キャンペーン管理のビューとレポートには、アカウントが無効になっている期間のデータは含まれません。 後でアカウントを再度有効にして、アカウントを使用したアクティビティを再開できます。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの操作をおこないます。

   * （[!UICONTROL Accounts] ビューから）:

      * （アカウントを有効にするには）アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Activate]**」をクリックします。

      * （アカウントを無効にするには）アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Pause]**」をクリックします。

   * （アカウント設定から）

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

         * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. [**[!UICONTROL Account Details]**] タブで、[**[!UICONTROL Account enabled]**] をオフにします。

      1. 「**[!UICONTROL Save]**」をクリックします。

## ネットワーク アカウント設定の追加 {#account-settings-api}

アカウント設定は、広告ネットワークによって異なります。 以下の設定の一部が表示されない場合があります。

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### 「[!UICONTROL Select Accounts]/[!UICONTROL Account Details]」タブ

**[!UICONTROL Account Name]:** 検索、ソーシャル、Commerce内でアカウントに対して表示される名前。

>[!NOTE]
>
>検索、ソーシャル、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更している場合は、Adobe アカウントチームに連絡してマッピングを更新してください。

**[!DNL [Ad Network] アカウント &#x200B;]:** （アカウントの作成中に表示）同期する広告ネットワーク アカウント。

**[ログイン詳細 ]:** （Yandex アカウントのみ）使用するアカウント資格情報：

* **[!UICONTROL Login]:** アカウントへの API アクセスを有効にするためのログイン名または ID。

* **[!UICONTROL Password]:** アカウントのパスワード。

* **[!UICONTROL Access Key]:** 使用する開発者アカウントのアクセスキー。

* **[!UICONTROL Application ID]:** アカウントに使用する開発者トークン。 すべての [!DNL Yandex] アカウントで同じトークンが使用されます。

* **[!UICONTROL Purse Campaign ID]:** （共有アカウント設定が無効の [!DNL Yandex] アカウントのみ。オプション） アカウント内のすべての広告キャンペーンの支払いに使用されるキャンペーンの数値 ID。

* **[!UICONTROL Finance Token]:** （共有アカウント設定が無効の [!DNL Yandex] アカウントのみ。オプション）ポートフォリオの最適化に必要な場合に広告主のキャンペーン間でウォレットからお金を再割り当てするなど、財務関連の API 呼び出しに使用する開発者トークン。

**[!UICONTROL Network Account ID]:** （[!DNL Yandex] を除くすべての広告ネットワーク広告ネットワークによって割り当てられたアカウント ID。

>[!NOTE]
>
>広告ネットワーク マネージャーアカウントは、ここではサポートされていません。 [!DNL Microsoft Advertising] の管理者アカウントを特定するには、それぞれマスターアカウント ID または MCC アカウント フィールドを使用します。 [&#x200B; 管理者アカウントの資格情報の設定  [!DNL Google Ads]  を行うには &#x200B;](/help/search-social-commerce/admin/manager-accounts.md)\> [!UICONTROL Admin]&#x200B;[!UICONTROL Manager Accounts] 移動します。

**[!UICONTROL Currency]:** （読み取り専用）口座に使用される通貨の略称。 この値には、レコードを保存した後に、広告ネットワーク上のアカウントに設定された通貨が自動的に入力されます。

**[!UICONTROL Time Zone]:** 広告主のタイムゾーン。 この値は、レコードを保存すると、広告主の検索、ソーシャル、Commerce アカウント用に設定されたタイムゾーンで自動的に入力されます。

**[!UICONTROL Login]:** （読み取り専用）アカウントへのログインに使用するユーザーアカウント。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** 検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオのキャンペーンの自動入札やキャンペーン予算をプッシュします。

## 「[!UICONTROL Setup Tracking]」タブ

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** トラッキングを有効にするかどうかAdobe Advertising コンバージョントラッキングサービスを使用します。 この手法により、一意のクリックトラッキング ID が生成され、トラッキング目的でユーザーがAdobe Advertising サーバーにリダイレクトされた後で、クライアントのランディングページにユーザーが送られます。 このメソッドには、オプションでカスタマイズできるデフォルトのトラッキングオプションがあり、各 URL に追加するパラメーターを指定することもできます。

この機能を有効にするには、「トラッキングを有効にする **[をオンに]** ます。

>[!NOTE]
>
>* この設定を変更した場合は、アカウントのトラッキング URL を再生成する必要があります。
>* キャンペーンレベルのトラッキングオプションは、アカウントレベルの設定より優先されます。

**[!UICONTROL Tracking Type]:** （検索、ソーシャル、Commerceのトラッキングが有効な場合） エンドユーザーを最終的な URL または宛先 URL にリダイレクトする方法。 選択したオプションは、アカウントまたはキャンペーン内のすべての入札単位に適用されます。 デフォルトのアカウントレベルの設定は、広告主のトラッキング設定から継承され、デフォルトのキャンペーンレベルの設定は、アカウント設定から継承されます。

* *[!UICONTROL Standard]:* 指定した URL にエンドユーザーをリダイレクトするだけです。

* *[!UICONTROL Token]:* エンドユーザーを URL にリダイレクトし、クリック（`ef_id`）の検索、ソーシャル、Commerce ID もクエリ文字列パラメーターとして記録して、トークンとして使用できるようにします。 オフライントランザクションのレポートを作成する場合、検索、ソーシャルおよびCommerceでAdobe Analyticsとデータを交換する場合、またはブラウザー内で発生するすべてのコンバージョンをトラッキングする場合 [!DNL Apple Safari]、このオプションを選択します。

>[!NOTE]
>
>* [!UICONTROL Standard] から [!UICONTROL Token]、またはその逆に切り替える場合は、アカウントのトラッキング URL を再生成する必要があります。
>* アカウントレベルの設定は、キャンペーンレベルで上書きできます。

**[!UICONTROL Auto Update]:** （検索、ソーシャル、Commerceのトラッキングが有効な場合）は、ブラウザーとサーバー間の互換性を保つためにトラッキング URL を標準化します。 検索、ソーシャル、Commerceは、次の同期中に広告ネットワークに次の内容を自動的にアップロードします。（a）トラッキングテンプレートの検索、ソーシャル、Commerceトラッキングパラメーターと、最終 URL に追加された同じパラメーター、または（b）検索、ソーシャル、Commerceトラッキングコードが埋め込まれた新しい宛先 URL。 [Adobe AdvertisingとAdobe Analyticsの統合 &#x200B;](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) およびサーバーサイドの AMO ID （s_kwcid）設定を持つ広告主の場合、アップロードには [&#x200B; アカウントと &#x200B;](/help/integrations/analytics/ids.md#amo-id) アカウントの [!DNL Google Ads]AMO ID パラメーター [!DNL Microsoft Advertising] も含まれます。 デフォルトのアカウントレベルの設定は、広告主のトラッキング設定から継承されます。 アカウントレベルの設定は、キャンペーンレベルで上書きできます。

トラッキング URL は、同期していないエンティティ（追加された新しいエンティティと、プロパティが変更された既存のエンティティ）についてのみ、毎日更新されます。 したがって、既存の広告主/アカウント/キャンペーンに対してこの設定を無効から有効に変更した場合、既に同期している既存のエンティティのトラッキング URL は更新されません。 既存の同期内エンティティの URL にトラッキングを追加するには、Adobe アカウントチームに連絡して、1 回限りの手動による同期プロセスをリクエストします。 自動アップロードプロセスは、今後の変更に対応します。

**[!UICONTROL URL Encoding]:** （検索、ソーシャル、Commerceのトラッキングが有効な場合、宛先 URL を持つアカウントのみ）エンドユーザーのブラウザーアドレスバー内のベース URL をエンコードします（`%3D` ではなく `=` など）。

**[!UICONTROL Tracking Level]:** （検索、ソーシャル、Commerceのトラッキングが有効な場合。アカウントレベルとキャンペーンレベルで使用できます。並列トラッキングが有効な広告ネットワークには適用されません） リダイレクトを追加し（関連する場合）、関連する URL にパラメーターを追加することで、クリック数と売上高をトラッキングするレベルを指定します。

* *[!UICONTROL Keyword]:* キーワードレベルでのみデータを追跡します。 [!DNL Yandex] では使用できません。

* *[!UICONTROL Ad]:* 広告レベルでのみデータを追跡します。 [!DNL Naver] では使用できません。

* *[!UICONTROL Keyword and Ad]:* キーワードと広告レベルの両方でデータを追跡します。 [!DNL Naver] および [!DNL Yandex] では使用できません。

**[!UICONTROL Landing Page Suffix]** （[!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的な URL の末尾に追加するパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターを含めます。

例：`param1=value1&param2=value2`

Adobe Advertisingのクリックの追跡を使用するアカウントでは、アドネットワークのクリック識別子（`msclkid` の場合は [!DNL Microsoft Advertising]、Googleの場合は `gclid`）をサフィックスに含める必要があります。 Adobe Analytics統合を持つアカウントは、（`s_kwcid` で始まる） AMO ID パラメーターを使用する必要があります。 アカウントにサーバーサイド AMO ID 実装がある場合は、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 [&#x200B; に必要なサフィックス形式  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)、および [&#x200B; に必要なサフィックス形式  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) を参照してください。

>[!NOTE]
>
>* このフィールドは、[!UICONTROL Auto Update] トラッキング設定によって更新されません。
>* 下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

**アカウントトラッキング URL**:（[!DNL Google Ads]、[!DNL Microsoft Advertising] および [!DNL Yahoo! Japan Ads] アカウントのみ。任意）アカウントのデフォルトのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的/ランディングページの URL をパラメーターに埋め込みます。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

* 最終的な URL を埋め込むには：

   * （[!DNL Google Ads] および [!DNL Microsoft Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（ドキュメント [!DNL Microsoft Advertising] の「使用可能なトラッキングパラメーター」の節の（[[!DNL Microsoft Advertising]  のみ） &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799) ドキュメント [!DNL Google Ads] または（[!DNL ValueTrack] のみ） [[!DNL Google Ads]  「トラッキングテンプレートのみ」パラメーターを参照してください &#x200B;](https://support.google.com/google-ads/answer/6305348)

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーター `!{lpurl}` を使用して、ランディングページの URL を指定します。

* オプションで、URL パラメーターと、キャンペーンに定義されたカスタムパラメーターをアンパサンド（&amp;）で区切ったもの（`{lpurl}?matchtype={matchtype}&device={device}` など）を含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

* キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれている場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的にプレフィックス付けされます。

>[!NOTE]
>
>* [!DNL Google Ads] えば、並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームはカスタマーサポートまたは実装チームと協力して、マクロを追加する必要があります。
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 広告を承認用に再送信しなくても、アカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートを更新できます。

## 「[!UICONTROL Setup Analytics]」タブ

**[!UICONTROL Adobe Analytics Report Suite]:** （[[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md); オプション）を使用する広告主。検索、ソーシャルおよびCommerceが広告ネットワークから収集するデータ（エンティティ分類やアカウントのクリックデータなど）を送信する 1 つ以上の Analytics レポートスイート。 この機能は、サポートされている広告ネットワークでのみ使用できます。

レポートスイートにデータを表示するには、（a） アカウントに対してサーバーサイド AMO ID 機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、検索、ソーシャル、Commerceからデータを受信するように広告主の [!DNL Analytics] アカウントを設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [&#x200B; 広告ネットワークアカウントについて &#x200B;](../ad-network-account-about.md)
>* [&#x200B; マーチャントセンターアカウントの管理 &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [&#x200B; アカウントの s_kwcid トラッキングコード  [!DNL Google Ads]  更新 &#x200B;](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
