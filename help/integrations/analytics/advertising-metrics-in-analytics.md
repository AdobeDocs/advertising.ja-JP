---
title: Analysis WorkspaceのAdobe Advertising指標
description: Analysis WorkspaceでのAdobe Advertisingの指標と分類
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
TQID: https://experienceleague.adobe.com/CLPeE8g0Mix4Scq90qCd-s-tCUuBmkTBrkBWT1aPEhw
autotag-review: '2026-04-13T23:29:38.865Z'
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2: id: cfd751d4-ee56-4323-8fd1-dc174b031709
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 6e85310e94f642ccf3ccb0d67f43d5ebbf03fa24
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Analysis WorkspaceのAdobe Advertising指標

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

>[!NOTE]
>
>* Adobe Advertisingは、毎日[!DNL Analytics]にトラフィック指標と分類を渡します。
>* [!DNL Analytics]は、Adobe Advertisingのクリックスルーとビュースルーをリアルタイムでキャプチャします。
>* [!DNL Search, Social, & Commerce]の場合、この機能はほとんどの広告ネットワークとキャンペーンの種類でサポートされています。 詳しくは、[ ガイドの「](/help/search-social-commerce/introduction/supported-inventory.md) サポートされているインベントリ [!DNL Search, Social, & Commerce]」を参照してください。

## Adobe Advertisingのトラフィック指標

[!DNL Analytics]のAdobe Advertising トラフィック指標は、通常、「[!UICONTROL AMO ID Instances]」以外は「Adobe Advertising」で始まります。 ただし、当初クリック数、コスト、インプレッション数の指標を作成するために（予約イベントではなく）カスタムイベントを使用した長期的な顧客の場合、これらの指標はまだ「AMO」で始まります。

一覧については、「[Adobe Advertising指標](https://experienceleague.adobe.com/en/docs/analytics/components/metrics/amo-metrics)」を参照してください。

<!--

| Traffic Metric | Description |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] or (some legacy customers) [!UICONTROL AMO Clicks] | The number of total Adobe Advertising clicks. |
| [!UICONTROL Adobe Advertising Cost] or (some legacy customers) [!UICONTROL AMO Cost] | The Adobe Advertising spend in the currency of the report suite. |
| [!UICONTROL Adobe Advertising Impressions] or (some legacy customers) [!UICONTROL AMO Impressions] | The number of Adobe Advertising impressions. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | The number of impressions that were served for which viewability instrumentation successfully initialized. This value is calculated as (instrumented impressions - the number of unmeasurable impressions). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | The number of minutes an Adobe Advertising video was viewed. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | The number of impressions that were determined to be not viewable. This value is calculated as ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | The number of impressions that were measured to be viewable according to the placement configuration. |
| [!UICONTROL Adobe Advertising Views] | The number of views on an ad. A view is counted when the viewer initiates the Adobe Advertising video. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | The number of views for which at least 25% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | The number of views for which at least 50% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | The number of views for which at least 75% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | The number of views for which 100% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO ID Instances] | The number of times the [!UICONTROL AMO ID] is set. |

-->

## Adobe Advertising分類

AMO ID ディメンションの「[分類](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#classifications)」を参照してください。
<!--

>[!NOTE]
>
>All Adobe Advertising dimensions in [!DNL Analytics] are followed by "[!DNL (AMO ID)]."

| Dimension | Applicable Adobe Advertising Data  | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Advertising DSP or the search engine name |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The account name. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) or the ad network name ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The campaign name. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The package ([!DNL DSP]) or portfolio ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | The placement name. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | The ad group name. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The search match type. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword and match type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad type, such as `text`, `video`, `display`, or `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data |The ad type ([!DNL DSP]) or ad title ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad description ([!DNL DSP]) or ad body ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The URL displayed in the ad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The destination URL for the ad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Whether the landing page entry was a view-through or a click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | The product target for a product listing ad. |

-->

## Adobe Advertisingの便利なカスタム計算指標

Adobe Advertisingデータについて、次の指標の作成を検討してください。

* ランディングページインスタンスへのクリック数（[!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]）：これは、広告をクリックしてランディングページに到達したユーザーの割合です。
* 測定可能なレート （[!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100）
* 表示可能なインプレッション率（[!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100）
* 表示単価（[!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views]）
* クリック単価（[!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks]）

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe Advertisingのデータ ](/help/integrations/analytics/analytics-data-in-advertising.md)
