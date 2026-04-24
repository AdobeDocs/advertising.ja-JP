---
title: Import Adobe Audience Manager segments for ad targeting
description: Learn how to import your [!DNL Adobe] audiences into Advertising DSP and Search using Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
TQID: https://experienceleague.adobe.com/-OqZLPZ1uWjBqSaCtGnmF5nrrxVIdT0kpE6YznQWttw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 992
ht-degree: 0%

---

# Import Adobe Audience Manager segments for ad targeting

Advertising DSP and [!DNL Advertising Search, Social, & Commerce] can each pull in metadata, hierarchy data, and unique audience data for all of an advertiser&#39;s or agency&#39;s [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs -->, including:

* Adobe Audience Manager セグメント

* Adobe CX Enterpriseに公開されるAdobe Analytics セグメント

* Adobe CX Enterprise [!DNL Audience Library]を使用して作成されたセグメント

* Segments that are created in Adobe Experience Platform and sent to Adobe Advertising via Audience Manager

To access [!DNL Adobe] audiences in DSP or [!DNL Creative], you must import the audiences into DSP. To access [!DNL Adobe] audiences in [!DNL Search, Social, & Commerce], you must import the audiences into [!DNL Search, Social, & Commerce].

## 前提条件

* The advertiser must implement [the [!DNL Adobe CX Enterprise Identity (ECID) Service]](https://experienceleague.adobe.com/ja/docs/id-service/using/intro/overview) version 2.0 or higher. The [!DNL Identity Service] provides a universal, persistent ID that identifies your visitors across all solutions in CX Enterprise.

  Implementation includes adding the [!DNL Identity service] code to each webpage on the advertiser&#39;s sites.

* The organization must be [enabled for CX Enterprise services](https://experienceleague.adobe.com/ja/docs/core-services/interface/services/overview) and have a CX Enterprise [!DNL Organization ID] (formerly called [!DNL IMS org ID]).

  The [!UICONTROL Organization ID] allows organizations with multiple Adobe CX Enterprise products to share data among some of the products.

* (Advertisers with [!DNL Analytics]) The advertiser must [implement [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/ja/docs/analytics/implementation/js/overview) version 1.6.4 or higher.

* The advertiser&#39;s website visitors don&#39;t include a high volume of [!DNL Apple Safari] users.

* (Recommended when the advertiser uses both Audience Manager and [!DNL Analytics]) To reduce calls to each webpage, remove existing Audience Manager [!DNL Data Integration Library] code for data collection and enable server-side forwarding for each [!DNL Analytics] report suite instead. For more information, see &quot;[Server-side forwarding overview](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* （推奨）一致率を高めるには、1st パーティのweb サイトデータのみをAdobe Advertisingに送信します。 広告主が顧客関係管理システムからサードパーティデータやオフラインデータをバンドルしている場合、データ漏洩により一致率が低下する可能性があります。

## DSPへのAudience Manager オーディエンスのインポート

### DSPにオーディエンスを読み込む手順

[!DNL Adobe] アカウントおよびデータ運用チームは、次の手順を実行します。

1. Adobe アカウントチームは、広告主レベルの設定「[!UICONTROL Adobe Analytics Cloud]」を設定する必要があります。

1. Adobe アカウントチームは、Advertising DSP ネイティブ API統合を使用して組織のAudience Manager セグメントをインポートするリクエストをデータオペレーションチームに送信する必要があります。

### Audience Managerでは、どのような変化が生まれるのでしょうか？

APIは自動的に以下を行います。

* Audience Managerに2つのDSPの宛先を作成します。

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* 2つの宛先をすべてのAudience Manager セグメントにマッピングし、Audience Managerが、Audience Managerに使用されているのと同じCX Enterprise [!DNL Organization ID]に関連付けられているDSP広告主アカウントとセグメントを共有できるようにします。

  組織は、オプションで、Audience Manager内の宛先から不要なセグメントを削除できます。

* 組織のAudience Manager コンテナに次のExchange Cookie-sync ピクセルを追加して、カスタマーキャンペーンのリーチを向上させます。

   * Adobe AdCloud: 411 （このピクセルは標準で、バージョン 2.0の[!DNL Identity Service]の一部として自動的に提供されます。 [!DNL Identity Service] バージョンが2.0未満の企業は、このピクセルをAudience Manager コンテナに追加する必要があります。

## Audience Manager オーディエンスを[!DNL Search, Social, & Commerce]にインポート

### オーディエンスを[!DNL Search, Social, & Commerce]に読み込む手順

[!DNL Adobe]人の担当者は、次の手順のほとんどまたはすべてを実行します。

1. Adobe アカウントチームは、[!DNL Search, Social, & Commerce]とAudience Manager間の統合を設定するためのリクエストをデータオペレーションチームに送信する必要があります。 [!DNL Search, Social, & Commerce]に書き出すAudience Manager セグメントの名前を含めます。

1. Audience Manager内で、[!DNL Search, Social, & Commerce]の宛先を設定します。

   1. 2つの新しい宛先を作成：`[!UICONTROL Adobe Media Optimizer (HTTP)]`と`[!UICONTROL Adobe Media Optimizer Batch Destination]`。

      [!DNL Media Optimizer]は[!DNL Search, Social, & Commerce]の旧名です。

   1. 各宛先のセグメントを指定します。

      [!UICONTROL Automatically map all current and future segments] オプションを使用すると、すべてのセグメントが毎日マッピングおよび同期されます。

      The [!UICONTROL Manually map segments] option allows you to manually map the segments to sync with the batch destination (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). No segments need to be manually mapped to the HTTP destination.

1. Within [!DNL Search, Social, & Commerce], either the [!DNL Search, Social, & Commerce] implementation team or a user with the direct access client manager role should initiate the import from [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   The organization&#39;s Adobe CX Enterprise [!DNL Organization ID] ([!DNL IMS org ID]) is required. The ID must be the same as the one used for the organization&#39;s Audience Manager account.

### Audience Managerでは、どのような変化が生まれるのでしょうか？

Two [!DNL Search, Social, & Commerce] destinations become available for the organization in Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Data synchronization

The initial import takes about 24 hours. After the initial import, data is synced in real time, with a one- to two-second delay.

Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

   * The segment is targeted in an Adobe Advertising display ad.

   * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search, Social, & Commerce]):

   * The segment is targeted in an Adobe Advertising search ad.

   * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### How DSP syncs the data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.everesttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/ja/docs/audience-manager/user-guide/reference/ids-in-aam), also called the [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### How Search, Social, &amp; Commerce syncs the data

Search, Social, &amp; Commerce syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.everesttech.net], which is a trusted domain that belongs to Adobe Advertising. Audience Managerは、[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/ja/docs/audience-manager/user-guide/reference/ids-in-aam)を使用して、デバイス IDで一意のユーザーを識別します。これは[!DNL Device ID]とも呼ばれます。

## 同期したセグメントの検索場所

### DSPの


DSPは、Audience Manager分類によってセグメント名を整理し、対応するセグメントメンバーシップ数を次の場所に含めます。

* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): [!UICONTROL Audience Targeting] セクションの「[!UICONTROL Adobe Segments]」タブ。

* [&#x200B; オーディエンス設定](/help/dsp/audiences/audience-settings.md):「[!UICONTROL Adobe Segments]」タブ。

### Advertising Creativeの


[!DNL Creative]では、セグメントはターゲットノードのエクスペリエンス設定で使用できます。

### [!DNL Advertising Search, Social, & Commerce]内

[!DNL Search, Social, & Commerce]では、[!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library]から[!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot;を使用して[!DNL Google] オーディエンスを作成すると、セグメントを利用できます。

作成した各[!DNL Google] オーディエンスに対して、[!DNL Google]はオーディエンスサイズを提供します。

>[!MORELIKETHIS]
>
>* [Adobe AdvertisingとAdobe Audience Managerの統合](/help/integrations/audience-manager/overview.md)
