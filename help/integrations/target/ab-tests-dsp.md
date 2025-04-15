---
title: Adobe Systems Advertising の A/B テストの設定 Adobe Target での広告DSP
description: DSP広告で A/B テストを設定する方法については [!DNL Target] こちらをご覧ください。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Advertising DSP Ads 用のAdobe Targetでの A/B テストの設定

*Advertising DSPのみの広告主*

Adobe AdvertisingとAdobe Targetを使用すると、マーケターは、有料メディアやオンサイトメッセージ全体を通じて、パーソナライズされた接続されたエクスペリエンスを簡単に提供できます。 製品間でシグナルを共有することで、次のことができます。

* DSP キャンペーンからの顧客の広告エクスポージャーをオンサイトエクスペリエンスにリンクすることで、サイトのフォールスルー率を下げます。

* Adobe Audience Managerの公開データとクリックしてフィードするオーディエンスを使用して、オンサイトエクスペリエンスを広告メッセージでミラーリングすることで、A/B テスト [!DNL Target] 確立します。

* Adobe Analytics for [!DNL Target] のシンプルなビジュアライゼーションを使用して、ユニファイドメッセージングがオンサイト目標リフトに与える影響を測定します。

前提条件と、クリックスルーおよびビュースルートラッキングの設定、DSPと [!DNL Target] の間のシグナル共有の実装および A/B テストアクティビティの設定、テストデータを表示するためのAnalysis Workspaceの設定に関す [!DNL Analytics] 手順については、次の節を参照してください。

その他の質問がある場合は、adcloud_support@adobe.comまでお問い合わせください。

## 前提条件

このユースケースには、次の製品および統合が必要です。

* [!DNL Target]

* [[!DNL Analytics] Advertisingの場合 ](/help/integrations/analytics/overview.md)integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 統合

* Audience Manager（ビュースルーテストでのみ必要）

## 手順 1：クリックスルーフレームワークの設定 {#click-through-framework}

![ クリックスルーフレームワーク ](/help/integrations/assets/target-ct-framework.png)

DSP マクロをクリックスルー URL （広告をクリックしてランディングページに到達したときに表示される URL）に追加すると、DSPはクリックスルー URL に `${TM_PLACEMENT_ID}` を含めることでプレースメントキーを自動的にキャプチャします。 このマクロは、数字の配置 ID ではなく、英数字の配置キーをキャプチャします。

![ ランディングページ URL に追加されたクリックスルー URL](/help/integrations/assets/target-ct-url.jpg)

### （DSPのみ）クリックスルー URL へのDSP マクロの追加

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

[!DNL Flashtalking] またはGoogle Campaign Manager 360 内で、各広告のクリックスルー URL を手動で更新して、AMO ID 変数のキャプチャに必要なマクロを含めます。 AMO ID 変数は、クリックデータをAdobe Analyticsに送信したり、A/B テストのプレースメントキーを共有したりするために使用されます。 手順については、次のページを参照してください。

* [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md)。 **注意：** 組織が [!DNL Flashtalking] と直接関係があり、データパスマクロを使用して `s_kwcid` および `ef_id` のトラッキングパラメーターを追跡する場合、[!DNL Flashtalking] サポートドキュメント （[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) に記載されている必要はありません。

* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad タグ](/help/integrations/analytics/macros-google-campaign-manager.md)

Adobe Systems アカウント チームと Advertising ソリューション グループ (aac-advertising-solutions-group@adobe.com) に連絡して、必要な 配置 キーを取得してセットアップを完了し、各クリックスルー URLに 配置 キーが設定されていることを確認してください。

## ステップ 2: Audience Managerを使用して表示スルーフレームワーク設定 {#view-through-framework}

![表示スルーフレームワーク](/help/integrations/assets/targetr-vt-framework.png)

広告タグと配置設定にAudience Managerインプレッションイベントピクセルを追加することで、表示スルーテストの機会を増やすためのテストセグメントを作成できます。

1. 広告 タグおよびDSP配置設定にAudience Managerインプレッションイベントピクセルを実装します。

   手順については、「[Advertising DSP キャンペーンからメディア露出データを収集 ](/help/integrations/audience-manager/media-data-integration/collect.md)」を参照してください。

   数値のプレースメント ID の `${TM_PLACEMENT_ID_NUM}` を含め、インプレッションイベントピクセルで渡すすべてのデータを取得するために、[DSP マクロ ](/help/dsp/campaign-management/macros.md) を必ず追加してください。

   >[!NOTE]
   >
   >クリックトラッキング URL には、数値のプレースメント ID の `${TM_PLACEMENT_ID_NUM}` の代わりに、英数字のプレースメントキーの `${TM_PLACEMENT_ID}` マクロが含まれます。

