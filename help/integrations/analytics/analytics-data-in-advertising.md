---
title: Adobe Advertisingの[!DNL Analytics] データ
description: Adobe Advertisingの[!DNL Analytics] データ
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Adobe Advertisingの[!DNL Analytics] データ

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

## Analytics セグメント

[!DNL Analytics]で作成され、Experience Cloudに公開されたすべてのセグメント。

新しいセグメントがAdobe Advertisingに表示されるまでに24～48時間かかります。 既存のセグメントの更新は、約8時間以内に同期されます。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## サイトエンゲージメント指標

>[!NOTE]
>
>* [!DNL Analytics]は、EF ID [!DNL eVar]のイベントをAdobe Advertisingに渡します。  デフォルトの統合では、計算指標やその他のディメンション（[!DNL eVars]）のAdobe Advertisingへの送信はサポートされていません。 ただし、計算された指標がカスタムイベントで完全にキャプチャできる場合、Adobe Advertisingはカスタムイベントを取り込むことができます。
>* [!DNL Analytics]は毎時間Adobe Advertisingにデータを渡します。

* [!UICONTROL Timespent_secs_1stvisit]：訪問者の最初の訪問中にサイトに滞在した秒数。
* [!UICONTROL Timespent_secs_total]: クリックのルックバックウィンドウ内のすべての訪問でサイトに費やされた合計秒数。
* [!UICONTROL Pageviews_1stvisit]：訪問者の初回訪問時のサイトのページビュー数。
* [!UICONTROL Pageviews_total]: クリック ルックバック ウィンドウ内のすべての訪問における、サイト上のページビューの合計数。
* [[!UICONTROL Bounces]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=ja)
* [[!UICONTROL Visits]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=ja)
* [!UICONTROL ef_id_instances]: [!DNL Analytics]が[!UICONTROL EF ID]を収集した回数。

## コンバージョン指標

[!DNL Analytics]は毎日Adobe Advertisingにコンバージョン指標を渡します。

### 標準コンバージョン指標

* [[!UICONTROL Revenue]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=ja)
* [[!UICONTROL Orders]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=ja)
* [[!UICONTROL Units]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=ja)
* [[!UICONTROL Carts]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=ja)
* [[!UICONTROL Cart Views]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=ja)
* [[!UICONTROL Checkouts]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=ja)
* [[!UICONTROL Cart Additions]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=ja)
* [[!UICONTROL Cart Removals]指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=ja)

### カスタムコンバージョン指標

これらの指標はレポートスイートに固有であるため、使用可能な指標は顧客およびレポートスイートごとに異なります。

### [!DNL eVars]と[!DNL Props]から作成されたカスタムコンバージョン指標

利用可能な指標は顧客によって異なります。 「[Adobe Analytics [!DNL eVars] および [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)からコンバージョン指標を作成する」を参照してください。

### 予約済みコンバージョン指標

これらの指標はレポートスイートに固有であるため、使用可能な指標は顧客およびレポートスイートごとに異なります。

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
