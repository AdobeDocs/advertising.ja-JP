---
title: カスタムシミュレーションの実行または再実行
description: ポートフォリオのカスタムシミュレーションを実行または再実行する方法について説明します。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# カスタムシミュレーションの実行または再実行

*Beta機能*

[最適化されたポートフォリオまたはアクティブな](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status) ポートフォリオのカスタムシミュレーションを生成できます。 リストでシミュレーションを選択して、同じポートフォリオに対して新しいシミュレーションを実行したり、既存の設定でシミュレーションを再実行したりすることもできます。

カスタムシミュレーションを作成するには[!UICONTROL Create Simulation]権限が必要です。 ポートフォリオを選択するには[!UICONTROL View Portfolios]権限が必要です。

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin]および[!UICONTROL Account Manager]人のユーザーは、他のユーザーが作成したシミュレーションを表示できます。 他のすべてのユーザーは、作成したカスタムシミュレーションのみを表示できます。

## 新しいシミュレーションの作成 {#simulation-create}

[!UICONTROL Simulations] ビューから開始するか、[&#x200B; カスタムシミュレーションを[!UICONTROL Portfolios] ビュー](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation)から実行できます。

1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

1. 選択したシミュレーション行をすべて消去し、**[!UICONTROL Run Simulation]**&#x200B;をクリックします。

1. ポートフォリオを選択します。

   1. **[!UICONTROL Select Portfolio]**&#x200B;をクリックします。

   1. ポートフォリオを選択します。

      特定のテキスト文字列を含むポートフォリオを検索するには、検索フィールドにテキスト文字列を入力します。 値では大文字と小文字は区別されません。

   1. **[!UICONTROL Proceed]**&#x200B;をクリックします。

1. [&#x200B; カスタムシミュレーション設定](#custom-simulation-settings)を指定します。

   1. （オプション）シミュレーションに使用するポートフォリオを変更するには、ポートフォリオ名の横にある&#x200B;**[!UICONTROL Change Portfolio]**&#x200B;をクリックし、ポートフォリオを選択してから&#x200B;**[!UICONTROL Proceed]**&#x200B;をクリックします。

   1. 「[!UICONTROL Basic Settings]」タブ：

      1. 一意の&#x200B;**[!UICONTROL Simulation Name]**&#x200B;を入力してください。

      1. （オプション）シミュレーションの基本パラメーターを変更します。

   1. （オプション）「[!UICONTROL Advanced Settings]」タブで、シミュレーションの詳細パラメーターを変更します。

   選択したポートフォリオの既存のパラメーターは、デフォルトで指定されます。 値を変更すると、ポートフォリオの既存のパラメーターを変更せずに異なるパラメーターが生成する結果が表示されます。

1. **[!UICONTROL Next]**&#x200B;をクリックします。

1. 設定を確認し、必要に応じて設定を編集します。

1. **[!UICONTROL Submit & Run]**&#x200B;をクリックします。

リクエストが送信され、[!UICONTROL Simulations] ビューが開きます。 シミュレーションレポートが使用可能になると、指定した他の電子メール受信者は、ダウンロードリンク付きの通知を受け取ります。 [!UICONTROL Simulations] ビュー[&#128279;](simulation-download.md)からシミュレーションを ダウンロードすることもできます。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 既存の設定でシミュレーションを再実行する {#rerun-a-simulation-with-the-existing-settings}

既存の設定を使用して、一度に最大10個のシミュレーションを再実行できます。 ステータスが[!UICONTROL Queued]または[!UICONTROL In Progress]のシミュレーションは再実行できません。 選択範囲にこれらのシミュレーションが含まれている場合、それらのシミュレーションはスキップされ、残りのシミュレーションが送信されます。

1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

1. 再実行するシミュレーションの横にあるチェックボックスをオンにします。

1. データテーブルの上のツールバーまたはバルクアクションツールバーで、**[!UICONTROL Re-Run Simulation]**&#x200B;をクリックします。

リクエストが送信され、ビューが更新されます。

## リスト内のポートフォリオの新しいシミュレーションを実行します {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

[!UICONTROL Run Simulation]をクリックする前にシミュレーションを選択すると、新しいシミュレーションのポートフォリオが選択されます。 フォームは、選択したシミュレーションの設定ではなく、ポートフォリオの現在の設定を使用します。 このアクションでは、既存のシミュレーションは編集されません。

1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

1. 使用するポートフォリオのシミュレーションの横にあるチェックボックスをオンにします。

   複数のシミュレーションを選択する場合は、すべて同じポートフォリオを使用する必要があります。 ポートフォリオは、アクティブまたは最適化されている必要があります。

1. データテーブルの上で、**[!UICONTROL Run Simulation]**&#x200B;をクリックします。

1. 一意の&#x200B;**[!UICONTROL Simulation Name]**&#x200B;を含む[&#x200B; カスタムシミュレーション設定](#custom-simulation-settings)を指定します。 必要に応じて、**[!UICONTROL Basic Settings]** タブと&#x200B;**[!UICONTROL Advanced Settings]** タブのパラメーターを変更します。

1. **[!UICONTROL Next]**&#x200B;をクリックします。

1. 設定を確認し、必要に応じて設定を編集します。

1. **[!UICONTROL Submit & Run]**&#x200B;をクリックします。

リクエストが送信され、[!UICONTROL Simulations] ビューが開きます。 シミュレーションが正常に完了したら、[&#x200B; ダウンロードできます](simulation-download.md)。

## カスタムシミュレーション設定 {#custom-simulation-settings}

カスタムシミュレーション設定について詳しくは、Search, Social, &amp; Commerce内から入手できるOptimization Guideを参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; シミュレーションについて](simulation-about.md)
>* [&#x200B; シミュレーションの詳細を表示](simulation-view.md)
>* [&#x200B; シミュレーションのダウンロード &#x200B;](simulation-download.md)
