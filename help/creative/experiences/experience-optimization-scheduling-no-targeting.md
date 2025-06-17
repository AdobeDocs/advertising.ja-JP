---
title: エクスペリエンスのクリエイティブの最適化とスケジュールのカスタマイズ
description: 方法を学ぶ
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 006b0c61c28f5fac111ccdcc007e1752e05da63f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# 意思決定ツリーターゲティングを使用しないエクスペリエンス向けのクリエイティブの最適化とスケジュールのカスタマイズ

*既存のクリエイティブを使用したエクスペリエンスのみ*
*クローズドベータ版*

デフォルトでは、広告エクスペリエンスタグのクリエイティブのローテーションは、全体的なクリックスルー率を最適化するためにアルゴリズムに基づいて決定され、クリエイティブの最適化設定は割り当てられたすべてのクリエイティブに適用されます。 クリエイティブローテーションをカスタマイズして、相対的な重み付けに従って手動でクリエイティブを実行したり、指定したAdvertising DSPのカスタム目標に合わせてアルゴリズムで最適化したりできます。 指定したクリエイティブを特定の期間に順次実行するようにスケジュールを設定し、各スケジュールにカスタムクリエイティブローテーション設定を適用することもできます。

## スケジュールを設定しない Creative Optimization の設定

クリエイティブスケジュールが無効になっている場合、クリエイティブの最適化設定は、割り当てられたすべてのクリエイティブに適用されます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Tag Manager]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Tag Manager]** をクリックします

1. 該当する広告タグの行の上にカーソルを置き、「![ 広告スケジュール ](/help/creative/assets/edit-gray.png " トラッキング URL を編集 ")」 **[!UICONTROL Ad Schedule]** タンをクリックします。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— 2/2 現在、タグマネージャーにはリスト表示しかありませんが、カード表示はありません。>

1. **[!UICONTROL Schedule]** を無効にします。

1. クリエイティブローテーションのタイプを選択します。

   * *[!UICONTROL Weighted]:* 相対的な重みに従って手動でクリエイティブを回転します。 各クリエイティブの重みをパーセンテージで入力します。 選択したすべてのクリエイティブの重みは、最大 100 を加算する必要があります。

   * *[!UICONTROL Algorithmic]:* 指定した最適化目標に従って、クリエイティブをアルゴリズムによって回転させます。

      * **[!UICONTROL Optimization Goal]** の場合は、「*[!UICONTROL Click Through Rate]*」または「*[!UICONTROL Custom Objective]*」を選択します。  *[!UICONTROL Custom Objective]* を選択した場合は、既存の [Advertising DSPのカスタム目標 ](/help/dsp/optimization/custom-goal.md).<!-- Verify --> を選択します

1. 「**[!UICONTROL Save]**」をクリックします。

## クリエイティブスケジュールを使用した Creative Optimization の設定

オプションで、広告エクスペリエンスタグに使用する特定のクリエイティブをスケジュールして、エクスペリエンスの開始日と終了日の間で指定された連続した期間に実行し、各スケジュールにカスタムクリエイティブローテーション設定を適用できます。 例えば、Creative 1 を最初の 2 週間に実行してクリックスルー率を最適化し、Creative 2 を次の 2 週間に実行して指定したカスタム目標を最適化するようにスケジュールできます。

スケジュールを使用する場合は、エクスペリエンスの期間を通じてクリエイティブをスケジュールする必要があります。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Tag Manager]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Tag Manager]** をクリックします

1. 該当する広告タグの行の上にカーソルを置き、「![ 広告スケジュール ](/help/creative/assets/edit-gray.png " トラッキング URL を編集 ")」 **[!UICONTROL Ad Schedule]** タンをクリックします。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— 2/2 現在、タグマネージャーにはリスト表示しかありませんが、カード表示はありません。>

1. **[!UICONTROL Schedule]** を有効にします。

1. 最初のスケジュールの場合：

   1. 左の列で、最初のスケジュールに追加する各クリエイティブの横にあるチェックボックスを選択します。

   1. スケジュールの開始日と終了日を指定します。

   1. クリエイティブローテーションのタイプを選択します。

      * *[!UICONTROL Weighted]:* 相対的な重みに従って手動でクリエイティブを回転します。 各クリエイティブの重みをパーセンテージで入力します。 選択したすべてのクリエイティブの重みは、最大 100 を加算する必要があります。

      * *[!UICONTROL Algorithmic]:* 指定した最適化目標に従って、クリエイティブをアルゴリズムによって回転させます。

         * **[!UICONTROL Optimization Goal]** の場合は、「*[!UICONTROL Click Through Rate]*」または「*[!UICONTROL Custom Objective]*」を選択します。  *[!UICONTROL Custom Objective]* を選択した場合は、既存の [Advertising DSPのカスタム目標 ](/help/dsp/optimization/custom-goal.md).<!-- Verify --> を選択します

1. 追加のスケジュールごとに、次の手順を実行します。

   1. 「**[!UICONTROL + Add Schedule]**」をクリックします。

   1. 左の列で、最初のスケジュールに追加する各クリエイティブの横にあるチェックボックスを選択します。

   1. スケジュールの開始日と終了日を指定します。

   1. クリエイティブローテーションのタイプを選択します。

      * *[!UICONTROL Weighted]:* 相対的な重みに従って手動でクリエイティブを回転します。 各クリエイティブの重みをパーセンテージで入力します。 選択したすべてのクリエイティブの重みは、最大 100 を加算する必要があります。

      * *[!UICONTROL Algorithmic]:* 指定した最適化目標に従って、クリエイティブをアルゴリズムによって回転させます。

         * **[!UICONTROL Optimization Goal]** の場合は、「*[!UICONTROL Click Through Rate]*」または「*[!UICONTROL Custom Objective]*」を選択します。  *[!UICONTROL Custom Objective]* を選択した場合は、既存の [Advertising DSPのカスタム目標 ](/help/dsp/optimization/custom-goal.md).<!-- Verify --> を選択します

1. 「**[!UICONTROL Save]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 該当するクリエイティブサイズの広告タグを手動で作成 ](/help/creative/experiences/experience-tag-create-manually.md)
>* [ ターゲティングを行わないエクスペリエンスの広告タグへのクリエイティブの割り当て ](experience-tag-assign-creatives.md)
>* [ デシジョンツリーでターゲット設定しないエクスペリエンス用のトラッキング URL のカスタマイズ ](experience-tracking-urls-no-targeting.md)
