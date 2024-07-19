---
title: ブランドセーフティとメディア品質
description: ブランドセーフティとメディア品質機能の詳細をご覧ください。
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: a927c073fd27e0b2c84bd1929eb4d6d233a29cb5
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# ブランドセーフティとメディア品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSPは、各キャンペーンがブランドセーフな環境で実際のユーザーに確実にリーチするためのブランド保護機能スイートを提供します。

アドビの不正監視チームは、[!DNL Interactive Advertising Bureau]、[!DNL Trust and Accountability Group] [!DNL (TAG)]、[!DNL WhiteOps] など業界をリードするパートナーと緊密に連携して、プラットフォーム上の在庫を慎重にキュレーションします。 DSPは、アドビの供給をプロアクティブに管理し、プラットフォーム全体のすべての広告主が人以外のトラフィック（ボット、クローラー、データセンタートラフィック、不正）から保護され、ブランドセーフなコンテキストでのみ配信されるようにします。

当社は、中央品質管理を提供するだけでなく、広告主がブランドに合致した管理を設計できるようにすることを信じています。 DSPは、[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Oracle Data Cloud] および [!DNL Peer39] との統合を提供し、各広告主が望ましいレベルの不正対策、コンテキストフィルタリングおよびキーワードターゲティングを選択できるようにします。

## 品質イニシアティブ

### [!DNL Ads.txt] サポートによる在庫検証

[[!DNL Ads.txt] は、を意味し  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt)2017 年 6 月に [!DNL Interactive Advertising Bureau] （[!DNL IAB]）が開始したイニシアチブで、オープンマーケットでの在庫の適切な表示を容易にし、それによってトラフィックやドメインスプーフィングの違法なソースと戦っています。 参加するパブリッシャーやディストリビューターは、ドメインの最上位レベルに `ads.txt` ページ（`example.com/ads.txt` など）を維持することで、デジタルインベントリを販売する権限のある会社と、それらの関係の性質を公に宣言します。

DSPでは、各出版社の `ads.txt` ファイルを読み取り、検証済みの [!DNL ads.txt] の販売者からのみ購入できるオプションを提供することで、[!DNL ads.txt] をサポートしています。 `nytimes.com` 例えば、ニューヨーク・タイムズの `ads.txt` ファイルにアクセスする際に見つかった売り手を照合することで、合法な売り手と合法でない売り手を特定できます。また、プレースメントが検証済みの売り手からのみ購入するように設定されている場合は、犯罪者をブロックします。<!-- can we actually mention NY Times? -->

各広告主に対してデフォルトの [!DNL ads.txt] コントロールを設定し <!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> 次に、オプションで [ 各プレースメントの設定をカスタマイズ ](/help/dsp/campaign-management/placements/placement-settings.md) できます。

* ドメインの正規の直販業者からのみ在庫を購入する

* ドメインの認定された直販業者および再販業者のみから在庫を購入

* ドメインの認定された直販業者および再販業者からの購入在庫を優先順位付けする

* すべての販売者から在庫を購入

### プラットフォーム不正監視

DSPは、[!DNL Whiteops] や [!DNL Integral Ad Science] などの業界をリードするベンダーと提携し、プラットフォーム全体で不正を管理するための強力な内部ツールとシステムを構築しています。

さらに、Adobeは [!DNL IAB] や [!DNL TAG] と緊密に連携し、[!DNL ads.txt] （前の節を参照）、[!DNL IAB] ボットとスパイダーのリスト、[!DNL TAG] データセンターの IP リストなどのツールを活用して、広告主を保護するための堅牢な業界標準の不正ブロッキングを確実に行います。

品質に対する多次元アプローチにより、アドビのチームは異常と無効なトラフィックパターンを監視し、保護された在庫の無効なトラフィックが 3% 未満であることを保証します。 特定のドメイン上の在庫、特定のパブリッシャーまたはセラーからの在庫など、疑わしい在庫は、プラットフォーム全体で直ちにブロックされます。

### インベントリのマッピング、階層化、分類

インベントリマッピングは、すべての新しいインベントリがプラットフォームに追加される前に必要な、詳細なレビューとオンボーディングプロセスです。 このプロセスは、DSP上のすべての在庫の安全性と品質を確保するように設計されています。

* **マッピング：** 在庫チームは、次のような側面を評価し、各ドメインを慎重にレビューします。

   * ブランドセーフティ

   * 広告タイプの検証

   * 一般的なコンテンツ、重複ドメインおよびフェイク広告サービス

* **階層化：** エコシステム全体におけるブランドプレゼンスを総合的に調査し、異なる階層にわたって在庫を分類します。 目的のリーチレベルに合わせて、これらの層に [ プレースメントをターゲットに ](/help/dsp/campaign-management/placements/placement-settings.md) 設定できます。

   * **[!UICONTROL T1]** — ブランド名、国際的に認識できるサイト

   * **[!UICONTROL T2]** - ユーザーが作成したコンテンツがなく、通常はグローバルな認識に欠ける、最新の見栄えのよいサイト

   * **[!UICONTROL T3]** - ユーザー作成コンテンツとニッチコンテンツ

