---
title: '[!DNL Adobe] [!DNL Audience Analytics] Adobe Advertisingのお客様向け'
description: 広告のユースケースに  [!DNL Adobe] [!DNL Audience Analytics] の使用方法を学ぶ
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Adobe Advertisingのお客様向けの [!DNL Adobe] [!DNL Audience Analytics]

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) は、Adobe Audience ManagerとAdobe Analyticsの統合で、Audience Managerのお客様はセグメントを [!DNL Analytics] に送信して、サイトアクティビティに関する有益なインサイトを得ることができます。

Adobe Advertisingのお客様は、[!DNL Audience Analytics] を使用することでメリットを得ることができます。 この統合により、次のことが可能になります。

* Adobe Advertisingの漏洩データを [!DNL Analytics] に直接送信して、funnelの上位アクティビティがダウンストリームサイトアクティビティに与える影響を判断します。

* funnelの公開量上限の広告からマーケティングチャネルとサイトのエントリポイントを特定します。

* [!DNL Analytics for Advertising] との統合を強化し、[Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) のサードパーティの人口統計セグメントと [!DNL Analytics for Advertising] データを組み込んで、ユーザープロファイルに関するより多くのインサイトを得ることができます。

  [!DNL Audience Marketplace] では、購入者が宛先にデータを送信できる「アクティベーション」サブスクリプションモデルを使用して、サードパーティのデータフィードにアクセスできます。 データが [!DNL Analytics] の宛先内で使用されている場合、アクティベーション料金は適用されません。

* （Advertising DSPを使用する広告主）包括的なジャーニー管理のインサイトを得るために、さらに公開セグメントを追加します。

  Advertising DSPは、Adobe Experience PlatformまたはAudience Managerのインプレッショントラッキングピクセルの実装を通じて、公開データを実用的なシグナルとしてAudience Managerに送信できます。 同じデータを [!DNL Analytics] に転送すると、高度なデータ分析が可能になります。 詳しくは、[DSP media の公開データをAdobe Audience Managerに送信する方法の概要」を参照 &#x200B;](/help/integrations/audience-manager/media-data-integration/overview.md) てください。

前提条件やワークフローなど、[!DNL Audience Analytics] について詳しくは、「[Audience Analyticsの概要 &#x200B;](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)」を参照してください。

## Adobe Advertising data での [!DNL Audience Analytics] data の使用例

[!DNL Analytics] 内で結合されたデータの使用例を次 [!DNL Analysis Workspace] 示します。

### funnelの上位アクティビティがダウンストリームアクティビティに与える影響を確認

Audience Managerの公開セグメントを使用して、funnelの上位サイトアクティビティがダウンストリームサイトアクティビティに与える影響を確認します。 Adobe Advertisingまたはサードパーティのマクロ ID をトラッキングピクセルに含めて、キャンペーンレベルからユーザーが公開されたサイトのレベルに至るまで、詳細レベルでの影響をトラッキングします。

主なメリット：

* funnel/広告タイプ別にエクスポージャーを追跡し、[!DNL Audience Analytics] れを使用してエントリレートを判断し、カスタマージャーニーの次のフェーズと重複させます。

* funnelの上位アクティビティがダウンストリームサイトアクティビティに与える影響を判断します。

* [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> と [!DNL Audience Analytics] データ <!-- (which includes the user's last exposure event) --> ースを接続して、サイトへの全体的なジャーニーを決定します。

[!DNL Analysis Workspace] で作成できるレポートの例を次に示します。

![funnel アクティビティの増加がダウンストリームサイトアクティビティに与える影響を参照 &#x200B;](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### ユーザープロファイル [!DNL Audience Analytics] 分析にサードパーティのセグメントデータを使用

サードパーティのAudience Manager セグメントを使用すると、ユーザーによるサイトの操作を詳細に分析できます。 情報を使用して、サードパーティのセグメントのプロファイルがメディアキャンペーンのサイトの主要パフォーマンス指標とどのように関わるかに基づいて、メディアをアクティブ化する新しいサードパーティオーディエンスを決定できます。

>[!TIP]
> `Audiences ID` が収集する他のディメンションと同様に、Audience Manager `Audiences Name` および [!DNL Analytics] ディメンションを [!DNL Analytics] 全体で使用します。

[!DNL Analysis Workspace] で作成できるレポートの例を次に示します。

![&#x200B; サードパーティセグメントを使用したユーザープロファイル分析のエンリッチメント &#x200B;](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe AdvertisingとAdobe Audience Managerの統合 &#x200B;](/help/integrations/audience-manager/overview.md)
