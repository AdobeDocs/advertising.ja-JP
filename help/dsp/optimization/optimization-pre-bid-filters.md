---
title: プレースメントレベルの事前入札フィルターとその使用方法
description: 使用可能なプレースメントレベルの事前入札フィルターを参照し、その使用方法を確認します。
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# プレースメントレベルの事前入札フィルターとその使用方法

| Pre-Bid フィルター | 説明 | このフィルターを使用するタイミング |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | オークションによってクリックスルーが発生する可能性を予測する最小しきい値を設定します。 例えば、しきい値を 0.1% に設定した場合、クリックの予測確率が 0.1% 以上の場合にのみオークションに入札します。<br><br><b> メモ：</b> フィルターは、最適化目標の前に適用されます。 その結果、非常に厳密なフィルターによって支出を防ぐことができます。 | クリックスルー率（CTR）の最小 KPI 目標があり、CTR がしきい値を下回っている場合に予算を費やしたくない場合に使用します。 このフィルターには非常に制限があるので、現実的な目標を設定することが重要です。 プレースメントの他の制限によっては、通常、0.03～07% の目標は出発点として適しています。 必要に応じてサイトレベルで最適化して、指標の改善に役立てることができます。<br><br> 最小限の CTR および可能な限り最高の CPM を達成することが目標である場合は、[!UICONTROL Click Through Rate] フィルターを最適化目標「[!UICONTROL Lowest CPM]」と組み合わせることをお勧めします。 目標が最大 CPM で過剰達成に実際のメリットがなく、最小 CTR の場合は、[!UICONTROL Click Through Rate] フィルターと最適化目標「[!UICONTROL Always Max Bid + Highest CTR]」をペアにする方が適切な場合があります。 |
| [!UICONTROL 100% Completion Rate] | インプレッションに入札する前に満たす必要のある、必須の最小完了率を設定します。 | キャンペーンの主な目標が完了率の場合は、このフィルターを使用します。 他のターゲティングパラメーターでは考慮しますが、65% が推奨される開始率です。 |
| [!UICONTROL Player Size - Adobe] | DSPのデータを使用して、必要な最小プレーヤーサイズを設定します。 しきい値に達したインプレッションに [!UICONTROL Player Size] を付けることができます。 | を使用すると、DSPのデータを使用して完全なエピソードのプレーヤーインベントリで配信していることを確認できます。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | [!DNL Moat] または [!DNL Integral Ad Science] のデータを使用して、必要な最小プレーヤーサイズを設定します（[!DNL IAS]）。 しきい値に達したインプレッションに [!UICONTROL Player Size] を付けることができます。 | を使用すると、プラットフォーム全体の [!DNL Moat] や [!DNL IAS] データを使用して、完全なエピソードのプレーヤーインベントリで配信していることを確認できます。<br><br><b> メモ：</b> このフィルターは、[!DNL Moat] または [!DNL IAS] データを使用するようにキャンペーンが設定されている場合にのみ使用してください。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | DSPのビューアビリティの数値と測定値を使用して、必要な最小ビューアビリティのパーセンテージを設定します。 指定したしきい値に達した場合、インプレッションの入札を行うことができます。<br><br><b> 注：</b><ul><li>キャンペーンの [!UICONTROL Viewability Sensitivity] 設定が「[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]」の場合、[!DNL Media Rating Council] （MRC）ビューアビリティ測定標準がキャンペーンに使用されます。 [!UICONTROL Viewability Sensitivity] 設定が「[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]」の場合、[!DNL GroupM] ビューアビリティ測定標準がキャンペーンに使用されます。</li><li>Adobeの定義はサードパーティの定義とは異なるので、サードパーティのデータとの間にわずかな不一致が生じる場合があります。</li></ul> | ベストプラクティスは、最適化目標と入札前のフィルター設定を、キャンペーンの [!UICONTROL Viewability Sensitivity] 設定と一致させることです。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSPによるキャンペーンの最適化方法 ](optimization-how-dsp-optimizes-campaigns.md)
>* [ パッケージ設定 ](/help/dsp/campaign-management/packages/package-settings.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ キャンペーン設定 ](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [ 最適化目標とその使用方法 ](optimization-goals.md)
