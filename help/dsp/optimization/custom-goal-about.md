---
title: カスタム目標について
description: 最も低い CPA または最も高い ROAS 向けに最適化されたパッケージで成功イベントを定義するためのカスタム目標について説明します。
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# カスタム目標について

カスタム目標は、広告主がビジネス目標を満たすために必要とする成功イベントを定義します。 最適化目標を使用する各パッケージ[!UICONTROL Highest ROAS - Custom Goal]&quot;または&quot;[!UICONTROL Lowest CPA - Custom Goal]「は、最適化全体の目標を達成するのに役立つカスタム目標を含む必要があります。 カスタム目標は、 *目標* in [!DNL Advertising Search, Social, & Commerce].

![カスタム目標](/help/dsp/assets/objective-goals.png)

各カスタム目標は、1 つ以上の指標で構成されます。 *トランザクションプロパティ*、およびこれらのトランザクションプロパティの相対的な重み付け。 使用可能なトランザクションプロパティには、Adobe広告コンバージョンピクセルおよびAdobe Analyticsを通じて追跡されるすべての指標が含まれます。

>[!NOTE]
>
>* [!DNL Analytics] ディメンションとセグメントは、Adobe広告の最適化には使用できません。
>* DSPで Analytics イベントを使用するには、Adobeアカウントチームと協力して、広告主レベルの統合を設定します。
>* [!DNL Analytics] カスタムイベントは、次の命名規則に従います。 `custom_event_[*event #*]_[*Analytics report suite ID*]`. 例： `custom_event_16_examplersid`


例えば、3 つの指標（トランザクションプロパティ）がキャンペーンの 1 つの特定のパッケージに関連しているとします。20 USD で評価された「PDFのダウンロード」、30 USD で評価された「E メールのサインアップ」、40 USD で評価された「注文確認」。 顧客アクションの 1 回限りの金額に従って重み付けを指定する場合、プロパティの相対的な重みは 1、2、1.5 になります。

詳しくは、 [カスタム目標の作成に関するベストプラクティス](custom-goal-best-practices.md) カスタム目標の設定方法に関するヒントを参照してください。

一度 [カスタム目標の作成](custom-goal-create.md)、 [パッケージに割り当てる](/help/dsp/campaign-management/packages/package-settings.md) Adobe Senseiを使用したレポートおよびアルゴリズムの最適化のための情報です。

>[!MORELIKETHIS]
>
>* [カスタム目標の作成](custom-goal-create.md)
>* [カスタム目標を構築するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)

