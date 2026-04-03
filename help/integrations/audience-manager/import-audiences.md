---
title: 広告のターゲティング用にAdobe Audience Manager セグメントをインポートする
description: Adobe Audience Managerを使用して [!DNL Adobe]  オーディエンスをAdvertising DSPに読み込み、検索する方法について説明します
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
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 920
ht-degree: 0%

---

# 広告のターゲティング用にAdobe Audience Manager セグメントをインポートする

Advertising DSPと[!DNL Advertising Search, Social, & Commerce]は、広告主または代理店のすべての[!DNL Adobe] オーディエンス <!-- segments or audiences? Standardize terms per AAM's docs -->に関するメタデータ、階層データ、固有のオーディエンスデータをそれぞれ取り込むことができます。次の項目を含みます。

* Adobe Audience Manager セグメント

* Adobe Experience Cloudに公開されるAdobe Analytics セグメント

* Adobe Experience Cloud [!DNL Audience Library]を使用して作成されたセグメント

* Adobe Experience Platformで作成され、Audience Manager経由でAdobe Advertisingに送信されるセグメント

DSPまたは[!DNL Adobe]の[!DNL Creative] オーディエンスにアクセスするには、オーディエンスをDSPに読み込む必要があります。 [!DNL Adobe]の[!DNL Search, Social, & Commerce] オーディエンスにアクセスするには、オーディエンスを[!DNL Search, Social, & Commerce]に読み込む必要があります。

## 前提条件

* 広告主は、[the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) バージョン 2.0以降を実装する必要があります。 [!DNL Identity Service]は、Experience Cloudのすべてのソリューションで訪問者を識別する、ユニバーサルで永続的なIDを提供します。

  実装には、広告主のサイトの各web ページに[!DNL Identity service] コードを追加することが含まれます。

* Experience Cloud サービス [に対して有効な](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview)組織で、Experience Cloud [!DNL Organization ID] （旧称：[!DNL IMS org ID]）が必要です。

  [!UICONTROL Organization ID]を使用すると、複数のAdobe Experience Cloud製品を持つ組織は、一部の製品間でデータを共有できます。

