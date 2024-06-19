---
title: ブランドセーフティとメディア品質
description: ブランドセーフティとメディア品質機能の詳細をご覧ください。
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: c8cad651585210d46cb0237e1843952e5e5cec3e
workflow-type: tm+mt
source-wordcount: '1348'
ht-degree: 0%

---

# ブランドセーフティとメディア品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSPは、各キャンペーンがブランドセーフな環境で実際のユーザーに確実にリーチするためのブランド保護機能スイートを提供します。

アドビの不正監視チームは、次のような業界をリードするパートナーと緊密に連携しています [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]、および [!DNL WhiteOps]プラットフォーム上の在庫を慎重にキュレーションします。 DSPは、アドビの供給をプロアクティブに管理し、プラットフォーム全体のすべての広告主が人以外のトラフィック（ボット、クローラー、データセンタートラフィック、不正）から保護され、ブランドセーフなコンテキストでのみ配信されるようにします。

当社は、中央品質管理を提供するだけでなく、広告主がブランドに合致した管理を設計できるようにすることを信じています。 DSPはと統合されています [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]、および [!DNL Peer39]を使用して、各広告主が望ましいレベルの不正保護、コンテキストフィルタリングおよびキーワードターゲティングを選択できるようにします。

## 品質イニシアティブ

### を使用したインベントリの検証 [!DNL Ads.txt] サポート

