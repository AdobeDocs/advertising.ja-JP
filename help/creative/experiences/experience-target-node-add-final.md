---
title: エクスペリエンスの最終レベルへのターゲットノードの追加
description: 広告エクスペリエンスの最終ターゲットレベルにターゲットノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 9f93990bcd6b3c8f7d6fb29186da620ac6d4ecf5
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# エクスペリエンスの最終レベルへのターゲットノードの追加

*デシジョンツリーのターゲット設定のみを使用したエクスペリエンス*
*クローズドベータ版*

ターゲットノードをエクスペリエンスの最上位レベル（ルートの「すべて」ノード、ターゲット固有のノード、「その他すべて」ノード）に追加した場合は、ターゲットを直接定義するので、兄弟ノードを作成する必要はありません。 下位レベルのノードを追加すると、同じレベルにターゲットノードと追加の「その他すべて」のノードが作成されます。

>[!NOTE]
>
>決定ツリーの既存のレベル間にターゲットノードを挿入するには、「[ エクスペリエンスのノード間にターゲットノードを挿入 ](experience-target-node-add-inner.md) を参照してください。

<!-- 1. [ways to get to the decision tree] -->

1. ターゲットを挿入するノードの下で、「![ 追加 ](/help/creative/assets/add.png " 追加 ")」をクリックし、「**[!UICONTROL Insert New Target]**」を選択します。

1. ターゲットを指定します。

   * Adobe オーディエンスのターゲットの場合は、「**[!UICONTROL Adobe Audience]**」を選択してから、以下を実行します。

      1. 「**[!UICONTROL Click to Browse]**」をクリックして [!UICONTROL Audience Targeting] オプションを開き、「**[!UICONTROL Adobe Segments]**」タブを開き、広告主の [!DNL Adobe] オーディエンスターゲットを 1 つ以上指定して、「**[!UICONTROL Create]**」をクリックします。

      1. （オプション）複数のオーディエンスが指定されている場合に複数のターゲットノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定されたオーディエンスごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定されたすべてのオーディエンスに属している必要があります。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   * 地理的ターゲットの場合は、単一の地理的カテゴリ（[!UICONTROL Geo: Country] など）を選択し、次の操作を実行します。

      1. [**[!UICONTROL Click to Browse]**] をクリックして [!UICONTROL Geo Targeting] のオプションを開き、1 つ以上の地理的ターゲットを指定して、[**[!UICONTROL Save]**] をクリックします。

         郵便番号ターゲットには一括編集オプションがあります。 複数の郵便番号を貼り付けるには、[**[!UICONTROL Paste postal codes]**] タブをクリックし、国を選択して、郵便番号をコンマまたは行で区切って貼り付けるか入力して、[**[!UICONTROL Include All]**] をクリックします。 含まれている郵便番号のターゲットを削除するには、ターゲットの上にカーソルを置き、「![ 削除 ](/help/creative/assets/delete.png " 削除 ")」 **[!UICONTROL Remove]** タンをクリックします。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   * データ受け渡しターゲットの場合、**[!UICONTROL Data Pass]** を選択し、必要に応じてデータ受け渡しキーをカスタマイズし、データ受け渡し値を 1 つ入力して、「**[!UICONTROL Apply]**」をクリックします。

   キーと値のペアのキーのデフォルト値は、[ エクスペリエンス設定 ](experience-settings-targeting.md) の [!UICONTROL Advanced] セクションの **[!UICONTROL Data Pass]** フィールドに既に設定されています。 オプションで、このキーをカスタマイズできます。

   * リターゲティングピクセルターゲットの場合は、「**[!UICONTROL RT Pixel]**」を選択し、使用するリターゲティングピクセルと、クリエイティブの表示に必要なピクセルの属性の値を 1 つ選択して、「**[!UICONTROL Apply]**」をクリックします。

     リターゲティングピクセルの属性は、[ リターゲティングピクセル設定 ](/help/creative/pixels/retargeting-pixel-manage.md) で設定します。

   * デバイス・ターゲットの場合は、次の手順を実行します。

      1. 単一のターゲット・カテゴリ（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]** または **[!UICONTROL Device: Browser]**）を選択し、ターゲットを選択します。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります。

      1. 「**[!UICONTROL Apply]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * （任意） [ クリエイティブの割り当て ](experience-assign-creative-bundles.md) を新しいターゲットノードと「その他すべて」ノードに割り当てます。

   * （オプション）エクスペリエンスを保存するには、次の手順に従います。

      1. 「**[!UICONTROL Save]**」をクリックし、「**[!UICONTROL OK]**」をクリックします。

      1. （最下位レベルの各ノードに 1 つ以上のクリエイティブが含まれていない場合）：次のいずれかの操作をおこないます。

         * すべての必要なクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「保存」をクリック **[!UICONTROL Save as Draft]** ます。

           ドラフトエクスペリエンス用の広告タグは作成できません。

         * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

         * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ ノード間にターゲットノードを挿入する ](experience-target-node-add-inner.md)
>* [ ノード間に兄弟ターゲットノードを追加する ](experience-target-node-add-sibling.md)
>* [ 子ノードとクリエイティブを同じレベルの別のノードにコピーする ](experience-target-node-copy.md)
>* [ 最終ノードへのクリエイティブの割り当て ](experience-assign-creative-bundles.md)
>* [ ターゲットノードまたはクリエイティブリーフノードの削除 ](/help/creative/experiences/experience-target-node-delete.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集 ](experience-edit-targeting.md)
>* [ ターゲット設定エクスペリエンス設定 ](experience-settings-targeting.md)
