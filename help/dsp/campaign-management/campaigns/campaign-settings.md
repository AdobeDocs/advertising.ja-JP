---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---

# キャンペーン設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** キャンペーン名。

**[!UICONTROL Advertiser]:** （既存のキャンペーンの場合は読み取り専用）該当する広告主（ブランド）。 既存の広告主を選択するか、新しい広告主を作成します。

**[!UICONTROL Advertiser URL]:** 広告主の公式ページ。 このフィールドは、在庫パートナーとの広告承認プロセスを迅速化します。

**[!UICONTROL Timezone]:** （既存のキャンペーンの場合は読み取り専用） レポートおよび入札のタイムゾーン。

**[!UICONTROL Customer PO]:** （オプション）挿入注文/発注書の顧客発注書。

**[キャンペーンの日付 ]:** キャンペーンの開始日と終了日。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** （マージンを使用してエージェンシーがサービスを提供するセルフサービス・アカウント）マージン管理のオプション：

* **[!UICONTROL Would you like to manage margins for this campaign?]:** キャンペーンの余白を管理するかどうか：*[!UICONTROL Yes]* または *[!UICONTROL No]* （デフォルト）。 *[!UICONTROL Yes]を選択する場合は* 追加設定を指定します。 証拠金管理を有効にしてキャンペーンを保存したら、証拠金管理を無効にすることはできません。

* **[!UICONTROL How would you like to compute agency fees?]:** （利益管理を使用するキャンペーンのみ）エージェンシー料金の計算方法。これは、キャンペーンの総予算のうち源泉徴収され、純支出に含まれていない部分です。

   * *[!UICONTROL Margin % of Total Budget]:* （デフォルト）総支出に対する割合として手数料を計算します。 [!UICONTROL Agency Fee Type] （固定または複合）と [!UICONTROL Margin %] または [!UICONTROL Composite Margin %] を指定します。

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* メディア費用、データ費用、その他の費用に対する指定された割合、および/または [!DNL Adobe] の技術費用として料金を計算します。 [!UICONTROL Markup %] を指定し、マークアップを適用するコンポーネントを選択します。

* **[!UICONTROL Agency Fee Type]:** （[!UICONTROL Margin % of Total Budget] を使用するキャンペーン）代理店手数料のタイプ。

   * *[!UICONTROL Fixed]:* （デフォルト）DSPが総支出の固定割合を代理店手数料として留保することを許可します。 [!UICONTROL Margin %] を指定してください

   * *[!UICONTROL Composite]:* DSPが、総支出の割合を留保して、代理店手数料と [!DNL Adobe] の技術手数料の両方を計上できるようにします。 [!UICONTROL Composite Margin %] を指定してください

* **[!UICONTROL Margin %]:** （利益幅が固定された [!UICONTROL Margin % of Total Budget] を使用するキャンペーン）代理店手数料として源泉徴収される総支出の割合。 利益値に対する変更は、キャンペーンの過去の総支出ではなく、将来の総支出にのみ適用されます。 [!UICONTROL Estimated Tax Withholding] の値は、マージンが適用される前に総支出から除外されます。 以下の例を参照してください。これらの例では、キャンペーンが過少または過剰に支出されていないことを前提としています。

   * 例 1:[!UICONTROL Gross Budget] が `100 USD` で、[!UICONTROL Margin %] がフライト全体で `5%` であるとします。 キャンペーンフライトの終了時に、代理店手数料は `5 USD` （`5% of 100 USD`）として計算され、純支出は `95 USD` （`campaign budget [100 USD] - agency fees [5 USD]`）になります。

   * 例 2 マージンを変更した場合：同じキャンペーンで、総支出が [!UICONTROL Margin %] 定されたときに `5%` が `10%` から `40 USD` に変更されたとします。 変更前の期間は `2 USD` （`5% of 40 USD`）として、変更後の期間は `6 USD` （`10% of 60 USD`）として計算されます。 総代理店手数料は `8 USD` （`2 USD + 6 USD`）として計算され、純支出は `92 USD` （`campaign budget [100 USD] - total agency fees [8 USD]`）です。

   * 例 3 源泉徴収税を使用する場合：[!UICONTROL Gross Budget] が `100 USD` で、キャンペーンのフライトの最後の [!UICONTROL Estimated Tax Withholding] が `10 USD` で、[!UICONTROL Margin %] がフライト全体で `5%` であるとします。 キャンペーンフライトの終了時に、代理店手数料は `4.5 USD` （`5% of (campaign budget [100 USD] - tax withholding [USD 10])`）として計算され、純支出は `85.5 USD` （`campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`）になります。

