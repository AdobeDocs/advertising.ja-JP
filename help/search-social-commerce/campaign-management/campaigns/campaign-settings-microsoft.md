---
title: '[!DNL Microsoft Advertising] キャンペーン設定'
description: ' [!DNL Microsoft Advertising]  キャンペーンの設定を参照します。'
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/1odLCTaPgF8iGeVgys2j124fhX1K208YYq0ftDp9l7w
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 3111796b54e2e633ca734c7141efbc2d82f3087d
workflow-type: tm+mt
source-wordcount: 2112
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キャンペーン設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーン作成時のみ利用可能）広告を配置する場所、および広告の種類
キャンペーンには、次の要素が含まれます。

* *[!UICONTROL Search]:*&#x200B;検索ネットワークにテキスト広告を表示します。

* *[!UICONTROL Shopping Network]:*&#x200B;は、お客様の[!DNL Microsoft Merchant Center]製品カタログ内の製品に関する製品広告をショッピング ネットワークに表示します。

* *[!UICONTROL Audience]:* [!DNL Microsoft Audience Network]にネイティブ/ディスプレイ広告を表示します。 a） [!UICONTROL Shopping Settings] セクションのマーチャント センターのストアにキャンペーンをリンクして、フィード ベースの広告を自動的に生成するか、b） テキストアセットとアップロードされた画像を含むレスポンシブ広告を作成できます。 どちらのオプションでも、ユーザーターゲティングを使用して広告グループを作成する必要があります。

* *[!UICONTROL Shopping Campaigns for Brands]:*&#x200B;は、検索およびオーディエンスネットワークを通じて、リンクされた小売業者を通じて製品を宣伝します。 子の広告グループと製品グループ（プロモーションするアプリ）を作成し、キャンペーンのオプションの製品広告を作成できます。[!DNL Microsoft Advertising]は製品グループの広告を自動的に作成します。 ブランドのショッピング キャンペーンの場合は、入札戦略[!UICONTROL Manual CPC]を使用します。ブランドのショッピング プロモーションの場合は、入札戦略[!UICONTROL Cost per Sale]を使用します。

* *[!UICONTROL Microsoft Store Ads Campaign]:*&#x200B;は、[!DNL Microsoft Store]で利用可能なアプリとゲームを宣伝します。 キャンペーンの子広告グループ、製品グループ、およびオプションの製品広告を作成できます。[!DNL Microsoft Advertising]は製品グループの広告を自動的に作成します。

* *[!UICONTROL Audience CTV Video]:* オーディエンスネットワーク上のコネクテッド TV （CTV） ビデオ広告を表示します。

* *[!UICONTROL Audience Video]:* オーディエンスネットワーク上に標準ビデオ広告を表示します。

* *[!UICONTROL Performance Max]:* [!DNL Microsoft Advertising] スマート入札を使用して、すべてのネットワークで複数の広告タイプを表示します。 キャンペーン設定では、画像、ロゴ、見出し、説明、オプションのcall to action、オーディエンスシグナルなど、1つ以上のアセットグループを指定する必要があります。 広告ネットワークは、アセットを自動的に組み合わせて、チャネルにもとづいて広告を配信します。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。 最大長は128文字です。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新規広告キャンペーンのデフォルトは&#x200B;*アクティブ*&#x200B;です。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:** （欧州連合（EU）のオーディエンスをターゲットとするキャンペーンに適用）キャンペーンに、EU規則2024/90に基づいて欧州連合で配信される広告の要件に従った政治的広告が含まれているかどうか：*[!UICONTROL Yes]*&#x200B;または&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Cost per Sale]:* （ショッピング キャンペーンのみ）検索、ソーシャル、Commerceではなく、広告ネットワークが[!UICONTROL Target CPS] （販売単価）に基づいて入札を最適化します。 料金は、商品広告をクリックするだけで24時間以内に販売が成立した場合にのみ支払われます。 **注：** ポートフォリオにこの入札戦略を含むキャンペーンを含めないでください。 Search, Social, &amp; Commerce optimizationは、この入札戦略を持つキャンペーンでは使用できません。

  この入札戦略を使用してブランドのショッピング キャンペーンを保存すると、入札戦略を変更することはできません。 その他のショッピングキャンペーンの種類については、この戦略は新しいキャンペーンでのみ使用できます。

* *[!UICONTROL CPV]* （Audience CTV ビデオ キャンペーンのみ）は、CPV モデルを使用します。 Search, Social, &amp; Commerceでは、ポートフォリオに含まれる入札戦略に基づいてキャンペーンを最適化できません。

