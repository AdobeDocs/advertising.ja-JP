---
title: デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集
description: デシジョンツリーを使用してターゲット広告エクスペリエンスの設定を編集する方法を説明します。
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. （任意） [&#x200B; ビューをカスタマイズ &#x200B;](/help/creative/introduction/customize-data-views.md) して、特定のエクスペリエンスを含めます。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Edit]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Edit]** をクリックします。

   決定ツリーは、デフォルトで開きます。

1. （オプション）必要に応じて、デシジョンツリーと一般設定を切り替えます。

   * デシジョンツリーから一般設定を開くには、右上の「**[!UICONTROL Experience Form]**」をクリックします。

   * [ 一般設定 ] からデシジョンツリーを開くには、右上の [**[!UICONTROL Decision Tree]**] をクリックします。

1. （オプション）デシジョンツリーを編集するには、次のいずれかの操作を行います。

   * （[&#x200B; 処理 &#x200B;](experience-about.md#experience-statuses) エクスペリエンス）次のいずれかの操作を行います。

      * ライブエクスペリエンスに対する既存の未投稿の変更を破棄するには、「**[!UICONTROL Discard and start again]**」をクリックします。

      * 既存の未投稿の変更を保持するには、[**[!UICONTROL Continue editing draft]**] をクリックします。

      * エクスペリエンスの詳細を編集するには、「**[!UICONTROL Edit Experience Details]**」をクリックします。

   * （任意）デシジョンツリーの表示設定を変更します。

     ログアウトするまで、設定は保存されます。

   * スライダーを移動してズームインまたはズームアウトします。

   * 垂直リストと水平リストの表示を切り替えるには、それぞれ ![&#x200B; 垂直ツリーとして表示 &#x200B;](/help/creative/assets/tree-vertical.png " 垂直ツリーとして表示 ") または ![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示") をクリックします。

   * （任意）次のいずれかの方法で、広告ターゲットと対応するクリエイティブを変更します。

      * ターゲット：

        *[&#x200B; エクスペリエンスの最終レベルにターゲットノード &#x200B;](experience-target-node-add-final.md) 追加します。

         * [&#x200B; ノード間にターゲットノードを挿入します &#x200B;](experience-target-node-add-inner.md)。

         * [&#x200B; ノード間に兄弟ターゲットノードを追加 &#x200B;](experience-target-node-add-sibling.md)。

         * [&#x200B; 子ノードとクリエイティブを同じレベルの別のノードにコピーします &#x200B;](experience-target-node-copy.md)。

      * Creative バンドル：

         * [&#x200B; 最終ノードにクリエイティブを割り当てる、割り当てを解除する &#x200B;](experience-assign-creative-bundles.md)。

           各最終ノードに 1 つ以上のバンドルを割り当てない場合は、エクスペリエンスを保存する際に、未割り当ての各ノードに対してデフォルトのクリエイティブを使用することを選択できます。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終ノードごとにデフォルトのクリエイティブを使用する必要があります。

         * [&#x200B; 割り当てられたバンドル内のクリエイティブのトラッキング URL をカスタマイズ &#x200B;](experience-tracking-urls-targeting.md)。

         * 割り当てられたバンドルの [&#x200B; クリエイティブの最適化とスケジュールのカスタマイズ &#x200B;](experience-optimization-scheduling-targeting.md)。

1. （任意） [&#x200B; 一般的なエクスペリエンス設定 &#x200B;](experience-settings-targeting.md) を編集します。

1. [**[!UICONTROL Save]**] をクリックし、次の操作を行います。

   * （最下部のレベルにある各ノードにクリエイティブバンドルが 1 つ以上含まれている場合）「**[!UICONTROL OK]**」をクリックします。

   * （最下部のレベルにある各ノードに 1 つ以上のクリエイティブバンドルが含まれていない場合）次のいずれかの操作を行います。

      * 必要なすべてのクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「**[!UICONTROL Save as Draft]**」をクリックします。

        [&#x200B; ドラフト &#x200B;](experience-about.md#experience-statuses) エクスペリエンス用の広告タグは作成できません。

      * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

      * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

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
>* [&#x200B; デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 &#x200B;](experience-create-targeting.md)
