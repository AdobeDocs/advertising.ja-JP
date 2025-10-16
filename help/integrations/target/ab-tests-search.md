---
title: Adobe TargetでのAdobe Advertising検索、ソーシャル、Commerce広告用の A/B テストの設定
description: 検索、ソーシャル、Commerceで広告と広告の A [!DNL Target] B テストを設定  [!DNL Google Ads]  る方法  [!DNL Microsoft Advertising]  ついて説明します。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Adobe TargetでのAdvertising検索、ソーシャル、Commerce広告用の A/B テストの設定

*Advertising検索、ソーシャル、Commerceのみを使用する広告主*

*[!DNL Google Ads]および [!DNL Microsoft Advertising] アカウントのみ*

Adobe AdvertisingとAdobe Targetを使用すると、次の操作を行うことで、デジタル広告トラフィックのランディングページエクスペリエンス A/B テストを簡単 [!DNL Google Ads] 設定で [!DNL Microsoft Advertising] ます。

* コンバージョン率（CVR）および取得効率測定（CPA、CPL、CAC など）を改善する。

* 広告に関連する、よりパーソナライズされたランディングページのエクスペリエンスを提供します（例えば、画像/ビデオクリエイティブ、コピー、キーワードまたはランディングページに対するその他の広告信号との一致）。

また、Adobe Analyticsに統合されているネイティブの [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) 統合レポートディメンションと [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja) 統合レポートディメンションを組み合わせて、テストデータを測定し、[!DNL Analytics] の指標と成功イベントで視覚化することもできます。

前提条件、検索、ソーシャル、Commerceの広告からのクリックスルートラフィックに [!DNL Target] して A/B テストを設定する手順、[!DNL Analytics] でテストを測定および視覚化する方法に関するヒントについては、次の節を参照してください。

## 前提条件

### 必要な製品

* 検索、ソーシャル、Commerce
* [!DNL Target]

### 推奨される製品と統合

* [!DNL Analytics]