* **[!UICONTROL Composite Margin %]:** （複合マージンを持つ [!UICONTROL Margin % of Total Budget] を使用するキャンペーン）技術手数料と代理店手数料を組み合わせた場合に源泉徴収される、総支出 [!DNL Adobe] 割合。 代理店手数料は、合成利益金額からAdobe工費を差し引いて算出しています。 複合マージン値に対する変更は、キャンペーンの過去の総支出ではなく、将来の総支出にのみ適用されます。 [!UICONTROL Estimated Tax Withholding] の値は、合成マージンが適用される前に総支出から除外されます。

  例えば、[!UICONTROL Gross Budget] が `100 USD` で、キャンペーンフライト終了時の [!DNL Adobe] の技術料金が `10 USD` で、[!UICONTROL Composite Margin %] がフライト全体で `17%` であるとします。 キャンペーンフライトの終了時（キャンペーンが過少支出または過剰支出に該当しないと仮定）、エージェンシー料金は `7 USD` （`(17% of 100 USD) - 10`）として計算され、純支出は `93 USD` （`campaign budget [100 USD] - agency fees [7 USD]`）になります。

* **[!UICONTROL Markup %]:** （[!UICONTROL Apply Markup % on top of individual cost components] を使用するキャンペーン）エージェンシー料金を計算するために指定のコストコンポーネントに適用する割合。 マークアップ値に対する変更は、キャンペーンの過去のコストではなく、将来のコストにのみ適用されます。

* **[!UICONTROL Select cost components on which markup will be applied]:** （[!UICONTROL Apply Markup % on top of individual cost components] を使用するキャンペーン） [!UICONTROL Markup %] が適用されるコストコンポーネント。 該当するすべてのコンポーネント（*[!UICONTROL Media cost]*、*[!UICONTROL Data and Other costs]*、*[!UICONTROL Adobe tech fees]* のいずれか、または両方）を選択します。 コンポーネントの選択に対する変更は、キャンペーンの過去のコストではなく、将来のコストにのみ適用されます。

  例えば、「[!UICONTROL Markup %]」と「`10%`」の [!UICONTROL Media cost] は [!UICONTROL Data and Other costs] です。 キャンペーンのフライトのいずれかの時点で、メディアコストが `20 USD` で、データおよびその他のコストが `5 USD` で、[!DNL Adobe] 技術コストが `2 USD` の場合、エージェンシー料金は `2.50 USD` （`10% of (20 USD + 5 USD)`）として計算され、総支出は `29.50 USD` （`media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`）となります。

**[!UICONTROL Gross Budget]:** （マージン管理のあるキャンペーンのみ）指定したマージン調整が適用される前のキャンペーン予算の総計。

**[!UICONTROL Budget]:** （マージン管理のないキャンペーン）キャンペーン予算全体。

**[!UICONTROL Estimated Tax Withholding]:** 国または地方税のアカウントレベルで、広告料金、広告配信料金、データ料金の合計支出の割合を源泉徴収します。 料金は予算やペーシングの目的で見積もられるため、請求済みの税率は異なる場合があります。

源泉徴収税を見積る手順は、次のとおりです。

1. 「**[!UICONTROL Update rates here]**」をクリックします。

1. **[!UICONTROL Estimated tax rate]** をパーセンテージで指定します。

1. 税金を源泉徴収する各手数料タイプの横にあるチェック ボックスをオンにします。 料金のタイプは次のとおりです。

   * *[!UICONTROL Include estimated tax - ads fee]:* キャンペーン管理手数料の税金を含む、Advertising DSPのすべてのメディア支出に適用されます。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* メディアとデータを除く、Advertising DSPに対するすべての支出に適用されます。 キャンペーン管理手数料の税金は除外されます

   * *[!UICONTROL Include estimated tax - data fee]:* は、Advertising DSPに関するすべてのデータ支出に適用されます。

1. 「**[!UICONTROL Submit]**」をクリックします。

>[!NOTE]
>
>* 米国では、広告、広告サービス、データ全体で税手数料を含める方法は州によって異なる場合があります。 他の国の組織の場合は、3 つのカテゴリすべてに VAT を計上する税金を含めます。
>
>* これらの値は、アカウントの料金設定でも設定できます。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** （2020 年 6 月 22 日以降に作成された既存のキャンペーンは読み取り専用、2020 年 6 月 22 日（PT）より前に作成されたキャンペーンは使用できません）DSPが広告をターゲットにし、フリークエンシーキャップを適用するレベルです。*同じデバイス* でデバイスをターゲットにするか、*人物* で既知のすべてのデバイスをターゲットにします。 **メモ：** クロスデバイスのサポートは、ユニバーサル ID をターゲットとするプレースメントでは使用できません。

**[!UICONTROL Device Graph]:** （既存のキャンペーンは読み取り専用、人物ベースのクロスデバイスターゲティングのみを使用するキャンペーン）クロスデバイスターゲティングと頻度管理に使用するデバイスグラフ：

* *[!UICONTROL LiveRamp - U.S. only]:* [!DNL LiveRamp] デバイスグラフを使用して配信されるインプレッション（つまり、ターゲットオーディエンスセグメントに含まれていないデバイス）に対する 0.35 USD のCPMでのクロスデバイスターゲティングについて、すべての広告主が利用できます。 クロスデバイスターゲティングはプレースメントレベルで設定できます。

  また、このオプションは、すべての広告主が料金無料で周波数管理とアトリビューション測定に使用できます。

  クロスデバイスサポートは、従来の ID をターゲットとするプレースメントにのみ適用され、ユニバーサル ID （[!DNL LiveRamps] を含む）をターゲットとするプレースメントには適用されません。 ユニバーサル ID のターゲティング、頻度管理、アトリビューションは、ID レベルでのみ適用されます。

