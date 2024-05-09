---
title: プレースメントレベルの事前入札フィルターとその使用方法
description: 使用可能なプレースメントレベルの事前入札フィルターを参照し、その使用方法を確認します。
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# プレースメントレベルの事前入札フィルターとその使用方法

| Pre-Bid フィルター | 説明 | このフィルターを使用するタイミング |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | オークションによってクリックスルーが発生する可能性を予測する最小しきい値を設定します。 例えば、しきい値を 0.1% に設定した場合、クリックの予測確率が 0.1% 以上の場合にのみオークションに入札します。<br><br><b>注意：</b> フィルターは、最適化目標の前に適用されます。 その結果、非常に厳密なフィルターによって支出を防ぐことができます。 | クリックスルー率（CTR）の最小 KPI 目標があり、CTR がしきい値を下回っている場合に予算を費やしたくない場合に使用します。 このフィルターには非常に制限があるので、現実的な目標を設定することが重要です。 プレースメントの他の制限によっては、通常、0.03～07% の目標は出発点として適しています。 必要に応じてサイトレベルで最適化して、指標の改善に役立てることができます。<br><br>目的が最小限の CTR と可能な限り最高の CPM を実現することである場合、推奨される設定は、 [!UICONTROL Click Through Rate] 最適化目標「」を使用したフィルタリング[!UICONTROL Lowest CPM].」と入力します。 目標が、オーバー達成率に実際のメリットがなく最大 CPM で、最小 CTR の場合は、 [!UICONTROL Click Through Rate] 最適化目標「」を使用したフィルタリング[!UICONTROL Always Max Bid + Highest CTR]」の方が適切な場合があります。 |
| [!UICONTROL 100% Completion Rate] | インプレッションに入札する前に満たす必要のある、必須の最小完了率を設定します。 | キャンペーンの主な目標が完了率の場合は、このフィルターを使用します。 他のターゲティングパラメーターでは考慮しますが、65% が推奨される開始率です。 |
| [!UICONTROL Player Size - Adobe] | DSPのデータを使用して、必要な最小プレーヤーサイズを設定します。 次の場合は、印象を入札します [!UICONTROL Player Size] しきい値に達しました | を使用すると、DSPのデータを使用して完全なエピソードのプレーヤーインベントリで配信していることを確認できます。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | からのデータを使用して、必要な最小プレーヤーサイズを設定します [!DNL Moat] または [!DNL Integral Ad Science] （[!DNL IAS]）に設定します。 次の場合は、印象を入札します [!UICONTROL Player Size] しきい値に達しました | を使用すると、プラットフォーム全体を使用して完全なエピソードのプレーヤーインベントリで配信していることを確認できます [!DNL Moat] または [!DNL IAS] データ。<br><br><b>注意：</b> このフィルターは、キャンペーンが使用するように設定されている場合にのみ使用します [!DNL Moat] または [!DNL IAS] データ。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | DSPのビューアビリティの数値と測定値を使用して、必要な最小ビューアビリティのパーセンテージを設定します。 指定したしきい値に達すると、インプレッションの入札が行われます。<br><br><b>メモ：</b><ul><li>キャンペーンの [!UICONTROL Viewability Sensitivity] の設定値は``[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],」の後に [!DNL Media Rating Council] キャンペーンには、（MRC）ビューアビリティ測定標準が使用されます。 次の場合 [!UICONTROL Viewability Sensitivity] の設定値は``[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],」の後に [!DNL GroupM] キャンペーンには、ビューアビリティ測定標準が使用されます。</li><li>Adobeの定義はサードパーティの定義とは異なるので、サードパーティのデータとの間にわずかな不一致が生じる場合があります。</li></ul> | ベストプラクティスは、最適化目標と入札前のフィルター設定を、キャンペーンのと一致させることです [!UICONTROL Viewability Sensitivity] の設定値。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSPによるキャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最適化目標とその使用方法](optimization-goals.md)
