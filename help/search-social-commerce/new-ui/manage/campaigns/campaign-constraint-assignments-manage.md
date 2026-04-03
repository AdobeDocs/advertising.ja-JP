---
title: キャンペーンの制約の割り当ての管理
description: キャンペーンに制約を割り当てる方法を説明します。
feature: Search Optimization, Search Campaign Management
hide: yes
exl-id: d886a228-24d7-4d8e-b68a-76e56b4304ed
TQID: https://experienceleague.adobe.com/qwisQ3OqMeymlREsTVY-Wf59ln37hBLR0X4R7RjkuTM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 445
ht-degree: 0%

---

# （新しいUI）キャンペーンの制約の割り当ての管理

*Beta機能*

キャンペーン、広告グループ、キーワード、プレースメント、ユニットレベルの商品グループ、動的検索ターゲットの検索エンティティに対して、入札制限を割り当てて削除できます。 各エンティティには1つの制約しか設定できません。

制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティに制約を割り当てる必要はありません。

制約の割り当てを解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、制約のレポートデータはそれらのコンポーネントでは使用できなくなります。 制約の割り当てを解除しても、制約やアカウントコンポーネント自体は削除されません。

>[!NOTE]
>
>* 後で広告のキーワードまたは広告コピーを編集して、新しいキーワードまたは広告を作成した場合、制約は新しいエンティティに割り当てられません。
>* アクティブな制約は、最適化された従来のキーワードレベルのポートフォリオで、割り当てられた入札単位のみに対して入札を制限します。 アクティブなポートフォリオにある、ハイブリッドポートフォリオにある、またはポートフォリオにない入札単位については無視されます。

## 新しい[!UICONTROL Campaigns] ビューから選択したキャンペーンに制約を割り当てます

1つ以上のキャンペーンに1つの制約を割り当てることができます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 1つの制約を割り当てる各キャンペーンの横にあるチェックボックスをオンにします。

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

## 新しい[!UICONTROL Campaigns] ビューから選択したキャンペーンから制約を割り当て解除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 制約の割り当てを解除する各キャンペーンの横にあるチェックボックスをオンにします。

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
>* [広告グループの制約の割り当てを管理](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [広告の制約の割り当てを管理](/help/search-social-commerce/new-ui/manage/ads/ad-constraint-assignments-manage.md)
>* [&#x200B; キーワードの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [&#x200B; プレースメントの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
