---
title: ' [!DNL Roku] 在庫を使用しています'
description: 在庫オプション、承認済みのサードパーティ追跡ベンダー、 [!DNL Roku]固有の配置に関するベストプラクティスなど、 [!DNL Roku]とのDSPのパートナーシップについて説明します。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# [!DNL Roku] インベントリを使用しています

Advertising DSPは[!DNL Roku]に広告の機能を提供します。

## オーディエンスマッチング

[!DNL Roku]とDSPのパートナーシップは、[!DNL DSP] インベントリ上の1[!DNL Roku]決定論的オーディエンスのターゲティングに対して、:1のオーディエンスを[!DNL Roku]のIDに一致させます。

## [!DNL Roku]個の在庫オプション

次のいずれかを実行できます。

* [!DNL Roku]と直接契約IDを設定し、契約ID データをDSPに入力します。

* [!DNL On Demand] ギャラリーにアクセスして、[!DNL Roku] プロファイルを購入します。

>[!NOTE]
>
>[!DNL Roku]のインベントリは、開いているマーケットプレイスや取引所では利用できません。

* プライベートな契約の場合、[DSP](/help/dsp/inventory/deal-id-create.md)で契約IDに関する情報を設定し、[!UICONTROL Roku Network - Audience]件のプレースメント内で「[!UICONTROL The Roku Channel - Audience]」と「[!DNL Roku]」をターゲットにします。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* [&#x200B; ギャラリー [!DNL Roku] 内の次の [!DNL On Demand]  インベントリを](/help/dsp/inventory/on-demand-inventory-subscribe.md)購読し、[!DNL Roku] プレースメント内の承認済み契約のいずれかをターゲットにすることができます。

   * [!UICONTROL Roku Network - Audience]、[!DNL Roku]、[!DNL The CW]など、プレミアムコンテンツパートナーを含む[!DNL ABC] エコシステム全体のインベントリの「[!DNL ESPN]」。

   * [!UICONTROL The Roku Channel - Audience]個の所有および運営（O&amp;O）アプリコンテンツの「[!DNL Roku]」。

### [!DNL Roku]でプライベートマーケットプレイスをカスタマイズする利点

プライベート取引では、ニーズに応じて取引パラメーターをカスタマイズできます。

* **価格交渉：** [!DNL Roku]の営業部門と協力して、キャンペーンのニーズを満たす取引の交渉と構成を行います。

* **スケールの優先度：** プライベートマーケットプレイス（PMP）は、常時対応案件（[!DNL On Demand]件など）よりも高い優先度を受け取ります。

* **頻度管理：** [!DNL Roku]のデフォルトの頻度上限は、ユーザーごとに30分あたり1回です。ただし、時間、日、週、月、またはフライト期間全体ごとに上限をカスタマイズできます。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]データのターゲット設定：** [!DNL Roku]のオーディエンスは、[!DNL Roku]のデバイスおよびテレビのシグナル、[!DNL The Roku Channel]によって追跡されたデータ（テレビのジャンルの親和性、ストリーミング テレビの動作、ケーブルのサブスクリプション状態など）、[!DNL Roku]顧客関係管理（CRM）システムからの追加データから構築されます。

* **[!DNL Roku]コンテンツのターゲット設定：** プライベート取引では、ジャンル、アプリのアプリケーション、季節イベントおよびテントポール イベント、および[!DNL The Roku Channel]内でのみアプリをターゲットにできます。

## [!DNL Roku] プレースメント

DSP キャンペーンでは、プレースメントタイプ「[」を使用して [!DNL Roku]特定のプレースメント &#x200B;](/help/dsp/campaign-management/placements/placement-create.md)を作成[!UICONTROL Connected TV (Roku)]します。 目標が定義された[!DNL Roku]固有のパッケージに[!DNL Roku]個のプレースメントを含めます。

各[!DNL Roku] プレースメントは、少なくとも1つの[!DNL Roku]案件またはソースをターゲットにする必要があります。 [!DNL Roku]と一致するDSPのオーディエンスを使用するには、[!DNL Roku] （オプトイン）決定論的データセットと照合できる1つ以上のオーディエンスセグメントを含めます。

### [!DNL Roku]件の承認済みサードパーティ追跡ベンダー

[!DNL Roku] プレースメントには、次のベンダーのサードパーティのイベントピクセルとコンバージョンピクセルを含めることができます：[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]、および[!DNL Research Now]。

### プレースメント戦略別のベストプラクティス

以下は、[!DNL Roku]固有のプレースメントの推奨される方法です。

リーチを拡大する方法：

* [!DNL Roku O&O]を使用して既にリーチしたオーディエンスを除外することで、[!DNL The Roku Channel]で公開されたオーディエンスを抑制します。

* [!DNL All Roku] プラットフォームで既にリーチしたオーディエンスを除外することで、[!DNL Roku]で公開されたオーディエンスを抑制します。

最速の設定のために：

* [!DNL The Roku Channel] インベントリ [[!DNL On Demand] の](/help/dsp/inventory/on-demand-inventory-subscribe.md)に関する既存の常時対応案件をターゲットにして、所有および操作されている[!DNL Roku]のインベントリにすばやくアクセスします。
* [!DNL Roku Network]Inventory[[!DNL On Demand] の](/help/dsp/inventory/on-demand-inventory-subscribe.md)に関する既存の常時対応案件をターゲットにして、[!DNL Roku] プラットフォーム全体で迅速に規模を拡大します。

最大スケールまで：

* [!DNL Roku]個のプライベート マーケットプレイスをカスタマイズして、交渉済みの価格で[!DNL Roku]個の供給に優先的にアクセスできます。

>[!MORELIKETHIS]
>
>* [取引IDの詳細を手動で作成する](/help/dsp/inventory/deal-id-create.md)
> * [&#x200B; プレミアム広告在庫のお得な情報 [!DNL On Demand] への登録とアクセスのリクエスト &#x200B;](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [&#x200B; プレースメントの作成](/help/dsp/campaign-management/placements/placement-create.md)
