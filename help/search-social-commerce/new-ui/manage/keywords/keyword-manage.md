---
title: キーワードの管理
description: 入札可能キーワードとネガティブキーワードを作成および管理し、キーワードに制約を割り当てる方法について説明します。
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%
---
# キーワードの管理

*Beta機能*

*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]および既存の[!DNL Baidu] アカウントのみ*

キーワードとは、広告に関連付けられた単語またはフレーズのことです。 キーワード設定には、キーワード一致タイプ、キーワードによって広告がトリガーされたときに使用される最大入札額、および（一部の広告ネットワークの場合）オプションのトラッキングパラメーターが含まれます。 キーワードレベルの設定は、広告グループまたはキャンペーンの設定を上書きします。 ネガティブキーワードは、一致する検索に対して広告が表示されるのを防ぎます。

[API接続を介して広告ネットワークアカウントにアクセスできるようにし](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)、Search, Social, &amp; Commerceがアカウントデータを広告ネットワークと同期したら、[&#x200B; サポートされているキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)で検索広告グループのキーワードを作成できます。 また、キーワードのステータスを編集および変更したり、負のキーワードを作成および削除したりすることもできます。

各広告ネットワークで使用できる機能について詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## [!UICONTROL Keywords] ビューについて {#keyword-view-about}

[!UICONTROL Manage] > [!UICONTROL Keywords] ビューには、選択した広告主アカウントの2つのタブが含まれています。

* 「[!UICONTROL Keywords]」タブには、フィルタリングされたビュー内のすべての入札可能なキーワードが一覧表示されます。

* 「[!UICONTROL Negatives]」タブには、フィルター処理されたビュー内のすべての否定的なキーワードが一覧表示されます。

### 使用可能なアクション

* [キーワードの作成](#keyword-create)

* [否定的なキーワードを作成](#keyword-negative-create)

* [キーワード設定の編集](#keyword-edit)

* [キーワードと負のキーワードのステータスを変更または削除](#keyword-status)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

* [キーワードに制約を割り当て、キーワードから制約を割り当て解除する](#keyword-constraints)

* [&#x200B; キーワードにラベル分類](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)を割り当てる

## キーワードの作成 {#keyword-create}

>[!TIP]
>
>一度に多数のキーワードを作成するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Keywords]**」タブで、「**[!UICONTROL Create Keywords]**」をクリックします。

1. **[!UICONTROL Basic Settings]** ステップで、ネットワーク、アカウント、キャンペーン、および広告グループを選択します。

1. [[!DNL Baidu]  キーワード設定](keyword-settings-baidu.md)、[[!DNL Google Ads]  キーワード設定](keyword-settings-google.md)、[[!DNL LY Ads]  キーワード設定](keyword-settings-yahoo-japan.md)、[[!DNL Microsoft Advertising]  キーワード設定](keyword-settings-microsoft.md)または[[!DNL Yandex]  キーワード設定](keyword-settings-yandex.md)を入力します。

   1回の操作で最大2000個のキーワードを入力またはペーストできます。 複数のキーワードをコンマで区切るか、別々の行に入力します。

   >[!NOTE]
   >
   >アカウントまたはキャンペーンの設定が広告レベルでのみトラッキングを指定する場合、Search, Social, &amp; Commerceではキーワードのトラッキングは生成されません。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、エンティティやキーワードの設定を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## キーワード設定の編集 {#keyword-edit}

キーワードテキストまたは一致タイプを変更すると、広告ネットワークに応じて、既存のキーワードを削除して新しいキーワードを作成できます。 詳しくは、広告ネットワークのキーワード設定を参照してください。

>[!TIP]
>
>異なる広告ネットワーク上のキーワードを含む、大量のキーワードデータを一度に編集するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Keywords]**」タブで、編集する各キーワードの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [[!DNL Baidu]  キーワード設定](keyword-settings-baidu.md)、[[!DNL Google Ads]  キーワード設定](keyword-settings-google.md)、[[!DNL LY Ads]  キーワード設定](keyword-settings-yahoo-japan.md)、[[!DNL Microsoft Advertising]  キーワード設定](keyword-settings-microsoft.md)または[[!DNL Yandex]  キーワード設定](keyword-settings-yandex.md)を編集します。

   複数のキーワードの場合は、選択したすべてのキーワードに共通するフィールドのみを編集でき、変更は選択したすべてのキーワードに適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、接頭辞を追加したり、接尾辞を追加したりできます。 一部の金銭的なフィールドでは、既存の値を指定した値に変更したり、指定した割合または金額を増減したりできます（制限あり）。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、キーワード設定を変更します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

## 否定的なキーワードを作成 {#keyword-negative-create}

*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]および既存の[!DNL Baidu] アカウントのみ*

検索やディスプレイ/ネイティブネットワークをターゲットとする検索広告グループまたはキャンペーンに対して、ネガティブキーワードを作成できます。

>[!NOTE]
>
>また、[広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)および[&#x200B; キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)で、否定的なキーワードを作成および編集することもできます。

>[!TIP]
>
>一度に多数の否定的なキーワードを作成するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Negatives]**」タブで「**[!UICONTROL Create Negatives]**」をクリックし、「**[!UICONTROL Campaign Negative Keyword]**」または「**[!UICONTROL Ad Group Negative Keyword]**」をクリックします。

1. ネットワーク、アカウント、キャンペーン、および（広告グループレベルのネガティブキーワードの場合）広告グループを選択します。

1. 否定的なキーワードを入力します。 マイナス記号（`-`）なしで次の構文を使用します。

   * 負の部分一致：`keyword` （[!DNL Microsoft Advertising]ではサポートされていません）

   * 否定的な語句の一致：`"keyword"`

   * 負の完全一致：`[keyword]`

   複数の値をコンマで区切るか、別々の行に入力します。 1回の操作で最大2000個のネガティブキーワードを入力またはペーストできます。 次の要件と制限が適用されます。

   * 最大文字長：[!DNL Baidu]: 30 シングルバイトまたは15 ダブルバイト、[!DNL Microsoft Advertising]: 100 シングルバイトまたは50 ダブルバイト、[!DNL Google Ads]および[!DNL LY Ads]: 80 シングルバイトまたは40 ダブルバイト。

   * [!DNL Baidu]では、広告グループごとにキーワードごとに1つの一致タイプのみが許可されます。 例えば、広告グループ 1に`"keyword"`と`[keyword]`の両方を含めることはできません。

   * [!DNL Google Ads]：各キーワードは10文字以下で構成でき、文字、数字、および次の特殊文字のみを含めることができます：スペース `# $ & _ - " [ ] ' + . / :`

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、エンティティおよび/または負のキーワードを変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## キーワードと否定的なキーワードのステータスの変更 {#keyword-status}

アクティブで入札可能な検索キーワードを一時停止して、入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブまたは一時停止した検索キーワードまたはネガティブキーワードを削除することもできます。 削除されたキーワードは、広告ネットワークから削除されます。 データフィルターに含めても表示されますが、変更することはできません。

### キーワードの有効化または一時停止

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Keywords]**」タブで、オプションでリストをフィルタリングし、ステータスを変更する各キーワードの横にあるチェックボックスを選択します。

1. 一括操作ツールバーで、ステータスを変更します。

   * 一時停止したキーワードを有効にするには、**[!UICONTROL Activate]**&#x200B;をクリックします。

   * アクティブなキーワードを一時停止するには、**[!UICONTROL Pause]**&#x200B;をクリックします。

### キーワードまたは否定的なキーワードの削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Keywords]**」または「**[!UICONTROL Negatives]**」タブで、オプションでリストをフィルタリングし、削除する各キーワードまたは負のキーワードの横にあるチェックボックスを選択します。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

## キーワードの制約の割り当ての管理 {#keyword-constraints}

キャンペーン、広告グループ、キーワード、プレースメント、単位レベルの商品グループ、動的検索対象に対して、入札制約を割り当て、削除できます。 各エンティティには1つの制約しか設定できません。

制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティに制約を割り当てる必要はありません。

制約の割り当てを解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、制約のレポートデータはそれらのコンポーネントでは使用できなくなります。 制約の割り当てを解除しても、制約やアカウントコンポーネント自体は削除されません。

>[!NOTE]
>
>* 後で変更不可の広告のキーワードまたは広告コピーを編集し、それによって新しいキーワードまたは広告を作成した場合、制約は新しいエンティティに割り当てられません。
>* アクティブな制約は、最適化された従来のキーワードレベルのポートフォリオで、割り当てられた入札単位のみに対して入札を制限します。 アクティブなポートフォリオにある、ハイブリッドポートフォリオにある、またはポートフォリオにない入札単位については無視されます。

### キーワードへの制約の割り当て {#keyword-constraint-assign}

1つ以上のキーワードに1つの制約を割り当てることができます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Keywords]**」タブで、1つの制約を割り当てる各キーワードの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

### キーワードからの制約の割り当て解除 {#keyword-constraint-unassign}

制約の割り当てを解除しても、その制約は削除されません。 制約を削除して後で使用できないようにするには、Search, Social, &amp; Commerce内から使用できる「入札制約」の最適化ガイドの「検索入札単位の制約を削除する」を参照してください。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 「**[!UICONTROL Keywords]**」タブで、制約の割り当てを解除する各キーワードの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [[!DNL Baidu]  キーワード設定](keyword-settings-baidu.md)
>* [[!DNL Google Ads]  キーワード設定](keyword-settings-google.md)
>* [[!DNL LY Ads]  キーワード設定](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising]  キーワード設定](keyword-settings-microsoft.md)
>* [[!DNL Yandex]  キーワード設定](keyword-settings-yandex.md)
>* [検索入札単位の制約の管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [&#x200B; ラベル分類の管理](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
