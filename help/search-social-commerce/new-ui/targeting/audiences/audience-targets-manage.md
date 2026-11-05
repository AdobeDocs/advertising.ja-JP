---
title: キャンペーンと広告グループのオーディエンスターゲットの管理
description: Google AdsおよびMicrosoft Advertisingのオーディエンスのターゲットと入札調整を管理する方法について説明します。
feature: Search Campaign Management
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
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%
---
# キャンペーンと広告グループのオーディエンスターゲットの管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

[!DNL Google Ads]件のキャンペーンと広告グループ、および[!DNL Microsoft Advertising]件の広告グループは、同じ広告ネットワークから特定の[&#x200B; オーディエンス &#x200B;](audience-manage.md)をターゲットにできます。 広告ネットワークは、ターゲティングできるオーディエンスの規模を決定します。

オーディエンスターゲットは、既存のオーディエンスをキャンペーンまたは広告グループに関連付けます。 既存のターゲットの入札調整とステータスを編集できます。

>[!NOTE]
>
>[&#x200B; オーディエンスの除外](audience-exclusions.md)は、常にターゲットを上書きします。

## [!UICONTROL Targets] ビューについて {#audience-targets-view-about}

[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] ビューには、選択した広告主のフィルター処理されたビュー内のオーディエンスターゲットが一覧表示されます。

データを表示するには、[!UICONTROL View Audiences]権限が必要です。 ターゲットの編集、ステータスの変更、および削除には、[!UICONTROL Edit Audience Targets]権限が必要です。

### 使用可能なアクション

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [オーディエンスターゲットの入札調整とステータスの編集](#audience-targets-edit)

* [オーディエンスターゲットのステータスの変更または削除](#audience-targets-status)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## オーディエンスターゲットの入札調整とステータスの編集 {#audience-targets-edit}

一度に1つ以上のオーディエンスターゲットを編集できます。 変更は、選択したすべてのターゲットに適用されます。

>[!NOTE]
>
>Search, Social, &amp; Commerceでは、親キャンペーンがCPC入札戦略を使用し、オーディエンスターゲットの入札調整値を自動最適化するように設定されたポートフォリオ内にある場合、入札修飾子が自動的に最適化されます。 [!DNL Microsoft Advertising]動的リマーケティングオーディエンスターゲットの入札修飾子が最適化されていません。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Audiences]**&#x200B;をクリックし、**[!UICONTROL Targets]** タブをクリックします。

1. 編集する各ターゲットの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Bid Modifier]**&#x200B;または&#x200B;**[!UICONTROL Status]**、またはその両方を編集します。 [設定の編集](#audience-targets-edit-settings)を参照してください。

   既存の値を保持するには、フィールドを変更しないでください。

1. （オプション）「**[!UICONTROL ADDITIONAL DETAILS]**」を展開し、**[!UICONTROL Project Name]**&#x200B;と&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

**[!UICONTROL Bid Adjustment]**&#x200B;列の値をクリックして、単一のターゲットの入札調整をデータテーブルで直接編集することもできます。

## オーディエンスターゲットのステータスの変更または削除 {#audience-targets-status}

アクティブなオーディエンスターゲットを一時停止して、そのターゲットの入札を無効にし、後でアクティブ化して入札を再開することができます。 アクティブまたは一時停止したターゲットを削除することもできます。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Audiences]**&#x200B;をクリックし、**[!UICONTROL Targets]** タブをクリックします。

1. （オプション）特定のオーディエンスターゲットを含めるようにリストをフィルタリングします。

1. ステータスを変更する各ターゲットの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、次のいずれかをクリックします。

   * 選択したターゲットをアクティブ化するには、**[!UICONTROL Activate]**&#x200B;してください。

   * 選択したターゲットを一時停止するには、**[!UICONTROL Pause]**&#x200B;してください。

   * 選択したターゲットを削除するには、**[!UICONTROL Delete]**&#x200B;してください。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

## オーディエンスターゲットの編集設定 {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** オーディエンス入札調整を変更する方法：

* *[!UICONTROL Set To]:*&#x200B;既存の入札調整を指定された割合に置き換えます。

* *[!UICONTROL Increase]:*&#x200B;既存の値を指定した割合だけ増やします。

* *[!UICONTROL Decrease]:*&#x200B;既存の値を指定した割合だけ減らします。

[!UICONTROL Increase]と[!UICONTROL Decrease]に対して、負でない値を入力します。

設定された値の場合、0%は入札を調整しません。 サポートされているその他の値の範囲は–90%から900%です。 例えば、キーワードレベルの入札が1 USDで、オーディエンスの入札調整が50%の場合、そのオーディエンスの入札は1.50 USDに増加します。

**[!UICONTROL Status]:**&#x200B;入札を有効にするには&#x200B;**[!UICONTROL Active]**&#x200B;を選択し、ターゲットの入札を無効にするには&#x200B;**[!UICONTROL Paused]**&#x200B;を選択します。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスの管理](audience-manage.md)
>* [&#x200B; キャンペーンと広告グループのオーディエンス除外の管理](audience-exclusions.md)
