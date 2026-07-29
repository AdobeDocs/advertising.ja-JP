---
title: '[!DNL Google Ads] キャンペーン設定'
description: ' [!DNL Google Ads]  キャンペーンの設定を参照します。'
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: cec8bc6b2b092a7c9a0ffec2da79acceab91b98b
workflow-type: tm+mt
source-wordcount: 3057
ht-degree: 0%

---

# [!DNL Google Ads] キャンペーン設定

## \[ ページの先頭]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新規広告キャンペーンのデフォルトは&#x200B;*アクティブ*&#x200B;です。

## [!UICONTROL Basic Settings] タブ

*新しいキャンペーンのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign Type]:**&#x200B;広告を配置する場所、およびキャンペーンに含めることができる広告タイプ：

* *[!UICONTROL Search Network Only]:*&#x200B;検索ネットワークに広告が表示されます。検索ネットワークには、[!DNL Google]件の検索結果と、オプションで検索パートナーサイトが含まれます。 広告グループごとにキーワードを指定する必要があります。

* *[!UICONTROL Search with Display Select]:*&#x200B;検索ネットワーク （検索結果[!DNL Google]件、オプションで検索パートナーサイトを含む）に広告が表示され、ディスプレイネットワークサイトに広告が表示される可能性があります。 ディスプレイ ネットワークでは、[!DNL Google Ads]は、キャンペーンの入札戦略に関係なく、自動入札を使用して選択的に広告を表示します。 検索広告の場合は、各広告グループのキーワードを指定します。ディスプレイ広告の場合は、プレースメントを指定し、オプションで各広告グループのキーワードを指定します。

* *[!UICONTROL Shopping Network]:* [!DNL Google]が商品に基づいて自動的に生成する商品広告を表示します。これは、[!DNL Google Shopping]の[!DNL Google Merchant Center]、[!DNL Google]の検索結果の横にある領域（テキスト広告とは別）、および（オプションで）パートナーのweb サイトを検索します。 キャンペーンの各広告グループに対して、広告する製品グループを指定できます。

* *[!UICONTROL Display Network Only]:* ディスプレイ ネットワークに広告を表示します。 広告グループごとに、プレースメントを指定する必要があり、オプションでキーワードを指定できます。

* *[!UICONTROL Performance Max]:* [!DNL Google Ads]件のスマート入札を使用して、チャネルをまたいで広告のコンバージョンを表示および最適化します。 キャンペーン設定では、画像、ロゴ、見出し、説明、オプション動画、オーディエンスシグナルなど、1つ以上のアセットグループを指定する必要があります。 [!DNL Google Ads]は、チャネル （[!DNL YouTube]、[!DNL Gmail]、または[!DNL Search]など）に基づいて、アセットを自動的に組み合わせて広告を配信します。

  **メモ：**

  * 必要な設定のみが使用できます。 オプションの設定については、[!DNL Google Ads] エディターにログインしてください。

  * [!DNL Google Merchant Center]個の製品フィードへのリンクはサポートされていません。

  * リストグループのサポートは利用できません。 リスト グループのデータを管理および表示するには、[!DNL Google Ads] エディターにログインします。

## [!UICONTROL Campaign Details] タブ

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** （ショッピング キャンペーンを含め、検索ネットワークのみをターゲットとするキャンペーン）広告ネットワークの検索パートナーネットワークに広告が表示されます。 デフォルトでは、このオプションは&#x200B;*[!UICONTROL Off]*&#x200B;です。

**[!UICONTROL Audience Target Method]:** （既存の、読み取り専用のGmail キャンペーンのみ）次の操作を実行するかどうか：

* *[!UICONTROL Bid Only]:*&#x200B;他の広告グループレベルのターゲットを満たしている限り、ターゲットオーディエンスに関連付けられていないユーザーにも広告を表示します。 ただし、特定のオーディエンスに対して高い入札額を設定することで、広告が表示される可能性を高めることができます。

* *[!UICONTROL Target and Bid]*&#x200B;広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーにのみ広告を表示します。

