---
title: プレースメント設定
description: 使用可能なプレースメント設定の説明を参照してください。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 9586b743df5af61db81f781224bed28b02e0c4a8
workflow-type: tm+mt
source-wordcount: '3540'
ht-degree: 0%

---

# プレースメント設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** プレースメント名。

>[!TIP]
>状況に応じて意味のある命名規則を使用します。 推奨される命名規則の 1 つは、です。*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.」と入力します。

**[!UICONTROL Status]:** プレースメントのステータス： *[!UICONTROL Active]* （デフォルト）または *[!UICONTROL Paused]*.

>[!TIP]
>ベストプラクティスは、ローンチの準備が整うまでプレースメントを一時停止することです。

**[!UICONTROL Details]:** （読み取り専用）該当する広告タイプ、プレースメントを作成または作成したアカウント、親キャンペーン。 詳細を表示するには、をクリックします **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** 既存のプレースメントテンプレートのリストを開きます。 テンプレートからターゲティング設定を自動入力するには：

1. 次のいずれかの操作をおこないます。

   * テンプレートからすべてのターゲットを再利用するには、テンプレート名の横にあるチェックボックスを選択します。

   * テンプレートから個々のターゲット・タイプを再利用するには、テンプレート名を展開し、再利用するターゲット・タイプの横にあるチェック・ボックスを選択します。

1. クリック **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （ビデオ広告フォーマットのみ）右側の Forecast プロジェクションを計算するために使用される広告期間および/または広告仕様。 フィールドは、広告タイプによって異なります。

**[!UICONTROL Environment]:** （ユニバーサルビデオ広告形式のみ）プレースメントのターゲットとして含めるデバイス環境（デスクトップ、モバイル、接続されたテレビ）。 1 つ以上を指定してください。

カスタムレポートでは、プレースメントレベルのディメンション「デバイス環境」は、ターゲット環境を示します。

**[!UICONTROL Placement tags]:** （オプション）このプレースメントを見つけるのに役立つキーワードまたはニックネーム。

## 目標

**[!UICONTROL Package]:** （オプション）プレースメントが割り当てられるパッケージ。 クリック ![編集](/help/dsp/assets/edit.png) 既存のパッケージを選択するか、パッケージを作成します。 プレースメントをパッケージに割り当てると、 [!UICONTROL Goals] セクションが、パッケージのフライト日、配信目標、予算で更新されます。

**[!UICONTROL Flight Dates]:** プレースメントの開始日と終了日。 承認済みの広告は、プレースメントがアクティブで、アクティブなパッケージまたはキャンペーンに割り当てられている場合、フライト中に実行できます。

パッケージ（該当する場合）またはキャンペーンの日付は、デフォルトで自動入力されます。

>[!NOTE]
>
>* フライト日は、キャンペーンフライト日とパッケージフライト日の範囲内に含める必要があります。

### パッケージレベルのペーシングを使用してパッケージに割り当てられたプレースメント

**[!UICONTROL Placement Funding]:** プレースメントの予算設定方法：

* *[!UICONTROL Optimize based on performance]:* パッケージレベルで予算を制御します。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* 最小および/または最大のプレースメント予算を設定できます。 予算の種類を少なくとも 1 つ指定してください：

   * *[!UICONTROL Maximum Budget]*：値と期間（*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*）に設定します。

   * *[!UICONTROL Minimum Budget]*：パッケージ予算に対する割合としての最小予算。 インターバル キャップを指定すると、最小の予算値は常にインターバル キャップのパーセンテージとして計算されます。 それ以外の場合は、パッケージ予算のパーセンテージとして計算されます。

**[!UICONTROL Max Bid]:** 1000 インプレッションの支払いの上限。

