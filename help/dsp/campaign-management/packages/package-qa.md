---
title: バルクシートを使用したパッケージ設定のレビューと編集
description: スプレッドシートを使用して主要なパッケージ設定を一括でレビューおよび編集する方法を説明します。
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# バルクシートを使用したパッケージ設定のレビューと編集

1 つ以上のパッケージの設定を XLSX （[!DNL Microsoft Excel] スプレッドシート）形式でダウンロードして確認できます。 *bulksheet* ファイルには、フライト情報を含む別のタブが含まれています。

複数の設定を一度に更新するには、次のいずれかを実行します。

* フィールドの選択を変更し、ファイルを保存して、編集したバルクシートファイルをDSPにアップロードして戻します。

* キャンペーンに追加のパッケージ、プレースメントまたは広告を変更するには、キャンペーンのバルクシートをダウンロードします。 更新した設定を入力またはファイルに貼り付け、ファイルをアップロードして変更します。 手順については、「[ バルクシートを使用した Campaign コンポーネント設定の確認と編集 ](/help/dsp/campaign-management/campaign-components-review-edit.md) を参照してください。

編集可能なフィールドには、通常は編集可能なほとんどの設定が含まれています。

>[!TIP]
>
>1 つ以上のパッケージの複数のフィールドをすばやく編集するには、「[ パッケージの編集 ](/help/dsp/campaign-management/packages/package-edit.md) を参照してください。

## キャンペーン内のすべてのパッケージの設定をダウンロード

キャンペーン内のすべてのパッケージの設定をダウンロードする場合、バルクシートにはパッケージ設定とフライト情報の別々のタブが含まれます。 オプションで、パッケージに関連付けられるプレースメントおよび広告の設定を含めることができます。プレースメントおよび広告設定用の追加のタブも含まれます。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * キャンペーンの横で、**[!UICONTROL ...]**/**[!UICONTROL Download Bulksheet]** をクリックします。

   * キャンペーン名をクリックします。 右上で、**[!UICONTROL ...]**/**[!UICONTROL Download Bulksheet]** をクリックします。

1. [!UICONTROL Bulksheet Download] ダイアログボックスで、ダウンロードしたファイルから設定を除外する Campaign コンポーネントの選択を解除し、「**[!UICONTROL Download]**」をクリックします。

デフォルトでは、パッケージに関連付けられているすべてのプレースメントと広告の設定が選択されます。

通知メッセージは、ファイルのダウンロードが可能なタイミングを示します。

1. ファイルをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

     ファイルはブラウザーのダウンロードフォルダーに保存されます。<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     設定を編集するには、ファイルを直接編集してから、変更内容をアップロードします。 編集可能な列はすべて青でハイライト表示されます。

## 特定のパッケージのダウンロード設定

特定のパッケージの設定をダウンロードする場合、バルクシート ファイルにはパッケージ設定とフライト情報のタブが別々に含まれ、ファイルは編集可能です。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Packages]** をクリックします。

1. 設定をダウンロードするパッケージのチェックボックスをオンにします。

1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Download Bulksheet]** をクリックします。

   バルクシートファイルをダウンロードできるときに通知メッセージが表示されます。

1. バルクシートをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

     ファイルはブラウザーのダウンロードフォルダーに保存されます。 含まれる列のリストについては、[ ダウンロードまたはアップロードされたバルクシートのプレースメント列 ](#qa-sheet-columns)」を参照してください。

     設定を編集するには、ファイルを直接編集してから、変更内容をアップロードします。 編集可能な列はすべて青でハイライト表示されます。 フィールドに正しい形式を使用するには、関連するパッケージ設定またはプレースメント設定から値を選択してコピーします。 日分割、カスタム目標、コンバージョン指標など、一部のターゲット設定では、設定内でコピーオプションを使用できます。

## パッケージ設定を含むバルクシートのアップロード {#upload-bulksheet-package}

パッケージの設定（パッケージに関連付けられたプレースメントや広告など）をバルクシートファイルにアップロードできます。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * 親キャンペーンの横で、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

   * キャンペーン名をクリックします。 右上で、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

     このオプションは、「[!UICONTROL Packages]」、「[!UICONTROL Placements]」または「[!UICONTROL Ads]」タブから使用できます。

   * サブメニューで「**[!UICONTROL Packages]**」をクリックし、パッケージのチェックボックスを選択します。 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

1. [!UICONTROL Upload Bulksheet] ダイアログで、次の手順を実行します。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. 「**[!UICONTROL Upload]**」をクリックします。

1. （オプション）更新が処理されたことを確認するには、上部のメニューバーの右側にある ![ ジョブ ](/help/dsp/assets/downloads.png) をクリックします。

設定の更新に失敗した場合、色分けしたバルクシートエラーファイルをダウンロードすると、保存された設定（行）と失敗した設定（失敗した行）と、失敗した各設定の理由を表示できます。 その後、同じファイル内の問題に対処し、もう一度アップロードして、修正された情報を処理できます。

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [ バルクシートを使用した Campaign コンポーネント設定のレビューと編集 ](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [ パッケージの編集 ](/help/dsp/campaign-management/packages/package-edit.md)
>* [ パッケージ設定 ](/help/dsp/campaign-management/packages/package-settings.md)
