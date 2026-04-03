---
title: エクスペリエンス内のノード間に兄弟ターゲットノードを追加する
description: ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードに兄弟ノードを追加する方法を説明します。
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
TQID: https://experienceleague.adobe.com/fRdbFmlTUBzHHkmrfonZ0COJ7-1x6t2HRczwlcVb99o
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 755
ht-degree: 0%

---

# エクスペリエンス内のノード間に兄弟ターゲットノードを追加する

*デシジョンツリーのターゲティングのみ*&#x200B;のエクスペリエンス

ターゲットを持つノード、またはターゲットを持つノードと同じレベルにあるノードには、兄弟ノードを追加できます。

<!--
 1. Open the decision tree:

In a new experience

In an existing experience,
 -->

1. 兄弟ノードを追加するノードの上で、![追加](/help/creative/assets/add.png "追加")をクリックし、**[!UICONTROL Insert Sibling Target]**&#x200B;を選択します。

1. ターゲットを指定します。

   * オーディエンスターゲティングの場合は、次の操作を行います。

      1. 「**[!UICONTROL Click to Browse]**」をクリックして[!UICONTROL Audience Targeting] オプションを開き、次の操作を行います。

         * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

         * 既存のセグメントグループにセグメントを追加するには：

            1. 右側のパネルでセグメントグループをクリックします。

            1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

               *[!UICONTROL Exclude All]*&#x200B;は、最初のセグメント グループでは使用できません。 除外のみを含むオーディエンスの場合は、このオーディエンスを&#x200B;*[!UICONTROL Include Any]*&#x200B;として構築し、DSP内のプレースメントに追加するときに、そのオーディエンスを除外します。

            1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

               セグメントグループは、新しいセグメントで自動的に更新されます。

         * 新しいセグメントグループを追加するには：

         1. 右側のパネルで「**[!UICONTROL + New Group]**」をクリックします。

         1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを&#x200B;*[!UICONTROL And]*&#x200B;または&#x200B;*[!UICONTROL Or]*&#x200B;に変更します。

         1. 左側のパネルで新しいグループのセグメントを探し、セグメント名の横にあるチェックボックスを選択します。

         1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

      1. **[!UICONTROL Create]**&#x200B;をクリックします。

      1. **[!UICONTROL Apply]**&#x200B;をクリックします。

   * 地理的目標については、次の操作を行います。

      1. **[!UICONTROL Click to Browse]**&#x200B;をクリックして[!UICONTROL Geo Targeting] オプションを開き、1つ以上の地理的目標を指定してから、**[!UICONTROL Save]**&#x200B;をクリックします。

         郵便番号ターゲットには一括編集オプションがあります。 複数の郵便番号を貼り付けるには、「**[!UICONTROL Paste postal codes]**」タブをクリックし、国を選択して、郵便番号をコンマ区切りまたは別々の行に貼り付けるか入力し、**[!UICONTROL Include All]**&#x200B;をクリックします。 含まれている郵便番号ターゲットを削除するには、ターゲットの上にカーソルを置き、![削除](/help/creative/assets/delete.png "削除") **[!UICONTROL Remove]**&#x200B;をクリックします。

      1. （オプション）複数の地理的ターゲットが指定されている場合に複数のターゲットノードを作成するには、**[!UICONTROL Split targets to create nodes]**&#x200B;を選択します。

         この機能は、指定された地理的ターゲットごとに（個別のクリエイティブバンドルを含む）個別のターゲットノードを作成します。 ターゲットを分割しない場合、ユーザーは指定したすべての場所（[!DNL Boolean] `AND` ステートメント）に属している必要があります。

      1. **[!UICONTROL Apply]**&#x200B;をクリックします。

   * データパスターゲットの場合は、オプションでデータパスキーをカスタマイズし、単一のデータパス値を入力して、**[!UICONTROL Apply]**&#x200B;をクリックします。

     キーと値のペアのキーのデフォルト値は、**[!UICONTROL Data Pass]** エクスペリエンス設定[!UICONTROL Advanced]の[ セクションの](experience-settings-targeting.md) フィールドで既に設定されています。 オプションでキーをカスタマイズできます。

   * リターゲティングピクセルターゲットの場合は、使用するリターゲティングピクセルと、クリエイターを表示するために存在する必要があるピクセルの属性の必要な値を選択します。 次に、**[!UICONTROL Apply]**&#x200B;をクリックします。

     リターゲティングピクセルの属性は、[ リターゲティングピクセル設定](/help/creative/pixels/retargeting-pixel-manage.md)で設定されます。

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

1. 次のいずれかの操作を行います。

   * （オプション） [新しいターゲットノードにクリエイター](experience-assign-creative-bundles.md)を割り当てます。

   * （オプション）エクスペリエンスを保存するには：

      1. 「**[!UICONTROL Save]**」をクリックし、「**[!UICONTROL OK]**」をクリックします。

      1. （最下位レベルの各ノードに1つ以上のクリエイティブが含まれていない場合）：次のいずれかの操作を行います。

         * 必要なクリエイティブバンドルをすべて含めずにエクスペリエンスを保存するには、**[!UICONTROL Save as Draft]**&#x200B;をクリックします。

           ドラフトエクスペリエンスの広告タグを作成することはできません。

         * クリエイティブバンドルがまだ割り当てられていない各ターゲットにデフォルトのクリエイティブを割り当てるには、**[!UICONTROL Assign Default Creatives]**&#x200B;をクリックします。 デフォルトのクリエイターが割り当てられている更新されたツリーを確認したら、「**[!UICONTROL Save]**」と「**[!UICONTROL OK]**」をクリックします。

         * 決定ツリーの編集を続行するには、**[!UICONTROL Continue Edit]**&#x200B;をクリックします。

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
