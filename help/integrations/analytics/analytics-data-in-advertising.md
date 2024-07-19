---
title: 'Adobe Advertising内の [!DNL Analytics] データ'
description: 'Adobe Advertising内の [!DNL Analytics] データ'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Adobe Advertising内の [!DNL Analytics] データ

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

## Analytics セグメント

[!DNL Analytics] で作成され、Experience Cloudに公開されたすべてのセグメント。

新しいセグメントのAdobe Advertisingが表示されるまで、24～48 時間かかります。 既存のセグメントの更新は、約 8 時間以内に同期されます。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## サイトエンゲージメント指標

>[!NOTE]
>
>* [!DNL Analytics] は、Adobe Advertisingに EF ID [!DNL eVar] のイベントを渡します。  デフォルトの統合では、計算指標や他のディメンション（[!DNL eVars]）をAdobe Advertisingに送信することはサポートされていません。 ただし、カスタムイベントで計算指標をすべて取り込むことができる場合は、Adobe Advertisingはカスタムイベントを取り込むことができます。
>* [!DNL Analytics] は、データを毎時Adobe Advertisingに渡します。

* [!UICONTROL Timespent_secs_1stvisit]：訪問者の最初の訪問中にサイトに滞在した秒数。
* [!UICONTROL Timespent_secs_total]：クリックルックバックウィンドウ内のすべての訪問でサイトに費やした合計秒数。
* [!UICONTROL Pageviews_1stvisit]：訪問者の初回訪問中のサイトのページビュー数。
* [!UICONTROL Pageviews_total]：クリックルックバックウィンドウ内のすべての訪問でのサイトのページビュー数の合計。
* [[!UICONTROL Bounces] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:[!UICONTROL EF ID] を収集し [!DNL Analytics] 回数。

## コンバージョン指標

[!DNL Analytics] では、コンバージョン指標を毎日Adobe Advertisingに渡しています。

### 標準コンバージョン指標

* [[!UICONTROL Revenue] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 指標 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### カスタムコンバージョン指標

これらの指標はレポートスイートに固有なので、使用できる指標は、顧客とレポートスイートによって異なります。

### [!DNL eVars] および [!DNL Props] から作成されたカスタムコンバージョン指標

使用可能な指標は、顧客ごとに異なります。 [Adobe Analyticsからのコンバージョン指標の作成  [!DNL eVars]  および  [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)」を参照してください。

### 予約済みコンバージョン指標

これらの指標はレポートスイートに固有なので、使用できる指標は、顧客とレポートスイートによって異なります。

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [Analysis WorkspaceのAdobe Advertising指標 ](/help/integrations/analytics/advertising-metrics-in-analytics.md)