**[!UICONTROL Placement Pre-bid Filters]:** 入札が行われるためには、最大 5 つの KPI しきい値（最小視聴可能指標やクリックスルー率など）を満たす必要があります。 事前入札フィルターは最適化戦術として使用できますが、各ルールによってこのプレースメントが入札できる機会が制限される可能性があることを理解してください。 フィルターを追加または編集するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作をおこないます。
   * フィルターを追加するには：
      1. クリック **[!UICONTROL Add Filter]**.
      1. 次の **[!UICONTROL Only bid if]**&#x200B;指標を選択し、値を入力します。
   * フィルターを削除するには、をクリックします **[!UICONTROL X]** フィルター行
1. クリック **[!UICONTROL Save]**.

各 pre-bid フィルターの説明については、「」を参照してください[プレースメントレベルの事前入札フィルターとその使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).」と入力します。

### その他のすべてのプレースメント

**[!UICONTROL Budget Goal]:** 総予算の上限と予算間隔（*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*）に設定します。

**[!UICONTROL Gross Budget Goal]:** （利益管理のみを使用するキャンペーンにおけるプレースメント）総予算の上限と予算間隔（*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*）に設定します。

**[!UICONTROL Optimization Goal]:**  パッケージの最適化目標。 各最適化目標の説明については、「」を参照してください[最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md)」と入力します。

**[!UICONTROL Target Goal]:** パフォーマンスの追跡に使用されるターゲット目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、意思決定には使用されません。

**[!UICONTROL Pace on]:** ペーシングの基礎：

* **[!UICONTROL Budget goal]:** （デフォルト）このオプションは、割り当てられた予算内でできるだけ多くのインプレッションを配信します。

* **[!UICONTROL Impressions]:** このオプションは、指定された期間内に指定された数に達するまでインプレッションを配信します。 このオプションを選択した場合は、インプレッションの数と間隔を指定します。 *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** 1000 インプレッションの支払いの上限。

**[!UICONTROL Flight pacing]:** （プレースメントレベルのペーシングのみを使用したプレースメント）広告配信のペーシング方法：

* *[!UICONTROL Even]:* （デフォルト）各フライト全体を通して配信を均等にペースで進めます。フライトの前半で配信の 50% をターゲットにします。

* *[!UICONTROL Slightly Ahead]:* （デフォルト）配信が加速されるので、投入期間の半ばで 55～65% 完了します。

* *[!UICONTROL Frontload]:* 配信を高速化して、フライトの半ばで 65～75% 完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を高速化して、飛行の半ばで 75～85% 完了するようにします。

**[!UICONTROL Intraday pacing]:** （プレースメントレベルのペーシングのみを使用したプレースメント）フライト内で毎日広告をペースで配信する方法：

* *[!UICONTROL Even]:* （デフォルト）在庫の可用性に基づいて配信をスケーリングします。 通常、オークションの量が多い昼間は 1 時間あたりにより多くの広告が配信され、朝と夜にはより少ない広告が配信されます。

* *[!UICONTROL ASAP]:* （デフォルト）配信を 2 倍の速度まで高速化します *偶数*.

  >[!CAUTION]
  >
  >このオプションは、パフォーマンスに悪影響を与える可能性があります。 配信の優先順位を完全に設定し、パフォーマンスの最適化よりも費用がかかる場合にのみ使用します。

**[!UICONTROL Placement Pre-bid Filters]:** （任意）入札が発生するには最大 5 つのフィルターに適合する必要があります。 事前入札フィルターは最適化戦術として使用できますが、各ルールによって、このプレースメントが入札できる機会が制限される可能性があることに注意してください。 フィルターを追加または編集するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作をおこないます。
   * フィルターを追加するには：
      1. クリック **[!UICONTROL Add Filter]**.
      1. 次の **[!UICONTROL Only bid if]**&#x200B;指標を選択し、値を入力します。
   * フィルターを削除するには、をクリックします **[!UICONTROL X]** フィルター行
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （任意）プレースメントに広告を含めるか除外する特定の場所。 場所を指定しない場合は、すべての場所がターゲットになります。

>[!NOTE]
>
>Roku プレースメントでは、市区町村と DMA の場所は使用できません。

