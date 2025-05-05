---
title: 広告ターゲティング用のAdobe Audience Manager セグメントのインポート
description: オーディエンスをAdvertising DSPに読み込み  [!DNL Adobe] Adobe Audience Managerを使用して検索する方法を説明します
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# 広告ターゲティング用のAdobe Audience Manager セグメントのインポート

Advertising DSPと [!DNL Advertising Search, Social, & Commerce] は、次のようなすべての広告主または代理店の [!DNL Adobe] ーザーオーディエンスのメタデータ、階層データおよび一意のオーディエンスデータを取り込むこ <!-- segments or audiences? Standardize terms per AAM's docs --> ができます。

* Adobe Audience Manager セグメント

* Adobe Experience Cloudに公開されるAdobe Analytics セグメント

* Adobe Experience Cloud [!DNL Audience Library] を使用して作成されたセグメント

* Adobe Experience Platformで作成され、Audience Managerを介してAdobe Advertisingに送信されるセグメント

DSPまたは [!DNL Creative] で [!DNL Adobe] オーディエンスにアクセスするには、オーディエンスをDSPに読み込む必要があります。 [!DNL Search, Social, & Commerce] で [!DNL Adobe] オーディエンスにアクセスするには、オーディエンスを [!DNL Search, Social, & Commerce] に読み込む必要があります。

## 前提条件

* 広告主は、[the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/ja/docs/id-service/using/intro/overview) バージョン 2.0 以降を実装する必要があります。 [!DNL Identity Service] は、Experience Cloudのすべてのソリューションで訪問者を特定する永続的な汎用 ID を提供します。

  実装には、広告主のサイトの各 web ページへの [!DNL Identity service] コードの追加が含まれます。