1. DSP インプレッションデータからAudience Manager セグメントを設定します。

   1. セグメントデータが使用可能であることを確認します。

      1. [ キーと値のペア ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) について [ シグナルを検索 ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) します。このペアは、セグメントユーザーをグループ化するレベルを決定します。

         Audience Managerのインプレッションイベントピクセルに追加したマクロに対応する値を持つ [ サポートされているキー ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) を使用します。

         例えば、特定のプレースメントのユーザーをグループ化するには、`d_placement` キーを使用します。 値には、DSP マクロ `${TM_PLACEMENT_ID_NUM}` によってキャプチャされた実際の数値プレースメント ID （2501853 など）を使用します。<!-- Explain where to find the placement ID, other than in a custom report. -->

         検索結果に、キーと値のペアのユーザー数が表示され、ピクセルが正しく配置され、データがフローしていることを示す場合は、次のステップに進みます。

   1. Audience Managerでセグメントを作成する場合は、[ ルールベースの特性を作成 ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) します。

      * テストアクティビティ内で簡単に識別できるように特性名前します。 任意のフォルダーに特性を保存します。

      * **[!UICONTROL Data Source]**&#x200B;として [`Ad Cloud`] を選択します。

      * 特性式については、 `d_event` を **[!UICONTROL Key]** として、 `imp` を **[!UICONTROL Value]**&#x200B;として使用します。

   1. [Audience Managerで新しい特性のテストセグメント](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) 設定、 `Ad Cloud` を **[!UICONTROL Data Source]**&#x200B;として選択します。

      Audience Manager、セグメントを、標準のランディングページエクスペリエンスを受け取るコントロール母集団と、パーソナライズされたオンサイトエクスペリエンスを受信するテストグループに自動的に分割します。

## 手順 3:[!DNL Target] でのDSPの A/B テストアクティビティの設定

次の手順では、DSPユースケースに関する情報を強調しています。

1. [Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)にログインします。

1. [A/B テスト](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)作成:

   1. [ **[!UICONTROL Enter Activity URL]** ] フィールドに、テストのランディングページURLを入力します。

      >[!NOTE]
      >
      >複数の URL を使用して表示スルー サイトへのエントリテストことができます。 詳しい情報については、「[複数ページアクティビティ](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)」を参照してください。 Analyticsで [サイトエントリレポート](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) を作成すると、URLページによってトップエントリを簡単に特定できます。

   1. [ **[!UICONTROL Goal]** ] フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >[!DNL Analytics] が [!DNL Target] 内のデータソースとして有効になっていること、および正しいレポートスイートが選択されていることを確認してください。

   1. `High`または`999`する&#x200B;**[!UICONTROL Priority]**&#x200B;設定、テスト内のユーザーがセグメント誤ったオンサイトエクスペリエンスを受け取った場合の競合を防ぎます。

   1. **[!UICONTROL Reporting Settings]**&#x200B;内で、DSPアカウントに接続されている&#x200B;**[!UICONTROL Company Name]**&#x200B;と&#x200B;**[!UICONTROL Report Suite]**&#x200B;を選択します。

      その他のレポートヒントについては、「[レポート作成のベストプラクティスとトラブルシューティング](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)」を参照してください。

   1. [ **[!UICONTROL Date Range]** ] フィールドに、テストの適切な開始と終了日を入力します。

   1. オーディエンスをアクティビティに追加します。

      1. 以前に セグメントAudience Manager で作成した [を選択し、表示スルーオーディエンス](#view-through-framework)テストします。

      1. **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**&#x200B;を選択し、**[!UICONTROL Value]**&#x200B;フィールドにDSP配置キーを入力して、クリックスルーオーディエンスのTargetクエリー文字列パラメーターを使用します。

   1. **[!UICONTROL Traffic Allocation Method]** の場合は、「**[!UICONTROL Manual (Default)]**」を選択し、オーディエンスを 50/50 に分割します。

   1. アクティビティを保存します。

1. [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) を使用して、A/B テストのランディングページテンプレートのデザインを変更します。

   * エクスペリエンス A：編集しないでください。パーソナライゼーションなしのデフォルト/コントロールランディングページエクスペリエンスです。

   * エクスペリエンス B: [!DNL Target] ユーザーインターフェイスを使用して、テストに含まれるアセット（見出し、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズします。

   >[!NOTE]
   >
   >クリエイティブなテストの使用例については、Adobe アカウントチームにお問い合わせください。

## 手順 4:[!DNL Analytics] で [!DNL Analytics for Target] Analysis Workspaceを設定する

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] （A4T）は、広告主がコンバージョン指標とオーディエンスセグメントに基づいて [!DNL Target] アクティビティを作成し、レポートソースとして [!DNL Analytics] を使用して結果を測定でき [!DNL Analytics] クロスソリューション統合環境です。 そのアクティビティのレポートとセグメント化はすべて、データ収集 [!DNL Analytics] 基づいています。

