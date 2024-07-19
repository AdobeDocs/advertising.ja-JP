---
title: '[!UICONTROL Simple Ad Serving] 契約設定'
description: '[!UICONTROL Simple Ad Serving] の取引で利用可能な設定について説明します。'
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Deal Settings

## 新しい [!UICONTROL Simple Ad Serving] 取引

### [!UICONTROL Select Ad Source]

| パラメーター | 説明 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | この契約のメディア タイプ：*[!UICONTROL Video]、* *[!UICONTROL Display]、* または *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | この在庫を販売しているパブリッシャーの名前。 名前の最初の 2 文字以上を入力して発行元を検索します。 一覧にない発行元を追加するには、Adobeアカウント チームに問い合わせてください。 |
| **[!UICONTROL Advertiser]** | この取引にアクセスできるアカウント内の単一の広告主。 また、キャンペーンと（オプションで）契約を使用できるパッケージを選択します。 |
| **[!UICONTROL Media Quality Assessment?]** | （一部のユーザー）サードパーティの検証のために、広告を別のDSPで実行できるようにします。<!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 唯一のオプションは *[!UICONTROL Site Serve (Event Pixels)]* です。 |
| **[!UICONTROL Ad Creation]** | （新規取引のみ）次の操作を行うかどうか：<ul><li>*[!UICONTROL Create New]:* この取引の広告を作成するには。</li><li>*[!UICONTROL Select Ads]:* この取引で既存の広告を使用するには、次の手順に従います。</li></ul> |
| **[!UICONTROL Ad Type]** | この取引の広告タイプ。 契約の広告を作成する場合は、リクエストに応じて広告サイズまたは期間を含めます。 使用できるオプションは、メディアタイプによって異なります。 |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

（既存の広告を使用している場合）取引に含める広告。 組み込む各広告の横にあるチェックボックスをオンにします。

### [!UICONTROL Select & Upload [Media Type]]

（新しい広告のみ）新しい [ サードパーティ広告 ](/help/dsp/campaign-management/ads/ad-create-multiple.md) を作成するためのScreens。

### [!UICONTROL Feed Details]

| パラメーター | 説明 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 契約の料金カードに反映される、1000 インプレッション数（CPM）あたりのコスト。 この値については、Adobeアカウントチームにお問い合わせください。 <br><br> 取引の通貨も指定します。 すべてのユーザーは、USD を選択するか、SSP が追加の通貨をサポートしている場合はDSP アカウントの通貨を選択できます。 |
| **[!UICONTROL Third Party Billed Fees]** | （任意）請求不可コストとしてトラッキングされる静的サードパーティ料金と取引の通貨。<br><br> すべてのユーザーが USD を選択できます。また、SSP で追加の通貨がサポートされている場合は、DSP アカウントの通貨を選択できます。 **メモ：** 請求可能な料金は [!UICONTROL Net CPM] 指標に反映されます。 |
| **[!UICONTROL Third Party Fee Description]** | （任意）サードパーティの料金の説明。 |
| **[!UICONTROL Flight Dates]** | この取引を使用するトラフィックの開始日と終了日。 フライト日は、キャンペーンフライト日の範囲内に含める必要があります。 広告タグは、指定されたフライト中にのみ応答を返します。<br><br> 1 年間の期間を持つ個別のシンプルな広告サービングキャンペーンを作成し、その中にトラッキングピクセルを作成するためのベストプラクティス。 |
| **[!UICONTROL Impressions]** | （任意）この取引を使用して実行すると予想される推定インプレッション数。 この値は、トラッキング目的でのみ使用され、配信の目標が満たされた場合にフラグを設定するために使用されます。パブリッシャーは実際の広告配信を制御します。 ベストプラクティスは、多数のインプレッションを入力して、DSP内でタグをアクティブに保ち、必要に応じて更新または拡張できるようにすることです。 |
| **[!UICONTROL Deal Name]** | 取引名。 名前を入力するか、「*[!UICONTROL Auto Generate Deal Name]*」を選択して、DSPで取引の詳細に基づいて名前を生成します。<br><br> 自動生成される名前の例：`Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （読み取り専用）取引の一部である広告。 広告を編集するには、広告名をクリックします。 契約から広告を削除するには、広告名の横にある「**[!UICONTROL X]**」をクリックします。 |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

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
>* [[!UICONTROL Simple Ad Serving]](simple-deal-about.md) について
>* [[!UICONTROL Simple Ad Serving] しい取引の作成 ](simple-deal-create.md)
>* [ 契約設定 [!UICONTROL Simple Ad Serving] 編集 ](simple-deal-edit.md)
>* [ 取引の詳細レポートの表示 ](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
