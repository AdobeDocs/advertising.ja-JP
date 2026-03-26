---
title: '[!UICONTROL Simple Ad Serving]件の取引設定'
description: '[!UICONTROL Simple Ad Serving]件の取引で使用可能な設定について説明します。'
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 90cc9d56a090136bc94270b048573d89503231c6
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving]件の取引設定

## 新規[!UICONTROL Simple Ad Serving]件の取引

### [!UICONTROL Select ad source]

| パラメーター | 説明 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | この契約のメディアタイプ：*[!UICONTROL Video]、*、*[!UICONTROL Display]、*&#x200B;または&#x200B;*[!UICONTROL Audio]。* |
| **[!UICONTROL Publisher Site Served On]** | この在庫を販売している発行者の名前。 名前の最初の2文字を入力して、発行者を検索します。 リストに記載されていない発行者を追加するには、Adobe アカウントチームにお問い合わせください。 |
| **[!UICONTROL Advertiser]** | この契約にアクセスできるアカウント内の1人の広告主。 キャンペーンと（オプションで）取引が使用可能なパッケージも選択します。 |
| **[!UICONTROL Media Quality Assessment?]** | （一部のユーザー）別のDSPで広告を実行し、サードパーティの検証を実行できるようにします。 |
| **[!UICONTROL Ad Source]** | 唯一のオプションは&#x200B;*[!UICONTROL Site Serve (Event Pixels)]*&#x200B;です。 |
| **[!UICONTROL Ad Creation]** | （新規のお得な情報のみ）次の操作を行うかどうか：<ul><li>*[!UICONTROL Create New]:*&#x200B;この取引の広告を作成するには。</li><li>*[!UICONTROL Select Ads]:*&#x200B;この取引に既存の広告を使用するには。</li></ul> |
| **[!UICONTROL Ad Type]** | この取引の広告タイプ。 取引のために広告を制作する場合は、必要に応じて広告のサイズや期間を含めるようにしましょう。 使用可能なオプションは、メディアタイプによって異なります。 |

{style="table-layout:auto"}

### [!UICONTROL Select ad(s)]

（既存の広告を使用している場合）取引に含める広告。 含める各広告の横にあるチェックボックスをオンにします。

### [!UICONTROL Select & upload [Media Type]]

（新しい広告のみ）新しい[&#x200B; サードパーティ広告](/help/dsp/campaign-management/ads/ad-create-multiple.md)を作成するためのScreens。

### [!UICONTROL Feed details]

| パラメーター | 説明 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 1000 インプレッションあたりのコスト（CPM）は、契約のレートカードに反映されます。 この値については、Adobe アカウントチームにお問い合わせください。 <br><br>取引の通貨も指定します。 すべてのユーザーがUSDを選択するか、SSPが追加通貨をサポートしている場合は、DSP アカウントの通貨を選択できます。 |
| **[!UICONTROL Third Party Billed Fees]** | （オプション）請求されないコストとして追跡される静的なサードパーティ料金、および取引の通貨。<br><br>すべてのユーザーがUSDを選択できます。また、SSPが追加通貨をサポートしている場合は、DSP アカウントの通貨を選択できます。 **メモ：**&#x200B;請求可能な手数料は、[!UICONTROL Net CPM]指標に反映されます。 |
| **[!UICONTROL Third Party Fee Description]** | （オプション）サードパーティ手数料の説明。 |
| **[!UICONTROL Flight Dates]** | この取引を使用したトラフィックの開始日と終了日。 フライト日は、キャンペーンのフライト日に含める必要があります。 広告タグは、指定されたフライト中にのみ応答を返します。<br><br>1年間の期間を持つシンプルな広告配信キャンペーンを個別に作成し、その中にトラッキングピクセルを構築するためのベストプラクティスです。 |
| **[!UICONTROL Impressions]** | （オプション）この契約を使用して実行するインプレッションの推定数。 この値は、追跡目的でのみ使用され、配信目標が達成されたときにフラグを立てるために使用されます。パブリッシャーは実際の広告配信を制御します。 DSP内でタグをアクティブに保ち、必要に応じて更新または拡張できるように、インプレッション数を多く入力することをお勧めします。 |
| **[!UICONTROL Deal Name]** | 取引名です。 名前を入力するか、*[!UICONTROL Auto Generate Deal Name]*&#x200B;を選択して、DSPが取引詳細に基づいて名前を生成できるようにします。<br><br>自動生成された名前の例：`Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （読み取り専用）契約に含まれる広告。 広告を編集するには、広告名をクリックします。 取引から広告を削除するには、広告名の横にある&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。 |

{style="table-layout:auto"}

<!-- 
## Existing [!UICONTROL Simple Ad Serving] deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!--
 From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [約[!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving]件の取引を作成](simple-deal-create.md)
>* [取引設定[!UICONTROL Simple Ad Serving]を編集](simple-deal-edit.md)
>* [取引に関する詳細なレポートを表示](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
