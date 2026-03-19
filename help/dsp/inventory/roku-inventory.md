---
title: Using [!DNL Roku] inventory
description: 在庫オプション、承認済みのサードパーティトラッキングベンダー、特定のプレースメントのベストプラクティスなど  [!DNL Roku] とのDSPのパートナーシップにつ  [!DNL Roku] て説明します。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: 54f69e4c0fa20b918a037cc5d2003d67db889913
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# [!DNL Roku] Inventory の使用

Advertising DSPは、[!DNL Roku] での広告用の機能を提供します。

## オーディエンスのマッチング

[!DNL Roku] とDSPのパートナーシップは、[!DNL DSP] オーディエンスを [!DNL Roku] ID に一致させて、インベントリに対する 1:1 決定論的なオーディエンスのターゲティング [!DNL Roku] 実現します。

## [!DNL Roku] 在庫オプション

a） [!DNL Roku] で直接プライベート取引 ID を設定し、取引 ID データをDSPに入力するか、b） [!DNL On Demand] Gallery にアクセスしてプロファイルを購読 [!DNL Roku] きます。

>[!NOTE]
>
>オ [!DNL Roku] プンマーケットプレイスおよび取引所では、在庫は利用できません。

* プライベートな取引の場合は、[DSPで取引 ID に関する情報を設定し &#x200B;](/help/dsp/inventory/deal-id-create.md) プレースメント内で「[!UICONTROL Roku Network - Audience]」と「[!UICONTROL The Roku Channel - Audience]」をターゲットに [!DNL Roku] ます <!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->。

* [Gallery 内で以下の  [!DNL Roku] inventory を購読  [!DNL On Demand]  し、プレースメント内の承認済みの取引をターゲッ &#x200B;](/help/dsp/inventory/on-demand-inventory-subscribe.md) 設定 [!DNL Roku] きます。

   * [!UICONTROL Roku Network - Audience]、[!DNL Roku]、[!DNL The CW] などのプレミアム・コンテンツ・パートナーを使用して、[!DNL ABC] エコシステム全体のインベントリを「[!DNL ESPN]」します。
   * 所有および運営（O&amp;O）アプリコンテンツ [!UICONTROL The Roku Channel - Audience] 場合は「[!DNL Roku]」。

### [!DNL Roku] を使用してプライベートマーケットプレイスをカスタマイズするメリット

プライベート取引では、必要に応じて取引パラメーターをカスタマイズできます。

* **交渉による価格設定：**&#x200B;[!DNL Roku] 営業チームと協力して、キャンペーンのニーズを満たす契約を交渉および構築します。

* **スケールの優先度：** プライベートマーケットプレイス（PMP）は、常にオンの取引（[!DNL On Demand] ールの取引など）よりも高い優先度を受け取ります。

* **頻度管理：** [!DNL Roku] のデフォルトの頻度キャップは、ユーザーあたり 30 分あたり 1 広告ですが、時間、日、週、月、またはフライト期間全体でキャップをカスタマイズできます。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Data Targeting:** [!DNL Roku] オーディエンスは、デバイスとテレビ信号、[!DNL Roku] で追跡され [!DNL The Roku Channel] データ（テレビのジャンル親和性、ストリーミング TV の動作、ケーブルの購読ステータスなど）、および [!DNL Roku] 顧客関係管理（CRM）システムからの追加データから作成されます。

* ブロックリストに加える **[!DNL Roku]コンテンツのターゲット設定：** 非公開の取引では、ジャンル、アプリの用途、季節やテントポールイベント、[!DNL The Roku Channel] 内の番組ごとにアプリをターゲットにすることができます。

## [!DNL Roku] placements

DSP キャンペーンでは、プレースメントタイプ「[」を使用して  [!DNL Roku] 作成 &#x200B;](/help/dsp/campaign-management/placements/placement-create.md) 固有のプレースメント [!UICONTROL Connected TV (Roku)] を作成します。 目標 [!DNL Roku] 定義された [!DNL Roku] 固有のパッケージにプレースメントを含めます。

各 [!DNL Roku] プレースメントは、少なくとも 1 つの [!DNL Roku] ースの契約またはソースをターゲットにする必要があります。 [!DNL Roku] でDSPのオーディエンスマッチングを使用するには、[!DNL Roku] （オプトイン）の決定論的データセットと照合できる 1 つ以上のオーディエンスセグメントを含めます。

### [!DNL Roku] 承認のサードパーティトラッキングベンダー

プレースメントに [!DNL Roku]、[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk] および [!DNL Research Now] のサードパーティイベントピクセルとコンバージョンピクセルを含めることができます。

### プレースメント戦略によるベストプラクティス

[!DNL Roku] 固有のプレースメントに対する推奨事項を次に示します。

増分リーチを最大化するには：

* [!DNL Roku O&O] を使用して既に到達したオーディエンスを除外することで、[!DNL The Roku Channel] で公開されたオーディエンスを抑制します。

* [!DNL All Roku] プラットフォーム全体で既に到達しているオーディエンスを除外することで、[!DNL Roku] で公開されたオーディエンスを抑制します。

最速のセットアップを実現：

* [!DNL The Roku Channel] [[!DNL On Demand]  在庫 &#x200B;](/help/dsp/inventory/on-demand-inventory-subscribe.md) 内の既存の常時稼動の取引をターゲットにして、所有および運用されてい [!DNL Roku] 在庫にすばやくアクセスします。
* [!DNL Roku Network] 在庫 [[!DNL On Demand]  の既存の常時稼動の取引をターゲットにして、](/help/dsp/inventory/on-demand-inventory-subscribe.md) プラットフォーム全体の [!DNL Roku] ケールを迅速に達成します。

最大スケールに設定：

* 交渉された価格で [!DNL Roku] 供給に優先的にアクセスできるように、[!DNL Roku] のプライベートマーケットプレイスをカスタマイズします。

>[!MORELIKETHIS]
>
>* [&#x200B; 取引 ID の詳細の手動作成 &#x200B;](/help/dsp/inventory/deal-id-create.md)
> * [&#x200B; プレミアム在庫取引の購入  [!DNL On Demand]  アクセスのリクエスト &#x200B;](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [&#x200B; プレースメントの作成 &#x200B;](/help/dsp/campaign-management/placements/placement-create.md)
