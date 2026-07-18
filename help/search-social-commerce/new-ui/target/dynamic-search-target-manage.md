---
title: ' [!DNL Google Ads] 動的検索ターゲットの管理'
description: ' [!DNL Google Ads] 動的検索ターゲットを作成および管理する方法について説明します。'
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 82db1b4d0d8703229a4002e932d5b2f52f845814
workflow-type: tm+mt
source-wordcount: 718
ht-degree: 0%

---

# [!DNL Google Ads]の動的検索ターゲットを管理

*[!DNL Google Ads]アカウントのみ*

検索ネットワークを使用する[!DNL Google Ads] キャンペーンの動的検索ターゲットのステータスを作成、編集、変更できます。

## 動的検索目標とは何ですか？

動的検索ターゲットは、広告ネットワークが動的検索広告のターゲットとしてweb サイト内のページの全体またはサブセットを使用するかどうかを定義します。 広告グループレベルで動的検索ターゲットを設定します。同じ広告グループ内のすべての動的検索広告に適用されます。

キャンペーン設定に応じて、動的検索ターゲットが必須またはオプションの場合があります。

* キャンペーンの「[!UICONTROL DSA Options]」セクションでweb サイトのドメインと言語を指定しない場合は、動的検索ターゲットを作成する必要があります。

* キャンペーンの「[!UICONTROL DSA Options]」セクションでweb サイトドメインと言語を指定する場合は、オプションで動的検索ターゲットを作成できます。

  [!DNL Google Ads]は、これらの設定で指定されたweb サイトのコンテンツに基づいて、動的検索広告を自動的に表示します。

パフォーマンスを最適に追跡するには、動的検索ターゲットごとに1つの広告グループでキャンペーンを設定し、すべての条件をターゲットとする広告グループを含めます。

[!DNL Google Ads]件の動的検索広告について詳しくは、https://support.google.com/google-ads/answer/2471185を参照してください。

## [!UICONTROL Auto Targets] ビュー

[!UICONTROL Auto Targets] ビューには、選択した広告主アカウントのフィルター処理されたビュー内のすべての動的検索ターゲットが一覧表示されます。

[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Auto Targets] ビューで、動的検索ターゲットのステータスを作成、編集、変更できます。

任意のターゲットに[ ラベル ](/help/search-social-commerce/campaign-management/label-classifications/classification-values-assign-campaign-management.md)を適用することもできます。

### 使用可能なアクション

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [動的検索ターゲットに制約を割り当て](#constraint-assign)、および[動的検索ターゲットから制約を割り当て解除](#constraint-unassign)

* [ ラベル分類](#classification-values-assign)を動的検索対象に割り当て、[動的検索対象からラベル分類](#classification-values-remove)を削除します

>[!NOTE]
>
>[ バルクシート ファイル ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)をアップロードして広告ネットワークに投稿すると、大量のターゲットデータ（ラベルや制約の割り当てを含む）を一度に作成および編集できます。

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## 新しい[!UICONTROL Auto Targets] ビューから選択した動的検索ターゲットに制約を割り当てます {#constraint-assign}

1. メインメニューで、**[!UICONTROL Target]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. 1つの制約を割り当てる各動的検索ターゲットの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

## 選択した動的検索対象から新しい[!UICONTROL Auto Targets] ビューから制約を割り当て解除する {#constraint-unassign}

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. 制約の割り当てを解除する動的検索ターゲットの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

## 動的検索対象への分類値の割り当て {#classification-values-assign}

>[!NOTE]
>
>ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

1. メインメニューで、**[!UICONTROL Target]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. ラベル値を割り当てる各動的検索ターゲットの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 適用できる各分類値について、次の操作を行います。

   1. **[!UICONTROL Classifications]**&#x200B;列で、分類を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、列見出しの[!UICONTROL +]をクリックします。 入力フィールドに分類名を入力し、![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")をクリックして、分類をすぐに保存します。 新しい分類を使用するには、分類名をクリックして展開します。

        名前は[ASCII文字32 ～ 126](https://www.asciitable.com/)で、最大長は27文字です。

   1. **[!UICONTROL Value Name]**&#x200B;列で、選択した分類の値を指定します。

      * 既存の値を使用するには、値を選択します。

      * 値を作成するには、列見出しの[!UICONTROL +]をクリックします。 入力フィールドに値を入力し、![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")をクリックして値をすばやく保存し、デフォルトで選択します。

        最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

1. **+[!UICONTROL Assign Now]**&#x200B;をクリックします。

## 動的検索対象からラベル分類値を削除します{#classification-values-remove}

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

1. メインメニューで、**[!UICONTROL Target]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. ラベル値を削除する各動的検索ターゲットの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられた値をすべて選択解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ （新しいUI）検索入札単位の制約を管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [ （新しいUI） ラベル分類の管理](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
