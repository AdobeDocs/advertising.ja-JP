---
title: 決定木ターゲティングを使用したエクスペリエンスの編集
description: 決定ツリーを使用して、ターゲット広告エクスペリエンスの設定を編集する方法を説明します。
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 528
ht-degree: 0%

---

# 決定木ターゲティングを使用したエクスペリエンスの編集

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. （オプション） [特定のエクスペリエンスを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Edit]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

   デフォルトでは、決定ツリーが開きます。

1. （オプション）必要に応じて、決定ツリーと一般設定を切り替えます。

   * 決定ツリーから一般設定を開くには、右上の「**[!UICONTROL Experience Form]**」をクリックします。

   * 一般設定から決定ツリーを開くには、右上の「**[!UICONTROL Decision Tree]**」をクリックします。

1. （オプション）決定ツリーを編集するには、次のいずれかの操作を行います。

   * （[処理中](experience-about.md#experience-statuses) エクスペリエンス）次のいずれかの操作を行います。

      * ライブエクスペリエンスに対する既存の未投稿の変更を破棄するには、**[!UICONTROL Discard and start again]**&#x200B;をクリックします。

      * 既存の未投稿の変更を保持するには、**[!UICONTROL Continue editing draft]**&#x200B;をクリックします。

      * エクスペリエンスの詳細を編集するには、**[!UICONTROL Edit Experience Details]**&#x200B;をクリックします。

   * （オプション）決定ツリーの表示設定を変更します。

     設定は、ログアウトするまで保存されます。

   * スライダーを移動して、ズームインまたはズームアウトします。

   * ![縦の木として表示](/help/creative/assets/tree-vertical.png "縦の木として表示")または![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示")をそれぞれクリックして、縦のリストと横のリストを表示する切り替えます。

   * （オプション）次のいずれかの方法で、広告ターゲットと対応するクリエイターを変更します。

      * 目標：

        *[&#x200B; エクスペリエンスの最終レベル &#x200B;](experience-target-node-add-final.md)にターゲットノードを追加します。

         * [&#x200B; ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)。

         * [&#x200B; ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)。

         * [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)。

      * Creative バンドル：

         * [&#x200B; クリエイターを最終ノードに割り当て解除](experience-assign-creative-bundles.md)。

           最後のノードごとに少なくとも1つのバンドルを割り当てない場合は、エクスペリエンスを保存するときに、割り当てられていないノードごとにデフォルトのクリエイティブを使用することを選択できます。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終的なノードごとにデフォルトのクリエイターを使用する必要があります。

         * [割り当てられたバンドル内のクリエイティブのトラッキング URLをカスタマイズする](experience-tracking-urls-targeting.md)。

         * [割り当てられたバンドルのクリエイティブの最適化とスケジュール &#x200B;](experience-optimization-scheduling-targeting.md)をカスタマイズします。

1. （オプション） [一般的なエクスペリエンス設定](experience-settings-targeting.md)を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックし、次の操作を行います。

   * （最下位レベルの各ノードに少なくとも1つのクリエイティブ バンドルが含まれている場合）「**[!UICONTROL OK]**」をクリックします。

   * （最下位レベルの各ノードに少なくとも1つのクリエイティブバンドルが含まれていない場合）次のいずれかの操作を行います。

      * 必要なクリエイティブバンドルをすべて含めずにエクスペリエンスを保存するには、**[!UICONTROL Save as Draft]**&#x200B;をクリックします。

        [&#x200B; ドラフト &#x200B;](experience-about.md#experience-statuses) エクスペリエンスの広告タグを作成することはできません。

      * クリエイティブバンドルがまだ割り当てられていない各ターゲットにデフォルトのクリエイティブを割り当てるには、**[!UICONTROL Assign Default Creatives]**&#x200B;をクリックします。 デフォルトのクリエイターが割り当てられている更新されたツリーを確認したら、「**[!UICONTROL Save]**」と「**[!UICONTROL OK]**」をクリックします。

      * 決定ツリーの編集を続行するには、**[!UICONTROL Continue Edit]**&#x200B;をクリックします。

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
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [&#x200B; エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
