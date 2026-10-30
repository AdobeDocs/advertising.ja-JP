---
title: 決定木ターゲティングを使用したエクスペリエンスの編集
description: AIを活用した手動の意思決定ツリーエディターを使用して、ターゲットを絞った広告エクスペリエンスを編集する方法を説明します。
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
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
source-wordcount: '655'
ht-degree: 0%
---
# 決定木ターゲティングを使用したエクスペリエンスの編集

ターゲティングを使用したエクスペリエンスの場合、AI ドリブン型エディター（Beta）がデフォルトで開きます。 AI エージェントを使用するか、キャンバスを直接編集するか、既存の手動エディターを開くことができます。

## エクスペリエンスを開く {#experience-open}

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. （オプション） [特定のエクスペリエンスを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. 次のいずれかの操作を行います。

   * AI駆動型エディターを開くには：

     * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Edit]**&#x200B;をクリックします。

     * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

   * 手動エディターを開くには：

     * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Create Decision Tree Manually (Legacy)]**&#x200B;をクリックします。

     * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Create Decision Tree Manually (Legacy)]**&#x200B;をクリックします。

     * AIを活用したエディターでは，

## AIを活用したエディターを使用した編集（Beta） {#ai-editor}

1. [ エクスペリエンスを開く](#experience-open)。

1. 会話で変更したいターゲティングを記述します。 ターゲットによって影響を受けるブランチを特定するか、キャンバスに表示されている場合はノード IDを特定します。

1. 更新されたツリーを確認し、その他の変更について説明します。 アシスタントが処理を完了するのを待ってから、キャンバスを操作します。

1. （オプション）キャンバスで直接変更を行います。

   * [最終レベルのターゲットを追加](experience-target-node-add-final.md#ai-editor)、[ ターゲットレベルを挿入](experience-target-node-add-inner.md#ai-editor)、または[兄弟ターゲットを追加](experience-target-node-add-sibling.md#ai-editor)。

   * ターゲットの横にある&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**&#x200B;をクリックして値を変更し、**[!UICONTROL Edit Node]**&#x200B;をクリックして、ターゲットの条件を編集します。

   * [子ノードとクリエイティブをコピー](experience-target-node-copy.md#ai-editor)または[ ノードを削除](experience-target-node-delete.md#ai-editor)。

   * [ クリエイティブバンドルの割り当てまたは割り当て解除](experience-assign-creative-bundles.md#ai-editor)。

   * [ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)または[ トラッキング URL](experience-tracking-urls-targeting.md#ai-editor)。

1. [ エクスペリエンスを保存](#save)。

## 手動エディターを使用した編集 {#manual-editor}

1. [ エクスペリエンスを開く](#experience-open)。

1. （ステータス `[processing](experience-about.md#experience-statuses)`のエクスペリエンス）既存の未投稿のドラフトについてプロンプトが表示された場合は、次のいずれかの操作を行います。

   * **[!UICONTROL Continue editing draft]**&#x200B;をクリックして下書きをレビューし、編集を続行します。

   * 「**[!UICONTROL Discard and start again]**」をクリックしてドラフトを破棄し、ライブバージョンから開始します。

   * **[!UICONTROL Cancel this edit]**&#x200B;をクリックして編集を停止します。

1. （オプション）ズームスライダーを調整するか、![縦の木として表示](/help/creative/assets/tree-vertical.png "縦の木として表示")または![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示")をクリックして、向きを変更します。

   ビュー設定は、ログアウトするまで保存されます。

1. 必要に応じてターゲットとクリエイターを変更する：

   * [最終レベルのターゲットを追加](experience-target-node-add-final.md#manual-editor)、[ ノード間にターゲットを挿入](experience-target-node-add-inner.md#manual-editor)または[兄弟ターゲットを追加](experience-target-node-add-sibling.md#manual-editor)。

   * [子ノードとクリエイティブをコピー](experience-target-node-copy.md#manual-editor)または[ ノードを削除](experience-target-node-delete.md#manual-editor)。

   * [ クリエイティブバンドルの割り当てまたは割り当て解除](experience-assign-creative-bundles.md#manual-editor)。

   * [ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)または[ トラッキング URL](experience-tracking-urls-targeting.md#manual-editor)。

1. [ エクスペリエンスを保存](#save)。

## エディターの切り替えやエクスペリエンス設定の編集 {#switch-editors}

>[!IMPORTANT]
>
>AIを活用したエディターを終了する前に、保持したいツリーの変更を保存します。 手動エディターまたはエクスペリエンスフォームに切り替えても、保存されていない変更は転送されません。

* **AIを活用したエディターから手動エディターへ：** 「**[!UICONTROL Manual Decision Tree]**」をクリックします。 確認ダイアログで、**[!UICONTROL Yes]**&#x200B;をクリックして未保存の変更を破棄し、手動エディターを開くか、**[!UICONTROL No]**&#x200B;をクリックして続行します。

* **AIを活用したエディターから一般設定：** **[!UICONTROL Experience Form]**&#x200B;をクリックし、**[!UICONTROL Yes]**&#x200B;をクリックして保存されていないツリーの変更を破棄し、フォームを開きます。 [一般的なエクスペリエンス設定](experience-settings-targeting.md)を編集し、**[!UICONTROL Save]**&#x200B;をクリックします。

* **一般的な設定に対する手動エディター：**&#x200B;保持するツリーの変更を保存し、**[!UICONTROL Experience Form]**&#x200B;をクリックします。 [一般的なエクスペリエンス設定](experience-settings-targeting.md)を編集し、**[!UICONTROL Save]**&#x200B;をクリックします。

* **AI ドリブン型エディターの一般的な設定：** 「**[!UICONTROL Decision Tree]**」をクリックします。 ターゲットエクスペリエンスの一般設定への変更を保存すると、AI駆動型エディターも開きます。

* **AI駆動型エディターへの手動エディター：** ツリーの変更を保存し、[!UICONTROL Experiences] ビューに戻り、エクスペリエンスに「**[!UICONTROL Edit]**」を選択します。

別のエディターを開かずにAI ドリブン型エディターを終了するには、**[!UICONTROL Cancel]**&#x200B;をクリックします。 保存されていないツリーの変更を破棄するには&#x200B;**[!UICONTROL Yes]**&#x200B;をクリックし、編集を続行するには&#x200B;**[!UICONTROL No]**&#x200B;をクリックします。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [ ターゲット設定](experience-settings-targeting.md)
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)
>* [ ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)
>* [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)
>* [ クリエイティブを最終ノードに割り当て](experience-assign-creative-bundles.md)
>* [割り当てられたバンドル内のクリエイティブのトラッキング URLをカスタマイズ ](experience-tracking-urls-targeting.md)
>* [ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)
>* [ ライブエクスペリエンスの広告エクスペリエンスタグの書き出しと実装](/help/creative/experiences/experience-tag-export.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [ エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
