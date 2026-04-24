---
title: 広告主アカウント設定
description: 使用可能な広告主設定の説明を参照してください。
role: User, Admin
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# 広告主アカウント設定

*読み取り専用ユーザーは利用できません*

<!-- Not published -->

## [!UICONTROL General]設定

**[!UICONTROL Advertiser Name]:**&#x200B;広告主名。

**[!UICONTROL Category]:**&#x200B;広告主のビジネスが運営されているカテゴリ。 在庫を入札すると、カテゴリがパブリッシャーに通知されます。 広告に適したカテゴリーを選択することを確認してください。そうしないと、メディア企業が広告を却下する可能性があります。

>[!NOTE]
>
>*[!UICONTROL Other]*&#x200B;を選択した場合、広告主はDSP [!DNL On Demand Inventory]にアクセスできません。

**[!UICONTROL Advertiser URL]:**&#x200B;広告主のホームページまたはメイン web サイトのURL （`http://`または`https://`から始まる）。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （新しい広告主アカウントのみ）組織のDSP アカウント用に設定されたすべてのプライベート Exchange フィードを広告主が利用できるようにします。

### [!UICONTROL Adobe IMS IDs]

Adobe CX Enterpriseの他の製品を使用している広告主は、CX Enterpriseの組織固有IDを使用して、一部の製品間でデータを共有できます。 [!UICONTROL Integrations] セクションで特定の製品統合を設定できます。

**[!UICONTROL Account IMS org and ID]:** （複数の広告主を含むCX Enterprise アカウントを通じてライセンス認証されたCX Enterprise製品を追加する広告主。オプション）広告主のCX Enterprise組織ID。

**[!UICONTROL Advertiser IMS org and ID]:** （CX Enterprise製品の直接使用ライセンスを持つ広告主。オプション）広告主のCX Enterprise組織ID。

### [!UICONTROL Integrations]

（オプション）DSP アカウントにリンクされているCX Enterpriseのその他の製品。 製品は、[!UICONTROL Adobe IMS IDs] セクションで指定されているのと同じCX Enterprise組織IDに関連付けられている必要があります。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** （[!DNL Advertising Search, Social, & Commerce]またはAdobe Advertising コンバージョンピクセルを使用する広告主） DSPがアトリビューションデータを交換する[!DNL Search, Social, & Commerce] アカウント。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** （Adobe Analyticsを使用する広告主。オプション。Adobe Advertising コンバージョントラッキングタグを使用して収集されたデータに対してのみ、[!DNL EF Redirect]とトークンのみを含む）DSPがパブリッシャーおよびサプライサイドパートナーから収集したデータを送信する1つ以上の[!DNL Analytics] レポートスイート。 また、Adobe Analyticsは、クライアントサイトから収集したデータをDSPに送信します。

データをレポートスイートに表示するには、適切な[!DNL Search, Social, & Commerce]広告主レベルの設定を有効にする必要があります。 さらに、広告主の[!DNL Analytics] アカウントは、Adobe Advertisingからデータを受信するように設定する必要があります。

>[!WARNING]
>
>以前にリンクされたレポートスイートを削除すると、DSPはそのスイートとのデータ交換を行わなくなります。 データの変動を確認できます。

[!DNL Analytics]との統合について詳しくは、「[ [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)の概要」を参照してください。

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** （Adobe Audience ManagerまたはAdobe Analyticsを使用している広告主。オプション）広告主のすべてのAdobe オーディエンスに対して、DSPがセグメントメタデータ、階層データ、一意のオーディエンスデータを取り込むAudience Managerまたは[!DNL Analytics] アカウント。 これには、次のデータが含まれます。

* Audience Manager セグメント
* Adobe CX Enterpriseに公開されている[!DNL Analytics] セグメント
* Adobe CX Enterprise [!DNL Audience Library]を使用して作成されたセグメント
* Adobe Experience Platformで作成され、Audience Manager経由でAdobe Advertisingに送信されるセグメント

最初の同期は約24時間かかります。 その後、データはリアルタイムで同期され、1～2秒間の遅延が発生します。
<!--
 I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting]設定

オプションで、広告主の新しいプレースメントのデフォルトターゲットを設定できます。 ユーザーは、新しいプレースメントのデフォルトターゲットを上書きできます。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:**&#x200B;各プレースメントの地域ターゲティングの既定の国。 ユーザーは国を変更し、各プレースメントに対してより具体的な地域ターゲティングを設定できます。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:**&#x200B;既定で抑制するオーディエンスまたはセグメント。 ユーザーは、プレースメントごとに除外を変更できます。

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