* **サイトの分類：** コンテンツのターゲティングとブロックを容易にするために、各プロパティに、プロパティのコンテンツに基づいてDSPで定義されたサイトカテゴリのタグを付けます。 プレースメントの目標に基づいて ](/help/dsp/campaign-management/placements/placement-settings.md) プレースメントごとにこれらのサイトカテゴリを [ ターゲット設定または除外）できます。

### サイトブロックの包括的なサポート

DSPには、グローバルにブロックされたサイトリストと、広告主とアカウント用にカスタムのブロックされたサイトリストを作成するオプションの両方が用意されています。

#### DSP グローバルにブロックされたサイトの一覧 {#global-blocked-sites}

DSPは、広告を実行することが安全でないと見なされるサイトのグローバルにブロックされたサイトリストを保持します。 このリストには、好ましくないコンテンツ（憎悪や恐怖など）を含むサイトや、ボットに感染したサイト、偽のプレロール、不一致のドメイン、その他の不正行為が含まれています。

広告主を騙す活動を根絶するためのブランドセーフティイニシアチブの一環として、すべてのサイトは、チャートのブロックされたサイトリストの対策を使用してスクリーニングされます。 ブランドの安全性チェックに合格しないすべてのサイトは、グローバルにブロックされたサイトのリストに追加されます。 DSPはこのリストを動的に管理するので、最新のブランドセーフティ分析に基づいて、サイトはいつでもリストの表示と非表示を切り替えることができます。

グローバルにブロックされたサイトのリストに配置ターゲットとしてサイトを含めると、そのサイトには赤い感嘆符（!）のフラグが付きます。 これは、フラグが設定されたサイトで広告が実行されていないことを示します。

>[!NOTE]
>
>オプションで、[ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md) の「[!UICONTROL Allow unscreened sites]」オプションを有効にすることで、信頼されたプライベート取引に添付された標準のディスプレイ広告のグローバルブロックサイトリストをバイパスできます。 必要に応じて、Adobeアカウントチームは、必要に応じて、取引の公開者設定で公開（オークションレベル）取引のサイトブロックを無効にすることもできます。

#### アカウントレベルと広告主レベルのブロックされたサイトリスト

ユーザーは、アカウントレベルおよび広告主レベルでブロックされたサイトリストを管理することもできます。このリストは <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) --> すべてのプレースメントに対して自動的に使用されます。 グローバルにブロックされたサイトの一覧に加えて、下位レベルのブロックされたサイトの一覧が適用されます。

## サードパーティの統合

### コンテキストフィルタリング

コンテキストフィルタリングを使用すると、広告が提供するページのコンテキストに基づいて、広告オポチュニティをターゲットに設定したりブロックしたりできます。 Adobeでは、[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39] など、業界の主要ベンダーと統合してコンテキストに応じたフィルタリングを提供しています。 現在のフィルターの例としては、[!UICONTROL Adult Content]、[!UICONTROL Natural Disasters]、[!UICONTROL Legal Drinking Age]、[!UICONTROL MANGA]、[!UICONTROL Epidemics]、[!UICONTROL G-rated Sites] などがあります。

各広告主に対してデフォルトのコンテキストフィルターコントロールを設定し <!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> その後、オプションで [ 各プレースメントの設定をカスタマイズ ](/help/dsp/campaign-management/placements/placement-settings.md) できます。 この機能を使用すると、追加料金が発生する場合があります。

![Comscore ロゴ ](/help/dsp/assets/comscore-logo.png)![DoubleVerify ロゴ ](/help/dsp/assets/doubleverify-logo.png)![ 統合広告サイエンスロゴ ](/help/dsp/assets/ias-logo.png)![Peer39 ロゴ ](/help/dsp/assets/peer39-logo.png)

### 入札前の不正ブロック

[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39] とのサードパーティ統合を活用して、キャンペーンから人間以外のトラフィックをブロックします。 これらの統合により、業界をリードする入札前ブロック機能が提供され、キャンペーンで一般的および高度な無効トラフィック（GIVT および SIVT）の両方を最小限に抑えることができます。

各広告主に対してデフォルトの入札前不正ブロッキング制御を設定してから <!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> オプションで [ 各プレースメントの設定をカスタマイズ ](/help/dsp/campaign-management/placements/placement-settings.md) できます。 この機能を使用すると、追加料金が発生する場合があります。

機能について詳しくは、ご希望のベンダーに直接問い合わせるか、Adobeアカウントチームにお問い合わせください。

![DoubleVerify ロゴ ](/help/dsp/assets/doubleverify-logo.png)![ 統合広告サイエンスロゴ ](/help/dsp/assets/ias-logo.png)![Peer39 ロゴ ](/help/dsp/assets/peer39-logo.png)

