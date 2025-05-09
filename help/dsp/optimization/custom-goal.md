---
title: カスタム目標
description: 最低 CPA または最高 ROAS 用に最適化されたパッケージで成功イベントを定義するカスタム目標について説明します。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# カスタム目標

カスタム目標は、広告主がビジネス目標を達成するために必要な成功イベントを定義します。 最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用する各パッケージには、全体的な最適化目標を達成するのに役立つカスタム目標を含める必要があります。 [!DNL Advertising Search, Social, & Commerce] でカスタム目標を *目標* として作成できます。 DSPの各目標の名前には、「ADSP_」というプレフィックスを付ける必要があります。

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

各カスタム目標（目標）は、1 つ以上のコンバージョン指標と、それらの指標の相対的な重み付けで構成されます。 使用可能なコンバージョン指標には、Adobe Advertising コンバージョンピクセルを使用してAdobe Analyticsを通じてトラッキングされるすべての指標が含まれます。 DSPのカスタム目標にはモバイル以外の重み付けが考慮されますが、すべての広告タイプで使用されます。

例えば、あるキャンペーンの特定のパッケージに関連する 3 つのコンバージョン指標（20 USD の「PDFのダウンロード」、30 USD の「電子メールのサインアップ」、40 USD の「注文確認」）があるとします。 顧客アクションの 1 回限りの金銭的価値に応じて重みを付ける場合、指標の相対的な重みは 1、1.5、2 になります。

[ カスタム目標を作成 ](#custom-goal-create) したら、[ パッケージに割り当てる ](/help/dsp/campaign-management/packages/package-settings.md) ことで、Adobe Senseiを使用したレポートやアルゴリズムの最適化を行うことができます。

重み付けレコメンデーションは、目標のDSP属性指標に対して自動的に生成され、ワンクリックですべての重み付けレコメンデーションを適用できます。 「ADSP_」が接頭辞の付いた目標に対するすべての重み付けの変更は、2 日以内にDSPでアルゴリズムにより適用されます。 重み付けの推奨事項について詳しくは、最適化ガイドの「（Beta）新しい目標」の章を参照してください。この章は、検索、ソーシャル、Commerce内から入手できます。

## カスタム目標の作成 {#custom-goal-create}

カスタム目標を作成するには、DSP アカウントが、[!DNL Search, Social, & Commerce] クライアント設定内から同じAdobe Experience Cloud組織 ID を持つ [!DNL Search, Social, & Commerce] アカウントにリンクされている必要があります。 DSP アカウントが [!DNL Search, Social, & Commerce] アカウントにリンクされていない場合は、Adobe アカウントチームにお問い合わせください。

1. （北米のユーザー） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) または（その他すべてのユーザー） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com) で [!DNL Advertising Search, Social, & Commerce] にログインします。

1. 目標に含める指標が追跡されていて、製品で使用でき、表示名を含んでいることを確認します。

   1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Conversions]** をクリックします。

   1. 指標を見つけ、その指標に対して **[!UICONTROL Show in UI and Reports]** が有効になっていることを確認します。

      >[!NOTE]
      >
      >* カスタムイベント [!DNL Analytics]、命名規則 `custom_event_[*event #*]_[*Analytics report suite ID*]` に従います。 例：`custom_event_16_examplersid`

   1. 指標の「**[!UICONTROL Display Name]**」列に値がない場合は、セル内をクリックし、表示名を入力して「**[!UICONTROL Apply]」をクリックします。**

