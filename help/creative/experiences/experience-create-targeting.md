---
title: デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成
description: デシジョンツリーを使用してターゲット設定された広告エクスペリエンスを作成する方法を説明します。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成

デシジョンツリーを使用してターゲット設定された広告エクスペリエンスを作成します。 各エクスペリエンスは、1 つのクリエイティブライブラリの広告を使用します。

>[!NOTE]
>
>* ターゲット設定されたエクスペリエンスを作成した後は、別のワークフローを使用する、ターゲット設定されていないエクスペリエンスに変更することはできません。
>* 広告エクスペリエンスに、実装するキャンペーンと互換性のあるターゲティングが含まれていることを確認します。 階層ターゲティングの動作は、DSPによって異なる場合があります。 広告エクスペリエンスタグをAdvertising DSPにアップロードし、プレースメントに添付すると、広告レベルのターゲティングが、プレースメントレベルのターゲティングの（ではなく）上に適用されます。 例えば、あるプレースメントがオーストラリアのユーザーをターゲットとし、広告が日本のユーザーをターゲットとする場合、その広告は「Everyone Else」分岐をターゲットにします。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 「**[!UICONTROL Create New Experience]**」をクリックします。

1. [&#x200B; 一般的なエクスペリエンス設定 &#x200B;](experience-settings-targeting.md) を入力します。

1. 「**[!UICONTROL Create]**」をクリックします。

1. デシジョンツリーで以下を行います。

   1. （任意）デシジョンツリーの表示設定を変更します。

      ログアウトするまで、設定は保存されます。

      * スライダーを移動してズームインまたはズームアウトします。

      * 垂直リストと水平リストの表示を切り替えるには、それぞれ ![&#x200B; 垂直ツリーとして表示 &#x200B;](/help/creative/assets/tree-vertical.png " 垂直ツリーとして表示 ") または ![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示") をクリックします。

   1. （任意）次のいずれかの方法で、広告ターゲットと対応するクリエイティブを設定します。

      * ターゲット：

         * [&#x200B; ターゲットノードを最終レベルに追加 &#x200B;](experience-target-node-add-final.md) します。

         * [&#x200B; ノード間にターゲットノードを挿入します &#x200B;](experience-target-node-add-inner.md)。

         * [&#x200B; ノード間に兄弟ターゲットノードを追加 &#x200B;](experience-target-node-add-sibling.md)。

         * [&#x200B; 子ノードとクリエイティブを同じレベルの別のノードにコピーします &#x200B;](experience-target-node-copy.md)。

      * Creative バンドル：

         * [&#x200B; 最終ノードにクリエイティブを割り当てる、割り当てを解除する &#x200B;](experience-assign-creative-bundles.md)。

           各最終ノードに 1 つ以上のバンドルを割り当てない場合は、エクスペリエンスを保存する際に、未割り当ての各ノードに対してデフォルトのクリエイティブを使用することを選択できます。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終ノードごとにデフォルトのクリエイティブを使用する必要があります。

         * 割り当てられたバンドルの [&#x200B; クリエイティブの最適化とスケジュールのカスタマイズ &#x200B;](experience-optimization-scheduling-targeting.md)。

         * [&#x200B; 割り当てられたバンドル内のクリエイティブのトラッキング URL をカスタマイズ &#x200B;](experience-tracking-urls-targeting.md)。

1. （オプション）デシジョンツリーと一般設定を切り替えます。

   * デシジョンツリーから一般設定を開くには、右上の「**[!UICONTROL Experience Form]**」をクリックします。

   * [ 一般設定 ] からデシジョンツリーを開くには、右上の [**[!UICONTROL Decision Tree]**] をクリックします。

1. [**[!UICONTROL Save]**] をクリックし、次の操作を行います。

   * （最下部のレベルにある各ノードにクリエイティブバンドルが 1 つ以上含まれている場合）「**[!UICONTROL OK]**」をクリックします。

   * （最下部のレベルにある各ノードに 1 つ以上のクリエイティブバンドルが含まれていない場合）次のいずれかの操作を行います。

      * すべての必要なクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「保存」をクリック **[!UICONTROL Save as Draft]** ます。

        [&#x200B; ドラフト &#x200B;](experience-about.md#experience-statuses) エクスペリエンス用の広告タグは作成できません。

      * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

      * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

エクスペリエンスがライブの場 [!DNL Creative]、該当するクリエイティブサイズまたはビデオ期間ごとに 1 つの広告タグが自動的に作成されます。 その後、[&#x200B; 広告タグを書き出してDSPに実装する &#x200B;](/help/creative/experiences/experience-tag-export.md) ことができます。

ビデオ広告エクスペリエンスの場合、ビデオクリエイティブは、Adobe Advertising DSPによって VAST 2.0 タグとして自動的にトランスコードされるので、プレビューできます。 オプションで、任意のビデオ広告エクスペリエンスタグに [&#x200B; 別のDSP用のトランスコーディングを適用する &#x200B;](experience-tag-video-transcoding.md) ことができます。

>[!MORELIKETHIS]
>
>* [&#x200B; ターゲット設定エクスペリエンス設定 &#x200B;](experience-settings-targeting.md)
>* [&#x200B; 最終レベルへのターゲットノードの追加 &#x200B;](experience-target-node-add-final.md)
>* [&#x200B; ノード間にターゲットノードを挿入する &#x200B;](experience-target-node-add-inner.md)
>* [&#x200B; ノード間に兄弟ターゲットノードを追加する &#x200B;](experience-target-node-add-sibling.md)
>* [&#x200B; 子ノードとクリエイティブを同じレベルの別のノードにコピーする &#x200B;](experience-target-node-copy.md)
>* [&#x200B; 最終ノードへのクリエイティブの割り当て &#x200B;](experience-assign-creative-bundles.md)
>* [&#x200B; 割り当てられたバンドル内のクリエイティブのトラッキング URL のカスタマイズ &#x200B;](experience-tracking-urls-targeting.md)
>* [&#x200B; クリエイティブの最適化とスケジュールのカスタマイズ &#x200B;](experience-optimization-scheduling-targeting.md)
>* [&#x200B; ライブエクスペリエンス用の広告エクスペリエンスタグのエクスポートと実装 &#x200B;](/help/creative/experiences/experience-tag-export.md)
>* [&#x200B; デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集 &#x200B;](experience-edit-targeting.md)
