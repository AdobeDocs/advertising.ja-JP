---
title: '[!DNL Microsoft Advertising] キャンペーン設定'
description: キャンペーンの設定  [!DNL Microsoft Advertising]  参照します。
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: b8aa2461d261af50e1bf66c4ae29e4e453dfd182
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キャンペーンの設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーンの作成時にのみ使用可能）広告の配置場所と広告タイプ
キャンペーンには、次の内容が含まれる場合があります。

* *[!UICONTROL Search]:* 検索ネットワークのテキスト広告を表示します。

* *[!UICONTROL Shopping Network]:* 商品カタログ内の商品に関する商品広告をショッピングネットワーク上に表示 [!DNL Microsoft Merchant Center] ます。

* *[!UICONTROL Audience]:* [!DNL Microsoft Audience Network] のネイティブ/ディスプレイ広告を表示します。 a） キャンペーンを「[!UICONTROL Shopping Settings]」セクションのマーチャントセンターストアにリンクして、フィードベースの広告を自動的に生成するか、b） テキストアセットとアップロードされた画像を使用してレスポンシブ広告を作成できます。 どちらのオプションでも、ユーザーターゲティングを使用して広告グループを作成する必要があります。

* *[!UICONTROL Shopping Campaigns for Brands]:* 検索およびオーディエンスネットワークをまたいでリンクされた小売業者を通じて、製品を宣伝します。 子の広告グループと製品グループ（昇格させるアプリ）、およびキャンペーンのオプションの製品広告を作成できます。[!DNL Microsoft Advertising] の場合は、製品グループの広告が自動的に作成されます。 ブランドのショッピングキャンペーンの場合は入札戦略 [!UICONTROL Manual CPC] を、ブランドのショッピングプロモーションの場合は入札戦略 [!UICONTROL Cost per Sale] を使用します。

* *[!UICONTROL Microsoft Store Ads Campaign]:* [!DNL Microsoft Store] で利用できるアプリやゲームを昇格します。 キャンペーンの子広告グループ、製品グループおよびオプションの製品広告を作成できます。[!DNL Microsoft Advertising] では、製品グループの広告が自動的に作成されます。

* *[!UICONTROL Audience CTV Video]:* 視聴者ネットワーク上の接続されたテレビ （CTV） ビデオ広告を表示します。

* *[!UICONTROL Audience Video]:* オーディエンスネットワーク上の標準ビデオ広告を表示します。

* *[!UICONTROL Performance Max]:* スマート入札を使用して、すべてのネットワークにわたる複数の広告タイプ [!DNL Microsoft Advertising] 表示します。 キャンペーンの設定内で、1 つ以上のアセットグループを指定する必要があります。このグループには、画像、ロゴ、ヘッドライン、説明、オプションのコールトゥアクション、オーディエンスシグナルが含まれます。 広告ネットワークは、アセットを自動的に組み合わせて、チャネルに基づいて広告を提供します。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。 最大長は 128 文字です。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ* または *一時停止*。 新しい広告キャンペーンのデフォルトは *アクティブ* です。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Cost per Sale]:* （ショッピングキャンペーンのみ）検索、ソーシャル、Commerceを除く広告ネットワークは、[!UICONTROL Target CPS] （セールあたりのコスト）に基づいて入札を最適化します。 お支払いは、商品の広告をクリックした結果、24 時間以内にセールが成立した場合に限ります。 **メモ：** この入札戦略のキャンペーンをポートフォリオに含めないでください。 この入札戦略を使用するキャンペーンでは、検索、ソーシャル、Commerceの最適化は利用できません。

  この入札戦略を使用してブランドのショッピングキャンペーンを保存すると、入札戦略を変更できなくなります。 他のショッピングキャンペーンタイプの場合、この戦略は新規キャンペーンでのみ使用できます。

* *[!UICONTROL CPV]* （オーディエンス CTV ビデオキャンペーンのみ） ビューあたりのコスト（CPV） モデルを使用します。 検索、ソーシャル、Commerceでは、ポートフォリオに含まれているこの入札戦略を使用したキャンペーンの最適化は提供されません。