**[!UICONTROL Contains EU Political Ads]:** （欧州連合（EU）のオーディエンスをターゲットとするキャンペーンに適用）キャンペーンに、EU規則2024/90に基づいて欧州連合で配信される広告の要件に従った政治的広告が含まれているかどうか：*[!UICONTROL No]*&#x200B;または&#x200B;*[!UICONTROL Yes]*。

## [!UICONTROL Budget Options] タブ

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** （オプション。必要なすべての設定を含み、広告グループのみを含むパフォーマンスの最大化および検索キャンペーンに適用されます） **[!UICONTROL Show Recommendation]**&#x200B;をクリックして、[!DNL Google Ads]が推奨する予算を表示します。 現在のところ、対象となるキーワードが4万個未満のキャンペーンのみです。

パフォーマンスの最大化および検索キャンペーンの場合、推奨事項には次の設定が必要です。

* 入札戦略の種類
* 最終URL
* アセットグループ

検索キャンペーンの場合、レコメンデーションには次の追加設定も必要です。

* 入札戦略目標
* 国
* 言語
* 含まれる場所または除外される場所
* キーワード

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Enhanced CPC]:*&#x200B;は非推奨です。 [!DNL Google Ads]は、2025年に既存の[拡張CPC入札戦略](https://support.google.com/google-ads/answer/2464964)を手動CPCに自動的に変更し始めました。

