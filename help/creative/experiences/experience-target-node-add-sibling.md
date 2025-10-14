---
title: エクスペリエンスのノード間に兄弟ターゲットノードを追加します
description: ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードに兄弟ノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# エクスペリエンスのノード間に兄弟ターゲットノードを追加します

*デシジョンツリーのターゲット設定のみを使用したエクスペリエンス*

兄弟ノードは、ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードに追加できます。

<!-- 1. Open the decision tree:

In a new experience

In an existing experience,
 -->

1. 兄弟ノードを追加するノードの上で、「![&#x200B; 追加 &#x200B;](/help/creative/assets/add.png " 追加 ")」をクリックし、「**[!UICONTROL Insert Sibling Target]**」を選択します。

1. ターゲットを指定します。

   * オーディエンスターゲットの場合は、次の手順を実行します。

      1. **[!UICONTROL Click to Browse]** をクリックして [!UICONTROL Audience Targeting] のオプションを開き、次の操作を行います。

         * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

         * 既存のセグメントグループにセグメントを追加するには：

            1. 右側のパネルでセグメントグループをクリックします。

            1. （オプション）必要に応じて、グループロジックを *[!UICONTROL Include Any]*、*[!UICONTROL Include All]* または *[!UICONTROL Exclude All]* に変更します。

               最初のセグメントグループには *[!UICONTROL Exclude All]* は使用できません。 除外のみを含むオーディエンスの場合、このオーディエンスを *[!UICONTROL Include Any]* として作成し、DSP内のプレースメントに追加するときにそのオーディエンスを除外します。

            1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

               セグメントグループは、新しいセグメントで自動的に更新されます。

         * 新しいセグメントグループを追加するには：

         1. 右側のパネルで「**[!UICONTROL + New Group]**」をクリックします。

         1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを *[!UICONTROL And]* または *[!UICONTROL Or]* に変更します。

         1. 左側のパネルで新しいグループのセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

         1. （オプション）必要に応じて、グループロジックを *[!UICONTROL Include Any]*、*[!UICONTROL Include All]* または *[!UICONTROL Exclude All]* に変更します。

      1. 「**[!UICONTROL Create]**」をクリックします。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   * 地理的ターゲットの場合は、次の手順を実行します。

      1. [**[!UICONTROL Click to Browse]**] をクリックして [!UICONTROL Geo Targeting] のオプションを開き、1 つ以上の地理的ターゲットを指定して、[**[!UICONTROL Save]**] をクリックします。

         郵便番号ターゲットには一括編集オプションがあります。 複数の郵便番号を貼り付けるには、[**[!UICONTROL Paste postal codes]**] タブをクリックし、国を選択して、郵便番号をコンマまたは行で区切って貼り付けるか入力して、[**[!UICONTROL Include All]**] をクリックします。 含まれている郵便番号のターゲットを削除するには、ターゲットの上にカーソルを置き、「![&#x200B; 削除 &#x200B;](/help/creative/assets/delete.png " 削除 ")」 **[!UICONTROL Remove]** タンをクリックします。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります（[!DNL Boolean] `AND` ステートメント）。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   * データ・パス・ターゲットの場合は、オプションでデータ・パス・キーをカスタマイズし、データ・パス値を 1 つ入力し、「**[!UICONTROL Apply]**」をクリックします。

     キーと値のペアのキーのデフォルト値は、**[!UICONTROL Data Pass]** エクスペリエンス設定 [!UICONTROL Advanced] の [&#x200B; セクションの &#x200B;](experience-settings-targeting.md) フィールドに既に設定されています。 オプションで、このキーをカスタマイズできます。

   * ピクセルターゲットをリターゲティングするには、使用するリターゲティングピクセルと、クリエイティブを表示するために必要なピクセルの属性に必要な値を選択します。 次に、「**[!UICONTROL Apply]**」をクリックします。

     リターゲティングピクセルの属性は、[&#x200B; リターゲティングピクセル設定 &#x200B;](/help/creative/pixels/retargeting-pixel-manage.md) で設定します。

   * デバイス・ターゲットの場合は、次の手順を実行します。

      1. ターゲットを選択します。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲット・ノードを作成するには、「**[!UICONTROL Split targets to create nodes]**」を選択します。

         この機能は、指定された地理的ターゲットごとに個別のターゲットノード（個別のクリエイティブバンドルを含む）を作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所に属している必要があります（[!DNL Boolean] `AND` ステートメント）。

      1. 「**[!UICONTROL Apply]**」をクリックします。

1. （オプション）ユーザー定義ブランチのカスタムブランチ名を指定します。

   デフォルトでは、ユーザー定義のブランチには、適用されたターゲットのラベルが付けられます。

   「All」または「Everyone Else」ブランチにカスタムのブランチ名を作成することはできません。

   1. ターゲットノードの上にカーソルを置き、**[!UICONTROL ...]**/**[!UICONTROL Edit Name]** をクリックします。

   1. **[!UICONTROL Node Name]** を入力し、[**[!UICONTROL Save]**] をクリックします。

1. 次のいずれかの操作をおこないます。

   * （任意） [&#x200B; クリエイティブの割り当て &#x200B;](experience-assign-creative-bundles.md) を新しいターゲットノードに割り当てます。

   * （オプション）エクスペリエンスを保存するには、次の手順に従います。

      1. 「**[!UICONTROL Save]**」をクリックし、「**[!UICONTROL OK]**」をクリックします。

      1. （最下位レベルの各ノードに 1 つ以上のクリエイティブが含まれていない場合）：次のいずれかの操作をおこないます。

         * 必要なすべてのクリエイティブバンドルを含めずにエクスペリエンスを保存するには、「**[!UICONTROL Save as Draft]**」をクリックします。

           ドラフトエクスペリエンス用の広告タグは作成できません。

         * クリエイティブバンドルをまだ割り当てていない各ターゲットにデフォルトのクリエイティブを割り当てるには、「割り当 **[!UICONTROL Assign Default Creatives]**」をクリックします。 デフォルトのクリエイティブが割り当てられた、更新されたツリーを確認したら、「**[!UICONTROL Save]**」をクリックして **[!UICONTROL OK]** をクリックします。

         * デシジョンツリーの編集を続行するには、「**[!UICONTROL Continue Edit]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; 最終レベルへのターゲットノードの追加 &#x200B;](experience-target-node-add-final.md)
>* [&#x200B; ノード間にターゲットノードを挿入する &#x200B;](experience-target-node-add-inner.md)
>* [&#x200B; 子ノードとクリエイティブを同じレベルの別のノードにコピーする &#x200B;](experience-target-node-copy.md)
>* [&#x200B; 最終ノードへのクリエイティブの割り当て &#x200B;](experience-assign-creative-bundles.md)
>* [&#x200B; ターゲットノードまたはクリエイティブリーフノードの削除 &#x200B;](/help/creative/experiences/experience-target-node-delete.md)
>* [&#x200B; デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 &#x200B;](experience-create-targeting.md)
>* [&#x200B; デシジョンツリーのターゲット設定を使用したエクスペリエンスの編集 &#x200B;](experience-edit-targeting.md)
>* [&#x200B; ターゲット設定エクスペリエンス設定 &#x200B;](experience-settings-targeting.md)
