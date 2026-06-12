---
title: Customer Journey AnalyticsのAdobe Advertising指標とディメンション
description: Customer Journey Analyticsで使用可能なAdobe Advertisingの指標とディメンションを参照します。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 97c89e03-ab15-4906-96fc-6bb77ea0cd7c
TQID: https://experienceleague.adobe.com/JN42ThofnM6kP8Urd8bTpyQbIWIReb-jgCbOvlnCAQ0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: b2f5488c286d6a01d78218488dbcaa799f4010ca
workflow-type: tm+mt
source-wordcount: 455
ht-degree: 0%

---

# Customer Journey AnalyticsのAdobe Advertising指標とディメンション

*Adobe AdvertisingとCustomer Journey Analyticsの統合のみを使用する広告主*

Adobe Advertisingは、毎日[!DNL Customer Journey Analytics]にトラフィック指標とディメンションを渡します。 [!DNL Web SDK]は、Adobe Advertisingのクリックとビュースルーをリアルタイムでキャプチャし、Customer Journey Analyticsに渡します。

![Customer Journey AnalyticsのAdobe Advertising データの例](/help/integrations/assets/cja-report-example.png "Customer Journey AnalyticsのAdobe Advertising データの例")

## Adobe Advertisingのトラフィック指標

<!-- Verify column names -->

次の表に示します。

* 「XDM フィールド名」は、Adobe Experience Platformのフィールド名です。

* 「XDM フィールド表示名」は、Customer Journey Analytics内の表示名を示します。

| Adobe Advertising フィールド名 | XDM フィールド名 | XDM フィールドの表示名 | Source |
|------------------------------|----------------|------------------------|--------|
| 日付 | 日付 | すべて | |
| AMO ID | skwcid | ADOBE ADVERTISING ID | すべて |
| AMO インプレッション数 | adobe_advertising_impressions | Adobe Advertising インプレッション | すべて |
| AMO クリック数 | adobe_advertising_clicks | Adobe Advertising クリック数 | すべて |
| AMO コスト | adobe_advertising_cost | Adobe Advertising コスト | すべて |
| 通貨コード | 通貨 | 通貨 | すべて |
| AMO ビュー | adobe_advertising_views | Adobe Advertising ビュー | Ad Cloud DSP |
| AMO ビュー数25%完了 | adobe_advertising_views_25_pct | Adobe Advertisingの閲覧数25%完了 | Ad Cloud DSP |
| AMO ビュー数50%完了 | adobe_advertising_views_50_pct | Adobe Advertisingの閲覧数50%完了 | Ad Cloud DSP |
| AMO ビュー75%完了 | adobe_advertising_views_75_pct | Adobe Advertisingの閲覧数75%完了 | Ad Cloud DSP |
| AMO ビュー数100%完了 | adobe_advertising_views_100_pct | Adobe Advertisingでの閲覧数が100%完了 | Ad Cloud DSP |
| AMOの表示時間（分） | adobe_advertising_minutes_viewed | Adobe Advertising分表示時間 | Ad Cloud DSP |
| AMO表示可能インプレッション数 | adobe_advertising_viewable_impressions | Adobe Advertisingで表示できるインプレッション数 | Ad Cloud DSP |
| AMOのインプレッションが表示されない | adobe_advertising_not_viewable_impressions | Adobe Advertisingで表示されないインプレッション | Ad Cloud DSP |
| AMO測定可能なインプレッション数 | adobe_advertising_measure_impressions | Adobe Advertisingの測定可能なインプレッション数 | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertisingのディメンション

次の表に示します。

<!-- Need to fill in the "Source" column -->

* 「XDM フィールド名」は、Adobe Experience Platformのフィールド名です。

* 「XDM フィールド表示名」は、Customer Journey Analytics内の表示名を示します。

| Adobe Advertising フィールド名 | XDM フィールド名 | XDM フィールドの表示名 | Source |
|------------------------------|----------------|------------------------|--------|
| キー | skwcid | ADOBE ADVERTISING ID |  |
| 広告プラットフォーム | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |  |
| アカウント | adobe_advertising_account | Adobe Advertising アカウント |  |
| キャンペーン | adobe_advertising_campaign | Adobe Advertising Campaign |  |
| 広告グループ | adobe_advertising_ad_group | Adobe Advertising Ad Group |  |
| キーワード | adobe_advertising_keyword | Adobe Advertising キーワード |  |
| 広告 | adobe_advertising_ad | Adobe Advertising広告 |  |
| プレースメント | adobe_advertising_placement | Adobe Advertising Placement |  |
| 一致タイプ | adobe_advertising_match_type | Adobe Advertisingの一致タイプ |  |
| 広告タイトル | adobe_advertising_ad_title | Adobe Advertising広告タイトル |  |
| Ad Description | adobe_advertising_ad_description | Adobe Advertising広告の説明 |  |
| 広告宛先URL | adobe_advertising_ad_destination_url | Adobe Advertising Ad Destination URL |  |
| 広告表示URL | adobe_advertising_ad_display_url | Adobe Advertising Ad Display URL |  |
| デバイス | adobe_advertising_device | Adobe Advertising Device |  |
| キーワード MatchType | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |  |
| ネットワーク | adobe_advertising_network | Adobe Advertising Network |  |
| 広告の種類 | adobe_advertising_ad_type | Adobe Advertisingの広告の種類 |  |
| 製品ターゲット | adobe_advertising_product_target | Adobe Advertising Product Target |  |
| ランディングタイプ | adobe_advertising_landing_type | Adobe Advertisingのランディングタイプ |  |
| 最適化 | adobe_advertising_optimization | Adobe Advertising Optimization |  |

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>* [前提条件](prerequisites.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)様が使用しているAdobe Advertising ID
>* [&#x200B; データ収集、データ転送、レポートの設定](set-up.md)