* [[!DNL Analytics] Advertisingの場合 &#x200B;](/help/integrations/analytics/overview.md)integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja) 統合

## 手順 1:[!DNL Target] で検索、ソーシャル、Commerce用の A/B テストアクティビティを作成する

以下の手順では、検索、ソーシャル、Commerceのユースケースに関する情報を重点的に説明しています。

1. [Adobe Targetにログインします &#x200B;](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=ja)。

1. [A/B テストの作成 &#x200B;](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=ja):

   1. 「**[!UICONTROL Enter Activity URL]**」フィールドに、テストのランディングページ URL を入力します。

   1. 「**[!UICONTROL Goal]**」フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >[!DNL Target] 内で [!DNL Analytics] がデータソースとして有効になっており、正しいレポートスイートが選択されていることを確認します。

   1. **[!UICONTROL Priority]** を `High` または `999` に設定して、テストセグメントのユーザーが誤ったオンサイトエクスペリエンスを受け取った場合の競合を防ぎます。


   1. **[!UICONTROL Reporting Settings]** 内で **[!UICONTROL Company Name]** を選択し、検索、ソーシャル、Commerce アカウントに接続してくださ **[!UICONTROL Report Suite]**。

      その他のレポートに関するヒントについては、[&#x200B; レポートのベストプラクティスとトラブルシューティング &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=ja) を参照してください。

   1. 「**[!UICONTROL Date Range]**」フィールドに、テストの適切な開始日と終了日を入力します。

   1. **[!UICONTROL Site Pages]**/**[!UICONTROL Landing Page]**/**[!UICONTROL Query]** を選択します。 「**[!UICONTROL Value]**」フィールドに、検索、ソーシャル、Commerceの関連する広告ネットワークエンティティの [!UICONTROL Network Account ID]、[!UICONTROL Network Campaign ID]、[!UICONTROL Network Adgroup ID] または [!UICONTROL Network Ad ID] を入力します。 これにより、エンティティのクリックスルーオーディエンスに [!DNL Target] のクエリ文字列パラメーターを使用できます。

      ID を見つけるには、[&#x200B; 関連する ID 列をエンティティビューに追加 &#x200B;](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) します。

      [!UICONTROL Accounts]![[!UICONTROL Network Account ID] 表示の列 &#x200B;](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID]&#x200B;[!UICONTROL Accounts] 表示の列 ")

      サポートが必要な場合は、Adobe アカウントチームにお問い合わせください。

   1. **[!UICONTROL Traffic Allocation Method]** の場合は、「**[!UICONTROL Manual (Default)]**」を選択し、オーディエンスを 50/50 に分割します。

   1. アクティビティを保存します。

1. [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=ja) を使用して、A/B テストのランディングページテンプレートのデザインを変更します。

   * エクスペリエンス A：編集しないでください。パーソナライゼーションなしのデフォルト/コントロールランディングページエクスペリエンスです。

   * エクスペリエンス B: [!DNL Target] ユーザーインターフェイスを使用して、テストに含まれるアセット（見出し、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズします。

   >[!NOTE]
   >
   >クリエイティブなテストの使用例については、Adobe アカウントチームにお問い合わせください。

## 手順 2:[!DNL Analytics] で [!DNL Analytics for Target] Analysis Workspaceを設定する

[!DNL Analytics for Target] （A4T）は、広告主がコンバージョン指標とオーディエンスセグメントに基づいて [!DNL Target] アクティビティを作成し、レポートソースとして [!DNL Analytics] を使用して結果を測定でき [!DNL Analytics] クロスソリューション統合環境です。 そのアクティビティのレポートとセグメント化はすべて、データ収集 [!DNL Analytics] 基づいています。

実装手順へのリンクなど、[!DNL Analytics for Target] について詳しくは、「Adobe Target （A4T）のレポートソースとしての [Adobe Analytics](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)」を参照してください。

### [!DNL Analytics for Target] パネルの設定

Analysis Workspaceで、[!DNL Target] アクティビティとエクスペリエンスを分析する [!DNL Analytics for Target panel] を設定します。 レポートに関する次の重要なポインタと情報に注意してください。

#### 指標

* テストが実行されたAdobe Advertising アカウント、キャンペーンまたは広告グループに固有のパネルを <!-- only applicable entities? --> ワークスペース内に作成します。 概要ビジュアライゼーションを使用すると、[!DNL Target] のテストパフォーマンスと同じレポートにAdobe Advertising指標を表示できます。

* パフォーマンスを測定するために、オンサイト指標（訪問数やコンバージョン数など）の使用に優先順位を付けます。

* Adobe Advertisingの集計メディア指標（インプレッション数、クリック数、コストなど）を [!DNL Target] の指標と一致させることはできないことを理解します。

#### 寸法

[!DNL Analytics for Target] に関連するディメンションは次のとおりです。

* **Target アクティビティ**:A/B テストの名前

* **Target エクスペリエンス**：アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **ターゲットアクティビティ**/**エクスペリエンス**：同じ行にあるアクティビティ名とエクスペリエンス名

### Analytics for [!DNL Target] Data のトラブルシューティング

Analysis Workspace内でアクティビティとエクスペリエンスのデータが最小限である、またはデータが入力されていないことに気付いた場合は、次の操作を行います。

* [!DNL Target] と [!DNL Analytics] の両方で同じ [!UICONTROL Supplemental Data ID] （SDID）が使用されていることを確認します。 SDID 値を検証するには、キャンペーンがユーザーを誘導するランディングページで [&#128279;](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=ja)0&rbrace;Adobe Experience Cloud Debugger&rbrace; を使用します。

[Adobe Debuggerの追加データ ID （SDID）値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a） [!UICONTROL Solutions]/[!UICONTROL Target] の下のAdobe Debuggerに表示される [!UICONTROL Hostname] が一致すること、b） アクティビティの [!DNL Target] に表示される [!UICONTROL Tracking Server] （[!UICONTROL Goals & Settings]/[!UICONTROL Reporting Settings] の下）が一致することを確認します。

  [!DNL Analytics For Target] では、[!DNL Target] から Analytics の [!DNL Modstats] データ収集サーバーへの呼び出しで [!DNL Analytics] トラッキングサーバーを送信する必要があります。<!-- just "to Analytics?"-->

[Adobe Debuggerのホスト名の値](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target のトラッキングサーバーの値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 参考情報

* [Target とAnalysis Workspaceの統合 &#x200B;](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=ja) - Analytics で [!DNL Target] レポートを設定する方法について説明します。
* [A/B テストの概要 &#x200B;](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=ja) - A/B テストアクティビティについて説明します。検索、ソーシャルおよびCommerce広告で使用できます。
* [Analytics for Advertisingの概要 &#x200B;](/help/integrations/analytics/overview.md) - Analytics for Advertisingについて説明します。この機能を使用すると、Analytics インスタンスでのクリックスルーおよびビュースルーサイトインタラクションをトラッキングできます。

>[!MORELIKETHIS]
>
>* [Advertising DSP Ads 用のAdobe Targetでの A/B テストの設定 &#x200B;](ab-tests-dsp.md)
