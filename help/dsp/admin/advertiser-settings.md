---
title: 広告主アカウント設定
description: 使用可能な広告主設定の説明を参照してください。
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# 広告主アカウント設定

*読み取り専用ユーザーは使用できません*

<!-- Not published -->

## [!UICONTROL General] Settings

**[!UICONTROL Advertiser Name]:** 広告主名。

**[!UICONTROL Category]:** 広告主のビジネスが運営されるカテゴリ。 在庫に対して入札すると、カテゴリが公開者に通知されます。 広告に合ったカテゴリを選択するようにしてください。選択しない場合、パブリッシャーが広告を拒否する可能性があります。

>[!NOTE]
>
>*[!UICONTROL Other]* を選択した場合、広告主はDSP [!DNL On Demand Inventory] にアクセスできません。

**[!UICONTROL Advertiser URL]:** 広告主のホームページまたはメインの web サイトの URL （`http://` または `https://` で始まる）。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （新しい広告主アカウントのみ）組織のDSP アカウント用に設定されたすべてのプライベート交換フィードを広告主が使用できるようにします。

### [!UICONTROL Adobe IMS IDs]

Experience Cloud商品をさらに持つ広告主は、Adobe Experience Cloud用の組織の一意の ID を使用して、一部の商品間でデータを共有できます。 [!UICONTROL Integrations] の節で、特定の製品の統合を設定できます。

**[!UICONTROL Account IMS org and ID]:** （複数の広告主とのExperience Cloud アカウントを通じてライセンスされた、追加のExperience Cloud製品を持つ広告主。オプション）広告主のExperience Cloud組織 ID。

**[!UICONTROL Advertiser IMS org and ID]:** （追加のExperience Cloud商品のダイレクトライセンスを持つ広告主。オプション）広告主のExperience Cloud組織 ID。

### [!UICONTROL Integrations]

（任意）DSP アカウントにリンクされている追加のExperience Cloud製品。 商品は、[!UICONTROL Adobe IMS IDs] の節で指定したのと同じExperience Cloud組織 ID に関連付ける必要があります。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** （[!DNL Advertising Search, Social, & Commerce] を使用する、またはAdobe Advertising コンバージョンピクセルを使用する広告主）DSPがアトリビューションデータを交換する [!DNL Search, Social, & Commerce] アカウント。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** （Adobe Analyticsを使用する広告主。オプション。[!DNL EF Redirect] とトークンのみを含むAdobe Advertising コンバージョントラッキングタグを使用して収集されたデータにのみ適用） DSPがパブリッシャーおよびサプライサイドパートナーから収集したデータを送信する 1 つ以上の [!DNL Analytics] レポートスイート。 また、Analytics は、収集したデータをクライアントのサイトからDSPに送信します。

データをレポートスイートに表示するには、適切な [!DNL Search, Social, & Commerce] 広告主レベルの設定を有効にする必要があります。 さらに、Adobe Advertisingからデータを受信するように広告主の [!DNL Analytics] アカウントを設定する必要があります。

>[!WARNING]
>
>以前にリンクされたレポートスイートを削除すると、DSPはそのスイートとデータを交換しなくなります。 データの変動が発生することが予想されます。

