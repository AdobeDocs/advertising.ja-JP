---
title: 決定木ターゲティングによるエクスペリエンスの作成
description: AIを活用した手動の意思決定ツリーエディターを使用して、ターゲットを絞った広告エクスペリエンスを作成する方法を説明します。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
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
source-wordcount: '715'
ht-degree: 0%
---
# 決定木ターゲティングによるエクスペリエンスの作成

デジジョンツリーを使用して、ターゲットを絞った広告体験を構築。 各エクスペリエンスでは、単一のクリエイティブライブラリの広告を使用します。

デフォルトでAI ドリブン型エディター（Beta）が開きます。 AI エージェントを使用してツリーを設定するか、そのキャンバスを直接編集できます。 既存の手動エディターに切り替えることもできます。

>[!NOTE]
>
>* ターゲティングされたエクスペリエンスを作成した後で、別のワークフローを使用する非ターゲティングされたエクスペリエンスに変更することはできません。
>* 広告エクスペリエンスには、それを実装するキャンペーンと互換性のあるターゲティングが含まれていることを確認します。 階層的なターゲティングの動作は、DSPによって異なる場合があります。 広告体験タグをAdvertising DSPにアップロードしてプレースメントに添付すると、広告レベルのターゲティングは（代わりに）プレースメントレベルのターゲティングの上に適用されます。 例えば、プレースメントがオーストラリアのユーザーをターゲットにし、広告が日本のユーザーをターゲットにした場合、広告は「その他のユーザー」ブランチをターゲットにします。

## エクスペリエンスの構築

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. **[!UICONTROL Create New Experience]**&#x200B;をクリックします。

1. **[!UICONTROL Targeting]**&#x200B;が有効になっている[一般的なエクスペリエンス設定](experience-settings-targeting.md)を入力します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

   AIを活用した決定ツリーエディターが開き、新しいエクスペリエンスが表示されます。

1. 次のいずれかの手順を使用して、ツリーを設定します。

## AI ドリブン型エディターを使用したツリーの設定（Beta） {#ai-editor}

1. 会話では、各ブランチの基準や、指定したターゲットに一致しない視聴者の処理方法など、希望するターゲット構造を記述します。

1. カンバスのツリーを確認します。 変更を要求するには、それを会話に記述します。 アシスタントが処理を完了するのを待ってから、キャンバスを操作します。

1. （オプション）キャンバスでツリーを直接調整します。

   * [最終レベルのターゲットを追加](experience-target-node-add-final.md#ai-editor)、[ ターゲットレベルを挿入](experience-target-node-add-inner.md#ai-editor)、または[兄弟ターゲットを追加](experience-target-node-add-sibling.md#ai-editor)。

   * [子ノードとクリエイティブをコピー](experience-target-node-copy.md#ai-editor)または[ ノードを削除](experience-target-node-delete.md#ai-editor)。

1. [ クリエイティブバンドルを最終ノード ](experience-assign-creative-bundles.md#ai-editor)に割り当て、オプションで[ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)と[ トラッキング URL](experience-tracking-urls-targeting.md#ai-editor)を行います。

   エクスペリエンスを公開するには、最終的なノードごとにバンドルを割り当てるか、エクスペリエンスのデフォルトのクリエイティブを使用する必要があります。 保存するときに、未割り当てのノードにデフォルトを割り当てることができます。

1. （オプション）一般的なエクスペリエンス設定を編集します。

   1. 保持するツリーの変更を保存するには、**[!UICONTROL Save]**&#x200B;をクリックします。

   1. **[!UICONTROL Experience Form]**&#x200B;をクリックし、**[!UICONTROL Yes]**&#x200B;をクリックして未保存のツリーの変更を破棄し、フォームを開きます。

   1. [一般的なエクスペリエンス設定](experience-settings-targeting.md)を編集し、**[!UICONTROL Save]**&#x200B;をクリックします。

      AIを活用したエディターが開きます。

1. [ エクスペリエンスを保存](#save)。

## 手動エディターを使用したツリーの設定 {#manual-editor}

1. AI ドリブン型エディターで、**[!UICONTROL Manual Decision Tree]**&#x200B;をクリックし、**[!UICONTROL Yes]**&#x200B;をクリックしてAI ドリブン型エディターを終了します。

   切り替える前に、維持したいAI エディターの変更を保存します。 スイッチを確認すると、保存されていないツリーの変更が破棄されます。

1. （オプション）表示設定を変更します。

   * スライダーを移動して、ズームインまたはズームアウトします。

   * ![縦のツリーとして表示](/help/creative/assets/tree-vertical.png "縦のツリーとして表示")または![水平ツリーとして表示](/help/creative/assets/tree-horizontal.png "水平ツリーとして表示")をクリックして、縦と横のビューを切り替えます。

   ビュー設定は、ログアウトするまで保存されます。

1. 広告ターゲットと対応するクリエイターを設定します。

   * [最終レベルのターゲットを追加](experience-target-node-add-final.md#manual-editor)、[ ノード間にターゲットを挿入](experience-target-node-add-inner.md#manual-editor)または[兄弟ターゲットを追加](experience-target-node-add-sibling.md#manual-editor)。

   * [子ノードとクリエイティブをコピー](experience-target-node-copy.md#manual-editor)または[ ノードを削除](experience-target-node-delete.md#manual-editor)。

   * [ クリエイティブバンドルを割り当て](experience-assign-creative-bundles.md#manual-editor)、オプションで[ クリエイティブの最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)および[ トラッキング URL](experience-tracking-urls-targeting.md#manual-editor)。

1. （オプション）一般的なエクスペリエンス設定を編集するには、**[!UICONTROL Experience Form]**&#x200B;をクリックし、[一般的なエクスペリエンス設定](experience-settings-targeting.md)を編集します。

1. [ エクスペリエンスを保存](#save)。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。

{{$include /help/_includes/experience-save.md}}

## 保存されたエクスペリエンスの広告タグと動画のトランスコーディング

エクスペリエンスがライブになると、[!DNL Creative]は、該当するクリエイティブサイズまたはビデオのデュレーションごとに1つの広告タグを自動的に作成します。 その後、[広告タグを書き出して、DSP](/help/creative/experiences/experience-tag-export.md)に実装できます。

ビデオ広告エクスペリエンスの場合、ビデオのクリエイティブはAdobe Advertising DSPによってVAST 2.0 タグとして自動的にトランスコードされるので、プレビューできます。 オプションで[別のDSP](experience-tag-video-transcoding.md)のトランスコードを任意のビデオ広告エクスペリエンスタグに適用できます。

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
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [ エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
