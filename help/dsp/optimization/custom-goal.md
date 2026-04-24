---
title: カスタム目標
description: 最小CPAまたは最大ROASに最適化されたパッケージで成功イベントを定義するためのカスタム目標について説明します。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 1207
ht-degree: 0%

---

# カスタム目標

カスタム目標は、広告主がビジネス目標を達成するために必要な成功イベントを定義します。 最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用する各パッケージには、全体的な最適化目標の達成に役立つカスタム目標が含まれている必要があります。 カスタム目標は、[!DNL Advertising Search, Social, & Commerce]で&#x200B;*目標*&#x200B;として作成できます。 DSPの各目的の名前には、「ADSP_」というプレフィックスを付ける必要があります。

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

各カスタム目標（目的）は、1つ以上のコンバージョン指標と、これらの指標の相対的な重みづけで構成されます。 使用可能なコンバージョン指標には、Adobe AdvertisingのコンバージョンピクセルとAdobe Analyticsを使用して追跡されたすべての指標が含まれます。 DSPのカスタム目標では、モバイル以外の重みのみを考慮しますが、すべての広告タイプに使用されます。

例えば、3つのコンバージョン指標が、キャンペーンの1つの特定のパッケージに関連するとします。例えば、「PDF ダウンロード」が20 USD、「メール登録」が30 USD、「注文確認」が40 USDです。 顧客アクションの1回限りの金銭的価値に応じて重みを付けたい場合、指標の相対的な重みは1、1.5、2になります。

