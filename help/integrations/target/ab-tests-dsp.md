---
title: Adobe TargetでのAdobe Advertising DSP広告のA/B テストの設定
description: DSP広告のA/B テストを [!DNL Target] で設定する方法について説明します。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
TQID: https://experienceleague.adobe.com/xETpACcZbZqfFjS58mS-k-kXhm0BT79W0aHz2bdKDGs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1404
ht-degree: 0%

---

# Advertising DSP広告用Adobe TargetでのA/B テストの設定

*Advertising DSPのみの広告主*

Adobe AdvertisingとAdobe Targetにより、マーケターは、有料メディアやサイト上のメッセージをまたいで、パーソナライズされた連続性のあるエクスペリエンスをさらに容易に提供できるようになります。 製品間でシグナルを共有することで、次のことが可能になります。

* DSPキャンペーンの顧客の広告露出をオンサイト体験に結び付けることで、サイトのフォールスルー率を低減します。

* Adobe Audience Managerの広告露出データと[!DNL Target]人のクリックツーフィードのオーディエンスを使用して、オンサイトのエクスペリエンスを広告メッセージとミラーリングすることで、A/B テストを実施します。

* [!DNL Target]のAdobe Analyticsのシンプルなビジュアライゼーションを使用して、オンサイトの目標リフトに対する統合メッセージの影響を測定します。

クリックスルーおよびビュースルートラッキングの設定、DSPと[!DNL Target]間のシグナル共有の実装、A/B テストアクティビティの設定、テストデータを表示するための[!DNL Analytics] Analysis Workspaceの設定について、前提条件および手順については、次の節を参照してください。

ご不明な点がございましたら、Adobeのアカウントチームにお問い合わせください。

## 前提条件

このユースケースでは、次の製品と統合が必要です。

* [!DNL Target]

* Advertising[[!DNL Analytics] 統合](/help/integrations/analytics/overview.md)の<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics]  [!DNL Target]統合用](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)

* Audience Manager（ビュースルーテストにのみ必要）

## 手順1：クリックスルーフレームワークの設定 {#click-through-framework}