場所を指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作をおこないます。
   * 国、都道府県、市区町村、DMA、連邦立法区または州立法区を含めるか除外するには、次の手順を実行します。
      1. 左側の列で場所のタイプを選択します。
      1. （必要に応じて）場所をクリックして展開します。
      1. 場所の横にある「」をクリックします *[!UICONTROL Include]* ターゲットとして含める、または *[!UICONTROL Exclude]* ターゲットとして除外します。
   * 郵便番号を検索し、選択したすべての結果を含めるか除外するには：
      1. クリック **[!UICONTROL Search Postal Code]**.
      1. 国を選択します。
      1. 市区町村名を入力し、 ![編集](/help/dsp/assets/search.png).
      1. 正しい検索結果をクリックします。
      1. クリック *[!UICONTROL Include All]* すべてのロケーションをターゲットとして含めるには、または *[!UICONTROL Exclude All]* すべての場所をターゲットとして除外します。
   * 郵便番号を入力または貼り付け、すべてを含めるか除外するには、次の手順を実行します。
      1. クリック **[!UICONTROL Paste Postal Code]**.
      1. 国を選択します。
      1. 1000 件までの郵便番号を入力または貼り付けます。
1 行に 1 つの郵便番号を含めるか、コンマまたはタブで区切って複数の値を入力します。
      1. クリック *[!UICONTROL Include All]* すべてのロケーションをターゲットとして含めるには、または *[!UICONTROL Exclude All]* すべての場所をターゲットとして除外します。
   * から場所を削除するには [!UICONTROL Included] または [!UICONTROL Excluded] リスト、クリック **[!UICONTROL X]** 右側の列の場所の横。
1. クリック **[!UICONTROL Done]**.

>[!NOTE]
>
>* すべての国に都道府県、市区町村または郵便番号の場所があるわけではありません。
>* DMA （指定市場地域）、連邦立法区、州立法区は、米国の場所でのみ使用できます。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** ターゲットとして含めるか除外する在庫ソース。 ほとんどのプレースメント タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 の場合 [!DNL Roku] プレースメントでは、在庫タイプとソースを指定する必要があります。 次のタイプの在庫から選択できます。

* [!UICONTROL Public]:（Roku を除くすべてのプレースメントタイプ）DSPがアクセスできるすべてのオープン交換在庫。 公開在庫を含めたり除外したりできます。

  このリストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合は、フィード名、フィードキー、または選択した特性タグで検索できます。

* [!UICONTROL Private] | [!UICONTROL Roku Private]：既存のプライベート取引（または既存のプライベート [!DNL Roku] の取引 [!DNL Roku] プレースメント）を使用する場合は、DSPで設定したパブリッシャーを使用します。 公開在庫を含めることはできますが、除外することはできません。

  キーワード、キー、取引 ID またはカスタムタグでリストを検索できます。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: （任意）入札価格アルゴリズムを上書きして、少なくとも取引の固定価格とフロア価格を入札します。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]：すべて [プレミアム、保証なし [!UICONTROL On Demand] 在庫](/help/dsp/inventory/on-demand-inventory-about.md) （または [!UICONTROL On Demand] [!DNL Roku] の取引 [!DNL Roku] 登録しているプレースメント） [!DNL DSP]. 次を含めたり除外したりできます [!UICONTROL On Demand] 在庫。

  このリストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合は、フィード名、フィード キー、または選択した発行元の地域、カテゴリ タグ、特性タグで検索できます。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: （任意）入札価格アルゴリズムを上書きして、少なくとも取引の固定価格とフロア価格を入札します。

在庫ターゲティングを指定する手順は、次のとおりです。

