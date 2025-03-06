---
title: エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除
description: 広告エクスペリエンスの各ターゲットにクリエイティブを割り当てる方法を説明します。
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: 115b769c2880936c422747b44f43b4be7281916d
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除

*デシジョンツリーのターゲット設定のみを使用したエクスペリエンス*
*クローズドベータ版*

エクスペリエンスの決定ツリーの一番下のレベルにあるターゲットノードに、クリエイティブバンドルを割り当てることができます。 ターゲットを設定していないエクスペリエンスの場合、一番下のレベルは「すべて」の下になります。

標準の広告エクスペリエンスの場合、割り当てることができるのは標準のクリエイティブバンドルのみです。 動的な広告エクスペリエンスの場合は、動的なクリエイティブバンドルのみを割り当てることができます。

>[!NOTE]
>
>各最終ノードに 1 つ以上のクリエイティブバンドルを割り当てない場合、（エクスペリエンスを保存 [ する際に、未割り当ての各ノードに対してデフォルトのクリエイティブを使用することを選択でき ](experience-create-targeting.md) す。 エクスペリエンスを公開するには、バンドルを割り当てるか、最終ノードごとにデフォルトのクリエイティブを使用する必要があります。

<!-- 1. [ways to get to the decision tree] -->

1. 次のいずれかの操作を行います。

   * （クリエイティブのない最終ノード） ノードの下の ![ 追加 ](/help/creative/assets/add.png " 追加 ") をクリックし、**[!UICONTROL Assign Bundles]** を選択します。

   * （既存のクリエイティブを持つノード）ターゲットノードの下にあるクリエイティブバンドルボックスの上にカーソルを置き <!-- wording???? -->**[!UICONTROL ...]**/**[!UICONTROL Edit Bundles]** をクリックします。

1. ターゲットノードに割り当てる各バンドルの横にあるチェックボックスをオンにし、割り当てを解除する各バンドルの横にあるチェックボックスの選択を解除します。

   関連するエクスペリエンスのバンドルタイプ（標準または動的）のバンドルのみが表示されます。

1. 「**[!UICONTROL Attach to Bundles]**」をクリックします。

1. （任意） [ 割り当てられたバンドル内のクリエイティブのトラッキング URL をカスタマイズ ](experience-tracking-urls-targeting.md) できます。

1. （オプション） [ 割り当てられたバンドルのクリエイティブの最適化とスケジュール設定をカスタマイズ ](experience-optimization-scheduling-targeting.md)。

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [ 最終レベルへのターゲットノードの追加 ](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入する ](experience-target-node-add-inner.md)
>* [ ノード間に兄弟ターゲットノードを追加する ](experience-target-node-add-sibling.md)
>* [ 子ノードとクリエイティブを同じレベルの別のノードにコピーする ](experience-target-node-copy.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集 ](experience-edit-targeting.md)
>* [ ターゲット設定エクスペリエンス設定 ](experience-settings-targeting.md)
>* [ ライブエクスペリエンス用の広告エクスペリエンスタグのエクスポートと実装 ](experience-tag-export.md)
