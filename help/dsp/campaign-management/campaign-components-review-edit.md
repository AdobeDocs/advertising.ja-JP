---
title: バルクシートを使用した Campaign コンポーネント設定のレビューと編集
description: スプレッドシートを使用して、主要なパッケージ、プレースメント、広告設定を一括でレビューおよび編集する方法を説明します。
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: c1039c59c0a1f8d2bbe08b4522b28f2f883a3dea
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# バルクシートを使用した Campaign コンポーネント設定のレビューと編集

1 つのキャンペーンでパッケージ、プレースメント、広告の設定を XLSX （[!DNL Microsoft Excel] スプレッドシート）形式でダウンロードして、設定を確認し編集できます。 デフォルトでは、ダウンロードしたファイルは *バルクシート* と呼ばれ、パッケージ設定、パッケージのフライト情報、プレースメント設定、プレースメント広告のスケジュール用の個別のタブが含まれています。 オプションで、一部のキャンペーンコンポーネントタイプの設定を除外できます。

複数の設定を一度に更新するには、変更を含む有効なバルクシートファイルをアップロードします。 バルクシートを作成するには、ダウンロードしたバルクシートを既存の設定で編集します。 編集可能なフィールドには、通常は編集可能なほとんどの設定が含まれています。

>[!NOTE]
>
>特定のパッケージと特定のプレースメントのみの設定をダウンロードして編集することもできます。 「[ バルクシートを使用したパッケージ設定のレビューと編集 ](/help/dsp/campaign-management/packages/package-qa.md)」および「[ バルクシートを使用したプレースメント設定のレビューと編集 ](/help/dsp/campaign-management/placements/placement-qa.md)」を参照してください。

## キャンペーン内のパッケージ、プレースメントおよび広告の設定のダウンロード {#download-bulksheet-campaign}

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * キャンペーンの横で、**[!UICONTROL ...]**/**[!UICONTROL Download Bulksheet]** をクリックします。

   * キャンペーン名をクリックします。 右上で、**[!UICONTROL ...]**/**[!UICONTROL Download Bulksheet]** をクリックします。

1. [!UICONTROL Bulksheet Download] ダイアログボックスで、ダウンロードしたファイルから設定を除外する Campaign コンポーネントの選択を解除し、「**[!UICONTROL Download]**」をクリックします。

デフォルトでは、すべてのキャンペーンコンポーネントの設定が選択されます。

通知メッセージは、ファイルのダウンロードが可能なタイミングを示します。

1. ファイルをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

     ファイルはブラウザーのダウンロードフォルダーに保存されます。<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     設定を編集するには、ファイルを直接編集してから、変更内容をアップロードします。 編集可能な列はすべて青でハイライト表示されます。 フィールドに正しい形式を使用するには、関連するパッケージ設定またはプレースメント設定から値を選択してコピーします。 日分割、カスタム目標、コンバージョン指標など、一部のターゲット設定では、設定内でコピーオプションを使用できます。

## パッケージ、プレースメント、広告設定を含んだキャンペーン用バルクシートのアップロード{#upload-bulksheet-campaign-components}

1 つのキャンペーンのパッケージ、プレースメントおよび広告の設定を、入力されたバルクシートに一度にアップロードします。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * キャンペーンの横で、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

   * キャンペーン名をクリックします。 右上で、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

1. [!UICONTROL Upload Bulksheet] ダイアログで、次の手順を実行します。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. 「**[!UICONTROL Upload]**」をクリックします。

1. （オプション）更新が処理されたことを確認するには、上部のメニューバーの右側にある ![ ジョブ ](/help/dsp/assets/downloads.png) をクリックします。

設定の更新に失敗した場合、色分けしたバルクシートエラーファイルをダウンロードすると、保存された設定（行）と失敗した設定（失敗した行）と、失敗した各設定の理由を表示できます。 その後、同じファイル内の問題に対処し、もう一度アップロードして、修正された情報を処理できます。


<!--
## Placement Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### Campaign-level Spreadsheets

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Whether the Inventory Targeting option to exclude outstream traffic is <i[!UICONTROL >ON]* or *[!UICONTROL OFF]*.<br>Outstream ads usually appear over the content as a pop-up or stuffed into content (in the native experience), rather than as regular video ads in a video player. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |
-->

>[!MORELIKETHIS]
>
>* [ バルクシートを使用したパッケージ設定のレビューと編集 ](/help/dsp/campaign-management/packages/package-qa.md)
>* [ パッケージ設定 ](/help/dsp/campaign-management/packages/package-settings.md)
>* [ バルクシートを使用した配置設定の確認と編集 ](/help/dsp/campaign-management/placements/placement-qa.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ オーディオ広告設定 ](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [ 接続されたテレビの設定 ](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [ 広告設定を表示 ](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [ モバイル広告設定 ](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [ ネイティブのディスプレイ広告設定 ](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [ プリロール広告設定 ](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [ ユニバーサルビデオ広告設定 ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
