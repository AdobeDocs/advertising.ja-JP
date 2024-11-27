---
title: 概要  [!DNL Analytics for Advertising]
description: 概要  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 8911f6ea16878bede96151f004e6de2717484140
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] の概要

*Advertising DSP[!DNL Advertising Search, Social, & Commerce]* の広告主

Adobe Analytics[!DNL Analytics for Advertising]Adobe Advertisingを統合し、各製品の機能を拡張および強化します。

この統合により、広告主は、[!DNL Analytics] ースインスタンスでのクリックスルーおよびビュースルーサイトインタラクションを追跡でき、ブランドは、広告費用がサイトエンゲージメントや重要なビジネス目標にどのように結びついているかを確認できます。

さらに、Adobe Advertisingは、既にサイトに存在するタグを使用して収集され [!DNL Analytics] 膨大なファーストパーティデータ [!DNL Analytics] アクセスできます。 これにより、より堅牢なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトレポートが可能になります。 Adobe Advertisingは、[!DNL Analytics] のデータを費用と入札の最適化にさらに使用できます。

適切に採用されると、[!DNL Analytics for Advertising] は、広告ジャーニー管理（広告を通じてサイトにユーザーを送信する行為）と web 分析を通じてそのサイトエンゲージメントを理解という、2 つの従来の役割の間の境界線をぼかします。

プライマリの利点：

* ファーストパーティサイトのリマーケティング用に [!DNL Analytics] セグメントをAdobe Advertisingに直接送信します。
* 有料メディア広告 [!DNL Analytics] 最適化するためのコンバージョンシグナルとして、カスタムイベントと標準イベントを使用します。
* [!DNL Analytics] Analysis Workspaceを活用して、サイトのエントリポイントと訪問行動をより深く理解します。
* Web アナリストと有料メディアチームの緊密な共同作業を可能にします。
* [!DNL Analytics] 内で永続的なAdobe Advertisingのビュースルー ID とクリックスルー ID を使用して、サイトエンゲージメントを把握します。
* データやピクセルを広告サーバーや他のDSPに書き出す場合には実現できないカスタム指標、カスタムディメンションおよびサイトアクティビティを使用して、Analysis Workspaceで従来の有料メディアレポートを強化します。
* Adobe Advertising内のトラッキング [!DNL Analytics] 最適化のために、既に web サイトに存在するコードを活用します。

>[!TIP]
>
> [ の概要ビデオ  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics) をご覧ください。

## Analytics for Paid メディアレポートの使用

[!DNL Analytics for Advertising] を使用すると、次のことが可能になるので、広告がサイトの行動をどのように促進するかについてのレポートとインサイトが向上します。

* [!DNL Analytics] 内で永続的なAdobe Advertisingのビュースルー ID とクリックスルー ID を使用して、サイトエンゲージメントを把握します。
* Analysis Workspaceを活用すると、サイトのエントリポイントと訪問の動作をより深く理解できます。 有料のメディアディメンションおよびイベントデータにアクセスできます。これには、Adobe Advertisingキャンペーンエンティティ名（プレースメントと広告に至るまで）とその関連指標（クリック数、インプレッション数、コストなど）が含まれます。

[!DNL Analytics] を有料メディアレポートツールとして使用するには、Analysis WorkspaceにアクセスできるExperience Cloudログインが必要です。 Adobe Advertisingチームは、Analysis WorkspaceでAdobe Advertisingデータを個々のレポートスイートにマッピングするのに役立ちます。 Adobe Advertisingデータは任意のレポートスイートに送信できますが、Adobe Advertisingにマッピングされたレポートスイートとマッピングされていないレポートスイートには注意する必要があります。レポートスイートによっては、これによりレポートされるデータが変更される場合があります。

[ 内のAdobe AdvertisingID [!DNL Analytics]](ids.md)、他の [!DNL eVars] と同様に機能し、有効期限が永続的にカスタム設定されます。 デフォルトでは、Adobe Advertising実装時のアトリビューションのルックバックウィンドウは 60 日に設定されています。 この設定を変更するには、Adobeアカウント チームに依頼してください。

