---
title: カスタム目標について
description: 最も低い CPA または最も高い ROAS 向けに最適化されたパッケージで成功イベントを定義するためのカスタム目標について説明します。
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# カスタム目標について

カスタム目標は、広告主がビジネス目標を満たすために必要とする成功イベントを定義します。 「 」で終わる最適化目標を使用する各パッケージ[!UICONTROL - Custom Goal]&quot; (&quot;[!UICONTROL Highest ROAS - Custom Goal]) には、全体的な最適化目標の達成に役立つカスタム目標を含める必要があります。 カスタム目標は、 *目標* in [!DNL Advertising Search, Social, & Commerce].

![カスタム目標](/help/dsp/assets/objective-goals.png)

各カスタム目標は、1 つ以上のコンバージョン指標と、それらの指標の相対的な重み付けで構成されます。 使用可能なコンバージョン指標には、Adobe Advertisingコンバージョンピクセルを使用して、およびAdobe Analyticsを通じて追跡されたすべての指標が含まれます。

>[!NOTE]
>
>* [!DNL Analytics] ディメンションとセグメントは、Adobe Advertisingの最適化には使用できません。
>* DSPで Analytics イベントを使用するには、Adobeアカウントチームと協力して、広告主レベルの統合を設定します。
>* [!DNL Analytics] カスタムイベントは、次の命名規則に従います。 `custom_event_[*event #*]_[*Analytics report suite ID*]`. 例： `custom_event_16_examplersid`

例えば、1 つのキャンペーンの特定のパッケージに関連する 3 つのコンバージョン指標があるとします。「PDFのダウンロード」は 20 USD で、「E メールのサインアップ」は 30 USD で、「注文の確認」は 40 USD で評価されます。 顧客アクションの 1 回限りの金額値に従って重み付けを指定する場合、プロパティの相対的な重み付けは 1、2、1.5 になります。

詳しくは、 [カスタム目標の作成に関するベストプラクティス](custom-goal-best-practices.md) カスタム目標の設定方法に関するヒントを参照してください。

一度 [カスタム目標の作成](custom-goal-create.md)を使用する場合、 [パッケージに割り当てる](/help/dsp/campaign-management/packages/package-settings.md) Adobe Senseiを使用したレポートおよびアルゴリズムの最適化のための情報です。

>[!MORELIKETHIS]
>
>* [カスタム目標の作成](custom-goal-create.md)
>* [カスタム目標を構築するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)
