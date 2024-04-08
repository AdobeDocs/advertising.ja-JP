---
title: カスタム目標
description: 最低 CPA または最高 ROAS 用に最適化されたパッケージで成功イベントを定義するカスタム目標について説明します。
feature: DSP Optimization
source-git-commit: c5973ac62ea6925252438dbd67d934303a23ccf3
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# カスタム目標

カスタム目標は、広告主がビジネス目標を達成するために必要な成功イベントを定義します。 最適化目標「」を使用する各パッケージ[!UICONTROL Highest Return on Ad Spend (ROAS)"] または&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]「」には、全体的な最適化目標を達成するのに役立つカスタム目標を含める必要があります。 カスタムの目標は、次のように作成できます *目標* 。対象： [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

各カスタム目標は、1 つ以上のコンバージョン指標と、それらの指標の相対的な重み付けで構成されます。 使用可能なコンバージョン指標には、Adobe Advertisingコンバージョンピクセルを使用してAdobe Analyticsを通じてトラッキングされるすべての指標が含まれます。

例えば、あるキャンペーンの特定のパッケージに関連する 3 つのコンバージョン指標（20 USD の「PDFのダウンロード」、30 USD の「電子メールのサインアップ」、40 USD の「注文確認」）があるとします。 顧客アクションの 1 回限りの金銭的価値に応じて重みを付ける場合、指標の相対的な重みは 1、1.5、2 になります。

1 回 [カスタム目標の作成](#custom-goal-create)の場合は、次のことができます [パッケージに割り当て](/help/dsp/campaign-management/packages/package-settings.md) Adobe Senseiを使用したレポートおよびアルゴリズムの最適化の場合。

## カスタム目標の作成 {#custom-goal-create}

カスタム目標を作成するには、DSP アカウントがにリンクされている必要があります [!DNL Search, Social, & Commerce] 内から同じAdobe Experience Cloud組織 ID を持つアカウント [!DNL Search, Social, & Commerce] クライアント設定。 DSP アカウントがにリンクされていない場合 [!DNL Search, Social, & Commerce] 次に、Adobeアカウントチームにお問い合わせください。

1. へのログイン [!DNL Advertising Search, Social, & Commerce] at （北米のユーザー） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) または（他のすべてのユーザー） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. 目標に含める指標が追跡されていて、製品で使用でき、表示名を含んでいることを確認します。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. 指標を見つけて、次のことを確認します **[!UICONTROL Show in UI and Reports]** 指標に対してが有効になっています。

      >[!NOTE]
      >
      >* [!DNL Analytics] カスタムイベントは、次の命名規則に従います。 `custom_event_[*event #*]_[*Analytics report suite ID*]`. 例： `custom_event_16_examplersid`

   1. 指標の値がでない場合 **[!UICONTROL Display Name]** 列をクリックしてから、セル内をクリックし、表示名を入力して、 **[!UICONTROL Apply].**

1. カスタム目標をとして作成 *目的*:

   1. メインメニューで、 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. ツールバーで、 ![作成](/help/dsp/assets/create-search-ui.png "作成").

   1. 非モバイルデバイスおよびモバイルデバイスの関連する指標とその相対的な数値の重み付けを含む目標設定を入力し、目標を保存します。

      少なくとも 1 つの指標のタイプが指標タイプである必要があります *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] カスタムイベントは、次の命名規則に従います。 `custom_event_[*event #*]_[*Analytics report suite ID*]`. 例： `custom_event_16_examplersid`
      >* [!DNL Analytics] ディメンションとセグメントは、Adobe Advertisingの最適化には使用できません。

      >[!TIP]
      >
      >最適なパフォーマンスを得るには、カスタム目標（目標）の合計指標が、1 日に少なくとも 10 回のコンバージョンを満たす必要があります。 そうでない場合は、製品ページやアプリケーション開始など、追加のサポートコンバージョン指標を目的に追加することをお勧めします。 参照： [カスタム目標を作成するためのベストプラクティス](#custom-goal-best-practices) （ガイドライン用）。

（最適化目標「」を使用するパッケージのDSP パッケージ設定）[!UICONTROL Highest Return on Ad Spend (ROAS)"] または&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]」という目標名が [!UICONTROL Custom Goals] リスト。 目的をパッケージのカスタム目標として選択すると、次のようになります [!UICONTROL Conversion Metric] リストには、目的のすべての目標指標が含まれます。

## カスタム目標を作成するためのベストプラクティス [#custom-goal-best-practices]

### 単一の指標を使用したカスタム目標

次の例は、単一のコンバージョン指標をターゲットとする目標を設定する方法を示しています。

#### 「」を含むキャンペーンの例[!UICONTROL Highest Return on Ad Spend (ROAS)]「最適化目標

キャンペーンの目標が売上高（[!UICONTROL Highest Return on Ad Spend (ROAS)]）、およびすべてのデバイスタイプからの売上高は、同様に重要であり、次に「[!UICONTROL Revenue]」指標。モバイル以外の重み付け（非モバイルデバイスからのコンバージョンの場合）が 1 で、モバイルの重み付け（モバイルデバイスからのコンバージョンの場合）が 1 です。 指標タイプを選択します *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> モバイル重み付けまたはモバイル以外の重み付け（1）は、トラッキングされる売上高$1 ごとに 1 の値と等しくなります。
>
> 例えば、モバイル以外の重み付けが 1 の$250 コンバージョンは、コンバージョンに対して$250 とレポートされます。 コンバージョン指標にモバイル以外の重み付け 0.5 が割り当てられている場合、モバイル以外のデバイスからの$250 のコンバージョンは$125 （Adobe Advertisingが$250 のコンバージョン * 0.5）とレポートされます [!UICONTROL Non-mobile Weight] = 125 ドル）。

#### 「」を含むキャンペーンの例[!UICONTROL Lowest Cost per Acquisition (CPA)]「最適化目標

キャンペーンの目標が獲得あたりの最小コスト（CPA）で、必要な成功イベントが 1 つのみ（「アプリケーションの送信」など）の場合は、その 1 つの指標を含め、指標タイプをとして指定します *[!UICONTROL Goal]*. ベストプラクティスは、モバイル以外の重み付けとモバイルの重み付けの両方を 1 つに設定することです。

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> モバイルの重み付けまたはモバイル以外の重み付け（1）は、トラッキングされる各コンバージョンに対して 1 の値と等しくなります。 例えば、10 件のアプリケーション送信コンバージョンが追跡される場合、10 件のアプリケーション送信コンバージョンがレポートされます。 ただし、コンバージョン指標にモバイル以外の重み付け 0.5 が割り当てられている場合、モバイル以外の 10 個のコンバージョンは 5 としてAdobe Advertisingにレポートされます（10 コンバージョン * 0.5） [!UICONTROL Non-mobile Weight] = 5）。

### 複数の指標を使用したカスタム目標

カスタム目標で複数の指標を使用する場合は、次の 2 つのシナリオがあります。

* キャンペーンの目標には複数の成功イベントがあります。 例えば、複数のオンサイトアクション（PDFのダウンロード、お問い合わせ、電子メールのサインアップ）を広告している場合、すべてのアクションが CPA 目標に貢献します。 目標に 3 つの異なる指標が含まれ、それぞれに 1 つのモバイルおよびモバイル以外の重み付けが含まれる場合、 [!DNL Adobe Sensei] アルゴリズムは、各指標とユーザーデバイスタイプを同じ重要度で処理します。 指標やデバイスタイプによってコストや重要度が異なる場合は、それに応じて相対的な重み付けを調整します。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* カスタム目標の単一コンバージョン指標が、パフォーマンスの最適化に必要な 1 日あたりのコンバージョン数が 10 以上に達していません。 これは、1 日あたりのパッケージ支出が最小限であるか、自然変換の数が限られているために発生する可能性があります。 カスタム目標に追加のサポート指標を追加すると、1 日あたり 10 コンバージョンのしきい値を達成できます。 10 個のサポートイベントは、各ウェイトが 1 未満の場合でも、パッケージが 10 日のしきい値を満たすのに役立ちます。 ただし、それほど多くのイベントを追加する必要はありません。

  カスタム目標にサポート指標を追加する場合は、メインの成功イベントに対する相対的な重要度に従って指標に重みを付け、データポイントの量に留意します。 これにより、Adobe Sensei アルゴリズムは複数の指標のバランスを取り、目標に向けて最適化できます。

  次の目標の例には、それぞれ異なるモバイル以外の重み付けを持つ 3 つの指標が含まれています。アプリケーション送信= 1、アプリケーション開始= 0.1、広告主ランディングページ = 0.01。つまり、非モバイルデバイスからの各アプリケーション送信コンバージョンは、非モバイルデバイスからの平均 10 個のアプリケーション開始コンバージョンと、非モバイルデバイスからの 100 個の広告主ランディングページ コンバージョンと同じ値をビジネスに持ちます。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

代わりに、ランディングページ訪問の重みをアプリケーション送信に等しく設定した場合、ランディングページ訪問数が自然に多くなると、目標を圧倒し、ランディングページ訪問に偏る可能性があります。<!--reword-->

>[!MORELIKETHIS]
>
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSPによるキャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)
