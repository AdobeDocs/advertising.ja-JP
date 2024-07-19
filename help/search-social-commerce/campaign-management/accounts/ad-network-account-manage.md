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

以下は、広告ネットワークアカウントの詳細の作成と編集、アカウントの [!DNL oAuth] トークンの更新、アカウントの無効化の手順です。

各広告ネットワークで使用できる機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## 広告ネットワークアカウントの詳細を作成 {#create-account}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

アカウントの同期または追跡を有効にするには、対応するアカウントレコードを作成する必要があります。これには、アカウントのアクセス資格情報と追跡オプションが含まれ、ステータスが *アクティブ* のアカウントレコードが含まれています。

>[!NOTE]
>
>* 新しい [!DNL Baidu] アカウントではサポートを利用できません。
>* 広告ネットワーク上に実際のアカウントを作成するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、「\>」 **[!UICONTROL Search]** 「\>」 **[!UICONTROL Campaigns]** 「\>」をクリッ **[!UICONTROL Campaigns]** します。 サブメニューで、[\> **[!UICONTROL Accounts]**]**[!UICONTROL Live]** クリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. [ アカウント設定 ](#account-settings) を指定します。

   1. 広告ネットワークの名前をクリックし、[**[!UICONTROL Next]**] をクリックします。

   1. 「**[!UICONTROL Account Details]**」セクションで、アカウントの詳細を入力します。

      ログイン認証タイプ「[!UICONTROL oAuth]」を使用する広告ネットワークの場合、検索、ソーシャル、Commerceから [OAuth 認証プロトコル ](https://oauth.net/2/) を使用してアカウントにアクセスできるようにします。

      1. アカウントの **[!UICONTROL Login]** 値を入力し、必要に応じてパスワードを入力し、[**[!UICONTROL Authenticate]**] をクリックします。

         ベストプラクティスは、アカウントへの API アクセスに login を使用することです。 暗号化する際にパスワードを入力して保存し、Adobeアカウントチームが必要に応じてトークンを更新できるようにします。

      1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへの API アクセスに資格情報を使用することです。

      1. 権限/アクセスのリクエスト画面で、「」ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、**[!UICONTROL oAuth Token]** フィールドに貼り付けます。

      1. 残りのアカウントの詳細を指定します。

   1. 「**[!UICONTROL Set Account Tracking]**」をクリックし、トラッキング設定を入力します。

1. 「**[!UICONTROL Post]**」をクリックします。

   アカウント内のすべてのキャンペーンに関する最近のコストとクリックデータは、検索、ソーシャル、Commerce内で約 24 時間で利用できます。 デフォルトでは、広告ネットワークに応じて、過去 5～10 日間データを利用できます。 ただし、必要に応じて、プロジェクトのローンチチームは最大 60 日間データを取得できます。

## 広告ネットワークアカウントの詳細の編集 {#edit-account}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

アカウント資格情報を変更する場合、アカウント全体のデフォルトのトラッキングパラメーターを変更するか、アカウントのアクティビティを有効または無効にしてから、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、「\>」 **[!UICONTROL Search]** 「\>」 **[!UICONTROL Campaigns]** 「\>」をクリッ **[!UICONTROL Campaigns]** します。 サブメニューで、[\> **[!UICONTROL Accounts]**]**[!UICONTROL Live]** クリックします。

1. カーソルをアカウント名の上に置き、「![ その他 ](/help/search-social-commerce/assets/more-filters.png " 詳細 ")」をクリックして「**[!UICONTROL Edit]**」を選択します。

1. [ アカウント設定 ](#account-settings) の編集：

   1. （任意）アカウントの詳細を編集します。

   1. （任意）「**[!UICONTROL Set Account Tracking]**」をクリックして、トラッキング設定を編集します。

1. 「**[!UICONTROL Post]**」をクリックします。

   >[!NOTE]
   >
   >検索、ソーシャル、Commerceでは、新しいアカウントデータを広告ネットワーク上のアカウントデータと同期する必要があります。 これは、1 日に 1 回か、検索、ソーシャル、Commerceが広告ネットワーク上の変更を検出した場合により多く発生します。

## 検索アカウントの OAuth アクセストークンの更新 {#refresh-oauth-tokens}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

検索、ソーシャル、Commerceが [OAuth 認証プロトコル ](https://oauth.net/2/) を使用してアカウントにアクセスし、アカウントの資格情報が変わった場合、または検索、ソーシャル、Commerceの新機能をサポートするために追加のアクセスが必要な場合は、アカウントの新しいアクセストークンを取得する必要があります。

新機能に新しいトークンが必要な場合は、Adobeアカウントチームからお知らせします。

1. （同じブラウザーアプリケーションで、同じ広告ネットワークの別のアカウントにログインしている場合）広告主以外のアカウントからログアウトします。

1. メインメニューで、「\>」 **[!UICONTROL Search]** 「\>」 **[!UICONTROL Campaigns]** 「\>」をクリッ **[!UICONTROL Campaigns]** します。 サブメニューで、[\> **[!UICONTROL Accounts]**]**[!UICONTROL Live]** クリックします。

1. カーソルをアカウント名の上に置き、「![ その他 ](/help/search-social-commerce/assets/more-filters.png " 詳細 ")」をクリックして「**[!UICONTROL Edit]**」を選択します。

1. 新しいアクセストークンの取得：

   1. 「**[!UICONTROL Get oAuth Token]**」をクリックします。

   1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへの API アクセスに資格情報を使用することです。

   1. 権限/アクセスのリクエスト画面で、「」ボタンをクリックして権限を確認します。

   1. 開いたポップアップウィンドウで認証文字列をコピーし、**[!UICONTROL oAuth Token]** フィールドに貼り付けます。

1. 「**[!UICONTROL Post]**」をクリックします。

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

Ad Network アカウントを有効にすると、検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。Ad Network アカウントを無効にすると、検索、ソーシャル、Commerceはアカウントのすべてのアクティビティを停止します。 アカウントがアクティブだった間に収集されたデータは引き続き保存されますが、キャンペーン管理のビューとレポートには、アカウントが無効になっている期間のデータは含まれません。 後でアカウントを再度有効にして、アカウントを使用したアクティビティを再開できます。

1. メインメニューで、「\>」 **[!UICONTROL Search]** 「\>」 **[!UICONTROL Campaigns]** 「\>」をクリッ **[!UICONTROL Campaigns]** します。 サブメニューで、[\> **[!UICONTROL Accounts]**]**[!UICONTROL Live]** クリックします。

1. 次のいずれかの操作をおこないます。

   * （1 つのアカウントのステータスを変更するには）アカウント名の上にカーソルを置き、![ 詳細 ") をクリックして ](/help/search-social-commerce/assets/more-filters.png "**[!UICONTROL Edit]** を選択します。 **[!UICONTROL Status]** を *有効* または *無効* に変更し、「**[!UICONTROL Post]**」をクリックします。

   * （1 つ以上のアカウントのステータスを変更するには）次の手順を実行します。

      1. 各アカウントの横にあるチェックボックスを選択します。

         複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. データテーブルの上にあるツールバーで ![ アクティベートアイコン ](/help/search-social-commerce/assets/activate.png " アクティベートアイコン ") をクリックして、アカウントを有効にするか、![無効アイコン](/help/search-social-commerce/assets/disable.png "無効アイコン") をクリックしてアカウントを無効にします。

## ネットワーク アカウント設定の追加 {#account-settings}

>[!NOTE]
>
>アカウント設定を構成できるのは、代理店アカウントマネージャー、[!DNL Adobe] ーザーアカウントマネージャー、管理者ユーザーのみです。

### アカウントの詳細

**[!UICONTROL SE Account ID]:** （[!DNL Naver] アカウントおよび [!DNL Yandex] アカウントを除くすべてのアカウント。新しいアカウントでのみ編集できます）広告ネットワークによって割り当てられたアカウント ID。

>[!NOTE]
>
>広告ネットワーク マネージャーアカウントは、ここではサポートされていません。 [!DNL Microsoft Advertising] または [!DNL Yandex] の管理者アカウントを特定するには、それぞれマスターアカウント ID または MCC アカウント フィールドを使用します。 [ 管理者アカウントの資格情報の設定 ](/help/search-social-commerce/admin/manager-accounts.md) を行うには  [!DNL Google Ads] \> [!UICONTROL Manager Accounts][!UICONTROL Admin] 移動します。

**[!UICONTROL Account Name]:** 検索、ソーシャル、Commerce内でアカウントに対して表示される名前。

>[!NOTE]
>
>検索、ソーシャル、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobeアカウントチームに通知して、マッピングを更新できるようにします。

**[!UICONTROL Login Details]: \[Login Type\]** - （[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] のみ）次を使用してアカウントへのログインを許可するかどうか：

* *[!UICONTROL oAuth]* （デフォルト）: [[!DNL OAuth]  認証プロトコル ](https://oauth.net/2/) を使用します。

* *[!UICONTROL Password]:* クライアントのパスワードを使用します。

[!DNL Microsoft Advertising] アカウントの場合は、[!DNL oAuth] 許可されたログインのみを使用できます。

**[!UICONTROL Login Details]: [!UICONTROL Login]:** （[!DNL Naver] を除くすべての広告ネットワーク）アカウントへの API アクセスを有効にするためのログイン名または ID。

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** （[!DNL Microsoft Advertising] [!DNL oAuth] 対応および [!DNL Meta] と [!DNL Yandex] を除くすべてのネットワーク） [[!DNL OAuth]  認証プロトコル ](https://oauth.net/2/) を使用してログインを認証するためのアカウントのトークン。

**[!UICONTROL Login Details]: [!UICONTROL Password]:** （[!DNL Naver] を除くすべての広告ネットワーク） アカウントのパスワード。 [!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] および [!DNL Yandex] のパスワード対応アカウントの場合、このフィールドは必須です。 [!DNL oAuth] 対応アカウントの場合、このフィールドはオプションです。必要に応じてアカウントマネージャーがトークンを更新できるように、パスワードを暗号化および保存する際に使用します。

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** （[!DNL Yandex] アカウントのみ）使用する開発者アカウントのアクセスキー。

**[!UICONTROL Currency]:** 勘定に使用する通貨の省略形。 このフィールドは、新しい [!DNL Naver] アカウントで編集できます。 その他のすべての検索ネットワークでは、レコードを保存すると、広告ネットワークのアカウントに設定された通貨が値に自動的に入力されます。

**[!UICONTROL Landing Page Suffix]** （[!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的な URL の末尾に追加するパラメーター。ビジネスで追跡する必要のあるすべてのパラメーターを含めます。

例：`param1=value1&param2=value2`

Adobe Advertisingのクリックの追跡を使用するアカウントでは、アドネットワークのクリック識別子（[!DNL Microsoft Advertising] の場合は `msclkid`、Googleの場合は `gclid`）をサフィックスに含める必要があります。 Adobe Analytics統合を持つアカウントは、（`s_kwcid` で始まる） AMO ID パラメーターを使用する必要があります。 アカウントにサーバーサイド AMO ID 実装がある場合は、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、手動でここに追加する必要があります。 [ に必要なサフィックス形式  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)、および [ に必要なサフィックス形式  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) を参照してください。

>[!NOTE]
>
>* このフィールドは、[!UICONTROL Auto Upload] トラッキング設定によって更新されません。
>* 下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

**タイムゾーン：** （[!DNL Baidu] と [!DNL Yahoo! Display Network] を除くすべての広告ネットワーク）広告主のタイムゾーン。 新しい [!DNL Naver] アカウントの場合、このフィールドは編集可能でオプションです。 その他のすべての検索ネットワークでは、レコードを保存すると、広告主の検索、ソーシャル、Commerce アカウント用に設定されたタイムゾーンが、値に自動的に入力されます。

**ステータス：** 検索、ソーシャル、Commerce内のアカウントのステータス：

* *有効：* 検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオのキャンペーンの自動入札やキャンペーン予算をプッシュします。
* *無効：* 検索、ソーシャル、Commerceでは、アカウント上のすべてのアクティビティが停止します。 アカウントがアクティブな間に収集されたデータは引き続き保存されますが、キャンペーン管理のビューやレポートには、アカウントが一時停止された期間のデータは含まれません。 後でアカウントを再アクティブ化して、アカウントでのアクティビティを再開できます。

**トラッキングテンプレート** - （[!DNL Google Ads]、[!DNL Microsoft Advertising] および [!DNL Yahoo! Japan Ads] アカウントのみ。オプション）ランディングドメインのすべてのリダイレクトとトラッキングパラメーターを指定し、最終的/ランディングページの URL をパラメーターに埋め込む、アカウントのデフォルトのトラッキングテンプレート。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

* 最終的な URL を埋め込むには：

   * （[!DNL Google Ads] および [!DNL Microsoft Advertising] のみ）トラッキングテンプレートで最終的な URL を示すパラメーターのリストについては、（ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799) の「使用可能なトラッキングパラメーター」の節の（[!DNL Microsoft Advertising] のみ） [[!DNL Microsoft Advertising]  ドキュメント [[!DNL Google Ads]  または（[!DNL Google Ads] のみ） [!DNL ValueTrack] 「トラッキングテンプレートのみ」パラメーターを参照してください ](https://support.google.com/google-ads/answer/6305348)

   * （[!DNL Yahoo! Japan Ads] のみ） パラメーター `!{lpurl}` を使用して、ランディングページの URL を指定します。

* オプションで、URL パラメーターと、キャンペーンに定義されたカスタムパラメーターをアンパサンド（&amp;）で区切ったもの（`{lpurl}?matchtype={matchtype}&device={device}` など）を含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

* キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれている場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的にプレフィックス付けされます。

>[!NOTE]
>
>* [!DNL Google Ads] えば、並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 広告を承認用に再送信しなくても、アカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートを更新できます。

**[!UICONTROL Master Account ID]:** （[!DNL Microsoft Advertising] アカウントのみ） アカウントに関連付けられている代理店/管理アカウントの ID。

**[!UICONTROL MCC Account]:** （[!DNL Yandex] アカウントのみ。オプション）アカウントに関連付けられた代理店/管理アカウント。 既存の関連付けを削除するには、「[!UICONTROL No MCC Account]」を選択します。

**[!UICONTROL Application ID]:** （[!DNL Yandex] アカウントのみ） アカウントに使用する開発者トークン。 すべての [!DNL Yandex] アカウントで同じトークンが使用されます。

**[!UICONTROL Purse Campaign ID]:** （共有アカウント設定が無効の [!DNL Yandex] アカウントのみ。オプション） アカウント内のすべての広告キャンペーンの支払いに使用されるキャンペーンの数値 ID。

**[!UICONTROL Finance Token]:** （共有アカウント設定が無効の [!DNL Yandex] アカウントのみ。オプション）ポートフォリオの最適化に必要な場合に広告主のキャンペーン間でウォレットからお金を再割り当てするなど、財務関連の API 呼び出しに使用する開発者トークン。

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

**[!UICONTROL Track Product Group]:** （[!UICONTROL EF Redirect] のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid フォーマット** - （Adobe AdvertisingとAdobe Analyticsの統合を持ち、AMO ID （s_kwcid）がまだ移行されていない広告主用の既存の [!DNL Google Ads] アカウント）

このアカウントは、AMO ID トラッキングコードの従来の形式を使用しています。これにより、Adobe AdvertisingはAdobe Analyticsとアカウントに関するデータを共有できます。 [ 最新フォーマット ](/help/integrations/analytics/ids.md#amo-id-formats) には、キャンペーン ID と広告グループ ID のパラメーターが含まれています。これらは、Analytics のパフォーマンス最大化キャンペーンやドラフトおよび実験キャンペーンで、キャンペーンレベルと広告グループレベルで正確にレポートす [!DNL Google Ads] ために必要です。

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

このアカウントをキャンペーンレベルおよび広告グループレベルでレポートする必要がある場合は、[!UICONTROL Edit] （鉛筆）アイコンをクリックし、新しい形式に変更する **[!UICONTROL Migrate to new s_kwcid format]** をクリックします。 これらのキャンペーンタイプを含まないアカウントの場合、新しい形式への移行はオプションですが、お勧めします。

詳しい手順については、「[ アカウントの AMO ID トラッキングコードの更新  [!DNL Google Ads]  を参照してください ](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)。

**レポートスイート名** - （トークンによる EF リダイレクトのみ。Adobe AdvertisingとAdobe Analyticsの統合を持つ広告主。オプション）検索、ソーシャル、Commerceが広告ネットワークから収集する 1 つ以上の Analytics レポートスイート。これには、アカウントのエンティティ分類やクリックデータが含まれます。 この機能は、サポートされている広告ネットワークでのみ使用できます。

レポートスイートにデータを表示するには、（a） アカウントに対してサーバーサイド AMO ID 機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable tracking for SAINT feeds]」設定を有効にする必要があります。 さらに、検索、ソーシャル、Commerceからデータを受信するように広告主の Analytics アカウントを設定する必要があります。 詳しくは、Adobe担当営業または販売店にお問い合わせください。

>[!MORELIKETHIS]
>
>* [ 広告ネットワークアカウントについて ](ad-network-account-about.md)
>* [ マーチャントセンターアカウントの管理 ](merchant-account-manage.md)
>* [ アカウントの s_kwcid トラッキングコード  [!DNL Google Ads]  更新 ](update-amo-id-google.md)