* *[!UICONTROL Manual CPC]* （デフォルト）: （パフォーマンスの最大キャンペーンでは使用できません） クリック単価（CPC）モデルを使用します。 オプションで、広告ネットワークがキャンペーンの入札額を変更できるようにすることができます。

  * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：これは、非推奨の「[!UICONTROL Enhanced CPC]」オプションを使用するのと同じです。 [!DNL Google Ads]は、2025年に既存の[拡張CPC入札戦略](https://support.google.com/google-ads/answer/2464964)を手動CPCに自動的に変更し始めました。

* *[!UICONTROL Maximize Clicks]:* （検索、表示、ショッピング キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが入札を最適化してクリック数を最大化します。 オプションで&#x200B;**[!UICONTROL Max CPC]** （クリック単価）を入力して、広告ネットワークがクリックごとに特定の金額を超えて支払わないようにします。 **注意：**&#x200B;この戦略を含むキャンペーンをポートフォリオに追加すると、入札はポートフォリオの目的ではなく、クリックの重みによって行われます。

* *[!UICONTROL Maximize Conversion Value]:* （Search, Performance Max, and smart shopping campaigns） Search, Social, &amp; Commerceではなく、広告ネットワークが入札を最適化し、コンバージョンの価値を最大化します。 オプションで&#x200B;**[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセントで入力します。 **注：**&#x200B;このオプションは、キャンペーンレベルまたは広告グループレベルの最適化を使用するポートフォリオのキャンペーンに使用しますが、キーワードレベルの最適化を使用するポートフォリオには使用しません。 キャンペーンまたは広告グループレベルの最適化を備えたポートフォリオでは、Search, Social, &amp; Commerceは、キャンペーンレベルまたは（利用可能な場合）広告グループレベルのTarget ROASを最適化します。

* *[!UICONTROL Maximize Conversions]:* （Search, Display, and Performance Max campaigns）検索、ソーシャル、Commerceではなく、広告ネットワークが入札を最適化してコンバージョンを最大化します。 必要に応じて、**[!UICONTROL Target CPA]** （獲得単価）と該当する&#x200B;**[!UICONTROL Portfolio]**&#x200B;入札戦略を入力します。 **注：**&#x200B;このオプションは、キャンペーンレベルまたは広告グループレベルの最適化を使用するポートフォリオのキャンペーンに使用しますが、キーワードレベルの最適化を使用するポートフォリオには使用しません。 キャンペーンまたは広告グループレベルの最適化を備えたポートフォリオでは、Search, Social, &amp; Commerceは、キャンペーンレベルまたは（利用可能な場合）広告グループレベルのTarget CPAを最適化します。

* *[!UICONTROL Target CPA]:* （ディスプレイのみのキャンペーン） Search, Social, &amp; Commerceではなく、広告ネットワークは、オプションの&#x200B;**[!UICONTROL Target CPA]** （獲得あたりのコスト）に基づいて入札を最適化します。これは、獲得（コンバージョン）に対して支払う30日間の平均金額です。 **注：** キャンペーンまたは広告グループレベルの最適化を伴うポートフォリオ内のキャンペーン （キーワードレベルの最適化を伴うポートフォリオは除く）。[!UICONTROL Weekly]または[!UICONTROL Google Target CPA]を除く任意の支出戦略を伴う。 キャンペーンまたは広告グループレベルの最適化を備えたポートフォリオでは、Search, Social, &amp; Commerceは、キャンペーンレベルまたは（利用可能な場合）広告グループレベルのTarget CPAを最適化します。

  平均順位とCPC入札データは、この入札戦略を持つキャンペーンでは利用できません。

* *[!UICONTROL Target Impression Share]:* （Search Campaigns） Search, Social, &amp; Commerceではなく、広告ネットワークが入札を最適化し、ターゲットのインプレッションのシェアと広告ポジションを達成します。 オプションで、**[!UICONTROL Target Impression Share]**&#x200B;をパーセント、**[!UICONTROL Target Ad Position]**&#x200B;および&#x200B;**[!UICONTROL Max CPC]** （クリック単価）として入力します。 **注：**&#x200B;このオプションは、ポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:* （ショッピング キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークは、パーセントで指定された指定された&#x200B;**[!UICONTROL Target ROAS]** （広告費用対効果）に基づいて入札を最適化します。 **注：**&#x200B;このオプションは、キャンペーンまたは広告グループレベルの最適化を伴うポートフォリオのキャンペーンに使用します（キーワードレベルの最適化を伴うポートフォリオは使用しません）。[!UICONTROL Weekly]または[!UICONTROL Google Target ROAS]を除く任意の支出戦略を伴います。 キャンペーンまたは広告グループレベルの最適化を備えたポートフォリオでは、Search, Social, &amp; Commerceは、キャンペーンレベルまたは（利用可能な場合）広告グループレベルのTarget ROASを最適化します。

  平均順位とCPC入札データは、この入札戦略を持つキャンペーンでは利用できません。

* *[!UICONTROL Viewable CPM]:* （既存、読み取り専用[!DNL Gmail] キャンペーンのみ）広告ネットワークは、Search、Social、およびCommerceではなく、表示可能と測定された広告にのみ入札します。 **注：**&#x200B;この戦略の最適化は、どのタイプのポートフォリオでもサポートされていません。

## [!UICONTROL Shopping Settings] タブ

**[!UICONTROL Sales Country]:** （ショッピング キャンペーンのみ。既存のキャンペーンの読み取り専用）
キャンペーンの商品が販売されています。 製品はターゲット国に関連付けられているため、この設定によって、キャンペーンで宣伝される製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** （ショッピングキャンペーンのみ。既に米国、英国、DE、FR、JP、AUの[!DNL Google Merchant Center]店舗でローカルショッピングプログラムに参加している広告主。オプション）により、[!DNL Google Ads]はGoogle.comでローカル在庫情報をショッピング広告に自動的に追加できます。

**ヒント：**&#x200B;この設定を使用する場合は、[!UICONTROL Inventory Filter]設定でローカル広告を除外しないでください。

**注：**&#x200B;のローカル在庫広告では、[!DNL Google Merchant Center]への2つの追加フィードが必要です。1つはローカル製品データで、もう1つはローカル製品の在庫で必要です。 [ ローカルショッピング広告](https://www.google.com/retail/local-inventory-ads/)について詳しくは、[!DNL Google Ads]のドキュメントを参照してください。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting] タブ

**[!UICONTROL Languages]:** （検索および表示ネットワークのみ）キャンペーン内の広告の1つ以上のターゲット言語。

[!DNL Google Ads]は、ユーザーの[!DNL Google]言語設定または検索クエリの言語、現在のページ、または[!DNL Google Display Network]で最近閲覧したページから、ユーザーの言語を決定します。

**[!UICONTROL Location Targets]:**&#x200B;特定のユーザーの地理的な場所をターゲットとして含めるか除外します。 デフォルトでは、すべての場所がターゲットになっています。 場所の任意の組み合わせでユーザーを含めることも除外することもできます。 除外は常にインクルージョンを上書きします。

* すべての場所をターゲットにするには、場所を選択しないでください。

* 特定の場所をターゲティングまたは除外するには：

  * （国、州、大都市圏、または都市） **[!UICONTROL Location Target]** （![場所ターゲット ](/help/search-social-commerce/assets/location-target.png "場所ターゲット ")）をクリックし、含める場所と除外する場所を見つけます。

    * 場所とその子の場所を含めるには、隣接する円を1回クリックして、青いチェックマーク（![含める](/help/search-social-commerce/assets/include.png "含める")）が表示されます。

    * 場所を除外するには、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されるように、隣接する円を2回クリックします。

    * 場所をサブコンポーネント（米国の州、都市圏、都市など）に展開するには、場所名をクリックします。

    * 場所を検索するには、入力フィールドに場所の最初の3文字を入力または貼り付けます。 検索結果で、含める場所の横にある&#x200B;**[!UICONTROL Include]**&#x200B;をクリックするか、除外する場所の横にある&#x200B;**[!UICONTROL Exclude]**&#x200B;をクリックします。

  * （アドレスの近くの場所、含まれるターゲットのみ）をクリックし、**[!UICONTROL Radius Target]** （![半径ターゲット ](/help/search-social-commerce/assets/radius-target.png "半径ターゲット ")）をクリックしてから、**[!UICONTROL Address]**&#x200B;をクリックします。 ターゲットとするアドレスの周りのアドレスと半径をマイルまたはキロメートル単位で入力し、**[!UICONTROL Add]**&#x200B;をクリックします。

  * （地理座標の近くの場所、含まれるターゲットのみ）をクリックし、**[!UICONTROL Radius Target]** （![半径ターゲット ](/help/search-social-commerce/assets/radius-target.png "半径ターゲット ")）をクリックしてから、**[!UICONTROL Coordinate]**&#x200B;をクリックします。 ターゲットとなる場所の緯度と経度と半径をマイルまたはキロメートル単位で入力し、**[!UICONTROL Add]**&#x200B;をクリックします。

* （含まれるターゲット場所の入札調整を追加するには）入札調整値を入力します。

* 0%：この場所の広告の入札額を調整しない。

* \[その他の値が–90%から300%\]の場合：この場所の広告の入札額を増減します。

**メモ：**

* Search, Social, &amp; Commerceでは、[!DNL Google Ads]が提供するサーファーの場所と場所ターゲットのマッピングに関するデータに制限があるため、次の場所ターゲットに対して自動調整された入札調整を提供していません。

  * 半径ターゲット：

  * [!DNL Google Ads]がサーファーのURLに親の場所を送信しない州/県/地域/県レベル以下の場所（空港や米国議会地区を含む）。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options] タブ