1. カスタム目標を *目標* として作成します。

   1. メインメニューで、**[!UICONTROL Search]**/**[!UICONTROL Optimization]/[!UICONTROL New Objectives Beta]** をクリックします。

   1. ツールバーで、「![ 作成 ](/help/dsp/assets/create-search-ui.png " 作成 ")」をクリックします。

   1. 非モバイルデバイスの関連指標とその相対数値の重み付けを含む目標設定を入力し、目標を保存します。 次の点に留意してください。

      * Advertising DSP パッケージに使用される目標の場合、目標名の先頭には「ADSP_Registrations」のように「ADSP_」を付ける必要があります。 プレフィックスでは大文字と小文字が区別されません。

      * DSPに関連付けられている指標のみを含めます。 検索、ソーシャル、Commerceまたはその他の広告ネットワークに起因する指標は無視されます。

      * 少なくとも 1 つの指標のタイプが *[!UICONTROL Goal]* である必要があります。

      * DSPでは、すべての広告にモバイル以外の重み付けを使用します。 指定したモバイルの重み付けは無視されます。

      >[!NOTE]
      >
      >* カスタムイベント [!DNL Analytics]、命名規則 `custom_event_[*event #*]_[*Analytics report suite ID*]` に従います。 例：`custom_event_16_examplersid`
      >* [!DNL Analytics] のディメンションとセグメントは、Adobe Advertisingの最適化では使用できません。

      >[!TIP]
      >
      >最適なパフォーマンスを得るには、カスタム目標（目標）の合計指標が、1 日に少なくとも 10 回のコンバージョンを満たす必要があります。 そうでない場合は、製品ページやアプリケーション開始など、追加のサポートコンバージョン指標を目的に追加することをお勧めします。 ガイドラインについては、[ カスタム目標を作成するためのベストプラクティス ](#custom-goal-best-practices) を参照してください。

最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用するパッケージのDSP パッケージ設定で、目標名が [!UICONTROL Custom Goals] リストに含まれるようになりました。 目標をパッケージのカスタム目標として選択すると、[!UICONTROL Conversion Metric] のリストには、その目標のすべての目標指標が含まれます。

## カスタム目標を作成するためのベストプラクティス {#custom-goal-best-practices}

### 単一の指標を使用したカスタム目標

次の例は、単一のコンバージョン指標をターゲットとする目標を設定する方法を示しています。

#### 「[!UICONTROL Highest Return on Ad Spend (ROAS)]」の最適化目標を持つキャンペーンの例

キャンペーンの目標が売上高（[!UICONTROL Highest Return on Ad Spend (ROAS)]）で、すべてのデバイスタイプの売上高が同じように重要な場合は、モバイル以外の重み付けが 1 の「[!UICONTROL Revenue]」指標を含めます。モバイルの重み付けは無視されます。 指標タイプ *[!UICONTROL Goal]* を選択します。

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> モバイル以外の重み付け（1）は、任意のデバイスのディスプレイ広告で追跡される売上高の$1 ごとに 1 の値と等しくなります。 例えば、モバイル以外の重み付けが 1 の$250 コンバージョンは、コンバージョンに対して$250 とレポートされます。 コンバージョン指標にモバイル以外の重み付け 0.5 が割り当てられている場合、$250 のコンバージョンは$125 としてAdobe Advertisingにレポートされます（$250 のコンバージョン * 0.5 [!UICONTROL Non-mobile Weight] = $125）。

#### 「[!UICONTROL Lowest Cost per Acquisition (CPA)]」の最適化目標を持つキャンペーンの例

キャンペーンの目標が獲得あたりの最小コスト（CPA）で、必要な成功イベントが 1 つのみ（「アプリケーションの送信」など）の場合は、その 1 つの指標を含め、指標タイプを *[!UICONTROL Goal]* のように指定します。 ベストプラクティスは、モバイル以外の重み付けを 1 に設定することです。モバイルの重み付けは無視されます。

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> モバイル以外の重み付け（1）は、任意のデバイスのディスプレイ広告で追跡されるコンバージョンごとに 1 つの値と等しくなります。 例えば、10 件のアプリケーション送信コンバージョンが追跡される場合、10 件のアプリケーション送信コンバージョンがレポートされます。 ただし、コンバージョン指標にモバイル以外の重み付け 0.5 が割り当てられている場合、10 個のコンバージョンはAdobe Advertisingで 5 とレポートされます（10 個のコンバージョン * 0.5 [!UICONTROL Non-mobile Weight] = 5）。

### 複数の指標を使用したカスタム目標

カスタム目標で複数の指標を使用する場合は、次の 2 つのシナリオがあります。

* キャンペーンの目標には複数の成功イベントがあります。 例えば、複数のオンサイトアクション（PDFのダウンロード、お問い合わせ、電子メールのサインアップ）を目的として広告をしており、すべてのアクションが CPA 目標に貢献している場合があります。 目標に 3 つの個別の指標が含まれ、それぞれに 1 つの非モバイル重み付けが含まれる場合、[!DNL Adobe Sensei] アルゴリズムは各指標とユーザーデバイスタイプを同じ重要度で処理します。 様々な指標のコストや重要度が異なる場合は、それに応じて相対的な重み付けを調整します。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* カスタム目標の単一コンバージョン指標が、パフォーマンスの最適化に必要な 1 日あたりのコンバージョン数が 10 以上に達していません。 これは、1 日あたりのパッケージ支出が最小限であるか、自然変換の数が限られているために発生する可能性があります。 カスタム目標に追加のサポート指標を追加すると、1 日あたり 10 コンバージョンのしきい値を達成できます。 10 個のサポートイベントは、各ウェイトが 1 未満の場合でも、パッケージが 10 日のしきい値を満たすのに役立ちます。 ただし、それほど多くのイベントを追加する必要はありません。

  カスタム目標にサポート指標を追加する場合は、メインの成功イベントに対する相対的な重要度に従って指標に重みを付け、データポイントの量に留意します。 これにより、Adobe Sensei アルゴリズムは複数の指標のバランスを取り、目標に向けて最適化できます。

  次の目標の例には、それぞれ異なるモバイル以外の重み付けを持つ 3 つの指標が含まれています。アプリケーション送信= 1、アプリケーション開始= 0.1、広告主ランディングページ = 0.01。つまり、各アプリケーション送信コンバージョンは、アプリケーション開始コンバージョンが平均 10 個、広告主ランディングページ コンバージョンが平均 100 個と、ビジネスに対して同じ値を持ちます。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

代わりに、ランディングページ訪問の重みをアプリケーション送信に等しく設定した場合、ランディングページ訪問数が自然に多くなると、目標が圧倒され、ランディングページ訪問に偏る可能性があります。<!--reword-->

>[!MORELIKETHIS]
>
>* [ 最適化目標とその使用方法 ](optimization-goals.md)
>* [ パッケージ設定 ](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSPによるキャンペーンの最適化方法 ](optimization-how-dsp-optimizes-campaigns.md)
