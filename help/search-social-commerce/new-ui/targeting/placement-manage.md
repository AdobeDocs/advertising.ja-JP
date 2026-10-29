---
title: プレースメントの管理
description: Google Ads プレースメントとネガティブプレースメントを作成および管理し、プレースメントに制約を割り当てる方法について説明します。
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
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 0%
---
# プレースメントの管理

*Beta機能*

*[!DNL Google Ads]アカウントのみ*

プレースメントは、広告を表示できるディスプレイネットワーク上の場所です。 配置の設定には、最大入札額とオプションのトラッキングパラメーターが含まれます。 配置レベルの設定は、広告グループまたはキャンペーンの設定を上書きします。 ネガティブな配置は、指定したサイトに広告が表示されないようにします。

[API接続を介して広告ネットワークアカウントにアクセスできるようにし](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)、Search, Social, &amp; Commerceがアカウントデータを広告ネットワークと同期したら、ディスプレイネットワークをターゲットとする[ サポートされているキャンペーンタイプ ](/help/search-social-commerce/introduction/supported-inventory.md)で広告グループのプレースメントを作成できます。 また、プレースメントのステータスを編集および変更したり、負のプレースメントを作成および削除することもできます。

>[!NOTE]
>
>[!DNL Google Ads]は、プレースメントの広告レベルのパフォーマンスデータを提供していません。

## [!UICONTROL Placements] ビューについて {#placement-view-about}

[!UICONTROL Targeting] > [!UICONTROL Placements] ビューには、選択した広告主アカウントの2つのタブが含まれています。

* 「[!UICONTROL Placements]」タブには、フィルタリングされたビュー内のすべての入札可能なプレースメントが一覧表示されます。

* 「[!UICONTROL Negatives]」タブには、フィルター処理されたビュー内のすべてのネガティブなプレースメントが一覧表示されます。

ページを表示するには[!UICONTROL View Placements]権限が必要です。 プレースメントまたはネガティブプレースメントの作成、プレースメントの編集、プレースメントのステータスの変更、プレースメントまたはネガティブプレースメントの削除には、[!UICONTROL Edit Placements]権限が必要です。

### 使用可能なアクション