[[!DNL Ads.txt]（の略） [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) は、が開始したイニシアチブ [!DNL Interactive Advertising Bureau] （[!DNL IAB]）、2017 年 6 月、オープンマーケットでの在庫の適切な表示を容易にし、それによってトラフィックやドメインスプーフィングの違法なソースと戦う。 参加する出版社および代理店は、以下を維持することにより、デジタルインベントリの販売を許可された会社、およびこれらの関係の性質を公表します。 `ads.txt` ドメインの最上位レベルにあるページ（など） `example.com/ads.txt`）に設定します。

DSPのサポート [!DNL ads.txt] 各出版社の `ads.txt` ファイルを開き、から購入するオプションを提供する検証済み [!DNL ads.txt] 販売者。 例えば、アクセスするセラーを照合する `nytimes.com` ニューヨークタイムズ紙に `ads.txt` ファイル、私たちは合法であるとされていないかを識別することができ、プレースメントが検証済みの売り手からのみ購入するように設定されている場合、犯罪者をブロックします。 <!-- can we actually mention NY Times? -->

デフォルトを設定できます [!DNL ads.txt] 各広告主のコントロール<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->、オプションで [各プレースメントの設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md) コピー先：

* ドメインの正規の直販業者からのみ在庫を購入する

* ドメインの認定された直販業者および再販業者のみから在庫を購入

* ドメインの認定された直販業者および再販業者からの購入在庫を優先順位付けする

* すべての販売者から在庫を購入

### プラットフォーム不正監視

DSPは、次のような主要な業界ベンダーと提携して、プラットフォーム全体で不正を管理するための強力な内部ツールとシステムを構築しています [!DNL Whiteops] および [!DNL Integral Ad Science].

また、Adobeはと緊密に連携します [!DNL IAB] および [!DNL TAG] 次のようなツールを活用して、広告主を保護するための堅牢な業界標準の不正ブロッキングを確保します。 [!DNL ads.txt] （前の節を参照）、 [!DNL IAB] ボットとスパイダーのリスト、 [!DNL TAG] データセンターの IP リスト。

品質に対する多次元アプローチにより、アドビのチームは異常と無効なトラフィックパターンを監視し、保護された在庫の無効なトラフィックが 3% 未満であることを保証します。 特定のドメイン上の在庫、特定のパブリッシャーまたはセラーからの在庫など、疑わしい在庫は、プラットフォーム全体で直ちにブロックされます。

### インベントリのマッピング、階層化、分類

インベントリマッピングは、すべての新しいインベントリがプラットフォームに追加される前に必要な、詳細なレビューとオンボーディングプロセスです。 このプロセスは、DSP上のすべての在庫の安全性と品質を確保するように設計されています。

* **マッピング :** インベントリチームは、各ドメインを慎重にレビューし、次のような側面を評価します。

   * ブランドセーフティ

   * 広告タイプの検証

   * 一般的なコンテンツ、重複ドメインおよびフェイク広告サービス

* **階層化：** 異なる階層に在庫を分類するために、エコシステム全体でのブランドプレゼンスを包括的に調べます。 次のことができます [プレースメントのターゲット設定](/help/dsp/campaign-management/placements/placement-settings.md) 次の層に対して、目的のリーチレベルを実現します。

   * **[!UICONTROL T1]** — ブランド名、国際的に認識できるサイト

   * **[!UICONTROL T2]**  – ユーザーが作成したコンテンツがなく、通常はグローバルに認識されない、最新の見栄えの良いサイト

   * **[!UICONTROL T3]** — ユーザー作成コンテンツとニッチコンテンツ

* **サイトの分類：** コンテンツのターゲティングとブロックを容易にするために、各プロパティに、プロパティのコンテンツに基づいてDSPで定義されたサイトカテゴリのタグを付けます。 次のことができます [各プレースメントに対してこれらのサイトカテゴリをターゲットにするか除外します](/help/dsp/campaign-management/placements/placement-settings.md) プレースメントの目標に基づいています。

### サイトブロックの包括的なサポート

DSPには、グローバルにブロックされたサイトリストと、広告主とアカウント用にカスタムのブロックされたサイトリストを作成するオプションの両方が用意されています。

#### DSP グローバルにブロックされたサイトの一覧 {#global-blocked-sites}

DSPは、広告を実行することが安全でないと見なされるサイトのグローバルにブロックされたサイトリストを保持します。 このリストには、好ましくないコンテンツ（憎悪や恐怖など）を含むサイトや、ボットに感染したサイト、偽のプレロール、不一致のドメイン、その他の不正行為が含まれています。

広告主を騙す活動を根絶するためのブランドセーフティイニシアチブの一環として、すべてのサイトは、チャートのブロックされたサイトリストの対策を使用してスクリーニングされます。 ブランドの安全性チェックに合格しないすべてのサイトは、グローバルにブロックされたサイトのリストに追加されます。 DSPはこのリストを動的に管理するので、最新のブランドセーフティ分析に基づいて、サイトはいつでもリストの表示と非表示を切り替えることができます。

グローバルにブロックされたサイトのリストに配置ターゲットとしてサイトを含めると、そのサイトには赤い感嘆符（!）のフラグが付きます。 これは、フラグが設定されたサイトで広告が実行されていないことを示します。

>[!NOTE]
>
>オプションで、「」を有効にして、信頼できるプライベート取引に添付された標準のディスプレイ広告のグローバルブロックサイトリストを回避できます[!UICONTROL Allow unscreened sites]の「」オプション [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md). 必要に応じて、Adobeアカウントチームは、必要に応じて、取引の公開者設定で公開（オークションレベル）取引のサイトブロックを無効にすることもできます。

#### アカウントレベルと広告主レベルのブロックされたサイトリスト

ユーザーは、アカウントレベルおよび広告主レベルのブロックされたサイトリストを維持することもできます<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->（すべてのプレースメントに自動的に使用されます）。 グローバルにブロックされたサイトの一覧に加えて、下位レベルのブロックされたサイトの一覧が適用されます。

## サードパーティの統合

### コンテキストフィルタリング

コンテキストフィルタリングを使用すると、広告が提供するページのコンテキストに基づいて、広告オポチュニティをターゲットに設定したりブロックしたりできます。 Adobeでは、業界の主要ベンダーとの統合により、状況に応じたフィルタリングを提供しています。 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39]. 現在のフィルターの例を次に示します [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]、および [!UICONTROL G-rated Sites].

広告主ごとに、デフォルトのコンテキストフィルターコントロールを設定できます<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->、オプションで [各プレースメントの設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用すると、追加料金が発生する場合があります。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![統合広告サイエンスロゴ](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ](/help/dsp/assets/peer39-logo.png)

### 入札前の不正ブロック

とのサードパーティ統合の活用 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39] キャンペーンからの人間以外のトラフィックをブロックする。 これらの統合により、業界をリードする入札前ブロック機能が提供され、キャンペーンで一般的および高度な無効トラフィック（GIVT および SIVT）の両方を最小限に抑えることができます。

