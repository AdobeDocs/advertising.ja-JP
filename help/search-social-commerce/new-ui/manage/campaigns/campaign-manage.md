---
title: キャンペーンの管理
description: 広告キャンペーンを作成および管理する方法を説明します。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6b67f3e2759ddd80300c86df610b36684b7a07e2
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# キャンペーンの管理

*Beta機能*

キャンペーンは、広告ネットワークアカウントの主要なコンポーネントです。 ほとんどのキャンペーンタイプでは、一連の広告グループまたは広告セットで構成されます。 キャンペーンの設定には、キャンペーンの予算パラメーター、広告ターゲット、キャンペーン内のすべての広告のオプションのトラッキングパラメーターが含まれます。 キャンペーンレベルのトラッキングパラメーターは、アカウントレベルのパラメーターを上書きしますが、それ自体が下位レベルで上書きされる場合があります。

[API接続を介して広告ネットワークアカウントにアクセスできるようにし](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)、Search, Social, &amp; Commerceがアカウントデータを広告ネットワークと同期したら、[ サポートされているキャンペーンの種類](/help/search-social-commerce/introduction/supported-inventory.md)を使用して新しいキャンペーンを作成できます。 キャンペーンのステータスを編集および変更することもできます。

各広告ネットワークで使用できる機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## [!UICONTROL Campaigns] ビューについて {#campaign-view-about}

[!UICONTROL Manage] > [!UICONTROL Campaigns] ビューには、選択した広告主アカウントのフィルター処理されたビュー内のすべてのキャンペーンが一覧表示されます。 キャンペーン名をクリックすると、キャンペーン内の広告グループのリストを開くことができます。

[!UICONTROL Campaigns] ビューでキャンペーンデータを追加および編集すると、Search, Social, &amp; Commerceは、データの変更を直ちに広告ネットワークにプッシュします。 また、Search, Social, &amp; Commerceでは、施策の構造データとクリックデータを毎日取得します。新しい施策が検出されたときに、より頻繁に取得します。 同期されているすべての広告ネットワークに対して、必要に応じてアカウントをオンデマンドで同期することもできます。

Search, Social, &amp; Commerceは、同期された[!DNL Google Ads]および[!DNL Microsoft Advertising]個のアカウントから毎時間、他の同期された広告ネットワーク アカウントに対して毎日パフォーマンスデータを取得します。

### 使用可能なアクション