Adobe Advertisingディメンションには、サフィックス「（AMO ID）」（「広告タイプ （AMO ID）」など）が付加されます。 使用可能なディメンションのリストについては、「[Analysis WorkspaceのAdobe Advertising指標 ](advertising-metrics-in-analytics.md)」を参照してください。

>[!NOTE]
>
> [!DNL Analytics] 内でAdobe Advertisingデータ（または任意のデータセット）を表示する場合、指標とレポートは [!DNL Analytics] 内で設定されたルールに基づいていることに注意してください。 データは、広告サーバーレポート、[!DNL DSP] レポート、検索エンジンレポートなど、他のレポートシステム内で表示されるものとは異なる場合があります。 [!DNL Analytics] のデータの違いを理解するには、データの有効期限、訪問を定義す [!DNL eVar] もの、ラストタッチアトリビューションと見なされる対象と持続性アトリビューションの合計との違い、およびその他の要因を知る必要があります。 詳しくは、[ とAdobe Advertisingの間で予期されるデータの相違  [!DNL Analytics]  を参照してください ](data-variances.md)。

## Analytics を使用したAdobe AdvertisingキャンペーンおよびPortfolioの強化

ピクセルを追加する必要なく、[!DNL Analytics for Advertising] は 2 つのメインシグナルをAdobe Advertisingに送信することで、より優れた最適化とオーディエンスのセグメント化の容易さを実現します。

* 入札シグナルとして使用されるコンバージョン指標：
   * 標準指標（[!UICONTROL Revenue]、[!UICONTROL Cart Views] など）。
   * ページビューや訪問指標などのサイトエンゲージメント指標。
   * カスタム売上高指標。
   * 予約済み売上高指標。
* [!DNL Analytics] で作成され、Experience Cloudに公開されたセグメント。

  [!DNL DSP] および有料検索広告でのファーストパーティサイトのリターゲティングに、[!DNL Analytics] のセグメントを使用できます。

  （[!DNL Search, Social, & Commerce] のみ）Audience Managerを持つが [!DNL Analytics] を持たない広告主は、Experience Cloudと共有される [!DNL Analytics] セグメントから、Google web サイトのタグベースのオーディエンス（リマーケティングリスト）とカスタマーマッチオーディエンス（カスタマーリスト）を作成することもできます。

### 入札シグナルとしてのサイトコンバージョン指標

[!DNL Analytics] の標準イベントとカスタムイベントを使用して、Adobe Advertisingの重み付けされた目標を作成できます。 目標は、[!DNL DSP] パッケージと検索、ソーシャル、Commerce ポートフォリオの入札に関する意思決定に役立ちます。

検索、ソーシャル、Commerceのハイブリッドポートフォリオにおける [!DNL Google Ads] および [!DNL Google Microsoft Advertising] キャンペーンの場合は、必要に応じて、目標内の [!DNL Analytics] イベントを含む目標を広告ネットワークに直接アップロードできます。広告ネットワークでは、アカウントレベルおよびキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

>[!NOTE]
>
> [!DNL Analytics] からAdobe Advertisingに計算指標をマッピングすることはできません。

Adobe Advertisingチームは、有料メディアパフォーマンスに適用されるイベントを特定し、Adobe Advertisingにマッピングするのに役立ちます。イベントは [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions] に一覧表示されます。