実装手順へのリンクなど、[!DNL Analytics for Target] について詳しくは、「Adobe Target （A4T）のレポートソースとしての [Adobe Analytics](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)」を参照してください。

### [!DNL Analytics for Target] パネルの設定

Analysis Workspaceで、[!DNL Target] アクティビティとエクスペリエンスを分析する [!DNL Analytics for Target panel] を設定します。 レポートに関する次の重要なポインタと情報に注意してください。

#### 指標

* テストが実行されたAdobe Advertisingのキャンペーン、パッケージまたはプレースメントに固有のパネルをワークスペース内に作成します。 概要ビジュアライゼーションを使用すると、[!DNL Target] のテストパフォーマンスと同じレポートにAdobe Advertising指標を表示できます。

* パフォーマンスを測定するために、オンサイト指標（訪問数やコンバージョン数など）の使用に優先順位を付けます。

* Adobe Advertisingの集計メディア指標（インプレッション数、クリック数、コストなど）を [!DNL Target] の指標と一致させることはできないことを理解します。

#### 寸法

[!DNL Analytics for Target] に関連するディメンションは次のとおりです。

* **[!UICONTROL Target Activities]**: A/B テストの名前

* **[!UICONTROL Target Experiences]**：アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **[!UICONTROL Target Activity]**/**[!UICONTROL Experience]**：同じ行にあるアクティビティ名とエクスペリエンス名

### Analytics for [!DNL Target] Data のトラブルシューティング

Analysis Workspace内でアクティビティとエクスペリエンスのデータが最小限である、またはデータが入力されていないことに気付いた場合は、次の操作を行います。

* [!DNL Target] と [!DNL Analytics] の両方で同じ [!UICONTROL Supplemental Data ID] （SDID）が使用されていることを確認します。 SDID 値を検証するには、キャンペーンがユーザーを誘導するランディングページで ](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)0}Adobe Experience Cloud Debugger} を使用します。[

[Adobe Debuggerの追加データ ID （SDID）値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a） [!UICONTROL Solutions]/[!UICONTROL Target] の下のAdobe Debuggerに表示される [!UICONTROL Hostname] が一致すること、b） アクティビティの [!DNL Target] に表示される [!UICONTROL Tracking Server] （[!UICONTROL Goals & Settings]/[!UICONTROL Reporting Settings] の下）が一致することを確認します。

  [!DNL Analytics For Target] では、[!DNL Target] から Analytics の [!DNL Modstats] データ収集サーバーへの呼び出しで [!DNL Analytics] トラッキングサーバーを送信する必要があります。<!-- just "to Analytics?"-->

[Adobe Debuggerのホスト名の値](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target のトラッキングサーバーの値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 参考情報

* [Target とAnalysis Workspaceの統合 ](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Analytics で [!DNL Target] レポートを設定する方法について説明します。
* [A/B テストの概要 ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - DSP広告で使用できる A/B テストアクティビティについて説明します。
* [ エクスペリエンスとオファー ](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - DSPのテストユーザーの公開先となるオンサイトコンテンツを決定するための [!DNL Target] のツールについて説明します。
* [ シグナル、特性、セグメント ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - DSPのビュースルーテストに役立つAudience Manager ツールの一部を定義します。
* [Analytics for Advertisingの概要 ](/help/integrations/analytics/overview.md) - Analytics for Advertisingについて説明します。この機能を使用すると、Analytics インスタンスでのクリックスルーおよびビュースルーサイトインタラクションをトラッキングできます。

>[!MORELIKETHIS]
>
>* [Adobe TargetでAdvertising検索、ソーシャル、Commerce広告用に A/B テストを設定する ](ab-tests-search.md)
