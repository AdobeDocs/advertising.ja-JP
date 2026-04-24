---
title: ' [!DNL Analytics for Advertising]の概要'
description: ' [!DNL Analytics for Advertising]の概要'
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
TQID: https://experienceleague.adobe.com/OHxJO1mtbzOtt5oGDJF26xSuVLG-HnRDdIGDrUH2pzk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1306
ht-degree: 0%

---

# [!DNL Analytics for Advertising]の概要

*Advertising Creative、Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*&#x200B;の広告主

[!DNL Analytics for Advertising]は、Adobe AnalyticsとAdobe Advertisingを統合して、各製品の機能を拡張および強化します。

この統合により、広告主は、[!DNL Analytics] インスタンスでのクリックスルーとビュースルーサイトのインタラクションを追跡できるようになり、広告費がどのようにサイトエンゲージメントや重要なビジネス目標につながるのかを把握できるようになります。

さらに、Adobe Advertisingは、サイトにすでに[!DNL Analytics]個のタグを使用して[!DNL Analytics]が収集する膨大な1st パーティデータにアクセスできます。 これにより、より強固なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトレポートが可能になります。 Adobe Advertisingでは、さらに[!DNL Analytics] データを使用して経費と入札最適化を行うことができます。

[!DNL Analytics for Advertising]は、適切に使用すると、従来の2つの役割の境界線をぼかします。広告ジャーニー管理（広告を通じてサイトにユーザーを送信する行為）と、web分析を通じてそのサイトエンゲージメントを理解することです。

プライマリの利点：

* [!DNL Analytics] セグメントをAdobe Advertisingに直接送信して、ファーストパーティサイトのリマーケティングを行います。
* 有料メディア広告を最適化するためのコンバージョンシグナルとして、[!DNL Analytics]個のカスタムイベントと標準イベントを使用します。
* [!DNL Analytics] Analysis Workspaceを活用して、サイトのエントリポイントと訪問の動作をより深く理解します。
* web アナリストと有料メディア部門の緊密な連携を実現する。
* 永続的なAdobe Advertising ビュースルーおよびクリックスルーIDを[!DNL Analytics]内で使用して、サイトエンゲージメントを把握します。
* Analysis Workspaceで従来の有料メディアレポートを強化しましょう。カスタムメトリクス、カスタムディメンションおよびサイトアクティビティは、データやピクセルを広告サーバーや他のDSPに書き出す際に達成不可能です。
* Adobe Advertising内でのトラッキングと最適化のために、web サイトに既に存在する[!DNL Analytics] コードを利用します。

