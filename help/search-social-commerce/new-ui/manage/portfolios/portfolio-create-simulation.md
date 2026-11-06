---
title: '[!UICONTROL Portfolios] ビューからシミュレーションを実行してダウンロードします'
description: カスタムシミュレーションを実行し、ポートフォリオビューから週別シミュレーションをダウンロードする方法を説明します。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# [!UICONTROL Portfolios] ビューからシミュレーションを実行してダウンロードします

*Beta機能*

単一の[最適化またはアクティブな](portfolio-about.md#portfolio-status) ポートフォリオに対してカスタムシミュレーションを実行し、最大100 ポートフォリオの自動毎週シミュレーションを[!UICONTROL Portfolios] ビューからダウンロードできます。

カスタムシミュレーションを実行するには、[!UICONTROL Create Simulation]権限が必要です。 週次シミュレーションをダウンロードするには、[!UICONTROL View Simulation]権限が必要です。

>[!NOTE]
>
>[!UICONTROL Simulations] ビュー](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)からカスタムシミュレーションを[作成または再実行することもできます。

## カスタムシミュレーションの実行 {#run-simulation}

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Portfolios]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * ポートフォリオ行の上にカーソルを置きます。 ポートフォリオ名の横で、**[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**&#x200B;をクリックします。

   * ポートフォリオの横にあるチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL More]>[!UICONTROL Run Simulation]**&#x200B;をクリックします。

1. [ カスタムシミュレーション設定](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md#custom-simulation-settings)を指定します。

   1. 「**[!UICONTROL Basic Settings]**」タブで、一意の&#x200B;**[!UICONTROL Simulation Name]**&#x200B;を入力し、必要に応じて基本パラメーターを変更します。

   1. （オプション）「**[!UICONTROL Advanced Settings]**」タブで、詳細パラメーターを変更します。

   選択したポートフォリオの現在の設定がデフォルトとして使用されます。 シミュレーション設定を変更しても、ポートフォリオの設定は変更されません。

1. **[!UICONTROL Next]**&#x200B;をクリックします。

1. 設定を確認し、必要に応じて変更します。

1. **[!UICONTROL Submit & Run]**&#x200B;をクリックします。

リクエストが送信され、[!UICONTROL Simulations] ビューが開きます。 シミュレーションが正常に完了したら、[ ダウンロードできます](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)。

## 週次シミュレーションのダウンロード {#download-simulations}

1回の実行日の週次シミュレーションを[!DNL Microsoft Excel] ワークブック （XLSX ファイル）としてダウンロードできます。 その日付の利用可能なシミュレーションレポートを含む、アクティブで最適化されたポートフォリオのみが含まれます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Portfolios]**&#x200B;をクリックします。

1. 毎週のシミュレーションをダウンロードする各ポートフォリオの横にあるチェックボックスをオンにします。 最大100個のポートフォリオを選択してください。

1. 一括操作ツールバーで、**[!UICONTROL More]>[!UICONTROL Download Simulation]**&#x200B;をクリックします。

1. **[!UICONTROL Weekly Simulation]**&#x200B;で、実行日を選択します。

   デフォルトでは、最新の使用可能な日付が選択されています。 選択した一部のポートフォリオでレポートが使用できない場合は、除外されるポートフォリオ数をダイアログに表示します。 必要に応じて別の日付を選択します。 選択したポートフォリオにその日付の使用可能なシミュレーションがない場合、レポートをダウンロードできません。

1. 使用可能なレポートを含むポートフォリオの数がラベルに含まれているダウンロードボタンをクリックします（例：**[!UICONTROL Download 2 portfolios]**）。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。 完了メッセージは、ポートフォリオがいくつ含まれているかを示します。

カスタムシミュレーションをダウンロードするか、毎週の個別のシミュレーションを選択するには、[[!UICONTROL Simulations] ビュー](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)を使用します。

>[!MORELIKETHIS]
>
>* [ （新しいUI） ポートフォリオパフォーマンスの詳細を表示](portfolio-details.md)
>* [ ポートフォリオについて](portfolio-about.md)
>* [ カスタムシミュレーションの実行または再実行](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [ シミュレーションのダウンロード ](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
