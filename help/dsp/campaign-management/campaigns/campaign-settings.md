---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1034'
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

**[!UICONTROL Margin Management]:** キャンペーンの余白を管理するかどうか：*[!UICONTROL Yes]* または *[!UICONTROL No]* （デフォルト）。

「*[!UICONTROL Yes]」を選択した場合は* マージンのタイプと金額を指定します。

* **[!UICONTROL Margin Type]:** 余白のタイプ。 マージン管理を有効化してキャンペーンを保存すると、マージンタイプを変更できなくなります。

   * *[!UICONTROL Fixed]:* （デフォルト）DSPで、[!UICONTROL Gross Budget] ーザーの固定利益率に基づいて費用の自動計算と上限を行うことができます。

   * *[!UICONTROL Dynamic]:* キャンペーン内のパッケージとプレースメントごとに個別の [!UICONTROL Budget Reserve %] と [!UICONTROL Gross Budget] を指定することで、プレースメントレベルまで余白を管理できます。 DSPは、特定の利益を保証することなく、各プレースメントの財務効率に基づいて最適化します。 固定金額の単位または単位タイプを固定レートで提供することに同意した複数の品目で構成される挿入注文の場合に使用します。

* **[!UICONTROL Fixed Margin %]:** （マージンが固定されているキャンペーンのみ）各挿入順序 <!-- impression? --> のデフォルトのマークアップ （パーセント）。 この金額は、キャンペーンの正味予算を定義するために [!UICONTROL Gross Budget] から差し引かれます。

* **[!UICONTROL Budget Reserve %]:** （固定マージンのあるキャンペーンのみ。オプション） [!UICONTROL Gross Budget] ータの指定した割合を保護手段として予約します。 この金額は、キャンペーンの正味予算を定義するために [!UICONTROL Gross Budget] から差し引かれます。

**[!UICONTROL Gross Budget]:** （マージン管理のあるキャンペーンのみ）指定したマージン調整が適用される前のキャンペーン予算の総計。

オプションで、日次、週次または月次の総予算を追加できます。

1. 「**[!UICONTROL Add an additional Gross Budget]**」をクリックします。

1. **[!UICONTROL Gross Budget]** を入力し、予算間隔（*[!UICONTROL Daily]、*、*[!UICONTROL Weekly]、* または *[!UICONTROL Monthly]*）を選択します。

キャンペーンの支出上限である純予算合計は、マージン設定に基づいて自動的に計算され、この値の下に示されます。

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

**[!UICONTROL Cross Device Level]:** （2020 年 6 月 22 日以降に作成された既存のキャンペーンは読み取り専用、2020 年 6 月 22 日（PT）より前に作成されたキャンペーンは使用できません） DSPが広告をターゲットにし、フリークエンシーキャップを適用するレベル。*同じデバイス* でデバイスをターゲットにしたり、*人物* で既知のすべてのデバイスをターゲットにしたりします。 **メモ：** クロスデバイスのサポートは、ユニバーサル ID をターゲットとするプレースメントでは使用できません。

**[!UICONTROL Device Graph]:** （既存のキャンペーンは読み取り専用、人物ベースのクロスデバイスターゲティングのみを使用するキャンペーン）クロスデバイスターゲティングと頻度管理に使用するデバイスグラフ：

* *[!UICONTROL LiveRamp - U.S. only]:* [!DNL LiveRamp] デバイスグラフを使用して配信されるインプレッションに対して（つまり、ターゲットオーディエンスセグメント内に見つからないデバイスに対して）、0.35 CPM ドルでのクロスデバイスターゲティングを許可しているすべての広告主が利用できます。 クロスデバイスターゲティングはプレースメントレベルで設定できます。

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

**[!UICONTROL Adelaide]:** プレースメントレベルの [!UICONTROL Attention Score] 指標（インプレッション間の [!DNL Adelaide] 「[!DNL Attention Units]」の加重平均数）のトラッキングを有効にします。 指標は、コネクテッド TV、VPAID のみのプレロール、ポッドキャスト [!DNL Roku] ないオーディオを除くすべてのプレースメントタイプで使用できます。 DSPでは、関連するすべてのクリエイティブにJavaScript タグを自動的に付加し、[!DNL Adelaide] で公開データを追跡して、それを毎日DSPに送信します。 この日付を使用して、より注意スコアの高いプレースメント戦術に向けて手動で支出を最適化できます。

「[!UICONTROL Attention Score]」フィールドは、レポートの [!UICONTROL Metrics] のセクション（[!UICONTROL Campaigns]、[!UICONTROL Packages]、[!UICONTROL Placements] の各ビュー内、および [ プレースメントの詳細ビュー ](/help/dsp/campaign-management/reports/placement-details-view.md) の「[!UICONTROL Sites]」、「[!UICONTROL Ads]」、「[!UICONTROL Inventory]」タブで使用できます。

測定に [!DNL Adelaide] セグメントを使用すると、測定タグの付いた広告から配信されるインプレッションごとに CPM 料金が発生 [!DNL Adelaide] ます。 この料金は、[ プレースメントレベルのアテンションターゲティング ](/help/dsp/campaign-management/placements/placement-settings.md) の料金とは別のものです。

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
>* [Campaign Managementについて ](campaign-about.md)
>* [ キャンペーンの作成 ](campaign-create.md)
>* [ キャンペーンの編集 ](campaign-edit.md)
>* [ キャンペーンの変更ログを表示 ](campaign-change-log.md)
