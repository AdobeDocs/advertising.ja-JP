---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
TQID: https://experienceleague.adobe.com/tLMBR-i1XpRHeFkfrhh2CtCQI4K0rPgCHqkZv8dk4cA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1437
ht-degree: 0%

---

# キャンペーン設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** キャンペーン名。

**[!UICONTROL Advertiser]:** （既存のキャンペーンの読み取り専用）該当する広告主（ブランド）。 既存の広告主を選択するか、新しい広告主を作成します。

**[!UICONTROL Advertiser URL]:**&#x200B;広告主の公式ページ。 このフィールドは、在庫パートナーとの広告承認プロセスを高速化します。

**[!UICONTROL Timezone]:** （既存のキャンペーンの読み取り専用） レポートと入札のタイムゾーン。

**[!UICONTROL Customer PO]:** （オプション）挿入オーダー/発注の顧客発注。

**[キャンペーンの開始日]:** キャンペーンの開始日と終了日。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** （マージンを使用する代理店がサービスを提供するセルフサービス アカウント）証拠金管理のオプション：

* **[!UICONTROL Would you like to manage margins for this campaign?]:** キャンペーンの余白を管理するかどうか：*[!UICONTROL Yes]*&#x200B;または&#x200B;*[!UICONTROL No]* （既定値）。 *[!UICONTROL Yes]を選択すると、*&#x200B;は追加の設定を指定します。 マージン管理を有効にしてキャンペーンを保存すると、マージン管理を無効にすることはできません。

* **[!UICONTROL How would you like to compute agency fees?]:** （利益管理を含むキャンペーンのみ）代理店手数料の計算方法。これは、キャンペーンの総予算のうち、源泉徴収され、純支出に含まれていない部分です。

   * *[!UICONTROL Margin % of Total Budget]:* （デフォルト）総支出に対する割合で手数料を計算します。 [!UICONTROL Agency Fee Type] （固定または複合）と[!UICONTROL Margin %]または[!UICONTROL Composite Margin %]を指定します。

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* メディアコスト、データおよびその他のコスト、および/または[!DNL Adobe]技術費の指定された割合で料金を計算します。 [!UICONTROL Markup %]を指定し、マークアップを適用するコンポーネントを選択します。

* **[!UICONTROL Agency Fee Type]:** （[!UICONTROL Margin % of Total Budget]を使用するキャンペーン）代理店手数料の種類。

   * *[!UICONTROL Fixed]:* （デフォルト）DSPでは、代理店手数料として総支出の一定の割合を源泉徴収できます。 [!UICONTROL Margin %]を指定します。

   * *[!UICONTROL Composite]:*&#x200B;は、代理店手数料と[!DNL Adobe]の技術費の両方を考慮して、DSPが総支出の割合を差し控えることを許可します。 [!UICONTROL Composite Margin %]を指定します。

* **[!UICONTROL Margin %]:** （マージンが固定された[!UICONTROL Margin % of Total Budget]を使用するキャンペーン）代理店手数料として源泉徴収する総支出の割合。 利益率の変更は、キャンペーンの過去の総支出ではなく、将来の総支出にのみ適用されます。 [!UICONTROL Estimated Tax Withholding]の値は、マージンが適用される前の総支出から除外されます。 次の例では、施策の費用が不足したり、過剰になったりしていないことを前提としています。

   * 例1: [!UICONTROL Gross Budget]が`100 USD`で、[!UICONTROL Margin %]がフライト中に`5%`であるとします。 キャンペーンのフライトが終了すると、代理店手数料は`5 USD` （`5% of 100 USD`）として計算され、純支出は`95 USD` （`campaign budget [100 USD] - agency fees [5 USD]`）となります。

   * マージンに変更を加えた例2：同じキャンペーンで、総支出が[!UICONTROL Margin %]だったときに`5%`が`10%`から`40 USD`に変更されたとします。 変更前の期間では、代理店手数料は`2 USD` （つまり`5% of 40 USD`）として計算され、変更後の期間では、代理店手数料は`6 USD` （つまり`10% of 60 USD`）として計算されます。 代理店手数料の合計は`8 USD` （つまり`2 USD + 6 USD`）と計算され、純支出は`92 USD` （つまり`campaign budget [100 USD] - total agency fees [8 USD]`）です。

   * 源泉徴収付きの例3: [!UICONTROL Gross Budget]が`100 USD`、キャンペーンフライトの終了時の[!UICONTROL Estimated Tax Withholding]が`10 USD`、フライト全体の[!UICONTROL Margin %]が`5%`であるとします。 キャンペーンのフライトが終了すると、代理店手数料は`4.5 USD` （`5% of (campaign budget [100 USD] - tax withholding [USD 10])`）として計算され、純支出は`85.5 USD` （`campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`）となります。

