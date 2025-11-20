---
title: '[!DNL Google Ads] キャンペーンの設定'
description: キャンペーンの設定  [!DNL Google Ads]  参照します。
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 21dc29e97915712053bbcc39d8141693c1dbf8bf
workflow-type: tm+mt
source-wordcount: '2583'
ht-degree: 0%

---

# [!DNL Google Ads] キャンペーンの設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーンの作成時にのみ使用可能）広告の配置場所と、キャンペーンに含まれる可能性のある広告タイプは次のとおりです。

* *[!UICONTROL Search Network Only]:* 検索ネットワーク上の広告を表示します。この広告には、検索結果と、オプションで検索パートナーサイト [!DNL Google] 含まれます。 各広告グループにキーワードを指定する必要があります。

* *[!UICONTROL Search with Display Select]:* 検索ネットワーク上の広告を表示し（検索結果 [!DNL Google] 表示し、必要に応じて検索パートナーサイトも表示）、表示ネットワークサイト上の広告を表示する場合があります。 ディスプレイネットワークで [!DNL Google Ads]、キャンペーンの入札戦略に関係なく、自動入札を使用して広告を選択的に表示します。 検索広告の場合は、広告グループごとにキーワードを指定します。表示広告の場合は、プレースメントを指定し、オプションで広告グループごとにキーワードを指定します。

* *[!UICONTROL Shopping Network]:* 製品に基づいて [!DNL Google] が自動的に生成する製品広告を表示します。[!DNL Google Merchant Center] on [!DNL Google Shopping]、検索結果の横にある領域（テキスト広告とは別）、（オプションで）検索パートナー web サイト [!DNL Google] 表示します。 キャンペーンの広告グループごとに、広告する製品グループを指定できます。

* *[!UICONTROL Display Network Only]:* ディスプレイネットワーク上の広告を表示します。 広告グループごとに、プレースメントを指定する必要があり、オプションでキーワードを指定することもできます。

* *[!UICONTROL Performance Max]:* スマート入札を使用して、チャネルをまたいで広告のコンバージョンを表示および最適化 [!DNL Google Ads] ます。 キャンペーン設定内で、1 つ以上のアセットグループ（画像、ロゴ、ヘッドライン、説明、オプションビデオ、オーディエンスシグナルを含む）を指定する必要があります。 [!DNL Google Ads] では、アセットを自動的に組み合わせ、チャネル（[!DNL YouTube]、[!DNL Gmail]、[!DNL Search] など）に基づいて広告を提供します。

  **注：**

   * 必要な設定のみ使用できます。 オプション設定の場合は、[!DNL Google Ads] エディターにログインします。

   * [!DNL Google Merchant Center] 製品フィードへのリンクはサポートされていません。

   * グループの一覧表示はサポートされていません。 グループをリストするデータを管理および表示するには、[!DNL Google Ads] エディターにログインします。

   * ハイブリッド最適化がサポートされています。 入札戦略のターゲットとキャンペーンの予算は、キャンペーンレベルで設定します。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:** （既存の読み取り専用 Gmail キャンペーンのみ）次のどちらを実行するか：

* *[!UICONTROL Target and Bid]* ターゲットオーディエンスに関連付けられているユーザーで、その広告グループの他のターゲットも満たしているユーザーにのみ広告を表示します。

* *[!UICONTROL Bid Only]:* 他の広告グループレベルのターゲットを満たす限り、ターゲットオーディエンスに関連付けられていない人物にも広告を表示する場合。 ただし、特定のオーディエンスに対してより高い入札を設定すると、それらのオーディエンスに広告が表示される可能性が高くなります。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ* または *一時停止*。 新しい広告キャンペーンのデフォルトは *アクティブ* です。

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** （検索ネットワークをターゲットとするキャンペーンで、ショッピングキャンペーンを含む）広告ネットワークの検索パートナーネットワークの広告を表示します。 デフォルトでは、このオプションは *[!UICONTROL Off]* です。

