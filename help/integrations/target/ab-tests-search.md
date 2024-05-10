---
title: Adobe TargetでのAdobe Advertising検索、ソーシャル、Commerce広告に対する A/B テストの設定
description: で A/B テストの設定方法を学ぶ [!DNL Target] の場合 [!DNL Google Ads] および [!DNL Microsoft Advertising] 検索、ソーシャル、Commerceの広告。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Advertising Search、Social、およびCommerce広告用にAdobe Targetで A/B テストを設定します

*広告検索、ソーシャル、Commerceのみを使用する広告主*

*[!DNL Google Ads]および [!DNL Microsoft Advertising] アカウントのみ*

Adobe AdvertisingとAdobe Targetを使用すると、デジタル広告トラフィックのランディングページエクスペリエンス A/B テストを簡単に設定できます [!DNL Google Ads] および [!DNL Microsoft Advertising] コピー先：

* コンバージョン率（CVR）および取得効率測定（CPA、CPL、CAC など）を改善する。

* 広告に関連する、よりパーソナライズされたランディングページのエクスペリエンスを提供します（例えば、画像/ビデオクリエイティブ、コピー、キーワードまたはランディングページに対するその他の広告信号との一致）。

ネイティブを組み合わせることもできます [[!DNL Analytics] 広告用](/help/integrations/analytics/overview.md) および [[!DNL Analytics] （用） [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) Adobe Analyticsに統合され、テストデータを測定および視覚化する統合レポートディメンション [!DNL Analytics] 指標と成功イベント。

前提条件、での A/B テストの設定手順については、次の節を参照してください [!DNL Target] 検索、ソーシャル、Commerceの広告からのクリックスルートラフィックのほか、でテストを測定および視覚化する方法に関するヒントについて説明します [!DNL Analytics].

## 前提条件

### 必要な製品

* 検索、ソーシャル、Commerce
* [!DNL Target]

### 推奨される製品と統合

* [!DNL Analytics]

* [[!DNL Analytics] 広告用](/help/integrations/analytics/overview.md) 統合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] （用） [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 統合

## 手順 1：での A/B テストアクティビティの作成 [!DNL Target] 検索、ソーシャル、Commerce

以下の手順では、検索、ソーシャル、Commerceのユースケースに関する情報を重点的に説明しています。

1. [Adobe Targetにログインします](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [A/B テストの作成](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. が含まれる **[!UICONTROL Enter Activity URL]** フィールドに、テストのランディングページ URL を入力します。

   1. が含まれる **[!UICONTROL Goal]** フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >次のことを確認します [!DNL Analytics] 内のデータソースとして有効になる [!DNL Target]正しいレポートスイートが選択されていることを確認します。

   1. を **[!UICONTROL Priority]** 対象： `High` または `999` テストセグメント内のユーザーが誤ったオンサイトエクスペリエンスを受け取った場合の競合を防ぐ。


   1. 内 **[!UICONTROL Reporting Settings]**&#x200B;を選択し、 **[!UICONTROL Company Name]** および **[!UICONTROL Report Suite]** 検索、ソーシャル、Commerce アカウントに接続しました。

      その他のレポートのヒントについては、「」を参照してください[レポートのベストプラクティスとトラブルシューティング](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).」と入力します。

   1. が含まれる **[!UICONTROL Date Range]** フィールドに、テストの適切な開始日と終了日を入力します。

   1. を選択 **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. が含まれる **[!UICONTROL Value]** フィールドに、 [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID]、または [!UICONTROL Network Ad ID] （検索、ソーシャル、Commerce内の関連する広告ネットワークエンティティ）。 を使用すると、 [!DNL Target] エンティティのクリックスルーオーディエンスの文字列パラメーターをクエリします。

      ID は次の方法で確認できます [エンティティビューへの関連する ID 列の追加](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] 列： [!UICONTROL Accounts] 表示](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] 列： [!UICONTROL Accounts] 表示")

      サポートが必要な場合は、Adobeアカウントチームにお問い合わせください。

   1. の場合 **[!UICONTROL Traffic Allocation Method]**&#x200B;を選択 **[!UICONTROL Manual (Default)]** オーディエンスを 50/50 に分割します。

   1. アクティビティを保存します。

1. 使用方法 [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) a/B テストランディングページテンプレートのデザインを変更します。

   * エクスペリエンス A：編集しないでください。パーソナライゼーションなしのデフォルト/コントロールランディングページエクスペリエンスです。

   * エクスペリエンス B：を使用する [!DNL Target] テストに含まれるアセット（見出し、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズするためのユーザーインターフェイスです。

   >[!NOTE]
   >
   >クリエイティブ テストの使用例については、Adobeアカウントチームにお問い合わせください。

## 手順 2：の設定 [!DNL Analytics for Target] Analysis Workspace: [!DNL Analytics]

[!DNL Analytics for Target] （A4T）は、広告主が以下を作成できるクロスソリューション統合環境です [!DNL Target] 基づいたアクティビティ [!DNL Analytics] 次に、コンバージョン指標とオーディエンスセグメントを使用して、結果を測定します [!DNL Analytics] をレポートソースとして使用します。 そのアクティビティのレポートとセグメント化はすべて、に基づいています [!DNL Analytics] データ収集。

詳しくは、 [!DNL Analytics for Target]（実装手順へのリンクを含む）。「」を参照してください[Adobe TargetのレポートソースとしてのAdobe Analytics（A4T）](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)」と入力します。

### の設定 [!DNL Analytics for Target] パネル

Analysis Workspaceで、以下を設定します [!DNL Analytics for Target panel] を分析するには [!DNL Target] アクティビティとエクスペリエンス。 レポートに関する次の重要なポインタと情報に注意してください。

#### 指標

* Adobe Advertisingアカウント、キャンペーン、広告グループに固有のパネルをワークスペース内に作成します<!-- only applicable entities? --> に対してテストが実行されました。 Adobe Advertising概要ビジュアライゼーションを使用すると、 [!DNL Target] パフォーマンスのテスト。

* パフォーマンスを測定するために、オンサイト指標（訪問数やコンバージョン数など）の使用に優先順位を付けます。

* Adobe Advertising（インプレッション数、クリック数、コストなど）の集計メディア指標を一致させることができないことを理解します [!DNL Target] 指標。

#### Dimension

次のディメンションは次に関連します [!DNL Analytics for Target]:

* **Target アクティビティ**:A/B テストの名前

* **Target エクスペリエンス**：アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **Target アクティビティ** > **経験**：同じ行にあるアクティビティ名とエクスペリエンス名

### Analytics for のトラブルシューティング [!DNL Target] データ

Analysis Workspace内でアクティビティとエクスペリエンスのデータが最小限である、またはデータが入力されていないことに気付いた場合は、次の操作を行います。

* 同じであることを確認します [!UICONTROL Supplemental Data ID] （SDID）は、次の両方に使用されます [!DNL Target] および [!DNL Analytics]. SDID 値を検証するには、 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) キャンペーンがユーザーを誘導するランディングページ上。

[Adobe Debuggerの追加データ ID （SDID）値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a） [!UICONTROL Hostname] の下のAdobe Debuggerに表示される [!UICONTROL Solutions] > [!UICONTROL Target] が b）に一致します [!UICONTROL Tracking Server] に表示 [!DNL Target] アクティビティ（の下 [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]）に設定します。

  [!DNL Analytics For Target] が必要 [!DNL Analytics] からの呼び出しで送信されるトラッキングサーバー [!DNL Target] に [!DNL Modstats] analytics 用データ収集サーバー。<!-- just "to Analytics?"-->

[Adobe Debuggerのホスト名の値](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target のトラッキングサーバーの値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 参考情報

* [Target と Analytics の統合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)  – 設定方法を説明します [!DNL Target] Analysis Workspaceでのレポート。
* [A/B テストの概要](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - A/B テストアクティビティを表します。検索、ソーシャル、Commerceの広告で使用できます。
* [Analytics for Advertising の概要](/help/integrations/analytics/overview.md) - Analytics for Advertising が導入されました。これにより、Analytics インスタンスでクリックスルーおよびビュースルーサイトインタラクションを追跡できます。

>[!MORELIKETHIS]
>
>* [Advertising DSP Ads 用のAdobe Targetでの A/B テストの設定](ab-tests-dsp.md)