**[!UICONTROL Frequency Cap]:** （任意）一意のデバイス、ユニバーサル ID またはユーザー（指定された [!UICONTROL Cross Device Level] とプレースメントの [!UICONTROL Targeting] 設定に応じて）がキャンペーンから広告を提供できる回数。 オプションには、1 日、1 週間または 1 か月あたりの *[!UICONTROL Unlimited]* 数または特定の金額が含まれます。

>[!NOTE]
>
> フリークエンシーキャップは、キャンペーン、パッケージ、プレースメントの各レベルで設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。

**[!UICONTROL Packages]:** キャンペーンに含める [ パッケージ ](/help/dsp/campaign-management/packages/package-about.md)。 既存のパッケージを選択するか、含めるパッケージを作成します。 パッケージを作成する場合、詳しくは、[ パッケージ設定 ](/help/dsp/campaign-management/packages/package-settings.md) に関する説明を参照してください。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>次の設定では、測定およびレポート機能のみが有効になります。 パフォーマンスの最適化は、パッケージレベルとプレースメントレベルでのみ実行されます。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （任意）指定した設定を使用して、ビューアビリティ、詐欺、ブランドセーフティ、オーディエンス検証の [!DNL IAS] しい測定とレポートを有効にします。 追加料金がかかります。

* **[!UICONTROL Measure On]:** 測定対象の在庫：*[!UICONTROL Display and VPAID video inventory]* （デフォルト）または *[!UICONTROL Display, VPAID & VAST video inventory]*。

  >[!NOTE]
  >
  >ビデオのビューアビリティは、VPAID インベントリでのみ測定できます。

* **[!UICONTROL IAS Account ID (AnID)]:** （独自の [!DNL IAS] アカウントを持つ広告主。オプション）組織の [!DNL IAS] アカウント ID。[!DNL IAS] が使用状況について直接請求します。

* **[!UICONTROL IAS Team ID]:** （独自の [!DNL IAS] アカウントを持つ広告主。オプション）組織の [!DNL IAS] アカウントのチーム ID。[!DNL IAS] が使用料を直接請求します。<!-- verify -->

#### オーディエンスの検証

**[!UICONTROL Comscore Campaign Ratings]:** （任意）指定された設定を使用し [!DNL Comscore]、オーディエンスの検証の測定およびレポート [!DNL Campaign Ratings] して検証を有効にします。 追加料金がかかります。

* **[!UICONTROL Target Gender]:** ターゲットとする性別：*[!UICONTROL Both]* （デフォルト）、*[!UICONTROL Male]* または *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットとする年齢の範囲。 必要に応じて、左右のスライダーを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （任意）ターゲットにする国。 [!DNL Comscore] は、サポート対象の国でのみ提供されたインプレッションを測定します。

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** プレースメントレベルの [!UICONTROL Attention Score] 指標（インプレッション間の [!DNL Adelaide] 「[!DNL Attention Units]」の加重平均数）のトラッキングを有効にします。 指標は、コネクテッド TV、VPAID のみのプレロール、ポッドキャスト [!DNL Roku] ないオーディオを除くすべてのプレースメントタイプで使用できます。 DSPでは、関連するすべてのクリエイティブにJavaScript タグを自動的に付加し、[!DNL Adelaide] で公開データをトラッキングして、それを毎日DSPに送信します。 この日付を使用して、より注意スコアの高いプレースメント戦術に向けて手動で支出を最適化できます。

「[!UICONTROL Attention Score]」フィールドは、レポートの [!UICONTROL Metrics] のセクション（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements] の各ビュー内、および [!UICONTROL Sites] プレースメントの詳細ビュー [!UICONTROL Ads] の「[!UICONTROL Inventory]」、「[」、「](/help/dsp/campaign-management/reports/placement-details-view.md)」タブで使用できます。

測定に [!DNL Adelaide] セグメントを使用すると、[!DNL Adelaide] の測定タグを使用して広告から配信されたインプレッションごとにCPM料金が発生します。 この料金は、[ プレースメントレベルのアテンションターゲティング ](/help/dsp/campaign-management/placements/placement-settings.md) の料金とは別のものです。

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 指定された機密レベルに基づいて、[!DNL IAB Open Video Viewability (OpenVV)] のテクノロジーを使用して、ビューアビリティのファーストパーティ測定およびレポートを有効にします。

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Campaign 管理について ](campaign-about.md)
>* [ キャンペーンの作成 ](campaign-create.md)
>* [ キャンペーンの編集 ](campaign-edit.md)
>* [ キャンペーンの変更ログを表示 ](campaign-change-log.md)
