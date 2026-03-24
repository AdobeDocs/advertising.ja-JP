---
title: 広告ネットワーク アカウントの管理
description: 広告ネットワークアカウントのアカウント詳細を設定および管理する方法について説明します。
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '2100'
ht-degree: 0%

---

# 広告ネットワーク アカウントの管理

以下は、広告ネットワークアカウントの詳細の作成と編集、アカウントの[!DNL oAuth] トークンの更新、アカウントの無効化の手順です。

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

各広告ネットワークで使用できる機能について詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

新しいUIでの広告ネットワークアカウントの管理方法については、「[&#x200B; （新しいUI） API接続を介した広告ネットワークアカウントの管理](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)」を参照してください。

## 広告ネットワークアカウントの詳細の作成 {#create-account}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの同期または追跡を有効にするには、アカウントのアクセス資格情報と追跡オプションを含み、ステータスが&#x200B;*active*&#x200B;の対応するアカウントレコードを作成する必要があります。

>[!NOTE]
>
>* 新しい[!DNL Baidu] アカウントではサポートを利用できません。
>* 広告ネットワークで実際のアカウントを作成するには、広告ネットワークのweb サイトに移動します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. [&#x200B; アカウント設定](#account-settings)を指定します。

   1. 広告ネットワークの名前をクリックし、**[!UICONTROL Next]**&#x200B;をクリックします。

   1. 「**[!UICONTROL Account Details]**」セクションで、アカウントの詳細を入力します。

      ログイン認証タイプ「[!UICONTROL oAuth]」を使用するアドネットワークの場合、Search、Social、およびCommerceが[OAuth認証プロトコル &#x200B;](https://oauth.net/2/)を使用してアカウントにアクセスできるようにします。

      1. アカウントの&#x200B;**[!UICONTROL Login]**&#x200B;値を入力し、必要に応じてパスワードを入力し、**[!UICONTROL Authenticate]**&#x200B;をクリックします。

         ベストプラクティスは、アカウントへのAPI アクセスにログインを使用することです。 暗号化して保存する際にパスワードを入力し、Adobe アカウントチームが必要に応じてトークンを更新できるようにします。

      1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへのAPI アクセスに資格情報を使用することです。

      1. 権限/アクセスのリクエスト画面で、ボタンをクリックして権限を確認します。

      1. 開いたポップアップウィンドウで認証文字列をコピーし、その文字列を&#x200B;**[!UICONTROL oAuth Token]** フィールドに貼り付けます。

      1. 残りのアカウントの詳細を指定します。

   1. **[!UICONTROL Set Account Tracking]**&#x200B;をクリックし、トラッキング設定を入力します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

   アカウント内のすべてのキャンペーンの最近のコストとクリックデータは、Search, Social, &amp; Commerce内で約24時間で利用できます。 デフォルトでは、広告ネットワークに応じて、過去5～10日間データを利用できます。 ただし、必要に応じて、プロジェクト立ち上げチームは過去60日間までのデータを取得できます。

## 広告ネットワークアカウントの詳細を編集 {#edit-account}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

アカウントの資格情報が変更された場合、アカウント全体でデフォルトのトラッキングパラメーターを変更するか、アカウントのアクティビティを有効または無効にしてから、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークのweb サイトに移動します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. アカウント名の上にカーソルを置き、![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

1. [&#x200B; アカウント設定](#account-settings)を編集します。

   1. （オプション）アカウントの詳細を編集します。

   1. （オプション）「**[!UICONTROL Set Account Tracking]**」をクリックし、トラッキング設定を編集します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

   >[!NOTE]
   >
   >Search, Social, &amp; Commerceは、新しいアカウントデータを広告ネットワーク上のアカウントデータと同期させる必要があります。 Search, Social, &amp; Commerceによって広告ネットワーク上の変化が検出されると、1日に1回、またはそれ以上の頻度で自動的に行われます。

## 検索アカウントのoAuth アクセストークンを更新する {#refresh-oauth-tokens}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

Search, Social, &amp; Commerceが[OAuth認証プロトコル &#x200B;](https://oauth.net/2/)を使用してアカウントにアクセスし、アカウントの資格情報が変更された場合、またはSearch, Social, &amp; Commerceの新機能をサポートするために追加のアクセスが必要な場合は、アカウントの新しいアクセストークンを取得する必要があります。

Adobeのアカウントチームは、新機能に新しいトークンが必要な場合にお知らせします。

1. （同じブラウザーアプリケーションで同じ広告ネットワークの別のアカウントにログインしている場合）広告主以外のアカウントからログアウトします。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. アカウント名の上にカーソルを置き、![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

1. 新しいアクセストークンを取得します。

   1. **[!UICONTROL Get oAuth Token]**&#x200B;をクリックします。

   1. （広告主のアカウントにログインしていない場合）広告主の広告アカウントにログインします。 ベストプラクティスは、アカウントへのAPI アクセスに資格情報を使用することです。

   1. 権限/アクセスのリクエスト画面で、ボタンをクリックして権限を確認します。

   1. 開いたポップアップウィンドウで認証文字列をコピーし、その文字列を&#x200B;**[!UICONTROL oAuth Token]** フィールドに貼り付けます。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

広告ネットワークアカウントを有効にすると、Search, Social, &amp; Commerceは、キャンペーンデータをアカウントと（サポートされている場合）同期し、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。 広告ネットワークアカウントを無効にすると、Search、Social、およびCommerceは、アカウント上のすべてのアクティビティを停止します。 アカウントがアクティブな間に収集されたデータは引き続き保存されますが、キャンペーン管理ビューとレポートには、アカウントが無効になっている期間のデータは含まれません。 後でアカウントを再度有効にして、アカウントのアクティビティを再開できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （1つのアカウントのステータスを変更するには） アカウント名にカーソルを合わせ、![詳細](/help/search-social-commerce/assets/more-filters.png "詳細")をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。 **[!UICONTROL Status]**&#x200B;を&#x200B;*有効*&#x200B;または&#x200B;*無効*&#x200B;に変更し、**[!UICONTROL Post]**&#x200B;をクリックします。

   * （1つ以上のアカウントのステータスを変更するには）次の操作を行います。

      1. 各アカウントの横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. データテーブルの上にあるツールバーで、![&#x200B; アクティベーションアイコン &#x200B;](/help/search-social-commerce/assets/activate.png " アクティベーションアイコン ")をクリックしてアカウントを有効にするか、![無効にするアイコン](/help/search-social-commerce/assets/disable.png "無効にするアイコン")してアカウントを無効にします。

## 広告ネットワークアカウント設定 {#account-settings}

>[!NOTE]
>
>エージェンシーアカウントマネージャー、[!DNL Adobe] アカウントマネージャー、および管理者ユーザーのみがアカウント設定を構成できます。

### アカウント詳細

**[!UICONTROL SE Account ID]:** （[!DNL Naver]および[!DNL Yandex] アカウントを除くすべてのアカウント。新規アカウントのみ編集可能）広告ネットワークによって割り当てられたアカウント ID。

>[!NOTE]
>
>Ad network manager アカウントは、ここではサポートされていません。 [!DNL Microsoft Advertising]または[!DNL Yandex]のマネージャーアカウントを特定するには、「マスターアカウント ID」フィールドまたは「MCC アカウント」フィールドをそれぞれ使用します。 [&#x200B; マネージャーアカウント  [!DNL Google Ads] の資格情報を設定するには、](/help/search-social-commerce/admin/manager-accounts.md) \> [!UICONTROL Admin]に移動します。[!UICONTROL Manager Accounts]

**[!UICONTROL Account Name]:**&#x200B;検索、ソーシャル、およびCommerce内のアカウントに表示される名前。

>[!NOTE]
>
>Search、Social、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobe アカウントチームにマッピングを更新するように依頼します。

**[!UICONTROL Login Details]: \[Login Type\]** - （[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]のみ）次を使用してアカウントへのログインを許可するかどうか：

* *[!UICONTROL oAuth]* （デフォルト）: [[!DNL OAuth] 認証プロトコル &#x200B;](https://oauth.net/2/)を使用するには。

* *[!UICONTROL Password]:* クライアントのパスワードを使用します。

[!DNL Microsoft Advertising] アカウントの場合、[!DNL oAuth]個の承認済みログインのみを使用できます。

**[!UICONTROL Login Details]: [!UICONTROL Login]:** （[!DNL Naver]を除くすべての広告ネットワーク） アカウントへのAPI アクセスを有効にするログイン名またはID。

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** （[!DNL Microsoft Advertising] [!DNL oAuth]が有効で、[!DNL Meta]と[!DNL Yandex]を除くすべてのネットワーク） アカウントのトークンは、[[!DNL OAuth] 認証プロトコル &#x200B;](https://oauth.net/2/)を使用してログインを認証します。

**[!UICONTROL Login Details]: [!UICONTROL Password]:** （[!DNL Naver]を除くすべての広告ネットワーク） アカウントのパスワード。 [!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]のパスワードが有効なアカウントの場合、このフィールドは必須です。 [!DNL oAuth]が有効なアカウントの場合、このフィールドはオプションです。アカウントマネージャーが必要に応じてトークンを更新できるように、パスワードを暗号化して保存する場合に使用します。

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** （[!DNL Yandex] アカウントのみ）使用する開発者アカウントのアクセスキー。

**[!UICONTROL Currency]:** アカウントに使用される通貨の略語。 このフィールドは、新しい[!DNL Naver] アカウントに対して編集できます。 その他のすべての検索ネットワークでは、レコードを保存すると、広告ネットワーク上のアカウントに設定された通貨で値が自動的に入力されます。

**[!UICONTROL Landing Page Suffix]** （[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ。オプション）情報を追跡するために最終的なURLの末尾に追加するパラメーター。企業が追跡する必要があるすべてのパラメーターを含めます。

例：`param1=value1&param2=value2`

Adobe Advertising クリック トラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック ID （`msclkid`の[!DNL Microsoft Advertising]; Googleの`gclid`）を含める必要があります。 Adobe Analyticsとの統合を持つアカウントでは、AMO ID パラメーター（`s_kwcid`で始まる）を使用する必要があります。 アカウントにサーバーサイド AMO ID実装がある場合、ユーザーが広告をクリックするとパラメーターが自動的に追加されます。それ以外の場合は、ここで手動で追加する必要があります。 [の [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必要なサフィックス形式と[の [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必要なサフィックス形式を参照してください。

>[!NOTE]
>
>* このフィールドは、[!UICONTROL Auto Upload] トラッキング設定で更新されません。
>* 下位レベルの最終URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

**タイムゾーン：** （[!DNL Baidu]と[!DNL Yahoo! Display Network]を除くすべての広告ネットワーク）広告主のタイムゾーン。 このフィールドは、新しい[!DNL Naver] アカウントに対して編集可能でオプションです。 その他のすべての検索ネットワークでは、レコードを保存すると、広告主のSearch, Social, &amp; Commerce アカウント用に設定されたタイムゾーンで値が自動的に入力されます。

**ステータス：** Search, Social, &amp; Commerce内のアカウントステータス：

* *有効：*&#x200B;検索、ソーシャル、およびCommerceは、キャンペーンデータをアカウントと（サポートされている場合）同期し、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。
* *無効：*&#x200B;検索、ソーシャル、およびCommerceは、アカウントのすべてのアクティビティを停止します。 アカウントがアクティブであった間に収集されたデータは引き続き保存されますが、キャンペーン管理ビューとレポートには、アカウントが一時停止された期間のデータは含まれません。 後でアカウントを再アクティブ化して、アカウントのアクティビティを再開できます。

**トラッキングテンプレート** - （[!DNL Google Ads]、[!DNL Microsoft Advertising]、および[!DNL Yahoo! Japan Ads] アカウントのみ。オプション）アカウントのデフォルトのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最後のページ URLもパラメーターに埋め込みます。 例：リダイレクトを含める`{lpurl}?source={network}&id=5`または`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`。

* 最終的なURLを埋め込むには：

   * （[!DNL Google Ads]および[!DNL Microsoft Advertising]のみ）トラッキングテンプレートの最終的なURLを示すパラメーターのリストについては、[!DNL Microsoft Advertising] ドキュメント [[!DNL Microsoft Advertising] の「使用可能な](https://help.ads.microsoft.com/#apex/3/en/56799) パラメーター」の節の「トラッキングテンプレートのみ」パラメーター（[!DNL Google Ads]のみ） [!DNL ValueTrack] ドキュメント [[!DNL Google Ads] または（](https://support.google.com/google-ads/answer/6305348)のみ）を参照してください。

   * （[!DNL Yahoo! Japan Ads]のみ） パラメーター`!{lpurl}`を使用して、ランディングページ URLを示します。

* 必要に応じて、URL パラメーターと、キャンペーン用に定義された任意のカスタムパラメーターを、アンパサンド（&amp;）で区切って含めることができます（`{lpurl}?matchtype={matchtype}&device={device}`）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

* キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合、レコードを保存すると、Search、Social、およびCommerceに独自のリダイレクトコードとトラッキングコードが自動的にプレフィックスされます。

>[!NOTE]
>
>* [!DNL Google Ads]の場合、並列追跡を有効にするソースからのクリックに代わらないマクロの使用を避けてください。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームは、カスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。
>* 最も詳細なレベルのトラッキングテンプレートは、より高いレベルのすべての値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンク、またはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 承認のために広告を再送信することなく、アカウントレベル、キャンペーンレベル、広告グループレベルでトラッキングテンプレートを更新できます。

**[!UICONTROL Master Account ID]:** （[!DNL Microsoft Advertising] アカウントのみ） アカウントに関連付けられている代理店/管理アカウントのID。

**[!UICONTROL MCC Account]:** （[!DNL Yandex] アカウントのみ。オプション）アカウントに関連付けられている代理店/管理アカウント。 既存の関連付けを削除するには、「[!UICONTROL No MCC Account]」を選択します。

**[!UICONTROL Application ID]:** （[!DNL Yandex] アカウントのみ） アカウントに使用する開発者トークン。 同じトークンがすべての[!DNL Yandex] アカウントに使用されます。

**[!UICONTROL Purse Campaign ID]:** （[!DNL Yandex] アカウント （共有アカウント設定が無効になっているアカウントのみ、オプション）アカウント内のすべての広告キャンペーンの支払いに使用されるキャンペーンの数値ID。

**[!UICONTROL Finance Token]:** （[!DNL Yandex] アカウントで、共有アカウント設定が無効になっている場合のみ、オプション）金融関連のAPI呼び出しに使用する開発者トークン。例えば、ポートフォリオの最適化に必要に応じて、広告主のキャンペーン間でウォレットから資金を再配分する場合などに使用します。

### アカウントの追跡

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

**[!UICONTROL Track Product Group]:** （[!UICONTROL EF Redirect]のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid形式：** （Adobe AdvertisingとAdobe Analyticsの統合を持ち、AMO ID （s_kwcid）がまだ移行されていない広告主向けの既存の[!DNL Google Ads] アカウント）

このアカウントは、AMO ID トラッキングコードの従来のフォーマットを使用しています。これにより、Adobe Advertisingはアカウントに関するデータをAdobe Analyticsと共有できます。 [最新の形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)には、キャンペーン IDと広告グループ IDのパラメーターが含まれています。これらは、[!DNL Google Ads]件のパフォーマンスの最大キャンペーン、ドラフト、およびAnalyticsの実験キャンペーンについて、キャンペーンおよび広告グループ レベルで正確にレポートするために必要です。

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

このアカウントをキャンペーンおよび広告グループのレベルで報告する必要がある場合は、[!UICONTROL Edit] （鉛筆）アイコンをクリックし、**[!UICONTROL Migrate to new s_kwcid format]**&#x200B;をクリックして新しい形式に変更します。 これらのキャンペーンタイプを含まないアカウントの場合、新しい形式への移行はオプションですが、推奨されます。

詳細な手順については、「[&#x200B; アカウント  [!DNL Google Ads] のAMO ID トラッキングコードの更新](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)」を参照してください。

**レポートスイート名：** （EF リダイレクトとトークンの場合のみ、Adobe AdvertisingとAdobe Analyticsの統合を持つ広告主、オプション） Search, Social, &amp; Commerceが広告ネットワークから収集したデータを送信する1つ以上のAnalytics レポートスイート（エンティティの分類やアカウントのクリックデータを含む）。 この機能は、サポートされている広告ネットワークでのみ使用できます。

レポートスイートにデータを表示するには、（a）アカウントにサーバーサイド AMO ID機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、広告主のAnalytics アカウントは、Search、Social、およびCommerceからデータを受信するように設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントについて](ad-network-account-about.md)
>* [&#x200B; マーチャント センターのアカウントの管理](merchant-account-manage.md)
>* [&#x200B; アカウント  [!DNL Google Ads] のs_kwcid トラッキングコードを更新します](update-amo-id-google.md)