**[!UICONTROL Mobile Carriers]:** （表示ネットワークのみ）ターゲットにする特定のモバイル キャリアが並べ替えられます
国別。 何も選択しない場合は、すべてがターゲットになります。

**[!UICONTROL Mobile Carriers]:** （表示ネットワークのみ）ターゲットにする特定のオペレーティング システム。 何も選択しない場合は、すべてがターゲットになります。

## [!UICONTROL URL Options] タブ

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options] タブ

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL AI Max] タブ

検索ネットワークのみをターゲットとする&#x200B;*キャンペーン*

**[!UICONTROL AI Max]:** AIによる検索語句の一致、テキストのカスタマイズ、最終URLの拡張をキャンペーンで[[!UICONTROL AI Max]](https://support.google.com/google-ads/answer/15910366)を有効にするかどうか。 **[!UICONTROL AI Max]**&#x200B;を有効にすると、次の2つの追加の設定が使用できるようになります。

* **[!UICONTROL Text customization]:** [!DNL Google Ads]が生成AIを使用して、既存の広告とランディングページのコピーに基づいて広告コピー、見出し、説明をカスタマイズするかどうか。

* **[!UICONTROL Final URL expansion]:** [!DNL Google Ads]が検索意図に基づいて、web サイト上で最も関連性の高いランディングページにトラフィックをルーティングするかどうか。 この設定は、**[!UICONTROL Text customization]**&#x200B;が有効になっている場合にのみ使用できます。

<!-- Clarify why this is "Unspecified" and read-only for me as of 7/23. Also, shouldn't we reword this? -->

**[!UICONTROL Bundling required]:** （[!UICONTROL AI Max]機能が有効になっている既存のキャンペーンのみ。読み取り専用）キャンペーンのテキストのカスタマイズとブランドリストの制御を尊重または変更するために[!UICONTROL AI Max]を有効にする必要があるかどうか：*[!UICONTROL Required]*、*[!UICONTROL Not required]*、または&#x200B;*[!UICONTROL Unspecified]*。

<!-- Is this based on the advanced location options set elsewhere in Google Ads editor? -->

**[!UICONTROL Geo Targeting Type]:** （[!UICONTROL AI Max]機能を有効にした既存のキャンペーン、読み取り専用）キャンペーンの広告グループに[!UICONTROL Locations of Interest]個のターゲットが含まれている場合、ターゲットとなるユーザーの関心の種類は&#x200B;*[!UICONTROL Search Interest]* （指定された場所に興味があるユーザー）、*[!UICONTROL Presence]* （指定された場所にいるユーザー、定期的に興味があるユーザー）または&#x200B;*[!UICONTROL Presence or Interest]* （指定された場所にいるユーザー、定期的に興味があるユーザー）と表示されます。

## [!UICONTROL Additional Campaign Information] タブ

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

### [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** （[!UICONTROL EF Redirect]の場合のみ）リダイレクトを追加し、関連URLにパラメーターを追加して、クリックと収益を追跡するレベル：

* *[!UICONTROL Keyword]:* キーワードレベルでのみデータを追跡します。

* *[!UICONTROL Creative]:*&#x200B;広告（クリエイティブ）レベルでのみデータを追跡します。

* *[!UICONTROL Creative and Keyword]:*&#x200B;広告（クリエイティブ）レベルとキーワードレベルの両方でデータを追跡します。

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** アカウントまたはキャンペーンの広告にURL パラメーターを追加して、コンバージョンを追跡します。

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

**[!UICONTROL Track Product Group]:** （[!UICONTROL EF Redirect]のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

### [!UICONTROL Asset Groups] （アセットグループごと）

*パフォーマンス最大キャンペーンのみ*

**[!UICONTROL Asset Group Name]:** アセットグループの名前。 [!DNL Google Merchant Center]個の製品フィードへのリンクはサポートされていません。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。

**[!UICONTROL Final URL]:** アセットグループから作成されたすべての広告の最終URL。<!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and [!DNL Google Ads] replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:**&#x200B;広告の最大15枚の画像（少なくとも1枚の風景画像（1.91:1、少なくとも600 x 314 ピクセル）と少なくとも1枚の正方形の画像（1:1、少なくとも300 x 300 ピクセル）を含む）。 オプションで、ポートレート画像（4:5、少なくとも480 x 600 ピクセル）を含めることができます。 [[!DNL Google Ads] 画像の仕様](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications)を参照してください。 画像をアップロードするか、[!UICONTROL Asset Library]から選択できますが、両方を同じ操作で選択することはできません。

* 画像をアップロードするには：

  1. 「[!UICONTROL Upload from Device]」タブで「**[!UICONTROL +]**」をクリックし、デバイスまたはネットワークから画像を選択します。

  1. 各画像について：

     1. 縦横比を選択します。

     1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択し、可能な限り画像の表示可能部分のサイズを変更します。

     1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

        選択した縦横比ごとに1つのアセットが作成されます。

     1. **[!UICONTROL Proceed]**&#x200B;をクリックします。

  1. 画像の指定が完了したら、**[!UICONTROL Upload]**&#x200B;をクリックします。

* [!UICONTROL Asset Library]から画像を選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックして画像を選択します。

**[!UICONTROL Logos]:**&#x200B;少なくとも1つの正方形（1:1、少なくとも128 x 128 ピクセル）ロゴ。 オプションで、横（4:1、少なくとも512 x 218 ピクセル）のロゴを含めることができます。 ロゴは合計5つまで含めることができます。 [[!DNL Google Ads]  ロゴの仕様](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications)を参照してください。 画像をアップロードするか、[!UICONTROL Asset Library]から選択できますが、両方を同じ操作で選択することはできません。

* 画像をアップロードするには：

  1. 「[!UICONTROL Upload from Device]」タブで「**[!UICONTROL +]**」をクリックし、デバイスまたはネットワークから画像を選択します。

  1. 各画像について：

     1. 縦横比を選択します。

     1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択し、可能な限り画像の表示可能部分のサイズを変更します。

     1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

        選択した縦横比ごとに1つのアセットが作成されます。

     1. **[!UICONTROL Proceed]**&#x200B;をクリックします。

  1. 画像の指定が完了したら、**[!UICONTROL Upload]**&#x200B;をクリックします。

* [!UICONTROL Asset Library]から画像を選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックして画像を選択します。

**[!UICONTROL Videos]:** （オプション）少なくとも1つ、最大5つ、[!DNL YouTube]のビデオが10秒以上の長さです。 URLを入力するか、[!UICONTROL Asset Library]から選択できますが、両方を同じ操作で選択することはできません。

* URLを入力するには：

  1. 「[!UICONTROL Enter Video Url]」タブで、URLを入力します。

  1. （オプション）別のURLを追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、URLを入力します。

* [!UICONTROL Asset Library]からビデオを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてビデオを選択します。

**[!UICONTROL Headlines]:**&#x200B;少なくとも3つ、最大5つの短い見出し。各見出しは最大30文字です。 1つ以上の見出しは、15文字以下にする必要があります。 最終的なURL拡張を有効にするキャンペーンレベルのオプションが[!DNL Google Ads]以内に設定されている場合、[!DNL Google Ads]はこの値をランディングページのコンテンツに基づくカスタム見出しに置き換えます。

テキストを入力するか、[!UICONTROL Asset Library]からアセットを選択できますが、両方を同じ操作で選択することはできません。

* テキストを入力するには：

  1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

  1. （オプション）別のテキスト文字列を追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、文字列を入力します。

* [!UICONTROL Asset Library]からアセットを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてアセットを選択します。

**[!UICONTROL Long Headlines]:**&#x200B;少なくとも1つ、最大5つの長い見出し（各90文字まで）。 テキストを入力するか、[!UICONTROL Asset Library]からアセットを選択できますが、両方を同じ操作で選択することはできません。

* テキストを入力するには：

  1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

  1. （オプション）別のテキスト文字列を追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、文字列を入力します。

* [!UICONTROL Asset Library]からアセットを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてアセットを選択します。

**[!UICONTROL Descriptions]:**&#x200B;少なくとも2文字、最大4文字の説明で、各文字は最大90文字です。 1つ以上の説明は、30文字以下にする必要があります。 テキストを入力するか、[!UICONTROL Asset Library]からアセットを選択できますが、両方を同じ操作で選択することはできません。

* テキストを入力するには：

  1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

  1. （オプション）別のテキスト文字列を追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、文字列を入力します。

* [!UICONTROL Asset Library]からアセットを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてアセットを選択します。

**[!UICONTROL Call to Action]:**&#x200B;広告に含めるcall to action。 デフォルトでは、*[!UICONTROL Automated]*&#x200B;が選択され、[!DNL Google Ads]がcall to actionを選択します。 オプションで別のアクションを選択できます。

**[!UICONTROL Business Name]:** ビジネス名（最大25文字）。

**[!UICONTROL Audience Signal]:** （オプション） キャンペーンのオーディエンスシグナルとして使用する[!DNL Google Ads] オーディエンス。 [!DNL Google Ads]個のマシンラーニング モデルは、オーディエンスを使用して、ターゲットとする類似のweb サーファーを見つけます。また、シグナルとして指定されていないオーディエンスに広告を表示して、パフォーマンス目標を達成するのに役立てることもできます。 コンバージョンに至る可能性が最も高いオーディエンスを特定：

>[!NOTE]
>
>オーディエンスシグナルは、[ キャンペーンレベルおよび広告グループレベルのオーディエンスターゲット ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)とは異なります。

**[!UICONTROL Primary Status]:** （パフォーマンスの最大キャンペーンの既存のアセットグループの読み取り専用フィールド）アセットグループがフルキャパシティで提供されている、または提供されていない理由。 アセットグループのステータスだけでなく、ポリシーや品質の承認など、その他のシグナルも考慮されます。 値には、*実施要件、* *制限付き、* *非実施要件、* *一時停止、* *保留中、* *削除済み、* *不明、*&#x200B;または&#x200B;*未指定*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->&#x200B;が含まれます。

**[!UICONTROL Primary Status Reason]:** （パフォーマンスの最大キャンペーンの既存のアセットグループの読み取り専用フィールド） アセットグループのプライマリステータスに関する追加の詳細。 値には、*ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* *CAMPAIGN_ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* UNKNOWN,*または*&#x200B;未指定。**

### [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** *[!UICONTROL Use account conversion goals for this campaign]* （既定値）か&#x200B;*[!UICONTROL Use campaign specific conversion goals]*&#x200B;かのどちらかです。 キャンペーンのコンバージョン目標を指定する場合は、標準目標を選択するか、キャンペーンのカスタム目標を作成します。

目標は毎日同期されるため、過去24時間に作成された既存の目標は一覧表示されない場合があります。 リストを更新するには、[広告ネットワークデータを手動で同期します](/help/search-social-commerce/campaign-management/campaigns/sync-network.md)。

カスタムコンバージョン目標を作成するには、**[!UICONTROL + Add custom goal]**&#x200B;をクリックし、カスタム目標名を入力し、カスタム目標に含める[ コンバージョンアクション ](https://support.google.com/google-ads/answer/6032150)を選択して、**[!UICONTROL Save]**&#x200B;をクリックします。 **注：**&#x200B;各キャンペーンには、1つのカスタム目標のみを設定できます。

>[!TIP]
>
>キャンペーンがハイブリッドポートフォリオの一部である場合、ベストプラクティスは、ポートフォリオの目的のコンバージョン目標に一致するキャンペーンレベルの目標を使用することです。追加のコンバージョン目標を含めると、ポートフォリオのパフォーマンスに影響を与える可能性があります。
>
>ただし、[目標を広告ネットワーク ](/help/search-social-commerce/tools/objective-upload-to-networks.md)にアップロードするハイブリッドポートフォリオのキャンペーンの場合は、ここで代わりに広告ネットワークのエディター内で次の操作を行います。a）アップロードされた検索、ソーシャル、およびCommerce ポートフォリオの目標指標（「O_ACS_OBJ」で始まる）をキャンペーンのコンバージョンアクションとして追加し、b）広告目標を追跡した指標が目的を広告ネットワークにアップロードされないため、[!DNL Google]追跡コンバージョンが含含まれます。

### [!UICONTROL Set Customer Acquisition Goal]

新規顧客、既存顧客、またはその両方に合わせて施策を最適化します。 この設定を使用するには、まず[!DNL Google Ads] アカウントの新しい顧客獲得目標をアクティブ化するか、必要に応じてマネージャーアカウントをアクティブ化する必要があります。 目標は、コンバージョン設定で、対象となる既存の顧客リストと新規顧客の追加コンバージョン値を定義します。 [!DNL Google Ads]のヘルプ「[新しい顧客獲得目標をアクティブ化](https://support.google.com/google-ads/answer/14007601)」の手順1 ～ 2を参照してください。

**[!UICONTROL Customer Goal]:**&#x200B;顧客獲得の目標タイプ：

* *[!UICONTROL All Customers]* （既定値）：新規顧客と既存顧客の両方に均等に最適化します。

* *[!UICONTROL New Customers]:*&#x200B;新規顧客の獲得を優先します。 このオプションを選択すると、**[!UICONTROL New Customer Bid Adjustment]**&#x200B;設定が表示されます。

* *[!UICONTROL Existing Customers]:*&#x200B;既存顧客の維持を優先します。

**[!UICONTROL New Customer Bid Adjustment]:** （**[!UICONTROL Customer Goal]**&#x200B;が&#x200B;**[!UICONTROL New Customers]**&#x200B;のみに設定）新規顧客をターゲティングする際に、0.1から10.0までの入札額に適用される乗数。 デフォルトは1.0 （調整なし）です。 例えば、新規顧客の入札が1.5倍、新規顧客の入札が2.0倍、新規顧客の入札が0.5倍といった具合に、新規顧客の入札が50%削減されます。

>[!MORELIKETHIS]
>
>* [ キャンペーンの管理](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
