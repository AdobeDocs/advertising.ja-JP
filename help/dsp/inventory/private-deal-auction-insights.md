---
title: プライベート取引のオークションインサイトの表示
description: オークションインサイトを使用して、プライベート取引の取引構成を分析する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: bbb99f6a-0276-4eb8-9607-75500d5634d9
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# プライベート取引のオークションインサイトの表示

オークションインサイトは、保証されている非公開取引と保証されていない非公開取引の両方の取引構成を分析できるトラブルシューティングツールです。 このツールでは、データのビジュアライゼーションを使用して、特定の期間内に [ 主要なオークション属性値 ](#auction-attributes) に対して受け取った値のトレンドと相対比率を表示します。

1. メインメニューで、**[!UICONTROL Inventory]**/**[!UICONTROL Deals].** をクリックします。

1. 取引行で、**[!UICONTROL ...]**/**[!UICONTROL Auction Insights]** をクリックします。

>[!NOTE]
>
>オークションインサイトは、プレースメント [!UICONTROL Inspector] 定ツールからも使用できます。 セグメントを開くには、[[!UICONTROL Inventory tab] ージのプレースメント [!UICONTROL Inspector]](/help/dsp/campaign-management/reports/placement-details-view.md) を開き、取引行で **[!UICONTROL ...]** > **[!UICONTROL Auction Insights]** をクリックします。

## オークション属性 {#auction-attributes}

面グラフは、次のオークション属性で使用できます。

* **広告タイプ：** オークションでリクエストされた広告タイプ（ディスプレイやオーディオなど）。

* **ブラウザー：** オークションの元となったブラウザー（Chrome、Firefox など）。

* **OS:** オークションの元となったオペレーティングシステム（OS）（Android、iOSなど）。

* **デバイスタイプ：** オークション元のデバイス（携帯電話、デスクトップなど）。

* **広告期間：** オークションでリクエストされた最大広告期間（15 秒、30 秒など）。

* **セキュア：** オークションにセキュア HTTPS URL クリエイティブアセットが必要かどうかを示します。 値：<i> セキュア </i> または <i> 非セキュア </i>。

* **MIME タイプ：** オークションでリクエストされた広告クリエイティブ MIME タイプ（mp4 や mov など）。

![ オークションのインサイト ](/help/dsp/assets/auction-insights.png)

>[!NOTE]
>
>特定の属性値にフィルターを適用して、結果を絞り込むことができます。

>[!MORELIKETHIS]
>
>* [ プライベートインベントリについて ](private-inventory-about.md)
>* [ 取引 ID のプレースメントと広告の指定 ](deal-id-attach-placements.md)
>* [ 取引の詳細レポートの表示 ](deal-view-report.md)
>* [Campaign Management ビューにおけるパフォーマンスレポートのタイプ ](/help/dsp/campaign-management/reports/campaign-reports-about.md)
