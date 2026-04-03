---
title: 'Adobe Advertisingのお客様向け[!DNL Adobe] [!DNL Audience Analytics] '
description: 広告のユースケースに [!DNL Adobe] [!DNL Audience Analytics]を使用する方法について説明します
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
TQID: https://experienceleague.adobe.com/XFaacUNElL25w5SMS5fzWkfRwnXr2WxhsBLe3sTccg4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 467
ht-degree: 0%

---

# Adobe Advertisingのお客様向け[!DNL Adobe] [!DNL Audience Analytics]

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ja)は、Adobe Audience ManagerとAdobe Analytics間の統合であり、Audience Managerのお客様は、サイトのアクティビティに関する詳細なインサイトを得るために[!DNL Analytics]にセグメントを送信できます。

Adobe Advertisingのお客様は、[!DNL Audience Analytics]を使用することでメリットを得ることができます。 この統合により、次のことが可能になります。

* Adobe Advertisingの露出データを[!DNL Analytics]に直接送信して、funnelの上位アクティビティが下流のサイトアクティビティに与える影響を判断します。

* Funnelにおける露出が高い広告から、マーケティングチャネルとサイトのエントリーポイントを特定します。

* [!DNL Analytics for Advertising]との統合をレイヤー化して、[Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html)のサードパーティのデモグラフィックセグメントを[!DNL Analytics for Advertising] データに組み込み、ユーザープロファイルに関する詳細なインサイトを入手します。

  [!DNL Audience Marketplace]は、「アクティベーション」サブスクリプションモデルを使用してサードパーティのデータフィードへのアクセスを提供します。このモデルを使用すると、購入者は宛先にデータを送信できます。 データが[!DNL Analytics]宛先内で使用されている場合、アクティベーション料金は適用されません。

* （Adobe Advertising DSPの広告主）包括的なジャーニー管理インサイトのために、露出セグメントを追加します。

  Advertising DSPは、Adobe Experience PlatformまたはAudience Managerのインプレッショントラッキングピクセルを実装することで、露出データをAudience Managerに実用的なシグナルとして送信できます。 同じデータを[!DNL Analytics]に転送すると、高度なデータ分析が可能になります。 詳しくは、「[Adobe Audience ManagerへのDSP メディア露出データの送信の概要](/help/integrations/audience-manager/media-data-integration/overview.md)」を参照してください。

前提条件やワークフローを含む[!DNL Audience Analytics]について詳しくは、「[Audience Analyticsの概要](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ja)」を参照してください。

## Adobe Advertising データで[!DNL Audience Analytics] データを使用する方法の例

[!DNL Analytics] [!DNL Analysis Workspace]内の結合データを使用する方法の例を次に示します。

### Funnelの上位アクティビティが下流アクティビティに与える影響を確認

Audience Managerの露出セグメントを使用して、funnelの上部サイトのアクティビティが下流サイトのアクティビティに与える影響を確認できます。 Adobe Advertisingやサードパーティのマクロ IDをトラッキングピクセルに含めることで、キャンペーンレベルからオーディエンスがアクセスしたサイトのレベルに至るまで、詳細なレベルで影響を追跡できます。

主な利点：

* Funnel/広告タイプ別の露出を追跡し、[!DNL Audience Analytics]を使用して開封率を決定し、カスタマージャーニーの次のフェーズと重複します。

* Funnelのアクティビティの上部が、下流のサイトアクティビティに与える影響を判断します。

* [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event -->と[!DNL Audience Analytics]のデータを接続して、サイトへの包括的なジャーニーを決定します。

<!-- (which includes the user's last exposure event) -->

[!DNL Analysis Workspace]で作成できるレポートの例を次に示します。

![funnelの上位アクティビティが下流のサイトアクティビティに与える影響を確認](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### ユーザープロファイル分析に[!DNL Audience Analytics]個のサードパーティのセグメントデータを使用

Audience Managerのサードパーティセグメントを利用して、利用者がサイトとどのようにやり取りしているのかをより詳細に分析できます。 サードパーティセグメントのプロファイルとメディアキャンペーンのサイトの主要業績評価指標とのエンゲージメントに基づいて、メディアをアクティベートする新しいサードパーティオーディエンスを決定するために情報を使用できます。

>[!TIP]
> `Audiences ID`が収集するその他のディメンションと同様に、`Audiences Name`全体でAudience Manager [!DNL Analytics]および[!DNL Analytics] ディメンションを使用します。

[!DNL Analysis Workspace]で作成できるレポートの例を次に示します。

![&#x200B; サードパーティのセグメントを使用したユーザープロファイル分析の強化](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe AdvertisingとAdobe Audience Managerの統合](/help/integrations/audience-manager/overview.md)
