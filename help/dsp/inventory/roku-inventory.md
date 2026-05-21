---
title: ' [!DNL Roku] 在庫を使用しています'
description: 在庫オプション、承認済みのサードパーティ追跡ベンダー、 [!DNL Roku]固有の配置に関するベストプラクティスなど、 [!DNL Roku]とのDSPのパートナーシップについて説明します。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
TQID: https://experienceleague.adobe.com/6CdN1InBGyd9pkECHBITFv1l8JjVdQ6Ot2MUDIAvDjY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: fbfa676f-2cdb-49be-b949-f2fab1be6dafid: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 477ab8f27ad0873b8cd919085cb2dba0db58924d
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# [!DNL Roku] インベントリを使用しています

Advertising DSPは[!DNL Roku]に広告の機能を提供します。

## オーディエンスマッチング

[!DNL Roku]とDSPのパートナーシップは、[!DNL Roku] インベントリ上の1:1決定論的オーディエンスのターゲティングに対して、[!DNL DSP]のオーディエンスを[!DNL Roku]のIDに一致させます。

## [!DNL Roku]個の在庫オプション

次のいずれかを実行できます。

* [!DNL Roku]と直接契約IDを設定し、契約ID データをDSPに入力します。

* [!DNL On Demand] ギャラリーにアクセスして、[!DNL Roku] プロファイルを購入します。

>[!NOTE]
>
>[!DNL Roku]のインベントリは、開いているマーケットプレイスや取引所では利用できません。

* プライベートな契約の場合、[DSP](/help/dsp/inventory/deal-id-create.md)で契約IDに関する情報を設定し、[!DNL Roku]件のプレースメント内で「[!UICONTROL Roku Network - Audience]」と「[!UICONTROL The Roku Channel - Audience]」をターゲットにします。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

*  [!DNL On Demand]  ギャラリー](/help/dsp/inventory/on-demand-inventory-subscribe.md)内の次の [!DNL Roku]  インベントリを[購読し、[!DNL Roku] プレースメント内の承認済み契約のいずれかをターゲットにすることができます。

   * [!DNL The CW]、[!DNL ABC]、[!DNL ESPN]など、プレミアムコンテンツパートナーを含む[!DNL Roku] エコシステム全体のインベントリの「[!UICONTROL Roku Network - Audience]」。

   * [!DNL Roku]個の所有および運営（O&amp;O）アプリコンテンツの「[!UICONTROL The Roku Channel - Audience]」。

### [!DNL Roku]でプライベートマーケットプレイスをカスタマイズする利点

プライベート取引では、ニーズに応じて取引パラメーターをカスタマイズできます。

* **価格交渉：** [!DNL Roku]の営業部門と協力して、キャンペーンのニーズを満たす取引の交渉と構成を行います。

* **スケールの優先度：** プライベートマーケットプレイス（PMP）は、常時対応案件（[!DNL On Demand]件など）よりも高い優先度を受け取ります。

* **頻度管理：** [!DNL Roku]のデフォルトの頻度上限は、ユーザーごとに30分あたり1回です。ただし、時間、日、週、月、またはフライト期間全体ごとに上限をカスタマイズできます。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]データのターゲット設定：** [!DNL Roku]のオーディエンスは、[!DNL Roku]のデバイスおよびテレビのシグナル、[!DNL The Roku Channel]によって追跡されたデータ（テレビのジャンルの親和性、ストリーミング テレビの動作、ケーブルのサブスクリプション状態など）、[!DNL Roku]顧客関係管理（CRM）システムからの追加データから構築されます。

* **[!DNL Roku]コンテンツのターゲット設定：** プライベート取引では、ジャンル、アプリのアプリケーション、季節イベントおよびテントポール イベント、および[!DNL The Roku Channel]内でのみアプリをターゲットにできます。

## [!DNL Roku] プレースメント

DSP キャンペーンでは、プレースメントタイプ「[!UICONTROL Connected TV (Roku)]」を使用して[特定のプレースメント  [!DNL Roku]を作成](/help/dsp/campaign-management/placements/placement-create.md)します。 目標が定義された[!DNL Roku]固有のパッケージに[!DNL Roku]個のプレースメントを含めます。

各[!DNL Roku] プレースメントは、少なくとも1つの[!DNL Roku]案件またはソースをターゲットにする必要があります。 [!DNL Roku]と一致するDSPのオーディエンスを使用するには、[!DNL Roku] （オプトイン）決定論的データセットと照合できる1つ以上のオーディエンスセグメントを含めます。

### [!DNL Roku]件の承認済みサードパーティ追跡ベンダー

[!DNL Roku] プレースメントには、次のベンダーのサードパーティのイベントピクセルとコンバージョンピクセルを含めることができます：[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]、[!DNL Research Now]、および[!DNL TransUnion]。

### プレースメント戦略別のベストプラクティス

以下は、[!DNL Roku]固有のプレースメントの推奨される方法です。

リーチを拡大する方法：

* [!DNL The Roku Channel]を使用して既にリーチしたオーディエンスを除外することで、[!DNL Roku O&O]で公開されたオーディエンスを抑制します。

* [!DNL Roku] プラットフォームで既にリーチしたオーディエンスを除外することで、[!DNL All Roku]で公開されたオーディエンスを抑制します。

最速の設定のために：

* [[!DNL On Demand]  インベントリ ](/help/dsp/inventory/on-demand-inventory-subscribe.md)の[!DNL The Roku Channel]に関する既存の常時対応案件をターゲットにして、所有および操作されている[!DNL Roku]のインベントリにすばやくアクセスします。
* [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)の[!DNL Roku Network]に関する既存の常時対応案件をターゲットにして、[!DNL Roku] プラットフォーム全体で迅速に規模を拡大します。

最大スケールまで：

* [!DNL Roku]個のプライベート マーケットプレイスをカスタマイズして、交渉済みの価格で[!DNL Roku]個の供給に優先的にアクセスできます。

>[!MORELIKETHIS]
>
>* [取引IDの詳細を手動で作成する](/help/dsp/inventory/deal-id-create.md)
> * [ プレミアム広告在庫のお得な情報 [!DNL On Demand] への登録とアクセスのリクエスト ](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [ プレースメントの作成](/help/dsp/campaign-management/placements/placement-create.md)
