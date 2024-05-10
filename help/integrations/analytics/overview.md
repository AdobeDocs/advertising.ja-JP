---
title: 概要 [!DNL Analytics for Advertising]
description: 概要 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# 概要 [!DNL Analytics for Advertising]

*Advertising DSPを使用した広告主[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] Adobe AnalyticsとAdobe Advertisingを統合して、各製品の機能を拡張および強化します。

この統合により、広告主は、自社でのクリックスルーおよびビュースルーサイトインタラクションを追跡できます [!DNL Analytics] インスタンスを使用すると、ブランドは広告費用がサイトエンゲージメントや重要なビジネス目標にどのように結び付くかを確認できます。

さらに、Adobe Advertisingは以下のような膨大なファーストパーティデータにアクセスできます [!DNL Analytics] を使用したの収集 [!DNL Analytics] タグは既にサイト上にあります。 これにより、より堅牢なジャーニー管理、ファーストパーティリマーケティング、有料メディアサイトレポートが可能になります。 Adobe Advertisingでは、次の項目をさらに使用できます [!DNL Analytics] 費用と入札の最適化に関するデータ。

適切に採用されている場合、 [!DNL Analytics for Advertising] advertising journey management （広告を通じてサイトにユーザーを送信する行為）と、web 分析を通じてそのサイトエンゲージメントを理解という、従来の 2 つの役割の間の境界線をぼかします。

プライマリの利点：

* 送信 [!DNL Analytics] ファーストパーティサイトリマーケティング用にAdobe Advertisingに直接セグメント化します。
* 使用方法 [!DNL Analytics] 有料メディア広告を最適化するためのコンバージョンシグナルとしてのカスタムイベントおよび標準イベント。
* 利用する [!DNL Analytics] サイトのエントリポイントと訪問の行動をより深く理解するためのAnalysis Workspace。
* Web アナリストと有料メディアチームの緊密な共同作業を可能にします。
* 内で永続的なAdobe Advertisingのビュースルー ID とクリックスルー ID を使用する [!DNL Analytics] サイトエンゲージメントを理解する
* データやピクセルを広告サーバーや他のDSPに書き出す場合には実現できないカスタム指標、カスタムディメンションおよびサイトアクティビティを使用して、Analysis Workspaceで従来の有料メディアレポートを強化します。
* 利用する [!DNL Analytics] Adobe Advertising内でのトラッキングと最適化のために、既に web サイトに存在しているコード。