* 在庫タイプを除外するには、名前の横にあるチェック ボックスをオフにします。
* 在庫タイプをターゲットにする手順は、次のとおりです。
   1. 在庫タイプ名の横にあるチェックボックスをオンにします。
   1. （オプション）ソースを次のように変更します。
      1. クリック ![編集](/help/dsp/assets/edit.png).
      1. （[!UICONTROL Public] および [!UICONTROL On Demand] 在庫）クリック **[!UICONTROL View by Source]** または **[!UICONTROL View by Feed]** ソースのリスト方法を変更する
      1. （該当する場合）必要に応じて在庫をフィルタリングします。
      1. 含めるソースと除外するソースを指定します。
         * を含めるには [!UICONTROL Public] または [!UICONTROL On Demand] ソース、クリック **[!UICONTROL Include]** ソース名の隣。
         * 次を含める [!UICONTROL Private] ソース :
            * すべての在庫を取引に含めるには、 **[!UICONTROL Include all]** 取引名の横。
            * 個別の在庫ソースを含めるには、取引名を展開し、ソース名の横にあるチェックボックスをクリックします。
         * を除外する場合 [!UICONTROL Public] または [!UICONTROL On source]を選択し、 **[!UICONTROL Exclude]** ソース名の隣。
   1. （オプション）ターゲット情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Save & Export]**.
   1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>登録している場合 [!UICONTROL On Demand] 在庫はあるが、ターゲットとするパブリッシャーまたは取引が見つからない場合は、取引のステータスを確認します。 ステータスの詳細については、を参照してください。 [について [!DNL On Demand] プレミアム在庫](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** （ビデオプレースメントのみ）アウトストリームトラフィックを除外します。

アウトストリーム広告は、通常、ビデオプレーヤーの通常のビデオ広告ではなく、ポップアップとして、またはコンテンツに詰め込まれた（ネイティブエクスペリエンスの）コンテンツ上に表示されます。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** ターゲットにするトラフィックのタイプ。 次のようなオプションがあります **[!UICONTROL Websites]** および **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** （次の場合に使用可能： **[!UICONTROL Paste list of targeted sites]** 等しい *[!UICONTROL Off]*）ターゲットとするサイトの品質。 Tier 1～3 はすべてブランドセーフであり、DSP マッピングチームによって審査および承認されています。

* *[!UICONTROL Tier 1]:* 全国的に認識できるプレミアムサイトとアプリケーション。

* *[!UICONTROL Tier 2]:* ターゲットは、階層 1 だけでなく、階層 1 よりも広く知られていない高品質のサイトとアプリケーションです。

* *[!UICONTROL Tier 3]:* ターゲット Tier 1～2 に加えて、ニッチなオーディエンスに対応する正当でブランドセーフなサイトとアプリケーション。 リーチまたはデータターゲティング購入には階層 3 を使用します。

* *[!UICONTROL All Sites]:* ターゲット Tier 1～3 およびスクリーニングまたは分類されていない新規在庫で、リーチに使用できます。

>[!NOTE]
>
>在庫は、プレースメント内の広告単位に固有です。

>[!TIP]
>
>パフォーマンスキャンペーンの場合、ベストプラクティスはを選択します。 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** （オプション、次の場合に使用可能： **[!UICONTROL Paste list of targeted sites]** 等しい *[!UICONTROL Off]*）を選択します。選択したサイト階層内のサイト カテゴリをターゲットとして含めるか除外します（両方は除く）。 件名に基づいてDSPがマッピングした垂直方向のサイトリストから選択します。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含めるか除外するサイト カテゴリを指定します。
   * サイト カテゴリを含めるには：
      1. クリック **[!UICONTROL Include categories]**.
      1. ターゲットにする各カテゴリの横にあるチェックボックスをオンにします。
   * サイト カテゴリを除外するには：
      1. クリック **[!UICONTROL Exclude categories]**.
      1. 除外する各カテゴリの横にあるチェックボックスをオンにします。
1. （オプション）ターゲット情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** （オプション、次の場合に使用可能： **[!UICONTROL Paste list of targeted sites]** 等しい *[!UICONTROL Off]*）除外するサイト。 サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. サイトを指定します。
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力するか、サイト層を選択するか、サイト カテゴリを選択します。
      1. 検索結果で、除外するサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （50 を超える結果がある場合）最初の 50 件の結果を除外するには、をクリックします **[!UICONTROL Exclude these 50]**. すべての検索結果を除外するには、 **[!UICONTROL Exclude these \<*NN *\>]**.
   * ドメイン名を入力するには：
      1. クリック **[!UICONTROL Paste]**.
      1. 1 つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Exclude All]**.