* 組織は、[Experience Cloudサービスを有効にする ](https://experienceleague.adobe.com/ja/docs/core-services/interface/services/overview)Experience Cloud[!DNL Organization ID] （以前の [!DNL IMS org ID]）が必要です。

  [!UICONTROL Organization ID] を使用すると、複数のAdobe Experience Cloud製品を持つ組織で、一部の製品間でデータを共有できます。

* （[!DNL Analytics] を使用する広告主）広告主は、バージョン 1.6.4 以降 `appMeasurement.js`[&#128279;](https://experienceleague.adobe.com/ja/docs/analytics/implementation/js/overview) 使用して  実装  [!DNL Analytics]  する必要があります。

* 広告主の web サイト訪問者には、大量の [!DNL Apple Safari] ユーザーは含まれていません。

* （Audience Managerと [!DNL Analytics] の両方を使用する場合にお勧めします）各 web ページへの呼び出しを減らすには、データ収集用の既存のAudience Manager[!DNL Data Integration Library] ードコードを削除し、代わりに各 [!DNL Analytics] レポートスイートのサーバーサイド転送を有効にします。 詳しくは、「[ サーバーサイド転送の概要 ](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf) を参照してください。

* （推奨）一致率を高めるには、ファーストパーティの web サイトデータのみをAdobe Advertisingに送信します。 広告主が顧客関係管理システムからサードパーティデータやオフラインデータをバンドルすると、データ漏洩によりマッチ率が低下する可能性があります。

## DSPへのAudience Managerオーディエンスの読み込み

### オーディエンスをDSPにインポートする手順

[!DNL Adobe] アカウントおよびデータ操作チームは、次の手順を実行します。

1. Adobeアカウントチームは、広告主レベルの設定「[!UICONTROL Adobe Analytics Cloud]」を構成する必要があります。

1. Adobeアカウントチームは、データ操作チームにリクエストを送信し、Advertising DSP native API 統合を使用して組織のAudience Managerセグメントを読み込む必要があります。

### Audience Managerに至る変化

API による自動アクセス：

* Audience Managerに 2 つのDSP宛先を作成します。

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* 2 つの宛先をすべてのAudience Managerセグメントにマップします。これにより、Audience Managerは、Audience Managerに使用した同じExperience Cloud[!DNL Organization ID] に関連付けられているDSP広告主アカウントとセグメントを共有できます。

  Audience Managerでは、オプションで、宛先内から不要なセグメントを削除できます。

* カスタマーキャンペーンのリーチを向上させるために、組織のAudience Managerコンテナに次の exchange cookie-sync ピクセルを追加します。

   * Adobe AdCloud: 411 （このピクセルは [!DNL Identity Service] バージョン 2.0 の一部として標準および自動で提供されます。[!DNL Identity Service] のバージョンが 2.0 未満の組織では、このピクセルをAudience Managerコンテナに追加する必要があります。

## [!DNL Search, Social, & Commerce] へのAudience Managerオーディエンスの読み込み

### オーディエンスを [!DNL Search, Social, & Commerce] にインポートする手順

次 [!DNL Adobe] 手順の大部分またはすべてを担当者が実行します。

1. Adobeアカウントチームは、データ操作チームにリクエストを送信して、[!DNL Search, Social, & Commerce] とAudience Managerの間の統合を設定する必要があります。 [!DNL Search, Social, & Commerce] に書き出すAudience Managerセグメントの名前を含めます。

1. Audience Manager内で、[!DNL Search, Social, & Commerce] の宛先を設定します。

   1. `[!UICONTROL Adobe Media Optimizer (HTTP)]` と `[!UICONTROL Adobe Media Optimizer Batch Destination]` の 2 つの新しい宛先を作成します。

      [!DNL Media Optimizer] は [!DNL Search, Social, & Commerce] の旧称である。

   1. 各宛先に対してセグメントを指定します。

      [!UICONTROL Automatically map all current and future segments] オプションを使用すると、すべてのセグメントが毎日マッピングされ、同期されます。

      [!UICONTROL Manually map segments] オプションを使用すると、セグメントを手動でマッピングして、バッチ宛先（`[!UICONTROL Adobe Media Optimizer Batch Destination]`）と同期できます。 セグメントを HTTP 宛先に手動でマッピングする必要はありません。

1. [!DNL Search, Social, & Commerce] 内で、[!DNL Search, Social, & Commerce] 実装チームまたは直接アクセスのクライアントマネージャーの役割を持つユーザーが、[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Audience Manager Setup] から読み込みを開始する必要があります。

   組織のExperience Cloud [!DNL Organization ID] （[!DNL IMS org ID]）が必要です。 ID は、組織のAudience Managerアカウントに使用されているものと同じにする必要があります。

### Audience Managerに至る変化

Audience Managerの組織は、[!DNL Search, Social, & Commerce] の 2 つの宛先を使用できるようになります。

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## データ同期

最初の読み込みには約 24 時間かかります。 最初の読み込み後、データは 1 秒から 2 秒の遅延でリアルタイムに同期されます。

セグメントメンバーシップデータは、次のいずれかのイベントの後にのみ送信されます。

* （DSPによる広告主）

   * セグメントは、Adobe Advertisingディスプレイ広告のターゲットになります。

   * セグメントは、Audience Managerユーザーインターフェイス内の [!DNL Adobe AdCloud Cross-Channel] バッチおよびリアルタイムの宛先に追加されます。

* （[!DNL Search, Social, & Commerce] の広告主）

   * セグメントは、Adobe Advertising検索広告でターゲットに設定されます。

   * セグメントは、Audience Managerユーザーインターフェイス内の [!DNL Adobe Media Optimizer] バッチおよび HTTP 宛先に追加されます。

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSPによるデータの同期方法

DSPは、[!DNL Adobe Experience Cloud Identity (ECID) Service] を使用してデータを自動的に同期します。 同期中、[!DNL ECID Service] は [!DNL cm.everesttech.net] でAdobe Advertisingを呼び出します。 Adobe Advertisingは信頼できるドメインなので、ID 同期は、ほとんどのサードパーティのアクティベーションパートナーで行われるように、宛先公開 iframe 内ではなく親ページから行われます。 Audience Managerは、[!DNL Device ID] とも呼ばれる [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/ja/docs/audience-manager/user-guide/reference/ids-in-aam) を使用して、デバイス ID ごとに一意のユーザーを識別します。

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### 検索、ソーシャル、Commerceでのデータの同期方法

検索、ソーシャル、Commerceでは、[!DNL Adobe Experience Cloud Identity (ECID) Service] を使用してデータが自動的に同期されます。 同期中に、[!DNL ECID Service] は、Adobe Advertisingに属する信頼されたドメインである [!DNL cm.everesttech.net] でAdobe Advertisingを呼び出します。 Audience Managerは、[!DNL Device ID] とも呼ばれる [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/ja/docs/audience-manager/user-guide/reference/ids-in-aam) を使用して、デバイス ID ごとに一意のユーザーを識別します。

## 同期したセグメントの場所

### DSP内

DSPは、セグメント名をAudience Manager分類別にまとめ、対応するセグメントメンバーシップの数をに含めます。

* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting):「プレースメント」セクションの「[!UICONTROL Adobe Segments]」タブ [!UICONTROL Audience Targeting] 使用します。

* [ オーディエンス設定 ](/help/dsp/audiences/audience-settings.md) の場合：「オーディ [!UICONTROL Adobe Segments] ンス」タブで設定します。

### Advertising Creative内

ま [!DNL Creative]、セグメントは、ターゲットノードのエクスペリエンス設定で使用できます。

### [!DNL Advertising Search, Social, & Commerce] 内

[!DNL Search, Social, & Commerce] では、[!UICONTROL Campaigns]/[!UICONTROL Audiences]/[!UICONTROL Library] の [!UICONTROL Data Source] 「[!UICONTROL Adobe Audience]」を使用して [!DNL Google] オーディエンスを作成する際に、セグメントを使用できます。

作成する [!DNL Google] オーディエンスごとに、[!DNL Google] がオーディエンスサイズを指定します。

>[!MORELIKETHIS]
>
>* [Adobe Audience ManagerとのAdobe Advertising統合 ](/help/integrations/audience-manager/overview.md)
