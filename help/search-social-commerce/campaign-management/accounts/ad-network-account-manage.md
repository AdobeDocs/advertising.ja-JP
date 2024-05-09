---
title: 広告ネットワークアカウントの管理
description: 広告ネットワークアカウントのアカウント詳細を設定および管理する方法について説明します。
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# 広告ネットワークアカウントの管理

以下は、広告ネットワークアカウントの詳細の作成と編集、更新手順です。 [!DNL oAuth] アカウントのトークンとアカウントの無効化。

各広告ネットワークで使用できる機能について詳しくは、「」を参照してください[サポートされているインベントリ](/help/search-social-commerce/introduction/supported-inventory.md).」と入力します。

## 広告ネットワークアカウントの詳細を作成 {#create-account}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

アカウントの同期またはトラッキングを有効にするには、対応するアカウントレコードを作成する必要があります。このアカウントレコードには、アカウントアクセス資格情報とトラッキングオプション、およびのステータスが含まれています *アクティブ*.

>[!NOTE]
>
>* 新規のサポートは利用できません [!DNL Baidu] アカウント。
>* 広告ネットワーク上に実際のアカウントを作成するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. データ テーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. を指定 [アカウント設定](#account-settings):

   1. 広告ネットワークの名前をクリックし、 **[!UICONTROL Next]**.

   1. が含まれる **[!UICONTROL Account Details]** セクションに、アカウントの詳細を入力します。

      ログイン認証タイプ「」を使用する広告ネットワークの場合[!UICONTROL oAuth],」の場合は、検索、ソーシャル、Commerceに [OAuth 認証プロトコル](https://oauth.net/2/):

      1. を入力 **[!UICONTROL Login]** アカウントの値。必要に応じてパスワードを入力し、 **[!UICONTROL Authenticate]**.

         ベストプラクティスは、アカウントへの API アクセスに login を使用することです。 暗号化する際にパスワードを入力して保存し、Adobeアカウントチームが必要に応じてトークンを更新できるようにします。

      1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへの API アクセスに資格情報を使用することです。

      1. 権限/アクセスのリクエスト画面で、「」ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、に貼り付けます。 **[!UICONTROL oAuth Token]** フィールド。

      1. 残りのアカウントの詳細を指定します。

   1. クリック **[!UICONTROL Set Account Tracking]**&#x200B;を選択し、トラッキング設定を入力します。

1. クリック **[!UICONTROL Post]**.

   アカウント内のすべてのキャンペーンに関する最近のコストとクリックデータは、検索、ソーシャル、Commerce内で約 24 時間で利用できます。 デフォルトでは、広告ネットワークに応じて、過去 5～10 日間データを利用できます。 ただし、必要に応じて、プロジェクトのローンチチームは最大 60 日間データを取得できます。

## 広告ネットワークアカウントの詳細の編集 {#edit-account}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

アカウント資格情報を変更する場合、アカウント全体のデフォルトのトラッキングパラメーターを変更するか、アカウントのアクティビティを有効または無効にしてから、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. アカウント名の上にカーソルを置き、クリックします ![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")を選択してから、 **[!UICONTROL Edit]**.

1. を編集する [アカウント設定](#account-settings):

   1. （任意）アカウントの詳細を編集します。

   1. （任意）クリック **[!UICONTROL Set Account Tracking]**&#x200B;で、トラッキング設定を編集します。

1. クリック **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >検索、ソーシャル、Commerceでは、新しいアカウントデータを広告ネットワーク上のアカウントデータと同期する必要があります。 これは、1 日に 1 回か、検索、ソーシャル、Commerceが広告ネットワーク上の変更を検出した場合により多く発生します。

## 検索アカウントの OAuth アクセストークンの更新 {#refresh-oauth-tokens}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

検索、ソーシャルおよびCommerceが、 [OAuth 認証プロトコル](https://oauth.net/2/) アカウント資格情報が変わった場合、または検索、ソーシャル、Commerceの新機能をサポートするために追加のアクセスが必要な場合は、アカウントの新しいアクセストークンを取得する必要があります。

新機能に新しいトークンが必要な場合は、Adobeアカウントチームからお知らせします。

1. （同じブラウザーアプリケーションで、同じ広告ネットワークの別のアカウントにログインしている場合）広告主以外のアカウントからログアウトします。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. アカウント名の上にカーソルを置き、クリックします ![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")を選択してから、 **[!UICONTROL Edit]**.

1. 新しいアクセストークンの取得：

   1. クリック **[!UICONTROL Get oAuth Token]**.

   1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへの API アクセスに資格情報を使用することです。

   1. 権限/アクセスのリクエスト画面で、「」ボタンをクリックして権限を確認します。

   1. 開いたポップアップウィンドウで認証文字列をコピーし、に貼り付けます。 **[!UICONTROL oAuth Token]** フィールド。

1. クリック **[!UICONTROL Post]**.

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

Ad Network アカウントを有効にすると、検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。Ad Network アカウントを無効にすると、検索、ソーシャル、Commerceはアカウントのすべてのアクティビティを停止します。 アカウントがアクティブだった間に収集されたデータは引き続き保存されますが、キャンペーン管理のビューとレポートには、アカウントが無効になっている期間のデータは含まれません。 後でアカウントを再度有効にして、アカウントを使用したアクティビティを再開できます。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 次のいずれかの操作をおこないます。

   * （単一のアカウントのステータスを変更するには）アカウント名の上にカーソルを置き、 ![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")を選択してから、 **[!UICONTROL Edit]**. 変更： **[!UICONTROL Status]** 対象： *Enabled* または *Disabled*&#x200B;を選択し、 **[!UICONTROL Post]**.

   * （1 つ以上のアカウントのステータスを変更するには）次の手順を実行します。

      1. 各アカウントの横にあるチェックボックスを選択します。

         複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

      1. データ テーブルの上にあるツールバーで、 ![アクティベートアイコン](/help/search-social-commerce/assets/activate.png "アクティベートアイコン") アカウントを有効にする ![無効アイコン](/help/search-social-commerce/assets/disable.png "無効アイコン") をクリックしてアカウントを無効にします。

## ネットワーク アカウント設定の追加 {#account-settings}

>[!NOTE]
>
>代理店アカウントマネージャーのみ、 [!DNL Adobe] アカウントマネージャーと管理者ユーザーは、アカウント設定を構成できます。

### アカウントの詳細

**[!UICONTROL SE Account ID]:** （を除くすべてのアカウント） [!DNL Naver] および [!DNL Yandex] アカウント。新しいアカウントでのみ編集できます）広告ネットワークによって割り当てられたアカウント ID。

>[!NOTE]
>
>広告ネットワーク マネージャーアカウントは、ここではサポートされていません。 の管理者アカウントを識別するには [!DNL Microsoft Advertising] または [!DNL Yandex]は、それぞれマスターアカウント ID または MCC アカウント フィールドを使用します。 終了 [の資格情報の設定 [!DNL Google Ads] manager account](/help/search-social-commerce/admin/manager-accounts.md)に移動します。 [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** 検索、ソーシャル、Commerce内でアカウントに対して表示される名前。

>[!NOTE]
>
>検索、ソーシャル、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobeアカウントチームに通知して、マッピングを更新できるようにします。

**[!UICONTROL Login Details]: \[ ログインタイプ\]** - （[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] のみ）次を使用してアカウントへのログインを認証するかどうか。

* *[!UICONTROL oAuth]* （デフォルト）：を使用します [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/).

* *[!UICONTROL Password]:* クライアントのパスワードを使用します。

の場合 [!DNL Microsoft Advertising] アカウント （のみ） [!DNL oAuth]許可されたログインを使用できます。

**[!UICONTROL Login Details]: [!UICONTROL Login]:** （次を除くすべての広告ネットワーク） [!DNL Naver]） ログイン名または ID。アカウントへの API アクセスを有効にします。

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** （[!DNL Microsoft Advertising] [!DNL oAuth]-enabled およびその他のすべてのネットワーク（を除く） [!DNL Meta] および [!DNL Yandex]） アカウントのトークンで、 [[!DNL OAuth] 認証プロトコル](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** （次を除くすべての広告ネットワーク） [!DNL Naver]） アカウントのパスワード。 パスワードが有効なアカウントの場合： [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]、および [!DNL Yandex]。このフィールドは必須です。 の場合 [!DNL oAuth]が有効なアカウントの場合は、このフィールドはオプションです。必要に応じてアカウント・マネージャがトークンを更新できるように、パスワードを暗号化および保存する場合に使用します。

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** （[!DNL Yandex] アカウントのみ）使用する開発者アカウントのアクセスキー。

**[!UICONTROL Currency]:** 勘定に使用される通貨の省略形。 このフィールドは新しいで編集可能です [!DNL Naver] アカウント。 その他のすべての検索ネットワークでは、レコードを保存すると、広告ネットワークのアカウントに設定された通貨が値に自動的に入力されます。

**[!UICONTROL Landing Page Suffix]** （[!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的な URL の末尾に追加するパラメーター。ビジネスで追跡する必要があるすべてのパラメーターが含まれます。

例： `param1=value1&param2=value2`

広告のクリックの追跡を使用するアカウントには、Adobe Advertisingネットワークのクリック識別子（`msclkid` （用） [!DNL Microsoft Advertising]; `gclid` （Googleの場合）。 Adobe Analytics統合を持つアカウントは、（で始まる） AMO ID パラメーターを使用する必要があります `s_kwcid`）に設定します。 アカウントにサーバーサイド AMO ID 実装がある場合は、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 を参照してください。 [に必要なサフィックス形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) および [に必要なサフィックス形式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* このフィールドは、によって更新されません [!UICONTROL Auto Upload] トラッキング設定。
>* 下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

**タイムゾーン：** （を除くすべての広告ネットワーク） [!DNL Baidu] および [!DNL Yahoo! Display Network]）広告主のタイムゾーン。 このフィールドは新しいに対して編集可能であり、オプションです [!DNL Naver] アカウント。 その他のすべての検索ネットワークでは、レコードを保存すると、広告主の検索、ソーシャル、Commerce アカウント用に設定されたタイムゾーンが、値に自動的に入力されます。

**状態：** 検索、ソーシャル、Commerce内のアカウントのステータス：

* *有効：* 検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオのキャンペーンの自動入札やキャンペーン予算をプッシュします。
* *無効：* 検索、ソーシャル、Commerceは、アカウント上のすべてのアクティビティを停止します。 アカウントがアクティブな間に収集されたデータは引き続き保存されますが、キャンペーン管理のビューやレポートには、アカウントが一時停止された期間のデータは含まれません。 後でアカウントを再アクティブ化して、アカウントでのアクティビティを再開できます。

**追跡テンプレート** - （[!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] アカウントのみ。オプション）アカウントのデフォルトのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込みます。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` これにより、リダイレクトが含まれます。

* 最終的な URL を埋め込むには：

   * （[!DNL Google Ads] および [!DNL Microsoft Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（[!DNL Microsoft Advertising] のみ） [[!DNL Microsoft Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/56799) または（[!DNL Google Ads] のみ）「使用可能」のセクションの「トラッキングテンプレートのみ」パラメーター [!DNL ValueTrack] のパラメーター [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/6305348).

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーターを使用します `!{lpurl}` ランディングページの URL を指定します。

* オプションで、次のような URL パラメーターと、キャンペーンに定義されたカスタムパラメーターをアンパサンド（&amp;）で区切って含めることができます `{lpurl}?matchtype={matchtype}&device={device}`.

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

* キャンペーン設定に「」が含まれる場合[!UICONTROL EF Redirect]「」と「」に対して検査する値[!UICONTROL Auto Upload],」という文字列が表示される場合、レコードを保存すると、検索、ソーシャル、Commerce自体のリダイレクトおよびトラッキングコードが自動的にプレフィックスとして付けられます。

>[!NOTE]
>
>* の場合 [!DNL Google Ads]を使用する場合は、マクロを使用しないでください。このマクロは、並列トラッキングを有効にするソースからのクリックに代わるものではありません。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 広告を承認用に再送信しなくても、アカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートを更新できます。

**[!UICONTROL Master Account ID]:** （[!DNL Microsoft Advertising] アカウントのみ）アカウントに関連付けられた代理店/管理アカウントの ID。

**[!UICONTROL MCC Account]:** （[!DNL Yandex] アカウントのみ。オプション）アカウントに関連付けられている代理店/管理アカウント。 既存の関連付けを削除するには、「」を選択[!UICONTROL No MCC Account].」と入力します。

**[!UICONTROL Application ID]:** （[!DNL Yandex] アカウントのみ） アカウントに使用する開発者トークン。 すべてに同じトークンが使用されます [!DNL Yandex] アカウント。

**[!UICONTROL Purse Campaign ID]:** （[!DNL Yandex] 共有アカウント設定が無効のアカウントのみ（オプション） アカウント内のすべての広告キャンペーンの支払いに使用されるキャンペーンの数値 ID。

**[!UICONTROL Finance Token]:** （[!DNL Yandex] 「共有アカウント」設定が無効のアカウントのみ（オプション）。ポートフォリオの最適化に必要に応じて広告主のキャンペーン間でウォレットから資金を再割り当てするなど、財務関連の API 呼び出しに使用する開発者トークンです。

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

**[!UICONTROL Track Product Group]:** （用 [!UICONTROL EF Redirect] のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid 形式** - （既存 [!DNL Google Ads] Adobe AdvertisingとAdobe Analytics統合を持ち、AMO ID （s_kwcid）がまだ移行されていない広告主用のアカウント）

このアカウントは、AMO ID トラッキングコードの従来の形式を使用しています。これにより、Adobe AdvertisingはAdobe Analyticsとアカウントに関するデータを共有できます。 この [最新フォーマット](/help/integrations/analytics/ids.md#amo-id-formats) 次のキャンペーンおよび広告グループ レベルで正確にレポートするために必要な、キャンペーン ID および広告グループ ID のパラメーターが含まれます [!DNL Google Ads] analytics のパフォーマンス最大キャンペーン数、ドラフト数、実験キャンペーン数：

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

このアカウントをキャンペーンレベルおよび広告グループレベルでレポートする必要がある場合は、 [!UICONTROL Edit] （鉛筆）アイコンで囲み、 **[!UICONTROL Migrate to new s_kwcid format]** を新しい形式に変更します。 これらのキャンペーンタイプを含まないアカウントの場合、新しい形式への移行はオプションですが、お勧めします。

詳しい手順については、を参照してください[の AMO ID トラッキングコードの更新 [!DNL Google Ads] アカウント](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).」と入力します。

**レポートスイート名** - （トークン付き EF リダイレクトのみ。Adobe AdvertisingとAdobe Analyticsの統合を持つ広告主。オプション）検索、ソーシャル、Commerceが広告ネットワークから収集するデータを送信する 1 つ以上の Analytics レポートスイート。これには、アカウントのエンティティ分類やクリックデータが含まれます。 この機能は、サポートされている広告ネットワークでのみ使用できます。

レポートスイートにデータを表示するには、（a） アカウントにサーバーサイド AMO ID 機能を設定するか、（b）広告主レベルの設定を「」にする必要があります[!UICONTROL Enable tracking for SAINT feeds]」を有効にする必要があります。 さらに、検索、ソーシャル、Commerceからデータを受信するように広告主の Analytics アカウントを設定する必要があります。 詳しくは、Adobe担当営業または販売店にお問い合わせください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントについて](ad-network-account-about.md)
>* [マーチャントセンターアカウントの管理](merchant-account-manage.md)
>* [の s_kwcid トラッキングコードを更新します [!DNL Google Ads] アカウント](update-amo-id-google.md)