1. クリック **[!UICONTROL Done]** あなたが終わったら。

>[!NOTE]
>
>* DSPに加えて、アカウントレベルと広告主レベルのブロックされたサイトリストも適用されます [グローバルにブロックされたサイト リスト](/help/dsp/introduction/features/brand-safety-media-quality.md)（広告に対して安全でないと見なされるサイトが含まれます）。
>* ブロックされたサイト リストは、ターゲットのサイト リストを常に上書きします。 プレースメントに、広告に対して同じターゲットが含まれず、除外される場合、そのターゲットは除外されます。

**[!UICONTROL Language]:** （任意）ターゲットとする単一の言語。

**[!UICONTROL Site List Preview]:** （読み取り専用）プレースメントのすべてのターゲットサイトとブロックサイト。

オプションで、ターゲットサイトとブロックされたサイトのリストをコンマ区切り値（CSV）ファイルとして書き出すことができます。 リストをエクスポートするには、 **[!UICONTROL Export full site list]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

**[!UICONTROL Allow unscreened sites]:** （標準の表示プレースメントのみ）監査されていないサイトでの広告配信を有効にします。 プレースメントがプライベートインベントリをターゲットにする場合、このオプションは、ブロックされたサイトに広告を配信する場合があります。

**[!UICONTROL Paste list of targeted sites]:** 特定のサイトのみをターゲットにすることができます。 このオプションを有効にすると、他のサイトのターゲティングオプションは無効になります。

**[!UICONTROL Sites]:** （次の場合に使用可能： **[!UICONTROL Paste list of targeted sites]** 等しい *[!UICONTROL On]*）ターゲットとするサイト。 サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

1. クリック ![編集](/help/dsp/assets/edit.png).
1. サイトを指定します。
   * サイトを検索するには：
      1. クリック **[!UICONTROL Search]**.
      1. キーワードを入力するか、サイト層を選択するか、サイト カテゴリを選択します。
      1. 検索結果で、含めるサイトを選択します。
         * 個々のサイトを除外するには、そのサイトの横にあるチェックボックスをオンにします。
         * （50 を超える結果がある場合）最初の 50 件の結果を含めるには、 **[!UICONTROL Include these 50]**. すべての検索結果を含めるには、 **[!UICONTROL Include these \<*NN *\>]**.
   * ドメイン名を入力するには：
      1. click **[!UICONTROL Paste]**.
      1. 1 つ以上のドメイン名を別々の行に入力します。
      1. クリック **[!UICONTROL Include All]**.
1. クリック **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** プレースメントに対するすべてのオーディエンスターゲット（以下を含む） [サードパーティセグメント、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存済みオーディエンス](/help/dsp/audiences/audience-settings.md). 選択したすべてのセグメントと保存されたオーディエンスにわたる、重複排除されたアクティブなオーディエンスの合計サイズも表示されます。 既存のオーディエンスを選択し、後で再利用できるオーディエンスを作成するか、特定のオーディエンスセグメントを選択できます。

* 既存のオーディエンスを選択するには、をクリックします。 ![を選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Included Audiences]次に、オーディエンスを選択します。
* オーディエンスを作成するには、をクリックします。 ![を選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Included Audiences]を選択してから、 **[!UICONTROL + Create Audience]**. 手順については、を参照してください [再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md)（手順 3 から開始）。
* 特定のオーディエンスセグメントを選択するには、をクリックします。 **[!UICONTROL Select segments for this placement only]**. セグメントロジックを選択します。手順については、「」の手順 6 を参照してください[再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md).」と入力します。 完了したら、 **保存**.

