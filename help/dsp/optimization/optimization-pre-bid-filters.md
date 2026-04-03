---
title: プレースメントレベルの入札前フィルターとその使用方法
description: 使用可能なプレースメントレベルの入札前フィルターを参照し、その使用方法を確認します。
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
TQID: https://experienceleague.adobe.com/3-OOibzlRa5ethq6xkaHBngX2kwENFWhCSA-qzJQ-h4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# プレースメントレベルの入札前フィルターとその使用方法

| 入札前のフィルター | 説明 | このフィルターを使用するタイミング |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | オークションがクリックにつながる可能性の最小予測しきい値を設定します。 たとえば、しきい値を0.1%に設定すると、クリックの予測確率が0.1%以上の場合にのみオークションに入札します。<br><br><b>注：</b>最適化目標の前にフィルターが適用されます。 その結果、非常に厳格なフィルターは支出を防ぐことができます。 | クリックスルー率（CTR）の最小KPI目標があり、CTRがしきい値を下回ったときに予算を使いたくない場合に使用します。 このフィルターには制限があるため、現実的な目標を設定することが重要です。 配置に関する他の制限に応じて、03 ～ 07%の目標を設定することが一般的に良い出発点となります。 必要に応じてサイトレベルで最適化することで、指標を向上させることができます。<br><br>CTRを最小限に抑え、可能な限りCPMを最適にすることが目標である場合は、[!UICONTROL Click Through Rate] フィルターと最適化目標「[!UICONTROL Lowest CPM]」を組み合わせて設定することをお勧めします。 目標が、超過に対する真のメリットのない最大CPMであり、最小CTRである場合、[!UICONTROL Click Through Rate] フィルターと最適化目標「[!UICONTROL Always Max Bid + Highest CTR]」を組み合わせることがより適切である可能性があります。 |
| [!UICONTROL 100% Completion Rate] | インプレッションに入札する前に満たす必要がある最低完了率を設定します。 | このフィルターは、キャンペーンの主な目標が完了率である場合に使用します。 他のターゲティングパラメーターも考慮しますが、65%が推奨される開始率です。 |
| [!UICONTROL Player Size - Adobe] | DSPのデータを使用して、必要な最小プレイヤーサイズを設定します。 [!UICONTROL Player Size]しきい値を満たした場合は、インプレッションに入札できます。 | DSPのデータを使用して、エピソード全体のプレーヤー在庫を確実に納品するために使用します。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | [!DNL Moat]または[!DNL Integral Ad Science] （[!DNL IAS]）のデータを使用して、必要な最小プレイヤーサイズを設定します。 [!UICONTROL Player Size]しきい値を満たした場合は、インプレッションに入札できます。 | プラットフォーム全体の[!DNL Moat]または[!DNL IAS] データを使用して、エピソード全体のプレーヤー在庫を確実に配信するために使用します。<br><br><b> メモ：</b>このフィルターは、キャンペーンが[!DNL Moat]または[!DNL IAS] データを使用するように設定されている場合にのみ使用します。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | DSPの表示可能率の数値と測定値を使用して、必要な最小表示率を設定します。 指定されたしきい値に達すると、インプレッションに入札できます。<br><br><b> メモ：</b><ul><li>キャンペーンの[!UICONTROL Viewability Sensitivity]設定が「[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]」の場合、キャンペーンには[!DNL Media Rating Council] （MRC）表示可能性測定標準が使用されます。 [!UICONTROL Viewability Sensitivity]設定が「[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]」の場合は、[!DNL GroupM]の表示可能性測定標準がキャンペーンに使用されます。</li><li>Adobe測定の定義はサードパーティの定義とは異なるため、サードパーティデータと若干の相違がある場合があります。</li></ul> | ベストプラクティスは、最適化目標と入札前のフィルター設定をキャンペーンの[!UICONTROL Viewability Sensitivity]設定と一致させることです。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSPによるキャンペーンの最適化](optimization-how-dsp-optimizes-campaigns.md)
>* [&#x200B; パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [&#x200B; キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最適化の目標とその使用方法](optimization-goals.md)
