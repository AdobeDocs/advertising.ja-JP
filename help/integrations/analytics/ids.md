---
title: ' [!DNL Analytics]様が使用しているAdobe Advertising ID'
description: ' [!DNL Analytics]様が使用しているAdobe Advertising ID'
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%

---

# [!DNL Analytics]が使用するAdobe Advertising ID

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*&#x200B;に適用可能

Adobe Advertisingは、オンサイトのパフォーマンス トラッキングに&#x200B;*EF ID*&#x200B;と&#x200B;*AMO ID*&#x200B;の2つのIDを使用しています。

広告インプレッションが発生すると、Adobe AdvertisingはAMO IDとEF IDの値を作成し、それらを保存します。 広告を見た訪問者が広告をクリックせずにサイトに入ると、[!DNL Analytics]は[!DNL Analytics for Advertising] JavaScript コードを使用してAdobe Advertisingからこれらの値を呼び出します。 ビュースルートラフィックの場合、[!DNL Analytics]は補足ID （`SDID`）を生成し、EF IDとAMO IDを[!DNL Analytics]に合成するために使用します。 クリックスルートラフィックの場合、これらのIDは、`ef_id`および`s_kwcid` （AMO ID用）クエリ文字列パラメーターを使用して、ランディングページ URLに含まれます。

Adobe Advertisingでは、web サイトへのクリックスルーまたはビュースルーエントリを次の条件で区別します。