**[!UICONTROL Excluded Audiences]:** プレースメント用に除外するオーディエンス（ [サードパーティセグメント、ファーストパーティセグメント、Adobeセグメント、カスタムセグメント、保存済みオーディエンス](/help/dsp/audiences/audience-settings.md). 除外されたすべてのオーディエンスの合計およびアクティブな重複排除されたオーディエンスサイズも表示されます。 既存のオーディエンスを選択するか、新しいオーディエンスを作成して後で再利用できます。

* 既存のオーディエンスを選択するには、をクリックします。 ![を選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Excluded Audiences]次に、オーディエンスを選択します。

* オーディエンスを作成するには、をクリックします。 ![を選択](/help/dsp/assets/chevron-down.png) 次の [!UICONTROL Excluded Audiences]を選択してから、 **+ オーディエンスを作成**. 手順については、を参照してください [再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md)（手順 3 から開始）。

* 特定のオーディエンスセグメントを選択するには、をクリックします。 **[!UICONTROL Select segments for this placement only]**. セグメントロジックを選択します。手順については、「」の手順 6 を参照してください[再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md).」と入力します。 完了したら、 **保存**.

**[!UICONTROL Cross Device Targeting]:** （少なくとも 1 つのセグメントまたはオーディエンスと [campaign は、ユーザーベースのクロスデバイスターゲティング用に設定されます](/help/dsp/campaign-management/campaigns/campaign-settings.md). を使用すると、指定されたセグメントに含まれていないデバイスも含め、個人の既知のすべてのデバイス（キャンペーン設定で指定されたデバイスグラフごと）にターゲティングを拡張できます。 キャンペーンに指定されたグラフによって料金が発生する場合があります。 デバイスグラフデータは、北米でのみ使用できます。

**[!UICONTROL Placement Cap]:** （任意）一意のデバイスまたはユーザーの回数（指定された回数による） [!UICONTROL Cross Device Level] キャンペーンの場合）がプレースメントから広告が提供されます。 次のようなオプションがあります *[!UICONTROL Unlimited]* または、1 日、1 週間または 1 か月あたりの特定の金額。

>[!NOTE]
>
> フリークエンシーキャップは、キャンペーン、パッケージ、プレースメントの各レベルで設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。

**[!UICONTROL Secondary Cap]:** （オプション。数値を含める場合に使用可能 [!UICONTROL Placement Cap]）プライマリプレースメントの上限の範囲内での追加の制限。 インプレッション数と期間（12 時間あたり 3 件など）を選択します。

