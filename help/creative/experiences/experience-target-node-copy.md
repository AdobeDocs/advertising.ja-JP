---
title: 子ノードを同じレベルの別のターゲットノードにコピーする
description: 親ターゲットノードのすべての子ノードを同じレベルの別のターゲットノードにコピーする方法について説明します
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 286
ht-degree: 0%

---

# 子ノードを同じレベルの別のターゲットノードにコピーする

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

親ターゲットノードのすべての子ノード（すべての子ターゲットとそれらに割り当てられたクリエイティブバンドルを含む）を、同じレベルの別のターゲットノードにコピーできます。 a）コピーしたノードを既存のフレームワークに追加するか、b）既存のフレームワークを完全に置き換えることで、ノードをコピーできます。<!-- Give the main use case or an example to explain. -->

この機能は、親ノードに指定されたターゲットには影響しません。子ノードにのみ影響します。

<!-- 1. [ways to get to the decision tree] -->

1. コピーする子を持つ親ノードをクリックし、![追加](/help/creative/assets/add.png "追加")をクリックしてから、a\）選択&#x200B;**[!UICONTROL Copy Children ctrl+c]**&#x200B;またはb\）キーボードで&#x200B;**[!UICONTROL Ctrl+C]** （[!DNL Microsoft Windows]）または&#x200B;**[!UICONTROL Command-C]** （[!DNL Apple Macintosh]）と入力します。

1. 次のいずれかの操作を行います。

   * ノードのすべての子ノードとクリエイターを置き換えるには、コピーした情報を貼り付けるノードをクリックし、**...**&#x200B;をクリックしてから、**[!UICONTROL Replace ctrl+shift+v]**&#x200B;またはb\）を選択し、キーボードに&#x200B;**[!UICONTROL Ctrl+Shift+V]** （[!DNL Microsoft Windows]）または&#x200B;**[!UICONTROL Command-Shift-V]** （[!DNL Apple Macintosh]）と入力します。

   * （複数の子ターゲットを持つノード、すべての「すべての」ノードなし、およびクリエイターのみ）既存のノードを削除せずに、すべての子ノードとクリエイターをノードに追加するには、コピーした情報を貼り付けるノードをクリックし、**...**&#x200B;をクリックし、a\）を選択します。**[!UICONTROL Add ctrl+v]** **またはb\）キーボードで&#x200B;**&#x200B;[!UICONTROL Ctrl+V] **&#x200B; （[!DNL Microsoft Windows]）または&#x200B;**&#x200B;[!UICONTROL Command-V]**）と入力します。[!DNL Apple Macintosh]

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
>* [&#x200B; クリエイティブを最終ノードに割り当て](experience-assign-creative-bundles.md)
>* [&#x200B; ターゲットノードまたはクリエイティブリーフノードを削除](/help/creative/experiences/experience-target-node-delete.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [&#x200B; ターゲット設定](experience-settings-targeting.md)