適用する[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]および[!DNL Peer39]のコンテキストフィルターの種類。 広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md)で上書きできます。

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （オプション）既定でブロックする1つ以上の種類のインベントリ コンテキスト。 追加料金が適用される場合があります。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （オプション）デフォルトでターゲットにする1つ以上のタイプのインベントリ属性。 追加料金が適用される場合があります。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする1つ以上のタイプのインベントリ属性。 追加料金が適用される場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Optional) The degree of adult content for which to block ads by default: *[!UICONTROL Do Not Block]* (the default), *[!UICONTROL Standard]*, or *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

**[!UICONTROL Alcohol Content]:** (Optional) The degree of alcohol content for which to block ads by default: *[!UICONTROL Do Not Block]* (the default), *[!UICONTROL Standard]*, or *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Types of sites to block based on fraudulent traffic and suspicious activities measured through [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39]. 広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md)で上書きできます。

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** By default, blocks all 100% invalid traffic, including traffic on hijacked devices, for new placements. 追加料金が適用される場合があります。

**[!UICONTROL Also block sites with]:** (Optional) An additional level of fraud and invalid traffic that causes DSP to block ads by default:  *[!UICONTROL None]* (the default, which doesn&#39;t block additional traffic), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, or *[!UICONTROL >25% Average Fraud/IVT levels]*. 追加料金が適用される場合があります。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Optional) One or more types of fraud that cause DSP to block ads by default: *[!UICONTROL Fraud]* (which blocks all sites with fraud), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, and/or *[!UICONTROL Fraud: Zero Ads]*. 追加料金が適用される場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Optional) A type of suspicious website or app activity that causes DSP to block ads by default: *[!UICONTROL None]* (the default, which doesn&#39;t block ads based on suspicious activity), *[!UICONTROL Suspicious Activity - High Risk]*, or *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 追加料金が適用される場合があります。

#### [!UICONTROL Pre-Bid Viewability]

Optional pre-bid viewability filters by [!DNL DoubleVerify] and [!DNL Integral Ad Science] to apply to placements. The advertiser-level defaults are selected for new placements. 広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md)で上書きできます。

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### ビデオ

** **[!UICONTROL Include URL's whose average video viewability rate is]**. With this option, select the criteria.

** **[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

** **[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. With this option, select the criteria.

** **[!UICONTROL Include URL's whose average player size composition is]**. With this option, select the criteria.

** **[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### 表示

** **[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. With this option, select the criteria.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. With this option, select the criteria.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

An optional **[!UICONTROL Video Viewability Targets]** filter and an optional **[!UICONTROL Display Viewability Targets]** filter. 追加料金が適用される場合があります。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** デフォルトでは、各パブリッシャーの[!DNL Authorized Digital Sellers] リストを活用して使用する[[!DNL Ads.txt] 入札前フィルタリング ](https://iabtechlab.com/ads-txt-about/)のレベル：
* *[!UICONTROL Opt out of ads.txt (default)]*：すべての販売者から在庫を購入します。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: ドメインの承認済みの直接販売者と再販者から購入在庫を優先します。
* *[!UICONTROL Ads.txt sellers only]*: ドメインの承認済みの直接販売者と再販者からのみ在庫を購入する場合。
* *[!UICONTROL Ads.txt sellers only]*: ドメインの承認済みの直接販売者からのみ在庫を購入する場合。

広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md)で上書きできます。

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:**&#x200B;初期設定では、リアルタイム入札後フィルターを有効にして、広告主がターゲットにしているサイトで広告が配信されるようにします。<!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** （[!DNL DoubleVerify]人のお客様のみ。オプション）組織の[!DNL DoubleVerify] アカウントに関連付けられた[!DNL DoubleVerify Authentic Brand Safety] セグメント IDは、すべてのプレースメントにデフォルトで使用されます。 IDを指定すると、指定したセグメント ID用に設定されたカスタムブランド安全ルールを使用して、入札後のインプレッションがブロックされます。 DSPは、セグメント IDの使用状況についてアカウントに請求します。

IDは「51」で始まり、8桁で構成されている必要があります。 広告主レベルのIDは、プレースメントレベルで変更または削除できます。

>[!MORELIKETHIS]
>
>* [広告主アカウントを作成](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the advertiser list for the account](/help/dsp/admin/advertiser-view.md) -->
