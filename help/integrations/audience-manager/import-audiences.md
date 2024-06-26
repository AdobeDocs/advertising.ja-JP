---
title: 広告ターゲティング用のAdobe Audience Manager セグメントのインポート
description: を読み込む方法を学ぶ [!DNL Adobe] Adobe Audience Managerを使用した Advertising DSP および検索に対するオーディエンス
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# 広告ターゲティング用のAdobe Audience Manager セグメントのインポート

Advertising DSP および [!DNL Advertising Search, Social, & Commerce] それぞれが、広告主または代理店のすべてのメタデータ、階層データおよび一意のオーディエンスデータを取り込むことができます [!DNL Adobe] オーディエンス<!-- segments or audiences? Standardize terms per AAM's docs -->次を含む

* Adobe Audience Manager セグメント

* Adobe Experience Cloudに公開されるAdobe Analytics セグメント

* Adobe Experience Cloudで作成されたセグメント [!DNL Audience Library]

* Adobe Experience Platformで作成され、Audience Managerを介してAdobe Advertisingに送信されるセグメント

アクセス対象 [!DNL Adobe] DSPまたは内のオーディエンス [!DNL Creative]オーディエンスをDSPに読み込む必要があります。 アクセス対象 [!DNL Adobe] のオーディエンス [!DNL Search, Social, & Commerce]オーディエンスをに読み込む必要があります。 [!DNL Search, Social, & Commerce].

## 前提条件