* **[!UICONTROL Composite Margin %]:** （複合利益率で[!UICONTROL Margin % of Total Budget]を使用するキャンペーン） [!DNL Adobe]件の技術費と代理店手数料を組み合わせて源泉徴収する、粗支出の割合。 代理店手数料は、複合利益率からAdobeの技術手数料を差し引いて計算されます。 複合利益率の値に対する変更は、キャンペーンの過去の総支出ではなく、将来の総支出にのみ適用されます。 複合利益率が適用される前に、[!UICONTROL Estimated Tax Withholding]値が総支出から除外されます。

  例えば、[!UICONTROL Gross Budget]が`100 USD`、キャンペーンのフライト終了時の[!DNL Adobe]の技術料金が`10 USD`、フライト全体の[!UICONTROL Composite Margin %]が`17%`であるとします。 キャンペーンのフライトの終了時（キャンペーンが過小支出または過剰支出になっていない場合）、代理店手数料は`7 USD` （つまり`(17% of 100 USD) - 10`）と計算され、純支出は`93 USD` （つまり`campaign budget [100 USD] - agency fees [7 USD]`）となります。

* **[!UICONTROL Markup %]:** （[!UICONTROL Apply Markup % on top of individual cost components]を使用するキャンペーン）指定されたコストコンポーネントに適用して代理店手数料を計算する割合。 マークアップ値の変更は、キャンペーンの過去のコストではなく、将来のコストにのみ適用されます。

* **[!UICONTROL Select cost components on which markup will be applied]:** （[!UICONTROL Apply Markup % on top of individual cost components]を使用するキャンペーン） [!UICONTROL Markup %]が適用されるコストコンポーネント。 該当するすべてのコンポーネントを選択：*[!UICONTROL Media cost]*、*[!UICONTROL Data and Other costs]*&#x200B;または&#x200B;*[!UICONTROL Adobe tech fees]*。 コンポーネントの選択に対する変更は、キャンペーンの過去のコストではなく、将来のコストにのみ適用されます。

  例えば、[!UICONTROL Markup %]は「`10%`」と「[!UICONTROL Media cost]」の[!UICONTROL Data and Other costs]です。 キャンペーンのフライトのどの時点でも、メディアコストが`20 USD`、データおよびその他のコストが`5 USD`、[!DNL Adobe]技術費が`2 USD`である場合、代理店手数料は`2.50 USD`と計算されます（これは`10% of (20 USD + 5 USD)`、総支出は`29.50 USD` （これは`media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`）。

**[!UICONTROL Gross Budget]:** （マージン管理のあるキャンペーンのみ）指定されたマージン調整が適用される前の総キャンペーン予算。

**[!UICONTROL Budget]:** （マージン管理のないキャンペーン） キャンペーン全体の予算。

**[!UICONTROL Estimated Tax Withholding]:**&#x200B;国または地方税のアカウントレベルで、広告費、広告料、および/またはデータ料金の合計支出の割合を源泉徴収します。 料金は予算編成およびペーシング目的の見積もりであるため、請求済み税率は異なる場合があります。

源泉徴収する税金を見積もるには：

1. **[!UICONTROL Update rates here]**&#x200B;をクリックします。

1. **[!UICONTROL Estimated tax rate]**&#x200B;をパーセンテージで指定します。

1. 源泉徴収対象の各料金タイプの横にあるチェックボックスをオンにします。 料金の種類は次のとおりです。

   * *[!UICONTROL Include estimated tax - ads fee]:* キャンペーン管理手数料の税金を含むすべてのAdvertising DSP メディア費用に適用されます。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* メディアとデータを除くすべてのAdvertising DSPの費用に適用されます。 キャンペーン管理手数料の税金は含まれていません

   * *[!UICONTROL Include estimated tax - data fee]:* Advertising DSPのすべてのデータ支出に適用されます。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

>[!NOTE]
>
>* 米国では、州によって広告、広告配信、データに対する税金負担が異なる場合があります。 その他の国の企業の場合は、VATを考慮して税金の3つのカテゴリーをすべて含めてください。
>
>* これらの値は、アカウントの料金設定で設定することもできます。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** （2020年6月22日以降に作成された既存のキャンペーンでは読み取り専用、2020年6月22日以前に作成されたキャンペーンでは利用できません） DSPが広告をターゲットにして頻度キャップを適用するレベル：*Same Device* to target a device or *People* to target a person across all of their known devices. **注：** ユニバーサル IDをターゲットとするプレースメントでは、クロスデバイスのサポートを利用できません。

**[!UICONTROL Device Graph]:** （既存のキャンペーンの読み取り専用、人物ベースのクロスデバイスターゲティングを使用するキャンペーンのみ） クロスデバイスターゲティングと頻度の管理に使用するデバイスグラフ：

* *[!UICONTROL LiveRamp - U.S. only]:* [!DNL LiveRamp] デバイスグラフを使用して配信されるインプレッションについては、すべての広告主が$0.35 CPMのクロスデバイスターゲティングで利用できます（ターゲットオーディエンスセグメント内に見つからないデバイスの場合）。 クロスデバイスのターゲティングは、プレースメントレベルで設定できます。

  このオプションは、頻度の管理とアトリビューションの測定のために、すべての広告主が無料で利用できます。

  クロスデバイスのサポートは、従来のIDをターゲットとするプレースメントにのみ適用されますが、ユニバーサル ID （[!DNL LiveRamps]を含む）をターゲットとするプレースメントには適用されません。 ユニバーサル IDのターゲティング、周波数管理、アトリビューションは、ID レベルでのみ適用されます。