* *[!UICONTROL Enhanced CPC]:* （オーディエンス、検索、ショッピング ネットワーク上のキャンペーン）広告ネットワークの強化されたクリック単価（eCPC）モデルを使用しています。これにより、広告ネットワークは、平均CPCを最大CPC未満に保ちながら、広告ネットワーク内で指定されたコンバージョンを使用して、コンバージョンを最大化しようとしながら、各オークションのクリック単価（CPC）入札を自動的に変更できます。

  eCPCを使用したキャンペーンを最適化されたSearch, Social, &amp; Commerce ポートフォリオに追加すると、Search, Social, &amp; Commerceは基本入札を最適化し、「[!UICONTROL Auto adjust campaign budget limits]」オプションが有効になっている場合はキャンペーンの予算を最適化します。 広告ネットワークは、すべての入札調整を最適化し、独自のデータとインサイトに基づいて、ユーザークエリの時点でSearch、Social、Commerce生成の入札を変更する可能性があります。 **注意：** ポートフォリオでeCPC キャンペーンを使用するのは、広告ネットワークで追跡されたコンバージョンの合計数がポートフォリオ目標に一致する場合のみです。

* *[!UICONTROL Manual CPC]*: （ブランドのショッピング キャンペーン；[!DNL Microsoft Store Ads] キャンペーン。他のキャンペーンタイプでは非推奨）クリック単価（CPC）モデルを使用します。 一部の広告タイプでは、オプションで広告ネットワークがキャンペーンの入札額を変更できるようにすることができます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）：このオプションは、「[!UICONTROL Enhanced CPC]」オプションを使用する場合と同じです。

* *[!UICONTROL Manual CPA]:* （[!DNL Microsoft Store Ads] キャンペーン）は、CPA （顧客獲得単価）モデルを使用します。

* *[!UICONTROL Manual CPM]* （オーディエンスキャンペーンとオーディエンスビデオキャンペーンのみ）は、1,000回のインプレッションあたりの費用を指定する数千インプレッション単価（CPM）モデルを使用します。 この入札戦略を採用したキャンペーンは、ポートフォリオに含まれると最適化されません。

* *[!UICONTROL Maximize Clicks]:* （検索およびショッピング キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが入札を最適化してクリック数を最大化します。 オプションで&#x200B;**[!UICONTROL Max CPC]** （クリック単価）を入力して、広告ネットワークがクリックごとに特定の金額を超えて支払わないようにします。 **注意：**&#x200B;この戦略を含むキャンペーンをポートフォリオに追加すると、クリックの重み（ポートフォリオの目標ではない）が入札を促進します。

* *[!UICONTROL Maximize Conversion Value]:* （検索とショッピング/スマートショッピングのネットワーク、パフォーマンスの最大キャンペーン）検索、ソーシャル、Commerceではなく、広告ネットワークが入札を最適化してコンバージョンの価値を最大化します。 オプションで&#x200B;**[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセントとして入力します。 **注：** ハイブリッドポートフォリオのキャンペーンには、このオプションを使用しますが、標準ポートフォリオには使用しません。 ハイブリッド型ポートフォリオでは、Search, Social, &amp; CommerceがTarget ROASを最適化します。

* *[!UICONTROL Maximize Conversions]:* （検索ネットワークまたはオーディエンスネットワーク上のPerformance max キャンペーンおよびキャンペーン （オーディエンスビデオまたはコネクテッド TVは除く））検索、ソーシャル、およびCommerceではなく、広告ネットワークが入札を最適化してコンバージョンを最大化します。 オプションで&#x200B;**[!UICONTROL Target CPC]** （クリック単価）を入力します。 オーディエンスキャンペーンの場合は、オプションの&#x200B;**[!UICONTROL Target CPA]** （獲得単価）を入力することもできます。 **注：** ハイブリッドポートフォリオのキャンペーンには、このオプションを使用しますが、標準ポートフォリオには使用しません。 Search, Social, &amp; Commerceのハイブリッドポートフォリオでは、Target CPAが最適化されています。

* *[!UICONTROL Target CPA]:* （検索ネットワーク上のキャンペーン） Search, Social, &amp; Commerceではなく、広告ネットワークは、オプションの&#x200B;**[!UICONTROL Target CPA]** （顧客獲得単価）に基づいて入札を最適化します。これは、顧客獲得（コンバージョン）に対して支払う30日間の平均金額です。 **注：**&#x200B;このオプションは、[!UICONTROL Weekly]または[!UICONTROL Google Target CPA]を除く任意の支出戦略を持つハイブリッドポートフォリオ（標準ポートフォリオではない）のキャンペーンに使用します。 Search, Social, &amp; Commerceのハイブリッドポートフォリオでは、Target CPAが最適化されています。

  平均順位とCPC入札データは、この入札戦略を持つキャンペーンでは利用できません。

