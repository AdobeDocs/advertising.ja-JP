---
title: 決定木ターゲティングによるエクスペリエンスの作成
description: 意思決定ツリーを使用して、ターゲット広告エクスペリエンスを作成する方法を説明します。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 625
ht-degree: 0%

---

# 決定木ターゲティングによるエクスペリエンスの作成

デジジョンツリーを使用して、ターゲットを絞った広告体験を構築。 各エクスペリエンスでは、単一のクリエイティブライブラリの広告を使用します。

>[!NOTE]
>
>* ターゲティングされたエクスペリエンスを作成した後で、別のワークフローを使用する非ターゲティングされたエクスペリエンスに変更することはできません。
>* 広告エクスペリエンスには、それを実装するキャンペーンと互換性のあるターゲティングが含まれていることを確認します。 階層的なターゲティングの動作は、DSPによって異なる場合があります。 広告体験タグをAdvertising DSPにアップロードしてプレースメントに添付すると、広告レベルのターゲティングは（代わりに）プレースメントレベルのターゲティングの上に適用されます。 例えば、プレースメントがオーストラリアのユーザーをターゲットにし、広告が日本のユーザーをターゲットにした場合、広告は「その他のユーザー」ブランチをターゲットにします。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. **[!UICONTROL Create New Experience]**&#x200B;をクリックします。

1. [一般的なエクスペリエンス設定](experience-settings-targeting.md)を入力します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

1. 決定ツリーで、次の操作を行います。

   1. （オプション）決定ツリーの表示設定を変更します。

      設定は、ログアウトするまで保存されます。

      * スライダーを移動して、ズームインまたはズームアウトします。

      * ![縦の木として表示](/help/creative/assets/tree-vertical.png "縦の木として表示")または![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示")をそれぞれクリックして、縦のリストと横のリストを表示する切り替えます。

   1. （オプション）次のいずれかの方法で、広告ターゲットと対応するクリエイターを設定します。

      * 目標：

         * [最終レベル &#x200B;](experience-target-node-add-final.md)にターゲットノードを追加します。

         * [&#x200B; ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)。

         * [&#x200B; ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)。

         * [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)。

      * Creative バンドル：

         * [&#x200B; クリエイターを最終ノードに割り当て解除](experience-assign-creative-bundles.md)。

           最後のノードごとに少なくとも1つのバンドルを割り当てない場合は、エクスペリエンスを保存するときに、割り当てられていないノードごとにデフォルトのクリエイティブを使用することを選択できます。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終的なノードごとにデフォルトのクリエイターを使用する必要があります。

         * [割り当てられたバンドルのクリエイティブの最適化とスケジュール &#x200B;](experience-optimization-scheduling-targeting.md)をカスタマイズします。

         * [割り当てられたバンドル内のクリエイティブのトラッキング URLをカスタマイズする](experience-tracking-urls-targeting.md)。

1. （オプション）決定ツリーと一般設定を切り替えます。

   * 決定ツリーから一般設定を開くには、右上の「**[!UICONTROL Experience Form]**」をクリックします。

   * 一般設定から決定ツリーを開くには、右上の「**[!UICONTROL Decision Tree]**」をクリックします。

1. **[!UICONTROL Save]**&#x200B;をクリックし、次の操作を行います。

   * （最下位レベルの各ノードに少なくとも1つのクリエイティブ バンドルが含まれている場合）「**[!UICONTROL OK]**」をクリックします。

   * （最下位レベルの各ノードに少なくとも1つのクリエイティブバンドルが含まれていない場合）次のいずれかの操作を行います。

      * 必要なすべてのクリエイティブ バンドルを含まないエクスペリエンスを保存するには、**[!UICONTROL Save as Draft]**&#x200B;をクリックします。

        [&#x200B; ドラフト &#x200B;](experience-about.md#experience-statuses) エクスペリエンスの広告タグを作成することはできません。

      * クリエイティブバンドルがまだ割り当てられていない各ターゲットにデフォルトのクリエイティブを割り当てるには、**[!UICONTROL Assign Default Creatives]**&#x200B;をクリックします。 デフォルトのクリエイターが割り当てられている更新されたツリーを確認したら、「**[!UICONTROL Save]**」と「**[!UICONTROL OK]**」をクリックします。

      * 決定ツリーの編集を続行するには、**[!UICONTROL Continue Edit]**&#x200B;をクリックします。

エクスペリエンスがライブになると、[!DNL Creative]は、該当するクリエイティブサイズまたはビデオのデュレーションごとに1つの広告タグを自動的に作成します。 その後、[広告タグを書き出して、DSP](/help/creative/experiences/experience-tag-export.md)に実装できます。

ビデオ広告エクスペリエンスの場合、ビデオのクリエイティブはAdobe Advertising DSPによってVAST 2.0 タグとして自動的にトランスコードされるので、プレビューできます。 オプションで[別のDSP](experience-tag-video-transcoding.md)のトランスコードを任意のビデオ広告エクスペリエンスタグに適用できます。

>[!MORELIKETHIS]
>
>* [&#x200B; ターゲット設定](experience-settings-targeting.md)
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [&#x200B; ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)
>* [&#x200B; ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)
>* [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)
>* [&#x200B; クリエイティブを最終ノードに割り当て](experience-assign-creative-bundles.md)
>* [割り当てられたバンドル内のクリエイティブのトラッキング URLをカスタマイズ &#x200B;](experience-tracking-urls-targeting.md)
>* [&#x200B; クリエイティブの最適化とスケジュールのカスタマイズ &#x200B;](experience-optimization-scheduling-targeting.md)
>* [&#x200B; ライブエクスペリエンスの広告エクスペリエンスタグの書き出しと実装](/help/creative/experiences/experience-tag-export.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [&#x200B; エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
