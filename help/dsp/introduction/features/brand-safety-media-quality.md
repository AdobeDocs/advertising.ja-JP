---
title: ブランドセーフティおよびメディア品質
description: ブランドセーフティとメディア品質機能について詳しく見る。
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
TQID: https://experienceleague.adobe.com/-buJmAx0gdtqiPETqfBFcr90LAHly8BNyjM6lVO-JKc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 47596cdd765ba7da7c10e21388f0230327b49c01
workflow-type: tm+mt
source-wordcount: 1445
ht-degree: 0%

---

# ブランドセーフティおよびメディア品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSPは、それぞれのキャンペーンがブランドを保護した環境で実際のユーザーにリーチできるように、一連のブランド保護機能を提供します。

アドビの不正監視チームは、[!DNL Interactive Advertising Bureau]、[!DNL Trust and Accountability Group]、[!DNL (TAG)]、[!DNL WhiteOps]などの業界をリードするパートナーと緊密に連携し、プラットフォーム上で在庫を慎重に監修しています。 DSPでは、供給を先見的に管理することで、プラットフォーム全体のあらゆる広告主を人間以外のトラフィック（ボット、web クローラー、データセンターのトラフィック、不正行為）から保護し、ブランドが安全な状況でのみ配信しています。

当社では、一元的な品質管理を提供するだけでなく、広告主が自社ブランドに即した管理機能を設計できるようにしています。 DSPは、[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39]との統合機能を提供しており、各広告主が希望するレベルの不正利用防止、コンテクスト型フィルタリング、キーワードターゲティングを選択できるようになります。

## 質の高い施策

### [!DNL Ads.txt]をサポートした在庫確認

[[!DNL Ads.txt]は、 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt)を表し、[!DNL Interactive Advertising Bureau] （[!DNL IAB]）が2017年6月に開始したイニシアチブで、オープンマーケットでの在庫の適切な表現を促進し、不正なトラフィック源やドメインのなりすましを防止します。 参加しているパブリッシャーやディストリビューターは、ドメインのトップレベルの`ads.txt` ページ（`example.com/ads.txt`など）を維持することで、デジタル在庫の販売を許可された企業とそれらの関係の性質を公に宣言します。

DSPでは、各発行者の`ads.txt` ファイルを読み取り、検証済みの[!DNL ads.txt]販売者からのみ購入できるオプションを提供することで、[!DNL ads.txt]をサポートしています。 例えば、`nytimes.com`へのアクセスが確認されている販売者をNew York Timesの`ads.txt` ファイルと一致させることで、どの販売者が正当で、どれが正当でないかを特定できます。また、プレースメントが検証済みの販売者からのみ購入するように設定されている場合は、違反者をブロックします。<!-- can we actually mention NY Times? -->

各広告主<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->に対してデフォルトの[!DNL ads.txt] コントロールを設定し、オプションで[各プレースメント &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)の設定を次のようにカスタマイズできます。

* ドメインの承認済みの直接販売者からのみ在庫を購入する

* ドメインの承認済みの直接販売者と再販者からのみ在庫を購入する

* ドメインの承認済みの直接販売者と再販者からの購入在庫を優先させる

* すべての販売者から在庫を購入する

### プラットフォーム不正監視

DSPは、[!DNL Whiteops]や[!DNL Integral Ad Science]などの主要な業界ベンダーと提携して、アドビのプラットフォーム全体で不正行為を管理するための強力な社内ツールやシステムを構築しています。

さらに、Adobeは[!DNL IAB]および[!DNL TAG]と緊密に連携し、業界標準の強力な不正ブロックを確保して[!DNL ads.txt] （前の節を参照）、[!DNL IAB] ボットとスパイダーのリスト、[!DNL TAG] データセンターのIP リストなどのツールを活用して、広告主を保護します。

多次元的な品質アプローチを通じて、異常値と無効なトラフィックパターンを監視し、保護された在庫の無効なトラフィックが3%未満であることを保証します。 特定のドメインや特定のメディア企業や販売者からの在庫など、疑わしい在庫は、プラットフォーム全体ですぐにブロックされます。

### 在庫のマッピング、階層化、分類

在庫マッピングとは、新しい在庫をプラットフォームに追加する前に、すべての在庫を確認し、オンボーディングする必要がある詳細なプロセスです。 このプロセスは、DSPのすべての在庫の安全性と品質を確保するように設計されています。

* **マッピング：**&#x200B;当社のインベントリ チームは、以下のような側面を評価しながら、各ドメインを慎重にレビューします。

   * ブランドセーフティ

   * 広告タイプの検証

   * 一般的なコンテンツ、重複したドメイン、偽の広告サービング