* *[!UICONTROL Target Impression Share]:* （検索ネットワーク上のキャンペーン） Search, Social, &amp; Commerceではなく、広告ネットワークが入札を最適化して、ターゲットのインプレッションのシェアと広告ポジションを達成します。 オプションで、**[!UICONTROL Target Impression Share]**&#x200B;をパーセント、**[!UICONTROL Target Ad Position]**&#x200B;および&#x200B;**[!UICONTROL Max CPC]** （クリック単価）として入力します。 **注：**&#x200B;このオプションは、ハイブリッドポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:* （検索およびショッピング ネットワークのキャンペーン） Search, Social, &amp; Commerceではなく、広告ネットワークは、割合で指定された&#x200B;**[!UICONTROL Target ROAS]** （広告費用対効果）に基づいて入札を最適化します。 オプションで&#x200B;**[!UICONTROL Max CPC]** （クリック単価）を入力して、広告ネットワークがクリックごとに特定の金額を超えて支払わないようにします。 **注：**&#x200B;このオプションは、[!UICONTROL Weekly]または[!UICONTROL Google Target ROAS]を除く任意の支出戦略を持つハイブリッドポートフォリオ（標準ポートフォリオではない）のキャンペーンに使用します。 ハイブリッド型ポートフォリオでは、Search, Social, &amp; CommerceがTarget ROASを最適化します。

  平均順位とCPC入札データは、この入札戦略を持つキャンペーンでは利用できません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** （ショッピング キャンペーンのみ。既存のキャンペーンの読み取り専用）
キャンペーンの商品が販売されています。 製品はターゲット国に関連付けられているため、この設定によって、キャンペーンで宣伝される製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** （オーディエンスキャンペーンのみ。オプション）レスポンシブ広告ではなく、自動フィード ベースの広告用に、特定のマーチャント センターのストアにキャンペーンをリンクします。 このオプションを選択する場合は、[!UICONTROL Merchant ID]と[!UICONTROL Products]を指定します。 キャンペーン用に広告グループを作成する必要がありますが、広告を作成する必要はありません。

キャンペーンをストアにリンクして設定を保存すると、このオプションを変更することはできません。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** （マーチャント センターのストアにリンクされたオーディエンス キャンペーンのみ）広告する製品。 デフォルトでは、*[!UICONTROL All products]*&#x200B;が選択されています。 特定の属性を持つ製品のみを広告するには、*[!UICONTROL Filter products]*&#x200B;を選択し、製品をフィルタリングする製品ディメンションと属性の組み合わせを最大7つ指定します。 製品に広告を表示するには、指定したすべての値を適用する必要があります。 例えば、Acme ペット用品の広告を表示するには、フィルター`Custom Label 1=animals`、`Category=pet supplies`、`Brand=Acme Pet Supplies`を作成します。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** （Performance max キャンペーンのみ）広告の言語。広告を表示できるサイトの言語と一致する必要があります。 [!DNL Microsoft Advertising]は、ユーザーのクエリ、発行者の国、ユーザーの言語設定など、様々なシグナルからユーザーの言語を決定します。

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

**[!UICONTROL Negative Websites]:** （ディスプレイ/ネイティブネットワーク上のキャンペーンのみ。オプション）広告を表示しないディスプレイネットワーク上のサイト。 www.example.comなどの有効なURLを入力します。 複数の文字列を指定するには、それらをコンマで区切るか、別々の行に入力します。

