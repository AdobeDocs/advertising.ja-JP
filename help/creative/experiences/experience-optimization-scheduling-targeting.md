---
title: エクスペリエンスのクリエイティブの最適化とスケジュールのカスタマイズ
description: 方法を学ぶ
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 4d0f4b2a46a65c7fa1afec0a4ef419e58b8f8f59
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# 意思決定ツリーターゲティングを使用したエクスペリエンスのクリエイティブの最適化とスケジュールのカスタマイズ

*既存のクリエイティブを持つターゲットノードのみ*
*クローズドベータ版*

デフォルトでは、エクスペリエンスのクリエイティブローテーションは、全体的なクリックスルー率を最適化するためにアルゴリズムによって決定され、クリエイティブの最適化設定は、割り当てられたすべてのバンドルに適用されます。 クリエイティブローテーションをカスタマイズし、相対ウェイトに従って各バンドルにクリエイティブを手動で実行したり、指定したAdvertising DSPのカスタム目標に合わせてアルゴリズムで最適化したりできます。 <!-- verify --> 特定のクリエイティブバンドルを指定した期間に連続して実行するようにスケジュールし、各スケジュールにカスタムのクリエイティブローテーション設定を適用することもできます。

>[!NOTE]
>
>これらの機能は、割り当てられたクリエイティブの代わりにデフォルトの画像クリエイティブを使用するノードでは使用できません。

## スケジュールを設定しない Creative Optimization の設定

クリエイティブスケジュールが無効になっている場合、クリエイティブの最適化設定は、割り当てられたすべてのクリエイティブに適用されます。

1. ターゲットノードの下にあるクリエイティブリーフノードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]** をクリックします。

1. **[!UICONTROL Schedule]** を無効にします。

1. クリエイティブローテーションのタイプを選択します。

   * &amp;ast;&amp;ast; *Weighted* &amp;ast;&amp;ast; – 各バンドルのクリエイティブを、相対的な重みに従って手動で回転します。 各バンドルの重みをパーセントで入力します。 すべてのバンドルの重みは、最大 100 を加算する必要があります。

   * &amp;ast;&amp;ast;&amp;Algorithmic *&amp;* amp;&amp;ast; – 指定した最適化目標に従って、各バンドルのクリエイティブをアルゴリズムによって回転させます。

      * **[!UICONTROL Optimization Goal]** の場合は、「*[!UICONTROL Click Through Rate]*」または「*[!UICONTROL Custom Objective]*」を選択します。  *[!UICONTROL Custom Objective]* を選択した場合は、既存の [Advertising DSPのカスタム目標 ](/help/dsp/optimization/custom-goal.md).<!-- Verify --> を選択します

1. 「**[!UICONTROL Save]**」をクリックします。

## クリエイティブスケジュールを使用した Creative Optimization の設定

オプションで、エクスペリエンスの開始日と終了日の間の特定のクリエイティブバンドルを指定した連続した期間に実行するようにスケジュールし、各スケジュールにカスタムのクリエイティブローテーション設定を適用できます。 例えば、バンドル 1 を最初の 2 週間に実行してクリックスルー率を最適化し、バンドル 2 を次の 2 週間に実行して指定したカスタム目標を最適化するようにスケジュールできます。

スケジュールを使用する場合は、エクスペリエンスの期間中にバンドルをスケジュールする必要があります。

1. ターゲットノードの下にあるクリエイティブリーフノードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]** をクリックします。

1. **[!UICONTROL Schedule]** を有効にします。

1. 最初のスケジュールの場合：

   1. 左の列で、最初のスケジュールに追加する各クリエイティブバンドルの横にあるチェックボックスを選択します。

   1. スケジュールの開始日と終了日を指定します。

   1. クリエイティブローテーションのタイプを選択します。

      * &amp;ast;&amp;ast; *Weighted* &amp;ast;&amp;ast; – 各バンドルのクリエイティブを、相対的な重みに従って手動で回転します。 各バンドルの重みをパーセントで入力します。 選択したすべてのバンドルの重みは、最大 100 を加算する必要があります。

      * &amp;ast;&amp;ast;&amp;Algorithmic *&amp;* amp;&amp;ast; – 指定した最適化目標に従って、各バンドルのクリエイティブをアルゴリズムによって回転させます。

         * **[!UICONTROL Optimization Goal]** の場合は、「*[!UICONTROL Click Through Rate]*」または「*[!UICONTROL Custom Objective]*」を選択します。  *[!UICONTROL Custom Objective]* を選択した場合は、既存の [Advertising DSPのカスタム目標 ](/help/dsp/optimization/custom-goal.md).<!-- Verify --> を選択します

1. 追加のスケジュールごとに、次の手順を実行します。

   1. 「**[!UICONTROL + Add Schedule]**」をクリックします。

   1. 左の列で、最初のスケジュールに追加する各クリエイティブバンドルの横にあるチェックボックスを選択します。

   1. スケジュールの開始日と終了日を指定します。

   1. クリエイティブローテーションのタイプを選択します。

      * &amp;ast;&amp;ast; *Weighted* &amp;ast;&amp;ast; – 各バンドルのクリエイティブを、相対的な重みに従って手動で回転します。 各バンドルの重みをパーセントで入力します。 選択したすべてのバンドルの重みは、最大 100 を加算する必要があります。

      * &amp;ast;&amp;ast;&amp;Algorithmic *&amp;* amp;&amp;ast; – 指定した最適化目標に従って、各バンドルのクリエイティブをアルゴリズムによって回転させます。

         * **[!UICONTROL Optimization Goal]** の場合は、「*[!UICONTROL Click Through Rate]*」または「*[!UICONTROL Custom Objective]*」を選択します。  *[!UICONTROL Custom Objective]* を選択した場合は、既存の [Advertising DSPのカスタム目標 ](/help/dsp/optimization/custom-goal.md).<!-- Verify --> を選択します

1. 「**[!UICONTROL Save]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除 ](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [ クリエイティブのトラッキング URL のカスタマイズ ](/help/creative/experiences/experience-tracking-urls-targeting.md)
