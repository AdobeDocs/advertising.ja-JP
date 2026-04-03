---
title: キャンペーン管理に関するよくある質問
description: 変更の待ち時間や、フライト中に予算が変更された場合の状況など、キャンペーン管理について詳しく説明します。
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
TQID: https://experienceleague.adobe.com/PgO4aktP20KQzNe6SG6Vw7ahvYqHTSISQ10FCum-vQg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# キャンペーン管理に関するよくある質問

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 設定の変更の遅延

* プレースメントまたはパッケージ設定を変更する場合、変更はいつから有効になりますか？

  設定の変更は通常、すぐに有効になりますが、最大で12時間かかる場合があります。

  納品最終日の場合は、その日の早い段階で変更を加えることで、DSPには変更内容に基づいてパッケージを再調整する時間が十分にあります。 例えば、偶数ペーシングからフロントロードペーシングに移行する場合、DSPは残りのフライトで支出を配分する方法を再評価する必要があります。 フライトの最終日に1時間しか残っていない場合は、そのような変更を行わないでください。

## 計画中の予算更新

* プレースメントに変更を加えた場合、DSPはパッケージの予算を再割り当てするのにどのくらいの時間がかかりますか？

  予算配分はプレースメントのパフォーマンスにもとづいて行われ、14日間の平均を用いて評価されます。 プレースメントに変更を加えると、14日間の平均でパフォーマンスが変化する場合にのみ、予算配分が変更されます。

  パフォーマンスの変更が発生すると、DSPは、キャンペーンのタイムゾーンの午前0時（00:00）頃に発生する次の予算最適化サイクル中に、それに応じてプレースメント間のパッケージ予算を再割り当てします。

* プレースメントがパッケージから削除され、別のパッケージに追加された場合、予算はどのように再割り当てされますか？

  プレースメントの支出履歴全体がプレースメントに添付され、パッケージからパッケージに移動します。

  パッケージからプレースメントを削除すると、パッケージにはプレースメントの使用履歴がなくなります。 パッケージの予算は（パッケージの予算 – 削除されたプレースメントの予算）/飛行中に残っている時間間隔になります。 パッケージの予算は、パッケージに残っているプレースメントに割り当てられます。

  同様に、同じプレースメントを別のパッケージに追加すると、DSPは、新しいパッケージ内のすべてのプレースメントに予算を割り当てる際に、プレースメントの使用履歴を考慮します。

* フライト最終日のパッケージペーシングはどのように変更されますか？

  最終日の24時間から23時間に短縮し、荷物の予算を超えないようにします。 また、パッケージのペーシングの塗りつぶし戦略は、「[!UICONTROL Frontload]」に設定されていても、自動的に「[!UICONTROL even]」に変更されます。 つまり、東部標準時午前11:30時までに、1日の予算の65%を確保する必要があります。

>[!MORELIKETHIS]
>
>* [ パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ パフォーマンスキャンペーンの設定に関するベストプラクティス ](/help/dsp/optimization/campaign-best-practices-performance.md)
