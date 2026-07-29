---
title: 広告グループの管理
description: 広告グループを作成および管理する方法について説明します。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e120af366651028227306e993e73f125f29a431f
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# 広告グループの管理

<!-- Go through all -->

*Beta機能*

広告グループには、一連の広告とその関連キーワードが含まれます。 ディスプレイネットワークをターゲットとするキャンペーン内の広告グループには、広告を表示できるディスプレイネットワーク上の場所であるプレースメントも含めることができます。 広告グループのすべてのコンポーネントに適用される広告グループの設定は、広告ネットワークによって異なります。

[API接続を介して広告ネットワークアカウントにアクセスできるようにし](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)、Search, Social, &amp; Commerceがアカウントデータを広告ネットワークと同期したら、[ サポートされているキャンペーンタイプ ](/help/search-social-commerce/introduction/supported-inventory.md)の広告グループを作成できます。 また、広告グループのステータスを編集および変更することもできます。

各広告ネットワークで使用できる機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## [!UICONTROL Ad Groups] ビューについて {#ad-group-view-about}

[!UICONTROL Manage] > [!UICONTROL Ad Groups] ビューには、選択した広告主アカウントのフィルター処理されたビュー内のすべての広告グループが一覧表示されます。

### 使用可能なアクション

* [広告グループの作成](#ad-group-create)

* [行内から広告グループの名前を変更する](#ad-group-rename)

* [広告グループ設定の編集](#ad-group-edit)

* [行内から広告グループのステータスを変更または削除する](#ad-group-status)

* [[!UICONTROL Ad Groups] ビューでのパフォーマンス グラフの表示](#ad-group-performance-graph)

* [広告グループに入札制約を割り当てる、広告グループから制約を割り当て解除する](#ad-group-constraints)

* [広告グループにラベル分類を割り当て、広告グループからラベル分類を削除します](#ad-group-classifications)

* [[!UICONTROL Ad Groups] ビューからのデータビューレポートの管理](#ad-group-reports)

## 広告グループの作成 {#ad-group-create}

>[!TIP]
>
>多数の広告グループを一度に作成するには、<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->を使用します [ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. **[!UICONTROL Create Ad Group]**&#x200B;をクリックします。

1. [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)、[Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)、[LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)、または[Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)広告グループの設定を指定します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックし、広告グループの設定を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

その後、広告グループ内の個々のキーワードまたはプレースメントの入札を設定することで、広告グループレベルの入札をオプションで上書きできます。

## 広告グループ名の変更 {#ad-group-rename}

広告グループ全体の設定を開かずに、広告グループの名前をすばやく変更できます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. 広告グループの行にカーソルを合わせ、**[!UICONTROL ...]>[!UICONTROL Rename]**&#x200B;をクリックします。

1. 名前を編集し、**[!UICONTROL Apply]**&#x200B;をクリックします。

## 広告グループ設定の編集 {#ad-group-edit}

個々の広告グループの設定を編集できます。 また、一部の広告グループの詳細、予算オプション、選択したすべての広告グループに共通するURL オプションなど、複数の広告グループの一部のフィールドを一度に編集することもできます。

>[!TIP]
>
><!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->を使用してデータを一括編集することもできます [ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * エンティティ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Edit]**&#x200B;をクリックします。

   * 広告グループの横にあるチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)、[Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)、[LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)、または[Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)広告グループの設定を編集します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックし、広告グループの設定を変更します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

## 広告グループのステータスの変更 {#ad-group-status}

広告グループ全体の設定を開かずに、広告グループのステータスをすばやく変更できます。

サポートされている広告ネットワーク上のアクティブな広告グループを一時停止して、入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブな広告グループまたは一時停止した広告グループを削除することもできます。 削除された広告グループは、広告ネットワークから削除されます。 データフィルターに含めても表示されますが、変更することはできません。

### 広告グループをアクティブ化または一時停止する

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. 広告グループの行にカーソルを置き、[!UICONTROL Status]列の横にある![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. ステータスの変更：

   * 一時停止した広告グループをアクティブ化するには、**[!UICONTROL Active]**&#x200B;を選択します。

   * アクティブな広告グループを一時停止するには、**[!UICONTROL Paused]**&#x200B;を選択します。

### 広告グループの削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * 広告グループの行にカーソルを合わせ、**[!UICONTROL ...]>[!UICONTROL Delete]**&#x200B;をクリックします。

   * 広告グループの行にカーソルを置き、[!UICONTROL Status]列の横にある![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。 **[!UICONTROL Deleted]**&#x200B;を選択します。

## 広告グループの入札制限の割り当てを管理 {#ad-group-constraints}

各エンティティには1つの制約しか設定できません。 制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティに制約を割り当てる必要はありません。

制約の割り当てを解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、制約のレポートデータはそれらのコンポーネントでは使用できなくなります。 制約の割り当てを解除しても、制約やアカウントコンポーネント自体は削除されません。

### 新しい[!UICONTROL Ad Groups] ビューから選択した広告グループに入札制限を割り当てます

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. 1つの制約を割り当てる各広告グループの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

### 従来の[!UICONTROL Campaigns] ビューから選択した検索入札単位に入札制約を割り当てます

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;で、アカウントコンポーネントビューを選択します。

1. 各関連行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. データテーブルの上にあるツールバーで、**[!UICONTROL More]**&#x200B;をクリックし、**[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 適用可能な制約を選択します。

1. （オプション）追加の詳細を入力します。

   1. [!UICONTROL Additional Details]の横にある「**[!UICONTROL Open]**」をクリックして詳細を展開します。

   1. オプションの&#x200B;**[!UICONTROL Project Name]**&#x200B;またはオプションの&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

### 新しい[!UICONTROL Ad Groups] ビューから選択した広告グループから入札制限を削除します

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. 制約の割り当てを解除する各広告グループの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

### 従来の[!UICONTROL Campaigns] ビューから検索入札単位から入札制限を削除します

>[!NOTE]
>
>制約を削除して後で使用できないようにするには、Search, Social, &amp; Commerce内から使用できる「入札制約」の最適化ガイドの「検索入札単位の制約を削除する」を参照してください。

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;で、アカウントコンポーネントビューを選択します。

1. 制約を削除する各コンポーネントの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. データテーブルの上にあるツールバーで、**[!UICONTROL More]**&#x200B;をクリックし、**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 確認ダイアログで、**[!UICONTROL Yes, Unassign]**&#x200B;を選択します。

## 広告グループへのラベル分類の割り当て {#ad-group-classifications}

>[!NOTE]
>
>ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

### 広告グループへの分類値の割り当て

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. ラベル値を割り当てる各広告グループの横にあるチェックボックスをオンにします。

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

### 広告グループからのラベル分類値の削除

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. ラベル値を削除する各広告グループの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられた値をすべて選択解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

## [!UICONTROL Ad Groups] ビューでのパフォーマンス グラフの表示 {#ad-group-performance-graph}

指定した日付範囲のビュー内のすべての広告グループで合計される最大3つの指標を含むパフォーマンスグラフを開いて設定します。

### パフォーマンスグラフを表示

1. データテーブルの上にある「![ グラフ ](/help/search-social-commerce/assets/charts.png " グラフ ")」をクリックします。

1. （オプション）通貨と、チャートに含める最大3つの指標を指定します。

### 表示されているパフォーマンスグラフを非表示にする

* データテーブルの上にある「![ グラフ ](/help/search-social-commerce/assets/charts.png " グラフ ")」をクリックします。

## [!UICONTROL Ad Groups] ビューからのデータビューレポートの管理 {#ad-group-reports}

[!UICONTROL Ad Groups] ビューの1つ以上の広告グループのデータ行を含むレポートを生成し、レポートをMicrosoft Excel ワークシート ファイル （XLXS形式）としてダウンロードします。 レポートには、表示されているすべての列がビューに含まれます。

生成されたレポートはすべて削除できます。

「>* [ （従来のUI） キャンペーン管理ビューからデータをダウンロード ](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)」および「[ （従来のUI） [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)からパフォーマンスデータレポートまたはバルクシートファイルを削除」も参照してください。

### フィルタリングされたデータ行を含むレポートを生成する

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. データをダウンロードする広告グループを指定します。

   * 特定の広告グループのデータをダウンロードするには、広告グループの横にあるチェックボックスをオンにします。

   * すべての広告グループのデータをダウンロードするには、チェックボックスをオンにする必要はありません。 デフォルトでは、すべての広告グループが含まれています。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports]設定で、一意のレポート名を入力し、**[!UICONTROL Generate]**&#x200B;をクリックします。

   デフォルトでは、ファイルの名前は「ad group_YYYYMMDD_NNNNN」です。ここでは、「NNNN」は順次ジョブ番号（「ad group_20250402_1326」など）です。

   ファイルが[!UICONTROL Recently Generated] リストに追加されます。

1. （オプション）完了したファイルをダウンロードするには、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完成したレポートをダウンロード

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完了済みレポートの削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

>[!MORELIKETHIS]
>
>* [検索入札単位の制約の管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [ キャンペーンの制約の割り当ての管理](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [ キーワードの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [ プレースメントの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [ （レガシーUI） キャンペーン管理ビューからデータをダウンロード ](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [ （従来のUI） [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)からパフォーマンス データ レポートまたはバルクシート ファイルを削除します
>* [[!DNL Baidu] 広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] 広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)
>* [[!DNL LY Ads] 広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] 広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] 広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)
