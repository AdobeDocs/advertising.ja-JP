---
title: Customer Journey AnalyticsのAdobe Advertising指標およびディメンション
description: Customer Journey Analyticsで使用可能なAdobe Advertisingの指標とディメンションを参照します。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 97c89e03-ab15-4906-96fc-6bb77ea0cd7c
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Customer Journey AnalyticsのAdobe Advertising指標およびディメンション

*Adobe AdvertisingとCustomer Journey Analyticsの統合のみを利用する広告主*

*Beta機能*

Adobe Advertisingは、トラフィック指標とディメンションを毎日 [!DNL Customer Journey Analytics] に渡します。 [!DNL Web SDK] は、Adobe Advertisingのクリックスルーとビュースルーをリアルタイムでキャプチャして、Customer Journey Analyticsに渡します。

## Adobe Advertisingのトラフィック指標

<!-- Verify column names -->

次の表を参照してください。

* 「XDM フィールド名」は、Adobe Experience Platformのフィールド名です。

* 「XDM フィールド表示名」は、Customer Journey Analytics内の表示名を示します。

| Adobe Advertising フィールド名 | XDM フィールド名 | XDM フィールドの表示名 | Source |
|------------------------------|----------------|------------------------|--------|
| 日付 | 日付 | すべて | |
| AMO ID | skwcid | ADOBE ADVERTISING ID | すべて |
| AMO インプレッション数 | adobe_advertising_impressions | Adobe Advertising インプレッション数 | すべて |
| AMO クリック数 | adobe_advertising_clicks | Adobe Advertising クリック数 | すべて |
| AMO コスト | adobe_advertising_cost | Adobe Advertisingコスト | すべて |
| 通貨コード | 通貨 | 通貨 | すべて |
| AMO ビュー数 | adobe_advertising_views | Adobe Advertising ビュー | Ad CloudDSP |
| AMO 再生 25% 時点の視聴数 | adobe_advertising_views_25_pct | Adobe Advertising再生 25% 時点の視聴数 | Ad CloudDSP |
| AMO 再生 50% 時点の視聴数 | adobe_advertising_views_50_pct | Adobe Advertising再生 50% 時点の視聴数 | Ad CloudDSP |
| AMO 再生 75% 時点の視聴数 | adobe_advertising_views_75_pct | Adobe Advertising再生 75% 時点の視聴数 | Ad CloudDSP |
| AMO 再生 100% 時点での視聴数 | adobe_advertising_views_100_pct | Adobe Advertising再生 100% 時点での視聴数 | Ad CloudDSP |
| AMO 視聴時間（分） | adobe_advertising_minutes_viewed | Adobe Advertising閲覧時間（分） | Ad CloudDSP |
| AMO ビューアブルインプレッション数 | adobe_advertising_viewable_impressions | Adobe Advertising ビューアブルインプレッション数 | Ad CloudDSP |
| AMO 非ビューアブルインプレッション数 | adobe_advertising_not_viewable_impressions | Adobe Advertising ノンビューアブルインプレッション数 | Ad CloudDSP |
| AMO 測定可能インプレッション数 | adobe_advertising_measureable_impressions | Adobe Advertising測定可能なインプレッション数 | Ad CloudDSP |

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

## Adobe Advertising ディメンション

次の表を参照してください。

* 「XDM フィールド名」は、Adobe Experience Platformのフィールド名です。

* 「XDM フィールド表示名」は、Customer Journey Analytics内の表示名を示します。

| Adobe Advertising フィールド名 | XDM フィールド名 | XDM フィールドの表示名 | Source |
|------------------------------|----------------|------------------------|--------|
| キー | skwcid | ADOBE ADVERTISING ID |  |
| 広告プラットフォーム | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |  |
| アカウント | adobe_advertising_account | Adobe Advertising アカウント |  |
| キャンペーン | adobe_advertising_campaign | Adobe Advertising キャンペーン |  |
| 広告グループ | adobe_advertising_ad_group | Adobe Advertising広告グループ |  |
| キーワード | adobe_advertising_keyword | Adobe Advertisingキーワード |  |
| 広告 | adobe_advertising_ad | Adobe Advertising広告 |  |
| プレースメント | adobe_advertising_placement | Adobe Advertisingの配置 |  |
| 一致のタイプ | adobe_advertising_match_type | Adobe Advertising一致タイプ |  |
| 広告タイトル | adobe_advertising_ad_title | Adobe Advertising広告タイトル |  |
| 広告の説明 | adobe_advertising_ad_description | Adobe Advertising広告の説明 |  |
| 広告の宛先 URL | adobe_advertising_ad_destination_url | Adobe Advertising広告の宛先 URL |  |
| 広告表示 URL | adobe_advertising_ad_display_url | Adobe Advertising広告の表示 URL |  |
| デバイス | adobe_advertising_device | Adobe Advertising デバイス |  |
| キーワード MatchType | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |  |
| ネットワーク | adobe_advertising_network | Adobe Advertisingネットワーク |  |
| 広告タイプ | adobe_advertising_ad_type | Adobe Advertising広告タイプ |  |
| 製品ターゲット | adobe_advertising_product_target | Adobe Advertising Product Target |  |
| ランディングタイプ | adobe_advertising_landing_type | Adobe Advertisingのランディングタイプ |  |
| 最適化 | adobe_advertising_optimization | Adobe Advertisingの最適化 |  |

>[!MORELIKETHIS]
>
>* [&#x200B; 概要 &#x200B;](overview.md)
>* [&#x200B; 前提条件 &#x200B;](prerequisites.md)
>* [&#x200B; 使用するAdobe Advertising ID [!DNL Customer Journey Analytics]](ids.md)
>* [&#x200B; データ収集、データ転送、レポートの設定 &#x200B;](set-up.md)
