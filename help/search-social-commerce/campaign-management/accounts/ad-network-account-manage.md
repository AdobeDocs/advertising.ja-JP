---
title: 広告ネットワークアカウントの管理
description: 広告ネットワークアカウントのアカウントの詳細を設定および管理する方法について説明します。
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 0%

---

# 広告ネットワークアカウントの管理

広告ネットワークアカウントの詳細を作成および編集し、 [!DNL oAuth] アカウントのトークン、およびアカウントの無効化。

## 広告ネットワークアカウントの詳細の作成 {#create-account}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの同期または追跡を有効にするには、アカウントアクセス資格情報とトラッキングオプション、およびステータスを含む対応するアカウントレコードを作成する必要があります *アクティブ*. 各広告ネットワークで使用できる機能について詳しくは、[サポートされている在庫](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>広告ネットワーク上に実際のアカウントを作成するには、広告ネットワークの Web サイトにアクセスします。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 次を指定： [アカウント設定](#account-settings):

   1. 広告ネットワークの名前をクリックし、 **[!UICONTROL Next]**.

   1. 内 **[!UICONTROL Account Details]** 「 」セクションで、アカウントの詳細を入力します。

      ログイン認証タイプ「 」を使用する広告ネットワークの場合[!UICONTROL oAuth]、「 [OAuth 認証プロトコル](https://oauth.net/2/):

      1. 次を入力します。 **[!UICONTROL Login]** アカウントの値（オプション）、パスワードを入力し、 **[!UICONTROL Authenticate]**.

         ベストプラクティスは、アカウントへの API アクセスにログインを使用することです。 パスワードを入力して保存し、必要に応じてAdobeアカウントチームがトークンを更新できるようにします。

      1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへの API アクセスに資格情報を使用することです。

      1. 権限/アクセスをリクエスト画面で、「 」ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、 **[!UICONTROL oAuth Token]** フィールドに入力します。

      1. 残りのアカウントの詳細を指定します。

   1. クリック **[!UICONTROL Set Account Tracking]**、トラッキング設定を入力します。

1. クリック **[!UICONTROL Post]**.

   アカウント内のすべてのキャンペーンの最近のコストとクリックデータは、Search、Social、および Commerce 内で約 24 時間で使用できます。 デフォルトでは、広告ネットワークに応じて、過去 5 ～ 10 日間データを使用できます。 ただし、必要に応じて、プロジェクトの開始チームは過去 60 日間までのデータを取得できます。

## 広告ネットワークアカウントの詳細を編集 {#edit-account}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの資格情報が変更された場合、アカウント全体でデフォルトのトラッキングパラメーターを変更する場合、またはアカウントでのアクティビティを有効または無効にする場合、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークの Web サイトに移動します。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. アカウント名の上にカーソルを置き、 ![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")を選択し、 **[!UICONTROL Edit]**.

1. を編集します。 [アカウント設定](#account-settings):

   1. （オプション）アカウントの詳細を編集します。

   1. （オプション）「 **[!UICONTROL Set Account Tracking]**、トラッキング設定を編集します。

1. クリック **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >検索、ソーシャル、コマースは、新しいアカウントデータを広告ネットワーク上のデータと同期する必要があります。 これは、1 日に 1 回、または検索、ソーシャル、コマースで広告ネットワーク上の変更が検出された場合に、より頻繁に自動的に発生します。

## 検索アカウントの OAuth アクセストークンを更新します {#refresh-oauth-tokens}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

検索、ソーシャル、コマースで、 [OAuth 認証プロトコル](https://oauth.net/2/) およびアカウントの資格情報が変更された場合、または検索、ソーシャル、コマースの新機能をサポートするために追加のアクセス権が必要な場合は、そのアカウントの新しいアクセストークンを取得する必要があります。

新しい機能に新しいトークンが必要な場合は、Adobeアカウントチームから通知が届きます。

1. （同じブラウザーアプリケーションで同じ広告ネットワークの別のアカウントにログインした場合）広告主以外のアカウントからログアウトします。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. アカウント名の上にカーソルを置き、 ![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")を選択し、 **[!UICONTROL Edit]**.

1. 新しいアクセストークンを取得する：

   1. クリック **[!UICONTROL Get oAuth Token]**.

   1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへの API アクセスに資格情報を使用することです。

   1. 権限/アクセスをリクエスト画面で、「 」ボタンをクリックして権限を確認します。

   1. 開いたポップアップウィンドウで認証文字列をコピーし、 **[!UICONTROL oAuth Token]** フィールドに入力します。

1. クリック **[!UICONTROL Post]**.

## 広告ネットワークアカウントの有効化または無効化 {#enable-disable-account}

*エージェンシーアカウントマネージャー、Adobeアカウントマネージャー、管理者ユーザーの役割のみ*

広告ネットワークアカウントを有効にすると、Search、Social、&amp;Commerce はキャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。 アカウントがアクティブな間に収集されたデータは保存されますが、キャンペーン管理の表示とレポートには、アカウントが無効になっている期間のデータは含まれません。 後でアカウントを再度有効にして、アカウントでのアクティビティを再開できます。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 次のいずれかの操作を行います。

   * （1 つのアカウントのステータスを変更する場合）アカウント名の上にカーソルを置いたまま、 ![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")を選択し、 **[!UICONTROL Edit]**. を **[!UICONTROL Status]** から *有効* または *無効*&#x200B;をクリックし、 **[!UICONTROL Post]**.

   * （1 つ以上のアカウントのステータスを変更するには）次の操作を行います。

      1. 各アカウントの横にあるチェックボックスを選択します。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. データテーブルの上にあるツールバーで、 ![アクティベートアイコン](/help/search-social-commerce/assets/activate.png "アクティベートアイコン") アカウントを有効にするか、 ![無効アイコン](/help/search-social-commerce/assets/disable.png "無効アイコン") をクリックして、アカウントを無効にします。

## 広告ネットワークアカウントの設定 {#account-settings}

>[!NOTE]
>
>代理店のアカウントマネージャーのみ [!DNL Adobe] アカウントマネージャーおよび管理者ユーザーは、アカウント設定を構成できます。

### アカウントの詳細

**[!UICONTROL SE Account ID]:** ( 以下を除くすべてのアカウント [!DNL Naver] および [!DNL Yandex] アカウント新規アカウントのみ編集可能 ) 広告ネットワークによって割り当てられるアカウント ID。

>[!NOTE]
>
>ここでは、広告ネットワークマネージャーアカウントはサポートされていません。 のマネージャアカウントを識別するには [!DNL Microsoft Advertising] または [!DNL Yandex]「アカウント ID 」または「 MCCマスター」フィールドをそれぞれ使用します。 宛先 [の資格情報を設定する [!DNL Google Ads] 管理者アカウント](/help/search-social-commerce/admin/manager-accounts.md)に移動します。 [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** 検索、ソーシャル、コマース内のアカウントに表示する名前。

>[!NOTE]
>
>検索、ソーシャル、およびコマース — Adobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobeのアカウントチームに通知して、マッピングを更新できるようにします。

**[!UICONTROL Login Details]:\[ ログインタイプ\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] （のみ）次を使用して、アカウントへのログインを承認するかどうかを指定します。

* *[!UICONTROL oAuth]* （デフォルト）:次の手順で [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/).

* *[!UICONTROL Password]:* クライアントのパスワードを使用する場合。

の場合 [!DNL Microsoft Advertising] アカウントのみ [!DNL oAuth] — 許可されたログインを使用できます。

**[!UICONTROL Login Details]: [!UICONTROL Login]:** ( 以下を除くすべての広告ネットワーク [!DNL Naver]) アカウントへの API アクセスを有効にするためのログイン名または ID。

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth] — 有効および以外のすべてのネットワーク [!DNL Baidu], [!DNL Meta]、および [!DNL Yandex]) [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** ( 以下を除くすべての広告ネットワーク [!DNL Naver]) アカウントのパスワードです。 パスワードが有効なアカウントの場合： [!DNL Baidu], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]、および [!DNL Yandex]の場合、このフィールドは必須です。 の場合 [!DNL oAuth]有効なアカウントの場合、このフィールドはオプションです。アカウントマネージャーが必要に応じてトークンを更新できるように、パスワードを暗号化して保存する場合に使用します。

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Baidu] および [!DNL Yandex] アカウントのみ ) 使用する開発者アカウントのアクセスキー。

**[!UICONTROL Currency]:** アカウントに使用する通貨の略称です。 このフィールドは新規用に編集可能です [!DNL Naver] アカウント。 その他すべての検索ネットワークでは、レコードを保存すると、広告ネットワーク上のアカウントに設定されている通貨が値に自動的に入力されます。

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ（オプション）情報を追跡するために最終 URL の末尾に追加するパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターを含めます。

例： `param1=value1&param2=value2`

Adobe広告のクリック追跡を使用するアカウントには、広告ネットワークのクリック識別子 (`msclkid` 対象 [!DNL Microsoft Advertising]; `gclid` (Googleの場合 ) をサフィックスに含めます。 Adobe Analytics統合のアカウントでは、 `s_kwcid` パラメーター。 アカウントにサーバー側の s\_kwcid 実装がある場合、ユーザーが広告をクリックすると、パラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 詳しくは、 [必要なサフィックス形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) および [必要なサフィックス形式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* このフィールドは [!UICONTROL Auto Upload] トラッキング設定。
>* 下位レベルでの最終的な URL サフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

**タイムゾーン：** ( を除くすべての広告ネットワーク [!DNL Baidu] および [!DNL Yahoo! Display Network]) 広告主のタイムゾーン。 このフィールドは編集可能で、新規の場合はオプションです [!DNL Naver] アカウント。 その他すべての検索ネットワークでは、レコードを保存すると、広告主の検索、ソーシャル、コマースアカウント用に設定されたタイムゾーンが値に自動的に入力されます。

**ステータス：** 検索、ソーシャル、コマース内のアカウントのステータス：

* *有効：* 検索、ソーシャル、コマースはキャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。
* *無効：* Search、Social、および Commerce は、アカウント上のすべてのアクティビティを停止します。 アカウントがアクティブな間に収集されたデータは保存されますが、キャンペーン管理の表示とレポートには、アカウントが一時停止された期間のデータは含まれません。 後でアカウントを再アクティブ化して、アカウントでのアクティビティを再開できます。

**トラッキングテンプレート** - ([!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] アカウントのみ（オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込む、アカウントのデフォルトのトラッキングテンプレート。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。

* 最終 URL を埋め込むには：

   * ([!DNL Google Ads] および [!DNL Microsoft Advertising] のみ ) トラッキングテンプレートの最終 URL を示すパラメーターのリストについては、[!DNL Microsoft Advertising] のみ ) [[!DNL Microsoft Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799) または ([!DNL Google Ads] （専用） [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] のみ ) パラメーターを使用する `!{lpurl}` をクリックして、ランディングページの URL を指定します。

* オプションとして、URL パラメーターと、キャンペーンに定義されているカスタムパラメーターを、アンパサンド (&amp;) で区切って含めることができます。例えば、 `{lpurl}?matchtype={matchtype}&device={device}`.

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

* キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。

>[!NOTE]
>
>* の場合 [!DNL Google Ads]を使用する場合は、並列追跡を有効にするソースからのクリック数に代わられないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。
>* 最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。
>* 広告、サイトリンク、またはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告が再送信され、レビューが必要になります。 広告を承認用に再送信しなくても、アカウント、キャンペーンまたは広告グループレベルでトラッキングテンプレートを更新できます。

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] アカウントのみ ) アカウントに関連付けられたエージェンシー/管理アカウントの ID。

**[!UICONTROL MCC Account]:** ([!DNL Yandex] アカウントのみ（オプション）アカウントに関連付けられたエージェンシー/管理アカウント。 既存の関連付けを削除するには、「[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] アカウントのみ ) アカウントに使用する開発者トークン。 すべてに同じトークンが使用されます [!DNL Yandex] アカウント。

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] [ 共有アカウント ] 設定が無効になっているアカウントのみ。（オプション）アカウント内のすべての広告キャンペーンの支払いに使用されるキャンペーンの数値 ID。

**[!UICONTROL Finance Token]:** ([!DNL Yandex] [ 共有アカウント ] 設定が無効になっているアカウントのみ。（オプション）財務関連の API 呼び出しに使用する開発者トークン。ポートフォリオの最適化に必要に応じて、広告主のキャンペーンの間のウォレットから金額を再割り当てする場合などに使用します。

### アカウントトラッキング

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** ( の [!UICONTROL EF Redirect] （のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S\_kwcid 形式** - ( 既存 [!DNL Google Ads] AdobeAdvertising とAdobe Analyticsの統合を持ち、s\_kwcid がまだ移行されていない広告主のアカウント )

このアカウントでは、s\_kwcid トラッキングコードの従来の形式を使用します。これにより、Adobe広告は、アカウントに関するデータをAdobe Analyticsと共有できます。 この [最新形式](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) には、キャンペーン ID と広告グループ ID のパラメーターが含まれます。これらのパラメーターは、次のキャンペーンレベルと広告グループレベルで正確にレポートするために必要です。 [!DNL Google Ads] Analytics の最大キャンペーン数およびドラフト&amp;実験キャンペーン数：

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

このアカウントがキャンペーンおよび広告グループレベルでレポートする必要がある場合は、 [!UICONTROL Edit] （鉛筆）アイコン **[!UICONTROL Migrate to new s\_kwcid format]** を新しい形式に変更します。 これらのキャンペーンタイプを含まないアカウントの場合、新しい形式への移行はオプションですが、お勧めします。

詳しい手順については、[の s\_kwcid トラッキングコードを更新します。 [!DNL Google Ads] アカウント](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;

**レポートスイート名** - ( トークンを使用した EF リダイレクトの場合のみ。広告主とAdobeAdvertising-Adobe Analyticsの統合；（オプション）検索、ソーシャル、コマースが広告ネットワークから収集したデータの送信先となる 1 つ以上の Analytics レポートスイート（エンティティの分類、アカウントのクリックデータなど）。 この機能は、サポートされている広告ネットワークでのみ使用できます。

データをレポートスイートに表示するには、(a) サーバー側の s\_kwcid をアカウント用に設定するか、(b) 広告主レベルの設定を「[!UICONTROL Enable tracking for SAINT feeds]」を有効にする必要があります。 さらに、検索、ソーシャル、コマースからデータを受け取るように広告主の Analytics アカウントを設定する必要があります。 詳しくは、担当のAdobeアカウントマネージャーにお問い合わせください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントについて](ad-network-account-about.md)
>* [マーチャントセンターアカウントの管理](merchant-account-manage.md)
>* [の s\_kwcid トラッキングコードを更新します。 [!DNL Google Ads] アカウント](update-skwcid-google.md)
