---
title: 使用 [!DNL Roku] 在庫
description: とのDSP パートナーシップのについて学ぶ [!DNL Roku]（在庫オプション、承認済みのサードパーティトラッキングベンダー、のベストプラクティスを含む） [!DNL Roku]固有のプレースメント。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 使用 [!DNL Roku] 在庫

Advertising DSPは、での広告用の機能を提供します。 [!DNL Roku].

## オーディエンスのマッチング

この [!DNL Roku] とDSP パートナーシップは次と一致します [!DNL DSP] オーディエンスの対象 [!DNL Roku] に対する 1 対 1 の決定論的オーディエンスターゲティングの ID [!DNL Roku] 在庫。

## [!DNL Roku] 在庫オプション

a）で直接民間取引 ID を設定できます。 [!DNL Roku] 次に、取引 ID データをDSPに入力します。または、b）にアクセスします。 [!DNL On Demand] 購読するギャラリー [!DNL Roku] プロファイル：

>[!NOTE]
>
>[!DNL Roku] 在庫は、オープンなマーケットプレイスおよび取引所では利用できません。

* プライベートな取引では、 [DSPでの取引 ID に関する情報の設定](/help/dsp/inventory/deal-id-create.md) 次に、をターゲットにします」[!UICONTROL Roku Network - Audience]「」と「」に対して検査する値[!UICONTROL The Roku Channel - Audience]内に [!DNL Roku] プレースメント。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 次のことができます [以下を購読 [!DNL Roku] 内の在庫 [!DNL On Demand] ギャラリー](/help/dsp/inventory/on-demand-inventory-subscribe.md)を選択し、内の承認済み取引のいずれかをターゲットにします [!DNL Roku] プレースメント :

   * “[!UICONTROL Roku Network - Audience]」に移動します [!DNL Roku] 次のようなプレミアムコンテンツパートナーとのエコシステム [!DNL The CW], [!DNL ABC]、および [!DNL ESPN].
   * “[!UICONTROL The Roku Channel - Audience]の場合 [!DNL Roku] 所有および運用（O&amp;O）アプリコンテンツ。

### を使用してプライベートマーケットプレイスをカスタマイズする場合の利点 [!DNL Roku]

プライベート取引では、必要に応じて取引パラメーターをカスタマイズできます。

* **交渉済み価格：** の操作 [!DNL Roku] セールス・チームは、お客様のキャンペーン・ニーズを満たす案件の交渉と構築を行います。

* **スケールの優先度：** プライベートマーケットプレイス（PMP）は、常に成立する取引よりも優先度が高くなります（例： [!DNL On Demand] 契約）。

* **頻度管理：** この [!DNL Roku] デフォルトのフリークエンシーキャップは、ユーザーあたり 30 分あたり 1 広告ですが、時間、日、週、月またはフライト期間全体でキャップをカスタマイズできます。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]データターゲティング：** [!DNL Roku] オーディエンスは、次の要素から構成されます [!DNL Roku] デバイスとテレビ信号、追跡対象のデータ [!DNL The Roku Channel] （テレビのジャンル親和性、ストリーミング TV の動作、ケーブル購読ステータスなど）、 [!DNL Roku] 顧客関係管理（CRM）システム。

* **[!DNL Roku]コンテンツのターゲティング：** ブロックリストに加える プライベート契約では、ジャンル、アプリの用途、季節的およびテントポールイベント、および内の番組ごとにアプリをターゲットにすることができます [!DNL The Roku Channel] のみ。

## [!DNL Roku] Placements

DSP キャンペーンでは、 [作成 [!DNL Roku]-specific placements](/help/dsp/campaign-management/placements/placement-create.md) プレースメント タイプの使用」[!UICONTROL Connected TV (Roku)].」と入力します。 次を含める [!DNL Roku] プレースメント [!DNL Roku]目標が定義された固有のパッケージ。

Each [!DNL Roku] プレースメントは、少なくとも 1 つをターゲットにする必要があります [!DNL Roku] 取引またはソース。 でのDSP オーディエンスマッチングを使用するには [!DNL Roku]、と照合できる 1 つ以上のオーディエンスセグメントを含めます [!DNL Roku] （オプトイン）決定論的データセット。

### [!DNL Roku] – 承認されたサードパーティトラッキングベンダー

[!DNL Roku] プレースメントには、次のベンダーのサードパーティイベントピクセルとコンバージョンピクセルを含めることができます。  [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]、および [!DNL Research Now].

### プレースメント戦略別のベストプラクティス

の推奨プラクティスを次に示します [!DNL Roku]固有のプレースメント。

増分リーチを最大化するには：

* で公開されるオーディエンスを抑制 [!DNL Roku O&O] を使用して既に到達したオーディエンスを除外する [!DNL The Roku Channel].

* で公開されるオーディエンスを抑制 [!DNL All Roku] に既に到達したオーディエンスを除外する [!DNL Roku] プラットフォーム。

最速のセットアップを実現：

* 既存の常時稼動の契約のターゲット [!DNL The Roku Channel] 。対象： [[!DNL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-subscribe.md) すばやくアクセスする [!DNL Roku] 所有済み及び運用済み在庫。
* 既存の常時稼動の契約のターゲット [!DNL Roku Network] 。対象： [[!DNL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-subscribe.md) を横断して迅速にスケールを達成する [!DNL Roku] プラットフォーム。

最大スケールに設定：

* のカスタマイズ [!DNL Roku] 優先的に利用できる民間市場 [!DNL Roku] 交渉価格で供給すること。

>[!MORELIKETHIS]
>
>* [取引 ID の詳細の手動作成](/help/dsp/inventory/deal-id-create.md)
> * [購読して次へのアクセスをリクエスト： [!DNL On Demand] プレミアム在庫取引](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [プレースメントの作成](/help/dsp/campaign-management/placements/placement-create.md)
