---
title: デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集
description: デシジョンツリーを使用してターゲット広告エクスペリエンスの設定を編集する方法を説明します。
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集

*クローズドベータ版*

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のエクスペリエンスを含めます。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Edit]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Edit]** をクリックします。

1. [ 一般的なエクスペリエンス設定 ](experience-settings-targeting.md) を編集します。

1. （オプション）デシジョンツリーを編集するには、右上の「**[!UICONTROL Decision Tree]**」をクリックし、次のいずれかの操作を行います。

   * （[ 処理 ](experience-about.md#experience-statuses) エクスペリエンス）次のいずれかの操作を行います。

      * ライブエクスペリエンスに対する既存の未投稿の変更を破棄するには、「**[!UICONTROL Discard and start again]**」をクリックします。

      * 既存の未投稿の変更を保持するには、[**[!UICONTROL Continue editing draft]**] をクリックします。

      * エクスペリエンスの詳細を編集するには、「**[!UICONTROL Edit Experience Details]**」をクリックします。

   * （任意）デシジョンツリーの表示設定を変更します。

     ログアウトするまで、設定は保存されます。

   * スライダーを移動してズームインまたはズームアウトします。

   * 垂直リストと水平リストの表示を切り替えるには、それぞれ ![ 垂直ツリーとして表示 ](/help/creative/assets/tree-vertical.png " 垂直ツリーとして表示 ") または ![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示") をクリックします。

   * （任意）次のいずれかの方法で、広告ターゲットと対応するクリエイティブを変更します。

      * ターゲット：

        *[ エクスペリエンスの最終レベルにターゲットノード ](experience-target-node-add-final.md) 追加します。

         * [ ノード間にターゲットノードを挿入します ](experience-target-node-add-inner.md)。

         * [ ノード間に兄弟ターゲットノードを追加 ](experience-target-node-add-sibling.md)。

         * [ 子ノードとクリエイティブを同じレベルの別のノードにコピーします ](experience-target-node-copy.md)。

      * クリエイティブバンドル：

         * [ 最終ノードにクリエイティブを割り当てる、割り当てを解除する ](experience-assign-creative-bundles.md)。

           各最終ノードに 1 つ以上のバンドルを割り当てない場合は、エクスペリエンスを保存する際に、未割り当ての各ノードに対してデフォルトのクリエイティブを使用することを選択できます。 公開するには、エクスペリエンスにバンドルを割り当てるか、エクスペリエンスから作成されたすべての広告でデフォルトのクリエイティブを使用する必要があります。

         * [ 割り当てられたバンドル内のクリエイティブのトラッキング URL をカスタマイズ ](experience-tracking-urls-targeting.md)。

         * 割り当てられたバンドルの [ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)。

1. [**[!UICONTROL Save]**] をクリックし、次の操作を行います。

   * （最下部のレベルにある各ノードにクリエイティブバンドルが 1 つ以上含まれている場合）「**[!UICONTROL OK]**」をクリックします。

   * （最下部のレベルにある各ノードに 1 つ以上のクリエイティブバンドルが含まれていない場合）次のいずれかの操作を行います。

      * すべての必要なクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「保存」をクリック **[!UICONTROL Save as Draft]** ます。

        [ ドラフト ](experience-about.md#experience-statuses) エクスペリエンス用の広告タグは作成できません。

      * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

      * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ ターゲット設定エクスペリエンス設定 ](experience-settings-targeting.md)
>* [ 最終レベルへのターゲットノードの追加 ](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入する ](experience-target-node-add-inner.md)
>* [ ノード間に兄弟ターゲットノードを追加する ](experience-target-node-add-sibling.md)
>* [ 子ノードとクリエイティブを同じレベルの別のノードにコピーする ](experience-target-node-copy.md)
>* [ 最終ノードへのクリエイティブの割り当て ](experience-assign-creative-bundles.md)
>* [ 割り当てられたバンドル内のクリエイティブのトラッキング URL のカスタマイズ ](experience-tracking-urls-targeting.md)
>* [ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)
>* [ ライブエクスペリエンス用の広告エクスペリエンスタグのエクスポートと実装 ](/help/creative/experiences/experience-tag-export.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
