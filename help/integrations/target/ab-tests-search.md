---
title: Adobe TargetでAdobe Advertising Search、Social、Commerce広告のA/B テストを設定する
description: Search, Social, & Commerceで [!DNL Target] 広告および [!DNL Google Ads] 広告の [!DNL Microsoft Advertising] でA/B テストを設定する方法について説明します。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
TQID: https://experienceleague.adobe.com/eu1dRdsQlJX4IlHLTUDyJ69r0txFvFUdzUiXpSAlpU8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 867
ht-degree: 0%

---

# Adobe TargetでAdvertising Search、Social、Commerce広告のA/B テストを設定する

*Advertising Search, Social, &amp; Commerceのみの広告主*

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

Adobe AdvertisingとAdobe Targetを使用すると、デジタル広告トラフィック [!DNL Google Ads]と[!DNL Microsoft Advertising]に対するランディングページ エクスペリエンス A/B テストを簡単に設定して、以下を行うことができます。

* コンバージョン率（CVR）と獲得効率の指標（CPA、CPL、CACなど）を改善します。

* 広告に合わせて、よりパーソナライズされたランディングページ体験を提供します（例えば、画像/動画のクリエイティブ、コピー、キーワード、その他の広告シグナルをランディングページに一致させます）。

また、Adobe Analyticsに統合されたAdvertising[[!DNL Analytics] 用のネイティブ ](/help/integrations/analytics/overview.md)と[[!DNL Analytics]  [!DNL Target]用の](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)統合レポートディメンションを組み合わせて、[!DNL Analytics]個の指標と成功イベントを使用してテストデータを測定および視覚化することもできます。

Search, Social, &amp; Commerceの広告からのクリックスルーのトラフィックについて、[!DNL Target]でA/B テストを設定する手順と、[!DNL Analytics]でテストを測定して視覚化する方法に関するヒントについては、次の節を参照してください。

## 前提条件

### 必要な製品

* Search, Social, &amp; Commerce
* [!DNL Target]

### 推奨される製品と統合

* [!DNL Analytics]

