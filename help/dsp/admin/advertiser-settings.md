---
title: 広告主アカウント設定
description: 使用可能な広告主設定の説明を参照してください。
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 広告主アカウント設定

*読み取り専用ユーザーは利用できません*

## [!UICONTROL General] 設定

**[!UICONTROL Advertiser Name]:** 広告主の名前。

**[!UICONTROL Category]:** 広告主のビジネスが運営されるカテゴリ。 在庫で入札すると、カテゴリは発行者に伝えられます。 広告に合うカテゴリを選択してください。選択しないと、パブリッシャーが広告を拒否する可能性があります。

>[!NOTE]
>
>次を選択した場合、 *[!UICONTROL Other]*&#x200B;そうしないと、広告主はDSPにアクセスできません [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** 広告主のホームページまたはメイン Web サイトの URL( `http://` または `https://`) をクリックします。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （新しい広告主アカウントのみ）組織のDSPアカウントに設定されているすべてのプライベートの Exchange フィードを広告主が使用できるようにします。

### [!UICONTROL Adobe IMS IDs]

追加のAdobe Experience Cloud製品を持つ広告主は、組織の一意の ID を使用して、一部の製品間でデータをExperience Cloudできます。 特定の製品統合は、 [!UICONTROL Integrations] 」セクションに入力します。

