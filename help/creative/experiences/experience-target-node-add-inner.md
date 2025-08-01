---
title: エクスペリエンスのノード間にターゲットノードを追加する
description: 広告エクスペリエンスのターゲットノード間にターゲットノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
source-git-commit: 81cbb3cdac21f4b4899b0c07d1eb0686b7b3c7d4
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# エクスペリエンスのノード間にターゲットノードを追加する

*デシジョンツリーのターゲット設定のみを使用したエクスペリエンス*
*クローズドベータ版*

既存のレベルの間にターゲット ノードを挿入すると、新しいターゲット ノードは既存のすべての子ターゲットとクリエイティブを保持し、新しいノードは最初に「すべて」と呼ばれます。 オプションで、特定のターゲットを追加せずに新しいノードを保持できます。

特定のターゲットを定義するには、同じレベルに兄弟ターゲットノードを追加し、新しいターゲットを指定してから、そのターゲットのみにクリエイティブを割り当てます。 兄弟ターゲットノードを追加すると、新しいターゲットノードが作成され、以前「すべて」に割り当てられたすべての子ターゲットとクリエイティブが、同じレベルの新しい「その他」ノードに移動します。 これにより、新しい兄弟ノードには新しいターゲット設定情報のみが含まれるので、新しいターゲットを追加しても既存の子ブランチには影響しません。

>[!NOTE]
>
>ターゲットノードを決定ツリーの下位レベルに追加するには、「[ エクスペリエンスの最終レベルにターゲットノードを追加する ](experience-target-node-add-final.md) を参照してください。

<!-- 1. [ways to get to the decision tree] -->

1. ターゲットを挿入するノードの下で、「![ 追加 ](/help/creative/assets/add.png " 追加 ")」をクリックし、「**[!UICONTROL Insert New Target]**」を選択します。

1. 次のいずれかの操作を行います。

   * 兄弟ノードが存在しない場合は、次の操作を行います。

      1. ターゲットの種類を選択し、[**[!UICONTROL Apply]**] をクリックします。

         * Adobe オーディエンスターゲットの場合は、「**[!UICONTROL Adobe Audience]**」を選択します。

         * 地理的ターゲットの場合は、単一の地理的カテゴリ（[!UICONTROL Geo: Country] など）を選択します。

         * データ・パス・ターゲットの場合は、「**[!UICONTROL Data Pass]**」を選択します。

         * ピクセルターゲットをリターゲティングする場合は、「**[!UICONTROL RT Pixel]」を選択します。

         * デバイス・ターゲットの場合は、単一のターゲット・カテゴリ（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**、**[!UICONTROL Device: Browser]**）を選択します。

   * 兄弟ノードが既に存在する場合は、次の操作を行います。

      * Adobe Audience Target の場合は、次の操作を行います。

         1. 「**[!UICONTROL Click to Browse]**」をクリックして [!UICONTROL Audience Targeting] オプションを開き、「**[!UICONTROL Adobe Segments]**」タブを開き、広告主の [!DNL Adobe] オーディエンスターゲットを 1 つ以上指定して、「**[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->」をクリックします。

         1. （オプション）複数のオーディエンスが指定されている場合に複数のターゲットノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

            この機能は、指定されたオーディエンスごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定されたすべてのオーディエンス（[!DNL Boolean] `AND` ステートメント）に属している必要があります。

         1. 「**[!UICONTROL Apply]**」をクリックします。

      * 地理的ターゲットの場合は、次の手順を実行します。

         1. [**[!UICONTROL Click to Browse]**] をクリックして [!UICONTROL Geo Targeting] のオプションを開き、1 つ以上の地理的ターゲットを指定して、[**[!UICONTROL Save]**] をクリックします。

            郵便番号ターゲットには一括編集オプションがあります。 複数の郵便番号を貼り付けるには、[**[!UICONTROL Paste postal codes]**] タブをクリックし、国を選択して、郵便番号をコンマまたは行で区切って貼り付けるか入力して、[**[!UICONTROL Include All]**] をクリックします。 含まれている郵便番号のターゲットを削除するには、ターゲットの上にカーソルを置き、「![ 削除 ](/help/creative/assets/delete.png " 削除 ")」 **[!UICONTROL Remove]** タンをクリックします。

         1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

            この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります（[!DNL Boolean] `AND` ステートメント）。

         1. 「**[!UICONTROL Apply]**」をクリックします。

      * データ受け渡しターゲットの場合、必要に応じてデータ受け渡しキーをカスタマイズし、データ受け渡し値を 1 つ入力し、「**[!UICONTROL Apply]**」をクリックします。

        キーと値のペアのキーのデフォルト値は、[ エクスペリエンス設定 ](experience-settings-targeting.md) の [!UICONTROL Advanced] セクションの **[!UICONTROL Data Pass]** フィールドに既に設定されています。 オプションで、このキーをカスタマイズできます。

      * リターゲティングピクセルターゲットの場合は、使用するリターゲティングピクセルを 1 つ選択し、クリエイティブの表示に必要なピクセルの属性の値を選択して、「**[!UICONTROL Apply]**」をクリックします。

        リターゲティングピクセルの属性は、[ リターゲティングピクセル設定 ](/help/creative/pixels/retargeting-pixel-manage.md) で設定します。

      * デバイス・ターゲットの場合は、次の手順を実行します。

         1. ターゲットを選択します。

         1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

            この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります（[!DNL Boolean] `AND` ステートメント）。

         1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         1. 「**[!UICONTROL Apply]**」をクリックします。

1. （オプション）ユーザー定義ブランチのカスタムブランチ名を指定します。

   デフォルトでは、ユーザー定義のブランチには、適用されたターゲットのラベルが付けられます。

   「All」または「Everyone Else」ブランチにカスタムのブランチ名を作成することはできません。

   1. ターゲットノードの上にカーソルを置き、**[!UICONTROL ...]**/**[!UICONTROL Edit Name]** をクリックします。

   1. **[!UICONTROL Node Name]** を入力し、[**[!UICONTROL Save]**] をクリックします。

1. 次のいずれかの操作をおこないます。

   * （任意） [ クリエイティブの割り当て ](experience-assign-creative-bundles.md) を新しいターゲットノードと「その他すべて」ノードに割り当てます。

   * （任意）指定したターゲットタイプの [ 兄弟ターゲットノードを追加 ](experience-target-node-add-sibling.md) します。

   * （オプション）エクスペリエンスを保存するには、次の手順に従います。

      1. 「**[!UICONTROL Save]**」をクリックし、「**[!UICONTROL OK]**」をクリックします。

      1. （最下位レベルの各ノードに 1 つ以上のクリエイティブが含まれていない場合）：次のいずれかの操作をおこないます。

         * すべての必要なクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「保存」をクリック **[!UICONTROL Save as Draft]** ます。

           ドラフトエクスペリエンス用の広告タグは作成できません。

         * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

         * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 最終レベルへのターゲットノードの追加 ](experience-target-node-add-final.md)
>* [ ノード間に兄弟ターゲットノードを追加する ](experience-target-node-add-sibling.md)
>* [ 子ノードとクリエイティブを同じレベルの別のノードにコピーする ](experience-target-node-copy.md)
>* [ 最終ノードへのクリエイティブの割り当て ](experience-assign-creative-bundles.md)
>* [ ターゲットノードまたはクリエイティブリーフノードの削除 ](/help/creative/experiences/experience-target-node-delete.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集 ](experience-edit-targeting.md)
>* [ ターゲット設定エクスペリエンス設定 ](experience-settings-targeting.md)