>[!TIP]
>
>  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics)に関する[ ビデオの概要をご覧ください。

## Analyticsを使用した有料メディアレポート

[!DNL Analytics for Advertising]では、次のことが可能になり、広告がサイトの動作をどのように促進するかについてのレポートとinsightが改善されます。

* 永続的なAdobe Advertising ビュースルーおよびクリックスルーIDを[!DNL Analytics]内で使用して、サイトエンゲージメントを把握します。
* Analysis Workspaceを活用して、サイトのエントリポイントと訪問行動をより詳細に把握します。 Adobe Advertisingのキャンペーンエンティティ名（プレースメントや広告に至るまで）や、クリック数、インプレッション数、コストなどの関連指標を含む、有料メディアのディメンションおよびイベントデータにアクセスできます。

有料メディアレポートツールとして[!DNL Analytics]を使用するには、Analysis WorkspaceにアクセスできるAdobe CX Enterprise（旧Adobe Experience Cloud）ログインが必要です。 Adobe Advertising チームは、Adobe Advertising データをAnalysis Workspaceの個々のレポートスイートにマッピングするのに役立ちます。 Adobe Advertising データを任意のレポートスイートに送信できますが、Adobe Advertisingにマッピングされたレポートスイートとそうでないレポートスイートを認識しておく必要があります。 レポートスイートによっては、レポートされるデータが変更される場合があります。

 [!DNL Analytics]](ids.md)内の[Adobe Advertising IDは、他の[!DNL eVars]と同様に、カスタムの永続的な有効期限で機能します。 デフォルトでは、Adobe Advertisingの実装中はアトリビューションルックバックウィンドウが60日に設定されます。 この設定を変更するには、Adobe アカウントチームと連携してください。

Adobe Advertising ディメンションには、接尾辞「（AMO ID）」（「Ad Type （AMO ID）」など）が追加されます。 使用可能なディメンションの一覧については、「[Analysis WorkspaceのAdobe Advertising指標](advertising-metrics-in-analytics.md)」を参照してください。

>[!NOTE]
>
> [!DNL Analytics]内のAdobe Advertising データ（または任意のデータセット）を表示する場合、指標とレポートは、[!DNL Analytics]内で設定されたルールに基づいていることに注意してください。 データは、広告サーバーレポート、[!DNL DSP] レポート、検索エンジンレポートなど、他のレポートシステムで表示されるものとは異なる場合があります。 [!DNL Analytics]のデータの違いを理解するには、[!DNL eVar] データの有効期限、訪問の定義、ラストタッチアトリビューションと永続アトリビューションの合計の比較、その他の要因を知る必要があります。 詳しくは、[Adobe Advertising](data-variances.md)と [!DNL Analytics] の間の予想されるデータの差異を参照してください。

## Adobe Analyticsを使用したAdobe Advertisingのキャンペーンとポートフォリオの強化

追加ピクセルを必要とせずに、[!DNL Analytics for Advertising]は2つの主要シグナルをAdobe Advertisingに送信することで、より優れた最適化と簡単なオーディエンスセグメンテーションを可能にします。

* 入札シグナルとして使用されるコンバージョン指標：
   * [!UICONTROL Revenue]や[!UICONTROL Cart Views]などの標準指標。
   * ページビューや訪問指標などのサイトエンゲージメント指標。
   * カスタム収益指標：
   * 予約済みの収益指標：
* [!DNL Analytics]で作成され、CX Enterpriseに公開されたセグメント。

  [!DNL Analytics] セグメントは、[!DNL DSP]、[!DNL Creative]および有料検索広告のファーストパーティサイトのリターゲティングに使用できます。

  （[!DNL Search, Social, & Commerce]のみ） [!DNL Analytics]を持つがAudience Managerを持たない広告主は、Googleと共有される[!DNL Analytics] セグメントからCX Enterprise web サイトのタグベースのオーディエンス（リマーケティングリスト）とカスタマーマッチオーディエンス（顧客リスト）を作成することもできます。

### 入札シグナルとしてのサイトコンバージョン指標

[!DNL Analytics]の標準イベントとカスタムイベントを使用して、Adobe Advertisingで重み付けされた目標を構築できます。 目標は、[!DNL DSP] パッケージとSearch, Social, &amp; Commerce ポートフォリオの入札決定に反映されます。

Search, Social, &amp; Commerce ハイブリッド ポートフォリオの[!DNL Google Ads]および[!DNL Google Microsoft Advertising]件のキャンペーンの場合、オプションで、目的（目的の[!DNL Analytics]件を含む）を広告ネットワークに直接アップロードして、アカウントレベルおよびキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

>[!NOTE]
>
> [!DNL Analytics]の計算指標をAdobe Advertisingにマッピングすることはできません。

Adobe Advertising チームは、有料メディアのパフォーマンスに適用されるイベントを特定し、Adobe Advertisingにマッピングするのに役立ちます。

使用可能な指標の一覧については、「[Adobe AdvertisingのAnalytics指標](analytics-data-in-advertising.md)」を参照してください。

### サイトリターゲティング用の分析セグメント

Adobe Advertisingは、[!DNL Analytics]とCX EnterpriseのネイティブなCX Enterprise Audiences統合を使用して、[!DNL Creative]、[!DNL DSP]、[!DNL Search, Social, & Commerce]の広告のリマーケティング目的で[!DNL Analytics] セグメントを取り込むことができます。

[!DNL Analytics] セグメントにアクセスするには、広告主アカウントで[Experience Cloud ID サービス ](https://experienceleague.adobe.com/docs/id-service/using/home.html)を有効にする必要があります。 ID サービスが有効になっている場合、すべてのCX Enterprise セグメントは、処理されるとすぐにAdobe Advertising内で利用できるようになります。 CX Enterprise セグメントには、[!DNL Analytics]で作成されCX Enterpriseに公開されたセグメント、Adobe Audience Managerで作成されたセグメント、[!DNL People core service]を使用してCX Enterpriseで作成されたセグメント、Adobe Experience Platformで作成されAudience Managerを介してAdobe Advertisingに送信されたセグメントが含まれます。

[!DNL Analytics]個のセグメントは24時間以内に利用でき、毎日更新されます。

CX Enterprise Audiences サービスについて詳しくは、[CX Enterprise Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)を参照してください。

## 統合機能の使用例 {#integration-examples}

### Analysis WorkspaceでのAdobe Advertising データの使用

Adobe Advertising データを使用してAnalysis Workspaceでビジュアルレポートを作成する方法については、ビデオ「[Workspaceとレポートの概要](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)」を参照してください。

#### レポートでのコネクテッド TV ビュースルーコンバージョンの使用

*Advertising DSP ユーザーのみ*

CTV デバイス上の広告への露出をオンサイトのコンバージョンに結びつけることで、コネクテッド TV （CTV）キャンペーンのfunnel全体の効果を測定できます。 新しい[!UICONTROL Landing Type] フィルター「[!UICONTROL View-through (CTV)]」は、コンバージョンを[!UICONTROL Click Through]、[!UICONTROL View Through]、および[!UICONTROL View Through (CTV)]の値に対して別々の行に分割します。

CTV ビュースルーコンバージョン指標を表示するには、Analysis Workspaceの配置ビューまたはマーケティングチャネルビューのいずれかを使用します。

プレースメントビューの使用：

1. レポートビューにCTV支出の配置を含めます。

1. 「インプレッション数」、「クリック数」など、希望する指標を含めます。

1. 次のフィルターを適用します。

   広告プラットフォーム：`Advertising Cloud DSP`

   ランディングページ：`View-Through (CTV)`

マーケティングチャネルビューの使用：

1. ディメンション `Marketing Channel`を含めます。

1. 「インプレッション数」、「クリック数」など、希望する指標を含めます。

1. 次のフィルターを適用します。

   広告プラットフォーム：`Advertising Cloud DSP`

   ランディングページ：`View-Through (CTV)`

### Adobe Advertising ダッシュボードの作成

Adobe Analyticsで目標に対してAdobe Advertising データを追跡する方法については、ビデオ「[Analysis WorkspaceでAdobe Advertising ダッシュボードを作成](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)」を参照してください。

### Adobe Advertising IDを使用したサイトエントリ分析

Adobe Advertising サイト入口レポートを作成して、曜日、時間帯、ブラウザー、地理的な影響をモニターする方法については、ビデオ「[Adobe Advertising サイト入口レポートを作成](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)」を参照してください。

## [!DNL Analytics for Advertising]実装の開始方法

Adobeのアカウントチームにお問い合わせください。最初に必要な設定を行い、組織のニーズに基づいて導入とデータ利用を計画するのに役立ちます。

>[!MORELIKETHIS]
>
>* [ ビデオ： [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)の概要
>* [実装の前提条件と主要情報 [!DNL Analytics for Advertising]](prerequisites.md)
>* Analyticsで使用される[Adobe Advertising ID](ids.md)
>* [Advertising向けAnalyticsのJavaScript コード ](/help/integrations/analytics/javascript.md)
>* [ [!DNL Analytics] とAdobe Advertising](data-variances.md)の間の予期されるデータの差異
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertisingのデータ ](/help/integrations/analytics/analytics-data-in-advertising.md)