[!DNL Analytics] との統合について詳しくは、「[ の概要  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を参照してください。

**[!UICONTROL Audiences]**/**[!UICONTROL Adobe Analytics Cloud]:** （Adobe Audience ManagerまたはAdobe Analyticsを使用する広告主。オプション）DSPがすべての広告主のAdobe オーディエンスのセグメントメタデータ、階層データおよび一意のオーディエンスデータを取り込むAudience Managerまたは [!DNL Analytics] アカウント。 これには、次のデータが含まれます。

* Audience Manager セグメント
* Adobe Experience Cloudに公開される [!DNL Analytics] セグメント
* Adobe Experience Cloud [!DNL Audience Library] を使用して作成されたセグメント
* Adobe Experience Platformで作成され、Audience Managerを介してAdobe Advertisingに送信されるセグメント

最初の同期には約 24 時間かかります。 その後、データは 1 秒から 2 秒の遅延でリアルタイムに同期されます。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Settings

オプションで、広告主の新しいプレースメントのデフォルトターゲットを設定できます。 ユーザーは、新しいプレースメントのデフォルトターゲットを上書きできます。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 各プレースメントのジオターゲティングのデフォルトの国。 ユーザーは、国を変更し、プレースメントごとに、より具体的なジオターゲティングを設定できます。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** デフォルトで抑制するオーディエンスまたはセグメント。 ユーザーは、各プレースメントの除外を変更できます。

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

適用する [!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science] および [!DNL Peer39] のコンテキストフィルターのタイプ。 広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md) で上書きできます。

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上のタイプのインベントリコンテキスト。 追加料金がかかる場合があります。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （オプション）デフォルトでターゲットにする 1 つ以上のタイプの在庫属性。 追加料金がかかる場合があります。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （任意）デフォルトでブロックする 1 つ以上のタイプの在庫属性。 追加料金がかかる場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** （任意）デフォルトで広告をブロックする成人向けコンテンツの程度です。*[!UICONTROL Do Not Block]* （デフォルト）、*[!UICONTROL Standard]*、*[!UICONTROL Strict]* のいずれかです。 追加料金がかかる場合があります。

**[!UICONTROL Alcohol Content]:** （任意）デフォルトで広告をブロックするアルコール度数。*[!UICONTROL Do Not Block]* （デフォルト）、*[!UICONTROL Standard]*、*[!UICONTROL Strict]* のいずれかです。 追加料金がかかる場合があります。

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39] を通じて測定された不正なトラフィックや疑わしいアクティビティに基づいてブロックされるサイトのタイプ。 広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md) で上書きできます。

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しいプレースメントに対して、ハイジャックされたデバイス上のトラフィックを含むすべての 100% 無効なトラフィックをブロックします。 追加料金がかかる場合があります。

**[!UICONTROL Also block sites with]:** （任意）DSPがデフォルトで広告をブロックする原因となる、追加の不正トラフィックおよび無効なトラフィックのレベル。*[!UICONTROL None]* （デフォルト。追加のトラフィックをブロックしません）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]* または *[!UICONTROL >25% Average Fraud/IVT levels]* です。 追加料金がかかる場合があります。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** （任意）DSPがデフォルトで広告をブロックする原因となる 1 つ以上の不正。*[!UICONTROL Fraud]* （不正を行うすべてのサイトをブロックする）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、*[!UICONTROL Fraud: Zero Ads]* のいずれかです。 追加料金がかかる場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** （任意）DSPがデフォルトで広告をブロックする原因となる、疑わしい web サイトまたはアプリアクティビティの一種。*[!UICONTROL None]* （デフォルト。疑わしいアクティビティに基づく広告をブロックしません）、*[!UICONTROL Suspicious Activity - High Risk]*、*[!UICONTROL Suspicious Activity - High or Moderate Risk]* のいずれかです。 追加料金がかかる場合があります。

#### [!UICONTROL Pre-Bid Viewability]

オプションの pre-bid viewability では、プレースメントに適用する [!DNL DoubleVerify] と [!DNL Integral Ad Science] でフィルターします。 新しいプレースメントには、広告主レベルのデフォルトが選択されます。 広告主レベルの設定は、[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md) で上書きできます。

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### ビデオ

** **[!UICONTROL Include URL's whose average video viewability rate is]**。 このオプションを使用して、条件を選択します。

** **[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

** **[!UICONTROL Include URL's whose average completion & fully viewable rate is]**。 このオプションを使用して、条件を選択します。

** **[!UICONTROL Include URL's whose average player size composition is]**。 このオプションを使用して、条件を選択します。

** **[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### 表示

** **[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**。 このオプションを使用して、条件を選択します。

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**。 このオプションを使用して、条件を選択します。

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

オプションの **[!UICONTROL Video Viewability Targets]** フィルターとオプションの **[!UICONTROL Display Viewability Targets]** フィルター。 追加料金がかかる場合があります。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** デフォルト。各パブリッシャーの [!DNL Authorized Digital Sellers] リストを活用して、どのレベルの [[!DNL Ads.txt] pre-bid フィルタリング ](https://iabtechlab.com/ads-txt-about/) を使用するか：
* *[!UICONTROL Opt out of ads.txt (default)]*：すべてのセラーから在庫を購入する場合。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：ドメインの承認済み直販業者および再販業者からの購買在庫を優先順位付けする手順です。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済み直販業者および再販業者からのみ在庫を購入する場合。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済ダイレクト・セラーからのみ在庫を購入する場合。

[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md) で広告主レベルの設定を上書きできます。

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** デフォルトでは、はリアルタイムの入札後フィルターを有効にして、広告主がターゲティングしているサイトに広告が配信されるようにします。<!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** （[!DNL DoubleVerify] 顧客のみ。オプション）すべてのプレースメントに対してデフォルトで使用する、組織の [!DNL DoubleVerify] アカウントに関連付けられた [!DNL DoubleVerify Authentic Brand Safety] 定のセグメント ID。 ID を指定すると、指定したセグメント ID に設定されたカスタムブランドセーフティルールを使用して、入札後のインプレッションがブロックされます。 DSPは、セグメント ID の使用に対してアカウントに請求します。

ID は「51」で始まり、8 桁で構成する必要があります。 広告主レベルの ID は、プレースメントレベルで変更または削除できます。

>[!MORELIKETHIS]
>
>* [ 広告主アカウントの作成 ](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