>[!TIP]
>
> を視聴 [の概要に関するビデオ [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Analytics for Paid メディアレポートの使用

[!DNL Analytics for Advertising] 次の項目を可能にすることで、広告がサイトの行動をどのように促進するかについてのレポートとインサイトを改善します。

* 内で永続的なAdobe Advertisingのビュースルー ID とクリックスルー ID を使用する [!DNL Analytics] サイトエンゲージメントを理解する
* Analysis Workspaceを活用すると、サイトのエントリポイントと訪問の動作をより深く理解できます。 有料のメディアディメンションおよびイベントデータにアクセスできます。これには、Adobe Advertisingキャンペーンエンティティ名（プレースメントと広告に至るまで）とその関連指標（クリック数、インプレッション数、コストなど）が含まれます。

使用目的 [!DNL Analytics] 有料メディアレポートツールを使用する場合は、Analysis WorkspaceにアクセスできるExperience Cloudログインが必要です。 Adobe Advertisingチームは、Analysis WorkspaceでAdobe Advertisingデータを個々のレポートスイートにマッピングするのに役立ちます。 Adobe Advertisingデータは任意のレポートスイートに送信できますが、Adobe Advertisingにマッピングされたレポートスイートとマッピングされていないレポートスイートには注意する必要があります。レポートスイートによっては、これによりレポートされるデータが変更される場合があります。

[内のAdobe AdvertisingID [!DNL Analytics]](ids.md) 他と同様に機能 [!DNL eVars]（カスタムの永続的な有効期限を使用）。 デフォルトでは、Adobe Advertising実装時のアトリビューションのルックバックウィンドウは 60 日に設定されています。 この設定を変更するには、Adobeアカウント チームに依頼してください。

Adobe Advertisingディメンションには、サフィックス「（AMO ID）」（「広告タイプ （AMO ID）」など）が付加されます。 参照先」[Analysis WorkspaceのAdobe Advertising指標](advertising-metrics-in-analytics.md)」を選択して使用可能なディメンションのリストを表示します。

>[!NOTE]
>
> 内でAdobe Advertisingデータ（または任意のデータセット）を表示する場合 [!DNL Analytics]指標とレポートは、内で設定されたルールに基づいていることに注意してください [!DNL Analytics]. データは、広告サーバーレポートなど、他のレポートシステム内で表示されるものとは異なる場合があります。 [!DNL DSP] レポート、または検索エンジンレポート。 のデータの違いを理解するには [!DNL Analytics]。時期を知っておく必要があります [!DNL eVar] データの有効期限、訪問を定義する内容、ラストタッチアトリビューションと見なされる内容と持続するアトリビューションの合計など、様々な要因。 詳しくは、を参照してください [間で予期されるデータの相違 [!DNL Analytics] とAdobe Advertising](data-variances.md).

## Analytics を使用したAdobe AdvertisingキャンペーンおよびPortfolioの強化

追加のピクセルを必要とせずに、 [!DNL Analytics for Advertising] 次の 2 つの主なシグナルをAdobe Advertisingに送信することで、最適化を改善し、オーディエンスのセグメント化を容易にします。

* 入札シグナルとして使用されるコンバージョン指標：
   * 標準指標（など） [!UICONTROL Revenue] および [!UICONTROL Cart Views].
   * ページビューや訪問指標などのサイトエンゲージメント指標。
   * カスタム売上高指標。
   * 予約済み売上高指標。
* で作成されたセグメント [!DNL Analytics] Experience Cloudに公開されます。

  次を使用できます [!DNL Analytics] でのファーストパーティサイトリターゲティング用のセグメント [!DNL DSP] 有料検索広告です。

  （[!DNL Search, Social, & Commerce] のみ）を使用する広告主 [!DNL Analytics] ただし、Audience Managerでは、Google web サイトのタグベースオーディエンス（リマーケティングリスト）とカスタマーマッチオーディエンス（カスタマーリスト）をから作成することはできません。 [!DNL Analytics] Experience Cloudと共有されるセグメント。

### 入札シグナルとしてのサイトコンバージョン指標

標準イベントとカスタムイベントは、次の場所から使用できます [!DNL Analytics] Adobe Advertisingにおいて重み付けされた目標を構築する。 目標は、の入札の決定に情報を提供します [!DNL DSP] パッケージと検索ポートフォリオ。

>[!NOTE]
>
> から計算指標をマッピングすることはできません [!DNL Analytics] をAdobe Advertisingに追加します。

Adobe Advertisingチームは、有料メディアのパフォーマンスに適用されるイベントを特定し、Adobe Advertisingにマッピングするのに役立ちます。このイベントは、に一覧表示されます [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

参照先」[Adobe Advertising内の Analytics 指標](analytics-data-in-advertising.md)」をクリックして使用可能な指標のリストを表示します。

### サイトリターゲティング用の Analytics セグメント

Adobe Advertisingによる取り込み可能 [!DNL Analytics] advertising DSPおよび用のリマーケティング目的のセグメント [!DNL Search, Social, & Commerce] とのネイティブExperience Cloudオーディエンス統合を使用した広告 [!DNL Analytics] とExperience Cloud。

にアクセスするには [!DNL Analytics] セグメント、広告主アカウントにはが必要です [Experience CloudID サービス](https://experienceleague.adobe.com/docs/id-service/using/home.html) 有効。 ID サービスが有効な場合、（で作成されたセグメントを含む）すべてのExperience Cloudセグメント [!DNL Analytics] を使用して、Experience Cloudに公開、Adobe Audience Managerで作成されたセグメント、Experience Cloudで作成されたセグメントに公開する [!DNL People core service]、およびAdobe Experience Platformで作成され、Audience Managerを介してAdobe Advertisingに送信されたセグメントは、処理されるとすぐにAdobe Advertising内で使用できるようになります。

[!DNL Analytics] セグメントは 24 時間以内に利用可能になり、毎日更新されます。

Experience Cloud Audiences サービスについて詳しくは、以下を参照してください。 [Experience Cloudオーディエンス](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 統合の使用例 {#integration-examples}

### Analysis WorkspaceでのAdobe Advertisingデータの使用

Adobe Advertisingデータを使用して、Analysis Workspaceで視覚的なレポートを作成する方法については、ビデオを参照してください。[Workspace とレポートの概要](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).」と入力します。

#### レポートでの接続された TV ビュースルー変換の使用

*Advertising DSP ユーザーのみ*

CTV デバイスの広告露出をオンサイトのコンバージョンにリンクすることで、接続された TV （CTV）キャンペーンのフルファネル効果を測定できます。 新しい [!UICONTROL Landing Type] フィルター&quot;[!UICONTROL View-through (CTV)]」は、コンバージョンを用に別々の行に分割します [!UICONTROL Click Through], [!UICONTROL View Through]、および [!UICONTROL View Through (CTV)] 値。

CTV ビュースルーコンバージョン指標を表示するには、Analysis Workspaceのプレースメント ビューまたはマーケティングチャネルビューを使用します。

プレースメント ビューの使用：

1. レポートビューに CTV-spending プレースメントを含めます。

1. 「インプレッション数」、「クリック数」など、必要な指標を含めます。

1. 次のフィルターを適用します。

   広告プラットフォーム： `Advertising Cloud DSP`

   ランディングページ : `View-Through (CTV)`

マーケティングチャネル表示の使用：

1. ディメンションを含める `Marketing Channel`.

1. 「インプレッション数」、「クリック数」など、必要な指標を含めます。

1. 次のフィルターを適用します。

   広告プラットフォーム： `Advertising Cloud DSP`

   ランディングページ : `View-Through (CTV)`

### Adobe Advertisingダッシュボードの作成

Analysis Workspaceで目標に照らしてAdobe Advertisingデータを追跡する方法については、ビデオを参照してください。[Adobe AnalyticsでのAdobe Advertisingダッシュボードの作成](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).」と入力します。

### Adobe Advertising ID をサイトの利用状況分析に使用する

Adobe Advertisingサイト入口レポートを作成して、曜日、時間帯、ブラウザー、地理的な影響を監視する方法については、ビデオ「」を参照してください[Adobe Advertisingサイト入口レポートの作成](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).」と入力します。

>[!MORELIKETHIS]
>
>* [ビデオ：の概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [実装の前提条件と主な情報 [!DNL Analytics for Advertising]](prerequisites.md)
>* [Analytics が使用するAdobe Advertising ID](ids.md)
>* [Analytics for Advertising 用 JavaScript コード](/help/integrations/analytics/javascript.md)
>* [間で予期されるデータの相違 [!DNL Analytics] とAdobe Advertising](data-variances.md)
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising内のデータ](/help/integrations/analytics/analytics-data-in-advertising.md)
