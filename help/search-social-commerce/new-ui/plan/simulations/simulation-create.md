---
title: カスタムシミュレーションの実行または再実行
description: ポートフォリオのカスタムシミュレーションを実行または再実行する方法について説明します。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2504e6a4eebeab74352606a89a5012ab96c89c47
workflow-type: tm+mt
source-wordcount: 505
ht-degree: 0%

---

# カスタムシミュレーションの実行または再実行

*Beta機能*

[最適化されたポートフォリオまたはアクティブな](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) ポートフォリオのカスタムシミュレーションを生成できます。 また、既存のシミュレーションのパラメーターを変更してシミュレーションを再生成したり、既存のパラメーターを使用して既存のシミュレーションを再実行したりすることもできます。

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin]および[!UICONTROL Account Manager]人のユーザーは、他のユーザーが作成したシミュレーションを表示できます。 他のすべてのユーザーは、作成したカスタムシミュレーションのみを表示できます。

## 新しいシミュレーションの作成

1. 次のいずれかの操作を行います。

* [!UICONTROL Simulations] ビューから：

   1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

   1. データテーブルの上で、**[!UICONTROL Run Simulation]**&#x200B;をクリックします。

   1. ポートフォリオを選択します。

      1. **[!UICONTROL Select Portfolio]**&#x200B;をクリックします。

      1. ポートフォリオを選択します。

         特定のテキスト文字列を含むポートフォリオを検索するには、検索フィールドにテキスト文字列を入力します。 値では大文字と小文字は区別されません。

      1. **[!UICONTROL Proceed]**&#x200B;をクリックします。

* [!UICONTROL Portfolios] ビューから：

   1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Portfolios]**&#x200B;をクリックします。

   1. ポートフォリオ行の上にカーソルを置きます。 ポートフォリオ名の横で、**[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**&#x200B;をクリックします。

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

シミュレーションレポートが使用可能になると、ユーザーと指定されたその他のメール受信者は、1つのワークブック（XLSX ファイル）を含むZIP ファイルにデータをダウンロードするためのリンクを含む通知を受け取ります。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 既存のシミュレーションの設定を編集して再実行する

1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

1. 再生成するシミュレーションの横にあるチェックボックスをオンにします。

1. データテーブルの上で、**[!UICONTROL Run Simulation]**&#x200B;をクリックします。

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

シミュレーションレポートが使用可能になると、ユーザーと指定されたその他のメール受信者は、1つのワークブック（XLSX ファイル）を含むZIP ファイルにデータをダウンロードするためのリンクを含む通知を受け取ります。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 既存の設定でシミュレーションを再実行する

現在キューに入っていないシミュレーションを再実行できます。

1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

1. 再実行するシミュレーションの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、![再実行](/help/search-social-commerce/assets/rerun.png "再実行")をクリックします。

## カスタムシミュレーション設定 {#custom-simulation-settings}

カスタムシミュレーション設定について詳しくは、Search, Social, &amp; Commerce内から入手できるOptimization Guideを参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; シミュレーションについて](simulation-about.md)
>* [&#x200B; シミュレーションの詳細を表示](simulation-view.md)
>* [&#x200B; シミュレーションのダウンロード &#x200B;](simulation-download.md)
