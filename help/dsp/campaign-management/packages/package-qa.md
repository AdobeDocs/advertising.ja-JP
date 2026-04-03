---
title: バルクシートを使用したパッケージ設定の確認と編集
description: スプレッドシートを使用して、主要なパッケージ設定を一括で確認および編集する方法について説明します。
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
TQID: https://experienceleague.adobe.com/daZta9ZI28ZyskwnM9RvJO3yGhFCi-DFKapeq5rtuNg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 715
ht-degree: 0%

---

# バルクシートを使用したパッケージ設定の確認と編集

レビュー用に、XLSX （[!DNL Microsoft Excel] スプレッドシート）形式の1つ以上のパッケージの設定をダウンロードできます。 *バルクシート* ファイルには、フライト情報を含む別のタブが含まれています。

複数の設定を一度に更新するには、次のいずれかの操作を行います。

* フィールドを選択し、ファイルを保存し、編集したバルクシートファイルをDSPにアップロードします。

* キャンペーン内の追加のパッケージ、プレースメントまたは広告に変更を加えるには、キャンペーンのバルクシートをダウンロードします。 更新された設定をファイルに入力または貼り付け、ファイルをアップロードして変更を加えます。 手順については、「[ バルクシートを使用したキャンペーンコンポーネント設定の確認と編集](/help/dsp/campaign-management/campaign-components-review-edit.md)」を参照してください。

編集可能なフィールドには、通常は編集可能なほとんどの設定が含まれています。

>[!TIP]
>
>1つ以上のパッケージのフィールドをすばやく編集するには、「[ パッケージを編集](/help/dsp/campaign-management/packages/package-edit.md)」を参照してください。

## キャンペーン内のすべてのパッケージの設定のダウンロード

キャンペーン内のすべてのパッケージの設定をダウンロードすると、バルクシートには、パッケージ設定とフライト情報のタブが個別に含まれます。 オプションで、パッケージに関連付けられているプレースメントと広告の設定を含めることができます。プレースメントと広告の設定には、追加のタブが含まれます。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * キャンペーンの横で、**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**&#x200B;をクリックします。

   * キャンペーン名をクリックします。 右上で、**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**&#x200B;をクリックします。

1. [!UICONTROL Bulksheet Download] ダイアログボックスで、ダウンロードしたファイルから設定を除外するキャンペーンコンポーネントの選択を解除し、**[!UICONTROL Download]**&#x200B;をクリックします。

デフォルトでは、パッケージに関連付けられたすべてのプレースメントと広告の設定が選択されています。

ファイルのダウンロードが可能な日時を示す通知メッセージが表示されます。

1. ファイルをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、**[!UICONTROL Download].**&#x200B;をクリックします

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある&#x200B;**[!UICONTROL Download]**&#x200B;をクリックします。

     ファイルはブラウザーのダウンロード フォルダーに保存されます。<!-- See "[Placement columns in downloaded/uploaded spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     いずれかの設定を編集するには、ファイルを直接編集し、変更をアップロードします。 編集可能なすべての列が青色で強調表示されます。

## 特定のパッケージの設定のダウンロード

特定のパッケージの設定をダウンロードする場合、バルクシートファイルには、パッケージ設定とフライト情報のタブが個別に含まれ、ファイルは編集可能です。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Packages]**&#x200B;をクリックします。

1. 設定をダウンロードするパッケージのチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**&#x200B;をクリックします。

   バルクシートファイルのダウンロードが可能なタイミングを示す通知メッセージが表示されます。

1. バルクシートをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、**[!UICONTROL Download].**&#x200B;をクリックします

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある&#x200B;**[!UICONTROL Download]**&#x200B;をクリックします。

     ファイルはブラウザーのダウンロードフォルダーに保存されます。 含まれる列のリストについては、「[ ダウンロードまたはアップロード済みのバルクシートに列を配置](#qa-sheet-columns)」を参照してください。

     いずれかの設定を編集するには、ファイルを直接編集し、変更をアップロードします。 編集可能なすべての列が青色で強調表示されます。 フィールドに正しい形式を使用するには、関連するパッケージ設定またはプレースメント設定から値を選択してコピーします。 日分割、カスタム目標、コンバージョン指標などの一部のターゲット設定では、設定内でコピーオプションを使用できます。

## パッケージ設定を含むバルクシートのアップロード {#upload-bulksheet-package}

パッケージに関連付けられているプレースメントや広告など、パッケージの設定をバルクシートファイルにアップロードできます。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * 親キャンペーンの横で、**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**&#x200B;をクリックします。

   * キャンペーン名をクリックします。 右上で、**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**&#x200B;をクリックします。

     このオプションは、[!UICONTROL Packages]、[!UICONTROL Placements]、または[!UICONTROL Ads] タブから利用できます。

   * サブメニューで「**[!UICONTROL Packages]**」をクリックし、任意のパッケージのチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**&#x200B;をクリックします。

1. [!UICONTROL Upload Bulksheet] ダイアログで、次の操作を行います。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックして、デバイスまたはネットワークからファイルを選択します。

   1. **[!UICONTROL Upload]**&#x200B;をクリックします。

1. （オプション）更新が処理されたことを確認するには、上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。

設定の更新に失敗した場合は、カラーコーディング付きのバルクシート エラーファイルをダウンロードして、各失敗の理由とともに、どの設定（行）が保存され、どの失敗したかを示すことができます。 その後、同じファイル内の問題に対処し、修正された情報を処理するために再度アップロードできます。

<!--
## Package setting columns in downloaded/uploaded bulksheets{#qa-sheet-columns-packages}

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
>* [ バルクシートを使用したキャンペーンコンポーネント設定のレビューと編集](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [ パッケージの編集](/help/dsp/campaign-management/packages/package-edit.md)
>* [ パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