* 広告主は、を実装する必要があります [この [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) バージョン 2.0 以降。 この [!DNL Identity Service] は、Experience Cloudのすべてのソリューションで訪問者を特定する永続的な汎用 ID を提供します。

  実装には、の追加が含まれます [!DNL Identity service] 広告主のサイトの各 web ページにコードを追加します。

* 組織は、 [Experience Cloudサービスに対して有効](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) そしてExperience Cloudがあります [!DNL Organization ID] （以前の名称： [!DNL IMS org ID]）に設定します。

  この [!UICONTROL Organization ID] を使用すると、複数のAdobe Experience Cloud製品を持つ組織が一部の製品間でデータを共有できます。

* （広告主 [!DNL Analytics]）を選択する必要があります [実装方法 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) バージョン 1.6.4 以降。

* 広告主の web サイト訪問者には、大量の [!DNL Apple Safari] ユーザー。

* （Audience Manager主が広告と [!DNL Analytics]）を使用して各 web ページへの呼び出しを減らすには、既存のAudience Managerを削除します [!DNL Data Integration Library] データ収集のコードと、それぞれのサーバーサイド転送の有効化 [!DNL Analytics] 代わりにレポートスイートを使用します。 詳しくは、「」を参照してください[サーバーサイド転送の概要](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* （推奨）一致率を高めるには、ファーストパーティの web サイトデータのみをAdobe Advertisingに送信します。 広告主が顧客関係管理システムからサードパーティデータやオフラインデータをバンドルすると、データ漏洩によりマッチ率が低下する可能性があります。

## DSPへのAudience Managerオーディエンスの読み込み

### オーディエンスをDSPにインポートする手順

この [!DNL Adobe] アカウントチームとデータ運用チームは、次の手順を実行します。

1. Adobeアカウントチームは、広告主レベルの設定を行う必要があります」[!UICONTROL Adobe Analytics Cloud].」と入力します。

1. Adobeアカウントチームは、データ操作チームにリクエストを送信し、Advertising DSP ネイティブ API 統合を使用して組織のAudience Managerセグメントをインポートする必要があります。

### Audience Managerに至る変化

API による自動アクセス：

* Audience Managerに 2 つのDSP宛先を作成します。

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* 2 つの宛先をすべてのAudience Managerセグメントにマッピングして、Audience Managerが同じExperience Cloudに関連付けられているDSP広告主アカウントとセグメントを共有できるようにします [!DNL Organization ID] Audience Managerに使用します。

  Audience Managerでは、オプションで、宛先内から不要なセグメントを削除できます。

* カスタマーキャンペーンのリーチを向上させるために、組織のAudience Managerコンテナに次の exchange cookie-sync ピクセルを追加します。

   * Adobe AdCloud: 411 （このピクセルは標準で、 [!DNL Identity Service] バージョン 2.0。組織と [!DNL Identity Service] バージョン 2.0 より前のバージョンでは、このピクセルがAudience Managerコンテナに追加されます。

## Audience Managerオーディエンスの読み込み先 [!DNL Search, Social, & Commerce]

### オーディエンスをにインポートする手順 [!DNL Search, Social, & Commerce]

[!DNL Adobe] 担当者は、次の手順の大部分またはすべてを実行します。

1. Adobeアカウントチームは、データ操作チームにリクエストを送信して、 [!DNL Search, Social, & Commerce] とAudience Manager。 書き出し先のAudience Managerセグメントの名前を含めます [!DNL Search, Social, & Commerce].

1. Audience Manager内での宛先の設定 [!DNL Search, Social, & Commerce]:

   1. 次の 2 つの新しい宛先を作成します。 `[!UICONTROL Adobe Media Optimizer (HTTP)]` および `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] は、の旧称です [!DNL Search, Social, & Commerce].

   1. 各宛先に対してセグメントを指定します。

      （を使用） [!UICONTROL Automatically map all current and future segments] オプションを選択すると、すべてのセグメントが毎日マッピングされ、同期されます。

      この [!UICONTROL Manually map segments] オプションを使用すると、セグメントを手動でマッピングして、バッチ宛先（`[!UICONTROL Adobe Media Optimizer Batch Destination]`）に設定します。 セグメントを HTTP 宛先に手動でマッピングする必要はありません。

1. 内 [!DNL Search, Social, & Commerce]、次のいずれか [!DNL Search, Social, & Commerce] 実装チームまたは direct access client manager の役割を持つユーザーが、からインポートを開始する必要があります。 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   組織のExperience Cloud [!DNL Organization ID] （[!DNL IMS org ID]）が必要です。 ID は、組織のAudience Managerアカウントに使用されているものと同じにする必要があります。

### Audience Managerに至る変化

2 [!DNL Search, Social, & Commerce] 宛先は、Audience Managerの組織で使用できるようになります。

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## データ同期

最初の読み込みには約 24 時間かかります。 最初の読み込み後、データは 1 秒から 2 秒の遅延でリアルタイムに同期されます。

セグメントメンバーシップデータは、次のいずれかのイベントの後にのみ送信されます。

* （DSPによる広告主）

   * セグメントは、Adobe Advertisingディスプレイ広告のターゲットになります。

   * セグメントがに追加されます [!DNL Adobe AdCloud Cross-Channel] Audience Managerユーザーインターフェイス内のバッチ宛先とリアルタイム宛先。

* （広告主 [!DNL Search, Social, & Commerce]）:

   * セグメントは、Adobe Advertising検索広告でターゲットに設定されます。

   * セグメントがに追加されます [!DNL Adobe Media Optimizer] Audience Managerユーザーインターフェイス内のバッチ宛先と HTTP 宛先。

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSPによるデータの同期方法

DSPは、 [!DNL Adobe Experience Cloud Identity (ECID) Service]. 同期中、 [!DNL ECID Service] からのAdobe Advertisingを呼び出す [!DNL cm.everesttech.net]. Adobe Advertisingは信頼できるドメインなので、ID 同期は、ほとんどのサードパーティのアクティベーションパートナーで行われるように、宛先公開 iframe 内ではなく親ページから行われます。 Audience Managerは、 [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)（別名） [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### 検索、ソーシャル、Commerceでのデータの同期方法

検索、ソーシャル、Commerceでは、 [!DNL Adobe Experience Cloud Identity (ECID) Service]. 同期中、 [!DNL ECID Service] からのAdobe Advertisingを呼び出す [!DNL cm.everesttech.net]（Adobe Advertisingに属する信頼されたドメイン）。 Audience Managerは、 [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)（別名） [!DNL Device ID].

## 同期したセグメントの場所

### DSP内

DSPは、セグメント名をAudience Manager分類別にまとめ、対応するセグメントメンバーシップの数をに含めます。

* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting)：の [!UICONTROL Adobe Segments] タブ [!UICONTROL Audience Targeting] セクション。

* 対象： [オーディエンス設定](/help/dsp/audiences/audience-settings.md)：の [!UICONTROL Adobe Segments] タブ。

### Advertising Creative内

対象： [!DNL Creative]セグメントは、target ノードのエクスペリエンス設定で使用できます。

### 対象： [!DNL Advertising Search, Social, & Commerce]

対象： [!DNL Search, Social, & Commerce]セグメントは、の作成時に使用できます。 [!DNL Google] を使用したオーディエンス [!UICONTROL Data Source] “[!UICONTROL Adobe Audience]から [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

それぞれに対して [!DNL Google] 作成するオーディエンス、 [!DNL Google] オーディエンスサイズを指定します。

>[!MORELIKETHIS]
>
>* [Adobe Audience ManagerとのAdobe Advertising統合](/help/integrations/audience-manager/overview.md)