**[!UICONTROL Frequency Cap]:** （オプション）一意のデバイス、ユニバーサル ID、またはユーザー（指定された[!UICONTROL Cross Device Level]とプレースメントの[!UICONTROL Targeting]設定に応じて）がキャンペーンから広告を配信できる回数。 オプションには、1日、週、または月あたりの特定の金額&#x200B;*[!UICONTROL Unlimited]*&#x200B;が含まれます。

>[!NOTE]
>
> 広告の表示頻度の上限は、キャンペーン、パッケージ、プレースメントレベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップを尊重しています。

**[!UICONTROL Packages]:** キャンペーンに含める[&#x200B; パッケージ &#x200B;](/help/dsp/campaign-management/packages/package-about.md)。 既存のパッケージを選択するか、含めるパッケージを作成します。 パッケージを作成する場合は、詳細については、[&#x200B; パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)に関する説明を参照してください。

## [!UICONTROL Campaign measurement]

>[!NOTE]
>
>次の設定では、測定とレポート機能のみを有効にします。 パフォーマンス最適化は、パッケージおよびプレースメントレベルでのみ実行されます。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, fraud, & brand safety]

**[!UICONTROL IAS]:** （オプション）指定した設定を使用して、ビューアビリティ、不正行為、ブランドの安全性、オーディエンスの検証の[!DNL IAS]測定とレポートを有効にします。 追加料金が適用されます。

* **[!UICONTROL Measure On]:**&#x200B;測定するインベントリ：*[!UICONTROL Display and VPAID video inventory]* （デフォルト）または&#x200B;*[!UICONTROL Display, VPAID & VAST video inventory]*。

  >[!NOTE]
  >
  >動画の視聴可能性は、VPAID インベントリでのみ測定可能です。

* **[!UICONTROL IAS Account ID (AnID)]:** （独自の[!DNL IAS] アカウントを持つ広告主。オプション）組織の[!DNL IAS] アカウント ID。これは[!DNL IAS]が直接使用料金を請求します。

* **[!UICONTROL IAS Team ID]:** （独自の[!DNL IAS] アカウントを持つ広告主。オプション）組織の[!DNL IAS] アカウントのチーム ID。このアカウントは[!DNL IAS]から直接使用料金が請求されます。<!-- verify -->

#### オーディエンスの検証

**[!UICONTROL Comscore Campaign Ratings]:** （オプション）指定した設定を使用して、オーディエンス検証の検証済み[!DNL Comscore]測定とレポート [!DNL Campaign Ratings]を有効にします。 追加料金が適用されます。

* **[!UICONTROL Target Gender]:** ターゲットにする性別：*[!UICONTROL Both]* （既定値）、*[!UICONTROL Male]*、または&#x200B;*[!UICONTROL Female]*

* **[!UICONTROL Target Age]:**&#x200B;対象となる年齢範囲。 左右のスライダーを使用して、必要に応じて範囲を縮小します。

* **[!UICONTROL Target Country]:** （オプション）対象の国。 [!DNL Comscore]は、サポートされている国でのみ提供されるインプレッションを測定します。

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** プレースメントレベル [!UICONTROL Attention Score]指標（インプレッション間の重み付け平均数[!DNL Adelaide] &quot;[!DNL Attention Units]&quot;など）のトラッキングを有効にします。 指標は、[!DNL Roku]接続されたテレビ、VPAID専用のプレロール、ポッドキャストではないオーディオを除くすべてのプレースメントタイプで使用できます。 DSPは、関連するすべてのクリエイターにJavaScript タグを自動的に添付し、[!DNL Adelaide]は露出データをトラッキングして、毎日DSPに送信します。 日付を使用すると、より高い注意スコアを使用して、配置戦術に向けて支出を手動で最適化できます。

[!UICONTROL Attention Score] フィールドは、レポートの[!UICONTROL Metrics] セクション、[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements] ビュー、および[!UICONTROL Sites]配置の詳細ビュー[!UICONTROL Ads]の[!UICONTROL Inventory]、[、および](/help/dsp/campaign-management/reports/placement-details-view.md) タブで使用できます。

[!DNL Adelaide] セグメントを測定に使用すると、[!DNL Adelaide]個の測定タグを持つ広告から配信されたインプレッションごとにCPM料金が発生します。 この料金は、[&#x200B; プレースメントレベルの注意ターゲティング &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)の料金とは別です。

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:**&#x200B;指定された機密レベルに基づいて、[!DNL IAB Open Video Viewability (OpenVV)] テクノロジーを使用してファーストパーティの測定とビューアビリティのレポートを有効にします。

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Advertising DSPでのキャンペーン管理について](campaign-about.md)
>* [&#x200B; キャンペーンを作成](campaign-create.md)
>* [&#x200B; キャンペーンを編集](campaign-edit.md)
>* [&#x200B; キャンペーンの変更ログを表示](campaign-change-log.md)
