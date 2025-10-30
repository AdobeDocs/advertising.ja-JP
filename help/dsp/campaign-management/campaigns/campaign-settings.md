---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 1b15b14b0ace6137e79b456c7c8f8444efa8acac
workflow-type: tm+mt
source-wordcount: '1062'
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

* **[!UICONTROL How would you like to compute agency fees?]:** （証拠金管理を行うキャンペーンのみ）エージェンシー手数料の計算方法：

   * *[!UICONTROL Margin % of Total Budget]:* （デフォルト）手数料を [!UICONTROL Gross Budget] のパーセンテージとして計算します。 [!UICONTROL Agency Fee Type] （固定または複合）と [!UICONTROL Margin %] または [!UICONTROL Composite Margin %] を指定します。

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* メディアコスト、データおよびその他のコスト、技術料金に、指定した割合 [!DNL Adobe] 加算します。 [!UICONTROL Markup %] を指定し、マークアップを適用するコンポーネントを選択します。

* **[!UICONTROL Agency Fee Type]:** （[!UICONTROL Margin % of Total Budget] を使用するキャンペーン）代理店手数料のタイプ。

   * *[!UICONTROL Fixed]:* （デフォルト）DSPが、[!UICONTROL Gross Budget] ーザーの固定割合に基づいて費用の自動計算と上限を行えるようにします。 [!UICONTROL Margin %] を指定してください

   * *[!UICONTROL Composite]:* DSPで、代理店手数料と [!UICONTROL Gross Budget] の技術手数料の複合割合を使用して、[!DNL Adobe] の割合に基づいて費用の自動計算と上限を設定できます。 [!UICONTROL Composite Margin %] を指定してください

* **[!UICONTROL Margin %]:** （余白が固定された [!UICONTROL Margin % of Total Budget] を使用するキャンペーン）各挿入順序 <!-- impression? --> のデフォルトのマークアップ （割合）。 この金額は、キャンペーンの正味予算を定義するために [!UICONTROL Gross Budget] から差し引かれます。 余白は、[!UICONTROL Estimated Tax Withholding] ージの [!UICONTROL Gross Budget] には適用されません。

* **[!UICONTROL Composite Margin %]:** （複合マージンを持つ [!UICONTROL Margin % of Total Budget] を使用するキャンペーン）代理店手数料と [!DNL Adobe] の技術手数料の合計（パーセンテージ）。 この金額は、キャンペーンの正味予算を定義するために [!UICONTROL Gross Budget] から差し引かれます。 余白は、[!UICONTROL Estimated Tax Withholding] ージの [!UICONTROL Gross Budget] には適用されません。

* **[!UICONTROL Markup %]:** （[!UICONTROL Apply Markup % on top of individual cost components] を使用するキャンペーン）指定したコストコンポーネントに追加する割合。

* **[!UICONTROL Select cost components on which markup will be applied]:** （[!UICONTROL Apply Markup % on top of individual cost components] を使用するキャンペーン） [!UICONTROL Markup %] が適用されるコストコンポーネント。 該当するすべてのコンポーネント（*[!UICONTROL Media cost]*、*[!UICONTROL Data and Other costs]*、*[!UICONTROL Adobe tech fees]* のいずれか、または両方）を選択します。

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
