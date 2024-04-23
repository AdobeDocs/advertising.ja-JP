---
title: '''[!DNL Microsoft® Advertising] キャンペーン設定'
description: の設定を参照します [!DNL Microsoft® Advertising] キャンペーン。
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 8d1ff29322799ff7905ee808703e00f5190ae8af
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] キャンペーン設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーンの作成時にのみ使用できます）広告の配置場所と、キャンペーンに含めることができる広告タイプは次のとおりです。

* *[!UICONTROL Search]:* 検索ネットワークのテキスト広告を表示します。

* *[!UICONTROL Shopping Network]:* 製品の広告を表示します – に含まれる製品の [!DNL Microsoft® Merchant Center] 製品カタログ：ショッピング・ネットワーク上。

* *[!UICONTROL Audience]:* のネイティブ/ディスプレイ広告を表示 [!DNL Microsoft® Audience Network]. a） キャンペーンを次のマーチャントセンターストアにリンクすることで、フィードベースの広告を自動的に生成できます [!UICONTROL Shopping Settings] セクションまたは b） テキストアセットとアップロードした画像を使用してレスポンシブ広告を作成します。 どちらのオプションでも、ユーザーターゲティングを使用して広告グループを作成する必要があります。

* *[!UICONTROL Shopping Campaigns for Brands]:* （ベータ版機能）検索およびオーディエンスネットワーク全体でリンクされた小売業者を通じて製品を宣伝します。 キャンペーンの子広告グループと製品グループ（昇格するアプリ）、およびオプションの製品広告を作成できます。 [!DNL Microsoft® Advertising] 製品グループの広告を自動的に作成します。 ブランドのショッピングキャンペーンの場合は、入札戦略を使用します [!UICONTROL Manual CPC]; ブランドのショッピングプロモーションの場合は、入札戦略を使用します [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft® Store Ads Campaign]:* （ベータ版機能）で利用可能なアプリやゲームを昇格します。 [!DNL Microsoft® Store]. キャンペーンの子広告グループ、製品グループおよびオプションの製品広告を作成できます。 [!DNL Microsoft® Advertising] 製品グループの広告を自動的に作成します。

* *[!UICONTROL Audience CTV Video]:* （ベータ版機能）接続された TV （CTV）ビデオ広告をオーディエンスネットワークで表示します。

* *[!UICONTROL Audience Video]:* （ベータ版機能）オーディエンスネットワーク上の標準ビデオ広告を表示します。

* *[!UICONTROL Performance Max]:* （ベータ版機能）を使用して、すべてのネットワークにわたって複数の広告タイプを表示します [!DNL Microsoft® Advertising] スマート入札。 キャンペーンの設定内で、1 つ以上のアセットグループを指定する必要があります。このグループには、画像、ロゴ、ヘッドライン、説明、オプションのコールトゥアクション、オーディエンスシグナルが含まれます。 広告ネットワークは、アセットを自動的に組み合わせて、チャネルに基づいて広告を提供します。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。 最大長は 128 文字です。

**[!UICONTROL Status]:** キャンペーンの表示ステータス： *アクティブ* または *一時停止*. 新規広告キャンペーンのデフォルトはです。 *アクティブ*.

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

* *[!UICONTROL Cost per Sale]:* （ショッピングキャンペーンのみ）広告ネットワーク（検索、ソーシャル、Commerceは除く）は、 [!UICONTROL Target CPS] （1 販売あたりのコスト）。 お支払いは、商品の広告をクリックした結果、24 時間以内にセールが成立した場合に限ります。 **注意：** この入札戦略のキャンペーンをポートフォリオに含めないでください。 この入札戦略を使用するキャンペーンでは、検索、ソーシャル、Commerceの最適化は利用できません。

  この入札戦略を使用してブランドのショッピングキャンペーンを保存すると、入札戦略を変更できなくなります。 他のショッピングキャンペーンタイプの場合、この戦略は新規キャンペーンでのみ使用できます。

* *[!UICONTROL CPV]* （オーディエンス CTV ビデオキャンペーンのみ）表示単価（CPV）モデルを使用します。 <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* （オーディエンス、検索、ショッピングネットワーク上のキャンペーン）広告ネットワークの拡張コストパークリック（eCPC）モデルを使用します。これにより、広告ネットワークは各オークションのコストパークリック（CPC）入札を自動的に変更し、コンバージョンを最大化しながら、広告ネットワーク内で指定されたコンバージョン（検索、ソーシャル、Commerceではない）を使用して、平均 CPC を最大 CPC 未満に保つことができます。

  eCPC を使用してキャンペーンを最適化された検索、ソーシャル、Commerce ポートフォリオに追加すると、検索、ソーシャル、Commerceによってベース入札が最適化され、「[!UICONTROL Auto adjust campaign budget limits]「」オプションが有効になっています – キャンペーンの予算。 アドネットワークは、すべての入札調整を最適化し、独自のデータとインサイトに基づいて、ユーザークエリ時に検索、ソーシャル、Commerceで生成された入札を変更する可能性があります。 **注意：** ポートフォリオで eCPC キャンペーンを使用するのは、広告ネットワークで追跡されるコンバージョンの合計がポートフォリオの目的と合致する場合のみです。

* *[!UICONTROL Manual CPC]*: （ブランドのショッピングキャンペーン； [!DNL Microsoft® Store Ads] キャンペーン、廃止者 [!DNL Microsoft® Advertising] 2021 年（その他のキャンペーンタイプの場合） クリック単価（CPC）モデルを使用します。 一部の広告タイプでは、オプションで、広告ネットワークにキャンペーンの入札の変更を許可できます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：このオプションは、「」を使用した場合と同じです[!UICONTROL Enhanced CPC]」オプションを選択します。

* *[!UICONTROL Manual CPA]:* （[!DNL Microsoft® Store Ads] キャンペーン）獲得あたりのコスト（CPA）モデルを使用します。

* *[!UICONTROL Manual CPM]* （オーディエンスキャンペーンおよびオーディエンスビデオキャンペーンのみ） 1,000 回の表示インプレッションごとに使用する費用を指定する、1,000 インプレッションあたりのコスト（CPM） モデルを使用します。 この入札戦略を使用したキャンペーンは、ポートフォリオに含まれている場合、最適化されません。

* *[!UICONTROL Maximize Clicks]:* （検索およびショッピングキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、入札を最適化してクリック数を最大化します。 オプションで、 **[!UICONTROL Max CPC]** （クリックあたりのコスト）広告ネットワークがクリックごとに特定の金額以上を支払わないようにします。 **注意：** この戦略を使用してキャンペーンをポートフォリオに追加すると、（ポートフォリオ目標ではなく）クリックの重みが入札を促進します。

* *[!UICONTROL Maximize Conversion Value]:* （検索およびショッピング/スマートショッピングネットワーク、パフォーマンス最大化キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、コンバージョン値を最大化するように入札を最適化します。 必要に応じて、 **[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセントで表したもの。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。

* *[!UICONTROL Maximize Conversions]:* （検索ネットワークまたはオーディエンスネットワーク（オーディエンスビデオまたは接続された TV を除く）上の Performance MAX のキャンペーンおよびキャンペーン）広告ネットワーク（検索、ソーシャル、Commerceを除く）は、コンバージョンを最大化するように入札を最適化します。 必要に応じて、 **[!UICONTROL Target CPC]** （クリック単価）。 オーディエンスキャンペーンの場合は、オプションのを入力することもできます **[!UICONTROL Target CPA]** （取得あたりのコスト）。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンに使用しますが、標準ポートフォリオでは使用しません。

* *[!UICONTROL Target CPA]:* （検索ネットワーク上のキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、オプションに基づいて入札を最適化します **[!UICONTROL Target CPA]** （1 購入あたりのコスト）獲得（コンバージョン）の支払いに対して支払う 30 日間の平均金額。 **注意：** このオプションは、次を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します [!UICONTROL Weekly] または [!UICONTROL Google Target CPA].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

* *[!UICONTROL Target Impression Share]:* （検索ネットワーク上のキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、目標インプレッションシェアと広告掲載順位を達成するように入札を最適化します。 オプションで、 **[!UICONTROL Target Impression Share]** パーセントで指定すると、 **[!UICONTROL Target Ad Position]**、および **[!UICONTROL Max CPC]** （クリック単価）。 **注意：** このオプションは、ハイブリッドポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:* （検索およびショッピングネットワーク上のキャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが、ユーザーの状況に基づいて入札を最適化します **[!UICONTROL Target ROAS]** （広告費用対効果）。パーセンテージで指定します。 オプションで、 **[!UICONTROL Max CPC]** （クリックあたりのコスト）広告ネットワークがクリックごとに特定の金額以上を支払わないようにします。 **注意：** このオプションは、次を除く任意の支出戦略を持つハイブリッドポートフォリオ（ただし、標準ポートフォリオは除く）のキャンペーンに使用します [!UICONTROL Weekly] または [!UICONTROL Google Target ROAS].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データは利用できません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）キャンペーンの商品が販売される国。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** （オーディエンスキャンペーンのみ。オプション）レスポンシブ広告ではなく、自動化されたフィードベース広告のために、キャンペーンを特定のマーチャントセンターストアにリンクします。 このオプションを選択した場合は、 [!UICONTROL Merchant ID] および [!UICONTROL Products]. キャンペーンの広告グループを作成する必要がありますが、広告を作成する必要はありません。

キャンペーンをストアにリンクして設定を保存すると、このオプションを変更できなくなります。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** （マーチャントセンターストアにリンクされたオーディエンスキャンペーンのみ）広告する製品。 デフォルトでは *[!UICONTROL All products]* が選択されました。 特定の属性を持つ製品のみをアドバタイズするには、 *[!UICONTROL Filter products]* を選択し、製品をフィルタリングする製品ディメンションと属性の組み合わせを最大 7 つ指定します。 製品に広告を表示するには、指定したすべての値が該当する必要があります。 例えば、Acme のペット用品の広告を表示するには、フィルターを作成します `Custom Label 1=animals`, `Category=pet supplies`、および `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** （Performance MAX キャンペーンのみ）広告の言語。広告が表示されるサイトの言語と一致する必要があります。 [!DNL Microsoft® Advertising] ユーザーのクエリ、発行者の国、ユーザーの言語設定など、様々なシグナルからユーザーの言語を決定します。

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

提供状況について詳しくは、Microsoft® Advertising ヘルプを参照してください。[特定の web サイトに広告が表示されないようにする](https://help.ads.microsoft.com/#apex/bae/en/14061/0).」と入力します。

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

**[!UICONTROL Asset Group Name]:** アセットフォルダー（アセットグループ）の名前。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス： *[!UICONTROL Active]* または *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** アセットグループから作成されたすべての広告の最終的な URL。

**[!UICONTROL Images]:** 少なくとも 1 つの正方形の画像と 1 つの横の画像を含む、広告の最大 20 の画像。 を参照してください。 [[!DNL Microsoft® Advertising] 画像のガイドライン](https://help.ads.microsoft.com/#apex/ads/en/60204/0). 画像をアップロードするか、から選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

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

**[!UICONTROL Logos]:** 少なくとも 1 つのロゴ。 最大 5 つを含めることができます。 を参照してください。 [[!DNL Microsoft® Advertising] アセットガイドライン](https://help.ads.microsoft.com/#apex/ads/en/60204/0). 画像をアップロードするか、から選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

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

**[!UICONTROL Headlines]:** 少なくとも 3 つの最大 15 文字の短い見出し（それぞれ最大 30 文字）。 テキストを入力するか、からアセットを選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* テキストを入力するには：

   1. 日 [!UICONTROL Enter Text] タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、 **[!UICONTROL + Add]** と文字列を入力します。

* からアセットを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** アセットを選択します。

**[!UICONTROL Long Headlines]:** それぞれ最大 90 文字の長い見出しを 1 つ以上、最大 5 つ含める。 テキストを入力するか、からアセットを選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* テキストを入力するには：

   1. 日 [!UICONTROL Enter Text] タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、 **[!UICONTROL + Add]** と文字列を入力します。

* からアセットを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** アセットを選択します。

**[!UICONTROL Descriptions]:** 少なくとも 2 つ、最大 5 つの説明（それぞれ最大 90 文字）。 テキストを入力するか、からアセットを選択できます [!UICONTROL Asset Library]  – ただし、同じ操作で両方が同時に実行されるわけではありません。

* テキストを入力するには：

   1. 日 [!UICONTROL Enter Text] タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、 **[!UICONTROL + Add]** と文字列を入力します。

* からアセットを選択するには [!UICONTROL Asset Library]を選択し、 **[!UICONTROL Asset Library]** アセットを選択します。

**[!UICONTROL Call to Action]:** 広告に含めるコールトゥアクション。 デフォルトでは *[!UICONTROL Act Now]* が選択されました。

**[!UICONTROL Business Name]:** ビジネス名（最大 25 文字）。 スクリプト、HTML、またはその他のマークアップ言語を含めることはできません。

**[!UICONTROL Audience Signal]:** （オプション） [!DNL Microsoft® Advertising] キャンペーンのオーディエンスシグナルとして使用するオーディエンス。 [!DNL Microsoft® Advertising] 機械学習モデルでは、オーディエンスを使用して、ターゲットとする類似の web サーファーを見つけます。また、パフォーマンス目標の達成に役立つシグナルとして指定されていないオーディエンスに広告を表示することもできます。 コンバージョンする可能性が最も高いオーディエンスを選択します。

>[!NOTE]
>オーディエンスシグナルは、とは異なります [広告グループレベルのオーディエンスターゲット](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** 別のアセットグループを指定できます。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** 対象 *[!UICONTROL Use account conversion goals for this campaign]* （デフォルト）または *[!UICONTROL Use campaign specific conversion goals]*. キャンペーンのコンバージョン目標を指定する場合は、使用可能なすべての目標のリストから目標を選択します。 **注意：** 目標は毎日同期されるので、過去 24 時間に作成された目標はリストされない場合があります。 リストを更新するには、 [広告ネットワークデータを手動で同期](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

キャンペーンがポートフォリオの一部である場合は、ポートフォリオの目標と同じコンバージョン目標を使用します。 異なるコンバージョン目標を使用すると、ポートフォリオのパフォーマンスに影響を与える可能性があります。

>[!MORELIKETHIS]
>
>* [キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
