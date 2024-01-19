---
title: Adobe TargetのAdobe Advertising検索、ソーシャル、コマース広告に対する A/B テストの設定
description: で A/B テストを設定する方法を説明します。 [!DNL Target] の [!DNL Google Ads] および [!DNL Microsoft® Advertising] 広告が検索、ソーシャル、コマースに表示されます。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Adobe Targetで広告検索、ソーシャル、コマース広告用に A/B テストを設定する

*広告検索、ソーシャル、コマースのみを使用する広告主*

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] アカウントのみ*

Adobe AdvertisingとAdobe Targetを使用すると、デジタル広告トラフィック用のランディングページエクスペリエンス A/B テストを簡単に設定できます [!DNL Google Ads] および [!DNL Microsoft® Advertising] 移動先：

* コンバージョン率 (CVR) と獲得効率の測定（CPA、CPL、CAC など）を改善します。

* 広告に関連する、よりパーソナライズされたランディングページエクスペリエンスを提供します（例えば、画像/ビデオのクリエイティブ、コピー、キーワードまたは他の広告シグナルとランディングページの照合）。

また、ネイティブの [[!DNL Analytics] （広告用）](/help/integrations/analytics/overview.md) および [[!DNL Analytics] 対象： [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) Adobe Analyticsに統合された統合レポートディメンションで、 [!DNL Analytics] 指標と成功イベントの両方を追加します。

前提条件と A/B テストを設定する手順については、次の節を参照してください。 [!DNL Target] 検索、ソーシャル、コマースの広告からのクリックスルートラフィック、およびでのテストの測定方法と視覚化方法に関するヒント [!DNL Analytics].

## 前提条件

### 必要な製品

* 検索、ソーシャル、コマース
* [!DNL Target]

### 推奨される製品と統合

* [!DNL Analytics]

* [[!DNL Analytics] （広告用）](/help/integrations/analytics/overview.md) 統合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 対象： [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 統合

## 手順 1：で A/B テストアクティビティを作成する [!DNL Target] 検索、ソーシャル、コマース

以下の手順では、検索、ソーシャル、コマースの使用例に関する情報をハイライトします。

1. [Adobe Targetにログイン](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [A/B テストの作成](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Adobe Analytics の **[!UICONTROL Enter Activity URL]** 「 」フィールドに、テストのランディングページ URL を入力します。

   1. Adobe Analytics の **[!UICONTROL Goal]** 「 」フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >次を確認します。 [!DNL Analytics] は、内のデータソースとして有効になります。 [!DNL Target]」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」) が正しいレポートスイートが選択されている。

   1. を設定します。 **[!UICONTROL Priority]** から `High` または `999` を使用して、テストセグメント内のユーザーが誤ったオンサイトエクスペリエンスを受け取った場合の競合を防ぎます。


   1. Within **[!UICONTROL Reporting Settings]**&#x200B;を選択し、 **[!UICONTROL Company Name]** および **[!UICONTROL Report Suite]** を検索、ソーシャル、コマースの各アカウントに接続しました。

      その他のレポートのヒントについては、[レポートのベストプラクティスとトラブルシューティング](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Adobe Analytics の **[!UICONTROL Date Range]** 「 」フィールドで、テストの適切な開始日と終了日を入力します。

   1. 選択 **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. Adobe Analytics の **[!UICONTROL Value]** フィールドに、 [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID]または [!UICONTROL Network Ad ID] 検索、ソーシャル、コマースの関連する広告ネットワークエンティティ用。 これにより、 [!DNL Target] エンティティのクリックスルーオーディエンス用のクエリー文字列パラメーター。

      ID は、 [関連する ID 列のエンティティビューへの追加](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] 列の [!UICONTROL Accounts] 表示](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] 列の [!UICONTROL Accounts] 表示")

      サポートが必要な場合は、Adobeのアカウントチームにご相談ください。

   1. の **[!UICONTROL Traffic Allocation Method]**&#x200B;を選択します。 **[!UICONTROL Manual (Default)]** オーディエンスを分割50/50た。

   1. アクティビティを保存します。

1. 用途 [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) A/B テストのランディングページテンプレートをデザイン上で変更する場合。

   * エクスペリエンス A：パーソナライゼーションがないデフォルト/コントロールのランディングページエクスペリエンスなので、編集しないでください。

   * エクスペリエンス B: [!DNL Target] テストに含まれるアセット（ヘッドライン、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズするユーザーインターフェイス。

   >[!NOTE]
   >
   >クリエイティブテストの使用例などについては、担当のAdobeアカウントチームにお問い合わせください。

## 手順 2: [!DNL Analytics for Target] Analysis Workspace [!DNL Analytics]

[!DNL Analytics for Target] (A4T) は、広告主が [!DNL Target] に基づくアクティビティ [!DNL Analytics] コンバージョン指標およびオーディエンスセグメントを使用して結果を測定し、 [!DNL Analytics] を使用します。 そのアクティビティのすべてのレポートとセグメント化は、 [!DNL Analytics] データ収集を行います。

詳しくは、 [!DNL Analytics for Target]（導入手順へのリンクを含む）[Adobe TargetのレポートソースとしてのAdobe Analytics(A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### を設定します。 [!DNL Analytics for Target] パネル

Analysis Workspaceで、 [!DNL Analytics for Target panel] を分析するには、 [!DNL Target] アクティビティとエクスペリエンス。 レポートに関する次の重要なポインターおよび情報に注意してください。

#### 指標

* ワークスペース内で、Adobe Advertisingアカウント、キャンペーンまたは広告グループに固有のパネルを作成します<!-- only applicable entities? --> テストを実行した対象の 概要ビジュアライゼーションを使用して、Adobe Advertising指標を [!DNL Target] テストのパフォーマンス。

* オンサイト指標（訪問回数、コンバージョン数など）を使用してパフォーマンスを測定することを優先します。

* Adobe Advertising（インプレッション数、クリック数、コストなど）の集計メディア指標を [!DNL Target] 指標。

#### Dimension

次のディメンションは、次に関係します。 [!DNL Analytics for Target]:

* **Target アクティビティ**:A/B テストの名前

* **Target エクスペリエンス**：アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **Target アクティビティ** > **エクスペリエンス**：同じ行のアクティビティ名とエクスペリエンス名

### Analytics でのトラブルシューティング [!DNL Target] データ

Analysis Workspace内で、アクティビティとエクスペリエンスのデータが最小限である、または入力されていないことに気付いた場合は、次の操作を行います。

* 同じ [!UICONTROL Supplemental Data ID] (SDID) は、 [!DNL Target] および [!DNL Analytics]. SDID の値は、 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) をクリックします。

[Adobe Debuggerの追加データ ID(SDID) 値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、「 [!UICONTROL Hostname] 下のAdobe Debuggerに示される [!UICONTROL Solutions] > [!UICONTROL Target] b) に一致 [!UICONTROL Tracking Server] 次に示す [!DNL Target] アクティビティ ( [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]) をクリックします。

  [!DNL Analytics For Target] にはが必要です [!DNL Analytics] からの呼び出しで送信されるトラッキングサーバー [!DNL Target] から [!DNL Modstats] Analytics のデータ収集サーバー。<!-- just "to Analytics?"-->

[ホスト名の値 (Adobe Debugger)](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target のトラッキングサーバー値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 参考情報

* [Target と Analytics の統合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)  — の設定方法を説明します。 [!DNL Target] Analysis Workspaceでのレポート
* [A/B テストの概要](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 検索、ソーシャル、コマースの広告で使用できる A/B テストアクティビティを表します。
* [広告用 Analytics の概要](/help/integrations/analytics/overview.md) - Analytics for Advertising を導入します。これにより、Analytics インスタンス内でのクリックスルーおよびビュースルーサイトでのインタラクションを追跡できます。

>[!MORELIKETHIS]
>
>* [Adobe TargetでDSP Ads 用に A/B テストを設定する](ab-tests-dsp.md)