**[!UICONTROL AI Max Enabled]:** （検索ネットワークをターゲットにするキャンペーンのみ。読み取り専用） [[!UICONTROL AI Max] 機能が有効になっているかどうか &#x200B;](https://support.google.com/google-ads/answer/15910366)*[!UICONTROL On]* または *[!UICONTROL Off]*。

**[!UICONTROL AI Max Bundling]:** （検索ネットワークをターゲットとするキャンペーンのみ、AI MAX 機能が有効になっているキャンペーン、読み取り専用） バンドルが必要かどうか（*[!UICONTROL Not Required]*、*[!UICONTROL Required]*、*[!UICONTROL Unknown]*、*[!UICONTROL Unspecified]*）。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** （オプション。すべての必須設定を使用し、広告グループのみを含むパフォーマンス最大化キャンペーンと検索キャンペーンに適用） **[!UICONTROL Show Recommendation]** をクリックして、[!DNL Google Ads] が推奨する予算を表示します。 現在、40,000 未満のキーワードを持つキャンペーンのみが実施要件を満たします。

パフォーマンス最大化キャンペーンおよび検索キャンペーンの場合、レコメンデーションに次の設定が必要です。

* 入札戦略タイプ
* 最終 URL
* アセットグループ

検索キャンペーンの場合、レコメンデーションには次の追加設定も必要です。

* 入札戦略のターゲット
* 国
* language
* 含まれる、または除外される場所
* キーワード

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Enhanced CPC]:* 非推奨（廃止予定）。 2025 年 3 月 15 日（PT） [!DNL Google Ads]、既存の [&#x200B; 拡張 CPC 入札戦略 &#x200B;](https://support.google.com/google-ads/answer/2464964) を手動 CPC に自動的に変更し始めました。

* *[!UICONTROL Manual CPC]* （デフォルト）: （Performance MAX キャンペーンでは使用できません）クリック単価（CPC）モデルを使用します。 オプションで、広告ネットワークにキャンペーンの入札の変更を許可できます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：これは、非推奨の「[!UICONTROL Enhanced CPC]」オプションを使用する場合と同じです。 2025 年 3 月 15 日（PT） [!DNL Google Ads]、既存の [&#x200B; 拡張 CPC 入札戦略 &#x200B;](https://support.google.com/google-ads/answer/2464964) を手動 CPC に自動的に変更し始めました。

* *[!UICONTROL Maximize Clicks]:* （検索、ディスプレイ、ショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、クリック数を最大化するように入札を最適化します。 必要に応じて、**[!UICONTROL Max CPC]** （クリック単価）を入力し、広告ネットワークがクリックごとに特定の金額以上を支払わないようにします。 **注意：** この戦略を使用してキャンペーンをポートフォリオに追加すると、入札はポートフォリオの目的ではなく、クリックの重み付けで行われます。

* *[!UICONTROL Maximize Conversion Value]:* （検索、パフォーマンス最大化、スマートショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、コンバージョン値を最大化するように入札を最適化します。 必要に応じて、**[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセンテージで入力します。 **メモ：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceを使用すると、キャンペーンレベルまたは（利用可能な場合は）広告グループレベルの Target ROAS を最適化できます。

* *[!UICONTROL Maximize Conversions]:* （検索、表示、Performance MAX キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、コンバージョンを最大化するように入札を最適化します。 必要に応じて、**[!UICONTROL Target CPA]** （取得原価）を入力します。 **メモ：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceを使用すると、キャンペーンレベルまたは（利用可能な場合は）広告グループレベルの Target CPA を最適化できます。

* *[!UICONTROL Target CPA]:* （ディスプレイキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークは、オプションの **[!UICONTROL Target CPA]** （獲得 1 件あたりのコスト）に基づいて入札を最適化します。これは、獲得（コンバージョン）に対して支払う 30 日間の平均額です。 **メモ：** このオプションは、[!UICONTROL Weekly] または [!UICONTROL Google Target CPA] を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceを使用すると、キャンペーンレベルまたは（利用可能な場合は）広告グループレベルの Target CPA を最適化できます。

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

* *[!UICONTROL Target Impression Share]:* （検索キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、目標インプレッションシェアと広告掲載順位を達成するように入札を最適化します。 必要に応じて、**[!UICONTROL Target Impression Share]** をパーセント、**[!UICONTROL Target Ad Position]** および **[!UICONTROL Max CPC]** （クリック単価）で入力します。 **メモ：** このオプションは、ポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:* （ディスプレイおよびショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークは、指定された **[!UICONTROL Target ROAS]** （広告費用対効果）に基づいて割合として入札を最適化します。 **メモ：** このオプションは、[!UICONTROL Weekly] または [!UICONTROL Google Target ROAS] を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceを使用すると、キャンペーンレベルまたは（利用可能な場合は）広告グループレベルの Target ROAS を最適化できます。

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

* *[!UICONTROL Viewable CPM]:* （既存の読み取り専用 [!DNL Gmail] キャンペーンのみ）広告ネットワーク（検索、ソーシャル、Commerceは除く）は、ビューアブルとして測定された広告にのみ入札します。 **メモ：この戦略の** 最適化は、どのタイプのポートフォリオでもサポートされていません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）次の国
キャンペーンの商品は販売されています。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** （ショッピングキャンペーンのみ。米国、英国、DE、FR、JP、AU の [!DNL Google Merchant Center] 店舗を使用したローカルショッピングプログラムに既に参加している広告主。オプション） Google.comで、ローカルの在庫情報をショッピング広告に自動的に追加で [!DNL Google Ads] ます。

**ヒント：** この設定を使用する場合は、[!UICONTROL Inventory Filter] 設定でローカル広告を除外しないでください。

**メモ：** ローカルの在庫広告には、[!DNL Google Merchant Center] ーザーに追加のフィードが 2 つ必要です。1 つはローカルの製品データを含むフィード、もう 1 つはローカルの製品インベントリを含むフィードです。 [!DNL Google Ads] ローカルショッピング広告 [&#x200B; について詳しくは、](https://www.google.com/retail/local-inventory-ads/) のドキュメントを参照してください。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** （ネットワークの検索と表示のみ） キャンペーンの広告の 1 つ以上のターゲット言語。

ユーザーの言語 [!DNL Google Ads]、ユーザーの [!DNL Google] 言語設定または検索クエリの言語、現在のページ、[!DNL Google Display Network] ージ上で最近閲覧されたページなどから特定されます。

**[!UICONTROL Location Targets]:** ターゲットとして含めるか除外する特定のユーザー地理的ロケーション。 デフォルトでは、すべての場所がターゲットになります。 任意の場所の組み合わせにユーザーを含めたり、除外したりできます。 除外は、常に包含を上書きします。

* すべての場所を対象にするには、どの場所も選択しないでください。

* 特定の場所をターゲットまたは除外するには：

   * （国、州、大都市圏、都市） **[!UICONTROL Location Target]** ージ（![Location Target](/help/search-social-commerce/assets/location-target.png "Location Target")）をクリックし、含めて除外する場所を探します。

      * 場所とその子場所を含めるには、隣の円を 1 回クリックすると、青いチェックマーク（![&#x200B; 含める &#x200B;](/help/search-social-commerce/assets/include.png " 含める ")）が表示されます。

      * 場所を除外するには、隣接する円を 2 回クリックして、赤いチェックマーク（![&#x200B; 除外 &#x200B;](/help/search-social-commerce/assets/exclude.png " 除外 ")）を表示します。

      * 場所をサブコンポーネント（米国の州、大都市圏、都市など）に展開するには、場所名をクリックします。

      * 場所を検索するには、入力フィールドに場所の最初の 3 文字以上を入力するか貼り付けます。 検索結果で、含める場所の横にある **[!UICONTROL Include]** をクリックするか、除外する場所の横に **[!UICONTROL Exclude]** をクリックします。

   * （アドレスの近くの場所。含まれるターゲットのみ） **[!UICONTROL Radius Target]** （![Radius Target](/help/search-social-commerce/assets/radius-target.png "Radius Target")）をクリックし、「**[!UICONTROL Address]**」をクリックします。 ターゲットとするアドレスとその周囲の半径（マイルまたはキロメートル）を入力し、[**[!UICONTROL Add]**] をクリックします。

   * （地理的座標の近くの位置。含まれるターゲットのみ） [**[!UICONTROL Radius Target]**] （![&#x200B; 半径ターゲット &#x200B;](/help/search-social-commerce/assets/radius-target.png " 半径ターゲット ")）をクリックし、[**[!UICONTROL Coordinate]**] をクリックします。 ターゲットとする位置の周りの緯度と経度、および半径をマイルまたはキロメートル単位で入力し、[**[!UICONTROL Add]**] をクリックします。

* （組み込み対象事業所に対する入札調整を追加する手順は、次のとおりです）入札調整値を入力します。

* 0%：この場所の広告の入札を調整しません。

* \[Other values from -90% to 300%\]：この場所の広告の入札額を増減させます。

**メモ：**

* 検索、ソーシャル、Commerceでは、サーファーの場所を場所の目標にマッピングするためのデータに制限があるため、次の場所の目標に対して自動調整された入札調整を提供しませ [!DNL Google Ads]。

   * 半径ターゲット。

   * [!DNL Google Ads] がサーファーの URL で親の場所を送信しない州/都道府県/地域/郡/県レベル以下の一部の場所（空港や米国議会選挙区など）。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** （ディスプレイネットワークのみ）ターゲットとする特定の携帯電話会社。通信会社は並べ替えられます
国別。 何も選択しない場合は、すべてがターゲットになります。

**[!UICONTROL Mobile Carriers]:** （ネットワークを表示のみ）ターゲットとする特定のオペレーティングシステム。 何も選択しない場合は、すべてがターゲットになります。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]:** （Performance max および検索キャンペーンのみ）新規顧客および既存顧客に入札を割り当てる方法：

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **メモ：** この設定を使用するには、まず [!DNL Google Ads] アカウント、または該当する場合は管理者アカウントの新規顧客獲得目標をアクティブにする必要があります。 目標では、適格な既存顧客リストと、コンバージョン設定の新規顧客に対する追加のコンバージョン値を定義します。 [!DNL Google Ads] ヘルプの手順 1 ～ 2 の「[&#x200B; 新規顧客獲得目標をアクティベートする &#x200B;](https://support.google.com/google-ads/answer/14007601) を参照してください。

* *[!UICONTROL Only bid for new customers]*

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

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

## [!UICONTROL Asset Groups] （アセットグループあたり）

**[!UICONTROL Asset Group Name]:** アセットグループの名前。 [!DNL Google Merchant Center] 製品フィードへのリンクはサポートされていません。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス：*[!UICONTROL Active]* または *[!UICONTROL Paused]*。

**[!UICONTROL Final URL]:** アセットグループから作成されたすべての広告の最終的な URL。<!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** 広告の画像（最大 15 個）。次のサイズを含みます。1） 3 つ以上の正方形画像、2） 3 つ以上の横長画像、および 3） 1 つ以上の縦長画像。 [[!DNL Google Ads]  画像仕様 &#x200B;](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications) を参照してください。 画像は、アップロードすることも、[!UICONTROL Asset Library] ージから選択することもできます。ただし、同じ操作で両方を選択することはできません。

* 画像をアップロードするには：

   1. [[!UICONTROL Upload from Device]] タブで [**[!UICONTROL +]**] をクリックし、デバイスまたはネットワークからイメージを選択します。

   1. 各画像に対して、次の手順を実行します。

      1. アスペクト比を選択します。

      1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択します。また、可能な場合は、画像の表示可能部分のサイズを必要に応じて変更します。

      1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

         選択した縦横比ごとに 1 つのアセットが作成されます。

      1. 「**[!UICONTROL Proceed]**」をクリックします。

   1. 画像の指定が終了したら、「**[!UICONTROL Upload]**」をクリックします。

* [!UICONTROL Asset Library] ージから画像を選択するには、「**[!UICONTROL Asset Library]**」をクリックして画像を選択します。

**[!UICONTROL Logos]:** 少なくとも 1 つの正方形（1:1）のロゴと 1 つの横（4:1）のロゴ。 各サイズを最大 5 つ含めることができます。 [[!DNL Google Ads]  ロゴの仕様 &#x200B;](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications) を参照してください。 画像は、アップロードすることも、[!UICONTROL Asset Library] ージから選択することもできます。ただし、同じ操作で両方を選択することはできません。

* 画像をアップロードするには：

   1. [[!UICONTROL Upload from Device]] タブで [**[!UICONTROL +]**] をクリックし、デバイスまたはネットワークからイメージを選択します。

   1. 各画像に対して、次の手順を実行します。

      1. アスペクト比を選択します。

      1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択します。また、可能な場合は、画像の表示可能部分のサイズを必要に応じて変更します。

      1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

         選択した縦横比ごとに 1 つのアセットが作成されます。

      1. 「**[!UICONTROL Proceed]**」をクリックします。

   1. 画像の指定が終了したら、「**[!UICONTROL Upload]**」をクリックします。

* [!UICONTROL Asset Library] ージから画像を選択するには、「**[!UICONTROL Asset Library]**」をクリックして画像を選択します。

**[!UICONTROL Videos]:** （オプション） 10 秒以上の長さのビデオ [!DNL YouTube] 少なくとも 1 つ、最大 5 つ。 URL を入力するか、[!UICONTROL Asset Library] ージから選択できますが、同じ操作で両方を選択することはできません。

* URL を入力するには：

   1. 「[!UICONTROL Enter Video Url]」タブで、URL を入力します。

   1. （任意）別の URL を追加するには、「**[!UICONTROL + Add]**」をクリックして URL を入力します。

* [!UICONTROL Asset Library] ージからビデオを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてビデオを選択します。

**[!UICONTROL Headlines]:** 少なくとも 3 つの短い見出し（最大 5 つまで）。各見出しは最大 30 文字です。 少なくとも 1 つのヘッドラインは 15 文字以下である必要があります。 最終的な URL 拡張を有効にするキャンペーンレベルのオプションが [!DNL Google Ads] 内に設定されている場合、[!DNL Google Ads] はこの値を、ランディングページのコンテンツに基づくカスタムのヘッドラインに置き換えます。

テキストを入力するか、[!UICONTROL Asset Library] ージからアセットを選択できますが、同じ操作で両方を選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、「**[!UICONTROL + Add]**」をクリックして文字列を入力します。

* [!UICONTROL Asset Library] ージからアセットを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてアセットを選択します。

**[!UICONTROL Long Headlines]:** 少なくとも 1 つ、最大 5 つの長い見出し（それぞれ最大 90 文字）。 テキストを入力するか、[!UICONTROL Asset Library] ージからアセットを選択できますが、同じ操作で両方を選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、「**[!UICONTROL + Add]**」をクリックして文字列を入力します。

* [!UICONTROL Asset Library] ージからアセットを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてアセットを選択します。

**[!UICONTROL Descriptions]:** 少なくとも 2 つ、最大 4 つの説明（それぞれ最大 90 文字）。 少なくとも 1 つの説明は、30 文字以下にする必要があります。 テキストを入力するか、[!UICONTROL Asset Library] ージからアセットを選択できますが、同じ操作で両方を選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、「**[!UICONTROL + Add]**」をクリックして文字列を入力します。

* [!UICONTROL Asset Library] ージからアセットを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてアセットを選択します。

**[!UICONTROL Call to Action]:** 広告に含めるcall to action。 デフォルトでは *[!UICONTROL Automated]* が選択されており、[!DNL Google Ads] はcall to actionを選択します。 オプションで、別のアクションを選択できます。

**[!UICONTROL Business Name]:** ビジネス名（最大 25 文字）。

**[!UICONTROL Audience Signal]:** （任意）キャンペーンのオーディエンスシグナルとして使用するオーディエンスを [!DNL Google Ads] 定します。 機械学習モデル [!DNL Google Ads]、オーディエンスを使用して、ターゲットとする類似の web サーファーを見つけます。また、パフォーマンス目標を達成するのに役立つシグナルとして指定されていないオーディエンスに広告を表示することもあります。 コンバージョンする可能性が最も高いオーディエンスを選択します。

>[!NOTE]
>オーディエンスシグナルは、[&#x200B; キャンペーンレベルと広告グループレベルのオーディエンスターゲット &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) とは異なります。

**[!UICONTROL Primary Status]:** （Performance MAX キャンペーンの既存のアセットグループの読み取り専用フィールド）アセットグループがフルキャパシティで提供されている、または提供されていない理由。 アセットグループのステータスに加え、ポリシーや品質の承認などの他のシグナルも考慮されます。 値には、*ELIGIBLE、**LIMITED、**&#x200B;NOT_ELIGIBLE、**PAUSED、**&#x200B;PENDING、**REMOVED、**&#x200B;UNKNOWN、**UNSPECIFIED*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. --> などがあります。

**[!UICONTROL Primary Status Reason]:** （Performance MAX キャンペーンの既存のアセットグループの読み取り専用フィールド）アセットグループのプライマリステータスに関する追加の詳細。 値には、*ASSET_GROUP_DISAPPROVED、* *ASSET_GROUP_LIMITED、* *ASSET_GROUP_PAUSED、* *ASSET_GROUP_REMOVED、* *ASSET_GROUP_UNDER_REVIEW、* *CAMPAIGN_ENDED、* *CAMPAIGN_PAUSED、* *CAMPAIGN_PENDING、* *CAMPAIGN_REMOVED、* *UNKNOWN、* **、または UNSPECIFIED.UNSPECIFIED。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** *[!UICONTROL Use account conversion goals for this campaign]* （デフォルト）か *[!UICONTROL Use campaign specific conversion goals]*。 キャンペーンのコンバージョン目標を指定する場合は、「標準目標」を選択するか、キャンペーンのカスタム目標を作成します。

目標は毎日同期されるので、過去 24 時間に作成された既存の目標はリストされない場合があります。 リストを更新するには、[&#x200B; 広告ネットワークデータを手動で同期 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/sync-network.md) します。

カスタムのコンバージョン目標を作成するには、[**[!UICONTROL + Add custom goal]**] をクリックし、カスタム目標名を入力して、カスタム目標に含める [&#x200B; コンバージョンアクション &#x200B;](https://support.google.com/google-ads/answer/6032150) を選択し、[**[!UICONTROL Save]**] をクリックします。 **メモ：** 各キャンペーンには、1 つのカスタム目標のみを設定できます。

>[!TIP]
>
>キャンペーンがハイブリッドポートフォリオの一部である場合は、ポートフォリオの目的のコンバージョン目標に一致するキャンペーンレベルの目標を使用することがベストプラクティスです。追加のコンバージョン目標を含めると、ポートフォリオのパフォーマンスに影響を与える可能性があります。
>
>ただし、[&#x200B; 広告ネットワークに目標をアップロード &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md) するハイブリッドポートフォリオ内のキャンペーンの場合、ここでは行わずに、広告ネットワークのエディター内で次の操作を行います。a） アップロードした検索、ソーシャルおよびCommerceのポートフォリオ目標指標（「O_ACS_OBJ」で始まる）をキャンペーンのコンバージョンアクションとして追加し、b）広告ネットワークのトラッキング指標が広告ネットワークにアップロードされないので、[!DNL Google] ーーールトラッキングされたコンバージョンを含むキャンペーン目標を追加します。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
