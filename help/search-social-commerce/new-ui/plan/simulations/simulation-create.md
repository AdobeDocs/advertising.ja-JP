---
title: カスタムシミュレーションの実行または再実行
description: ポートフォリオのカスタムシミュレーションを実行または再実行する方法を説明します。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# カスタムシミュレーションの実行または再実行

*Beta機能*

カスタムシミュレーションは、（最適化またはアクティブ [&#x200B; ポートフォリオに対して生成 &#x200B;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) きます。 また、既存のシミュレーションのパラメータを変更してシミュレーションを再生成するか、既存のパラメータを使用して既存のシミュレーションを再実行することもできます。

[!UICONTROL Admin] および [!UICONTROL Account Manager] ユーザーは、他のユーザーが作成したシミュレーションを表示できます。 他のすべてのユーザーには、作成したカスタムシミュレーションのみが表示されます。

## 新しいシミュレーションの作成

1. メインメニューで、**[!UICONTROL Plan]/[!UICONTROL Simulations]** をクリックします。

1. データ テーブルの上にある [**[!UICONTROL Run Simulation]**] をクリックします。

1. ポートフォリオを選択します。

   1. 「**[!UICONTROL Select Portfolio]**」をクリックします。

   1. ポートフォリオを選択します。

      特定のテキスト文字列を含むポートフォリオを検索するには、検索フィールドにテキスト文字列を入力します。 値では大文字と小文字が区別されません。

   1. 「**[!UICONTROL Proceed]**」をクリックします。

1. [&#x200B; カスタム シミュレーション設定 &#x200B;](#custom-simulation-settings) を指定します。

   1. （オプション）シミュレーションに使用するポートフォリオを変更するには、ポートフォリオ名の横にある [**[!UICONTROL Change Portfolio]**] をクリックし、ポートフォリオを選択して、[**[!UICONTROL Proceed]**] をクリックします。

   1. 「[!UICONTROL Basic Settings]」タブで、次の操作を行います。

      1. 一意の **[!UICONTROL Simulation Name]** を入力します。

      1. （任意）シミュレーションの基本パラメーターを変更します。

   1. （オプション）「[!UICONTROL Advanced Settings]」タブで、シミュレーションの詳細設定パラメーターを変更します。

   選択したポートフォリオの既存のパラメーターが、デフォルトで指定されます。 値を変更すると、ポートフォリオの既存のパラメーターを変更せずに、様々なパラメーターで生成される結果が表示されます。

1. 「**[!UICONTROL Next]**」をクリックします。

1. 設定を確認し、必要に応じて設定を編集します。

1. 「**[!UICONTROL Submit & Run]**」をクリックします。

シミュレーションレポートが使用可能になると、指定された他のメール受信者は、1 つのワークブック（XLSX ファイル）を含んだ ZIP ファイルにデータをダウンロードするためのリンクが付いた通知を受け取ります。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 既存のシミュレーションの設定を編集し、再実行します

1. メインメニューで、**[!UICONTROL Plan]/[!UICONTROL Simulations]** をクリックします。

1. 再生成するシミュレーションの横にあるチェック ボックスをオンにします。

1. データ テーブルの上にある [**[!UICONTROL Run Simulation]**] をクリックします。

1. [&#x200B; カスタム シミュレーション設定 &#x200B;](#custom-simulation-settings) を指定します。

   1. （オプション）シミュレーションに使用するポートフォリオを変更するには、ポートフォリオ名の横にある [**[!UICONTROL Change Portfolio]**] をクリックし、ポートフォリオを選択して、[**[!UICONTROL Proceed]**] をクリックします。

   1. 「[!UICONTROL Basic Settings]」タブで、次の操作を行います。

      1. 一意の **[!UICONTROL Simulation Name]** を入力します。

      1. （任意）シミュレーションの基本パラメーターを変更します。

   1. （オプション）「[!UICONTROL Advanced Settings]」タブで、シミュレーションの詳細設定パラメーターを変更します。

   選択したポートフォリオの既存のパラメーターが、デフォルトで指定されます。 値を変更すると、ポートフォリオの既存のパラメーターを変更せずに、様々なパラメーターで生成される結果が表示されます。

1. 「**[!UICONTROL Next]**」をクリックします。

1. 設定を確認し、必要に応じて設定を編集します。

1. 「**[!UICONTROL Submit & Run]**」をクリックします。

シミュレーションレポートが使用可能になると、指定された他のメール受信者は、1 つのワークブック（XLSX ファイル）を含んだ ZIP ファイルにデータをダウンロードするためのリンクが付いた通知を受け取ります。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 既存の設定でシミュレーションを再実行します

現在キューに入っていないシミュレーションを再実行できます。

1. メインメニューで、**[!UICONTROL Plan]/[!UICONTROL Simulations]** をクリックします。

1. 再実行するシミュレーションの横にあるチェック ボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[![&#x200B; 再実行 &#x200B;](/help/search-social-commerce/assets/rerun.png " 再実行 ")] をクリックします。

## カスタムシミュレーション設定 {#custom-simulation-settings}

カスタムシミュレーション設定について詳しくは、検索、ソーシャル、Commerce内から利用できる最適化ガイドを参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; シミュレーションについて &#x200B;](simulation-about.md)
>* [&#x200B; シミュレーションのダウンロード &#x200B;](simulation-download.md)