* Advertising[[!DNL Analytics] 統合](/help/integrations/analytics/overview.md)の<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics]  [!DNL Target]統合用](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

## 手順1: Search, Social, &amp; Commerce用に[!DNL Target]でA/B テストアクティビティを作成する

次の手順では、Search, Social, &amp; Commerceのユースケースに関する情報を強調表示します。

1. [Adobe Targetにログイン ](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. [A/B テストを作成](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. 「**[!UICONTROL Enter Activity URL]**」フィールドに、テストのランディングページ URLを入力します。

   1. 「**[!UICONTROL Goal]**」フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >[!DNL Analytics]が[!DNL Target]内のデータソースとして有効になっており、正しいレポートスイートが選択されていることを確認してください。

   1. **[!UICONTROL Priority]**&#x200B;を`High`または`999`に設定して、テストセグメントのユーザーが誤ったオンサイトエクスペリエンスを受け取ったときに競合を防ぎます。


   1. **[!UICONTROL Reporting Settings]**&#x200B;内で、Search, Social, &amp; Commerce アカウントに接続されている&#x200B;**[!UICONTROL Company Name]**&#x200B;と&#x200B;**[!UICONTROL Report Suite]**&#x200B;を選択します。

      その他のレポートのヒントについては、「[ レポートのベストプラクティスとトラブルシューティング ](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)」を参照してください。

   1. 「**[!UICONTROL Date Range]**」フィールドに、テストの適切な開始日と終了日を入力します。

   1. **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**&#x200B;を選択します。 「**[!UICONTROL Value]**」フィールドに、Search, Social, &amp; Commerceの関連する広告ネットワークエンティティの[!UICONTROL Network Account ID]、[!UICONTROL Network Campaign ID]、[!UICONTROL Network Adgroup ID]または[!UICONTROL Network Ad ID]を入力します。 これにより、エンティティのクリックスルーオーディエンスに[!DNL Target] クエリ文字列パラメーターを使用できます。

      IDは、[関連するID列をエンティティビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)に追加することで見つけることができます。

      ![[!UICONTROL Network Account ID] ビュー[!UICONTROL Accounts]の](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] ビュー[!UICONTROL Accounts]列の")列

      サポートが必要な場合は、Adobe アカウントチームにお問い合わせください。

   1. **[!UICONTROL Traffic Allocation Method]**&#x200B;の場合、**[!UICONTROL Manual (Default)]**&#x200B;を選択し、オーディエンスを50/50に分割します。

   1. アクティビティを保存します。

1. [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)を使用して、A/B テスト ランディングページ テンプレートにデザイン変更を加えます。

   * エクスペリエンス A: パーソナライゼーションなしでデフォルト/コントロールのランディングページエクスペリエンスであるため、編集しないでください。

   * エクスペリエンス B: [!DNL Target] ユーザーインターフェイスを使用して、テストに含まれるアセット（見出し、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズします。

   >[!NOTE]
   >
   >クリエイティブテストのユースケースなど、Adobeのアカウントチームにお問い合わせください。

## 手順2: [!DNL Analytics for Target]で[!DNL Analytics] Analysis Workspaceを設定する

[!DNL Analytics for Target] （A4T）は、広告主が[!DNL Target]個のコンバージョン指標とオーディエンスセグメントに基づいて[!DNL Analytics]個のアクティビティを作成し、[!DNL Analytics]をレポートソースとして使用して結果を測定できるクロスソリューション統合です。 そのアクティビティのすべてのレポートとセグメント化は、[!DNL Analytics] データ収集に基づいています。

実装手順へのリンクを含む[!DNL Analytics for Target]について詳しくは、「[Adobe Analytics as the reporting source for Adobe Target （A4T） ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)」を参照してください。

### [!DNL Analytics for Target] パネルの設定

Analysis Workspaceで、[!DNL Analytics for Target panel]を設定して、[!DNL Target]のアクティビティとエクスペリエンスを分析します。 レポートに関する次の重要なポイントと情報を考慮してください。

#### 指標

* テストを実行したAdobe Advertising アカウント、キャンペーンまたは広告グループ <!-- only applicable entities? -->に固有のパネルをワークスペース内に作成します。 サマリービジュアライゼーションを使用して、[!DNL Target] テストのパフォーマンスと同じレポートでAdobe Advertising指標を表示します。

* 訪問やコンバージョンなどのオンサイト指標を活用してパフォーマンスを測定し、

* Adobe Advertisingの集約されたメディア指標（インプレッション数、クリック数、コストなど）は、[!DNL Target]指標と一致させることができません。

#### ディメンション

次のディメンションは[!DNL Analytics for Target]に関連しています：

* **ターゲットアクティビティ**:A/B テストの名前

* **ターゲットエクスペリエンス**: アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **ターゲットアクティビティ** > **エクスペリエンス**：同じ行のアクティビティ名とエクスペリエンス名

### [!DNL Target] データのAnalyticsのトラブルシューティング

Analysis Workspace内で、アクティビティとエクスペリエンスのデータが最小限に抑えられているか入力されていないことがわかったら、次の操作を行います。

* [!UICONTROL Supplemental Data ID]と[!DNL Target]の両方に同じ[!DNL Analytics] （SDID）が使用されていることを確認します。 SDID値を確認するには、キャンペーンがユーザーを促進しているランディングページで[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)を使用します。

[Adobe Debuggerの補足データ ID （SDID）値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a）Adobe Debuggerに表示されている[!UICONTROL Hostname]が[!UICONTROL Solutions] > [!UICONTROL Target]に一致することを確認しますb）アクティビティの[!UICONTROL Tracking Server]に表示されている[!DNL Target]が（[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]に一致することを確認します。

  [!DNL Analytics For Target]では、Analytics用の[!DNL Analytics] データ収集サーバーに[!DNL Target]から[!DNL Modstats] トラッキング サーバーを呼び出して送信する必要があります。<!-- just "to Analytics?"-->

[Adobe Debuggerのホスト名の値](/help/integrations/assets/target-troubleshooting-hostname.png)

[Targetでのトラッキングサーバー値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 関連トピックス

* [TargetとAnalyticsの統合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Analysis Workspaceで[!DNL Target] レポートを設定する方法について説明します。
* [A/B テストの概要](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) – 検索、ソーシャル、およびCommerceの広告で使用できるA/B テスト アクティビティについて説明します。
* [概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) - [!DNL Analytics for Advertising]が導入されました。これにより、Analytics インスタンスでのクリックスルーとビュースルーサイトインタラクションを追跡できます。

>[!MORELIKETHIS]
>
>* [Advertising DSP広告に対するAdobe TargetでのA/B テストの設定](ab-tests-dsp.md)
