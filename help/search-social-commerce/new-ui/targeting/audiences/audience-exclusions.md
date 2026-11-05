---
title: キャンペーンと広告グループのオーディエンス除外の管理
description: Google広告の除外を削除する方法など、Google AdsとMicrosoft Advertisingのオーディエンスの除外について説明します。
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
source-wordcount: '269'
ht-degree: 0%
---
# キャンペーンと広告グループのオーディエンス除外の管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

オーディエンスの除外は、キャンペーンまたは広告グループ内の広告が、特定の[&#x200B; オーディエンス &#x200B;](audience-manage.md)のユーザーに表示されるのを防ぎます。

[!DNL Google Ads] アカウントの場合、任意のオーディエンスタイプを除外できます。 [!DNL Microsoft Advertising] アカウントの場合、動的リマーケティングオーディエンスのみを除外できます。

>[!NOTE]
>
>除外は常に[&#x200B; オーディエンスターゲット &#x200B;](audience-targets-manage.md)を上書きします。

## [!UICONTROL Exclusions] ビューについて {#audience-exclusions-view-about}

[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] ビューには、選択した広告主のフィルタリングされたビューのオーディエンス除外が一覧表示されます。

データを表示するには、[!UICONTROL View Audiences]権限が必要です。 行を選択し、サポートされている除外を削除するには、[!UICONTROL Edit Audience Exclusions]権限が必要です。

### 使用可能なアクション

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [オーディエンス除外の削除](#audience-exclusions-delete)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## オーディエンス除外の削除 {#audience-exclusions-delete}

*[!DNL Google Ads]件の除外のみ*

1つ以上の[!DNL Google Ads]個のオーディエンス除外を削除できます。 このビューでは、[!DNL Microsoft Advertising]件の除外の削除はサポートされていません。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Audiences]**&#x200B;をクリックし、**[!UICONTROL Exclusions]** タブをクリックします。

1. （オプション）特定のオーディエンス除外を含めるようにリストをフィルタリングします。

1. 削除する各[!DNL Google Ads]除外の横にあるチェックボックスをオンにします。 選択範囲に別の広告ネットワークからの除外を含めないでください。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスの管理](audience-manage.md)
>* [&#x200B; キャンペーンと広告グループのオーディエンスターゲットの管理](audience-targets-manage.md)
