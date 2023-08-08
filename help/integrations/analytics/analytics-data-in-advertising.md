---
title: '''[!DNL Analytics] Adobe Advertising''のデータ'
description: '''[!DNL Analytics] Adobe Advertising''のデータ'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: b382184072af88273570fc045d0bcebe24ed81fb
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# [!DNL Analytics] データのAdobe Advertising

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

## Analytics セグメント

で作成されたすべてのセグメント [!DNL Analytics] Experience Cloudに公開

新しいセグメントがAdobe Advertisingに表示されるまでに 24 ～ 48 時間かかります。 既存のセグメントの更新は、約 8 時間以内に同期されます。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## サイトのエンゲージメント指標

>[!NOTE]
>
>* [!DNL Analytics] は EF ID イベントをAdobe Advertisingに渡します。  デフォルトの統合では、計算指標または他のディメンション (eVar) のAdobe Advertisingへの送信はサポートされていません。 ただし、計算指標がカスタムイベントで完全に取り込める場合は、Adobe Advertisingはカスタムイベントを取り込むことができます。
>* [!DNL Analytics] は 1 時間ごとにデータをAdobe Advertisingに渡します。

* [!UICONTROL Timespent_secs_1stvisit]：訪問者の初回訪問時にサイトで費やした秒数。
* [!UICONTROL Timespent_secs_total]：クリックのルックバックウィンドウ内のすべての訪問で、サイトでの滞在時間（秒）の合計です。
* [!UICONTROL Pageviews_1stvisit]：訪問者の初回訪問中のサイトでのページビュー数。
* [!UICONTROL Pageviews_total]：クリックのルックバックウィンドウ内のすべての訪問におけるサイトでのページビューの合計数。
* [[!UICONTROL Bounces] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: [!DNL Analytics] 収集された [!UICONTROL EF ID].

## コンバージョン指標

[!DNL Analytics] では、コンバージョン指標が毎日Adobe Advertisingに渡されます。

### 標準コンバージョン指標

* [[!UICONTROL Revenue] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 指標](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### カスタムコンバージョン指標

これらの指標はレポートスイートに固有なので、利用できる指標は顧客とレポートスイートごとに異なります。

### eVar および prop から作成されたカスタムコンバージョン指標

使用可能な指標は、顧客ごとに異なります。 参照：[Adobe Analytics eVar および prop からのコンバージョン指標の作成](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### 予約済みのコンバージョン指標

これらの指標はレポートスイートに固有なので、利用できる指標は顧客とレポートスイートごとに異なります。

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