* [キャンペーンの作成](#campaign-create)

* [行内からキャンペーンの名前を変更する](#campaign-rename)

* [キャンペーン設定の編集](#campaign-edit)

* [行内からキャンペーンのステータスを変更または削除する](#campaign-status)

* [キャンペーンをポートフォリオに割り当て、キャンペーンをポートフォリオから削除する](#campaign-portfolio)

* [[!UICONTROL Campaigns] ビューでのパフォーマンス グラフの表示](#campaign-performance-graph)

* [キャンペーンに入札制約を割り当て、キャンペーンから制約を割り当て解除します](#campaign-constraints)

* [キャンペーンにターゲット制約を割り当て、キャンペーンからターゲット制約を割り当て解除します](#campaign-target-constraints)

* [キャンペーンにラベル分類を割り当て、キャンペーンからラベル分類を削除します](#campaign-classifications)

* [[!UICONTROL Campaigns] ビューからのデータビューレポートの管理](#campaign-reports)

## キャンペーンの作成 {#campaign-create}

>[!NOTE]
>
>* キャンペーンを作成する前に、広告主のweb ページに[ コンバージョン追跡タグ ](/help/search-social-commerce/tracking/conversion-tracking-about.md)を実装します。
>* 一度に多数のキャンペーンを作成するには、<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->を使用します [ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. **[!UICONTROL Create Campaign]**&#x200B;をクリックします。

1. [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)、[Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)、[LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)、または[Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)のキャンペーン設定を指定します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックし、キャンペーン設定を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

キャンペーンが作成された広告ネットワークによっては、キャンペーンが広告ネットワークにプッシュされる前に、関連する広告グループと広告を作成する必要がある場合があります。

## キャンペーン名の変更 {#campaign-rename}

キャンペーンの全設定を開かずに、キャンペーンの名前をすばやく変更できます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーン行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Rename]**&#x200B;をクリックします。

1. 名前を編集し、**[!UICONTROL Apply]**&#x200B;をクリックします。

## キャンペーン設定の編集 {#campaign-edit}

個々のキャンペーンの設定を編集することもできます。 また、キャンペーンの詳細、予算オプション、選択したすべてのキャンペーンに共通するURL オプションなど、複数のキャンペーンの一部のフィールドを一度に編集することもできます。

>[!TIP]
>
><!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->を使用してデータを一括編集することもできます [ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * エンティティ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Edit]**&#x200B;をクリックします。

   * キャンペーンの横にあるチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)、[Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)、[LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)、<!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), -->を編集します [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)または[Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)のキャンペーン設定。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックし、キャンペーン設定を変更します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

キャンペーンを作成した広告ネットワークによっては、広告ネットワークにプッシュする前に、キャンペーンに広告グループと広告を含める必要がある場合があります。

## キャンペーンのステータスの変更 {#campaign-status}

キャンペーンの全設定を開かずに、キャンペーンのステータスをすばやく変更できます。

サポートされている広告ネットワークでアクティブなキャンペーンを一時停止して、入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブなキャンペーンまたは一時停止したキャンペーンを削除することもできます。 削除されたキャンペーンは、広告ネットワークから削除されます。 データフィルターに含めても表示されますが、変更することはできません。

### キャンペーンの有効化または一時停止

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーン行の上にカーソルを置き、[!UICONTROL Status]列の横にある![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. ステータスの変更：

   * 一時停止したキャンペーンをアクティブ化するには、**[!UICONTROL Active]**&#x200B;を選択します。

   * アクティブなキャンペーンを一時停止するには、**[!UICONTROL Paused]**&#x200B;を選択します。

### キャンペーンの削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * キャンペーン行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Delete]**&#x200B;をクリックします。

   * キャンペーン行の上にカーソルを置き、[!UICONTROL Status]列の横にある![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。 **[!UICONTROL Deleted]**&#x200B;を選択します。

## キャンペーンのポートフォリオへの割り当て {#campaign-portfolio}

キャンペーンを最適化されたポートフォリオに割り当てることで、Search, Social, &amp; Commerceで、キャンペーン内のキーワードと広告の入札額、キャンペーン予算、入札戦略目標を最適化できます。 ポートフォリオを作成する際、またはポートフォリオの設定を編集する際に、[!UICONTROL Campaigns] ビューからキャンペーンをポートフォリオに割り当てることができます。

すべてのキャンペーンタイプと広告ネットワークが最適化の対象になるわけではありません。ポートフォリオに含めることができる[ サポートされているキャンペーンタイプ ](/help/search-social-commerce/introduction/supported-inventory.md)のリストを参照してください。 さらに、各キャンペーン入札戦略](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)に対する[最適化サポートを確認します。

>[!NOTE]
>
>各キャンペーンは、1つのポートフォリオにのみ割り当てることができます。 既に別のポートフォリオに関連付けられているキャンペーンを新しいポートフォリオに割り当てると、元のポートフォリオから削除されます。

### [!UICONTROL Campaigns] ビューから既存のポートフォリオにキャンペーンを割り当てます

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 各キャンペーンの横にあるチェックボックスを選択して、1つのポートフォリオに割り当てます。

1. 一括操作ツールバーで、「**+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]**」をクリックします。

1. ポートフォリオを選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

### [!UICONTROL Campaigns] ビューから新しいポートフォリオにキャンペーンを割り当てます

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 新しいポートフォリオを作成する各キャンペーンの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**&#x200B;をクリックします。

1. [!UICONTROL Create Portfolio]画面で、ポートフォリオ設定を指定します。

   以前に選択したキャンペーンは、既にキャンペーンに割り当てられています。 必要に応じて、ポートフォリオのキャンペーンリストを編集できます。

   ポートフォリオ設定について詳しくは、Search, Social, &amp; Commerce内から入手できる最適化ガイドを参照してください。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

### ポートフォリオのキャンペーン割り当てを[!UICONTROL Portfolios] ビューから変更します

ポートフォリオから施策を削除すると、Search, Social, &amp; Commerceでは、その施策の入札額、施策の予算、入札戦略の目標を最適化できません。

アクションは、ポートフォリオの変更履歴に記録されます。

最適化について詳しくは、Search, Social, &amp; Commerce内から入手できる最適化ガイドを参照してください。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Portfolios]**&#x200B;をクリックします。

1. ポートフォリオの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. ポートフォリオ設定で、[!UICONTROL Assign Campaigns] セクションに移動し、キャンペーンの割り当てを変更します。

   ポートフォリオ設定について詳しくは、Search, Social, &amp; Commerce内から入手できる最適化ガイドを参照してください。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 設定を確認し、必要に応じて変更を加え、**[!UICONTROL Save]**&#x200B;をクリックします。

## キャンペーンの入札制約の割り当てを管理 {#campaign-constraints}

各エンティティには1つの制約しか設定できません。 制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティに制約を割り当てる必要はありません。

制約の割り当てを解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、制約のレポートデータはそれらのコンポーネントでは使用できなくなります。 制約の割り当てを解除しても、制約やアカウントコンポーネント自体は削除されません。

>[!NOTE]
>
>アクティブな制約は、最適化された従来のキーワードレベルのポートフォリオで、割り当てられた入札単位のみに対して入札を制限します。 アクティブなポートフォリオにある、ハイブリッドポートフォリオにある、またはポートフォリオにない入札単位については無視されます。

### 新しい[!UICONTROL Campaigns] ビューから選択したキャンペーンに入札制約を割り当てます

1つ以上のキャンペーンに1つの制約を割り当てることができます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 1つの制約を割り当てる各キャンペーンの横にあるチェックボックスをオンにします。

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

### 新しい[!UICONTROL Campaigns] ビューから、選択したキャンペーンから入札制限を削除します

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 制約の割り当てを解除する各キャンペーンの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

### 従来の[!UICONTROL Campaigns] ビューから検索入札単位から入札制限を削除します

>[!NOTE]
>
>制約を削除して後で使用できないようにするには、Search, Social, &amp; Commerce内から使用できる「入札制約」の最適化ガイドの「検索入札単位の制約の削除」を参照してください。<!-- verify convention for referencing Optimization Guide here -->

1. **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;で、アカウントコンポーネントビューを選択します。

1. 制約を削除する各コンポーネントの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. データテーブルの上にあるツールバーで、**[!UICONTROL More]**&#x200B;をクリックし、**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 確認ダイアログで、**[!UICONTROL Yes, Unassign]**&#x200B;を選択します。

## キャンペーンのターゲット制約の割り当てを管理 {#campaign-target-constraints}

### 新しい[!UICONTROL Campaigns] ビューから選択したキャンペーンにターゲット制約を割り当てます

1つまたは複数のキャンペーンに単一のターゲット制約を割り当てることができます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 1つのターゲット制約を割り当てる各キャンペーンの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

### 新しい[!UICONTROL Campaigns] ビューから、選択したキャンペーンからターゲット制約を削除します

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. ターゲット制約の割り当てを解除する各キャンペーンの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

## キャンペーンへのラベル分類の割り当て {#campaign-classifications}

>[!NOTE]
>
>ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

### キャンペーンへの分類値の割り当て

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. ラベル値を割り当てる各キャンペーンの横にあるチェックボックスをオンにします。

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

### キャンペーンからのラベル分類値の削除

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. ラベル値を削除する各キャンペーンの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられた値をすべて選択解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

## [!UICONTROL Campaigns] ビューでのパフォーマンス グラフの表示 {#campaign-performance-graph}

指定した日付範囲のビューのすべてのキャンペーンをまたいで合計3つの指標を含むパフォーマンスグラフを開いて設定します。

### パフォーマンスグラフを表示

1. データテーブルの上にある「![ グラフ ](/help/search-social-commerce/assets/charts.png " グラフ ")」をクリックします。

1. （オプション）通貨と、チャートに含める最大3つの指標を指定します。

### 表示されているパフォーマンスグラフを非表示にする

* データテーブルの上にある「![ グラフ ](/help/search-social-commerce/assets/charts.png " グラフ ")」をクリックします。

## [!UICONTROL Campaigns] ビューからのデータビューレポートの管理 {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

[!UICONTROL Campaigns] ビューの1つ以上のキャンペーンのデータ行を含むレポートを生成し、レポートをMicrosoft Excel ワークシート ファイル （XLXS形式）としてダウンロードします。 レポートには、表示されているすべての列がビューに含まれます。

生成されたレポートはすべて削除できます。

「>* [ （従来のUI） キャンペーン管理ビューからデータをダウンロード ](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)」および「[ （従来のUI） [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)からパフォーマンスデータレポートまたはバルクシートファイルを削除」も参照してください。

### フィルタリングされたデータ行を含むレポートを生成する

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. データをダウンロードするキャンペーンを指定します。

   * 特定のキャンペーンのデータをダウンロードするには、キャンペーンの横にあるチェックボックスをオンにします。

   * すべてのキャンペーンのデータをダウンロードするには、チェックボックスをオンにする必要はありません。 すべてのキャンペーンはデフォルトで含まれています。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports]設定で、一意のレポート名を入力し、**[!UICONTROL Generate]**&#x200B;をクリックします。

   デフォルトでは、ファイル名は「campaign_YYYYMMDD_NNNNN」です。ここでは、「NNNN」は順次ジョブ番号（「campaign_20250402_1326」など）です。

   ファイルが[!UICONTROL Recently Generated] リストに追加されます。

1. （オプション）完了したファイルをダウンロードするには、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完成したレポートをダウンロード

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完了済みレポートの削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

>[!MORELIKETHIS]
>
>* [検索入札単位の制約の管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [広告グループの制約の割り当てを管理](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [ キーワードの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [ プレースメントの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [ （レガシーUI） キャンペーン管理ビューからデータをダウンロード ](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [ （従来のUI） [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)からパフォーマンス データ レポートまたはバルクシート ファイルを削除します
>* [[!DNL Baidu]  キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads]  キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads]  キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising]  キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex]  キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