* ビュースルーエントリは、オーディエンスが広告を閲覧したものの、クリックしなかった場合にサイトにアクセスしたときに取得されます。 [!DNL Analytics]は、次の2つの条件が満たされた場合にビュースルーを記録します。

   * 訪問者には、[!DNL DSP] クリックのルックバックウィンドウ [!DNL Search, Social, & Commerce]の間に[または](/help/integrations/analytics/prerequisites.md#lookback-a4adc)広告のクリックスルーがありません。

   * 訪問者は、[!DNL DSP] インプレッションのルックバックウィンドウ [中に少なくとも1つの](/help/integrations/analytics/prerequisites.md#lookback-a4adc)広告を見ました。 最後のインプレッションはビュースルーとして渡されます。

* クリックスルーエントリは、サイト訪問者がサイトに入る前に広告をクリックしたときにキャプチャされます。 次のいずれかの条件が発生した場合、[!DNL Analytics]はクリックスルーをキャプチャします。

   * URLには、Adobe Advertisingによってランディングページ URLに追加されたEF IDとAMO IDが含まれます。

   * このURLにはトラッキングコードはありませんが、Adobe Advertising JavaScriptのコードでは、過去2分以内にクリックが検出されます。

![Adobe Advertising ビューベースの[!DNL Analytics]統合](/help/integrations/assets/a4adc-view-through-process.png)

*図1: Adobe Advertising ビューベースの[!DNL Analytics]統合*

![Adobe Advertising クリック URL ベースの[!DNL Analytics]統合](/help/integrations/assets/a4adc-click-through-process.png)

*図2: Adobe Advertising クリック URL ベースの[!DNL Analytics]統合*

## ADOBE ADVERTISING EF ID

EF IDは、Adobe Advertisingがアクティビティを個々のブラウザーまたはデバイスレベルでオンラインクリックまたは広告露出に関連付けるために使用する一意のトークンです。 EF IDは、主に、[!DNL Analytics] データとCustomer Journey Analytics データをAdobe Advertisingに送信し、Adobe Advertising内でレポートと入札を最適化するためのキーとして機能します。

[!DNL Analytics]の場合、EF IDは[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)または[!DNL rVar] （予約済み[!DNL eVar]）ディメンション（Adobe Advertising EF ID）に保存されます。

Customer Journey Analyticsの場合、EF IDは`trackingIdentities` オブジェクトの`conversionDetails` プロパティに格納されます。これは[the [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)の一部です。

### EF ID形式 {#ef-id-formats}

「Adobe Analytics コンポーネントガイド」のEF ID ディメンション項目[の](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-ef-id#dimension-items)形式を参照してください。

>[!NOTE]
>
>EF IDでは、大文字と小文字が区別されます。 [!DNL Analytics]またはCustomer Journey Analyticsの実装でURL トラッキングが小文字に強制される場合、Adobe AdvertisingはEF IDを認識しません。 これはAdobe Advertisingの入札とレポートに影響しますが、[!DNL Analytics]またはCustomer Journey Analytics内のAdobe Advertising レポートには影響しません。

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->

### [!DNL Analytics]のEF ID ディメンション

[!DNL Analytics] レポートでは、[!UICONTROL EF ID] ディメンションを検索し、[!UICONTROL EF ID Instance]指標を使用してEF ID データを検索できます。

EF IDは、Analysis Workspaceの500 kの一意のID制限の対象となります。 500 kの値に達すると、すべての新しいトラッキングコードが1行の項目タイトル「[!UICONTROL Low Traffic]」の下にレポートされます。 レポートの忠実性が欠落する可能性があるため、EF IDは分類されないので、[!DNL Analytics]のセグメントまたはレポートに使用しないでください。

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### AMO IDを実装する方法 {#amo-id-implement}

パラメーターは、次のいずれかの方法でトラッキング URLに追加されます。

* （推奨）サーバーサイド挿入機能を実装する場合。

   * DSPのお客様：エンドユーザーがAdobe Advertising ピクセルを使用してディスプレイ広告を表示すると、pixel serverはs_kwcid パラメーターをランディングページのサフィックスに自動的に追加します。

   * Search, Social, &amp; Commerceのユーザー：

      * アカウントまたはキャンペーンに対して[!DNL Google Ads]設定が有効になっている[!DNL Microsoft Advertising]および[!UICONTROL Auto Upload] アカウントの場合、エンドユーザーがAdobe Advertising ピクセルで広告をクリックすると、ピクセルサーバーはs_kwcid パラメーターをランディングページのサフィックスに自動的に追加します。

      * 他の広告ネットワーク、または[!DNL Google Ads]設定が無効になっている[!DNL Microsoft Advertising]および[!UICONTROL Auto Upload] アカウントの場合は、パラメーターを[ アカウントレベルの追加パラメーター](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}に手動で追加し、ベース URLに追加します。

* サーバーサイド挿入機能が実装されていない場合：

   * DSPのお客様：[JavaScript コード ](javascript.md)は、クリックスルーとビュースルーを自動的に記録します。 ブラウザーがサードパーティ Cookieをサポートしていない場合でも、次の広告タイプのクリックベースのコンバージョンを追跡できます。

      * [!DNL Flashtalking]個の広告タグの場合、「[追加 [!DNL Analytics for Advertising] 個のマクロを [!DNL Flashtalking] 個の広告タグ ](/help/integrations/analytics/macros-flashtalking.md)に手動で追加マクロを挿入します。」 **注：**&#x200B;組織が[!DNL Flashtalking]と直接パートナーシップを締結しており、データ渡しマクロを使用して`s_kwcid`および`ef_id`のトラッキングパラメーターを[!DNL Flashtalking] サポート ドキュメント（[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros)）で追跡する場合、この手順は必要ありません。

      * [!DNL Google Campaign Manager 360]個の広告タグの場合、「[追加 [!DNL Analytics for Advertising] 個のマクロを [!DNL Google Campaign Manager 360] 個の広告タグ ](/help/integrations/analytics/macros-google-campaign-manager.md)に手動で追加マクロを挿入します。」

   * Search, Social, &amp; Commerceのユーザー：

      * （[!DNL Google Ads]および[!DNL Microsoft Advertising]）広告の場合、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、AMO ID パラメーターを手動でランディングページのサフィックスに追加します。理想的には、[ アカウントレベル ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}で追加します。

      * 他のすべての広告ネットワークの広告の場合は、AMO ID パラメーターを[ アカウントレベルの追加パラメーター](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}に手動で追加し、ベース URLに追加します。

サーバーサイド挿入機能を導入する場合や、自社に最適な方法を判断する場合は、Adobeのアカウントチームにお問い合わせください。

### [!DNL Analytics]のAMO ID ディメンション

Analytics レポートでは、[!UICONTROL AMO ID] ディメンションを検索し、[!UICONTROL AMO ID Instances]指標を使用してAMO ID データを検索できます。 [!UICONTROL AMO ID] ディメンションには、キャプチャされたすべてのAMO ID値が格納されますが、[!UICONTROL AMO ID Instances]指標は、AMO ID値がサイトによってキャプチャされた頻度を示します。 例えば、同じ検索広告が4回クリックされ、Analyticsが7つのサイトエントリを追跡した場合、[!UICONTROL AMO ID Instances]は7つ（7）、[!UICONTROL Clicks]は4つ（4）になります。

[!DNL Analytics]内のレポートまたは監査の場合、AMO IDと対応するインスタンスを使用することをお勧めします。 詳しくは、「[とAdobe Advertising間の予想されるデータの差異」の「 [!DNL Analytics for Advertising]](data-variances.md#data-validation)のクリックスルーのデータ検証」を参照してください。[!DNL Analytics]

## Analyticsの分類について

[!DNL Analytics]では、[分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)は、アカウント、キャンペーン、広告など、特定のトラッキングコードのメタデータの一部です。 Adobe Advertisingでは、Adobe Advertisingの生データを分類して分類するため、レポートを生成する際に、広告タイプやCampaignなどのさまざまな方法でデータを表示できます。 分類は、[!DNL Analytics]のAdobe Advertising レポートのベースとなり、[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]、[!UICONTROL AMO Clicks]などのAMO指標や、[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]、[!UICONTROL Revenue]などのカスタムおよび標準のオンサイトイベントで使用できます。

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [ [!DNL Analytics] とAdobe Advertising](data-variances.md)の間の予期されるデータの差異
