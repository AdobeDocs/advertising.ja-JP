---
title: '''[!DNL Google Ads] キャンペーン設定'
description: 次の設定を参照してください： [!DNL Google Ads] キャンペーン。
exl-id: d16ef1a9-f943-494c-8655-975383707f3c
feature: Search Campaign Management
source-git-commit: 1dbe8da7122b38dd11a242c453d71a832b31eee8
workflow-type: tm+mt
source-wordcount: '2025'
ht-degree: 0%

---

# [!DNL Google Ads] キャンペーン設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーンの作成時のみ使用可能）広告を配置する場所と、キャンペーンに含めることのできる広告タイプ：

* *[!UICONTROL Search Network Only]:* 検索ネットワーク上に広告を表示します（以下を含む） [!DNL Google] 検索結果、およびオプションでパートナーサイトを検索します。 広告グループごとにキーワードを指定する必要があります。

* *[!UICONTROL Search with Display Select]:* 検索ネットワーク上の広告を表示します ( [!DNL Google] 検索結果、および（オプションで検索パートナーサイト）、ディスプレイネットワークサイトに広告を表示する場合もあります。 ディスプレイネットワーク上で、 [!DNL Google Ads] キャンペーンの入札戦略に関係なく、自動入札を使用して広告を選択的に表示します。 検索広告の場合は、各広告グループのキーワードを指定します。ディスプレイ広告の場合は、プレースメントを指定し、必要に応じて各広告グループのキーワードを指定します。

* *[!UICONTROL Shopping Network]:* 製品広告を表示します。 [!DNL Google] は、の製品に基づいて自動的にを生成します。 [!DNL Google Merchant Center] オン [!DNL Google Shopping]（の隣の領域） [!DNL Google] 検索結果（テキスト広告とは別のもの）、および（オプションで）検索パートナー web サイト。 キャンペーン内の広告グループごとに、広告を提供する製品グループを指定できます。

* *[!UICONTROL Display Network Only]:* ディスプレイネットワーク上に広告を表示します。 各広告グループに対して、プレースメントを指定し、必要に応じてキーワードを指定する必要があります。

* *[!UICONTROL Performance Max]:* （ベータ版機能）を使用して、様々なチャネルの広告のコンバージョンを表示および最適化します。 [!DNL Google Ads] スマート入札。 キャンペーン設定では、1 つ以上のアセットグループを指定する必要があります。このグループには、画像、ロゴ、ヘッドライン、説明、オプションのビデオおよびオーディエンスシグナルが含まれます。 [!DNL Google Ads] チャネルに基づいて広告を提供するために、アセットを自動的に組み合わせます ( 例： [!DNL YouTube], [!DNL Gmail]または [!DNL Search]) をクリックします。

  **メモ：**

   * 必要な設定のみを使用できます。 オプション設定の場合は、 [!DNL Google Ads] 編集者です。

   * リンク先 [!DNL Google Merchant Center] 製品フィードはサポートされていません。

   * リストグループのサポートは利用できません。 リストグループのデータを管理および表示するには、 [!DNL Google Ads] 編集者です。

   * ハイブリッドの最適化がサポートされています。 入札戦略のターゲットとキャンペーンの予算は、キャンペーンレベルで設定します。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**（既存の、読み取り専用の Gmail キャンペーンのみ）次のいずれを実行するかを指定します。

* *[!UICONTROL Target and Bid]* 広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーに対してのみ広告を表示する。

* *[!UICONTROL Bid Only]:*  ターゲットオーディエンスに関連付けられていないユーザーが他の広告グループレベルのターゲットを満たしている限り、広告を表示する。 ただし、特定のオーディエンスに対して広告が表示される可能性を高めるには、それらのオーディエンスの入札額を高く設定します。

**[!UICONTROL Status]:** キャンペーンの表示ステータス： *アクティブ* または *一時停止*. 新しい広告キャンペーンのデフォルトは、 *アクティブ*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** ( 検索ネットワークのみをターゲットにするキャンペーン（ショッピングキャンペーンを含む）広告ネットワークの検索パートナーネットワークに広告を表示します。 デフォルトでは、このオプションは *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Enhanced CPC]:* （パフォーマンスの最大値または既存値は読み取り専用では使用できません） [!DNL Gmail] キャンペーン ) は、広告ネットワークの拡張クリック単価 (eCPC) モデルを使用します。これにより、広告ネットワーク内で指定されたコンバージョン（検索、ソーシャル、コマースではなく）を使用して、コンバージョンを最大化します。

eCPC を持つキャンペーンを最適化された検索、ソーシャル、コマースのポートフォリオに追加すると、検索、ソーシャル、コマースがベース入札を最適化し、「[!UICONTROL Auto adjust campaign budget limits]「 」オプションは有効です — キャンペーンの予算です。 広告ネットワークは、すべての入札調整を最適化し、独自のデータとインサイトに基づいて、ユーザークエリの実行時に検索、ソーシャル、コマースで生成された入札を変更する場合があります。 **注意：** ポートフォリオで eCPC キャンペーンを使用するのは、広告ネットワークで追跡される合計コンバージョンがポートフォリオの目標と一致する場合のみです。 <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* （デフォルト）: （パフォーマンスの最大キャンペーンでは使用できません）クリック単価 (CPC) モデルを使用します。 オプションで、広告ネットワークにキャンペーンの入札の変更を許可できます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：これは、[!UICONTROL Enhanced CPC]&quot;オプション。

* *[!UICONTROL Maximize Clicks]:* （検索、表示、およびショッピングキャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークは、入札を最適化して、クリック数を最大化します。 必要に応じて、 **[!UICONTROL Max CPC]** （クリックあたりのコスト）を使用して、広告ネットワークが各クリックに対して特定の金額を超えないようにします。 **注意：** この戦略を持つキャンペーンをポートフォリオに追加すると、入札は、ポートフォリオの目的ではなく、クリックの重み付けによって駆動されます。

* *[!UICONTROL Maximize Conversion Value]:* （検索、パフォーマンス最大、スマートショッピングキャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークが、入札を最適化して、コンバージョン値を最大化します。 必要に応じて、 **[!UICONTROL Target Return on Ad Spend]** (ROAS) を割合で示します。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンで使用しますが、標準のポートフォリオでは使用しません。

* *[!UICONTROL Maximize Conversions]:* （検索、表示、パフォーマンスの最大キャンペーン）広告ネットワーク（検索、ソーシャル、コマースではなく）は、入札を最適化して、コンバージョンを最大化します。 必要に応じて、 **[!UICONTROL Target CPA]** （獲得あたりのコスト）。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンで使用しますが、標準のポートフォリオでは使用しません。

* *[!UICONTROL Target CPA]:* （ディスプレイキャンペーン、既存の検索キャンペーン）広告ネットワーク（検索、ソーシャル、コマースではなく）は、オプションのに基づいて入札を最適化します **[!UICONTROL Target CPA]** （獲得あたりのコスト）：獲得（コンバージョン）に対して支払う 30 日間の平均金額。 **注意：** このオプションは、支出戦略を除くハイブリッドポートフォリオのキャンペーン（標準のポートフォリオではない）に使用します。 [!UICONTROL Weekly] または [!UICONTROL Google Target CPA].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データを使用できません。

  新しい検索キャンペーンの場合、 [!DNL Google Ads] は、この入札戦略を [!UICONTROL Maximize Conversions] 使用する戦略 [!UICONTROL Target CPA] の値です。 この方法で既存の検索キャンペーンを使用する場合は、ターゲット値の編集のみ可能で、その結果、戦略が [!UICONTROL Maximize Conversions] 指定した [!UICONTROL Target CPA] の値です。

* *[!UICONTROL Target Impression Share]:* （検索キャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークによって、入札を最適化して、ターゲットのインプレッション共有と広告の位置を達成します。 必要に応じて、 **[!UICONTROL Target Impression Share]** パーセンテージでは、 **[!UICONTROL Target Ad Position]**、および **[!UICONTROL Max CPC]** （クリックあたりのコスト）。 **注意：** このオプションは、ポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:*  （ディスプレイ広告およびショッピングキャンペーン、既存の検索キャンペーン）広告ネットワーク（検索、ソーシャル、コマースではなく）は、指定した値に基づいて入札を最適化します **[!UICONTROL Target ROAS]** （広告費用対効果）。割合で指定します。 **注意：** このオプションは、支出戦略を除くハイブリッドポートフォリオのキャンペーン（標準のポートフォリオではない）に使用します。 [!UICONTROL Weekly] または [!UICONTROL Google Target ROAS].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データを使用できません。

  新しい検索キャンペーンの場合、 [!DNL Google Ads] は、この入札戦略を [!UICONTROL Maximize Conversion Value] 使用する戦略 [!UICONTROL Target Return on Ad Spend value]. この方法で既存の検索キャンペーンを使用する場合は、ターゲット値の編集のみ可能で、その結果、戦略が [!UICONTROL Maximize Conversion Value] 指定した [!UICONTROL Target Return on Ad Spend] の値です。

* *[!UICONTROL Viewable CPM]:* （既存、読み取り専用） [!DNL Gmail] キャンペーンのみ ) 広告ネットワーク（検索、ソーシャル、コマースではなく）は、表示可能と測定された広告にのみ入札します。 **注意：** この戦略の最適化は、どの種類のポートフォリオでもサポートされていません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** （買い物キャンペーンのみ、既存のキャンペーンの読み取り専用）キャンペーンの製品が販売される国。 製品は対象国に関連付けられているので、この設定によってキャンペーンで広告される製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** ( 買い物キャンペーンのみ。既にローカルのショッピングプログラムに参加している広告主 [!DNL Google Merchant Center] 米国、英国、DE、FR、JP、AU に店舗（オプション）許可 [!DNL Google Ads] Google.comのショッピング広告にローカルの在庫情報を自動的に追加する。

**ヒント：** この設定を使用する場合、 [!UICONTROL Inventory Filter] 設定。

**注意：** ローカルの在庫広告には、次の操作を行うための追加のフィードが 2 つ必要です。 [!DNL Google Merchant Center] —1 つはローカルの製品データで、もう 1 つはローカルの製品在庫です。 詳しくは、 [!DNL Google Ads] 詳細に関するドキュメント [ローカルショッピング広告](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** （検索および表示ネットワークのみ）キャンペーン内の広告の 1 つ以上のターゲット言語。

[!DNL Google Ads] は、ユーザーの [!DNL Google] 言語設定、検索クエリの言語、現在のページ、または [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** ターゲットとして含めるまたは除外する特定のユーザーの地理的な場所。 デフォルトでは、すべてのロケーションがターゲットになっています。 任意の場所の組み合わせに対して、ユーザーを含めたり除外したりできます。 除外は、常に含めるものを上書きします。

* すべての場所をターゲットにする場合は、どの場所も選択しないでください。

* 特定の場所をターゲットにする、または除外するには：

   * （国、都道府県、大都市、市区町村）クリック **[!UICONTROL Location Target]** (![場所のターゲット](/help/search-social-commerce/assets/location-target.png "場所のターゲット")) をクリックし、以下を含めて除外する場所を特定します。

      * 場所とその子の場所を含めるには、その横の円を 1 回クリックして、青いチェックマーク (![次を含む](/help/search-social-commerce/assets/include.png "次を含む")) が表示されます。

      * 場所を除外するには、その場所の横にある円を 2 回クリックして、赤いチェックマーク (![除外](/help/search-social-commerce/assets/exclude.png "除外")) が表示されます。

      * 場所をそのサブコンポーネント（米国の州、大都市地域、市区町村など）に展開するには、場所名をクリックします。

      * 場所を検索するには、その場所の最初の 3 文字以上を入力フィールドに入力または貼り付けます。 検索結果で、 **[!UICONTROL Include]** 含める場所の横または **[!UICONTROL Exclude]** をクリックします。

   * （住所の近くの場所、含まれるターゲットのみ）クリック **[!UICONTROL Radius Target]** (![半径ターゲット](/help/search-social-commerce/assets/radius-target.png "半径ターゲット")) をクリックし、次に「 **[!UICONTROL Address]**. 目標とする住所と住所の周囲の半径（マイルまたはキロメートル）を入力し、次に、 **[!UICONTROL Add]**.

   * （地理的座標の近くの位置、含まれるターゲットのみ）クリック **[!UICONTROL Radius Target]** (![半径ターゲット](/help/search-social-commerce/assets/radius-target.png "半径ターゲット")) をクリックし、次に「 **[!UICONTROL Coordinate]**. ターゲットとする位置の周囲の緯度と経度および半径をマイルまたはキロメートル単位で入力し、次に、 **[!UICONTROL Add]**.

   * ( 近い場所 [!DNL My Business] 場所の拡張として使用できる場所（ターゲットのみを含む） **[!UICONTROL Location Group Target]** (![ロケーショングループ](/help/search-social-commerce/assets/location-group.png "ロケーショングループ"))。必要に応じて、国、都道府県、大都市、または市区町村を入力して、使用可能な場所のリストを下に矢印を付け、次のリストから 1 つ以上の場所を選択します。 [!DNL Google My Business] 場所。 ターゲットとする位置の周りの半径をマイルまたはキロメートル単位で指定し、 **[!UICONTROL Add]**.

* （含まれるターゲット・ロケーションに入札調整を追加する手順は、次のとおりです）入札調整値を入力します。

* 0%：この場所の広告の入札を調整しない。

* \[ その他の値 (-90% ～ 300%)\]：この場所での広告の入札額を増減させます。

**注意：**

* 検索、ソーシャル、コマースでは、以下の場所のターゲットに対して自動調整された入札調整は行われません。これは、 [!DNL Google Ads] は、サーファーの場所を場所のターゲットにマッピングします。

   * 半径のターゲット。

   * 都道府県/地域/郡/都道府県レベル以下の一部の場所。 [!DNL Google Ads] では、空港や米国議会の地区を含む親の場所をサーファーの URL に送信しません。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** （ディスプレイネットワークのみ）ターゲットとする特定の携帯電話会社。通信事業者は国別に並べ替えられます。 何も選択しない場合、すべてのターゲットが設定されます。

**[!UICONTROL Mobile Carriers]:** （ディスプレイネットワークのみ）ターゲットとする特定のオペレーティングシステム。 何も選択しない場合、すべてのターゲットが設定されます。

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

**[!UICONTROL Track Product Group]:** ( の [!UICONTROL EF Redirect] （のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （アセットグループごと）

**[!UICONTROL Asset Group Name]:** アセットグループの名前。 リンク先 [!DNL Google Merchant Center] 製品フィードはサポートされていません。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス： *[!UICONTROL Active]* または *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** アセットグループから作成されるすべての広告の最終 URL。 <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** 広告に対する最大 15 個の画像（以下のサイズを含む）:1) 正方形の画像が 3 つ以上、2) 横置きの画像が 3 つ以上、3) 少なくとも 1 つの縦置きの画像が 1 つ以上。 詳しくは、 [[!DNL Google Ads] 画像仕様](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 画像をアップロードするには：

1. クリック **[!UICONTROL +]** お使いのデバイスまたはネットワークから画像を選択します。

1. 各画像に対して、次の操作を実行します。

   1. 縦横比を選択します。

   1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能な部分を選択し、可能な限り画像の表示可能な部分のサイズを変更します。

   1. （オプション）追加の縦横比を選択し、必要に応じて、選択した各縦横比に合わせて画像の位置を変更したりサイズを変更したりします。

      選択した縦横比ごとに 1 つのアセットが作成されます。

   1. クリック **[!UICONTROL Proceed]**.

1. 画像の指定が完了したら、 **[!UICONTROL Upload]**.

**[!UICONTROL Logos]:** 1 つ以上の正方形のロゴ(1:1)、1 つの横向きのロゴ(4:1)。 各サイズには最大 5 個を含めることができます。 詳しくは、 [[!DNL Google Ads] ロゴの仕様](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 画像をアップロードするには：

1. クリック **[!UICONTROL +]** お使いのデバイスまたはネットワークから画像を選択します。

1. 各画像に対して、次の操作を実行します。

   1. 縦横比を選択します。

   1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能な部分を選択し、可能な限り画像の表示可能な部分のサイズを変更します。

   1. （オプション）追加の縦横比を選択し、必要に応じて、選択した各縦横比に合わせて画像の位置を変更したりサイズを変更したりします。

      選択した縦横比ごとに 1 つのアセットが作成されます。

   1. クリック **[!UICONTROL Proceed]**.

1. 画像の指定が完了したら、 **[!UICONTROL Upload]**.

**[!UICONTROL Videos]:** （オプション）少なくとも 1 つ、最大 5 つのの URL。 [!DNL YouTube] ビデオの長さは 10 秒以上です。

**[!UICONTROL Headlines]:** 少なくとも 3 つ、最大 5 つの短い見出し（それぞれ 30 文字まで）。 1 つ以上のヘッドラインは 15 文字以下にする必要があります。 最終的な URL 拡張を有効にするキャンペーンレベルのオプションが、 [!DNL Google Ads]を、 [!DNL Google Ads] この値を、ランディングページのコンテンツに基づくカスタムヘッドラインに置き換えます。

**[!UICONTROL Long Headlines]:** 少なくとも 1 つ、最大 5 つの長いヘッドライン（それぞれ最大 90 文字）。

**[!UICONTROL Descriptions]:** 少なくとも 2 つ、最大 4 つの説明で、それぞれ最大 90 文字です。 少なくとも 1 つの説明は 30 文字以下にする必要があります。

**[!UICONTROL Call to Action]:** 広告に含めるコールトゥアクション。 デフォルトでは、 *[!UICONTROL Automated]* が選択され、 [!DNL Google Ads] コールトゥアクションを選択します。 必要に応じて、別のアクションを選択できます。

**[!UICONTROL Business Name]:** ビジネス名（最大 25 文字）。

**[!UICONTROL Add new asset group]:** 別のアセットグループを指定できます。

>[!MORELIKETHIS]
>
>* [キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
