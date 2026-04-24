---
title: Adobe TargetでAdobe Advertising Search、Social、Commerce広告のA/B テストを設定する
description: Search, Social, & Commerceで [!DNL Google Ads] 広告および [!DNL Microsoft Advertising] 広告の [!DNL Target] でA/B テストを設定する方法について説明します。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
TQID: https://experienceleague.adobe.com/eu1dRdsQlJX4IlHLTUDyJ69r0txFvFUdzUiXpSAlpU8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 958
ht-degree: 0%

---

# Adobe TargetでAdvertising Search、Social、Commerce広告のA/B テストを設定する

*Advertising Search, Social, &amp; Commerceのみの広告主*

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

Adobe AdvertisingとAdobe Targetを使用すると、デジタル広告トラフィック [!DNL Google Ads]と[!DNL Microsoft Advertising]に対するランディングページ エクスペリエンス A/B テストを簡単に設定して、以下を行うことができます。

* コンバージョン率（CVR）と獲得効率の指標（CPA、CPL、CACなど）を改善します。

* 広告に合わせて、よりパーソナライズされたランディングページ体験を提供します（例えば、画像/動画のクリエイティブ、コピー、キーワード、その他の広告シグナルをランディングページに一致させます）。

また、Adobe Analyticsに統合されたAdvertising](/help/integrations/analytics/overview.md)用のネイティブ [[!DNL Analytics] と [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)用の[[!DNL Analytics] 統合レポートディメンションを組み合わせて、[!DNL Analytics]個の指標と成功イベントを使用してテストデータを測定および視覚化することもできます。

Search, Social, &amp; Commerceの広告からのクリックスルーのトラフィックについて、[!DNL Target]でA/B テストを設定する手順と、[!DNL Analytics]でテストを測定して視覚化する方法に関するヒントについては、次の節を参照してください。

## 前提条件

### 必要な製品

* Search, Social, &amp; Commerce
* [!DNL Target]

### 推奨される製品と統合

* [!DNL Analytics]

* Advertising](/help/integrations/analytics/overview.md)統合<!-- necessary for testing view-throughs, which most advertisers want to do -->の[[!DNL Analytics] 

*  [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)統合用[[!DNL Analytics] 

## Step 1: Create an A/B test activity in [!DNL Target] for Search, Social, &amp; Commerce

The following instructions highlight information pertaining to the Search, Social, &amp; Commerce use case.

1. [Adobe Targetにログイン ](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. [A/B テストを作成](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. 「**[!UICONTROL Enter Activity URL]**」フィールドに、テストのランディングページ URLを入力します。

   1. 「**[!UICONTROL Goal]**」フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >[!DNL Analytics]が[!DNL Target]内のデータソースとして有効になっており、正しいレポートスイートが選択されていることを確認してください。

   1. Set the **[!UICONTROL Priority]** to `High` or `999` to prevent conflicts when users in the test segment receive an incorrect on-site experience.


   1. Within **[!UICONTROL Reporting Settings]**, select the **[!UICONTROL Company Name]** and **[!UICONTROL Report Suite]** connected to your Search, Social, &amp; Commerce account.

      For additional reporting tips, see &quot;[Reporting best practices and troubleshooting](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. In the **[!UICONTROL Date Range]** field, enter the appropriate start and end dates for the test.

   1. Select **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. In the **[!UICONTROL Value]** field, enter the [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], or [!UICONTROL Network Ad ID] for the relevant ad network entity in Search, Social, &amp; Commerce. This allows you to use the [!DNL Target] query string parameters for click-through audiences for the entity.

      You can find the ID by [adding the relevant ID column to the entity view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] column in the [!UICONTROL Accounts] view")

      Work with your Adobe Account Team if you need assistance.

   1. For the **[!UICONTROL Traffic Allocation Method]**, select **[!UICONTROL Manual (Default)]** and split the audience 50/50.

   1. Save the activity.

1. Use [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) to make design changes to the A/B test landing page template.

   * Experience A: Don&#39;t edit because it&#39;s the default/control landing page experience without personalization.

   * Experience B: Use the [!DNL Target] user interface to customize the landing page template based on the assets included in the test (such as headlines, copy, button placement, and creatives).

   >[!NOTE]
   >
   >For example creative test use cases, contact your Adobe Account Team.

## Step 2: Set up your [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) is a cross-solution integration that lets advertisers create [!DNL Target] activities based on [!DNL Analytics] conversion metrics and audience segments and then measure the results using [!DNL Analytics] as the reporting source. そのアクティビティのすべてのレポートとセグメント化は、[!DNL Analytics] データ収集に基づいています。

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

* [!DNL Target]と[!DNL Analytics]の両方に同じ[!UICONTROL Supplemental Data ID] （SDID）が使用されていることを確認します。 SDID値を確認するには、キャンペーンがユーザーを促進しているランディングページの[Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)を使用します。

  [Adobe Debuggerの補足データ ID （SDID）値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a）Adobe Debuggerに表示されている[!UICONTROL Hostname]が[!UICONTROL Solutions] > [!UICONTROL Target]に一致することを確認しますb）アクティビティの[!DNL Target]に表示されている[!UICONTROL Tracking Server]が（[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]に一致することを確認します。

  [!DNL Analytics For Target]では、Analytics用の[!DNL Modstats] データ収集サーバーに[!DNL Target]から[!DNL Analytics] トラッキング サーバーを呼び出して送信する必要があります。<!-- just "to Analytics?"-->

  [Adobe Debuggerのホスト名の値](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Targetでのトラッキングサーバー値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 関連トピックス

* [TargetとAnalyticsの統合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Analysis Workspaceで[!DNL Target] レポートを設定する方法について説明します。
* [A/B テストの概要](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) – 検索、ソーシャル、およびCommerceの広告で使用できるA/B テスト アクティビティについて説明します。
* [概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) - [!DNL Analytics for Advertising]が導入されました。これにより、Analytics インスタンスでのクリックスルーとビュースルーサイトインタラクションを追跡できます。

>[!MORELIKETHIS]
>
>* [Advertising DSP広告に対するAdobe TargetでのA/B テストの設定](ab-tests-dsp.md)
