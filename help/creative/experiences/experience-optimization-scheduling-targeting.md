---
title: エクスペリエンスのクリエイティブの最適化とスケジューリングのカスタマイズ
description: ターゲットエクスペリエンスの最適化と広告スケジュールを設定する方法について説明します。
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%
---
# 決定木ターゲティングにより、エクスペリエンスのクリエイティブの最適化とスケジュールをカスタマイズ

*既存のクリエイターのみを含むTarget ノード*

デフォルトでは、エクスペリエンスは、割り当てられたすべてのバンドルのクリックスルー率を全体的に最適化するために、クリエイティブのローテーションを最適化します。 回転設定をカスタマイズしたり、特定のバンドルをスケジュールして、各スケジュールに対して個別の回転設定を使用して連続期間に実行したりできます。

>[!NOTE]
>
>これらの機能は、割り当てられたクリエイティブの代わりにデフォルトのクリエイティブを使用するノードでは使用できません。

これらの設定は、AI ドリブン型エディター（Beta）のキャンバスまたは手動エディターで直接設定できます。 どちらのエディターでも、バンドルダイアログを保存すると、作業ツリーが更新されます。ツリーヘッダーから[&#x200B; エクスペリエンス &#x200B;](#save)も保存する必要があります。

## 回転設定 {#rotation-settings}

* **[!UICONTROL Weighted]:**&#x200B;関連するクリエイティブバンドルの広告バリエーションを、相対的な重みに従って表示します。

* **[!UICONTROL Algorithmic]:** クリックスルー率やAdvertising DSPのカスタム目標など、指定された最適化目標に基づいて、最も効果的な広告バリエーションをより頻繁に表示します。

* **[!UICONTROL Sequence]（AI駆動型エディター）または[!UICONTROL Sequencing] （手動エディター）:**&#x200B;関連するクリエイティブバンドルを、シーケンス内の各バンドルに対して指定された数のインプレッション数で、指定された順序で表示します。 デフォルトでは、バンドルはエクスペリエンスに追加された順序で順序付けされます。 提供される広告のサイズは、利用可能な在庫によって決まります。 最終的なバンドルは無期限に提供できます（デフォルト）。または、シーケンスは最初のバンドルにループバックできます。

  例えば、シーケンスでは、3つのインプレッションに対してバンドル 1の広告バリアント、1つのインプレッションに対してバンドル 2の広告バリアント、2つのインプレッションに対してバンドル 3の広告バリアントを配信し、その後を繰り返すことができます。 ループせずに、バンドル 3は無期限に機能し続けます。

## スケジュールを設定せずにクリエイティブの最適化を実施

クリエイティブのスケジュール設定を無効にすると、割り当てられたすべてのクリエイティブにクリエイティブの最適化設定が適用されます。

### AI ドリブン型エディターの使用（Beta） {#without-scheduling-ai}

1. エクスペリエンスを[作成](experience-create-targeting.md#ai-editor)または[編集](experience-edit-targeting.md#ai-editor)している間に、クリエイティブ リーフ ノードの&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

   バンドルのない最終ノードの場合は、**[!UICONTROL Assign Bundles]**&#x200B;をクリックし、[&#x200B; バンドルを最初に割り当てます](experience-assign-creative-bundles.md#ai-editor)。

1. 「**[!UICONTROL Creative optimisation]**」タブを開きます。

1. **[!UICONTROL Schedule]**&#x200B;を無効にします。

1. クリエイティブの回転タイプを選択し、その設定を行います。

   * **[!UICONTROL Weighted]:**&#x200B;各バンドル行の相対的な重みを入力します。 重みは合計100でなければなりません。 重みを均等に配分するには、**[!UICONTROL Apply equal weight]**&#x200B;をクリックします。

   * **[!UICONTROL Algorithmic]:** **[!UICONTROL Optimization goals]** オプションを選択します。 カスタム目標を選択する場合は、**[!UICONTROL Custom objective]**&#x200B;の既存の[Advertising DSP カスタム目標](/help/dsp/optimization/custom-goal.md)を選択します。

   * **[!UICONTROL Sequence]:** バンドルを目的の順序にドラッグし、各シーケンスのインプレッション数を入力します。 **[!UICONTROL Keep in loop]**&#x200B;を有効にしてシーケンスを繰り返すか、最後のバンドルのインプレッションを&#x200B;**[!UICONTROL Infinite]**&#x200B;に設定することを無効のままにします。

1. ダイアログで「**[!UICONTROL Save]**」をクリックします。

1. [&#x200B; エクスペリエンスを保存](#save)。

### 手動エディターの使用 {#without-scheduling-manual}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. エクスペリエンスを[作成](experience-create-targeting.md)または[編集](experience-edit-targeting.md)している間に、クリエイティブ最適化の設定を開きます。

   1. ターゲットノードの下にあるクリエイティブリーフノードの上にカーソルを置き、次の操作を行います。

      * 既存のバンドルの場合は、**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

      * 新しいバンドルの場合は、**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;をクリックし、[&#x200B; バンドルを割り当てます](experience-assign-creative-bundles.md)。

   1. 「**[!UICONTROL Creative Optimization]**」タブをクリックします。

1. **[!UICONTROL Schedule]**&#x200B;を無効にします。

1. 関連するバンドルの広告バリアントのクリエイティブのローテーションタイプを選択します。

   * *[!UICONTROL Weighted]:*&#x200B;各バンドルの重みをパーセントで入力します。 関連付けられたすべてのバンドルに同じ重みを適用するには、「（![同じ重みを適用](/help/creative/assets/apply-equal-weight.png "同じ重みを適用")）」をクリックします。 選択したすべてのバンドルの重みは、最大100個まで追加する必要があります。

   * *[!UICONTROL Algorithmic]:* **[!UICONTROL Optimization Goal]**&#x200B;の場合は、*[!UICONTROL Click Through Rate]*、（標準ビデオ広告エクスペリエンス） *[!UICONTROL Completion Rate]*&#x200B;または&#x200B;*[!UICONTROL Custom Objective]*&#x200B;を選択します。 *[!UICONTROL Custom Objective]*&#x200B;を選択した場合は、既存の[Advertising DSP カスタム目標](/help/dsp/optimization/custom-goal.md)を選択します。

   * *[!UICONTROL Sequencing]:*

     1. 割り当てられたバンドルを目的の順序にドラッグ&amp;ドロップします。

     1. 各シーケンスのインプレッション数を入力します。

     1. 最後のシーケンスに対して、a\）でシーケンスの最終バンドルを無期限に表示するか（*[!UICONTROL Infinite]* （デフォルト）またはb\）でループして、最終バンドルが表示された後の最初のバンドルに戻るか（*[!UICONTROL Keep in Loop]*）を変更します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## クリエイティブのスケジュール設定によるクリエイティブの最適化

必要に応じて、エクスペリエンスの開始日と終了日の間の指定された連続時間に特定のクリエイティブバンドルを実行するようにスケジュールし、各スケジュールにカスタムクリエイティブローテーション設定を適用することができます。 例えば、クリック率を最適化するために最初の2週間にバンドル 1を実行するようにスケジュールし、指定されたカスタム目標に対して最適化するために、次の2週間にバンドル 2を実行するようにスケジュールできます。

スケジューリングを使用する場合、エクスペリエンスの期間を通じてバンドルをスケジュールする必要があります。

### AI ドリブン型エディターの使用（Beta） {#with-scheduling-ai}

1. エクスペリエンスを[作成](experience-create-targeting.md#ai-editor)または[編集](experience-edit-targeting.md#ai-editor)している間に、クリエイティブ リーフ ノードの&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

   バンドルのない最終ノードの場合は、**[!UICONTROL Assign Bundles]**&#x200B;をクリックし、[&#x200B; バンドルを最初に割り当てます](experience-assign-creative-bundles.md#ai-editor)。

1. 「**[!UICONTROL Creative optimisation]**」タブを開き、**[!UICONTROL Schedule]**&#x200B;を有効にします。

1. スケジュールの&#x200B;**[!UICONTROL Timezone]**&#x200B;を選択します。

1. 最初のスケジュール：

   1. 左側の列に含める各バンドルの横にあるチェックボックスをオンにします。

   1. 開始日と終了日と時刻を指定します。

   1. クリエイティブの回転タイプを選択し、その設定を行います。

      * **[!UICONTROL Weighted]:** スケジュールの各バンドル行の相対的な重みを入力します。 重みは合計100でなければなりません。 重みを均等に配分するには、**[!UICONTROL Apply equal weight]**&#x200B;をクリックします。

      * **[!UICONTROL Algorithmic]:** **[!UICONTROL Optimization goals]** オプションを選択します。 カスタム目標を選択する場合は、**[!UICONTROL Custom objective]**&#x200B;の既存の[Advertising DSP カスタム目標](/help/dsp/optimization/custom-goal.md)を選択します。

      * **[!UICONTROL Sequence]:** バンドルを目的の順序にドラッグし、各シーケンスのインプレッション数を入力します。 **[!UICONTROL Keep in loop]**&#x200B;を有効にしてシーケンスを繰り返すか、最後のバンドルのインプレッションを&#x200B;**[!UICONTROL Infinite]**&#x200B;に設定することを無効のままにします。

1. 追加のスケジュールごとに、**[!UICONTROL + Add Schedule]**&#x200B;をクリックし、スケジュールカードを選択し、バンドル、日付と時刻、およびローテーション設定を設定します。

   バンドルのチェックボックスは、すべてのスケジュールではなく、選択したスケジュールに適用されます。 スケジュールが、割り当てられたバンドルを使用したエクスペリエンス期間全体をカバーしていることを確認します。

1. ダイアログで「**[!UICONTROL Save]**」をクリックします。

1. [&#x200B; エクスペリエンスを保存](#save)。

### 手動エディターの使用 {#with-scheduling-manual}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. エクスペリエンスを[作成](experience-create-targeting.md)または[編集](experience-edit-targeting.md)している間に、クリエイティブ最適化の設定を開きます。

   1. ターゲットノードの下にあるクリエイティブリーフノードの上にカーソルを置き、次の操作を行います。

      * 既存のバンドルの場合は、**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

      * 新しいバンドルの場合は、**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;をクリックし、[&#x200B; バンドルを割り当てます](experience-assign-creative-bundles.md)。

   1. 「**[!UICONTROL Creative Optimization]**」タブをクリックします。

1. **[!UICONTROL Schedule]**&#x200B;を有効にします。

1. 最初のスケジュール：

   1. 左側の列で、最初のスケジュールに追加する各クリエイティブバンドルの横にあるチェックボックスを選択します。

   1. スケジュールの開始日と開始時間、終了日と終了時間を指定します。

   1. クリエイティブの回転タイプを選択します。

      * *[!UICONTROL Weighted]:*&#x200B;各バンドルの重みをパーセントで入力します。 スケジュール内のすべてのバンドルに同じ重みを適用するには、「（![同じ重みを適用](/help/creative/assets/apply-equal-weight.png "同じ重みを適用")）」をクリックします。 選択したすべてのバンドルの重みは、最大100個まで追加する必要があります。

      * *[!UICONTROL Algorithmic]:* **[!UICONTROL Optimization Goal]**&#x200B;の場合は、*[!UICONTROL Click Through Rate]*、（標準ビデオ広告エクスペリエンス） *[!UICONTROL Completion Rate]*&#x200B;または&#x200B;*[!UICONTROL Custom Objective]*&#x200B;を選択します。 *[!UICONTROL Custom Objective]*&#x200B;を選択した場合は、既存の[Advertising DSP カスタム目標](/help/dsp/optimization/custom-goal.md)を選択します。

      * *[!UICONTROL Sequencing]:*

        1. 割り当てられたバンドルを目的の順序にドラッグ&amp;ドロップします。

        1. 各シーケンスのインプレッション数を入力します。

        1. 最後のシーケンスに対して、a\）でシーケンスの最終バンドルを無期限に表示するか（*[!UICONTROL Infinite]* （デフォルト）またはb\）でループして、最終バンドルが表示された後の最初のバンドルに戻るか（*[!UICONTROL Keep in Loop]*）を変更します。

1. 追加の各スケジュールについて：

   1. **[!UICONTROL + Add Schedule]**&#x200B;をクリックします。

   1. 左側の列で、最初のスケジュールに追加する各クリエイティブバンドルの横にあるチェックボックスを選択します。

   1. スケジュールの開始日と終了日を指定します。

   1. クリエイティブの回転タイプを選択します。

      * *[!UICONTROL Weighted]:*&#x200B;各バンドルの重みをパーセントで入力します。 選択したすべてのバンドルの重みは、最大100個まで追加する必要があります。

      * *[!UICONTROL Algorithmic]:* **[!UICONTROL Optimization Goal]**&#x200B;の場合、*[!UICONTROL Click Through Rate]*&#x200B;または&#x200B;*[!UICONTROL Custom Objective]*&#x200B;のいずれかを選択します。 *[!UICONTROL Custom Objective]*&#x200B;を選択した場合は、既存の[Advertising DSP カスタム目標](/help/dsp/optimization/custom-goal.md)を選択します。

      * *[!UICONTROL Sequencing]:*

        1. 割り当てられたバンドルを目的の順序にドラッグ&amp;ドロップします。

        1. 各シーケンスのインプレッション数を入力します。

        1. 最後のシーケンスに対して、a\）でシーケンスの最終バンドルを無期限に表示するか（*[!UICONTROL Infinite]* （デフォルト）またはb\）でループして、最終バンドルが表示された後の最初のバンドルに戻るか（*[!UICONTROL Keep in Loop]*）を変更します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [&#x200B; クリエイティブのトラッキング URLのカスタマイズ &#x200B;](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [&#x200B; エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