### Pre-Bid Viewability {#pre-bid-viewability}

アドビの業界をリードするパートナーである [!DNL DoubleVerify]、[!DNL Oracle Advertising] （[!DNL Moat]）および [!DNL Integral Ad Science] を活用した Pre-bid Viewability フィルターにより、広告主は、ビデオおよびディスプレイの在庫全体で、キャンペーンが望ましいビューアビリティパフォーマンス目標を満たしていることを確認できます。

>[!NOTE]
>
>[!DNL Oracle] は、2024 年 9 月 30 日（PT）までに、[!DNL MOAT] の全サービスを含む広告事業を廃止する予定です。

各広告主に対してデフォルトのビューアビリティフィルターを設定し <!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> その後でオプションで [ 各プレースメントの設定をカスタマイズ ](/help/dsp/campaign-management/placements/placement-settings.md) できます。 この機能を使用すると、追加料金が発生する場合があります。

![DoubleVerify ロゴ ](/help/dsp/assets/doubleverify-logo.png) ![OracleAdvertising ロゴ ](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science ロゴ ](/help/dsp/assets/ias-logo.png)

### アテンションのターゲティングと測定

[!DNL Adelaide] とのパートナーシップ [!DNL Adobe's]、広告主に、アイトラッキング、露出、結果データに基づいてメディア品質を測定するアデレード指標「[!DNL Attention Units]」のサポートを提供します。

[ プレースメントレベルの事前入札注意ターゲティング ](/help/dsp/campaign-management/placements/placement-settings.md) を使用すると、広告主は特定の注意レベルをターゲットにして、顧客エンゲージメントを向上させることができます。

さらに、広告主は、任意のキャンペーンで [ プレースメントレベルの [!UICONTROL Attention Score] 指標のトラッキング ](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) （インプレッション間の重み付け平均 [!DNL Attention Units] 数）を有効にして、どのプレースメント戦術が最適なビジネス成果を生み出すかを把握できます。

各機能に対して追加料金が発生します。

### トピックのターゲティング

DSP トピックのターゲット設定を使用すると、業界をリードするアドビのコンテキストパートナー [!DNL Comscore] and [!DNL Oracle Data Cloud] （旧称 [!DNL Grapeshot]）を活用して、キーワードリストをターゲット設定したりブロックしたりできます。 トピックのターゲティングは、有害なコンテンツのブロックや、より大きな結果を確実にするコンテキストでの費用の確保など、ブランドに合致した環境で広告を常に提供するのに役立ちます。

>[!NOTE]
>
>[!DNL Oracle] は、2024 年 9 月 30 日（PT）までに、[!DNL Oracle Data Cloud] （旧 [!DNL Grapeshot]）のすべてのサービスを含む広告事業を廃止する予定です。

トピックのターゲティングでは、パートナープラットフォームと直接カスタムトピックセグメントを作成する必要があります。 セグメントを作成したら、[ 各プレースメントの「[!UICONTROL Audience Targeting]」セクションでセグメント ID をターゲット設定または除外 ](/help/dsp/campaign-management/placements/placement-settings.md) できます。 この機能には追加料金が発生する場合があります。

[!DNL Comscore] アカウントを作成し、カスタムトピックセグメントを作成するには、[https://agents.comscore.com](https://agents.comscore.com) で [!DNL Activation Segment Manager] のログインをリクエストします。 カスタムセグメントの設定手順について詳しくは、[[!DNL Comscore]  ヘルプセンター ](https://comscoreactivation.zendesk.com/hc/) を参照してください。 カスタムセグメントの料金は、カスタムセグメントの作成時に [!DNL Segment Manager] に表示されます。

![Comscore ロゴ ](/help/dsp/assets/comscore-logo.png)![Grapeshot ロゴ ](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSPは [!DNL DoubleVerify] と提携し、[!DNL Authentic Brand Safety] のターゲティングソリューションを提供しています。これにより、一貫性を保つためにすべての購入プラットフォームをまたいでターゲットにする、一連のブランドセーフティ要件を一元的に作成できます。

必要なターゲティングを持つ [!DNL DoubleVerify] ブランドセーフティセグメントを作成したら、DSP内でそれを使用して、web 環境全体で事前入札を含む入札後のブロックルールをレプリケートできます。

各広告主に対して [!DNL DoubleVerify] セグメント ID を指定し <!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> 必要に応じて [ プレースメントごとに [!UICONTROL Authentic Brand Safety] を有効または無効にする ](/help/dsp/campaign-management/placements/placement-settings.md) ことができます。 DSPは、セグメント ID の使用に対してアカウントに請求します。

機能について詳しくは、[!DNL DoubleVerify] に直接問い合わせるか、Adobeアカウントチームにお問い合わせください。

![DoubleVerify ロゴ ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