利用方法について詳しくは、「[特定のweb サイトに広告が表示されないようにする](https://help.ads.microsoft.com/#apex/bae/en/14061/0)」のMicrosoft Advertising ヘルプを参照してください。

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

**[!UICONTROL Track Product Group]:** （[!UICONTROL EF Redirect]のみ）実装されていません

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （アセットグループごと）

**[!UICONTROL Asset Group Name]:** アセットフォルダー（アセットグループ）の名前。

**[!UICONTROL Asset Group Status]:** アセットグループのステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。

**[!UICONTROL Final URL]:** アセットグループから作成されたすべての広告の最終URL。

**[!UICONTROL Images]:**&#x200B;少なくとも1つの正方形の画像と1つの横長の画像を含む、広告の最大20枚の画像。 [[!DNL Microsoft Advertising] 画像のガイドライン &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60204/0)を参照してください。 画像をアップロードするか、[!UICONTROL Asset Library]から選択できますが、両方を同じ操作で選択することはできません。

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

**[!UICONTROL Logos]:**&#x200B;少なくとも1つのロゴ。 5つまで含めることができます。 [[!DNL Microsoft Advertising]  アセットガイドライン &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60204/0)を参照してください。 画像をアップロードするか、[!UICONTROL Asset Library]から選択できますが、両方を同じ操作で選択することはできません。

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

**[!UICONTROL Headlines]:**&#x200B;少なくとも3つ、最大15個の短い見出し。各見出しは最大30文字です。 テキストを入力するか、[!UICONTROL Asset Library]からアセットを選択できますが、両方を同じ操作で選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、文字列を入力します。

* [!UICONTROL Asset Library]からアセットを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてアセットを選択します。

**[!UICONTROL Long Headlines]:**&#x200B;少なくとも1つ、最大5つの長い見出し（各90文字まで）。 テキストを入力するか、[!UICONTROL Asset Library]からアセットを選択できますが、両方を同じ操作で選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、文字列を入力します。

* [!UICONTROL Asset Library]からアセットを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてアセットを選択します。

**[!UICONTROL Descriptions]:**&#x200B;少なくとも2文字、最大5文字の説明で、各文字は最大90文字です。 テキストを入力するか、[!UICONTROL Asset Library]からアセットを選択できますが、両方を同じ操作で選択することはできません。

* テキストを入力するには：

   1. 「[!UICONTROL Enter Text]」タブで、テキストを入力します。

   1. （オプション）別のテキスト文字列を追加するには、**[!UICONTROL + Add]**&#x200B;をクリックし、文字列を入力します。

* [!UICONTROL Asset Library]からアセットを選択するには、**[!UICONTROL Asset Library]**&#x200B;をクリックしてアセットを選択します。

**[!UICONTROL Call to Action]:**&#x200B;広告に含めるcall to action。 デフォルトでは、*[!UICONTROL Act Now]*&#x200B;が選択されています。

**[!UICONTROL Business Name]:** ビジネス名（最大25文字）。 スクリプト、HTML、その他のマークアップ言語を含めることはできません。

**[!UICONTROL Audience Signal]:** （オプション） キャンペーンのオーディエンスシグナルとして使用する[!DNL Microsoft Advertising] オーディエンス。 [!DNL Microsoft Advertising]個のマシンラーニング モデルは、オーディエンスを使用して、ターゲットとする類似のweb サーファーを見つけます。また、シグナルとして指定されていないオーディエンスに広告を表示して、パフォーマンス目標を達成するのに役立てることもできます。 コンバージョンに至る可能性が最も高いオーディエンスを特定：

>[!NOTE]
>オーディエンスシグナルは、[広告グループレベルのオーディエンスターゲット &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)とは異なります。

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:**&#x200B;別のアセットグループを指定できます。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** *[!UICONTROL Use account conversion goals for this campaign]* （既定値）か&#x200B;*[!UICONTROL Use campaign specific conversion goals]*&#x200B;かのどちらかです。 キャンペーンのコンバージョン目標を指定する場合は、使用可能なすべての目標のリストから目標を選択します。 **注：**&#x200B;目標は毎日同期されるため、過去24時間に作成された目標は一覧表示されない場合があります。 リストを更新するには、[広告ネットワークデータを手動で同期します](/help/search-social-commerce/campaign-management/campaigns/sync-network.md)。

>[!TIP]
>
>キャンペーンがハイブリッドポートフォリオの一部である場合、ベストプラクティスは、ポートフォリオの目的のコンバージョン目標に一致するキャンペーンレベルの目標を使用することです。追加のコンバージョン目標を含めると、ポートフォリオのパフォーマンスに影響を与える可能性があります。
>
> ただし、[目標を広告ネットワークにアップロード &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md)するハイブリッドポートフォリオのキャンペーンの場合は、ここで設定する代わりに、広告ネットワークのエディター内で次の操作を行います。a）アップロードされたSearch, Social, &amp; Commerce ポートフォリオの目標指標（「O_ACS_OBJ」で始まる）をキャンペーンのコンバージョン目標として追加し、b）広告ネットワークにアップロードされた指標が広告ネットワークにアップロードされないので、[!DNL Microsoft Advertising] ユニバーサルイベントトラッキング（UET）タグが含されます。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