* （広告主と[!DNL Analytics]）広告主は、[&#x200B; [!DNL Analytics]  バージョン 1.6.4以降を使用して`appMeasurement.js`実装](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview)する必要があります。

* 広告主のweb サイト訪問者には、大量の[!DNL Apple Safari]人のユーザーが含まれていません。

* （広告主がAudience Managerと[!DNL Analytics]の両方を使用する場合にお勧めします）各web ページへの呼び出しを減らすには、データ収集用に既存のAudience Manager [!DNL Data Integration Library] コードを削除し、代わりに[!DNL Analytics] レポートスイートごとにサーバーサイド転送を有効にします。 詳しくは、「[&#x200B; サーバーサイド転送の概要](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf)」を参照してください。

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

* 2つの宛先をすべてのAudience Manager セグメントにマッピングし、Audience Managerが、Audience Managerに使用されているのと同じExperience Cloud [!DNL Organization ID]に関連付けられているDSP広告主アカウントとセグメントを共有できるようにします。

  組織は、オプションで、Audience Manager内の宛先から不要なセグメントを削除できます。

* 組織のAudience Manager コンテナに次のExchange Cookie-sync ピクセルを追加して、カスタマーキャンペーンのリーチを向上させます。

   * Adobe AdCloud: 411 （このピクセルは標準で、バージョン 2.0の[!DNL Identity Service]の一部として自動的に提供されます。[!DNL Identity Service] バージョンが2.0未満の企業は、このピクセルをAudience Manager コンテナに追加する必要があります。

## Audience Manager オーディエンスを[!DNL Search, Social, & Commerce]にインポート

### オーディエンスを[!DNL Search, Social, & Commerce]に読み込む手順

[!DNL Adobe]人の担当者は、次の手順のほとんどまたはすべてを実行します。

1. Adobe アカウントチームは、[!DNL Search, Social, & Commerce]とAudience Manager間の統合を設定するためのリクエストをデータオペレーションチームに送信する必要があります。 [!DNL Search, Social, & Commerce]に書き出すAudience Manager セグメントの名前を含めます。

1. Audience Manager内で、[!DNL Search, Social, & Commerce]の宛先を設定します。

   1. 2つの新しい宛先を作成：`[!UICONTROL Adobe Media Optimizer (HTTP)]`と`[!UICONTROL Adobe Media Optimizer Batch Destination]`。

      [!DNL Media Optimizer]は[!DNL Search, Social, & Commerce]の旧名です。

   1. 各宛先のセグメントを指定します。

      [!UICONTROL Automatically map all current and future segments] オプションを使用すると、すべてのセグメントが毎日マッピングおよび同期されます。

      [!UICONTROL Manually map segments] オプションを使用すると、バッチ宛先（`[!UICONTROL Adobe Media Optimizer Batch Destination]`）と同期するようにセグメントを手動でマッピングできます。 セグメントをHTTP宛先に手動でマッピングする必要はありません。

1. [!DNL Search, Social, & Commerce]以内に、[!DNL Search, Social, & Commerce]実装チームまたはDirect Access クライアントマネージャーの役割を持つユーザーが、[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup]からインポートを開始する必要があります。

   組織のExperience Cloud [!DNL Organization ID] （[!DNL IMS org ID]）が必要です。 IDは、組織のAudience Manager アカウントに使用されているものと同じである必要があります。

### Audience Managerでは、どのような変化が生まれるのでしょうか？

2つの[!DNL Search, Social, & Commerce]の宛先が、Audience Managerの組織で利用できるようになります。

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## データの同期

最初のインポートには約24時間かかります。 最初のインポート後、データはリアルタイムで同期され、1～2秒の遅延が発生します。

セグメントメンバーシップデータは、次のいずれかのイベントが発生した後にのみ送信されます。

* （DSPの広告主）:

   * このセグメントは、Adobe Advertisingのディスプレイ広告のターゲットとなります。

   * セグメントは、Audience Manager ユーザーインターフェイス内の[!DNL Adobe AdCloud Cross-Channel] バッチおよびリアルタイムの宛先に追加されます。

* （広告主、[!DNL Search, Social, & Commerce]）:

   * このセグメントは、Adobe Advertisingの検索広告のターゲットになっています。

   * セグメントは、Audience Manager ユーザーインターフェイス内の[!DNL Adobe Media Optimizer] バッチおよびHTTP宛先に追加されます。

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSPによるデータの同期

DSPは、[!DNL Adobe Experience Cloud Identity (ECID) Service]を使用してデータを自動的に同期します。 同期中、[!DNL ECID Service]は[!DNL cm.everesttech.net]にAdobe Advertisingを呼び出します。 Adobe Advertisingは信頼できるドメインであるため、IDの同期は、ほとんどのサードパーティのアクティベーションパートナーと同様に、宛先の公開iframe内ではなく、親ページから行われます。 Audience Managerは、[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)を使用して、デバイス IDで一意のユーザーを識別します。これは[!DNL Device ID]とも呼ばれます。

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Search, Social, &amp; Commerceにおけるデータの同期方法

Search, Social, &amp; Commerceは、[!DNL Adobe Experience Cloud Identity (ECID) Service]を使用してデータを自動的に同期します。 同期中、[!DNL ECID Service]は[!DNL cm.everesttech.net]にAdobe Advertisingを呼び出します。これは、Adobe Advertisingに属する信頼できるドメインです。 Audience Managerは、[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)を使用して、デバイス IDで一意のユーザーを識別します。これは[!DNL Device ID]とも呼ばれます。

## 同期したセグメントの検索場所

### DSPの


DSPは、Audience Manager分類によってセグメント名を整理し、対応するセグメントメンバーシップ数を次の場所に含めます。

* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): [!UICONTROL Adobe Segments] セクションの「[!UICONTROL Audience Targeting]」タブ。

* [&#x200B; オーディエンス設定](/help/dsp/audiences/audience-settings.md):「[!UICONTROL Adobe Segments]」タブ。

### Advertising Creativeの


[!DNL Creative]では、セグメントはターゲットノードのエクスペリエンス設定で使用できます。

### [!DNL Advertising Search, Social, & Commerce]内

[!DNL Search, Social, & Commerce]では、[!DNL Google] > [!UICONTROL Data Source] > [!UICONTROL Adobe Audience]から[!UICONTROL Campaigns] &quot;[!UICONTROL Audiences]&quot;を使用して[!UICONTROL Library] オーディエンスを作成すると、セグメントを利用できます。

作成した各[!DNL Google] オーディエンスに対して、[!DNL Google]はオーディエンスサイズを提供します。

>[!MORELIKETHIS]
>
>* [Adobe AdvertisingとAdobe Audience Managerの統合](/help/integrations/audience-manager/overview.md)
