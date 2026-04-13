---
title: プレースメントの制約の割り当ての管理
description: プレースメントに拘束を割り当てる方法について説明します。
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: 325fb6b2-7f6f-41bc-bae7-9ee8590c6263
source-git-commit: 235ba59f2d9e37259431b415c2e34c0da8209ef9
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# （新しいUI）プレースメントの制約の割り当てを管理する

*Beta機能*

キャンペーン、広告グループ、キーワード、プレースメント、ユニットレベルの商品グループ、動的検索ターゲットの検索エンティティに対して、入札制限を割り当てて削除できます。 各エンティティには1つの制約しか設定できません。

制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティに制約を割り当てる必要はありません。

制約の割り当てを解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、制約のレポートデータはそれらのコンポーネントでは使用できなくなります。 制約の割り当てを解除しても、制約やアカウントコンポーネント自体は削除されません。

>[!NOTE]
>
>* 後で変更不可の広告のキーワードまたは広告コピーを編集し、それによって新しいキーワードまたは広告を作成した場合、制約は新しいエンティティに割り当てられません。
>* アクティブな制約は、最適化された従来のキーワードレベルのポートフォリオで、割り当てられた入札単位のみに対して入札を制限します。 アクティブなポートフォリオにある、ハイブリッドポートフォリオにある、またはポートフォリオにない入札単位については無視されます。

## 新しい[!UICONTROL Placements] ビューから選択した配置に制約を割り当てます

1つ以上のプレースメントに1つのコンストレインを割り当てることができます。

1. メインメニューで、**[!UICONTROL Target]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、1つの制約を割り当てる各配置の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

## 従来の[!UICONTROL Campaigns] ビューから選択した検索入札単位に制約を割り当てます

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;で、アカウントコンポーネントビューを選択します。

1. 各関連行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. データテーブルの上にあるツールバーで、**[!UICONTROL More]**&#x200B;をクリックし、**[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 適用可能な制約を選択します。

1. （オプション）追加の詳細を入力します。

   1. [!UICONTROL Additional Details]の横にある「**[!UICONTROL Open]**」をクリックして詳細を展開します。

   1. オプションの&#x200B;**[!UICONTROL Project Name]**&#x200B;またはオプションの&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 新しい[!UICONTROL Placements] ビューから選択したプレースメントから制約を割り当て解除する

1. メインメニューで、**[!UICONTROL Target]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、制約の割り当てを解除する各プレースメントの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

## 従来の[!UICONTROL Campaigns] ビューから検索入札単位から制約を割り当て解除します

>[!NOTE]
>
>制約を削除して後で使用できないようにするには、Search, Social, &amp; Commerce内から使用できる「入札制約」の最適化ガイドの「検索入札単位の制約の削除」を参照してください。<!-- verify convention for referencing Optimization Guide here -->

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;で、アカウントコンポーネントビューを選択します。

1. 制約を削除する各コンポーネントの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. データテーブルの上にあるツールバーで、**[!UICONTROL More]**&#x200B;をクリックし、**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 確認ダイアログで、**[!UICONTROL Yes, Unassign]**&#x200B;を選択します。

>[!MORELIKETHIS]
>
>* [ キャンペーンの制約の割り当ての管理](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [広告グループの制約の割り当てを管理](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [ キーワードの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
