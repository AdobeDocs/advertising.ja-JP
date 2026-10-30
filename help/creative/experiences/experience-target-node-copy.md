---
title: 子ノードを同じレベルの別のターゲットノードにコピーする
description: 親ターゲットノードのすべての子ノードを同じレベルの別のターゲットノードにコピーする方法について説明します
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: 'https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%
---
# 子ノードを同じレベルの別のターゲットノードにコピーする

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

親ターゲットノードのすべての子ノード（すべての子ターゲットとそれらに割り当てられたクリエイティブバンドルを含む）を、同じレベルの別のターゲットノードにコピーできます。 a）コピーしたノードを既存のフレームワークに追加するか、b）既存のフレームワークを完全に置き換えることで、ノードをコピーできます。<!-- Give the main use case or an example to explain. -->

この機能は、親ノードに指定されたターゲットには影響しません。子ノードにのみ影響します。

## AI ドリブン型エディターの使用（Beta） {#ai-editor}

エクスペリエンスを[作成中](experience-create-targeting.md#ai-editor)または[編集中](experience-edit-targeting.md#ai-editor)に、キャンバス コントロールを使用します。

1. コピーする子を持つ親ノードで、**[!UICONTROL ...]** > **[!UICONTROL Copy Children]**&#x200B;をクリックします。

1. 同じレベルの宛先ノードで、**[!UICONTROL ...]**&#x200B;をクリックし、次のいずれかを選択します。

   * 既存の子を削除せずに、コピーされた子ターゲットとクリエイティブを追加するには、**[!UICONTROL Add]**&#x200B;をクリックします。

   * 既存の子ターゲットとクリエイティブをコピーされた子に置き換えるには、**[!UICONTROL Replace]**&#x200B;をクリックします。

   ツリー構造がサポートしていない場合、アクションは無効になります。 続行する前に警告を確認してください。

1. 宛先ブランチを確認し、[ エクスペリエンスを保存](#save)します。

## 手動エディターの使用 {#manual-editor}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. コピーする子を持つ親ノードをクリックし、![追加](/help/creative/assets/add.png "追加")をクリックしてから、a\）選択&#x200B;**[!UICONTROL Copy Children ctrl+c]**&#x200B;またはb\）キーボードで&#x200B;**[!UICONTROL Ctrl+C]** （[!DNL Microsoft Windows]）または&#x200B;**[!UICONTROL Command-C]** （[!DNL Apple Macintosh]）と入力します。

1. 次のいずれかの操作を行います。

   * ノードのすべての子ノードとクリエイターを置き換えるには、コピーした情報を貼り付けるノードをクリックし、**[!UICONTROL ...]**&#x200B;をクリックして、**[!UICONTROL Replace ctrl+shift+v]**&#x200B;を選択するかb\）を選択します。キーボードに&#x200B;**[!UICONTROL Ctrl+Shift+V]** （[!DNL Microsoft Windows]）または&#x200B;**[!UICONTROL Command-Shift-V]** （[!DNL Apple Macintosh]）と入力します。

   * （複数の子ターゲットを持つノード、すべての「すべての」ノードなし、およびクリエイターのみ）既存のノードを削除せずに、すべての子ノードとクリエイターをノードに追加するには、コピーした情報を貼り付けるノードをクリックし、**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Add ctrl+v]**&#x200B;またはb\）を選択します。キーボードで&#x200B;**[!UICONTROL Ctrl+V]** （[!DNL Microsoft Windows]）または&#x200B;**[!UICONTROL Command-V]** （[!DNL Apple Macintosh]）と入力します。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)
>* [ ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)
>* [ クリエイティブを最終ノードに割り当て](experience-assign-creative-bundles.md)
>* [ ターゲットノードまたはクリエイティブリーフノードを削除](/help/creative/experiences/experience-target-node-delete.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [ ターゲット設定](experience-settings-targeting.md)
