---
title: "[!DNL Microsoft Advertising] キャンペーン設定"
description: 次の設定を参照してください： [!DNL Microsoft Advertising] キャンペーン。
source-git-commit: 0706f4dbc5f2a27e7d0cf43a6865d242865f9d36
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] キャンペーン設定

## \[ キャンペーン作成画面\]

**[!UICONTROL Campaign Type]:** （キャンペーンの作成時のみ使用可能）広告を配置する場所と、キャンペーンに含めることのできる広告タイプ：

* *[!UICONTROL Search and Display Network]:* 検索ネットワーク上のテキスト広告のみを表示します。

* *[!UICONTROL Shopping Network]:* お使いの製品の製品広告を表示します [!DNL Microsoft Merchant Center] 商品カタログ — ショッピングネットワーク上

* *[!UICONTROL Audience]:* 上にネイティブ/ディスプレイ広告を表示 [!DNL Microsoft Audience Network]. (a) キャンペーンを [!UICONTROL Shopping Settings] セクションまたは b) テキストアセットとアップロードされた画像を使用してレスポンシブ広告を作成する。 どちらのオプションを使用する場合も、ユーザーターゲティングを持つ広告グループを作成する必要があります。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。 最大長は 128 文字です。

**[!UICONTROL Status]:** キャンペーンの表示ステータス： *アクティブ* または *一時停止*. 新しい広告キャンペーンのデフォルトは、 *アクティブ*.

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

* *[!UICONTROL Enhanced CPC]:* （オーディエンス、検索、ショッピングネットワークに関するキャンペーン）広告ネットワークの拡張クリック単価 (eCPC) モデルを使用して、広告ネットワーク内のコンバージョン（検索、ソーシャル、コマースではなく）を使用し、平均 CPC を下に保つ最大 CPC。

eCPC を持つキャンペーンを最適化された検索、ソーシャル、コマースのポートフォリオに追加すると、検索、ソーシャル、コマースがベース入札を最適化し、[!UICONTROL Auto adjust campaign budget limits]「 」オプションは有効です — キャンペーンの予算です。 広告ネットワークは、すべての入札調整を最適化し、独自のデータとインサイトに基づいて、ユーザークエリの実行時に検索、ソーシャル、コマースで生成された入札を変更する場合があります。 **注意：** ポートフォリオで eCPC キャンペーンを使用するのは、広告ネットワークで追跡される合計コンバージョンがポートフォリオの目標と一致する場合のみです。

