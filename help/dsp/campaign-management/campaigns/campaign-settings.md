---
title: キャンペーン設定
description: 使用可能なキャンペーン設定の説明を参照してください。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 0%

---

# キャンペーン設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** キャンペーン名。

**[!UICONTROL Advertiser]:** （既存のキャンペーンの場合は読み取り専用）該当する広告主（ブランド）。 既存の広告主を選択するか、新しい広告主を作成します。

**[!UICONTROL Advertiser URL]:** 広告主の公式ページ。 このフィールドは、在庫パートナーとの広告承認プロセスを迅速化します。

**[!UICONTROL Timezone]:** （既存のキャンペーンの場合は読み取り専用）レポートおよび入札のタイムゾーン。

**[!UICONTROL Customer PO]:** （オプション）挿入注文/発注書の顧客発注書。

**[キャンペーンの日付]:** キャンペーンの開始日と終了日。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** キャンペーンの余白を管理するかどうか： *[!UICONTROL Yes]* または *[!UICONTROL No]* （デフォルト）。

選択する場合 *[!UICONTROL Yes],* 利益のタイプと金額を指定します。

* **[!UICONTROL Margin Type]:** 余白のタイプ。 マージン管理を有効化してキャンペーンを保存すると、マージンタイプを変更できなくなります。

   * *[!UICONTROL Fixed]:* DSP （デフォルト）を使用すると、 [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* 個別に指定することで、配置レベルまで余白を管理できます [!UICONTROL Budget Reserve %] および [!UICONTROL Gross Budget] キャンペーン内のパッケージとプレースメントごとに。 DSPは、特定の利益を保証することなく、各プレースメントの財務効率に基づいて最適化します。 固定金額の単位または単位タイプを固定レートで提供することに同意した複数の品目で構成される挿入注文の場合に使用します。

* **[!UICONTROL Fixed Margin %]:** （固定マージンのあるキャンペーンのみ）各挿入指示のデフォルトのマークアップ <!-- impression? -->をパーセンテージで表示します。 この金額は、 [!UICONTROL Gross Budget] キャンペーン純予算を定義する場合。

* **[!UICONTROL Budget Reserve %]:** （固定マージンのあるキャンペーンのみ。オプション）指定した割合の [!UICONTROL Gross Budget] 保護手段として。 この金額は、 [!UICONTROL Gross Budget] キャンペーン純予算を定義する場合。

**[!UICONTROL Gross Budget]:** （利益率管理を使用するキャンペーンのみ）指定した限界調整が適用される前の、キャンペーンの総予算。

オプションで、日次、週次または月次の総予算を追加できます。

1. クリック **[!UICONTROL Add an additional Gross Budget]**.

1. を入力 **[!UICONTROL Gross Budget]** 予算間隔を選択します。 *[!UICONTROL Daily],* *[!UICONTROL Weekly],* または *[!UICONTROL Monthly]*.

キャンペーンの支出上限である純予算合計は、マージン設定に基づいて自動的に計算され、この値の下に示されます。

**[!UICONTROL Budget]:** （利益管理のないキャンペーン）キャンペーン予算全体。

**[!UICONTROL Estimated Tax Withholding]:** 国または地方税のアカウントレベルで、広告手数料、広告配信手数料、データ手数料の合計支出の割合を源泉徴収します。 料金は予算やペーシングの目的で見積もられるため、請求済みの税率は異なる場合があります。

源泉徴収税を見積る手順は、次のとおりです。

1. クリック **[!UICONTROL Update rates here]**.

1. を指定 **[!UICONTROL Estimated tax rate]**&#x200B;をパーセンテージで表示します。

1. 税金を源泉徴収する各手数料タイプの横にあるチェック ボックスをオンにします。 料金のタイプは次のとおりです。

   * *[!UICONTROL Include estimated tax - ads fee]:* キャンペーン管理手数料の税金を含む、すべての Advertising DSP メディア支出に適用されます。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* メディアとデータを除く、広告DSPに対するすべての支出に適用されます。 キャンペーン管理手数料の税金は除外されます

   * *[!UICONTROL Include estimated tax - data fee]:* Advertising DSPに関するすべてのデータ支出に適用されます。

1. クリック **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 米国では、広告、広告サービス、データ全体で税手数料を含める方法は州によって異なる場合があります。 他の国の組織の場合は、3 つのカテゴリすべてに VAT を計上する税金を含めます。
>
>* これらの値は、アカウントの料金設定でも設定できます。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** （2020 年 6 月 22 日以降に作成された既存のキャンペーンは読み取り専用、2020 年 6 月 22 日（PT）より前に作成されたキャンペーンは使用できません） DSPが広告をターゲットにし、フリークエンシーキャップを適用するレベル。 *同じデバイス* デバイスをターゲットにする *人物* 既知のすべてのデバイスをまたいで人物をターゲット設定する。

**[!UICONTROL Device Graph]:** （既存のキャンペーンは読み取り専用、人物ベースのクロスデバイスターゲティングのみを使用するキャンペーン）クロスデバイスターゲティングと頻度管理に使用するデバイスグラフ：

* *[!UICONTROL LiveRamp - U.S. only]:* を使用して配信されるインプレッションに対して、すべての広告主がクロスデバイスターゲティングを午後 0.35 CPM ドルで利用できます。 [!DNL LiveRamp] デバイスグラフ（ターゲットオーディエンスセグメント内に見つからないデバイス用）。 クロスデバイスターゲティングはプレースメントレベルで設定できます。

  また、このオプションは、すべての広告主が料金無料で周波数管理とアトリビューション測定に使用できます。

**[!UICONTROL Frequency Cap]:** （任意）一意のデバイスまたはユーザーの回数（指定された回数による） [!UICONTROL Cross Device Level]）は、キャンペーンから広告が提供される場合があります。 次のようなオプションがあります *[!UICONTROL Unlimited]* または、1 日、1 週間または 1 か月あたりの特定の金額。

>[!NOTE]
>
> フリークエンシーキャップは、キャンペーン、パッケージ、プレースメントの各レベルで設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。

**[!UICONTROL Packages]:** この [パッケージ](/help/dsp/campaign-management/packages/package-about.md) をキャンペーンに含めます。 既存のパッケージを選択するか、含めるパッケージを作成します。 パッケージを作成する場合は、の説明を参照してください [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md) を参照してください。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>次の設定では、測定およびレポート機能のみが有効になります。 パフォーマンスの最適化は、パッケージレベルとプレースメントレベルでのみ実行されます。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （オプション）有効 [!DNL IAS] 指定された設定を使用した、ビューアビリティ、詐欺、ブランドセーフティおよびオーディエンス検証の測定とレポート。 追加料金がかかります。

* **[!UICONTROL Measure On]:** 測定する在庫： *[!UICONTROL Display and VPAID video inventory]* （デフォルト）または *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >ビデオのビューアビリティは、VPAID インベントリでのみ測定できます。

* **[!UICONTROL IAS Account ID (AnID)]:** （自己の広告主） [!DNL IAS] アカウント；オプション）組織の [!DNL IAS] アカウント ID [!DNL IAS] は使用状況について直接請求します。

* **[!UICONTROL IAS Team ID]:** （自己の広告主） [!DNL IAS] アカウント（オプション）組織のチーム ID [!DNL IAS] アカウント [!DNL IAS] は使用状況について直接請求します。 <!-- verify -->

**[!UICONTROL MOAT]:** （オプション）有効 [!DNL MOAT] ビューアビリティ、詐欺、ブランドセーフティおよびオーディエンス検証の測定とレポート。 追加料金がかかります。

#### オーディエンスの検証

**[!UICONTROL Nielsen]:** （オプション）有効 [!DNL Nielsen] 指定された設定を使用した、オーディエンス検証の測定とレポート。 追加料金がかかります。

* **[!UICONTROL Target Gender]:** ターゲットにする性別： *[!UICONTROL Both]* （デフォルト）、 *[!UICONTROL Male]*、または *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットにする年齢の範囲。 必要に応じて、左右のスライダーを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （任意）ターゲットにする国。 [!DNL Nielsen] サポート対象の国でのみ提供されたインプレッションを測定します。

**[!UICONTROL comScore vCE]:** （オプション）有効 [!DNL Comscore validated Campaign Essentials (vCE)] 指定された設定を使用した、オーディエンス検証の測定とレポート。 追加料金がかかります。

* **[!UICONTROL Target Gender]:** ターゲットにする性別： *[!UICONTROL Both]* （デフォルト）、 *[!UICONTROL Male]*、または *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** ターゲットにする年齢の範囲。 必要に応じて、左右のスライダーを使用して範囲を狭めます。

* **[!UICONTROL Target Country]:** （任意）ターゲットにする国。 [!DNL Comscore] サポート対象の国でのみ提供されたインプレッションを測定します。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** を使用して、ビューアビリティのファーストパーティ測定とレポートを有効にします。 [!DNL IAB Open Video Viewability (OpenVV)] 指定された感度レベルに基づくテクノロジー：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Campaign Managementについて](campaign-about.md)
>* [キャンペーンの作成](campaign-create.md)
>* [キャンペーンの編集](campaign-edit.md)
>* [キャンペーンの変更ログの表示](campaign-change-log.md)
