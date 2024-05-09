---
title: 広告主アカウント設定
description: 使用可能な広告主設定の説明を参照してください。
role: User, Admin
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# 広告主アカウント設定

*読み取り専用ユーザーは使用できません*

## [!UICONTROL General] 設定

**[!UICONTROL Advertiser Name]:** 広告主名。

**[!UICONTROL Category]:** 広告主のビジネスが運営されるカテゴリ。 在庫に対して入札すると、カテゴリが公開者に通知されます。 広告に合ったカテゴリを選択するようにしてください。選択しない場合、パブリッシャーが広告を拒否する可能性があります。

>[!NOTE]
>
>を選択する場合 *[!UICONTROL Other]*&#x200B;その場合、広告主はDSPにアクセスできません [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** 広告主のホームページまたはメインの web サイトの URL （で始まる） `http://` または `https://`）に設定します。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （新しい広告主アカウントのみ）組織のDSP アカウント用に設定されたすべてのプライベート交換フィードを広告主が使用できるようにします。

### [!UICONTROL Adobe IMS IDs]

Adobe Experience Cloud商品を追加してExperience Cloudする広告主は、広告用に組織の一意の ID を使用して、一部の商品間でデータを共有できます。 特定の製品統合は、 [!UICONTROL Integrations] セクション。

**[!UICONTROL Account IMS org and ID]:** （複数の広告主とのExperience Cloudアカウントを通じてライセンスを取得した追加のExperience Cloud商品を持つ広告主。オプション）広告主のExperience Cloud団体 ID。

**[!UICONTROL Advertiser IMS org and ID]:** （Experience Cloud商品のダイレクトライセンスを持つ広告主。任意）広告主のExperience Cloud組織 ID。

### [!UICONTROL Integrations]

（任意）DSP アカウントにリンクされている追加のExperience Cloud製品。 商品は、で指定したのと同じExperience Cloud組織 ID に関連付ける必要があります [!UICONTROL Adobe IMS IDs] セクション。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** （広告主 [!DNL Advertising Search, Social, & Commerce] またはAdobe Advertisingコンバージョンピクセルを使用するユーザー） A [!DNL Search, Social, & Commerce] DSPがアトリビューションデータを交換するアカウント。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** （Adobe Analyticsを使用する広告主。オプション。Adobe Advertisingコンバージョントラッキングタグを使用して収集された、 [!DNL EF Redirect] およびトークンのみ） 1 つ以上 [!DNL Analytics] DSPがパブリッシャーおよびサプライサイドパートナーから収集するデータの送信先となるレポートスイート。 また、Analytics は、収集したデータをクライアントのサイトからDSPに送信します。

レポートスイートに表示されるデータに適したもの [!DNL Search, Social, & Commerce] 広告主レベルの設定を有効にする必要があります。 また、広告主のです [!DNL Analytics] Adobe Advertisingからデータを受け取るようにアカウントを設定する必要があります。

>[!WARNING]
>
>以前にリンクされたレポートスイートを削除すると、DSPはそのスイートとデータを交換しなくなります。 データの変動が発生することが予想されます。

との統合に関する詳細情報 [!DNL Analytics]を参照してください。[概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).」と入力します。

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** （Adobe Audience ManagerまたはAdobe Analyticsを使用する広告主。オプション）Audience Manager [!DNL Analytics] DSPがセグメントメタデータ、Adobeデータ、すべての広告主の階層オーディエンスの一意のオーディエンスデータを取り込むアカウント。 これには、次のデータが含まれます。

* Audience Managerセグメント
* [!DNL Analytics] Adobe Experience Cloudに公開されるセグメント
* Adobe Experience Cloudで作成されたセグメント [!DNL Audience Library]
* Adobe Experience Platformで作成され、Audience Managerを介してAdobe Advertisingに送信されるセグメント

最初の同期には約 24 時間かかります。 その後、データは 1 秒から 2 秒の遅延でリアルタイムに同期されます。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 設定