**[!UICONTROL Account IMS org and ID]:** ( 複数のExperience Cloud主との広告アカウントを通じてライセンスを受けたExperience Cloud製品を持つ広告主。（オプション）広告主のExperience Cloud組織 ID。

**[!UICONTROL Advertiser IMS org and ID]:** ( 追加のExperience Cloud製品の直接ライセンスを有する広告主（オプション）広告主のExperience Cloud組織 ID。

### [!UICONTROL Integrations]

（オプション） DSPアカウントにリンクされた追加のExperience Cloud製品。 製品は、 [!UICONTROL Adobe IMS IDs] 」セクションに入力します。

**[!UICONTROL Attribution services]> [!UICONTROL Adobe Media Optimizer]:** ( [!DNL Adobe Advertising Search] または (Adobe広告コンバージョンピクセルを使用する ) A [!DNL Search] DSPがアトリビューションデータを交換するアカウント。

**[!UICONTROL Report suites]> [!UICONTROL Adobe Analytics]:** (Adobe Analyticsの広告主オプション；は、 [!DNL EF Redirect] およびトークンのみ ) 1 つ以上 [!DNL Analytics] パブリッシャーおよびサプライサイドのパートナーからDSPが収集したデータを送信するレポートスイート。 また、Analytics は、クライアントのサイトから収集したデータをDSPに送信します。

データをレポートスイートに表示する場合は、 [!DNL Search] 広告主レベルの設定を[!UICONTROL Enable tracking for SAINT feeds]」を有効にする必要があります。 また、 [!DNL Analytics] アカウント広告からデータを受け取るようにアカウントをAdobeする必要があります。

>[!WARNING]
>
>以前にリンクしたレポートスイートを削除すると、DSPはそのスイートとのデータ交換を停止します。 データの変動を期待する。

との統合について詳しくは、 [!DNL Analytics]を参照してください。[の概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]> [!UICONTROL Adobe Analytics Cloud]:** (Adobe Audience Manager又はAdobe Analyticsの広告主（オプション）Audience Managerまたは [!DNL Analytics] DSPがすべての広告主のAdobeオーディエンスのセグメントメタデータ、階層データおよび一意のオーディエンスデータを取り込むアカウント。 これには、以下のデータが含まれます。

* Audience Managerセグメント
* [!DNL Analytics] Adobe Experience Cloudに公開されたセグメント
* Adobe Experience Cloudで [!DNL People core service]
* Adobe Experience Platformで作成され、Audience Managerを介してAdobe広告に送信されるセグメント

初期同期には約 24 時間かかります。 その後、データはリアルタイムで同期され、1～2 秒の遅延が発生します。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 設定

オプションで、広告主の新しい配置のデフォルトターゲットを設定できます。 ユーザーは、新しいプレースメントのデフォルトターゲットを上書きできます。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 各プレースメントのジオターゲティングのデフォルトの国です。 ユーザーは、各プレースメントに対して国を変更したり、より具体的な地域ターゲティングを設定したりできます。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** デフォルトで抑制するオーディエンスまたはセグメント。 ユーザーは、各配置の除外を変更できます。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

のタイプ [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39] 適用するコンテキストフィルター。 広告主レベルの設定は、 [配置レベル](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上のタイプの在庫コンテキスト。 追加料金が適用される場合があります。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （オプション）デフォルトでターゲットにする 1 つ以上の在庫属性のタイプ。 追加料金が適用される場合があります。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上の在庫属性のタイプ。 追加料金が適用される場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** （オプション）デフォルトで広告をブロックする成人向けコンテンツの程度： *[!UICONTROL Do Not Block]* （デフォルト） *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

**[!UICONTROL Alcohol Content]:** （オプション）デフォルトで広告をブロックするアルコールコンテンツの程度： *[!UICONTROL Do Not Block]* （デフォルト） *[!UICONTROL Standard]*&#x200B;または *[!UICONTROL Strict]*. 追加料金が適用される場合があります。

#### [!UICONTROL Pre-Bid Fraud Blocking]

不正なトラフィックや、を通じて測定された疑わしいアクティビティに基づいてブロックするサイトのタイプ [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39]. 広告主レベルの設定は、 [配置レベル](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しい配置に対する、ハイジャックされたデバイス上のトラフィックを含む、100%すべての無効なトラフィックをブロックします。 追加料金が適用される場合があります。

**[!UICONTROL Also block sites with]:** （オプション）デフォルトでDSPが広告をブロックする原因となる、追加レベルの詐欺および無効なトラフィック：  *[!UICONTROL None]* （デフォルトでは、追加のトラフィックはブロックされません）。 *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;または *[!UICONTROL >25% Average Fraud/IVT levels]*. 追加料金が適用される場合があります。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでDSPが広告をブロックする 1 つ以上のタイプの詐欺。 *[!UICONTROL Fraud]* （詐欺行為を伴うすべてのサイトをブロックします）。 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、または *[!UICONTROL Fraud: Zero Ads]*. 追加料金が適用される場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでDSPが広告をブロックする原因となる疑わしい Web サイトまたはアプリアクティビティのタイプ。 *[!UICONTROL None]* （疑わしいアクティビティに基づいて広告をブロックしないデフォルト） *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;または *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 追加料金が適用される場合があります。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** デフォルトでは、 [[!DNL Ads.txt] 入札前フィルター](https://iabtechlab.com/ads-txt-about/) 各パブリッシャーの [!DNL Authorized Digital Sellers] リスト：
* *[!UICONTROL Opt out of ads.txt (default)]*:すべての販売者から在庫を購入する。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:ドメインの許可されたダイレクト販売者および再販売者からの在庫の購入を優先する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可された直接販売者および再販売者からのみ在庫を購入する。
* *[!UICONTROL Ads.txt sellers only]*:ドメインの許可されたダイレクトセラーからのみ在庫を購入する場合。

広告主レベルの設定は、 [配置レベル](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** デフォルトでは、は、入札後のリアルタイムフィルターを有効にして、広告主がターゲットとするサイトで広告が機能するようにします。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] 顧客のみ（オプション）組織の [!DNL DoubleVerify] アカウント

**[!UICONTROL Enable Authentic Brand Safety]:** （オプション）デフォルトでは、を有効にします。 [!DNL DoubleVerify] Authentic Brand Safety：指定したセグメント ID に対して設定されたカスタム Brand Safety ルールを使用して、入札後のインプレッションをブロックします。 DSPは、セグメント ID の使用を目的としてアカウントを請求します。

配置レベルで広告主レベルの設定を上書きできます。

>[!MORELIKETHIS]
>
>* [広告主アカウントの作成](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