使用可能な指標のリストについては ](analytics-data-in-advertising.md)[Adobe Advertisingの分析指標」を参照してください。

### サイトリターゲティング用の Analytics セグメント

Adobe Advertisingは、[!DNL Analytics] とExperience Cloudの間のネイティブExperience Cloudオーディエンス統合を使用して、Advertising DSPおよび [!DNL Search, Social, & Commerce] 広告のリマーケティング目的で [!DNL Analytics] のセグメントを取り込むことができます。

[!DNL Analytics] セグメントにアクセスするには、広告主アカウントで [Experience CloudID サービス ](https://experienceleague.adobe.com/docs/id-service/using/home.html) を有効にする必要があります。 ID サービスを有効にすると、すべてのExperience Cloudセグメント（[!DNL Analytics] で作成され、Experience Cloudに公開されたセグメント、Adobe Audience Managerで作成されたセグメント、[!DNL People core service] を使用してExperience Cloudで作成されたセグメント、Adobe Experience Platformで作成され、Audience Managerを介してAdobe Advertisingに送信されたセグメントを含む）が、処理され次第、Adobe Advertising内で使用できるようになります。

[!DNL Analytics] セグメントは 24 時間以内に使用可能になり、毎日更新されます。

Experience Cloud Audiences サービスについて詳しくは、[Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) を参照してください。

## 統合の使用例 {#integration-examples}

### Analysis WorkspaceでのAdobe Advertisingデータの使用

Adobe Advertisingデータを使用してAnalysis Workspaceでビジュアルレポートを作成する方法については、ビデオ「[Workspaceとレポートの概要 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html) を参照してください。

#### レポートでの接続された TV ビュースルー変換の使用

*Advertising DSP ユーザーのみ*

CTV デバイスの広告露出をオンサイトのコンバージョンにリンクすることで、接続された TV （CTV）キャンペーンのフルファネル効果を測定できます。 新しい [!UICONTROL Landing Type] フィルター「[!UICONTROL View-through (CTV)]」は、コンバージョンを [!UICONTROL Click Through]、[!UICONTROL View Through] および [!UICONTROL View Through (CTV)] 値の別々の行に分割します。

CTV ビュースルーコンバージョン指標を表示するには、Analysis Workspaceのプレースメント ビューまたはマーケティングチャネルビューを使用します。

プレースメント ビューの使用：

1. レポートビューに CTV-spending プレースメントを含めます。

1. 「インプレッション数」、「クリック数」など、必要な指標を含めます。

1. 次のフィルターを適用します。

   広告プラットフォーム：`Advertising Cloud DSP`

   ランディングページ：`View-Through (CTV)`

マーケティングチャネル表示の使用：

1. ディメンション `Marketing Channel` を含めます。

1. 「インプレッション数」、「クリック数」など、必要な指標を含めます。

1. 次のフィルターを適用します。

   広告プラットフォーム：`Advertising Cloud DSP`

   ランディングページ：`View-Through (CTV)`

### Adobe Advertisingダッシュボードの作成

Adobe Analyticsで目標に照らしてAdobe Advertisingデータを追跡する方法については、「[Analysis WorkspaceでAdobe Advertisingダッシュボードを作成する ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html) のビデオを参照してください。

### Adobe Advertising ID をサイトの利用状況分析に使用する

曜日、時間帯、ブラウザーおよび地理的な影響を監視するAdobe Advertisingサイト入口レポートの作成方法については、ビデオ「[Adobe Advertisingサイト入口レポートの作成 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)」を参照してください。

## [!DNL Analytics for Advertising] 実装の開始方法

Adobeアカウントチームにお問い合わせください。このチームが開始に必要な初期設定を行い、組織のニーズに基づいて実装とデータ使用の計画を支援します。

>[!MORELIKETHIS]
>
>* [ ビデオ：の概要  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [ 実装の前提条件と主な情報  [!DNL Analytics for Advertising]](prerequisites.md)
>* [Analytics で使用されるAdobe AdvertisingID](ids.md)
>* [Analytics for AdvertisingのJavaScript コード ](/help/integrations/analytics/javascript.md)
>* [ とAdobe Advertisingの間で予期されるデータ  [!DNL Analytics]  相違 ](data-variances.md)
>* [Analysis WorkspaceのAdobe Advertising指標 ](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising内データ ](/help/integrations/analytics/analytics-data-in-advertising.md)
