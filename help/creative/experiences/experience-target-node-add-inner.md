---
title: エクスペリエンス内のノード間にターゲットノードを追加する
description: 広告エクスペリエンスのターゲットボード間にターゲットノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%
---
# エクスペリエンス内のノード間にターゲットノードを追加する

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

既存のレベル間にターゲットノードを挿入すると、新しいターゲットノードは既存のすべての子ターゲットとクリエイティブを保持し、新しいノードは最初に「すべて」と呼ばれます。 オプションとして、特定のターゲットを追加せずに新しいノードを維持できます。

特定のターゲットを定義するには、同じレベルに兄弟ターゲットノードを追加し、新しいターゲットを指定してから、そのターゲットのみにクリエイターを割り当てます。 兄弟ターゲットノードを追加すると、新しいターゲットノードが作成され、以前「すべて」に割り当てられたすべての子ターゲットとクリエイターが、同じレベルの新しい「その他すべて」ノードに移動します。 この方法では、新しいターゲットの追加は、新しいターゲティング情報が新しい兄弟ノードにのみ含まれるため、既存の子ブランチには影響しません。

>[!NOTE]
>
>ターゲットノードを決定ツリーの下位レベルに追加するには、「[ エクスペリエンスの最終レベルにターゲットノードを追加](experience-target-node-add-final.md)」を参照してください。

## AI ドリブン型エディターの使用（Beta） {#ai-editor}