* *[!UICONTROL Enhanced CPC]:* （オーディエンス、検索、ショッピングネットワークのキャンペーン）広告ネットワークの拡張コストパークリック（eCPC）モデルを使用します。これにより、広告ネットワークは各オークションのコストパークリック（CPC）入札を自動的に変更し、コンバージョンを最大化しながら、広告ネットワーク内（検索、ソーシャル、Commerceではない）で指定されたコンバージョンを使用して、平均 CPC を最大 CPC 未満に保つことができます。

  eCPC を使用してキャンペーンを最適化された検索、ソーシャル、Commerceの各ポートフォリオに追加すると、検索、ソーシャル、Commerceによってベース入札が最適化され、「[!UICONTROL Auto adjust campaign budget limits]」オプションが有効になっている場合はキャンペーン予算が最適化されます。 アドネットワークは、すべての入札調整を最適化し、独自のデータとインサイトに基づいて、ユーザークエリ時に検索、ソーシャル、Commerceで生成された入札を変更する可能性があります。 **注意：** ポートフォリオで eCPC キャンペーンを使用するのは、広告ネットワークで追跡されるコンバージョンの合計がポートフォリオの目的と一致する場合のみです。

* *[!UICONTROL Manual CPC]*: （ブランド向けのショッピングキャンペーン、[!DNL Microsoft Store Ads] キャンペーン、その他のキャンペーンタイプでは非推奨）クリック単価（CPC）モデルを使用します。 一部の広告タイプでは、オプションで、広告ネットワークにキャンペーンの入札の変更を許可できます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：このオプションは、「[!UICONTROL Enhanced CPC]」オプションを使用する場合と同じです。

* *[!UICONTROL Manual CPA]:* （[!DNL Microsoft Store Ads] キャンペーン）獲得あたりのコスト（CPA） モデルを使用します。

* *[!UICONTROL Manual CPM]* （オーディエンスキャンペーンおよびオーディエンスビデオキャンペーンのみ） 1,000 回の表示インプレッションごとに使用する費用を指定する、1,000 回のインプレッションあたりのコスト（CPM） モデルを使用します。 この入札戦略を使用したキャンペーンは、ポートフォリオに含まれている場合、最適化されません。

* *[!UICONTROL Maximize Clicks]:* （検索およびショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、クリック数を最大化するように入札を最適化します。 必要に応じて、**[!UICONTROL Max CPC]** （クリック単価）を入力し、広告ネットワークがクリックごとに特定の金額以上を支払わないようにします。 **注意：** この戦略を使用してキャンペーンをポートフォリオに追加すると、クリックの重み（ポートフォリオ目標ではありません）が入札を促進します。

