---
title: '[!DNL Google Ads]の動的検索ターゲットを管理'
description: '[!DNL Google Ads]動的検索ターゲットを作成および管理する方法について説明します。'
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
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

## [!UICONTROL Auto Targets] ビュー {#auto-target-view-about}

[!UICONTROL Targeting] > [!UICONTROL Auto Targets] ビューには、選択した広告主アカウントのフィルター処理されたビュー内のすべての動的検索ターゲットが一覧表示されます。 また、動的検索目標を管理することもできます。

データを表示するには、[!UICONTROL View Auto Targets]権限が必要です。 ターゲットを作成し、入札またはステータスを編集するには、[!UICONTROL Edit Auto Targets]権限が必要です。

### 使用可能なアクション

* [動的検索ターゲットの作成](#auto-target-create)

* [動的検索ターゲットの設定の編集](#auto-target-edit)

* [動的検索対象のステータスの変更または削除](#auto-target-status)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

* [動的検索対象に制約](#constraint-assign)を割り当て、[動的検索対象から制約](#constraint-unassign)を削除します

* [ ラベル分類](#classification-values-assign)を動的検索対象に割り当て、[動的検索対象からラベル分類](#classification-values-remove)を削除します

>[!NOTE]
>
>[ バルクシート ファイル ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)をアップロードして広告ネットワークに投稿すると、大量のターゲットデータ（ラベルや制約の割り当てを含む）を一度に作成および編集できます。

## [!DNL Google Ads]動的検索ターゲットの作成 {#auto-target-create}

同じ広告グループ内の動的検索広告のターゲットにコンテンツを使用するweb サイト（広告の表示URLで使用されるドメイン）のページを定義するために、動的検索目標を作成できます。

インデックス付きのすべてのページをターゲットにすることも、3つまで条件を指定することもできます。

>[!NOTE]
>
>パフォーマンスを最適に追跡するには、キャンペーンごとに1つの広告グループのみに[!UICONTROL All] オプションを使用してターゲットを作成します。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Create Auto Target]**&#x200B;をクリックします。

1. **[!UICONTROL Basic Settings]**&#x200B;で、広告ネットワーク、アカウント、キャンペーン、広告グループを選択します。

1. 残りの[動的検索ターゲット設定](#auto-target-create-settings)を指定します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 設定を確認します。 設定を変更するには、該当するセクションの![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、設定を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## [!DNL Google Ads]動的検索ターゲット設定の編集 {#auto-target-edit}

1つ以上の動的検索対象のステータスまたは最大入札額を編集できます。 ターゲットとなる基準は変更できません。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. 編集する各行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Edit Auto Targets]** パネルで、[ ステータスと入札設定](#auto-target-edit-settings)を編集します。

   変更は、選択したすべてのターゲットに適用されます。 変更しない設定では、既存の値が保持されます。

   選択したターゲットが複数の通貨を使用する場合、入札編集は無効になります。 ステータスは変更できます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1つのターゲットの入札値をクリックして、データテーブル内で直接、1つのターゲットの入札額を編集することもできます。

## [!DNL Google Ads]動的検索対象のステータスを変更または削除します {#auto-target-status}

アクティブな動的検索ターゲットを一時停止して、同じ広告グループ内の動的検索広告の使用を停止できます。 後で、ステータスをアクティブに戻すことで、ターゲットの使用を再開できます。 また、動的検索対象を削除することもできます。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. （オプション）特定の動的検索対象を含めるようにリストをフィルタリングします。

1. 次のいずれかの操作を行います。

   * 1つのターゲットのステータスを変更するには、**[!UICONTROL Status]**&#x200B;列でその値をクリックし、**[!UICONTROL Active]**&#x200B;または&#x200B;**[!UICONTROL Paused]**&#x200B;を選択します。

   * 複数のターゲットのステータスを変更するには、各ターゲットの横にあるチェックボックスを選択し、一括アクションツールバーの&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックし、**[!UICONTROL Edit Auto Targets]** パネルの&#x200B;**[!UICONTROL Status]**&#x200B;を選択して、**[!UICONTROL Save]**&#x200B;をクリックします。

   * 1つ以上のターゲットを削除するには、各ターゲットの横にあるチェックボックスを選択し、一括アクションツールバーの&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**&#x200B;をクリックし、確認メッセージの&#x200B;**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

## 動的検索対象の制約の割り当ての管理 {#constraints}

### 動的検索対象への制約の割り当て {#constraint-assign}

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. 1つの制約を割り当てる各動的検索ターゲットの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

### 選択した動的検索ターゲットから制約を削除 {#constraint-unassign}

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. 制約の割り当てを解除する動的検索ターゲットの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

## 動的検索対象の分類値の管理 {#classification-values}

### 動的検索対象への分類値の割り当て {#classification-values-assign}

>[!NOTE]
>
>ラベル値は子エンティティによって継承されるため、継承された値を上書きしない限り、動的検索対象の値を入力しないでください。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

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

### 動的検索対象からラベル分類値を削除します {#classification-values-remove}

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**&#x200B;をクリックします。

1. ラベル値を削除する各動的検索ターゲットの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられたすべての値の選択を解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

## [!DNL Google Ads]動的検索ターゲット設定 {#dynamic-search-target-settings}

### 作成時に使用可能な設定 {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**自動ターゲット：** コンテンツが広告グループ内の動的検索広告のターゲット設定に使用される、インデックス付きのページ：

* *[!UICONTROL All]* （既定値）：すべてのインデックス付きページをターゲットにします。

* *[!UICONTROL Specific]:*&#x200B;は、最大3つの条件に一致するページをターゲットにします。 基準を選択し、その値を入力します。 別の基準を追加するには、**[!UICONTROL And]**&#x200B;をクリックします。 条件はANDと組み合わされるので、ページは指定したすべての条件に一致する必要があります。 **[!UICONTROL Reset]**&#x200B;をクリックして条件をクリアします。

  * *[!UICONTROL Category]:* ページの[!DNL Google Ads] コンテンツカテゴリが、指定された値に等しい。 値を入力します。

  * *[!UICONTROL URL]:* ページのURLには、`shoes.example.com`など、指定された値が含まれています。 有効なURLを入力してください。

  * *[!UICONTROL Page Title]:* ページタイトルには、指定されたテキストが含まれています。 値を入力します。

  * *[!UICONTROL Page Content]:* ページのコンテンツに、指定したテキストが含まれています。 値を入力します。

ターゲットの作成後にターゲット条件を変更することはできません。

**[!UICONTROL Status]:** ターゲットのステータス：

* *[!UICONTROL Active]* （既定値）：入札を有効にします。

* *[!UICONTROL Paused]:*&#x200B;入札を無効にします。

**[!UICONTROL Bid]:** ターゲットのクリック単価（CPC）の上限です。 この値は、広告グループレベルの入札を上書きします。 このフィールドはオプションです。入札を入力すると、最小値はアカウント通貨で0.01になります。

>[!NOTE]
>
>ターゲットが最適化されたポートフォリオにある場合、指定されたCPC入札は1日適用されます。 その後、最適化機能では、独自の計算に従って入札を行います。

### 編集中に使用可能な設定 {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** **[!UICONTROL Active]**&#x200B;または&#x200B;**[!UICONTROL Paused]**&#x200B;を選択してください。

#### [!UICONTROL Bid details]

選択したターゲットが複数の通貨を使用している場合、入札編集は無効になります。

**[!UICONTROL Bid adjustment]:**&#x200B;最大入札額の変更方法：

* *[!UICONTROL Set to]:*&#x200B;各入札を[!UICONTROL Set value]の金額に置き換えます。

* *[!UICONTROL Increase]:*&#x200B;各入札額を[!UICONTROL Set value]の金額または割合で増やします。

* *[!UICONTROL Decrease]:*&#x200B;各入札額を[!UICONTROL Set value]の金額または割合で減らします。

**[!UICONTROL Modifier type]:** （[!UICONTROL Increase]および[!UICONTROL Decrease]の場合）は&#x200B;**[!UICONTROL Currency]**&#x200B;または&#x200B;**[!UICONTROL Percentage]**&#x200B;を選択します。

**[!UICONTROL Set value]:**&#x200B;新しい入札、または各入札を変更する金額または割合。 最小値は0.01です。

**[!UICONTROL Max limit]:** （オプション、[!UICONTROL Increase]および[!UICONTROL Decrease]の場合）口座通貨の上限です。 増加のために、これは最大の結果として生じる入札です。 減少の場合、これは最小結果の入札です。 制限を入力すると、最小値は0.01になります。

>[!MORELIKETHIS]
>
>* [ （新しいUI）検索入札単位の制約を管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [ （新しいUI） ラベル分類の管理](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
