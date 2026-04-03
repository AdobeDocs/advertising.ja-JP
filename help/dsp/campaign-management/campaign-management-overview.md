---
title: Adobe Advertising DSPのキャンペーン管理の概要
description: キャンペーン管理の階層とコンポーネントについて説明します。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: d9510790-d834-436d-8423-8d69cd50464aid: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Adobe Advertising DSPのキャンペーン管理の概要

DSP キャンペーンには、次の階層があります。

* キャンペーン
   * パッケージ
      * 配置
         * 広告
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[ キャンペーン ](/help/dsp/campaign-management/campaigns/campaign-about.md)は、フライト設定の包括的なフレームワークです。 各キャンペーンには、広告主、開始日と終了日、全体的な予算、クロスデバイスのターゲティングオプションとデフォルトの頻度制限、視認性、不正行為、ブランドセーフティ、オーディエンス検証のためのレポートオプションが設定されます。 キャンペーンレベルの設定はすべて、キャンペーン内の各パッケージとプレースメントに自動的に適用されます。

## [!UICONTROL Packages]

各キャンペーンには1つ以上の[ パッケージ ](/help/dsp/campaign-management/packages/package-about.md)を含めることができ、それぞれにプレースメントのセットが含まれます。

パッケージを使用して、設定された予算、パフォーマンス目標、カスタムペーシング戦略への配信のプレースメントをグループ化します。 DSPは、予算をパッケージ内で最もパフォーマンスの高いプレースメントに移行することで、パッケージを最適化します。 配置フォーマット、在庫タイプ、データプロバイダー、ペルソナなどの識別可能な特性にもとづいてパッケージを整理することができます。

パッケージはオプションですが、推奨されます。

## [!UICONTROL Placements]

[ プレースメント ](/help/dsp/campaign-management/placements/placement-about.md)には、同じ広告タイプの1つ以上の広告のターゲティングパラメーターが格納されます。 単一のキャンペーンまたはパッケージのプレースメントを作成し、それに広告を割り当てることができます。

## [!UICONTROL Ads]

[広告](/help/dsp/campaign-management/ads/ad-about.md)には、クリエイティブアセットとトラッキング URLが含まれています。 パートナータグシートまたはバルクタグテンプレートを使用して、サードパーティの広告配信タグを個別にアップロードしたり、一括アップロードしたりできます。 DSPが提供するネイティブのディスプレイ広告を手動で作成することもできます。

広告を設定したら、広告の実行を開始するには、各広告をプレースメントに添付する必要があります。 1つの広告を1つ以上のプレースメントにアタッチできます。

アクティブなキャンペーン内のアクティブなプレースメント内のすべてのアクティブな承認済み広告は、プレースメントのターゲティングパラメーターに基づいて実行する資格があります。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのキャンペーン管理について](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Advertising DSPでのパッケージ管理について](/help/dsp/campaign-management/packages/package-about.md)
>* [Advertising DSPでのプレースメント管理について](/help/dsp/campaign-management/placements/placement-about.md)
>* [Advertising DSPの広告管理について](/help/dsp/campaign-management/ads/ad-about.md)
>* [ キャンペーン開始のチェックリスト ](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [ パフォーマンスキャンペーンの設定に関するベストプラクティス ](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [ キャンペーン管理ビューのパフォーマンスレポートの種類](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [ キャンペーンデータビューの管理](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [ ビデオ：DSP アカウント構造とユーザーインターフェイス ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