* *[!UICONTROL Manual CPC]* （デフォルト）:( 非推奨： [!DNL Microsoft Advertising] （2021 年） CPC（コストパークリック）モデルを使用します。 オプションで、広告ネットワークにキャンペーンの入札の変更を許可できます。

   * **[!UICONTROL Enable Enhanced CPC]** （デフォルトでは無効）:これは、[!UICONTROL Enhanced CPC]&quot;オプション。

* *[!UICONTROL Manual CPM]* （オーディエンスネットワーク上のキャンペーンのみ）1,000 件のインプレッションに費やす費用 (CPM) モデルを使用します。CPM モデルでは、1,000 件のインプレッションにつき使用する費用を指定します。 この入札戦略を使用するキャンペーンがポートフォリオに含まれる場合、最適化されません。

* *[!UICONTROL Maximize Clicks]:* （検索および買い物キャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークが入札を最適化して、クリック数を最大化します。 必要に応じて、 **[!UICONTROL Max CPC]** （クリックあたりのコスト）を使用して、広告ネットワークが各クリックに対して特定の金額を超えないようにします。 **注意：** この戦略を持つキャンペーンをポートフォリオに追加すると、入札は、ポートフォリオの目的ではなく、クリックの重み付けによって駆動されます。

* *[!UICONTROL Maximize Conversion Value]:* （検索およびショッピング/スマートショッピングネットワーク）検索、ソーシャル、コマースではなく、広告ネットワークは、コンバージョン値を最大化するために入札を最適化します。 必要に応じて、 **[!UICONTROL Target Return on Ad Spend]** (ROAS) を割合で示します。 **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンで使用しますが、標準のポートフォリオでは使用しません。

* *[!UICONTROL Maximize Conversions]:* ( 検索ネットワーク上のキャンペーン <!-- future: and audience network -->) 広告ネットワーク（検索、ソーシャル、コマースではなく）は、コンバージョンを最大化するために入札を最適化します。 必要に応じて、 **[!UICONTROL Target CPC]** （クリックあたりのコスト）<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **注意：** このオプションは、ハイブリッドポートフォリオのキャンペーンで使用しますが、標準のポートフォリオでは使用しません。

* *[!UICONTROL Target CPA]:* （検索ネットワーク上のキャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークは、オプションのに基づいて入札を最適化します **[!UICONTROL Target CPA]** （獲得あたりのコスト）：獲得（コンバージョン）に対して支払う 30 日間の平均金額。 **注意：** このオプションは、支出戦略を除くハイブリッドポートフォリオのキャンペーン（標準のポートフォリオではない）に使用します。 [!UICONTROL Weekly] または [!UICONTROL Google Target CPA].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データを使用できません。

* *[!UICONTROL Target Impression Share]:* （検索ネットワーク上のキャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークは、ターゲットのインプレッション共有および広告の位置を達成するために、入札を最適化します。 必要に応じて、 **[!UICONTROL Target Impression Share]** パーセント **[!UICONTROL Target Ad Position]**、および **[!UICONTROL Max CPC]** （クリックあたりのコスト）。 **注意：** このオプションは、ハイブリッドポートフォリオではサポートされていません。

* *[!UICONTROL Target Return on Ad Spend]:*  （検索およびショッピングネットワーク上のキャンペーン）検索、ソーシャル、コマースではなく、広告ネットワークは、ユーザーの **[!UICONTROL Target ROAS]** （広告費用対効果）。割合で指定します。 必要に応じて、 **[!UICONTROL Max CPC]** （クリックあたりのコスト）を使用して、広告ネットワークがクリックごとに特定の金額を超えないようにします。 **注意：** このオプションは、支出戦略を除くハイブリッドポートフォリオのキャンペーン（標準のポートフォリオではない）に使用します。 [!UICONTROL Weekly] または [!UICONTROL Google Target ROAS].

  この入札戦略を使用するキャンペーンでは、平均順位と CPC 入札データを使用できません。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** ( 買い物キャンペーンのみ、既存のキャンペーンの読み取り専用 ) キャンペーンの製品が販売された国。 製品は対象国に関連付けられているので、この設定によってキャンペーンで広告される製品が決まります。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** ( オーディエンスキャンペーンのみ、（オプション）レスポンシブ広告ではなく、フィードベースの自動広告を提供する、特定のマーチャントセンターストアとキャンペーンをリンクします。 このオプションを選択する場合、 [!UICONTROL Merchant ID] および [!UICONTROL Products]. キャンペーン用の広告グループを作成する必要がありますが、広告を作成する必要はありません。

キャンペーンをストアにリンクし、設定を保存した後は、このオプションを変更できません。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** （マーチャントセンターの店舗にリンクされたオーディエンスキャンペーンのみ）広告を提供する製品。 デフォルトでは、 *[!UICONTROL All products]* が選択されている。 特定の属性を持つ製品のみをアドバタイズするには、「 」を選択します。 *[!UICONTROL Filter products]* 製品をフィルタリングする製品ディメンションと属性の組み合わせを 7 つまで指定できます。 指定されたすべての値は、製品に表示される広告に適用できる必要があります。 例えば、Acme のペット用品の広告を表示するには、フィルターを作成します `Custom Label 1=animals`, `Category=pet supplies`、および `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

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

**[!UICONTROL Negative Websites]:** ( ディスプレイ/ネイティブネットワーク上のキャンペーンのみ。（オプション）広告を表示したくないディスプレイネットワーク上のサイト。 有効な URL( 例： www.example.com) を入力します。 複数の文字列を指定するには、コンマで区切るか、複数の文字列を別々の行に入力します。

可用性について詳しくは、 Microsoft Advertising のヘルプで[特定の Web サイトに広告が表示されないようにする](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

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

>[!MORELIKETHIS]
>
>* [キャンペーンの管理](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