* **階層化：**&#x200B;全体的なエコシステムのブランドプレゼンスを総合的に調査して、異なる階層の在庫を分類します。 プレースメント [&#128279;](/help/dsp/campaign-management/placements/placement-settings.md)をこれらの階層に ターゲット設定して、目的のレベルのリーチを行うことができます。

   * **[!UICONTROL T1]** — ブランド名で国際的に認知されたサイト

   * **[!UICONTROL T2]** – 最新で最新の、ユーザー生成コンテンツがなく、通常はグローバル認識が不足している見栄えのいいサイト

   * **[!UICONTROL T3]** — ユーザー生成コンテンツとニッチなコンテンツ

* **サイトのカテゴリ化：** コンテンツのターゲティングとブロックを容易にするために、各プロパティにプロパティの内容に基づいてDSP定義のサイト カテゴリをタグ付けします。 プレースメントの目標に基づいて、各プレースメント [&#128279;](/help/dsp/campaign-management/placements/placement-settings.md)に対してこれらのサイトカテゴリを ターゲットまたは除外できます。

### サイトブロッキングの包括的なサポート

DSPには、グローバルにブロックされたサイトリストと、広告主とアカウントのカスタムブロックされたサイトリストを作成するオプションの両方が用意されています。

#### DSPのグローバルにブロックされたサイトの一覧 {#global-blocked-sites}

DSPでは、広告を実行する上で安全でないと判断されたサイトのリストを、グローバルにブロックして維持します。 このリストには、好ましくないコンテンツ（ヘイトやテロなど）を掲載したサイトや、ボット、偽のプレロール、不一致ドメイン、その他の不正なアクティビティに感染したサイトが含まれています。

広告主を詐欺する行為を根絶するためのブランドセーフティの取り組みの一環として、すべてのサイトがチャートブロックされたサイトリストの指標を使用してスクリーニングされます。 ブランドセーフティチェックに合格しないすべてのサイトは、グローバルにブロックされたサイトリストに追加されます。 DSPでは、そうしたリストを動的に管理するため、最新のブランドセーフティ分析にもとづいて、サイトはいつでもリストの上または外に移動できます。

グローバルにブロックされたサイト リストに配置ターゲットとしてサイトを含めると、そのサイトに赤い感嘆符（!）が付きます。 これは、フラグが付けられたサイトで広告が実行されないことを示します。

>[!NOTE]
>
>[&#x200B; プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)で「[!UICONTROL Allow unscreened sites]」オプションを有効にすることで、信頼できるプライベート取引に添付された標準ディスプレイ広告のグローバルブロックサイトリストをオプションでバイパスできます。 必要に応じて、Adobe アカウントチームは、取引用のパブリッシャー設定のパブリック（オークションレベル）取引のサイトブロッキングをオプションで無効にすることもできます。

#### アカウントレベルと広告主レベルのブロックされたサイトリスト

ユーザーは、アカウントレベルと広告主レベルのブロックされたサイトリスト <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->を管理することもできます。これらのサイトリストは、すべてのプレースメントに自動的に使用されます。 グローバルにブロックされたサイトリストに加えて、下位レベルのブロックされたサイトリストが適用されます。

## サードパーティ製アプリケーションとの統合

### コンテキストフィルタリング

コンテキストフィルタリングを使用すると、広告が配信されるページのコンテキストに基づいて、広告機会をターゲットまたはブロックできます。 Adobeは、業界の主要ベンダー[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39]との統合により、コンテキストフィルタリングを提供します。 現在のフィルターの例には、[!UICONTROL Adult Content]、[!UICONTROL Natural Disasters]、[!UICONTROL Legal Drinking Age]、[!UICONTROL MANGA]、[!UICONTROL Epidemics]および[!UICONTROL G-rated Sites]が含まれます。

広告主<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->ごとにデフォルトのコンテキストフィルター制御を設定し、オプションで[各プレースメントの設定をカスタマイズ &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)できます。 この機能を使用する場合、追加料金が適用される場合があります。

![Comscore ロゴ &#x200B;](/help/dsp/assets/comscore-logo.png) ![DoubleVerify ロゴ &#x200B;](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ロゴ &#x200B;](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ &#x200B;](/help/dsp/assets/peer39-logo.png)

### 入札前の不正行為のブロック

[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39]のサードパーティとの統合を活用して、キャンペーンからの人間以外のトラフィックをブロックします。 これらの統合は、業界をリードする入札前ブロック機能を提供し、キャンペーンにおける一般的なトラフィックと高度な無効トラフィック（GIVTおよびSIVT）の両方を最小限に抑えます。

各広告主<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->に対してデフォルトの入札前の不正防止ブロック制御を設定し、オプションで[各配置の設定をカスタマイズ &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)できます。 この機能を使用する場合、追加料金が適用される場合があります。

機能の詳細については、ご希望のベンダーに直接お問い合わせいただくか、Adobeアカウントチームにお問い合わせください。

![DoubleVerify ロゴ &#x200B;](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science ロゴ &#x200B;](/help/dsp/assets/ias-logo.png) ![Peer39 ロゴ &#x200B;](/help/dsp/assets/peer39-logo.png)

### 入札前の視認性 {#pre-bid-viewability}

業界最先端のパートナー[!DNL DoubleVerify]および[!DNL Integral Ad Science]が提供する入札前の視聴可能性フィルターを使用すると、広告主は、ビデオおよびディスプレイのインベントリ全体で、キャンペーンが希望する視聴可能性パフォーマンス目標を満たしていることを確認できます。

各広告主<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->に対してデフォルトの表示可能性フィルターを設定し、オプションで[各プレースメントの設定をカスタマイズ &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)できます。 この機能を使用する場合、追加料金が適用される場合があります。

![DoubleVerify ロゴ &#x200B;](/help/dsp/assets/doubleverify-logo.png) ![統合広告サイエンス ロゴ &#x200B;](/help/dsp/assets/ias-logo.png)

### アテンションのターゲティングと測定

[!DNL Adobe's]と[!DNL Adelaide]のパートナーシップにより、広告主は、アイトラッキング、露出、結果データに基づいてメディア品質を測定するアデレード指標「[!DNL Attention Units]」をサポートできます。

[広告主は、プレースメントレベルの入札前アテンションのターゲティング &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)により、特定のアテンションのレベルをターゲットにして、顧客エンゲージメントを向上させることができます。

さらに、広告主は、あらゆるキャンペーンに対してプレースメントレベル [!UICONTROL Attention Score]指標[&#128279;](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement)の トラッキング（インプレッションの重み付け平均数[!DNL Attention Units]）を有効にして、どのプレースメント戦術が最も優れたビジネス成果を生み出すのかを把握できます。

追加料金は、個別の機能ごとに適用されます。

### トピックターゲティング

DSPのトピックターゲティングでは、業界をリードするコンテキストパートナー[!DNL Comscore]を活用して、キーワードリストをターゲットにしたりブロックしたりすることができます。 トピック別ターゲティングを実施することで、有害なコンテンツをブロックしたり、より大きな成果を生み出すコンテクストで費用を確保したりするなど、広告を企業に合った環境で常に提供することができます。

トピックターゲティングでは、パートナープラットフォームで直接カスタムトピックセグメントを作成する必要があります。 セグメントを作成したら、各プレースメント [&#128279;](/help/dsp/campaign-management/placements/placement-settings.md)の[!UICONTROL Audience Targeting] セクションでセグメント IDを ターゲットまたは除外できます。 この機能には追加料金が適用される場合があります。

[!DNL Comscore] アカウントを作成してカスタム トピックセグメントを作成するには、[!DNL Activation Segment Manager]の[https://agents.comscore.com](https://agents.comscore.com)へのログインをリクエストできます。 カスタムセグメントの設定方法について詳しくは、[[!DNL Comscore]  ヘルプセンター](https://comscoreactivation.zendesk.com/hc/)を参照してください。 カスタムセグメントを作成すると、カスタムセグメントの料金が[!DNL Segment Manager]に表示されます。

![Comscore ロゴ &#x200B;](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Suitability]

DSPは[!DNL DoubleVerify]と提携して[!DNL Authentic Brand Suitability] ターゲティングソリューションを提供しています。これにより、ブランドの適合性に関する一元的な要件を作成し、あらゆる購買プラットフォームをまたいで一貫性を確保できます。

必要なターゲティングを使用して[!DNL DoubleVerify] セグメントを構築したら、DSP内で使用して、入札後のブロックルールをweb環境全体で事前入札とレプリケートできます。

各広告主に[!DNL DoubleVerify] セグメント IDを指定し、オプションで[各プレースメントに[!UICONTROL Authentic Brand Suitability]を有効または無効にできます](/help/dsp/campaign-management/placements/placement-settings.md)。 DSPは、セグメント IDの使用状況についてアカウントに請求します。

機能の詳細については、[!DNL DoubleVerify]に直接お問い合わせいただくか、Adobe アカウントチームにお問い合わせください。

![DoubleVerify ロゴ &#x200B;](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
