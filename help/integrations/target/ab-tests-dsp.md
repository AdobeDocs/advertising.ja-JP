---
title: Adobe TargetでのAdobe Advertising広告の A/B テストの設定
description: で A/B テストを設定する方法を説明します。 [!DNL Target] DSP広告用。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 48f755b6f3ac00a69086fe4c7ce69d320946635b
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 0%

---

# Adobe TargetでDSP Ads 用に A/B テストを設定する

<!-- In title and Heading1:  DSP and [!DNL Advertising Search, Social, & Commerce] Ads -->

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Advertising DSPのみの広告主*

Adobe AdvertisingとAdobe Targetを使用すると、マーケターは、有料メディアやオンサイトメッセージにわたって、パーソナライズされ、接続されたエクスペリエンスをより簡単に提供できます。 製品間でシグナルを共有することで、次のことができます。

* 顧客の広告露出をDSPキャンペーンから自社のオンサイトエクスペリエンスにリンクすることで、サイトのフォールスルー率を低下させます。

* Adobe Audience Managerの公開データを使用した広告メッセージでオンサイトエクスペリエンスをミラーリングし、Target のオーディエンスをクリックしてフィードすることで、A/B テストを確立します。

* Adobe Analyticsのシンプルなビジュアライゼーションを使用して、統合メッセージがオンサイトの目標上昇に与える影響を測定します。 [!DNL Target].

前提条件と、クリックスルーおよびビュースルートラッキングの設定、DSPとの間でのシグナル共有の実装の手順については、以下の節を参照してください。 [!DNL Target] A/B テストアクティビティを設定し、 [!DNL Analytics] Analysis Workspaceをクリックして、テストデータを表示します。

その他のご質問は、adcloud_support@adobe.comまでお問い合わせください。

## 前提条件

この使用例では、次の製品と統合が必要です。

* [!DNL Target]