![&#x200B; クリックスルーフレームワーク &#x200B;](/help/integrations/assets/target-ct-framework.png)

DSP マクロをクリックスルーURL （ユーザーが広告をクリックしてランディングページに到達したときに表示されるURL）に追加すると、DSPは、クリックスルーURLに`${TM_PLACEMENT_ID}`を含めることで、プレースメントキーを自動的にキャプチャします。 このマクロは、数値プレースメント IDではなく、英数字プレースメント キーをキャプチャします。

![&#x200B; ランディングページ URL](/help/integrations/assets/target-ct-url.jpg)に追加されたクリックスルーURL

### （DSPのみ）クリックスルーURLにDSP マクロを追加する

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

[!DNL Flashtalking]またはGoogle Campaign Manager 360内で、各広告のクリックスルーURLを手動で更新し、AMO ID変数の取得に必要なマクロを含めます。 AMO ID変数は、クリックデータをAdobe Analyticsに送信し、A/B テスト用のプレースメントキーを共有するために使用されます。 手順については、次のページを参照してください。

* [追加 [!DNL Analytics for Advertising]  マクロを [!DNL Flashtalking] 広告タグ &#x200B;](/help/integrations/analytics/macros-flashtalking.md)に追加します。 **注：**&#x200B;組織が[!DNL Flashtalking]と直接パートナーシップを締結しており、データ渡しマクロを使用して`s_kwcid`および`ef_id`のトラッキングパラメーターを[!DNL Flashtalking] サポート ドキュメント（[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros)）で追跡する場合、この手順は必要ありません。

* [&#x200B; [!DNL Analytics for Advertising]  マクロを [!DNL Google Campaign Manager 360] 広告タグに追加](/help/integrations/analytics/macros-google-campaign-manager.md)

Adobe アカウントチームに連絡して、必要なプレースメントキーを取得し、設定を確定し、各クリックスルーURLにプレースメントキーが入力されていることを確認します。

## 手順2:Audience Managerを使用したビュースルーフレームワークの設定 {#view-through-framework}

![&#x200B; ビュースルーフレームワーク &#x200B;](/help/integrations/assets/targetr-vt-framework.png)

広告タグとプレースメント設定にAudience Manager インプレッションイベントピクセルを追加することで、ビュースルーテストの機会を増やすためのテストセグメントを作成できます。

1. 広告タグとDSPの配置の設定にAudience Manager インプレッションイベントピクセルを実装します。

   手順については、「[Advertising DSP キャンペーンからメディア露出データを収集](/help/integrations/audience-manager/media-data-integration/collect.md)」を参照してください。

   インプレッションイベントピクセルが渡すすべてのデータを取得するには、[DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)を追加します。これには、数値プレースメント IDの`${TM_PLACEMENT_ID_NUM}`も含まれます。

   >[!NOTE]
   >
   >クリックトラッキング URLには、数値プレースメント IDの`${TM_PLACEMENT_ID}`ではなく、英数字プレースメント キーの`${TM_PLACEMENT_ID_NUM}` マクロが含まれます。

1. DSP インプレッションデータからAudience Manager セグメントを設定します。

   1. セグメントデータが使用可能であることを確認します。

      1. [&#x200B; セグメントユーザーがどのレベルでグループ化されているかを決定する](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html?lang=ja) キー値ペア [のシグナル &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html)を検索します。

         Audience Manager インプレッション イベント ピクセルに追加したマクロに対応する値を持つ[&#x200B; サポートされているキー](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=ja)を使用します。

         例えば、特定のプレースメントのユーザーをグループ化するには、`d_placement` キーを使用します。 値には、DSP マクロ `${TM_PLACEMENT_ID_NUM}`によってキャプチャされた実際の数値プレースメント ID （2501853など）を使用します。<!-- Explain where to find the placement ID, other than in a custom report. -->

         検索結果にキーと値のペアのユーザーカウントが表示されている場合（ピクセルが正しく配置され、データが流れていることを示す）、次の手順に進みます。

   1. Audience Managerでセグメントを作成するための[&#x200B; ルールベースの特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)を作成します。

      * テストアクティビティ内で容易に識別できるように、特性に名前を付けます。 好みのフォルダーに特性を保存します。

      * `Ad Cloud`を&#x200B;**[!UICONTROL Data Source]**&#x200B;として選択します。

      * 特性の式には、`d_event`を&#x200B;**[!UICONTROL Key]**&#x200B;として、`imp`を&#x200B;**[!UICONTROL Value]**&#x200B;として使用します。

   1. [Audience Managerの新しい特性のテストセグメント &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html)を設定し、`Ad Cloud`を&#x200B;**[!UICONTROL Data Source]**&#x200B;として選択します。

      Audience Managerは、標準的なランディングページのエクスペリエンスを受け取るコントロールグループと、パーソナライズされたオンサイトエクスペリエンスを受け取るテストグループに、セグメントを自動的に分割します。

## 手順3: DSPの[!DNL Target]でA/B テストアクティビティを設定する

次の手順では、DSPのユースケースに関する情報を示します。

1. [Adobe Targetにログイン &#x200B;](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=ja)。

1. [A/B テストを作成](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. 「**[!UICONTROL Enter Activity URL]**」フィールドに、テストのランディングページ URLを入力します。

      >[!NOTE]
      >
      >複数のURLを使用して、ビュースルーサイトエントリをテストできます。 詳しくは、「[&#x200B; マルチページアクティビティ &#x200B;](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)」を参照してください。 Analyticsで[&#x200B; サイト入口レポート &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports)を作成することで、ページ URLで上位エントリを簡単に識別できます。

   1. 「**[!UICONTROL Goal]**」フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >[!DNL Analytics]が[!DNL Target]内のデータソースとして有効になっており、正しいレポートスイートが選択されていることを確認してください。

   1. **[!UICONTROL Priority]**&#x200B;を`High`または`999`に設定して、テストセグメントのユーザーが誤ったオンサイトエクスペリエンスを受け取ったときに競合を防ぎます。

   1. **[!UICONTROL Reporting Settings]**&#x200B;内で、DSP アカウントに接続されている&#x200B;**[!UICONTROL Company Name]**&#x200B;と&#x200B;**[!UICONTROL Report Suite]**&#x200B;を選択します。

      その他のレポートのヒントについては、「[&#x200B; レポートのベストプラクティスとトラブルシューティング &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=ja)」を参照してください。

   1. 「**[!UICONTROL Date Range]**」フィールドに、テストの適切な開始日と終了日を入力します。

   1. アクティビティにオーディエンスを追加します。

      1. 以前にAudience Managerで作成した[&#x200B; セグメントを選択して、ビュースルーオーディエンスをテストします](#view-through-framework)。

      1. **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**&#x200B;を選択し、**[!UICONTROL Value]** フィールドにDSP配置キーを入力して、クリックスルーのオーディエンスにTarget クエリ文字列パラメーターを使用します。

   1. **[!UICONTROL Traffic Allocation Method]**&#x200B;の場合、**[!UICONTROL Manual (Default)]**&#x200B;を選択し、オーディエンスを50/50に分割します。

   1. アクティビティを保存します。

1. [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)を使用して、A/B テスト ランディングページ テンプレートにデザイン変更を加えます。

   * エクスペリエンス A: パーソナライゼーションなしでデフォルト/コントロールのランディングページエクスペリエンスであるため、編集しないでください。

   * エクスペリエンス B: [!DNL Target] ユーザーインターフェイスを使用して、テストに含まれるアセット（見出し、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズします。

   >[!NOTE]
   >
   >クリエイティブテストのユースケースなど、Adobeのアカウントチームにお問い合わせください。

## 手順4: [!DNL Analytics for Target]で[!DNL Analytics] Analysis Workspaceを設定する

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] （A4T）は、広告主が[!DNL Target]個のコンバージョン指標とオーディエンスセグメントに基づいて[!DNL Analytics]個のアクティビティを作成し、[!DNL Analytics]をレポートソースとして使用して結果を測定できるクロスソリューション統合です。 そのアクティビティのすべてのレポートとセグメント化は、[!DNL Analytics] データ収集に基づいています。

実装手順へのリンクを含む[!DNL Analytics for Target]について詳しくは、「[Adobe Analytics as the reporting source for Adobe Target （A4T） &#x200B;](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=ja)」を参照してください。

### [!DNL Analytics for Target] パネルの設定

Analysis Workspaceで、[!DNL Analytics for Target panel]を設定して、[!DNL Target]のアクティビティとエクスペリエンスを分析します。 レポートに関する次の重要なポイントと情報を考慮してください。

#### 指標

* テストを実行したAdobe Advertising キャンペーン、パッケージ、またはプレースメントに固有のパネルをワークスペース内に作成します。 サマリービジュアライゼーションを使用して、[!DNL Target] テストのパフォーマンスと同じレポートでAdobe Advertising指標を表示します。

* 訪問やコンバージョンなどのオンサイト指標を活用してパフォーマンスを測定し、

* Adobe Advertisingの集約されたメディア指標（インプレッション数、クリック数、コストなど）は、[!DNL Target]指標と一致させることができません。

#### ディメンション

次のディメンションは[!DNL Analytics for Target]に関連しています：

* **[!UICONTROL Target Activities]**: A/B テストの名前

* **[!UICONTROL Target Experiences]**: アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**：同じ行のアクティビティ名とエクスペリエンス名

### [!DNL Target] データのAnalyticsのトラブルシューティング

Analysis Workspace内で、アクティビティとエクスペリエンスのデータが最小限に抑えられているか入力されていないことがわかったら、次の操作を行います。

* [!UICONTROL Supplemental Data ID]と[!DNL Target]の両方に同じ[!DNL Analytics] （SDID）が使用されていることを確認します。 SDID値を確認するには、キャンペーンがユーザーを促進しているランディングページで[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=ja)を使用します。

[Adobe Debuggerの補足データ ID （SDID）値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a）Adobe Debuggerに表示されている[!UICONTROL Hostname]が[!UICONTROL Solutions] > [!UICONTROL Target]に一致することを確認しますb）アクティビティの[!UICONTROL Tracking Server]に表示されている[!DNL Target]が（[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]に一致することを確認します。

  [!DNL Analytics For Target]では、Analytics用の[!DNL Analytics] データ収集サーバーに[!DNL Target]から[!DNL Modstats] トラッキング サーバーを呼び出して送信する必要があります。<!-- just "to Analytics?"-->

[Adobe Debuggerのホスト名の値](/help/integrations/assets/target-troubleshooting-hostname.png)

[Targetでのトラッキングサーバー値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 関連トピックス

* [TargetとAnalyticsの統合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=ja) - Analysis Workspaceで[!DNL Target] レポートを設定する方法について説明します。
* [A/B テストの概要](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - DSP広告で使用できるA/B テストアクティビティについて説明します。
* [&#x200B; エクスペリエンスとオファー](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - DSP テストユーザーが公開されるオンサイトコンテンツを決定するための[!DNL Target] ツールについて説明します。
* [信号、特性、セグメント &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html?lang=ja) - DSP ビュースルーテストに役立つ一部のAudience Manager ツールを定義します。
* [概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) - [!DNL Analytics for Advertising]が導入されました。これにより、Analytics インスタンスでのクリックスルーとビュースルーサイトインタラクションを追跡できます。

>[!MORELIKETHIS]
>
>* [Advertising Search、Social、およびCommerceの広告用にAdobe TargetでA/B テストを設定する](ab-tests-search.md)
