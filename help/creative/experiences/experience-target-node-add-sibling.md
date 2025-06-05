---
title: エクスペリエンスのノード間に兄弟ターゲットノードを追加します
description: ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードに兄弟ノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: dac7252e118e467fbc924cf162756d7ecd69892f
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# エクスペリエンスのノード間に兄弟ターゲットノードを追加します

*デシジョンツリーのターゲット設定のみを使用したエクスペリエンス*
*クローズドベータ版*

兄弟ノードは、ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードに追加できます。

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. 兄弟ノードを追加するノードの上で、「![ 追加 ](/help/creative/assets/add.png " 追加 ")」をクリックし、「**[!UICONTROL Insert Sibling Target]**」を選択します。

1. ターゲットを指定します。

   * Adobe Audience Target の場合は、次の操作を行います。

      1. 「**[!UICONTROL Click to Browse]**」をクリックして [!UICONTROL Audience Targeting] オプションを開き、「**[!UICONTROL Adobe Segments]**」タブを開き、広告主の [!DNL Adobe] オーディエンスターゲットを 1 つ以上指定して、「**[!UICONTROL Save]**」をクリックします。

      1. （オプション）複数のオーディエンスが指定されている場合に複数のターゲットノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定されたオーディエンスごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定されたすべてのオーディエンスに属している必要があります。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   * 地理的ターゲットの場合は、次の手順を実行します。

      1. [**[!UICONTROL Click to Browse]**] をクリックして [!UICONTROL Geo Targeting] のオプションを開き、1 つ以上の地理的ターゲットを指定して、[**[!UICONTROL Save]**] をクリックします。

         郵便番号ターゲットには一括編集オプションがあります。 複数の郵便番号を貼り付けるには、[**[!UICONTROL Paste postal codes]**] タブをクリックし、国を選択して、郵便番号をコンマまたは行で区切って貼り付けるか入力して、[**[!UICONTROL Include All]**] をクリックします。 含まれている郵便番号のターゲットを削除するには、ターゲットの上にカーソルを置き、「![ 削除 ](/help/creative/assets/delete.png " 削除 ")」 **[!UICONTROL Remove]** タンをクリックします。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   * データ・パス・ターゲットの場合は、オプションでデータ・パス・キーをカスタマイズし、データ・パス値を 1 つ入力し、「**[!UICONTROL Apply]**」をクリックします。

     キーと値のペアのキーのデフォルト値は、[ エクスペリエンス設定 ](experience-settings-targeting.md) の [!UICONTROL Advanced] セクションの **[!UICONTROL Data Pass]** フィールドに既に設定されています。 オプションで、このキーをカスタマイズできます。

   * ピクセルターゲットをリターゲティングするには、使用するリターゲティングピクセルと、クリエイティブを表示するために必要なピクセルの属性に必要な値を選択します。 次に、「**[!UICONTROL Apply]**」をクリックします。

     リターゲティングピクセルの属性は、[ リターゲティングピクセル設定 ](/help/creative/pixels/retargeting-pixel-manage.md) で設定します。

   * デバイス・ターゲットの場合は、次の手順を実行します。

      1. ターゲットを選択します。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります。

      1. 「**[!UICONTROL Apply]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * （任意） [ クリエイティブの割り当て ](experience-assign-creative-bundles.md) を新しいターゲットノードに割り当てます。

   * （オプション）エクスペリエンスを保存するには、次の手順に従います。

      1. 「**[!UICONTROL Save]**」をクリックし、「**[!UICONTROL OK]**」をクリックします。

      1. （最下位レベルの各ノードに 1 つ以上のクリエイティブが含まれていない場合）：次のいずれかの操作をおこないます。

         * 必要なすべてのクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「**[!UICONTROL Save as Draft]**」をクリックします。

           ドラフトエクスペリエンス用の広告タグは作成できません。

         * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

         * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 最終レベルへのターゲットノードの追加 ](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入する ](experience-target-node-add-inner.md)
>* [ 子ノードとクリエイティブを同じレベルの別のノードにコピーする ](experience-target-node-copy.md)
>* [ 最終ノードへのクリエイティブの割り当て ](experience-assign-creative-bundles.md)
>* [ ターゲットノードまたはクリエイティブリーフノードの削除 ](/help/creative/experiences/experience-target-node-delete.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集 ](experience-edit-targeting.md)
>* [ ターゲット設定エクスペリエンス設定 ](experience-settings-targeting.md)
