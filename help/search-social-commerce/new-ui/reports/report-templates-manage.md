---
title: （新しいUI）レポートテンプレートの管理
description: スケジュール済みレポートとオンデマンド済みレポートの再利用可能なレポートテンプレートを作成、表示、編集、削除する方法について説明します。
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# （新しいUI）レポートテンプレートの管理

レポートテンプレートは、ほとんどのレポートを生成するときに再利用できる、事前定義されたレポートレイアウトです。 テンプレートを使用すると、デフォルト以外のパラメーターを使用したり、同じレポートのバリエーションを実行したり、通常のスケジュールに従って同じレポートを実行したりする場合の時間を節約できます。 保存されたテンプレートは、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;の&#x200B;**[!UICONTROL Templates]** タブで利用できます。

一度に最大100個のテンプレートを管理できます。

データを表示するには、[!UICONTROL View Scheduled Reports]権限が必要です。 テンプレートの作成、複製、編集、実行、削除、および行データのコピーには、[!UICONTROL Edit Scheduled Reports]権限が必要です。 編集できるのは、作成したテンプレートのみです。

## 使用可能なアクション

* [新しいテンプレートとして、または既存のテンプレートに基づいて、レポートテンプレート &#x200B;](#template-create)を作成します。

* [元の](#template-view)を変更せずにレポートテンプレートの設定を表示します。

* [&#x200B; レポートテンプレート &#x200B;](#template-edit)を編集し、そのスケジュールを表示します。

* [指定したテンプレートに対してオンデマンドでレポートを実行](#template-run)。

* [&#x200B; レポートテンプレートを削除](#template-delete)。

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)。

## レポートテンプレートの作成 {#template-create}

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 次のいずれかの操作を行います。

   * 新しいテンプレートを作成するには、**[!UICONTROL Create Template]**&#x200B;をクリックします。 **[!UICONTROL Create a New Template]** パネルで、レポートカテゴリとレポートタイプを選択し、**[!UICONTROL Proceed]**&#x200B;をクリックします。

   * 既存のテンプレートに基づいてテンプレートを作成するには、テンプレート行の上にカーソルを置き、![&#x200B; テンプレート設定](/help/search-social-commerce/assets/settings-new.png " テンプレート設定") **[!UICONTROL Template Settings]**&#x200B;または&#x200B;**[!UICONTROL ...]>[!UICONTROL Duplicate]**&#x200B;のいずれかをクリックします。

1. テンプレートの一意の&#x200B;**[!UICONTROL Report Name]**&#x200B;を入力し、**[!UICONTROL Save as Template]**&#x200B;が有効になっていることを確認します。

   設定は、**[!UICONTROL Create Template]**&#x200B;で開始すると、デフォルトで有効になります。 これを無効にすると、最終的なアクションは&#x200B;**[!UICONTROL Run Report]**&#x200B;に変わり、テンプレートを保存する代わりにレポートが生成されます。

1. [基本レポートおよび詳細レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)、[&#x200B; アシストレポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md)、[&#x200B; モデル精度レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md)、または[特殊レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md)のレポート設定を構成します。

   **[!UICONTROL Next]**&#x200B;をクリックして、設定セクション間を移動します。

1. （オプション）レポートを自動的に生成するには、**[!UICONTROL Frequency]**&#x200B;と&#x200B;**[!UICONTROL Scheduling]**&#x200B;の配信設定を設定します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

レポート設定を送信する前に&#x200B;**[!UICONTROL Save as Template]**&#x200B;を有効にすることで、[最新レポート タブからレポートを作成する](/help/search-social-commerce/new-ui/reports/management/report-manage.md)際にテンプレートを保存することもできます。

## レポートテンプレートの設定の表示 {#template-view}

元のテンプレートを変更せずに設定を調べるには、複製を開きます。 これには[!UICONTROL Edit Scheduled Reports]権限が必要です。 複製を開いても、新しいテンプレートは保存されません。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレート行の上にカーソルを置き、![&#x200B; テンプレート設定](/help/search-social-commerce/assets/settings-new.png " テンプレート設定")**[!UICONTROL Template Settings]**&#x200B;をクリックします。

1. レポート設定を確認します。

1. 完了したら、**[!UICONTROL Cancel]**&#x200B;をクリックします。 設定を破棄するよう求められた場合は、**[!UICONTROL Discard]**&#x200B;をクリックします。

代わりにコピーを保存するには、[&#x200B; テンプレート作成手順](#template-create)に従います。

## レポートテンプレートの編集 {#template-edit}

作成したテンプレートの設定とスケジュールを変更できます。 変更は、今後テンプレートから生成されるレポートに適用されます。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 作成した1つのテンプレートの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

   複数のテンプレートが選択されているか、選択したテンプレートが別のユーザーによって作成されている場合、[!UICONTROL Edit]は使用できません。

1. レポート設定を変更します。 スケジュールを追加、変更、または削除するには、**[!UICONTROL Scheduling]**&#x200B;で&#x200B;**[!UICONTROL Frequency]**&#x200B;を編集します。

   スケジュールされたレポートの日単位、週単位、月単位の頻度を選択します。 定期的なスケジュールを削除するには、**[!UICONTROL Now]**&#x200B;を選択します。

   **[!UICONTROL Save as Template]**&#x200B;と&#x200B;**[!UICONTROL Type]**&#x200B;は、既存のテンプレートを編集する際に読み取り専用です。 [!UICONTROL Save as Template]を再度有効にする必要はありません。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 指定したテンプレートに対してオンデマンドでレポートを実行します {#template-run}

1つ以上のテンプレートに対するレポートは、いつでも実行できます。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 次のいずれかの操作を行います。

   * （単一テンプレートを実行するには）:

     1. テンプレート行のメニューを開き、**[!UICONTROL Run]**&#x200B;を選択します。

     1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

   * （1つ以上のテンプレートを実行するには）:

     1. 実行する各テンプレートの横にあるチェックボックスをオンにします。

     1. 一括操作ツールバーで、**[!UICONTROL Run]**&#x200B;をクリックします。

     1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

**[!UICONTROL Run Report]**&#x200B;をクリックしてから&#x200B;**[!UICONTROL Confirm]**&#x200B;をクリックすると、テンプレートを編集中に実行することもできます。 最初に変更を保存します。このアクションは、保存されたテンプレートを実行します。

## レポートテンプレートの削除 {#template-delete}

使用可能な任意のレポートテンプレートを削除できます。 スケジュールを含むテンプレートを削除しても、そのレポートは今後生成されません。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 次のいずれかの操作を行います。

   * （単一のテンプレートを削除するには）:

     1. テンプレート行のメニューを開き、**[!UICONTROL Delete]**&#x200B;を選択します。

     1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

   * （1つ以上のテンプレートを削除するには）:

     1. 削除する各テンプレートの横にあるチェックボックスをオンにします。

     1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

     1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。
