---
title: エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除
description: 広告エクスペリエンスの各ターゲットにクリエイターを割り当てる方法について説明します。
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: 'https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M'
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
source-wordcount: '453'
ht-degree: 0%
---
# エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

クリエイティブバンドルは、エクスペリエンス決定ツリーの最下部レベルのターゲットノードに割り当てることができます。 ターゲットを設定していないエクスペリエンスの場合、一番下のレベルは「すべて」になります。

標準的な広告エクスペリエンスには、標準的なクリエイティブバンドルのみを割り当てることができます。 動的な広告エクスペリエンスの場合は、動的なクリエイティブバンドルのみを割り当てることができます。

>[!NOTE]
>
>最終ノードごとに少なくとも1つのクリエイティブバンドルを割り当てない場合は、[ エクスペリエンスを保存](experience-create-targeting.md)するときに、割り当てられていない各ノードにデフォルトのクリエイティブを使用することを選択できます。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終的なノードごとにデフォルトのクリエイターを使用する必要があります。

## AI ドリブン型エディターの使用（Beta） {#ai-editor}

エクスペリエンスを[作成中](experience-create-targeting.md#ai-editor)または[編集中](experience-edit-targeting.md#ai-editor)に、キャンバス コントロールを使用します。

1. 次のいずれかの操作を行います。

   * バンドルのない最終ノードの場合は、**[!UICONTROL Assign Bundles]**&#x200B;をクリックします。

   * 既存のバンドルを持つノードの場合は、そのクリエイティブ リーフ ノードで&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

1. 「**[!UICONTROL Assign Bundles]**」タブで、割り当てる各バンドルの横にあるチェックボックスを選択し、割り当てを解除する各バンドルの横にあるチェックボックスをオフにします。

   エクスペリエンスに関連するタイプ（標準または動的）のバンドルのみが一覧表示されます。

1. （オプション）「**[!UICONTROL Creative optimisation]**」タブを開いて、[ ローテーションとスケジュールのカスタマイズ ](experience-optimization-scheduling-targeting.md)を行います。

1. ダイアログで「**[!UICONTROL Save]**」をクリックして、作業ツリーを更新します。

1. （オプション） [ トラッキング URLをカスタマイズ ](experience-tracking-urls-targeting.md#ai-editor)。

1. [変更を保持するために、ツリーヘッダーからエクスペリエンス ](#save)を保存します。

## 手動エディターの使用 {#manual-editor}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. 次のいずれかの操作を行います。

   * （クリエイティブを含まない最終ノード） ノードの下で、**[!UICONTROL Assign Bundles]**&#x200B;をクリックします。

   * （既存のクリエイティブを持つノード）ターゲットノードの下にあるクリエイティブバンドルボックスにカーソルを合わせ、**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

1. ターゲットノードに割り当てる各バンドルの横にあるチェックボックスを選択し、割り当てを解除する各バンドルの横にあるチェックボックスをオフにします。

   エクスペリエンス（標準または動的）に関連するバンドルタイプのバンドルのみが一覧表示されます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （オプション） [割り当てられたバンドルのクリエイティブの最適化とスケジュール ](experience-optimization-scheduling-targeting.md)をカスタマイズします。

1. （オプション） [割り当てられたバンドル内のクリエイティブのトラッキング URLをカスタマイズ ](experience-tracking-urls-targeting.md)。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。 バンドルダイアログを単独で保存しても、エクスペリエンスは保存または公開されません。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)
>* [ ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)
>* [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [ ターゲット設定](experience-settings-targeting.md)
>* [ ライブエクスペリエンスの広告エクスペリエンスタグの書き出しと実装](experience-tag-export.md)
>* [ エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
