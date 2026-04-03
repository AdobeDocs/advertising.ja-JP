---
title: エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除
description: 広告エクスペリエンスの各ターゲットにクリエイターを割り当てる方法について説明します。
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

クリエイティブバンドルは、エクスペリエンス決定ツリーの最下部レベルのターゲットノードに割り当てることができます。 ターゲットを設定していないエクスペリエンスの場合、一番下のレベルは「すべて」になります。

標準的な広告エクスペリエンスには、標準的なクリエイティブバンドルのみを割り当てることができます。 動的な広告エクスペリエンスの場合は、動的なクリエイティブバンドルのみを割り当てることができます。

>[!NOTE]
>
>最終ノードごとに少なくとも1つのクリエイティブバンドルを割り当てない場合は、[&#x200B; エクスペリエンスを保存](experience-create-targeting.md)するときに、割り当てられていない各ノードにデフォルトのクリエイティブを使用することを選択できます。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終的なノードごとにデフォルトのクリエイターを使用する必要があります。

<!-- 1. [ways to get to the decision tree] -->

1. 次のいずれかの操作を行います。

   * （クリエイティブを含まない最終ノード） ノードの下で、**[!UICONTROL Assign Bundles]**&#x200B;をクリックします。

   * （既存のクリエイティブを持つノード）ターゲットノードの下にあるクリエイティブバンドルボックスにカーソルを合わせ、**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**&#x200B;をクリックします。

1. ターゲットノードに割り当てる各バンドルの横にあるチェックボックスを選択し、割り当てを解除する各バンドルの横にあるチェックボックスをオフにします。

   エクスペリエンス（標準または動的）に関連するバンドルタイプのバンドルのみが一覧表示されます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （オプション） [割り当てられたバンドルのクリエイティブの最適化とスケジュール &#x200B;](experience-optimization-scheduling-targeting.md)をカスタマイズします。

1. （オプション） [割り当てられたバンドル内のクリエイティブのトラッキング URLをカスタマイズ &#x200B;](experience-tracking-urls-targeting.md)。

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [&#x200B; ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)
>* [&#x200B; ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)
>* [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [&#x200B; ターゲット設定](experience-settings-targeting.md)
>* [&#x200B; ライブエクスペリエンスの広告エクスペリエンスタグの書き出しと実装](experience-tag-export.md)
>* [&#x200B; エクスペリエンスの変更ログを表示](/help/creative/experiences/experience-view-change-log.md)
