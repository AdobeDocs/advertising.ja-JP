---
title: '[!DNL Adobe] [!DNL Audience Analytics] Adobe Advertisingカスタマー向け」'
description: 広告のユースケースに  [!DNL Adobe] [!DNL Audience Analytics] の使用方法を学ぶ
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Adobe Advertising版のお客様向けの [!DNL Adobe] [!DNL Audience Analytics]

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ja) は、Adobe Audience ManagerとAdobe Analyticsの統合で、Audience Managerのお客様はセグメントを [!DNL Analytics] に送信して、サイトアクティビティに関するエンリッチメントされたインサイトを得ることができます。

Adobe Advertisingのお客様は、[!DNL Audience Analytics] を使用することでメリットを得ることができます。 この統合により、次のことが可能になります。

* Adobe Advertisingの漏洩データを [!DNL Analytics] に直接送信して、上位ファネルアクティビティがダウンストリームサイトアクティビティに与える影響を判断します。

* 上位ファネル暴露広告からマーケティングチャネルとサイトエントリポイントを決定します。

* [!DNL Analytics for Advertising] との統合を強化し、[Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html?lang=ja) のサードパーティの人口統計セグメントと [!DNL Analytics for Advertising] データを組み込んで、ユーザープロファイルに関するより多くのインサイトを得ることができます。

  [!DNL Audience Marketplace] では、購入者が宛先にデータを送信できる「アクティベーション」サブスクリプションモデルを使用して、サードパーティのデータフィードにアクセスできます。 データが [!DNL Analytics] の宛先内で使用されている場合、アクティベーション料金は適用されません。

* （Advertising DSPを使用する広告主）包括的なジャーニー管理のインサイトを得るために、さらに公開セグメントを追加します。

  Advertising DSPは、Adobe Experience PlatformまたはAudience Managerのインプレッショントラッキング画素の実装を通じて、曝露データを実用的なシグナルとしてAudience Managerに送信できます。 同じデータを [!DNL Analytics] に転送すると、高度なデータ分析が可能になります。 詳しくは、[Adobe Audience Managerを使用したAdobe Advertisingメディアデータ統合の概要」 ](/help/integrations/audience-manager/media-data-integration/overview.md) 参照してください。

前提条件やワークフローなど、[!DNL Audience Analytics] について詳しくは、「[Audience Analyticsの概要 ](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ja)」を参照してください。

## Adobe Advertisingデータを含む [!DNL Audience Analytics] データの使用例

[!DNL Analysis Workspace] 内で結合されたデータの使用例を次 [!DNL Analytics] 示します。

### 上位ファネルアクティビティがダウンストリームアクティビティに与える影響を確認

Audience Manager曝露セグメントを使用して、上位ファネルサイトのアクティビティがダウンストリームサイトのアクティビティに与える影響を確認します。 Adobe Advertisingまたはサードパーティのマクロ ID をトラッキングピクセルに含めて、キャンペーンレベルからユーザーが公開されたサイトのレベルに至るまで、詳細レベルでの影響をトラッキングします。

主なメリット：

* ファネル/広告タイプ別にエクスポージャーを追跡し、[!DNL Audience Analytics] れを使用してエントリレートを決定し、カスタマージャーニーの次のフェーズと重複させます。

* 上位ファネルアクティビティがダウンストリームサイトアクティビティに与える影響を決定します。

* [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> と [!DNL Audience Analytics] データ <!-- (which includes the user's last exposure event) --> ースを接続して、サイトへの全体的なジャーニーを決定します。

[!DNL Analysis Workspace] で作成できるレポートの例を次に示します。

![ 上位ファネルアクティビティがダウンストリームサイトアクティビティに与える影響を確認 ](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### ユーザープロファイル [!DNL Audience Analytics] 分析にサードパーティセグメントデータを使用する

サードパーティのAudience Managerセグメントを使用すると、ユーザーによるサイトの操作を詳細に分析できます。 情報を使用して、サードパーティのセグメントのプロファイルがメディアキャンペーンのサイトの主要パフォーマンス指標とどのように関わるかに基づいて、メディアをアクティブ化する新しいサードパーティオーディエンスを決定できます。

>[!TIP]
> 収集される他のディメンションと同様に、[!DNL Analytics] 全体でAudience Manager`Audiences ID` および `Audiences Name` のディメンションを使用 [!DNL Analytics] ます。

[!DNL Analysis Workspace] で作成できるレポートの例を次に示します。

![ サードパーティセグメントを使用したユーザープロファイル分析のエンリッチメント ](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Audience ManagerとのAdobe Advertising統合 ](/help/integrations/audience-manager/overview.md)