* [プレースメントの作成](#placement-create)

* [ネガティブプレースメントを作成](#placement-negative-create)

* [プレースメント設定の編集](#placement-edit)

* [プレースメントと負のプレースメントのステータスを変更または削除する](#placement-status)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

* [プレースメントに制約を割り当て、プレースメントから制約を割り当て解除する](#placement-constraints)

* [プレースメントへのラベル分類の割り当て](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## プレースメントの作成 {#placement-create}

>[!TIP]
>
>一度に多数のプレースメントを作成するには、[ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、「**[!UICONTROL Create Placement]**」をクリックします。

1. **[!UICONTROL Basic Settings]** ステップで、ネットワーク、アカウント、キャンペーン、および広告グループを選択します。

1. [ プレースメント設定](#placement-create-settings)を入力します。

   複数のプレースメントを作成するには、web サイトのURLをコンマで区切ります。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、エンティティやプレースメント設定を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## ネガティブプレースメントを作成 {#placement-negative-create}

ディスプレイ ネットワークをターゲットとする[!DNL Google Ads] キャンペーンまたは広告グループに対して、ネガティブなプレースメントを作成できます。

>[!NOTE]
>
>また、[広告グループ設定](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)および[ キャンペーン設定](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)でネガティブプレースメントを作成および編集することもできます。

>[!TIP]
>
>一度に多数のネガティブプレースメントを作成するには、[ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Negatives]**」タブで「**[!UICONTROL Create Negative]**」をクリックし、「**[!UICONTROL Campaign Negative]**」または「**[!UICONTROL Ad Group Negative]**」をクリックします。

1. **[!UICONTROL Basic Settings]** ステップで、ネットワーク、アカウント、キャンペーン、および（広告グループレベルのネガティブプレースメントの場合）広告グループを選択します。

1. **[!UICONTROL Manage Websites]** ステップで、`www.example.com`や`example.com/shoes`などのネガティブ web サイト URLを入力します。

   複数のURLをコンマで区切ります。 このフォームは、トピックやカテゴリ文字列ではなく、web サイトのURLを受け入れます。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、エンティティおよび/またはネガティブ web サイト URLを変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## プレースメント設定の編集 {#placement-edit}

1つ以上のプレースメントのステータス、入札、ベース URL、およびトラッキングテンプレートを編集できます。 ターゲット web サイト URLを変更したり、削除したプレースメントを編集したりすることはできません。

>[!TIP]
>
>大量の配置データを一度に編集するには、[ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、編集する各プレースメントの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Edit Placements]** パネルで、[ プレースメント設定](#placement-edit-settings)を編集します。

   複数のプレースメントの場合、変更は選択したすべてのプレースメントに適用されます。 入札を指定した値に設定したり、指定した割合または金額だけ入札を増減したりできます。制限があります。 URLの場合、既存の値を置き換えたり、テキストを検索して置換したり、接頭辞を追加したり、接尾辞を追加したりできます。

   選択したプレースメントが複数の通貨を使用している場合、入札編集は無効になります。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## プレースメントとネガティブプレースメントのステータスの変更 {#placement-status}

アクティブで入札可能なプレースメントを一時停止して、入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

また、アクティブなプレースメントまたは一時停止したプレースメントまたはネガティブなプレースメントを削除することもできます。 削除されたプレースメントは、広告ネットワークから削除されます。 データフィルターに含めても表示されますが、変更することはできません。

### プレースメントの有効化または一時停止

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、オプションでリストをフィルタリングし、ステータスを変更する各プレースメントの横にあるチェックボックスを選択します。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Placement Details]** セクションで、**[!UICONTROL Status]**&#x200B;を変更します。

   * 一時停止したプレースメントをアクティブにするには、**[!UICONTROL Active]**&#x200B;を選択します。

   * アクティブなプレースメントを一時停止するには、**[!UICONTROL Paused]**&#x200B;を選択します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

### プレースメントまたはネガティブプレースメントの削除

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」または「**[!UICONTROL Negatives]**」タブで、オプションでリストをフィルタリングし、削除するプレースメントまたは負のプレースメントの横にあるチェックボックスを選択します。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

## プレースメントの制約の割り当ての管理 {#placement-constraints}

キャンペーン、広告グループ、キーワード、プレースメント、単位レベルの商品グループ、動的検索対象に対して、入札制約を割り当て、削除できます。 各エンティティには1つの制約しか設定できません。

制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティに制約を割り当てる必要はありません。

制約の割り当てを解除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除され、制約のレポートデータはそれらのコンポーネントでは使用できなくなります。 制約の割り当てを解除しても、制約やアカウントコンポーネント自体は削除されません。

>[!NOTE]
>
>* 後で変更不可の広告のキーワードまたは広告コピーを編集し、それによって新しいキーワードまたは広告を作成した場合、制約は新しいエンティティに割り当てられません。
>* アクティブな制約は、最適化された従来のキーワードレベルのポートフォリオで、割り当てられた入札単位のみに対して入札を制限します。 アクティブなポートフォリオにある、ハイブリッドポートフォリオにある、またはポートフォリオにない入札単位については無視されます。

### プレースメントへの制約の割り当て {#placement-constraint-assign}

1つ以上のプレースメントに1つのコンストレインを割り当てることができます。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、1つの制約を割り当てる各配置の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

### プレースメントから制約を割り当て解除 {#placement-constraint-unassign}

制約の割り当てを解除しても、その制約は削除されません。 制約を削除して今後の使用に使用できないようにするには、「[検索入札単位の制約を管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status)」を参照してください。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Placements]**&#x200B;をクリックします。

1. 「**[!UICONTROL Placements]**」タブで、制約の割り当てを解除する各プレースメントの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

## 配置の設定 {#placement-settings}

### プレースメント作成時の設定 {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。 [!DNL Google Ads]のみがサポートされています。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。

**[!UICONTROL Ad Group]:**&#x200B;広告グループ。

#### [!UICONTROL Placement Details]

広告を表示できるディスプレイ ネットワーク上の&#x200B;**[!UICONTROL Placements]:** サイト `www.example.com`、`example.com`、`example.com/shoes`など、有効なWeb サイト URLを入力してください。 複数のURLをコンマで区切ります。 URLに疑問符（`?`）を含めることはできません。

代わりにweb サイトを除外するには、[!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] タブから[ ネガティブプレースメント ](#placement-negative-create)を作成するか、広告グループとキャンペーン設定を使用します。

**[!UICONTROL Status]:** プレースメントの表示ステータス：*[!UICONTROL Active]* （入札を有効にする場合）または&#x200B;*[!UICONTROL Paused]* （入札を無効にする場合）。

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** （オプション） キャンペーン入札戦略に応じて、プレースメントベースの広告のクリック単価（CPC）または表示可能インプレッション数（vCPM）の千単位あたりのコストを指定します。 この値は、広告グループレベルの入札を上書きします。

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>新しいUI作成フォームでは、ベース URLとトラッキングテンプレートを指定する場合、`http://`または`https://`から開始する必要があります。

### プレースメントの編集時の設定 {#placement-edit-settings}

[!UICONTROL Edit Placements] パネルでは、選択した1つ以上のプレースメントに対して次の設定がサポートされています。 ターゲットサイトのURLは変更できません。

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:**&#x200B;入札方法：

* *[!UICONTROL Set to]:*&#x200B;既存の入札を指定した値に置き換えます。

* *[!UICONTROL Increase]:*&#x200B;既存の入札額を指定した金額または割合で増やします。

* *[!UICONTROL Decrease]:*&#x200B;既存の入札額を指定した金額または割合で減らします。

**[!UICONTROL Modifier type]:** （増減の場合）調整で&#x200B;*[!UICONTROL Currency]*&#x200B;または&#x200B;*[!UICONTROL Percentage]*&#x200B;を使用しているかどうか。

**[!UICONTROL Set value]:**&#x200B;新しい入札額または調整額。 最小値は0.01です。

**[!UICONTROL Max limit]:** （増減の場合。オプション）調整された入札の制限。 増加の場合は、これが最大入札額です。減少の場合は、これが最小入札額です。 最小制限値は0.01です。

選択したプレースメントが複数の通貨を使用している場合、入札編集は無効になります。

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**、**[!UICONTROL Tracking Template]:**&#x200B;各フィールドについて、値を変更する方法を選択します。

* *[!UICONTROL Set To]:*&#x200B;値を置き換えます。 `http://`または`https://`で始まる有効なWeb サイト URLを入力してください。

* *[!UICONTROL Find/Replace]:*&#x200B;指定したテキストを値の範囲内で置換します。 検索するテキストと置換テキストを入力します。

* *[!UICONTROL Add Suffix]:*&#x200B;値にテキストを追加します。 接尾辞テキストを入力します。

* *[!UICONTROL Add Prefix]:*&#x200B;値の先頭にテキストを追加します。 接頭辞テキストを入力します。

>[!NOTE]
>
>新しいベース URLはすべて、`http://`または`https://`で始まる有効なURLである必要があります。

>[!MORELIKETHIS]
>
>* [検索入札単位の制約の管理](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [ ラベル分類の管理](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
