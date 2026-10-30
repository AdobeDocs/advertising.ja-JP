---
title: エクスペリエンス内のノード間に兄弟ターゲットノードを追加する
description: ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードに兄弟ノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
TQID: 'https://experienceleague.adobe.com/fRdbFmlTUBzHHkmrfonZ0COJ7-1x6t2HRczwlcVb99o'
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
source-wordcount: '1151'
ht-degree: 0%
---
# エクスペリエンス内のノード間に兄弟ターゲットノードを追加する

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードには、兄弟ノードを追加できます。

## AI ドリブン型エディターの使用（Beta） {#ai-editor}

エクスペリエンスを[作成](experience-create-targeting.md#ai-editor)または[編集](experience-edit-targeting.md#ai-editor)している間に、新しい兄弟ターゲットをAI エージェントに記述できます。 親ブランチとターゲット値を特定し、結果を確認します。 キャンバスに兄弟を直接追加するには：

1. 別の兄弟が必要なレベルのノードの親の上にカーソルを置き、**[!UICONTROL +]**&#x200B;をクリックします。

   ターゲットカテゴリは既存のレベルによって決定され、そのカテゴリの値セレクターが開きます。

1. カテゴリの目標値を指定します。

   * オーディエンスターゲティングの場合：

     * 最初のセグメントを追加するには、オーディエンスセグメントを見つけて選択します。

     * 既存のセグメントグループにセグメントを追加するには：

       1. セグメントグループを選択します。

       1. （オプション）必要に応じて、グループロジックを&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;または&#x200B;**[!UICONTROL Exclude All]**&#x200B;に変更します。

          **[!UICONTROL Include Any]**&#x200B;は、選択した1つ以上のセグメントのユーザーと一致します。**[!UICONTROL Include All]**&#x200B;には、選択したすべてのセグメントのメンバーシップが必要です。

          **[!UICONTROL Exclude All]**&#x200B;は、最初のセグメント グループでは使用できません。 除外のみを含むオーディエンスの場合は、**[!UICONTROL Include Any]**&#x200B;を使用してオーディエンスを作成し、DSP内のプレースメントに追加するときに、そのオーディエンスを除外します。

       1. 追加のセグメントを探して選択します。

     * 新しいセグメントグループを追加するには：

       1. グループを追加します。

       1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを&#x200B;**[!UICONTROL And]**&#x200B;または&#x200B;**[!UICONTROL Or]**&#x200B;に変更します。

          **[!UICONTROL And]**&#x200B;では、ユーザーが両方のグループの条件を満たす必要があります。**[!UICONTROL Or]**&#x200B;では、少なくとも1つのグループの条件を満たす必要があります。

       1. 新しいグループのセグメントを見つけて選択します。

       1. （オプション）必要に応じて、グループロジックを&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;または&#x200B;**[!UICONTROL Exclude All]**&#x200B;に変更します。

   * 地理的な目標：

     * 国、地域、都市など、既存レベルの地理的カテゴリ内の場所を選択します。

     * 郵便番号ターゲットの場合は、国を選択し、含める郵便番号を入力します。 複数の郵便番号を一括入力するには、それらをコンマで区切るか、各コードを別々の行に置きます。

   * データパスターゲットの場合は、一致するキーと値を入力します。

     デフォルトのデータパスキーは、[一般的なエクスペリエンス設定](experience-settings-targeting.md)の&#x200B;**[!UICONTROL Advanced]** セクションの&#x200B;**[!UICONTROL Data Pass]** フィールドで設定されます。 必要に応じて、ターゲットのキーをカスタマイズします。

   * リターゲティングピクセルターゲットの場合は、リターゲティングピクセルを選択し、クリエイターの表示に必要なピクセル属性の値を指定します。

     使用可能な属性は、[ リターゲティングピクセル設定](/help/creative/pixels/retargeting-pixel-manage.md)で設定されます。

   * デバイスターゲットの場合は、デバイスタイプ、オペレーティングシステム、ブラウザーなど、既存のレベルでデバイスカテゴリ内の値を選択します。

1. （使用可能な場合、オプション） **[!UICONTROL Split Nodes]**&#x200B;を選択して、選択した値ごとに個別のターゲットノードを作成し、独自のクリエイティブバンドルの割り当てを行います。 それ以外の場合、選択した値は1つのターゲットノードにグループ化されます。

1. **[!UICONTROL Add Node]**&#x200B;をクリックします。

1. （オプション）新しいノードの名前を変更するには、**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**&#x200B;をクリックし、**[!UICONTROL Node Name]**&#x200B;を入力して、**[!UICONTROL Save]**&#x200B;をクリックします。

1. [新しいノードが最終ノードの場合はクリエイティブバンドル ](experience-assign-creative-bundles.md#ai-editor)を割り当て、次に[ エクスペリエンスを保存](#save)します。

## 手動エディターの使用 {#manual-editor}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. 兄弟ノードを追加するノードの上で、![追加](/help/creative/assets/add.png "追加")をクリックし、**[!UICONTROL Insert Sibling Target]**&#x200B;を選択します。

1. カテゴリの目標値を指定します。

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

   * リターゲティングピクセルターゲットの場合は、使用するリターゲティングピクセルと、クリエイターを表示するために存在する必要があるピクセルの属性の必要な値を選択します。 次に、**[!UICONTROL Apply]**&#x200B;をクリックします。

     使用可能な属性は、[ リターゲティングピクセル設定](/help/creative/pixels/retargeting-pixel-manage.md)で設定されます。

   * デバイスターゲットの場合は、次の操作を行います。

     1. ターゲットを選択します。

     1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲットノードを作成するには、**[!UICONTROL Split targets to create nodes]**&#x200B;を選択します。

        この機能は、指定された地理的ターゲットごとに（個別のクリエイティブバンドルを含む）個別のターゲットノードを作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所（[!DNL Boolean] `AND` ステートメント）に属している必要があります。

     1. **[!UICONTROL Apply]**&#x200B;をクリックします。

1. （オプション）ユーザー定義ブランチのカスタムブランチ名を指定します。

   デフォルトでは、ユーザー定義のブランチには、適用されたターゲットがラベル付けされます。

   「すべて」または「その他の全員」ブランチのカスタムブランチ名を作成することはできません。

   1. ターゲットノードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**&#x200B;をクリックします。

   1. **[!UICONTROL Node Name]**&#x200B;を入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. （オプション） [ クリエイティブバンドル ](experience-assign-creative-bundles.md#manual-editor)を新しいターゲットノードに割り当てます。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [最終レベルにターゲットノードを追加](experience-target-node-add-final.md)
>* [ ノード間にターゲットノードを挿入](experience-target-node-add-inner.md)
>* [子ノードとクリエイターを同じレベルの別のノードにコピー](experience-target-node-copy.md)
>* [ クリエイティブを最終ノードに割り当て](experience-assign-creative-bundles.md)
>* [ ターゲットノードまたはクリエイティブリーフノードを削除](/help/creative/experiences/experience-target-node-delete.md)
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングでエクスペリエンスを編集](experience-edit-targeting.md)
>* [ ターゲット設定](experience-settings-targeting.md)