オプションで、広告主の新しいプレースメントのデフォルトターゲットを設定できます。 ユーザーは、新しいプレースメントのデフォルトターゲットを上書きできます。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 各プレースメントのジオターゲティングのデフォルトの国。 ユーザーは、国を変更し、プレースメントごとに、より具体的なジオターゲティングを設定できます。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** デフォルトで抑制するオーディエンスまたはセグメント。 ユーザーは、各プレースメントの除外を変更できます。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

のタイプ [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39] 適用するコンテキストフィルター。 で広告主レベルの設定を上書きできます [プレースメントレベル](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上のタイプのインベントリコンテキスト。 追加料金がかかる場合があります。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （オプション）デフォルトでターゲットにする 1 つ以上のタイプの在庫属性。 追加料金がかかる場合があります。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （任意）デフォルトでブロックする 1 つ以上のタイプの在庫属性。 追加料金がかかる場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** （任意）デフォルトで広告をブロックするアダルトコンテンツの程度。 *[!UICONTROL Do Not Block]* （デフォルト）、 *[!UICONTROL Standard]*、または *[!UICONTROL Strict]*. 追加料金がかかる場合があります。

**[!UICONTROL Alcohol Content]:** （任意）デフォルトで広告をブロックするアルコール度数。 *[!UICONTROL Do Not Block]* （デフォルト）、 *[!UICONTROL Standard]*、または *[!UICONTROL Strict]*. 追加料金がかかる場合があります。

#### [!UICONTROL Pre-Bid Fraud Blocking]

で測定された不正なトラフィックや疑わしいアクティビティに基づいてブロックするサイトのタイプ [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39]. で広告主レベルの設定を上書きできます [プレースメントレベル](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しいプレースメントに対して、ハイジャックされたデバイス上のトラフィックを含む 100% 無効なトラフィックをすべてブロックします。 追加料金がかかる場合があります。

**[!UICONTROL Also block sites with]:** （任意）追加のレベルの不正と無効なトラフィックにより、DSPがデフォルトで広告をブロックする場合があります。  *[!UICONTROL None]* （デフォルト。追加のトラフィックをブロックしません）、 *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*、または *[!UICONTROL >25% Average Fraud/IVT levels]*. 追加料金がかかる場合があります。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** （任意）DSPがデフォルトで広告をブロックする原因となる 1 つ以上の種類の不正。 *[!UICONTROL Fraud]* （すべてのサイトを不正でブロックします）、 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、および/または *[!UICONTROL Fraud: Zero Ads]*. 追加料金がかかる場合があります。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** （オプション）DSPがデフォルトで広告をブロックする原因となる、疑わしい web サイトまたはアプリアクティビティの種類。 *[!UICONTROL None]* （デフォルト。疑わしいアクティビティに基づく広告をブロックしません）、 *[!UICONTROL Suspicious Activity - High Risk]*、または *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 追加料金がかかる場合があります。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** デフォルトでは、次のどのレベルか [[!DNL Ads.txt] 入札前のフィルタリング](https://iabtechlab.com/ads-txt-about/) 各パブリッシャーのを活用して使用するには [!DNL Authorized Digital Sellers] リスト :
* *[!UICONTROL Opt out of ads.txt (default)]*：すべてのセラーから在庫を購入する。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：ドメインの承認済みダイレクトセラーおよびリセラーからの購入在庫を優先順位付けする。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済みダイレクトセラーおよびリセラーからのみ在庫を購入できます。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済みダイレクトセラーからのみ在庫を購入する場合。

で広告主レベルの設定をオーバーライドできます [プレースメントレベル](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** デフォルトでは、はリアルタイムの入札後フィルターを有効にして、広告主がターゲティングしているサイトに広告が配信されるようにします。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** （[!DNL DoubleVerify] 顧客のみ。オプション）組織に関連付けられたブランドセーフティセグメント ID [!DNL DoubleVerify] アカウント。

**[!UICONTROL Enable Authentic Brand Safety]:** （オプション）デフォルトでは、 [!DNL DoubleVerify] Authentic Brand Safety：指定したセグメント ID に対して設定されたカスタムブランドセーフティルールを使用して、入札後のインプレッションをブロックします。 DSPは、セグメント ID の使用に対してアカウントに請求します。

広告主レベルの設定は、プレースメントレベルで上書きできます。

>[!MORELIKETHIS]
>
>* [広告主アカウントの作成](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
