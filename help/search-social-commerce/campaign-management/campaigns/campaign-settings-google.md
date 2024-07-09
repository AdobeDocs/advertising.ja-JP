---
title: '''[!DNL Google Ads] キャンペーン設定'
description: の設定を参照します [!DNL Google Ads] キャンペーン。
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 977314f07d1299d9b94680861b046161bb444228
workflow-type: tm+mt
source-wordcount: '2450'
ht-degree: 0%

---

# [!DNL Google Ads] キャンペーン設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーンの作成時にのみ使用できます）広告の配置場所と、キャンペーンに含めることができる広告タイプは次のとおりです。

* *[!UICONTROL Search Network Only]:* 検索ネットワーク上の広告を表示します。次のものが含まれます [!DNL Google] 検索結果と、オプションでパートナーサイトを検索できます。 各広告グループにキーワードを指定する必要があります。

* *[!UICONTROL Search with Display Select]:* 検索ネットワーク上の広告を表示します（次を含む） [!DNL Google] 検索結果と（オプションでパートナーサイトを検索）、潜在的に表示ネットワークサイトに広告を表示します。 ディスプレイネットワークで、 [!DNL Google Ads] は、キャンペーンの入札戦略に関係なく、自動入札を使用して広告を選択的に表示します。 検索広告の場合は、広告グループごとにキーワードを指定します。表示広告の場合は、プレースメントを指定し、オプションで広告グループごとにキーワードを指定します。

* *[!UICONTROL Shopping Network]:* 製品広告を表示し、 [!DNL Google] では、の製品に基づいて自動的にを生成します [!DNL Google Merchant Center] 日付： [!DNL Google Shopping]、の隣の領域 [!DNL Google] 検索結果（テキスト広告とは別）および（オプションで）パートナー web サイトを検索します。 キャンペーンの広告グループごとに、広告する製品グループを指定できます。

* *[!UICONTROL Display Network Only]:* ディスプレイ ネットワーク上の広告を表示します。 広告グループごとに、プレースメントを指定する必要があり、オプションでキーワードを指定することもできます。

* *[!UICONTROL Performance Max]:* を使用して、チャネルをまたいだ広告のコンバージョンを表示および最適化します。 [!DNL Google Ads] スマート入札。 キャンペーン設定内で、1 つ以上のアセットグループ（画像、ロゴ、ヘッドライン、説明、オプションビデオ、オーディエンスシグナルを含む）を指定する必要があります。 [!DNL Google Ads] では、アセットを自動的に組み合わせ、チャネルに基づいて広告を提供します（例： [!DNL YouTube], [!DNL Gmail]、または [!DNL Search]）に設定します。

  **メモ：**

   * 必要な設定のみ使用できます。 オプションの設定については、にログインしてください [!DNL Google Ads] 編集者。

   * リンク先 [!DNL Google Merchant Center] 製品フィードはサポートされていません。

   * グループの一覧表示はサポートされていません。 グループをリストするデータを管理および表示するには、にログインします [!DNL Google Ads] 編集者。

   * ハイブリッド最適化がサポートされています。 入札戦略のターゲットとキャンペーンの予算は、キャンペーンレベルで設定します。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**（既存の読み取り専用 Gmail キャンペーンのみ）次のどちらを実行するか：

* *[!UICONTROL Target and Bid]* ターゲットオーディエンスに関連付けられているユーザーで、その広告グループに対する他のターゲットも満たしているユーザーにのみ広告を表示する。

* *[!UICONTROL Bid Only]:*  ターゲットオーディエンスに関連付けられていない人物であっても、他の広告グループレベルのターゲットを満たす限り、広告を表示する。 ただし、特定のオーディエンスに対してより高い入札を設定すると、それらのオーディエンスに広告が表示される可能性が高くなります。

**[!UICONTROL Status]:** キャンペーンの表示ステータス： *アクティブ* または *一時停止*. 新規広告キャンペーンのデフォルトはです。 *アクティブ*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** （ショッピングキャンペーンを含む、検索ネットワークのみをターゲットとするキャンペーン）広告ネットワークの検索パートナーネットワーク上の広告を表示します。 デフォルトでは、このオプションは *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Enhanced CPC]:* （Performance max または既存では使用できません。読み取り専用です [!DNL Gmail] キャンペーン）広告ネットワークの拡張コストパークリック（eCPC）モデルを使用します。これにより、広告ネットワークは、平均 CPC を最大 CPC 未満に保ちながら、広告ネットワーク（検索、ソーシャル、Commerceではない）内で指定されたコンバージョンを使用して、コンバージョンを最大化するために、各オークションのコストパークリック（CPC）入札を自動的に変更できます。

eCPC を使用してキャンペーンを最適化された検索、ソーシャル、Commerce ポートフォリオに追加すると、検索、ソーシャル、Commerceによってベース入札が最適化され、「[!UICONTROL Auto adjust campaign budget limits]「」オプションが有効になっています – キャンペーンの予算。 アドネットワークは、すべての入札調整を最適化し、独自のデータとインサイトに基づいて、ユーザークエリ時に検索、ソーシャル、Commerceで生成された入札を変更する可能性があります。 **注意：** ポートフォリオで eCPC キャンペーンを使用するのは、広告ネットワークで追跡されるコンバージョンの合計がポートフォリオの目的と合致する場合のみです。 <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* （デフォルト）: （パフォーマンス最大化キャンペーンでは使用できません）クリック単価（CPC）モデルを使用します。 オプションで、広告ネットワークにキャンペーンの入札の変更を許可できます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：これは「」の使用と同じです[!UICONTROL Enhanced CPC]」オプションを選択します。

* *[!UICONTROL Maximize Clicks]:* （検索、ディスプレイ、ショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、クリック数を最大化するように入札を最適化します。 オプションで、 **[!UICONTROL Max CPC]** （クリックあたりのコスト）広告ネットワークがクリックごとに特定の金額以上を支払わないようにします。 **注意：** この戦略を使用してキャンペーンをポートフォリオに追加すると、入札はポートフォリオの目的ではなく、クリックの重み付けで決まります。

* *[!UICONTROL Maximize Conversion Value]:* （検索、パフォーマンス最大化、スマートショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、コンバージョン値を最大化するように入札を最適化します。 必要に応じて、 **[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセンテージで表示します。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。

* *[!UICONTROL Maximize Conversions]:* （検索、ディスプレイ、Performance MAX キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、コンバージョンを最大化するように入札を最適化します。 必要に応じて、 **[!UICONTROL Target CPA]** （取得あたりのコスト）。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。

* *[!UICONTROL Target CPA]:* （ディスプレイキャンペーン、既存の検索キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、オプションに基づいて入札を最適化します **[!UICONTROL Target CPA]** （1 購入あたりのコスト）獲得（コンバージョン）の支払いに対して支払う 30 日間の平均金額。 **注意：** このオプションは、次を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します [!UICONTROL Weekly] または [!UICONTROL Google Target CPA].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

  新しい検索キャンペーンの場合、 [!DNL Google Ads] 様はこの入札戦略をに置き換えました [!UICONTROL Maximize Conversions] を使用した戦略 [!UICONTROL Target CPA] の値。 この戦略を使用している既存の検索キャンペーンの場合は、ターゲット値のみを編集でき、編集すると戦略がに変更されます。 [!UICONTROL Maximize Conversions] 指定されたを使用した戦略 [!UICONTROL Target CPA] の値。

* *[!UICONTROL Target Impression Share]:* （検索キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークを使用すると、ターゲットインプレッションシェアと広告掲載順位を達成するように入札を最適化できます。 オプションで、 **[!UICONTROL Target Impression Share]** 割合で、 **[!UICONTROL Target Ad Position]**、および **[!UICONTROL Max CPC]** （クリック単価）。 **注意：** このオプションは、ポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:*  （ディスプレイおよびショッピングキャンペーン、既存の検索キャンペーン）広告ネットワーク（検索、ソーシャル、Commerceではない）は、指定されたに基づいて入札を最適化します **[!UICONTROL Target ROAS]** （広告費用対効果）。パーセンテージで指定します。 **注意：** このオプションは、次を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します [!UICONTROL Weekly] または [!UICONTROL Google Target ROAS].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

  新しい検索キャンペーンの場合、 [!DNL Google Ads] 様はこの入札戦略をに置き換えました [!UICONTROL Maximize Conversion Value] を使用した戦略 [!UICONTROL Target Return on Ad Spend value]. この戦略を使用している既存の検索キャンペーンの場合は、ターゲット値のみを編集でき、編集すると戦略がに変更されます。 [!UICONTROL Maximize Conversion Value] 指定されたを使用した戦略 [!UICONTROL Target Return on Ad Spend] の値。

* *[!UICONTROL Viewable CPM]:* （Existing, read-only [!DNL Gmail] キャンペーンのみ）広告ネットワーク（検索、ソーシャル、Commerceは除く）は、ビューアブルとして測定された広告のみを入札します。 **注意：** この戦略の最適化は、どのタイプのポートフォリオでもサポートされていません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）キャンペーンの商品が販売される国。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** （ショッピングキャンペーンのみ。既にローカルショッピングプログラムに参加している広告主 [!DNL Google Merchant Center] 米国、英国、DE、FR、JP、AU の店舗（オプション） [!DNL Google Ads] でローカルの在庫情報をショッピング広告に自動的に追加するにはGoogle.com。

**ヒント：** この設定を使用する場合は、でローカル広告を除外しないでください [!UICONTROL Inventory Filter] の設定値。

**注意：** ローカルの在庫広告には、に 2 つの追加フィードが必要です。 [!DNL Google Merchant Center] — 1 つはローカルの製品データを使用し、もう 1 つはローカルの製品インベントリを使用します。 を参照してください。 [!DNL Google Ads] の詳細情報に関するドキュメント [ローカルショッピング広告](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** （ネットワークの検索と表示のみ） キャンペーンの広告の 1 つ以上のターゲット言語。

[!DNL Google Ads] ユーザーの言語をユーザーの言語から決定します [!DNL Google] 検索クエリ、現在のページ、または最近表示されたページの言語設定または言語 [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** ターゲットとして含めるか除外する特定のユーザー地理的ロケーション。 デフォルトでは、すべての場所がターゲットになります。 任意の場所の組み合わせにユーザーを含めたり、除外したりできます。 除外は、常に包含を上書きします。

* すべての場所を対象にするには、どの場所も選択しないでください。

* 特定の場所をターゲットまたは除外するには：

   * （国、都道府県、大都市圏、または市区町村）をクリックします。 **[!UICONTROL Location Target]** （![場所のターゲット](/help/search-social-commerce/assets/location-target.png "場所のターゲット")）を選択し、含める場所と除外する場所を見つけます。

      * 位置とその子位置を含めるには、隣の円を 1 回クリックして、青いチェックマーク（![次を含める](/help/search-social-commerce/assets/include.png "次を含める")）が表示されます。

      * 位置を除外するには、隣の円を 2 回クリックして、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されます。

      * 場所をサブコンポーネント（米国の州、大都市圏、都市など）に展開するには、場所名をクリックします。

      * 場所を検索するには、入力フィールドに場所の最初の 3 文字以上を入力するか貼り付けます。 検索結果で、 **[!UICONTROL Include]** 含める場所または含める場所の横 **[!UICONTROL Exclude]** 除外する場所の横。

   * （所在地に近い場所。ターゲットのみ含む）クリック **[!UICONTROL Radius Target]** （![半径ターゲット](/help/search-social-commerce/assets/radius-target.png "半径ターゲット")）を選択し、 **[!UICONTROL Address]**. ターゲットとするアドレスとその周囲の半径（マイルまたはキロメートル）を入力し、 **[!UICONTROL Add]**.

   * （地理的座標に近い場所。含まれるターゲットのみ）をクリック **[!UICONTROL Radius Target]** （![半径ターゲット](/help/search-social-commerce/assets/radius-target.png "半径ターゲット")）を選択し、 **[!UICONTROL Coordinate]**. ターゲットとする位置の周りの緯度と経度、および半径（マイルまたはキロメートル単位）を入力し、 **[!UICONTROL Add]**.

* （組み込み対象事業所に対する入札調整を追加する手順は、次のとおりです）入札調整値を入力します。

* 0%：この場所の広告の入札を調整しません。

* \[Other values from -90% to 300%\]：この場所の広告の入札額を増減させます。

**注意：**

* 検索、ソーシャル、Commerceでは、データに制限があるため、次の場所目標に対して自動調整された入札調整を提供しません [!DNL Google Ads] では、サーファーの場所を場所ターゲットにマッピングできます。

   * 半径ターゲット。

   * 州/都道府県/地域/郡/県レベルの下に次の一部の場所があります [!DNL Google Ads] は、空港や米国議会選挙区を含め、サーファーの URL に親の場所を送信しません。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** （ディスプレイネットワークのみ）ターゲットとする特定の携帯電話会社。通信会社は国別に分類されます。 何も選択しない場合は、すべてがターゲットになります。

**[!UICONTROL Mobile Carriers]:** （ネットワークのみを表示）ターゲットにする特定のオペレーティングシステム。 何も選択しない場合は、すべてがターゲットになります。

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

**[!UICONTROL Track Product Group]:** （用 [!UICONTROL EF Redirect] のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （アセットグループあたり）

**[!UICONTROL Asset Group Name]:** アセットグループの名前。 リンク先 [!DNL Google Merchant Center] 製品フィードはサポートされていません。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス： *[!UICONTROL Active]* または *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** アセットグループから作成されたすべての広告の最終的な URL。 <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** 広告の最大 15 枚の画像（次のサイズを含む）: 1） 3 つ以上の正方形画像、2） 3 つ以上の横長画像、3） 1 つ以上の縦長画像。 を参照してください。 [[!DNL Google Ads] 画像仕様](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 画像をアップロードするか、から選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* 画像をアップロードするには：

   1. 日 [!UICONTROL Upload from Device] タブ、クリック **[!UICONTROL +]** さらに、デバイスまたはネットワークから画像を選択します。

   1. 各画像に対して、次の手順を実行します。

      1. アスペクト比を選択します。

      1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択します。また、可能な場合は、画像の表示可能部分のサイズを必要に応じて変更します。

      1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

         選択した縦横比ごとに 1 つのアセットが作成されます。

      1. クリック **[!UICONTROL Proceed]**.

   1. 画像の指定が終了したら、 **[!UICONTROL Upload]**.

* から画像を選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** 画像を選択します。

**[!UICONTROL Logos]:** 正方形（1:1）のロゴと横（4:1）のロゴが 1 つ以上。 各サイズを最大 5 つ含めることができます。 を参照してください。 [[!DNL Google Ads] ロゴの仕様](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 画像をアップロードするか、から選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* 画像をアップロードするには：

   1. 日 [!UICONTROL Upload from Device] タブ、クリック **[!UICONTROL +]** さらに、デバイスまたはネットワークから画像を選択します。

   1. 各画像に対して、次の手順を実行します。

      1. アスペクト比を選択します。

      1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択します。また、可能な場合は、画像の表示可能部分のサイズを必要に応じて変更します。

      1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

         選択した縦横比ごとに 1 つのアセットが作成されます。

      1. クリック **[!UICONTROL Proceed]**.

   1. 画像の指定が終了したら、 **[!UICONTROL Upload]**.

* から画像を選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** 画像を選択します。

**[!UICONTROL Videos]:** （オプション）少なくとも 1 つ、最大 5 つ [!DNL YouTube] 10 秒以上の長さのビデオ。 URL を入力するか、 [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* URL を入力するには：

   1. 日 [!UICONTROL Enter Video Url] タブで、URL を入力します。

   1. （任意）別の URL を追加するには、次をクリックします： **[!UICONTROL + Add]** URL を入力します。

* からビデオを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** ビデオを選択します。

**[!UICONTROL Headlines]:** 少なくとも 3 つの最大 5 つの短いヘッドライン（それぞれ最大 30 文字）。 少なくとも 1 つのヘッドラインは 15 文字以下である必要があります。 最終的な URL 拡張を有効にするキャンペーンレベルのオプションが内で設定されている場合 [!DNL Google Ads]、次に [!DNL Google Ads] は、この値を、ランディングページのコンテンツに基づくカスタムのヘッドラインに置き換えます。

テキストを入力するか、からアセットを選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* テキストを入力するには：

   1. 日 [!UICONTROL Enter Text] タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、 **[!UICONTROL + Add]** と文字列を入力します。

* からアセットを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** アセットを選択します。

**[!UICONTROL Long Headlines]:** それぞれ最大 90 文字の長い見出しを 1 つ以上、最大 5 つ含める。 テキストを入力するか、からアセットを選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* テキストを入力するには：

   1. 日 [!UICONTROL Enter Text] タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、 **[!UICONTROL + Add]** と文字列を入力します。

* からアセットを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** アセットを選択します。

**[!UICONTROL Descriptions]:** 少なくとも 2 つ、最大 4 つの説明（それぞれ最大 90 文字）。 少なくとも 1 つの説明は、30 文字以下にする必要があります。 テキストを入力するか、からアセットを選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* テキストを入力するには：

   1. 日 [!UICONTROL Enter Text] タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、 **[!UICONTROL + Add]** と文字列を入力します。

* からアセットを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** アセットを選択します。

**[!UICONTROL Call to Action]:** 広告に含めるコールトゥアクション。 デフォルトでは *[!UICONTROL Automated]* が選択され、 [!DNL Google Ads] コールトゥアクションを選択します。 オプションで、別のアクションを選択できます。

**[!UICONTROL Business Name]:** ビジネス名（最大 25 文字）。

**[!UICONTROL Audience Signal]:** （オプション） [!DNL Google Ads] キャンペーンのオーディエンスシグナルとして使用するオーディエンス。 [!DNL Google Ads] 機械学習モデルでは、オーディエンスを使用して、ターゲットとする類似の web サーファーを見つけます。また、パフォーマンス目標の達成に役立つシグナルとして指定されていないオーディエンスに広告を表示することもできます。 コンバージョンする可能性が最も高いオーディエンスを選択します。

>[!NOTE]
>オーディエンスシグナルは、とは異なります [キャンペーンレベルおよび広告グループレベルのオーディエンスターゲット](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** 別のアセットグループを指定できます。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** 対象 *[!UICONTROL Use account conversion goals for this campaign]* （デフォルト）または *[!UICONTROL Use campaign specific conversion goals]*. キャンペーンのコンバージョン目標を指定する場合は、「標準目標」を選択するか、キャンペーンのカスタム目標を作成します。

目標は毎日同期されるので、過去 24 時間に作成された既存の目標はリストされない場合があります。 リストを更新するには、 [広告ネットワークデータを手動で同期](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

カスタムコンバージョン目標を作成するには、をクリックします。 **[!UICONTROL + Add custom goal]**&#x200B;を入力し、カスタム目標名を入力して、 [コンバージョンアクション](https://support.google.com/google-ads/answer/6032150) をカスタム目標に含めて、 **[!UICONTROL Save]**. **注意：** 各キャンペーンには、1 つのカスタム目標のみを設定できます。

>[!TIP]
>
>キャンペーンがハイブリッドポートフォリオの一部である場合は、ポートフォリオの目的のコンバージョン目標に一致するキャンペーンレベルの目標を使用することがベストプラクティスです。追加のコンバージョン目標を含めると、ポートフォリオのパフォーマンスに影響を与える可能性があります。
>
>ただし、次の条件を満たすハイブリッドポートフォリオ内のキャンペーンの場合： [広告ネットワークへの目標のアップロード](/help/search-social-commerce/tools/objective-upload-to-networks.md)a） アップロードした検索、ソーシャル、Commerceの各ポートフォリオの目標指標（「O_ACS_OBJ」で始まる）をキャンペーンのコンバージョンアクションとして追加し、b）以下を含むキャンペーン目標を追加します [!DNL Google] – 広告ネットワークで追跡される指標は目的と共に広告ネットワークにアップロードされないので、で追跡されるコンバージョン。

>[!MORELIKETHIS]
>
>* [キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