**[!UICONTROL Day Parting]:** （任意）広告を実行できる特定の曜日および時刻。 日分割間隔を指定するには

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 該当するタイムゾーンを選択します。
1. 間隔を指定します。
   * プリセット間隔を選択するには、いずれかの間隔ボタンをクリックします。 オプションは次のとおりです*[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*、または *[!UICONTROL Prime]* （primetime）を指定します。
   * 間隔を手動で選択するには、セル内をクリックし、必要に応じてドラッグして間隔を選択します。
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** （オプション。で設定された広告主が使用できます [!DNL Comscore] および [!DNL Grapeshot] セグメント）から特定のセグメント名または ID [!DNL Comscore] および [!DNL Grapeshot] をターゲットとして含めます。 この機能には追加料金が発生する場合があります。 この機能をアクティブにしてトピックセグメントを設定するには、Adobeアカウントチームにお問い合わせください。

トピックのターゲティングを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. ターゲットにするセグメントを指定します。
   1. 左の列で、「パートナー」（*[!UICONTROL Comscore]* または *[!UICONTROL Grapeshot]*）に設定します。
   1. 入力フィールドに、セグメント名またはセグメント ID を入力します。
1. （オプション）トピック情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

>[!TIP]
>
>* トピックターゲティングは、プレースメントが入札できる在庫を制限するので、全体の購入のごく一部に対してのみトピックターゲティングを使用します。
>
>* 次の場合は、セグメント内でのネガティブターゲティングの設定 [!DNL Comscore] または [!DNL Grapeshot].

**[!UICONTROL Device Targeting]:** （任意）デバイスの種類、製造元、オペレーティングシステム、ブラウザー、接続の種類など、特定のデバイス情報。ターゲットに含めたりターゲットから除外したりできます。 デバイスのターゲティングを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含めるおよび除外するデバイスの詳細を指定します：
   1. 左の列で、カテゴリを選択します。
   1. ターゲティングを指定：
      * 値を含めるには、 **[!UICONTROL Include]** 値の名前の横。
      * 値を除外するには、をクリックします **[!UICONTROL Exclude]** 値の名前の横。
1. （オプション）デバイスのターゲット情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （オプション）ターゲットとして含めるか除外する（ただし両方にしない）特定のインターネットサービスプロバイダー（ISP）。 ISP ターゲティングを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 含める、または除外する ISP を指定してください：
   * ISP を組み込むには：
      1. クリック **[!UICONTROL Include ISPs]**.
      1. （オプション）キーワードでリストをフィルタリングします。
      1. ターゲットにする各 ISP の横にあるチェックボックスをオンにします。
   * ISP を除外するには：
      1. クリック **[!UICONTROL Exclude ISPs]**.
      1. （オプション）キーワードでリストをフィルタリングします。
      1. 除外する各 ISP の横にあるチェックボックスをオンにします。
1. （オプション） ISP のターゲット情報が記載された CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、 **[!UICONTROL Export]**.
1. クリック **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** のタイプ [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39] 適用するコンテキストフィルター。 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上のタイプのインベントリコンテキスト。 追加料金がかかる場合があります。

* [!UICONTROL Peer 39]:

   * **次のようなターゲットサイト：** （オプション）デフォルトでターゲットにする 1 つ以上のタイプの在庫属性。 追加料金がかかる場合があります。

* [!UICONTROL ComScore]:

   * **次のサイトをブロック：** （任意）デフォルトでブロックする 1 つ以上のタイプの在庫属性。 追加料金がかかる場合があります。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （任意）デフォルトで広告をブロックするアダルトコンテンツの程度。 *[!UICONTROL Do Not Block]* （デフォルト）、 *[!UICONTROL Standard]*、または *[!UICONTROL Strict]*. 追加料金がかかる場合があります。

   * **[!UICONTROL Alcohol Content]:** （任意）デフォルトで広告をブロックするアルコール度数。 *[!UICONTROL Do Not Block]* （デフォルト）、 *[!UICONTROL Standard]*、または *[!UICONTROL Strict]*. 追加料金がかかる場合があります。

**[!UICONTROL Pre-bid fraud blocking]:** で測定された不正なトラフィックや疑わしいアクティビティに基づいてブロックするサイトのタイプ [!DNL DoubleVerify], [!DNL Integral Ad Science]、および [!DNL Peer39]. 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しいプレースメントに対して、ハイジャックされたデバイス上のトラフィックを含む 100% 無効なトラフィックをすべてブロックします。 追加料金がかかる場合があります。

   * **[!UICONTROL Also block sites with]:** （任意）DSPがデフォルトで広告をブロックする原因となる、さらに高レベルの不正トラフィックおよび無効なトラフィック。  *[!UICONTROL None]* （デフォルト。追加のトラフィックをブロックしません）、 *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*、または *[!UICONTROL >25% Average Fraud/IVT levels]*. 追加料金がかかる場合があります。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （任意）DSPがデフォルトで広告をブロックする原因となる 1 つ以上の種類の詐欺。 *[!UICONTROL Fraud]* （すべてのサイトを不正でブロックします）、 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、および/または *[!UICONTROL Fraud: Zero Ads]*. 追加料金がかかる場合があります。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （オプション）DSPがデフォルトで広告をブロックする原因となる、疑わしい web サイトまたはアプリアクティビティの一種。 *[!UICONTROL None]* （デフォルト。疑わしいアクティビティに基づく広告をブロックしません）、 *[!UICONTROL Suspicious Activity - High Risk]*、または *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 追加料金がかかる場合があります。

**[!UICONTROL Ads.txt filtering]:**

次のどのレベル [Ads.txt](https://iabtechlab.com/ads-txt-about/) 各パブリッシャーの認証済みデジタルセラーのリストを適用して使用する事前入札フィルタリング。 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。

* *[!UICONTROL Opt out of ads.txt (default)]*：すべてのセラーから在庫を購入する。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：ドメインの承認済みダイレクトセラーおよびリセラーからの購入在庫を優先順位付けする。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済みダイレクトセラーおよびリセラーからのみ在庫を購入できます。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済みダイレクトセラーからのみ在庫を購入する場合。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** （を設定した広告主） [!UICONTROL DoubleVerify Authentic Brand Safety] （オプション）有効 [!DNL DoubleVerify Authentic Brand Safety]：指定したセグメント ID に設定されたカスタムブランドセーフティルールを使用して、入札後のインプレッションをブロックします。 DSPは、広告主設定で指定されたセグメント ID の使用に対してアカウントに請求します。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>（[!DNL Roku] プレースメント）サードパーティのトラッキングベンダーの承認 [!DNL Roku] 次を含める [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]、および [!DNL Research Now].

**[!UICONTROL Event Pixels]:** （任意）サードパーティのイベントトラッキングピクセル。デフォルトでプレースメント内のすべての新規広告に添付されます。 イベントのピクセルを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作をおこないます。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * ピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを識別しやすい名前を使用します。
         * **[!UICONTROL Pixel event fires on]:** 発生するピクセルをトリガーするイベント。 使用できるイベントは、広告タイプによって異なります。
         * **[!UICONTROL Pixel type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、 *[!UICONTROL HTML]*、または *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** ピクセル画像の URL。
      1. クリック **[!UICONTROL Create and attach]**.
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （任意）コンバージョントラッキングピクセル。デフォルトでプレースメント内のすべての新規広告に添付されます。 変換ピクセルを指定するには：

1. クリック ![編集](/help/dsp/assets/edit.png).
1. 次のいずれかの操作をおこないます。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * ピクセルを作成するには：
      1. クリック **[!UICONTROL Create]**.
      1. 次の情報を入力します。
         * **[!UICONTROL Conversion pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを識別しやすい名前を使用します。
         * **[!UICONTROL Conversion category]:** コンバージョンのタイプ。
         * **[!UICONTROL Impression conversion window]:** インプレッションをコンバージョンに関連付けることができる広告インプレッションが発生した後の日数。 デフォルトは 30 日です。
         * **[!UICONTROL Click conversion window]:** クリックをコンバージョンに関連付けることができる広告クリックが発生した後の日数です。 デフォルトは 30 日です。
         * **[!UICONTROL Notes]:** （任意）ピクセルに関する説明またはその他の情報。
      1. クリック **[!UICONTROL Create and attach]**.
      1. 関連する web ページに変換ピクセルを実装します。
         1. メインメニューで、に移動します **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. ピクセル行で、 **[!UICONTROL edit]**.
         1. 値を次にコピー [!UICONTROL HTML Tag] および [!UICONTROL Flash Tag] 必要に応じて、広告主または web サイトの連絡先に提供するフィールド。

            広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。
   1. クリック **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （任意） 1,000 インプレッションあたり請求不可コストとしてトラッキングされる、静的なサードパーティの料金レート。 異なる値を入力しない限り、新しいプレースメントには、該当する場合、パッケージレベルのデフォルトが自動的に適用されます。

>[!NOTE]
>
>請求可能な料金は次に反映されます [!UICONTROL Net CPM] 指標。

>[!MORELIKETHIS]
>
>* [プレースメント管理について](placement-about.md)
>* [プレースメントの作成](placement-create.md)
>* [プレースメントの編集](placement-edit.md)
>* [プレースメントの入札乗数の管理](placement-manage-bid-multipliers.md)
>* [プレースメントの変更ログの表示](placement-change-log.md)
>* [ショートカットキー](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Campaign Managementに関する FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
