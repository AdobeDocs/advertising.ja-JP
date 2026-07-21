---
title: ショッピング商品グループの管理
description: Google AdsおよびMicrosoft Advertisingのショッピング商品グループについて説明します。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# ショッピング商品グループの管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising]個のショッピング キャンペーンのみ*

製品グループは、[!UICONTROL Assets] > [!UICONTROL Shopping]の[!UICONTROL Product Groups] ビューで作成および管理できます。

製品グループに関するデータは、[の[!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)で表示できます。

## 製品グループとは？

ショッピング施策では、キーワードではなく商品グループが、ショッピング広告が表示されるマーチャントセンターのアカウント内の商品を決定します。 各製品グループは、単一の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品ID、カスタムラベルなど）に基づいており、一致するすべての製品に同じ入札を使用します。 各グループの商品に入札を含めることも、除外することもできます。

広告グループレベルで商品グループを設定し、マーチャントセンターのアカウントのどの商品が広告グループのショッピング広告に表示されるかを決定します。 広告グループに広告エンティティが含まれていない場合でも、広告ネットワークには製品の広告が表示されます。

同じ製品が複数のキャンペーンに含まれている場合、広告ネットワークはまずキャンペーンの優先順位を使用して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを決定します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。

[!DNL Google]個のショッピング キャンペーンと広告について詳しくは、「[実装 [!DNL Google Ads]  ショッピング キャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)」および[Google広告のドキュメント &#x200B;](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1)を参照してください。 [!DNL Microsoft]個のショッピング キャンペーンについて詳しくは、「[実装 [!DNL Microsoft Advertising]  ショッピング キャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)」および[[!DNL Microsoft Advertising]  ドキュメント &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500)を参照してください。

>[!NOTE]
>
>パフォーマンスの最大キャンペーンの[!DNL Google Ads] リストグループでは、サポートを利用できません。 リスト グループのデータを管理および表示するには、[!DNL Google Ads] エディターを使用します。

### 製品グループの階層

広告グループに特定の属性を持つ製品グループを作成する前に、まず「[!UICONTROL All Products]」という包括的な製品グループを作成する必要があります。 この親製品グループから、製品のサブセットの子製品グループを作成したり、子製品グループから孫を作成したりできます。 広告グループの最初の子製品グループを作成すると、デフォルトの広告グループ入札を使用して、「[!UICONTROL Everything Else]」という別の製品グループが自動的に作成されます。 製品グループを追加すると、「[!UICONTROL Everything Else]」グループが調整され、別の製品グループに含まれないすべての製品を構成するようになります。

広告グループ内で、入札を含めたり除外したりするために最大7つのレベルの製品グループ（「[!UICONTROL All Products]」を含まない）を作成できます。各レベルで同じ属性をターゲットとする1つ以上の製品グループを作成できます（例：[!UICONTROL Brand]=1つの製品グループにはAcme、同じレベルで別の製品グループには[!UICONTROL Brand]=AcmePlus）。 親製品グループはサブディビジョンと呼ばれ、サブディビジョンの最下位レベルはユニットと呼ばれます。 単体レベルで、入札額やトラッキングテンプレートを設定したり、入札を完全に除外したりできます。 広告グループのアクティブな製品グループ全体が階層的に適用され、対象製品が決定されます。 例えば、[!UICONTROL All Products]を[!UICONTROL Brand]=AcmeBasicと[!UICONTROL Brand]=AcmePlusに分割し、それぞれの製品グループを[!UICONTROL Condition]=Newとset Bidに分割すると、AcmeBasic ブランドとAcmePlus ブランドを持つ新しい製品のみが広告または広告から除外されます。

![製品グループセットの例](/help/search-social-commerce/assets/product-group-list-new.png "製品グループセットの例")

![製品グループ階層の例](/help/search-social-commerce/assets/product-group-tree-new.png "製品グループ階層の例")

### 製品フィルター {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

[!DNL Google Ads]のヘルプ「[製品グループを使用したショッピング キャンペーンの管理](https://support.google.com/google-ads/answer/6275317)」および[!DNL Microsoft Advertising]のヘルプ「[製品グループの理解と使用](https://help.ads.microsoft.com/#apex/bae/en/56782)」も参照してください。

| ショッピングネットワーク | Product Dimension | 属性 | メモ |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: [!UICONTROL Category 1=] ～ [!UICONTROL Category 5=] | \[ カテゴリ ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[ ブランド\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[項目ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Product Type (1st level)=] ～ [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[製品タイプ\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] ～ [!UICONTROL Custom Label 4=] | \[ カスタムラベルの属性\] | — |
| [!DNL Google Ads] | Channel= | [!UICONTROL Local], [!UICONTROL Online] | ローカル製品またはオンライン製品の広告のみを表示するには、<br><br><b>注意：</b> ローカル製品の広告を作成するには、「ローカル在庫広告」オプションを有効にする必要があります。また、[!DNL Google Merchant Center]さんと一緒にローカルショッピングプログラムに参加する必要があります。 |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | 1つのチャネル（ローカルのみ、またはオンラインのみ）でのみ使用できる製品の広告を表示するか、複数のチャネル（ローカルとオンラインの両方）で使用できる製品の広告を表示するかどうか。 |

## [!UICONTROL Product Groups] ビュー

[!UICONTROL Assets] > [!UICONTROL Shopping] ビューの[!UICONTROL Product Groups] ビューには、選択した広告主アカウントのフィルター処理されたビュー内のすべての製品グループが一覧表示されます。 また、製品グループを作成し管理することもできます。

### 使用可能なアクション <!-- Go through all -->

* [「[!UICONTROL All Products]」製品グループの作成](#product-group-create-all-products)

* [既存の製品グループに子製品グループノードを作成する](#node-add)

* 製品グループノードの設定を編集：

  * [任意の設定を編集](#node-edit)

  * [[!UICONTROL Tracking Template]のみを編集](#node-edit-tracking-template)

  * [[!UICONTROL Max CPC]のみを編集](#node-edit-maxcpc)

* [製品グループノードの削除](#node-delete)

* [製品グループに制約](#constraint-assign)を割り当て、[製品グループから制約](#constraint-unassign)を削除

* [&#x200B; ラベル分類](#classification-values-assign)を製品グループに割り当て、[&#x200B; ラベル分類](#classification-values-remove)を製品グループから削除

>[!NOTE]
>
>[&#x200B; バルクシート ファイル &#x200B;](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)をアップロードして広告ネットワークに投稿すると、大量の製品グループデータ（ラベルや制約の割り当てを含む）を一度に作成および編集できます。

## 「[!UICONTROL All Products]」製品グループの作成 {#product-group-create-all-products}

特定の属性を持つ製品グループを作成する前に、まず「[!UICONTROL All Products]」という名前の包括的な製品グループを作成する必要があります。 各広告グループには、「[!UICONTROL All Products]」グループを1つだけ設定できます。

>[!TIP]
>
>多くのアカウントコンポーネントを一度に作成するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Create Product Group]**&#x200B;をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. [Google Ads製品グループ設定](#google-ads-product-group-settings)または[Microsoft Advertising製品グループ設定](#microsoft-advertising-product-group-settings)を指定します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックし、[Google Ads product group settings](#google-ads-product-group-settings)または[Microsoft Advertising product group settings](#microsoft-advertising-product-group-settings)を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## 既存の製品グループに子製品グループノードを作成する {#product-group-create-child}

広告グループのオールインクルーシブ「[!UICONTROL All Products]」グループを少なくとも作成したら、入札に含める製品のサブセットまたは入札から除外する製品の子製品グループノードを作成できます。各レベルで同じ属性をターゲットとする製品グループを1つ以上作成できます（例：[!UICONTROL Brand]=1つの製品グループに対してAcme、同じレベルで別の製品グループに対して[!UICONTROL Brand]=AcmePlus。 「[!UICONTROL All Products]」を含めずに、最大7 レベルの子製品グループノードを作成できます。

>[!NOTE]
>
>「[!UICONTROL Everything Else]」製品グループの子製品グループを作成することはできません。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. （オプション）製品グループとその子製品グループノードをツリービューで表示するには、製品グループ名にカーソルを合わせ、**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;をクリックします。

1. 製品グループ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL + Add Node]**&#x200B;をクリックします。

1. [Google Ads製品グループ設定](#google-ads-product-group-settings)または[Microsoft Advertising製品グループ設定](#microsoft-advertising-product-group-settings)を指定します。

1. **[!UICONTROL Center]**&#x200B;をクリックします。

## 製品グループノードの設定の編集 {#node-edit}

広告グループに含まれるユニット製品グループノード（子製品グループノードのない製品グループ）の入札および追跡テンプレートを編集できます。 除外単位製品グループ、または子の製品グループノードを持つ製品グループである含まれるサブディビジョン ノードまたは除外されたサブディビジョン ノードの情報を編集することはできません。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. （オプション）製品グループとその子製品グループノードをツリービューで表示するには、製品グループ名にカーソルを合わせ、**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;をクリックします。

1. 製品グループ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL + Edit Node]**&#x200B;をクリックします。

1. [Google Ads製品グループ設定](#google-ads-product-group-settings)または[Microsoft Advertising製品グループ設定](#microsoft-advertising-product-group-settings)を編集します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

## 製品グループ ノードの[!UICONTROL Tracking Template]のみを編集 {#node-edit-tracking-template}

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. 製品グループ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;をクリックして、製品グループとその子製品グループノードをツリー表示で表示します。

1. **[!UICONTROL Tracking Template]**&#x200B;列で、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックします。

1. **[!UICONTROL Tracking Template]**&#x200B;値を変更し、**[!UICONTROL Save]**&#x200B;をクリックします。

## 製品グループ ノードの[!UICONTROL Max CPC]のみを編集 {#node-edit-maxcpc}

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. 製品グループ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;をクリックして、製品グループとその子製品グループノードをツリー表示で表示します。

1. **[!UICONTROL Max CPC]**&#x200B;列で、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックします。

1. **[!UICONTROL Max CPC]**&#x200B;値を変更し、**[!UICONTROL Save]**&#x200B;をクリックします。

## 製品グループノードの削除 {#node-delete}

他の商品グループが同じレベルに存在する場合は、「その他すべて」グループを除いて、あらゆる商品グループを削除できます。このグループは、マーチャント センターのアカウントのどの商品が広告グループのショッピング広告に含まれているかを判断するために使用されます。 製品グループを削除すると、すべての子製品グループが削除されます。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. 製品グループ名の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;をクリックして、製品グループとその子製品グループノードをツリー表示で表示します。

1. **[!UICONTROL Status]**&#x200B;列をクリックし、**[!UICONTROL Delete]**&#x200B;を選択します。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## 選択した製品グループへの制約の割り当て {#constraint-assign}

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. 1つの制約を割り当てる各製品グループの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

## 選択した製品グループから制約を削除 {#constraint-unassign}

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. 制約の割り当てを解除する各製品グループの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

## 製品グループへの分類値の割り当て {#classification-values-assign}

>[!NOTE]
>
>ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. ラベル値を割り当てる各製品グループの横にあるチェックボックスをオンにします。

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

## 製品グループからのラベル分類値の削除 {#classification-values-remove}

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Shopping]**&#x200B;をクリックします。

1. ラベル値を削除する各製品グループの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられた値をすべて選択解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

## [!DNL Google Ads]製品グループの設定 {#google-ads-product-group-settings}

### 「すべての製品」製品グループ

**[!UICONTROL Network]:** （新製品グループのみ）広告ネットワーク。

**[!UICONTROL Account]:** （新製品グループのみ）広告ネットワークアカウント名。

**[!UICONTROL Campaign]:** （新製品グループのみ）キャンペーン。

**[!UICONTROL Ad Group]:** （新製品グループのみ）広告グループ。

**[!UICONTROL Condition]**&#x200B;または&#x200B;**[!UICONTROL Condition Type]:** （読み取り専用）すべての製品

**[!UICONTROL Condition Value]:** （既存の製品グループのみ）  

**[!UICONTROL Bid]**&#x200B;または&#x200B;**[!UICONTROL Max CPC]:** （含まれる製品グループのみ）広告クリックに対する支払い額が最も高いクリック単価（CPC）。 この値は、子製品グループのないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

{{$include /help/_includes/tracking-template-google.md}}

このテンプレートは、より高いレベルでテンプレートを上書きし、子製品グループのないユニットにのみ使用されます。 アカウントまたはキャンペーンに指定された追加パラメーターは含まれません。 アカウントまたはキャンペーンに指定された追加パラメーターは含まれません。

### その他すべての製品グループ

**[!UICONTROL Condition Type]**&#x200B;および&#x200B;**[!UICONTROL Condition Value]:** （既存の製品グループの読み取り専用） ターゲットにする製品ディメンション。 新しい製品グループの場合、製品をターゲットにするディメンションと、選択した情報カテゴリの適格属性を入力します（ブランド別のターゲット設定の場合は「Acme」、条件別のターゲット設定の場合は「New」など）。

特定の商品ディメンション（つまり「すべての商品」ではなく）の商品グループを作成すると、Search, Social, &amp; Commerceは、「その他」の商品グループを自動的に作成します。

使用可能な製品ディメンションのリストについては、「[製品フィルター](#product-filters)」を参照してください。 ディメンションのリストは、キャンペーンの[!UICONTROL Inventory Filter]設定に基づいて制限される場合があります。

**[!UICONTROL Excluded]:** （新製品グループの場合はオプション、既存製品グループの場合は読み取り専用）一致する製品の広告の入札を除外します。

**[!UICONTROL Max CPC]:** （含まれる製品グループのみ）広告クリックに対する支払い額が最も高いクリック単価（CPC）です。 この値は、子製品グループのないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

このテンプレートは、より高いレベルでテンプレートを上書きし、子製品グループのないユニットにのみ使用されます。

## [!DNL Microsoft Advertising]製品グループの設定 {#microsoft-advertising-product-group-settings}

### 「すべての製品」製品グループ

**[!UICONTROL Network]:** （新製品グループのみ）広告ネットワーク。

**[!UICONTROL Account]:** （新製品グループのみ）広告ネットワークアカウント名。

**[!UICONTROL Campaign]:** （新製品グループのみ）キャンペーン。

**[!UICONTROL Ad Group]:** （新製品グループのみ）広告グループ。

**[!UICONTROL Condition]**&#x200B;または&#x200B;**[!UICONTROL Condition Type]:** （読み取り専用）すべての製品

**[!UICONTROL Condition Value]:** （既存の製品グループのみ）  

**[!UICONTROL Bid]**&#x200B;または&#x200B;**[!UICONTROL Max CPC]:** （含まれる製品グループのみ）広告クリックに対する支払い額が最も高いクリック単価（CPC）。 この値は、子製品グループのないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

**[!UICONTROL Base URL]:** （新製品グループのみ）未使用<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

このテンプレートは、より高いレベルでテンプレートを上書きし、子製品グループのないユニットにのみ使用されます。

### その他すべての製品グループ

**[!UICONTROL Condition Type]**&#x200B;および&#x200B;**[!UICONTROL Condition Value]:** （既存の製品グループの読み取り専用） ターゲットにする製品ディメンション。 新しい製品グループの場合、製品のターゲットとなるディメンションと、選択した情報カテゴリの適格属性を入力します（ブランド別のターゲット設定の場合は「Acme」、条件別のターゲット設定の場合は「New」など）。

特定の商品ディメンション（つまり「すべての商品」ではなく）の商品グループを作成すると、Search, Social, &amp; Commerceは、「その他」の商品グループを自動的に作成します。

使用可能な製品ディメンションのリストについては、「[製品フィルター](#product-filters)」を参照してください。 ディメンションのリストは、キャンペーンの[!UICONTROL Inventory Filter]設定に基づいて制限される場合があります。

**[!UICONTROL Excluded]:** （新製品グループの場合はオプション、既存製品グループの場合は読み取り専用）一致する製品の広告の入札を除外します。

**[!UICONTROL Max CPC]:** （含まれる製品グループのみ）広告クリックに対する支払い額が最も高いクリック単価（CPC）です。 この値は、子製品グループのないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

このテンプレートは、より高いレベルでテンプレートを上書きし、子製品グループのないユニットにのみ使用されます。

>[!MORELIKETHIS]
>
>* [&#x200B; ショッピング キャンペーン  [!DNL Google Ads] を実装](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [&#x200B; ショッピング キャンペーン  [!DNL Microsoft Advertising] を実装](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [The [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
