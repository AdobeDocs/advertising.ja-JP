---
title: キャンペーン管理ビューでのデータのカスタマイズについて
description: キャンペーンデータビューでカスタマイズできるデータの種類について説明します。
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 2f170883b2876ea4a7b39e814df598d337f7ca07
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---
# キャンペーン管理ビューでのデータのカスタマイズについて

ほとんどのキャンペーンデータビューでは、データテーブル内に表示されるデータをカスタマイズできます。 データは、次の方法でカスタマイズできます。

* [特定のエンティティ表示（[!UICONTROL Campaigns]など）のデフォルトビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit)全体の設定を編集して、特定の列の順序、フィルター、日付範囲、アトリビューションルールなどを含め、設定を一時的に適用するか、保存します。 [追加のカスタムビューを作成](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view)、[既存のビューを複製](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone)および[いずれかのビューを適用](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view)することもできます。

* [&#x200B; ツールバーの[!UICONTROL Custom Columns] コントロールを使用して、列とその並べ替え順序](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md)を変更します。 新しいUIで、ツールバーが狭すぎてコントロールが表示されない場合は、**[!UICONTROL Actions]>[!UICONTROL Custom Columns]**&#x200B;をクリックします。 また、ビューの任意の列見出しから[列だけを変更することもできます](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)。

* （レガシーユーザーインターフェイスのみ） [左側のナビゲーションパネル &#x200B;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md)から、次の操作を実行できます。

  * 広告ネットワーク別にエンティティを参照または検索し、エンティティのステータスと、アカウント、キャンペーン、広告グループまたは広告セットのステータスでフィルタリングします。 パネル内の任意のエンティティまたはエンティティグループをクリックして、子エンティティのビューを読み込みます（例えば、キャンペーン名をクリックして子広告グループを表示します）。

  * ポートフォリオまたはポートフォリオグループ別にキャンペーンを参照または検索し、エンティティのステータスとポートフォリオグループ、ポートフォリオ、キャンペーンのステータスでフィルタリングします。 パネルで任意のポートフォリオグループ、ポートフォリオ、またはキャンペーンをクリックして、現在のエンティティビュー内のポートフォリオグループ、ポートフォリオ、またはキャンペーンのデータを読み込みます。

  * デフォルトビューへのアクセス、編集、リセット、カスタムビューへのアクセス、編集、削除を行います。 任意のビュー名をクリックすると、適切なビューが読み込まれます。

* 使用可能なデータ列にフィルターを適用して、現在のタブに表示されるデータを変更します。 フィルター[は、列見出し](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)または[からツールバー](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)のボタンから作成できます。 キャンペーン管理ビューの場合、子エンティティを開いたときに、フィルターは適用可能な状態に保たれます。 例えば、\> 100 クリックのキャンペーンを表示し、そのキャンペーン内で広告グループを開くと、\> 100 クリックの広告グループのみが表示されます。

* [特定の日付範囲を保存していないすべてのデフォルトビューとカスタムビューで使用されている日付範囲](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md)を変更します。

* [特定の列の値に従ってデータ &#x200B;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md)を並べ替えます。

* 任意のページの下部に25行、50行、100行、（レガシーユーザーインターフェイスのみ） 200行、または（レガシーユーザーインターフェイスのみ） [!UICONTROL Continuous Scroll]を表示するかどうかを制御します。

<!--

## (New UI) Data table tools {#grid-controls-new-ui}

In applicable management views, the toolbar includes the following controls:

* On the left, the [!UICONTROL Filter] control appears before grid search. Where supported, the [!UICONTROL Conversion based on] selector follows search and lets you select [!UICONTROL Click Date] or [!UICONTROL Transaction Date].

* On the right, operational actions, such as [!UICONTROL Reports], appear alongside view and display controls. The available controls depend on the view and your permissions.

* When the available width is reduced, controls move into the [!UICONTROL Actions] menu. This can happen when you narrow the window or open the AI Assistant panel. If a control isn't visible in the toolbar, look for it in [!UICONTROL Actions]. In wider layouts, controls remain inline.

* Within [!UICONTROL Actions], a horizontal divider separates operational actions from view and display controls, such as the current view, [!UICONTROL Custom Columns], [!UICONTROL Compressed Mode], and [!UICONTROL Charts], where available.

* The primary create button remains outside [!UICONTROL Actions].

The [!UICONTROL Refresh] icon is beside the page title in applicable views. The date range control is in the page header. For instructions on comparing two date ranges and changing the comparison format, see "[Filter data by date range](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)."

### Change the grid density

* Where available, click **[!UICONTROL Compressed Mode]** in the toolbar or **[!UICONTROL Actions]** menu to turn compact grid spacing on or off.

  The toolbar button is selected when compressed mode is on. In [!UICONTROL Actions], a switch indicates the current state.

### Show or hide charts

* Where available, click **[!UICONTROL Charts]** in the toolbar or **[!UICONTROL Actions]** menu.

  The toolbar button is selected when charts are shown. In [!UICONTROL Actions], a switch indicates whether charts are shown. Click the control again to hide the charts.

-->
