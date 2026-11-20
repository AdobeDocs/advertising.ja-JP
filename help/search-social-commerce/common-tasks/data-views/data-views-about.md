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
source-git-commit: 972ed9c0662fc3b74bc5c3597f010170fbce69d7
workflow-type: tm+mt
source-wordcount: '672'
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

## （新しいUI） データテーブルコントロール {#data-table-tools-new-ui}

データテーブルの上にあるツールバーを使用して、データを管理し、表示方法を変更します。 使用可能なツールは、ビューと権限によって異なります。

ツールバーの幅が狭すぎてツールが表示されない場合は、**[!UICONTROL Actions]** メニューでツールバーを探します。

利用可能な場合は、次のことができます。

* [!UICONTROL Conversion based on]から&#x200B;*[!UICONTROL Click Date]*&#x200B;または&#x200B;*[!UICONTROL Transaction Date]*&#x200B;を選択して、コンバージョンデータのレポート方法を制御します。

* 2つの期間のパフォーマンスを比較し、違いを表示する方法を選択します。 「[日付範囲](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)でデータをフィルタリング」を参照してください。

* ツールバーまたは&#x200B;**[!UICONTROL Actions]** メニューの&#x200B;**[!UICONTROL Compressed Mode]**&#x200B;を使用して、コンパクト表の間隔をオンまたはオフにします。

  圧縮モードがオンの場合、ツールバーボタンが選択されます。 [!UICONTROL Actions]では、スイッチは現在の状態を示します。

* ツールバーまたは&#x200B;**[!UICONTROL Actions]** メニューの&#x200B;**[!UICONTROL Charts]**&#x200B;を使用して、グラフを表示または非表示にします。

  グラフが表示されているときにツールバーボタンが選択されます。 [!UICONTROL Actions]では、グラフが表示されているかどうかをスイッチで示します。 コントロールをもう一度クリックして、グラフを非表示にします。

## （新しいUI）列幅とテーブル値 {#column-widths-values-new-ui}

キャンペーンデータテーブルの場合：

* 列見出しの境界をドラッグして、列のサイズを変更します。 また、対象となる[&#x200B; ロック済み列](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-lock-unlock.md)のサイズを、最初にロック解除せずに変更することもできます。 最小幅は、値を読みやすくするのに役立ちます。 一部のアイコン列とアクション列の幅は固定されており、サイズを変更できません。

* 切り捨てられたエンティティ名の上にカーソルを置くと、フルネームが表示されます。

* 名前がリンクされているエンティティの詳細を開くには、名前が強調表示されるまで&#x200B;**Tab**&#x200B;を押し、次に&#x200B;**Enter**&#x200B;を押します。

* 末尾ダッシュ（ – ）は、値が見つからないか、NULLであるか、適用できない値であることを示します。 ゼロ値とfalse値は表示されたままです。