* *[!UICONTROL Maximize Conversion Value]:* （検索およびショッピング/スマートショッピングネットワーク、パフォーマンス最大化キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、コンバージョン値を最大化するように入札を最適化します。 必要に応じて、**[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセントで入力します。 **メモ：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceが Target ROAS を最適化します。

* *[!UICONTROL Maximize Conversions]:* （検索ネットワークまたはオーディエンスネットワーク（オーディエンスビデオまたは接続された TV を除く）上の Performance MAX のキャンペーンおよびキャンペーン）広告ネットワーク（検索、ソーシャル、Commerceを除く）は、コンバージョンを最大化するように入札を最適化します。 必要に応じて、**[!UICONTROL Target CPC]** （クリック単価）を入力します。 オーディエンスキャンペーンの場合は、オプションで **[!UICONTROL Target CPA]** （獲得あたりのコスト）を入力することもできます。 **メモ：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceが Target CPA を最適化します。

* *[!UICONTROL Target CPA]:* （検索ネットワーク上のキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークは、オプションの **[!UICONTROL Target CPA]** （獲得あたりのコスト）に基づいて入札を最適化します。これは、獲得（コンバージョン）に対して支払う 30 日間の平均金額です。 **メモ：** このオプションは、[!UICONTROL Weekly] または [!UICONTROL Google Target CPA] を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceが Target CPA を最適化します。

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

* *[!UICONTROL Target Impression Share]:* （検索ネットワーク上のキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、目標インプレッションシェアと広告掲載順位を達成するように入札を最適化します。 必要に応じて、**[!UICONTROL Target Impression Share]** をパーセント、**[!UICONTROL Target Ad Position]** および **[!UICONTROL Max CPC]** （クリック単価）で入力します。 **メモ：** このオプションは、ハイブリッドポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:* （検索およびショッピングネットワーク上のキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、パーセン **[!UICONTROL Target ROAS]** ー（広告費用対効果）に基づいて入札を最適化します（割合で指定）。 必要に応じて、**[!UICONTROL Max CPC]** （クリック単価）を入力し、広告ネットワークがクリックごとに特定の金額以上を支払わないようにします。 **メモ：** このオプションは、[!UICONTROL Weekly] または [!UICONTROL Google Target ROAS] を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します。 ハイブリッドポートフォリオでは、検索、ソーシャルおよびCommerceが Target ROAS を最適化します。

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）次の国
キャンペーンの商品は販売されています。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** （オーディエンスキャンペーンのみ。オプション）レスポンシブ広告ではなく、自動化されたフィードベース広告のために、キャンペーンを特定のマーチャントセンターストアにリンクします。 このオプションを選択する場合は、[!UICONTROL Merchant ID] と [!UICONTROL Products] を指定します。 キャンペーンの広告グループを作成する必要がありますが、広告を作成する必要はありません。

キャンペーンをストアにリンクして設定を保存すると、このオプションを変更できなくなります。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** （マーチャントセンターストアにリンクされたオーディエンスキャンペーンのみ）広告する製品。 デフォルトでは、*[!UICONTROL All products]* が選択されています。 特定の属性を持つ製品のみをアドバタイズするには、「*[!UICONTROL Filter products]*」を選択し、製品をフィルタリングするための製品ディメンションと属性の組み合わせを最大 7 つ指定します。 製品に広告を表示するには、指定したすべての値が該当する必要があります。 例えば、Acme のペット用品の広告を表示するには、`Custom Label 1=animals`、`Category=pet supplies`、`Brand=Acme Pet Supplies` のフィルターを作成します。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** （Performance MAX キャンペーンのみ）広告の言語。広告が表示されるサイトの言語と一致する必要があります。 [!DNL Microsoft Advertising] は、ユーザーのクエリ、発行者の国、ユーザーの言語設定など、様々なシグナルからユーザーの言語を決定します。

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

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

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** （ディスプレイ/ネイティブネットワーク上のキャンペーンのみ。オプション）広告を表示しないディスプレイネットワーク上のサイト。 www.example.comのように、有効な URL を入力します。 複数の文字列を指定する場合は、コンマで区切るか、別の行に入力します。

公開について詳しくは、Microsoft Advertisingのヘルプで「[&#x200B; 特定の web サイトに広告が表示されないようにする &#x200B;](https://help.ads.microsoft.com/#apex/bae/en/14061/0) を参照してください。

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

**[!UICONTROL Asset Group Name]:** アセットフォルダー（アセットグループ）の名前。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス：*[!UICONTROL Active]* または *[!UICONTROL Paused]*。

**[!UICONTROL Final URL]:** アセットグループから作成されたすべての広告の最終的な URL。

**[!UICONTROL Images]:** 少なくとも 1 つの正方形の画像と 1 つの風景の画像を含む、広告の最大 20 の画像。 [[!DNL Microsoft Advertising]  画像のガイドライン &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60204/0) を参照してください。 画像は、アップロードすることも、[!UICONTROL Asset Library] ージから選択することもできます。ただし、同じ操作で両方を選択することはできません。

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

**[!UICONTROL Logos]:** 1 つ以上のロゴ。 最大 5 つを含めることができます。 [[!DNL Microsoft Advertising]  アセットガイドライン &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60204/0) を参照してください。 画像は、アップロードすることも、[!UICONTROL Asset Library] ージから選択することもできます。ただし、同じ操作で両方を選択することはできません。

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

**[!UICONTROL Headlines]:** 少なくとも 3 つの最大 15 文字の短い見出し。各見出しは最大 30 文字です。 テキストを入力するか、[!UICONTROL Asset Library] ージからアセットを選択できますが、同じ操作で両方を選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、「**[!UICONTROL + Add]**」をクリックして文字列を入力します。

* [!UICONTROL Asset Library] ージからアセットを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてアセットを選択します。

**[!UICONTROL Long Headlines]:** 少なくとも 1 つ、最大 5 つの長い見出し（それぞれ最大 90 文字）。 テキストを入力するか、[!UICONTROL Asset Library] ージからアセットを選択できますが、同じ操作で両方を選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、「**[!UICONTROL + Add]**」をクリックして文字列を入力します。

* [!UICONTROL Asset Library] ージからアセットを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてアセットを選択します。

**[!UICONTROL Descriptions]:** 少なくとも 2 つ、最大 5 つの説明（それぞれ最大 90 文字）。 テキストを入力するか、[!UICONTROL Asset Library] ージからアセットを選択できますが、同じ操作で両方を選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、「**[!UICONTROL + Add]**」をクリックして文字列を入力します。

* [!UICONTROL Asset Library] ージからアセットを選択するには、「選 **[!UICONTROL Asset Library]**」をクリックしてアセットを選択します。

**[!UICONTROL Call to Action]:** 広告に含めるコールトゥアクション。 デフォルトでは、*[!UICONTROL Act Now]* が選択されています。

**[!UICONTROL Business Name]:** ビジネス名（最大 25 文字）。 スクリプト、HTML、またはその他のマークアップ言語を含めることはできません。

**[!UICONTROL Audience Signal]:** （任意）キャンペーンのオーディエンスシグナルとして使用するオーディエンスを [!DNL Microsoft Advertising] 定します。 機械学習モデル [!DNL Microsoft Advertising]、オーディエンスを使用して、ターゲットとする類似の web サーファーを見つけます。また、パフォーマンス目標を達成するのに役立つシグナルとして指定されていないオーディエンスに広告を表示することもあります。 コンバージョンする可能性が最も高いオーディエンスを選択します。

>[!NOTE]
>オーディエンスシグナルは、[&#x200B; 広告グループレベルのオーディエンスターゲット &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) とは異なります。

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** 別のアセットグループを指定できます。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** *[!UICONTROL Use account conversion goals for this campaign]* （デフォルト）か *[!UICONTROL Use campaign specific conversion goals]*。 キャンペーンのコンバージョン目標を指定する場合は、使用可能なすべての目標のリストから目標を選択します。 **メモ：** 目標は毎日同期されるので、過去 24 時間に作成された目標はリストされない場合があります。 リストを更新するには、[&#x200B; 広告ネットワークデータを手動で同期 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/sync-network.md) します。

>[!TIP]
>
>キャンペーンがハイブリッドポートフォリオの一部である場合は、ポートフォリオの目的のコンバージョン目標に一致するキャンペーンレベルの目標を使用することがベストプラクティスです。追加のコンバージョン目標を含めると、ポートフォリオのパフォーマンスに影響を与える可能性があります。
>
> ただし、ハイブリッドポートフォリオ内のキャンペーンで [&#x200B; 広告ネットワークに目標をアップロード &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md) する場合は、ここではなく、広告ネットワークのエディター内で次の操作を行います。a） アップロードした検索、ソーシャルおよびCommerceのポートフォリオ目標指標（「O_ACS_OBJ」で始まる）をキャンペーンのコンバージョン目標として追加し、b）広告ネットワーク追跡指標は広告ネットワークにアップロードされないので、[!DNL Microsoft Advertising] ユニバーサルイベントトラッキング（UET） タグでで追跡されるコンバージョンをを含める目標を追加します。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