* [[!DNL Analytics] （広告用）](/help/integrations/analytics/overview.md) 統合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 対象： [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 統合

* Audience Manager（ビュースルーテストの場合のみ必要）

## 手順 1：クリックスルーフレームワークの設定 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![クリックスルーフレームワーク](/help/integrations/assets/target-ct-framework.png)

クリックスルー URL にDSPマクロを追加する場合（ユーザーが広告をクリックしてランディングページに到達すると表示される URL）、DSPは配置キーを自動的に取り込みます ( `${TM_PLACEMENT_ID}` をクリックスルー URL に追加します。 このマクロは、数値配置 ID ではなく、英数字配置キーをキャプチャします。

![ランディングページの URL に追加されたクリックスルー URL](/help/integrations/assets/target-ct-url.jpg)

### (DSPのみ ) クリックスルー URL にDSPマクロを追加する

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

FlashトーキングまたはGoogle Campaign Manager 360 内で、各広告のクリックスルー URL を手動で更新し、AMO ID 変数を取得するために必要なマクロを含めます。 AMO ID 変数は、クリックデータをAdobe Analyticsに送信し、A/B テスト用の配置キーを共有するために使用されます。 手順については、次のページを参照してください。

* [追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Flashtalking] 広告タグ](/help/integrations/analytics/macros-flashtalking.md)

* [追加 [!DNL Analytics for Advertising] マクロ先 [!DNL Google Campaign Manager 360] 広告タグ](/help/integrations/analytics/macros-google-campaign-manager.md)

Adobeアカウントチームと Advertising Solutions Group(aac-advertising-solutions-group@adobe.com) に連絡して、必要な配置キーを取得し、設定を完了し、各クリックスルー URL に配置キーが入力されていることを確認してください。

## 手順 2:Audience Managerを使用したビュースルーフレームワークの設定 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![ビュースルーフレームワーク](/help/integrations/assets/targetr-vt-framework.png)

広告タグと配置設定にAudience Managerインプレッションイベントピクセルを追加することで、追加のビュースルーテスト機会のためのテストセグメントを作成できます。

1. 広告タグとDSPの配置設定にAudience Managerインプレッションイベントピクセルを実装します。

   手順については、[Advertising DSP Campaigns からメディア露出データを収集](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   必ず [DSPマクロ](/help/dsp/campaign-management/macros.md) を使用して、インプレッションイベントピクセルが渡すすべてのデータをキャプチャします。 `${TM_PLACEMENT_ID_NUM}` （数値のプレースメント ID）。

   >[!NOTE]
   >
   >クリック追跡 URL には、 `${TM_PLACEMENT_ID}` マクロは、代わりに英数字配置キーを使用します。 `${TM_PLACEMENT_ID_NUM}` （数値のプレースメント ID）。

1. DSPインプレッションAudience Managerからデータセグメントを設定します。

   1. セグメントデータが使用可能であることを確認します。

      1. [シグナルを検索](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) （の） [キー値ペア](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) これにより、どのレベルでセグメントユーザーをグループ化するかが決まります。

         の使用 [サポートキー](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) に、Audience Managerインプレッションイベントピクセルに追加したマクロに対応する値を指定します。

         例えば、特定のプレースメントのユーザーをグループ化するには、 `d_placement` キー。 値には、DSPマクロで取り込まれた実際の数値配置 ID(2501853など ) を使用します `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         検索結果にキーと値のペアのユーザー数が表示される場合は、ピクセルが正しく配置され、データが流れていることを示し、次の手順に進みます。

   1. [ルールベースの特性の作成](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) (Audience Managerでのセグメント作成用 )

      * テストアクティビティ内で簡単に識別できるように、特性に名前を付けます。 目的のフォルダーに特性を保存します。

      * 選択 `Ad Cloud` として **データソース**.

      * 特性の式には、 `d_event` として **キー** および `imp` として **値**.

   1. [テストセグメントの設定](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) Audience Managerの新しい特性の場合、「 `Ad Cloud` として **データソース**.

      Audience Managerは、セグメントを、標準のランディングページエクスペリエンスを受け取るコントロール母集団と、パーソナライズされたオンサイトエクスペリエンスを受け取るテストグループに自動的に分割します。

## 手順 3:Target での「A/B テスト」アクティビティの設定

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

以下の手順は、DSPの使用例に関する情報をハイライトします。 詳細な手順については、「」を参照してください。

1. [Adobe Targetにログイン](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [A/B テストの作成](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Adobe Analytics の **アクティビティ URL を入力** 「 」フィールドに、テストのランディングページ URL を入力します。

      >[!NOTE]
      >
      >複数の URL を使用して、ビュースルーサイトエントリをテストできます。 詳しくは、[複数ページアクティビティ](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; 上位のエントリをページ URL 別に簡単に識別するには、 [サイト入口レポート](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) Analytics で使用できます。

   1. Adobe Analytics の **目標** 「 」フィールドに、テストの成功指標を入力します。

      >[!NOTE]
      >
      >次を確認します。 [!DNL Analytics] は、内のデータソースとして有効になります。 [!DNL Target]」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」、「 」) が正しいレポートスイートが選択されている。

   1. を設定します。 **優先度** から `High` または `999` を使用して、テストセグメント内のユーザーが誤ったオンサイトエクスペリエンスを受け取った場合の競合を防ぎます。

   1. Within **レポート設定**&#x200B;を選択し、 **会社名** および **レポートスイート** DSPアカウントに接続しました。

      その他のレポートのヒントについては、[レポートのベストプラクティスとトラブルシューティング](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Adobe Analytics の **日付範囲** 「 」フィールドで、テストの適切な開始日と終了日を入力します。

   1. オーディエンスをアクティビティに追加します。

      1. を選択します。 [以前にAudience Managerで作成したセグメントで、ビュースルーオーディエンスをテストします。](#view-through-framework).

      1. 選択 **サイトのページ** > **ランディングページ** > **クエリ**&#x200B;をクリックし、DSPプレースメントキーを **値** フィールドを使用して、クリックスルーオーディエンスに Target クエリー文字列パラメーターを使用します。

   1. の **トラフィック配分方法**&#x200B;を選択します。 **手動（デフォルト）** オーディエンスを分割50/50た。

   1. アクティビティを保存します。

1. 用途 [!DNL Target] [Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) A/B テストのランディングページテンプレートをデザイン上で変更する場合。

   * エクスペリエンス A：パーソナライゼーションがないデフォルト/コントロールのランディングページエクスペリエンスなので、編集しないでください。

   * エクスペリエンス B: [!DNL Target] テストに含まれるアセット（ヘッドライン、コピー、ボタンの配置、クリエイティブなど）に基づいてランディングページテンプレートをカスタマイズするユーザーインターフェイス。

   >[!NOTE]
   >
   >クリエイティブテストの使用例などについては、担当のAdobeアカウントチームにお問い合わせください。

## 手順 4: [!DNL Analytics for Target] Analysis Workspace [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) は、広告主が [!DNL Target] に基づくアクティビティ [!DNL Analytics] コンバージョン指標およびオーディエンスセグメントを使用して結果を測定し、 [!DNL Analytics] を使用します。 そのアクティビティのすべてのレポートとセグメント化は、 [!DNL Analytics] データ収集を行います。

詳しくは、 [!DNL Analytics for Target]（導入手順へのリンクを含む）[Adobe TargetのレポートソースとしてのAdobe Analytics(A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### を設定します。 [!DNL Analytics for Target] パネル

Analysis Workspaceで、 [!DNL Analytics for Target panel] を分析するには、 [!DNL Target] アクティビティとエクスペリエンス。 レポートに関する次の重要なポインターおよび情報に注意してください。

#### 指標

* テストを実行したAdobe Advertisingキャンペーン、パッケージまたは配置に固有のパネルをワークスペース内に作成します。 概要ビジュアライゼーションを使用して、Target のテストAdobe Advertisingと同じレポートにパフォーマンス指標を表示します。

* オンサイト指標（訪問回数、コンバージョン数など）を使用してパフォーマンスを測定することを優先します。

* Adobe Advertising（インプレッション数、クリック数、コストなど）の集計メディア指標を Target 指標と一致させることはできないことを理解します。

#### Dimension

次のディメンションは、次に関係します。 [!DNL Analytics for Target]:

* **Target アクティビティ**:A/B テストの名前

* **Target エクスペリエンス**：アクティビティ内で使用されるランディングページエクスペリエンスの名前

* **Target アクティビティ** > **エクスペリエンス**：同じ行のアクティビティ名とエクスペリエンス名

### Analytics でのトラブルシューティング [!DNL Target] データ

Analysis Workspace内で、アクティビティとエクスペリエンスのデータが最小限である、または入力されていないことに気付いた場合は、次の操作を行います。

* Target と Analytics の両方で同じ Supplemental Data ID(SDID) が使用されていることを確認します。 SDID の値は、 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) をクリックします。

[Adobe Debuggerの追加データ ID(SDID) 値](/help/integrations/assets/target-troubleshooting-sdid.png)

* 同じランディングページで、a) ソリューション/ Target の下のAdobe Debuggerに表示されるホスト名が b) に表示されるトラッキングサーバー ( [!DNL Target] アクティビティの（目標と設定/レポート設定の下）を選択します。

  [!DNL Analytics For Target] にはが必要です [!DNL Analytics] からの呼び出しで送信されるトラッキングサーバー [!DNL Target] から [!DNL Modstats] Analytics のデータ収集サーバー。<!-- just "to Analytics?"-->

[ホスト名の値 (Adobe Debugger)](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target のトラッキングサーバー値](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 参考情報

* [Target と Analytics の統合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Analysis Workspaceで Target レポートを設定する方法を説明します。
* [A/B テストの概要](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - DSP広告で使用できる A/B テストアクティビティを表します。
* [エクスペリエンスとオファー](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 説明 [!DNL Target] DSPのテストユーザーが公開されるオンサイトコンテンツを決定するためのツール。
* [シグナル、特性、セグメント](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - DSPビュースルーテストに役立つAudience Managerツールの一部を定義します。
* [広告用 Analytics の概要](/help/integrations/analytics/overview.md) - Analytics for Advertising を導入します。これにより、Analytics インスタンス内でのクリックスルーおよびビュースルーサイトでのインタラクションを追跡できます。

<!-- 
>[!MORELIKETHIS]
>
>* 
-->