カスタム目標](#custom-goal-create)を[作成したら、[!DNL Adobe AI]を使用してレポートとアルゴリズムの最適化を行うために、[それをパッケージ ](/help/dsp/campaign-management/packages/package-settings.md)に割り当てることができます。

目標のDSPに関連付けられた指標に対してウェイトのレコメンデーションが自動的に生成され、ワンクリックですべてのウェイトのレコメンデーションを適用できます。 「ADSP_」でプレフィックスが付いた目標に対するすべての重み付けの変更は、DSPで2日以内にアルゴリズムで適用されます。 重み付けの推奨事項について詳しくは、Search, Social, &amp; Commerce内から入手できる「目標」に関する最適化ガイドの章を参照してください。

## カスタム目標の作成 {#custom-goal-create}

カスタム目標を作成するには、[!DNL Search, Social, & Commerce] クライアント設定から同じDSP組織IDを持つ[!DNL Search, Social, & Commerce] アカウントにAdobe CX Enterprise アカウントをリンクする必要があります。 DSP アカウントが[!DNL Search, Social, & Commerce] アカウントにリンクされていない場合は、Adobe アカウントチームにお問い合わせください。

1. [Advertising Search, Social, &amp; Commerce](/help/search-social-commerce/getting-started/sign-in.md){target="_blank"}にログインします。

1. 目標に含める指標が追跡され、製品で使用でき、表示名が含まれていることを確認します。

   1. メインメニューで、**[!UICONTROL Goals]** > **[!UICONTROL Conversions]**&#x200B;をクリックします。

      コンバージョンビューが新しいブラウザーまたはブラウザーのタブで開きます。

   1. 指標を探し、指標に&#x200B;**[!UICONTROL Show in UI and Reports]**&#x200B;が有効になっていることを確認します。

      >[!NOTE]
      >
      >* [!DNL Analytics]個のカスタムイベントは、次の命名規則に従います：`custom_event_[*event #*]_[*Analytics report suite ID*]`。 例：`custom_event_16_examplersid`

   1. 指標が&#x200B;**[!UICONTROL Display Name]**&#x200B;列に値を持たない場合は、セル内をクリックし、表示名を入力して&#x200B;**[!UICONTROL Apply]をクリックします。**

1. [ カスタム目標を&#x200B;*目標*](/help/search-social-commerce/new-ui/goals/objectives/objective-create.md){target="_blank"}&#x200B;として作成します。 次の点を考慮してください。

   * Advertising DSP パッケージに使用する目的の場合、目的の名前の前に「ADSP_Registrations」などの「ADSP_」を付ける必要があります。 接頭辞では大文字と小文字が区別されません。

   * DSPに関連付けられている指標のみを含めます。 Search, Social, &amp; Commerceまたはその他の広告ネットワークに起因する指標は無視されます。

   * 少なくとも1つの指標に指標タイプ *[!UICONTROL Goal]*&#x200B;が必要です。

   * DSPでは、すべての広告にモバイル以外の重みが使用されます。 指定されたモバイルの重みはすべて無視されます。

   >[!NOTE]
   >
   >* [!DNL Analytics]個のカスタムイベントは、次の命名規則に従います：`custom_event_[*event #*]_[*Analytics report suite ID*]`。 例：`custom_event_16_examplersid`
   >* [!DNL Analytics]個のディメンションとセグメントは、Adobe Advertisingの最適化には使用できません。

   >[!TIP]
   >
   >最適なパフォーマンスを得るには、カスタム目標（目標）内の複合指標を合計して、1日あたり少なくとも10回のコンバージョンを行う必要があります。 そうでない場合は、商品ページやアプリケーションの開始など、サポートするコンバージョン指標を目標に追加するのがベストプラクティスです。 ガイドラインについては、[ カスタム目標を作成するためのベストプラクティス ](#custom-goal-best-practices)を参照してください。

最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用するパッケージのDSP パッケージ設定で、目的の名前が[!UICONTROL Custom Goals] リストに含まれるようになりました。 目的をパッケージのカスタム目標として選択すると、[!UICONTROL Conversion Metric] リストには目的のすべての目標指標が含まれます。

## カスタム目標を作成するためのベストプラクティス {#custom-goal-best-practices}

### 単一の指標でカスタム目標を設定

次の例は、単一のコンバージョン指標をターゲットとする目標を設定する方法を示しています。

#### 「[!UICONTROL Highest Return on Ad Spend (ROAS)]」最適化目標を持つキャンペーンの例

キャンペーンの目標が収益（[!UICONTROL Highest Return on Ad Spend (ROAS)]）で、すべてのデバイスタイプからの収益が同じくらい重要な場合は、「[!UICONTROL Revenue]」指標をモバイル以外の重みが1 （1）の指標として含めます。モバイルの重みは無視されます。 指標タイプ *[!UICONTROL Goal]*&#x200B;を選択します。

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> モバイル以外の重みが1 （1）の場合、任意のデバイスのディスプレイ広告で追跡される収益の$1ごとに1 （1）の値に相当します。 例えば、モバイル以外の重みが1 （1）の250 ドルのコンバージョンは、コンバージョンの場合250 ドルと報告されます。 コンバージョン指標にモバイル以外の重みが0.5と割り当てられている場合、$250のコンバージョンは$125とAdobe Advertisingで報告されます（$250 Conversion * 0.5 [!UICONTROL Non-mobile Weight] = $125）。

#### 「[!UICONTROL Lowest Cost per Acquisition (CPA)]」最適化目標を持つキャンペーンの例

キャンペーン目標が顧客獲得単価（CPA）が最も低く、成功イベントが1つだけ必要な場合（「アプリケーション送信」など）、その1つの指標を含め、指標の種類を&#x200B;*[!UICONTROL Goal]*&#x200B;として指定します。 最善の方法は、モバイル以外のウエイトを1つ（1）に設定することです。モバイルのウエイトは無視されます。

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> モバイル以外の重み付け1は、任意のデバイスのディスプレイ広告で追跡されるコンバージョンごとに1の値に相当します。 例えば、10件のアプリケーション送信コンバージョンが追跡された場合、10件のアプリケーション送信コンバージョンが報告されます。 ただし、コンバージョン指標にモバイル以外の重みが0.5に割り当てられている場合、Adobe Advertisingでは10回のコンバージョンが5回（5）と報告されます（10回のコンバージョン * 0.5 [!UICONTROL Non-mobile Weight] = 5）。

### 複数の指標を持つカスタム目標

カスタム目標で複数の指標を使用するには、次の2つのシナリオがあります。

* キャンペーンの目標には、複数の成功イベントがあります。 たとえば、複数のオンサイトアクション（PDFのダウンロード、お問い合わせ、メール登録）の広告を行っている場合、これらはすべてCPA目標に貢献するアクションです。 目標に3つの別々の指標が含まれ、それぞれモバイル以外の重みが1つ（1）である場合、[!DNL Adobe AI]を活用したアルゴリズムは、各指標とユーザーデバイスタイプを同じ重要性で扱います。 異なる指標に様々なコストや重要度がある場合は、それに応じて相対的な重みを調整します。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* カスタム目標のひとつのコンバージョン指標では、パフォーマンスを最適化するために必要な1日あたり最低10回のコンバージョンを達成できません。 これは、1日のパッケージ費用が最小限であるか、自然なコンバージョンの数が限られているため発生する可能性があります。 カスタム目標にさらに支援指標を追加することで、1日あたり10 コンバージョンの閾値を達成することができます。 10個のサポートイベントを使用すると、それぞれの重みが1個より小さい場合でも、パッケージが10個/日のしきい値を満たすことができます（1）。 しかし、そんなに多くのイベントを追加する必要はありません。

  サポート指標をカスタム目標に追加する際には、主要な成功イベントに対する相対的な重要度に従って重み付けをおこない、データポイントの量を考慮します。 これにより、[!DNL Adobe AI]を活用したアルゴリズムで、複数の指標のバランスを取り、目標に向かって最適化することができます。

  次の目標の例には、モバイル以外の重みが異なる3つの指標が含まれています。それぞれ、Application Submit = 1、Application Start = 0.1、Advertiser Landing Page = 0.01です。 つまり、アプリケーション送信の各コンバージョンは、平均10件のアプリケーション開始コンバージョンと100件の広告主ランディングページのコンバージョンと同じ値をビジネスに持ちます。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

代わりに、ランディングページの訪問をアプリケーションの送信に均等に重み付けした場合、ランディングページの訪問の量が自然に多くなると、目標を上回り、ランディングページの訪問に歪む可能性があります。<!--reword-->

>[!MORELIKETHIS]
>
>* [最適化の目標とその使用方法](optimization-goals.md)
>* [ パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSPによるキャンペーンの最適化](optimization-how-dsp-optimizes-campaigns.md)