各広告主に対して、デフォルトの入札前不正防止コントロールを設定できます<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->、オプションで [各プレースメントの設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用すると、追加料金が発生する場合があります。

機能について詳しくは、ご希望のベンダーに直接問い合わせるか、Adobeアカウントチームにお問い合わせください。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![統合広告サイエンスロゴ](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ](/help/dsp/assets/peer39-logo.png)

### Pre-Bid Viewability {#pre-bid-viewability}

業界をリードするパートナーが提供する Pre-bid viewability フィルター [!DNL DoubleVerify], [!DNL Oracle Advertising] （[!DNL Moat]）、および [!DNL Integral Ad Science] 広告主が、ビデオおよびディスプレイのインベントリ全体で、キャンペーンが目的のビューアビリティパフォーマンス目標を満たしていることを確認できます。

各広告主に対して、デフォルトのビューアビリティフィルターを設定できます<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->、オプションで [各プレースメントの設定のカスタマイズ](/help/dsp/campaign-management/placements/placement-settings.md). この機能を使用すると、追加料金が発生する場合があります。

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png) ![Oracle Advertising ロゴ](/help/dsp/assets/oracle-advertising-logo.png) ![統合広告サイエンスロゴ](/help/dsp/assets/ias-logo.png)

### トピックのターゲティング

DSP トピックのターゲット設定では、業界をリードするアドビのコンテキストパートナーを活用して、キーワードリストをターゲット設定したりブロックしたりできます [!DNL Comscore] および [!DNL Oracle Data Cloud] （formerly [!DNL Grapeshot]）に設定します。 トピックのターゲティングは、有害なコンテンツのブロックや、より大きな結果を確実にするコンテキストでの費用の確保など、ブランドに合致した環境で広告を常に提供するのに役立ちます。

トピックのターゲティングでは、パートナープラットフォームと直接カスタムトピックセグメントを作成する必要があります。 セグメントの作成後、次の操作を実行できます [でのセグメント ID のターゲット設定または除外 [!UICONTROL Audience Targeting] プレースメントごとのセクション](/help/dsp/campaign-management/placements/placement-settings.md). この機能には追加料金が発生する場合があります。

カスタムトピックセグメントを作成するには：

* を作成するには [!DNL Comscore] アカウントおよびカスタムセグメントの作成、次のログインをリクエストできます [!DNL Activation Segment Manager] 時刻 [https://agents.comscore.com](https://agents.comscore.com). を参照してください。 [[!DNL Comscore] ヘルプセンター](https://comscoreactivation.zendesk.com/hc/) カスタムセグメントの設定手順について詳しくは、を参照してください。 カスタムセグメントの料金はで表示されます。 [!DNL Segment Manager] 作成する際に選択します。

* を使用するには [!DNL Oracle Data Cloud]、連絡先 [!DNL Oracle Data Cloud] またはAdobeアカウントチームから入手できます。

![Comscore ロゴ](/help/dsp/assets/comscore-logo.png) ![Grapeshot ロゴ](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSPは次と提携しています [!DNL DoubleVerify] 申し出る [!DNL Authentic Brand Safety] ターゲティングソリューション。一貫性を保つため、すべての購入プラットフォームをまたいでターゲットとする、ブランドの安全要件の一元化されたセットを作成できます。

ビルドが完了したら、 [!DNL DoubleVerify] brand safety segment 必要なターゲティングを使用すると、DSP内で web 環境全体で事前入札と共に入札後のブロックルールをレプリケートできます。

以下を指定できます [!DNL DoubleVerify] 各広告主のセグメント ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->、オプションで [有効または無効 [!UICONTROL Authentic Brand Safety] プレースメントごとに](/help/dsp/campaign-management/placements/placement-settings.md). DSPは、セグメント ID の使用に対してアカウントに請求します。

機能について詳しくは、にお問い合わせください。 [!DNL DoubleVerify] 直接アクセスするか、Adobeアカウントチームにお問い合わせください。

![DoubleVerify ロゴ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
