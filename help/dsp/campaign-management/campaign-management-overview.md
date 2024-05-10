---
title: Advertising DSPでのCampaign Managementの概要
description: キャンペーン管理の階層とコンポーネントについて説明します。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Advertising DSPでのCampaign Managementの概要

DSP キャンペーンには次の階層があります。

* キャンペーン
   * パッケージ
      * プレースメント
         * 広告
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[キャンペーン](/help/dsp/campaign-management/campaigns/campaign-about.md) は、フライト設定の包括的なフレームワークです。 各キャンペーンは、広告主、開始日と終了日、全体的な予算、クロスデバイスターゲティングオプションとデフォルトのフリークエンシーキャップ、ビューアビリティ、詐欺、ブランドセーフティ、オーディエンス検証のレポートオプションで設定されます。 キャンペーンレベルのすべての設定は、キャンペーン内の各パッケージおよびプレースメントに自動的に適用されます。

## [!UICONTROL Packages]

各キャンペーンには 1 つ以上を含めることができます [パッケージ](/help/dsp/campaign-management/packages/package-about.md)。各には、プレースメントのセットが含まれます。

パッケージを使用すると、設定した予算、パフォーマンス目標、カスタムペーシング戦略に配信するプレースメントをグループ化できます。 DSPでは、パッケージ内の最もパフォーマンスの高いプレースメントに予算をシフトすることで、パッケージを最適化します。 プレースメント形式、インベントリタイプ、データプロバイダー、ペルソナ、その他の識別可能な特性でパッケージを整理できます。

パッケージはオプションですが、推奨されます。

## [!UICONTROL Placements]

A [配置](/help/dsp/campaign-management/placements/placement-about.md) 同じ広告タイプの 1 つ以上の広告に対するターゲティングパラメーターを格納します。 1 つのキャンペーンまたはパッケージのプレースメントを作成し、それに広告を割り当てることができます。

## [!UICONTROL Ads]

[広告](/help/dsp/campaign-management/ads/ad-about.md) クリエイティブアセットとトラッキング URL を含めます。 サードパーティの広告サービングタグは、個別にまたは一括でアップロードできます。それには、パートナータグシートまたは一括タグテンプレートを使用します。 また、DSPが提供するネイティブディスプレイ広告を手動で作成することもできます。

広告を設定したら、広告の実行を開始するために、各広告をプレースメントに添付する必要があります。 1 つの広告を 1 つ以上のプレースメントに添付できます。

アクティブなキャンペーンのアクティブなプレースメントに含まれるすべてのアクティブで承認済みの広告は、プレースメントのターゲティングパラメーターに基づいて実行できます。

>[!MORELIKETHIS]
>
>* [Campaign Managementについて](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [パッケージ管理について](/help/dsp/campaign-management/packages/package-about.md)
>* [プレースメント管理について](/help/dsp/campaign-management/placements/placement-about.md)
>* [Ad Management について](/help/dsp/campaign-management/ads/ad-about.md)
>* [Campaign Launch チェックリスト](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [パフォーマンスキャンペーンの設定のベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Campaign Management ビューでのパフォーマンスレポートのタイプ](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [キャンペーンデータビューの管理](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [ビデオ：DSP アカウント構造とユーザーインターフェイス](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
