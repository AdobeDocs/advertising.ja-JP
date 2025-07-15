---
title: 広告グループの制約割り当ての管理
description: 広告グループに制約を割り当てる方法について説明します。
feature: Search Optimization, Search Campaign Management
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# （新しい UI）広告グループの制約割り当ての管理

*Beta機能*

キャンペーン、広告グループ、キーワード、プレースメント、単位レベルの製品グループ、動的検索ターゲットの検索エンティティに対して、入札制約を割り当てたり、削除したりできます。 各エンティティに設定できる拘束は 1 つだけです。

制約は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティに制約を割り当てる必要はありません。

制約を割り当て解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、それらのコンポーネントでは制約のレポートデータを使用できなくなります。 拘束を割り当て解除しても、拘束もアカウント コンポーネント自体も削除されません。

## 新しい [!UICONTROL Ad Groups] ビューから選択した広告グループに制約を割り当てる

1. メインメニューで、**[!UICONTROL Manage]/[!UICONTROL Ad Groups]** をクリックします。

1. 単一の制約を割り当てる各広告グループの横にあるチェックボックスをオンにします。

1. ツールバーで、![ その他のアクション ](/help/search-social-commerce/assets/more-actions.png " その他のアクション ") **[!UICONTROL More Actions]** / ![割り当て](/help/search-social-commerce/assets/assign.png "割り当て") **[!UICONTROL Assign]** / **[!UICONTROL Constraint]** をクリックします。

1. 制約を選択します。

1. 「**[!UICONTROL Assign Now]**」をクリックします。

## 従来の [!UICONTROL Campaigns] ビューから選択した検索入札単位に制約を割り当てる

1. **[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** で、勘定科目コンポーネント表示を選択します。

1. 関連する各行の横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL More]**] をクリックし、**[!UICONTROL Assign]** > **[!UICONTROL Constraint]** をクリックします。

1. 該当する制約を選択します。

1. （オプション）追加の詳細を入力します。

   1. 「[!UICONTROL Additional Details]」の横の「**[!UICONTROL Open]**」をクリックして、詳細を展開します。

   1. オプションの **[!UICONTROL Project Name]** や **[!UICONTROL Description]** を入力します。

1. 「**[!UICONTROL Save]**」をクリックします。

## 選択した広告グループの制約を新しい [!UICONTROL Ad Groups] ビューから割り当て解除する

1. メインメニューで、**[!UICONTROL Manage]/[!UICONTROL Ad Groups]** をクリックします。

1. 制約の割り当てを解除する各広告グループの横にあるチェックボックスをオンにします。

1. ツールバーで、![ その他のアクション ](/help/search-social-commerce/assets/more-actions.png " その他のアクション ") **[!UICONTROL More Actions]** / ![割り当て](/help/search-social-commerce/assets/unassign.png "割り当て解除") **[!UICONTROL Unassign]** / **[!UICONTROL Constraint]** をクリックします。

1. 「**[!UICONTROL Confirm]**」をクリックします。

## 従来の [!UICONTROL Campaigns] ビューから検索入札単位の制約の割り当てを解除する

>[!NOTE]
>
>制約を削除し、後で使用できないようにする方法については、検索、ソーシャル、Commerceから利用できる「入札制約」に関する最適化ガイドの章で、「検索入札単位の制約を削除する」を参照してください <!-- verify convention for referencing Optimization Guide here -->

1. **[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** で、勘定科目コンポーネント表示を選択します。

1. 拘束を削除する各コンポーネントの横にあるチェック ボックスをオンにします。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL More]**] をクリックし、**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]** をクリックします。

1. 確認ダイアログで、「**[!UICONTROL Yes, Unassign]**」を選択します。

>[!MORELIKETHIS]
>
>* [ キャンペーンの制約割り当ての管理 ](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