エクスペリエンスを[作成中](experience-create-targeting.md#ai-editor)または[編集中](experience-edit-targeting.md#ai-editor)に、AI エージェントにターゲットレベルの挿入を依頼できます。 挿入する場所と、保持する既存の支店やクリエイターを特定し、その結果を確認します。 レベルをカンバスに直接挿入するには：

1. レベルを挿入する境界で、**[!UICONTROL Add targeting level]**&#x200B;をクリックします。

   水平表示では、このコントロールは同じラベルのアイコンです。

1. **[!UICONTROL New targeting level]**&#x200B;で、対象カテゴリを選択し、**[!UICONTROL Add targeting level]**&#x200B;をクリックします。

   * オーディエンスターゲットの場合は、**[!UICONTROL Audience]**&#x200B;を選択します。

   * 地理的ターゲットの場合は、1つの地理的カテゴリ（**[!UICONTROL Geo: Country]**&#x200B;など）を選択します。

   * データ パス ターゲットの場合は、**[!UICONTROL Data Pass]**&#x200B;を選択します。

   * ピクセルターゲットをリターゲティングするには、**[!UICONTROL RT Pixel]**&#x200B;を選択します。

   * デバイス ターゲットの場合は、単一のターゲット カテゴリ （**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;または&#x200B;**[!UICONTROL Device: Browser]**）を選択します。

   レベルを挿入しても、ターゲット値が表示されません。 新しいレベルでは、最初に「すべて」が使用され、既存の子ターゲットとクリエイターが保持されます。

1. （オプション）新しいレベルで特定のターゲットを定義するには、[兄弟ターゲットノード ](experience-target-node-add-sibling.md#ai-editor)を追加します。 それ以外の場合は、特定のターゲットを追加せずに新しい「すべて」ノードを維持します。

1. （オプション）ユーザー定義のターゲットノードの名前を変更するには、**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**&#x200B;をクリックし、**[!UICONTROL Node Name]**&#x200B;を入力してから&#x200B;**[!UICONTROL Save]**&#x200B;をクリックします。

   「All」または「Everyone Else」ノードの名前は変更できません。

1. 保持されているブランチを確認し、新しい最終ノードにクリエイティブバンドル ](experience-assign-creative-bundles.md#ai-editor)を[割り当てます。

1. [ エクスペリエンスを保存](#save)。

## 手動エディターの使用 {#manual-editor}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. ターゲットを挿入するノードの下で、![追加](/help/creative/assets/add.png "追加")をクリックし、**[!UICONTROL Insert New Target]**&#x200B;を選択します。

1. 次のいずれかの操作を行います。

   * 兄弟ノードがまだ存在しない場合は、次の操作を行います。

     1. ターゲットの種類を選択し、**[!UICONTROL Apply]**&#x200B;をクリックします。

        * オーディエンスターゲットの場合は、**[!UICONTROL Audience]**&#x200B;を選択します。

        * 地理的ターゲットの場合は、1つの地理的カテゴリ（**[!UICONTROL Geo: Country]**&#x200B;など）を選択します。

        * データ パス ターゲットの場合は、**[!UICONTROL Data Pass]**&#x200B;を選択します。

        * ピクセルターゲットをリターゲティングするには、**[!UICONTROL RT Pixel]**&#x200B;を選択します。

        * デバイス ターゲットの場合は、単一のターゲット カテゴリ （**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;または&#x200B;**[!UICONTROL Device: Browser]**）を選択します。

   * 兄弟ノードが既に存在する場合は、次の操作を行います。

     * オーディエンスターゲティングの場合：

       1. 「**[!UICONTROL Click to Browse]**」をクリックして、**[!UICONTROL Audience Targeting]** オプションを開きます。

       1. オーディエンスセグメントとグループを設定します。

          * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

          * 既存のセグメントグループにセグメントを追加するには：

            1. 右側のパネルでセグメントグループをクリックします。

            1. （オプション）必要に応じて、グループロジックを&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;または&#x200B;**[!UICONTROL Exclude All]**&#x200B;に変更します。

               **[!UICONTROL Include Any]**&#x200B;は、選択した1つ以上のセグメントのユーザーと一致します。**[!UICONTROL Include All]**&#x200B;には、選択したすべてのセグメントのメンバーシップが必要です。

               **[!UICONTROL Exclude All]**&#x200B;は、最初のセグメント グループでは使用できません。 除外のみを含むオーディエンスの場合は、**[!UICONTROL Include Any]**&#x200B;を使用してオーディエンスを作成し、DSP内のプレースメントに追加するときに、そのオーディエンスを除外します。

            1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。 追加のセグメントごとに繰り返します。

               セグメントグループは、新しいセグメントで自動的に更新されます。

          * 新しいセグメントグループを追加するには：

            1. 右側のパネルで「**[!UICONTROL + New Group]**」をクリックします。

            1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを&#x200B;**[!UICONTROL And]**&#x200B;または&#x200B;**[!UICONTROL Or]**&#x200B;に変更します。

               **[!UICONTROL And]**&#x200B;では、ユーザーが両方のグループの条件を満たす必要があります。**[!UICONTROL Or]**&#x200B;では、少なくとも1つのグループの条件を満たす必要があります。

            1. 左側のパネルで新しいグループのセグメントを探し、セグメント名の横にあるチェックボックスを選択します。

            1. （オプション）必要に応じて、グループロジックを&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;または&#x200B;**[!UICONTROL Exclude All]**&#x200B;に変更します。

       1. **[!UICONTROL Create]**&#x200B;をクリックします。

       1. **[!UICONTROL Apply]**&#x200B;をクリックします。

     * 地理的目標については、次の操作を行います。

       1. **[!UICONTROL Click to Browse]**&#x200B;をクリックして[!UICONTROL Geo Targeting] オプションを開き、1つ以上の地理的目標を指定してから、**[!UICONTROL Save]**&#x200B;をクリックします。

          郵便番号ターゲットには一括編集オプションがあります。 複数の郵便番号を貼り付けるには、「**[!UICONTROL Paste postal codes]**」タブをクリックし、国を選択して、郵便番号をコンマ区切りまたは別々の行に貼り付けるか入力し、**[!UICONTROL Include All]**&#x200B;をクリックします。 含まれている郵便番号ターゲットを削除するには、ターゲットの上にカーソルを置き、![削除](/help/creative/assets/delete.png "削除") **[!UICONTROL Remove]**&#x200B;をクリックします。

       1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲットノードを作成するには、**[!UICONTROL Split targets to create nodes]**&#x200B;を選択します。

          この機能は、指定された地理的ターゲットごとに（個別のクリエイティブバンドルを含む）個別のターゲットノードを作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所（[!DNL Boolean] `AND` ステートメント）に属している必要があります。

       1. **[!UICONTROL Apply]**&#x200B;をクリックします。

     * データパスターゲットの場合は、オプションでデータパスキーをカスタマイズし、単一のデータパス値を入力して、**[!UICONTROL Apply]**&#x200B;をクリックします。

       デフォルトのデータパスキーは、[一般的なエクスペリエンス設定](experience-settings-targeting.md)の&#x200B;**[!UICONTROL Advanced]** セクションの&#x200B;**[!UICONTROL Data Pass]** フィールドで設定されます。 必要に応じて、ターゲットのキーをカスタマイズします。

     * リターゲティングピクセルターゲットの場合は、使用する1つのリターゲティングピクセルと、クリエイターを表示するために必要なピクセル属性の値を選択し、**[!UICONTROL Apply]**&#x200B;をクリックします。

       使用可能な属性は、[ リターゲティングピクセル設定](/help/creative/pixels/retargeting-pixel-manage.md)で設定されます。

     * デバイスターゲットの場合は、次の操作を行います。

       1. ターゲットを選択します。

       1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲットノードを作成するには、**[!UICONTROL Split targets to create nodes]**&#x200B;を選択します。

          この機能は、指定された地理的ターゲットごとに（個別のクリエイティブバンドルを含む）個別のターゲットノードを作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所（[!DNL Boolean] `AND` ステートメント）に属している必要があります。

       1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲットノードを作成するには、**[!UICONTROL Split targets to create nodes]**&#x200B;を選択します。

       1. **[!UICONTROL Apply]**&#x200B;をクリックします。

1. （オプション）ユーザー定義ブランチのカスタムブランチ名を指定します。

   デフォルトでは、ユーザー定義のブランチには、適用されたターゲットがラベル付けされます。

   「すべて」または「その他の全員」ブランチのカスタムブランチ名を作成することはできません。

   1. ターゲットノードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**&#x200B;をクリックします。

   1. **[!UICONTROL Node Name]**&#x200B;を入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. （オプション） [ クリエイティブバンドル ](experience-assign-creative-bundles.md#manual-editor)を新しいターゲットノードと「その他のすべてのもの」ノードに割り当てます。

1. （オプション） [指定したターゲットタイプの兄弟ターゲットノード ](experience-target-node-add-sibling.md#manual-editor)を追加します。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [ ノード間に兄弟ターゲットノードを追加](experience-target-node-add-sibling.md)
>* [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)
>* [ クリエイティブを最終ノードに割り当て](experience-assign-creative-bundles.md)
>* [ ターゲットノードまたはクリエイティブリーフノードを削除](/help/creative/experiences/experience-target-node-delete.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [ ターゲット設定](experience-settings-targeting.md)
