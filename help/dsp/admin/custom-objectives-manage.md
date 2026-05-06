---
title: カスタム目標の管理
description: パッケージレベルの最適化目標を達成するのに役立つ成功イベントを定義する方法を説明します。
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# カスタム目標の管理

*Search、Social、およびCommerce アカウントにリンクされているDSP アカウントで使用できます*

目標は、広告主がビジネス目標を達成するために設定する成功イベントを定義します。 目標は、[&#x200B; カスタム目標](/help/dsp/campaign-management/packages/package-settings.md)としてDSP パッケージで利用できます。 最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用する各パッケージには、全体的な最適化目標の達成に役立つカスタム目標が含まれている必要があります。

目的は、追跡および最適化される指標（プロパティ）と、これらの指標の相対的な重みによって構成されます。 各目的には、次のようなものがあります。

* 広告主の主な成功指標を表す&#x200B;**[!UICONTROL Goal]指標**。 通常、売上、リード、売上などのパッケージの主要なビジネス成果が含まれます。 各目標には、少なくとも1つの目標指標が必要です。

* オプションの&#x200B;**[!UICONTROL Assist]指標**。目標指標の促進を支援、予測、先行、または貢献します。 例えば、テストドライブやトライアルなどのエンゲージメント指標があります。

  目標イベントを最大化するために、重み付けされたアシストイベントを[!DNL Adobe AI]が自動的に割り当てて更新できるようにします。 独自の重み付けされたアシスト指標を割り当てたい場合は、DSPとAdobe Analyticsの過去のパフォーマンスデータに基づいて、オプションでアシスト指標をレコメンドできます。 レコメンデーションを適用するかどうかを選択できます。

目的オプションへのすべての変更はフィールドレベルで追跡され、変更ログに一覧表示されます。

>[!PREREQUISITES]
>
>目標を作成する前に、Search, Social, &amp; Commerceのお客様でない場合でも、DSP アカウントを同じAdobe Experience Cloud組織IDのSearch, Social, &amp; Commerce アカウントにリンクする必要があります。 DSP アカウントが[!DNL Search, Social, & Commerce] アカウントにリンクされていない場合は、Adobe アカウントチームにお問い合わせください。

>[!NOTE]
>
>* また、Advertising Search, Social, &amp; Commerceでは、 Search, Social, &amp; Commerceの各ポートフォリオには、最適化機能がポートフォリオのクリックと収益モデルを作成できるように、目的が必要です。
>* 複数のDSP パッケージまたは複数のSearch、Social、およびCommerce ポートフォリオに同じ目的を使用できます。

## 利用可能な指標

目標には、次のいずれかを含めることができます。

* [Adobe Advertising コンバージョントラッキングピクセル &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)を使用してAdobe Advertisingが追跡する指標。

* （広告主と[!DNL Adobe Analytics for Advertising]） [&#x200B; コンバージョンとサイトエンゲージメントの指標がAdobe Analytics](/help/integrations/analytics/overview.md)から同期されました。

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## 目標のステータス

[!UICONTROL Settings] > [!UICONTROL Custom Objectives] ビューは、各目標のステータスを示します。 値には、次の項目を含めることができます。

* *[!UICONTROL Waiting]*: レコメンデーションが生成されるまで、目標はドラフト状態です。

* *[!UICONTROL Active]*：目標は保存され、使用可能です。

## レコメンデーションステータス

* *[!UICONTROL Not Initiated]*: レコメンデーションは要求されませんでした。

* *[!UICONTROL Generating]*: レコメンデーションを生成しています。

* *[!UICONTROL Ready]*：推奨事項を適用できます。

* *[!UICONTROL Error]*: レコメンデーションを生成できませんでした。

## 目標の設定

1. メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**&#x200B;をクリックします。

1. 右上の「**[!UICONTROL Create]**」をクリックします。

1. [目標の設定](#custom-objective-settings)を入力します。

   自動入札を選択すると、目的にプロパティ （指標）を&quot;[!UICONTROL Goal]&quot;指標として割り当てることができます。 カスタム入札では、プロパティを「[!UICONTROL Goal]」または重み付けされた「[!UICONTROL Assist]」指標として割り当てることができますが、少なくとも1つの目標指標を含める必要があります。

   目標とアシストのラベルは最適化に影響しません。 含まれる指標の重みのみが最適化に影響します。

1. （カスタム入札を使用した目標、オプション）過去のパフォーマンスデータに基づいて推奨されるアシスト指標を生成するには、下部の「**[!UICONTROL Generate]**」をクリックします。 **[!UICONTROL Generate Recommendation]**&#x200B;で、**[!UICONTROL Generate]**&#x200B;をクリックします。

   推奨される指標の生成には最大で20分かかります。 レコメンデーションの生成中、カスタム目標のステータスは&#x200B;*[!UICONTROL Waiting]*&#x200B;です。 レコメンデーションが生成されたら、「[推奨アシストイベントを表示して適用できます](#view-apply-recommendations)」。

1. （レコメンデーションを生成しなかった場合）右上の「**[!UICONTROL Save]**」をクリックします。

最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用するパッケージの[DSP パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)で、目的の名前が[!UICONTROL Custom Goals] リストに含まれるようになりました。 目的をパッケージのカスタム目標として選択すると、[!UICONTROL Conversion Metric] リストには目的のすべての目標指標が含まれます。

## 目標の編集

1. メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**&#x200B;をクリックします。

1. 行で、**...*** > **[!UICONTROL Edit]**&#x200B;をクリックします。

1. 任意の[目標の設定](#custom-objective-settings)を変更します。

1. （レコメンデーションが使用可能な場合、オプション）推奨指標を表示し、オプションで適用します。

   1. 下部セクションで、**[!UICONTROL View Recommendations]**&#x200B;をクリックします。

   1. レコメンデーションを適用するには、次のいずれかの操作を行います。

      * レコメンデーションの横にある&#x200B;**[!UICONTROL Apply]**&#x200B;をクリックします。

      * レコメンデーションを手動で調整し、レコメンデーションの横にある&#x200B;**[!UICONTROL Apply]**&#x200B;をクリックします。

   1. 「**[!UICONTROL Close]**」をクリックして、[!UICONTROL Recommendations] リストを閉じます。

   変更は、目的の設定を同期した後に有効になります。

1. （カスタム入札を使用した目標、オプション）過去のパフォーマンスデータに基づいて推奨されるアシスト指標を生成するには、下部の「**[!UICONTROL Generate]**」をクリックします。 **[!UICONTROL Generate Recommendation]**&#x200B;で、**[!UICONTROL Generate]**&#x200B;をクリックします。

   推奨される指標の生成には最大で20分かかります。 レコメンデーションの生成中、カスタム目標のステータスは&#x200B;*[!UICONTROL Waiting]*&#x200B;です。 レコメンデーションが生成されたら、「[推奨アシストイベントを表示して適用できます](#view-apply-recommendations)」。

1. （新しいレコメンデーションを生成しなかった場合）右上の「**[!UICONTROL Save]**」をクリックします。

## 推奨アシストイベントの表示と適用 {#view-apply-recommendations}

*カスタム入札を使用した目標*

目的のステータスが&#x200B;*[!UICONTROL Active]*&#x200B;で[!UICONTROL Recommendation Status]が&#x200B;*[!UICONTROL Ready]*&#x200B;の場合、推奨事項を表示し、オプションでそれらを適用できます。

1. メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**&#x200B;をクリックします。

1. 行で、**...*** > **[!UICONTROL Edit]**&#x200B;をクリックします。

1. 下部セクションで、**[!UICONTROL View Recommendations]**&#x200B;をクリックします。

1. （オプション）推奨事項を適用するには、次のいずれかの操作を行います。

   * レコメンデーションの横にある&#x200B;**[!UICONTROL Apply]**&#x200B;をクリックします。

   * レコメンデーションを手動で調整し、レコメンデーションの横にある&#x200B;**[!UICONTROL Apply]**&#x200B;をクリックします。

1. 「**[!UICONTROL Close]**」をクリックして、[!UICONTROL Recommendations] リストを閉じます。

1. 右上の「**[!UICONTROL Save]**」をクリックします。

   変更は、目的の設定を同期した後に有効になります。

## カスタム目標の変更ログの表示

1. メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**&#x200B;をクリックします。

1. 行で、**...*** > **[!UICONTROL Change Log]**&#x200B;をクリックします。

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## カスタムの目標設定 {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| セクション | パラメーター | 説明 |
|---------|-----------|-------------|
| 基本情報 | AMOClient | 広告主の一意のAdobe Advertising ID。 |
| 基本情報 | 客観名 | 目的の名前。<br><br>Advertising DSPのすべての目的の名前には、「ADSP_Registrations」など、「ADSP_」のプレフィックスを付ける必要があります（大文字と小文字は区別されません）。 パッケージに割り当てる際に識別しやすい名前を使用します。 |
|  | 説明 | （オプション）目的の説明。 説明は、カスタム目標リストの名前にカーソルを合わせると表示されます。 説明を含まない場合は、目的の名前が代わりに繰り返されます。 |
| 入札戦略 |  | 目的の入札戦略。設定できるイベントの種類を決定します。<ul><li><b>[!UICONTROL Automated Bidding]:</b>目標にプロパティ （指標）を[!DNL goal]指標として割り当てます。 [!DNL Adobe AI]は、バランスの取れたfunnel アプローチを使用して、目標イベントを最大化するために、重み付けされたアシスト イベントを自動的に割り当てて更新します。</li><li><b>[!UICONTROL Custom Bidding]:</b> プロパティを&quot;[!DNL goal]&quot;または重み付けされた&quot;[!DNL assist]&quot;イベントとして割り当てることで、独自の入札戦略を設定します。 定義済みの戦略に対して、この詳細オプションを使用します。</li></ul>入札戦略を変更すると、以前に選択したすべての指標が消去されます。 |
| プロパティ | [!UICONTROL Available Metrics] | 広告主が追跡するすべての指標。 指標を目標として追加するには、指標の名前の横にある<b>[!UICONTROL Goal]</b>をクリックします。 （[!UICONTROL Custom Bidding]のみ）割り当てられた目標指標を支援する指標を追加するには、指標の名前の横にある<b>[!UICONTROL Assist]</b>をクリックします。<br><br><b> メモ：</b> [!DNL Analytics]個のカスタムイベントは、次の命名規則に従います：`custom_event_[*event #*]_[*Analytics report suite ID*]`。 例：`custom_event_16_examplersid.` [!DNL Analytics]のディメンションとセグメントは、Adobe Advertisingの最適化には使用できません。<br><br><b> ヒント：</b>最適なパフォーマンスを得るには、カスタム目標（目標）内の複合指標を1日あたり合計10個まで使用する必要があります。 そうでない場合は、商品ページやアプリケーションの開始など、サポートするコンバージョン指標を目標に追加するのがベストプラクティスです。 ガイドラインについては、[&#x200B; カスタム目標を作成するためのベストプラクティス &#x200B;](#custom-goal-best-practices)を参照してください。 |
|  | 選択した指標 | 目的に含まれる各コンバージョン指標の名前。 次のいずれかの操作を行います。<ul><li>指標を目標として追加するには、[!UICONTROL Available Metrics]列の指標の名前の横にある<b>[!UICONTROL Goal]</b>をクリックします。</li><li>（[!UICONTROL Custom Bidding]戦略のみ）割り当てられた目標指標を支援する指標を追加するには、[!UICONTROL Available Metrics]列の指標名の横にある<b>[!UICONTROL Assist]</b>をクリックします。 次に、目的の他の指標に対する指標の数値ウェイトを入力します。 重みは0.001から1までで、小数を含めることができます。 デフォルトの重みは1です。</li><li>（[!UICONTROL Custom Bidding]戦略のみ）アシスト指標の重みを編集するには、フィールド内をクリックし、目的の他の指標に対する指標の重みの数値を入力します。 重みは0より大きくなければならず、小数点を含めることができます。 デフォルトの重みは1です。</li><li>目的から指標を削除するには、指標の名前にカーソルを合わせて「**[!UICONTROL X]**」をクリックします。/li></ul>**メモ：**<ul><li>さまざまな指標とその重みが比較的意味のあるものであることを確認します。 たとえば、カウントを直接金額と比較することはできません。</li><li>目的の重みの間の大きな相対的な変化は、パフォーマンスの一時的な変動を引き起こす可能性があるので、変更後のパフォーマンスを監視します。</li></ul>. |

>[!MORELIKETHIS]
>
>* [最適化の目標とその使用方法](/help/dsp/optimization/optimization-goals.md)
>* [&#x200B; カスタム目標に関するベストプラクティス &#x200B;](/help/dsp/optimization/custom-goal.md)
>* [&#x200B; パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [&#x200B; コンバージョンの管理](/help/dsp/admin/conversion-metrics-manage.md)
