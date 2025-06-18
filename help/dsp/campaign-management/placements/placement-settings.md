---
title: プレースメント設定
description: 使用可能なプレースメント設定の説明を参照してください。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 1478e61ebd7dac59cac7566b86e5b1ea97838508
workflow-type: tm+mt
source-wordcount: '4477'
ht-degree: 0%

---

# プレースメント設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** プレースメント名。

>[!TIP]
>状況に応じて意味のある命名規則を使用します。 推奨される命名規則の 1 つは、「*\&lt; キャンペーン名\>: \&lt; 広告ユニット\>: \&lt; 期間\>: \&lt; ターゲティング\>*」です。

**[!UICONTROL Status]:** プレースメントのステータス：*[!UICONTROL Active]* （デフォルト）または *[!UICONTROL Paused]*。

>[!TIP]
>ベストプラクティスは、ローンチの準備が整うまでプレースメントを一時停止することです。

**[!UICONTROL Details]:** （読み取り専用）該当する広告タイプ、プレースメントを作成または作成したアカウント、親キャンペーン。 詳細を表示するには、[**[!UICONTROL Show more]**] をクリックしてください。

**[!UICONTROL Templates]:** 既存のプレースメントテンプレートのリストを開きます。 テンプレートからターゲティング設定を自動入力するには：

1. 次のいずれかの操作をおこないます。

   * テンプレートからすべてのターゲットを再利用するには、テンプレート名の横にあるチェックボックスを選択します。

   * テンプレートから個々のターゲット・タイプを再利用するには、テンプレート名を展開し、再利用するターゲット・タイプの横にあるチェック・ボックスを選択します。

1. 「**[!UICONTROL Apply]**」をクリックします。

**[!UICONTROL Ad specs for forecast]:** （ビデオ広告フォーマットのみ）広告期間および/または広告仕様。右側の Forecast プロジェクションの計算に使用されます。 フィールドは、広告タイプによって異なります。

**[!UICONTROL Environment]:** （ユニバーサルビデオ広告形式のみ）プレースメントのターゲットとして含めるデバイス環境（デスクトップ、モバイル、接続テレビ）。 1 つ以上を指定してください。

カスタムレポートでは、プレースメントレベルのディメンション「デバイス環境」は、ターゲット環境を示します。

**[!UICONTROL Placement tags]:** （オプション）このプレースメントを見つけるのに役立つキーワードまたはニックネーム。

## 目標

**[!UICONTROL Package]:** （オプション）プレースメントが割り当てられるパッケージ。 ![ 編集 ](/help/dsp/assets/edit.png) をクリックして、既存のパッケージを選択するか、パッケージを作成します。 プレースメントをパッケージに割り当てると、「[!UICONTROL Goals]」セクションがパッケージのフライト日、配信目標、予算で更新されます。

**[!UICONTROL Flight Dates]:** プレースメントの開始日と終了日。 承認済みの広告は、プレースメントがアクティブで、アクティブなパッケージまたはキャンペーンに割り当てられている場合、フライト中に実行できます。

パッケージ（該当する場合）またはキャンペーンの日付は、デフォルトで自動入力されます。

>[!NOTE]
>
>* フライト日は、キャンペーンフライト日とパッケージフライト日の範囲内に含める必要があります。

### パッケージレベルのペーシングを使用してパッケージに割り当てられたプレースメント

**[!UICONTROL Placement Funding]:** プレースメントの予算設定方法：

* *[!UICONTROL Optimize based on performance]:* パッケージレベルで予算を制御します。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* 最小および/または最大のプレースメント予算を設定できます。 予算の種類を少なくとも 1 つ指定してください：

   * *[!UICONTROL Maximum Budget]*：値と期間（*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*）を入力します。

   * *[!UICONTROL Minimum Budget]*：最小予算（パッケージ予算に対する比率）。 インターバル キャップを指定すると、最小の予算値は常にインターバル キャップのパーセンテージとして計算されます。 それ以外の場合は、パッケージ予算のパーセンテージとして計算されます。

**[!UICONTROL Max Bid]:** 1000 件のインプレッションに対して支払う最大値。

**[!UICONTROL Placement Pre-bid Filters]:** 入札を行うために満たす必要がある最大 5 つの KPI しきい値（最小視聴可能指標またはクリックスルー率など）です。 事前入札フィルターは最適化戦術として使用できますが、各ルールによってこのプレースメントが入札できる機会が制限される可能性があることを理解してください。 フィルターを追加または編集するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 次のいずれかの操作をおこないます。
   * フィルターを追加するには：
      1. 「**[!UICONTROL Add Filter]**」をクリックします。
      1. 「**[!UICONTROL Only bid if]**」の横で指標を選択し、値を入力します。
   * フィルターを削除するには、フィルター行の **[!UICONTROL X]** をクリックします。
1. 「**[!UICONTROL Save]**」をクリックします。

「[ プレースメントレベルの Pre-Bid フィルターとその使用方法 ](/help/dsp/optimization/optimization-pre-bid-filters.md)」の各 Pre-bid フィルターの説明を参照してください。

### その他のすべてのプレースメント

**[!UICONTROL Budget Goal]:** 総予算計上上限と予算間隔（*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*）。

**[!UICONTROL Gross Budget Goal]:** （マージン管理を使用したキャンペーンにおけるプレースメントのみ）総予算の上限と予算間隔（*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*）。

**[!UICONTROL Optimization Goal]:** パッケージの最適化目標。 「[ 最適化目標とその使用方法 ](/help/dsp/optimization/optimization-goals.md)」の各最適化目標の説明を参照してください。

**[!UICONTROL Target Goal]:** パフォーマンスの追跡に使用されるターゲット目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、意思決定には使用されません。

**[!UICONTROL Pace on]:** ペーシングの基礎：

* **[!UICONTROL Budget goal]:** （デフォルト）このオプションは、割り当てられた予算内でできるだけ多くのインプレッションを配信します。

* **[!UICONTROL Impressions]:** このオプションは、指定された期間内に指定された数に達するまでインプレッションを配信します。 このオプションを選択した場合は、インプレッション数と間隔を *[!UICONTROL All time]、*、*[!UICONTROL Daily]、*、*[!UICONTROL Monthly]、* または *[!UICONTROL Weekly]* から指定します。

**[!UICONTROL Max Bid]:** 1000 件のインプレッションに対して支払う最大値。

**[!UICONTROL Flight pacing]:** （プレースメントレベルのペーシングのみを使用したプレースメント）広告配信のペーシング方法：

* *[!UICONTROL Even]:* （デフォルト）各飛行の間、均等に配信のペースを調整します。飛行の前半では配信の 50% をターゲットにします。

* *[!UICONTROL Slightly Ahead]:* （デフォルト）配信が加速されるので、フライト期間の半ばで 55～65% 完了します。

* *[!UICONTROL Frontload]:* 配信を高速化して、フライトの半ばで 65～75% 完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を高速化して、飛行の半ばで 75～85% 完了するようにします。

**[!UICONTROL Intraday pacing]:** （プレースメントレベルのペーシングのみを使用したプレースメント）フライト内で毎日広告をペーシングする方法：

* *[!UICONTROL Even]:* （デフォルト）在庫の可用性に基づいて配信のスケールを設定します。 通常、オークションの量が多い昼間は 1 時間あたりにより多くの広告が配信され、朝と夜にはより少ない広告が配信されます。

* *[!UICONTROL ASAP]:* （デフォルト）配信を 2 倍の速度 *偶数* に高速化します。

  >[!CAUTION]
  >
  >このオプションは、パフォーマンスに悪影響を与える可能性があります。 配信の優先順位を完全に設定し、パフォーマンスの最適化よりも費用がかかる場合にのみ使用します。

**[!UICONTROL Placement Pre-bid Filters]:** （オプション）入札が発生するために満たす必要がある最大 5 つのフィルター。 事前入札フィルターは最適化戦術として使用できますが、各ルールによって、このプレースメントが入札できる機会が制限される可能性があることに注意してください。 フィルターを追加または編集するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 次のいずれかの操作をおこないます。
   * フィルターを追加するには：
      1. 「**[!UICONTROL Add Filter]**」をクリックします。
      1. 「**[!UICONTROL Only bid if]**」の横で指標を選択し、値を入力します。
   * フィルターを削除するには、フィルター行の **[!UICONTROL X]** をクリックします。
1. 「**[!UICONTROL Save]**」をクリックします。

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （任意）プレースメントに広告を含めるか除外する特定の場所。 場所を指定しない場合は、すべての場所がターゲットになります。

>[!NOTE]
>
>Roku プレースメントでは、市区町村と DMA の場所は使用できません。

場所を指定するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 次のいずれかの操作をおこないます。
   * 国、都道府県、市区町村、DMA、連邦立法区または州立法区を含めるか除外するには、次の手順を実行します。
      1. 左側の列で場所のタイプを選択します。
      1. （必要に応じて）場所をクリックして展開します。
      1. 場所の横にある「*[!UICONTROL Include]*」をクリックしてターゲットとして含めるか、「*[!UICONTROL Exclude]*」をクリックしてターゲットとして除外します。
   * 郵便番号を検索し、選択したすべての結果を含めるか除外するには：
      1. 「**[!UICONTROL Search Postal Code]**」をクリックします。
      1. 国を選択します。
      1. 都市名を入力し、「![ 編集 ](/help/dsp/assets/search.png)」をクリックします。
      1. 正しい検索結果をクリックします。
      1. 「*[!UICONTROL Include All]*」をクリックして、すべてのロケーションをターゲットとして含めるか、「*[!UICONTROL Exclude All]*」をクリックしてすべてのロケーションをターゲットとして除外します。
   * 郵便番号を入力または貼り付け、すべてを含めるか除外するには、次の手順を実行します。
      1. 「**[!UICONTROL Paste Postal Code]**」をクリックします。
      1. 国を選択します。
      1. 1000 件までの郵便番号を入力または貼り付けます。
1 行に 1 つの郵便番号を含めるか、コンマまたはタブで区切って複数の値を入力します。
      1. 「*[!UICONTROL Include All]*」をクリックして、すべてのロケーションをターゲットとして含めるか、「*[!UICONTROL Exclude All]*」をクリックしてすべてのロケーションをターゲットとして除外します。
   * [!UICONTROL Included] または [!UICONTROL Excluded] のリストから場所を削除するには、右側の列で場所の横にある **[!UICONTROL X]** をクリックします。
1. 「**[!UICONTROL Done]**」をクリックします。

>[!NOTE]
>
>* すべての国に都道府県、市区町村または郵便番号の場所があるわけではありません。
>* DMA （指定市場地域）、連邦立法区、州立法区は、米国の場所でのみ使用できます。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** ターゲットとして含めるか除外する在庫ソース。 ほとんどのプレースメント タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 プレースメント [!DNL Roku] 場合、在庫タイプとソースを指定する必要があります。 次のタイプの在庫から選択できます。

* [!UICONTROL Public]: （Roku を除くすべてのプレースメント タイプ）DSPがアクセスできるすべてのオープンな交換在庫。 公開在庫を含めたり除外したりできます。

  このリストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合は、フィード名、フィードキー、または選択した特性タグで検索できます。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:DSPに設定したパブリッシャーとの既存のプライベート [!DNL Roku] ール（または [!DNL Roku] プレースメントの既存のプライベート取引）および既存の [ プライベート取引リスト ](/help/dsp/inventory/lists-deals-manage.md)。 公開在庫を含めることはできますが、除外することはできません。

  「[!UICONTROL Deals]」タブでは、キーワード、キー、取引 ID、カスタムタグでリストを検索できます。 「[!UICONTROL Deal Lists]」タブから、取引リスト名または取引リスト ID でリストを検索できます。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: （任意）入札価格アルゴリズムを上書きして、少なくとも取引の固定価格とフロア価格を入札します。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]:[!DNL DSP] で購読したすべての [ プレミアム、保証されていない [!UICONTROL On Demand] 在庫 ](/help/dsp/inventory/on-demand-inventory-about.md) （または [!DNL Roku] のプレースメントの [!DNL Roku] い [!UICONTROL On Demand] い取引）。 在庫を含めたり除外 [!UICONTROL On Demand] たりできます。

  このリストは、ソース別またはフィード別に表示できます。 フィード別にリストを表示する場合は、フィード名、フィード キー、または選択した発行元の地域、カテゴリ タグ、特性タグで検索できます。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: （任意）入札価格アルゴリズムを上書きして、少なくとも取引の固定価格とフロア価格を入札します。

在庫ターゲティングを指定する手順は、次のとおりです。

* 在庫タイプを除外するには、名前の横にあるチェック ボックスをオフにします。
* 在庫タイプをターゲットにする手順は、次のとおりです。
   1. 在庫タイプ名の横にあるチェックボックスをオンにします。
   1. （オプション）ソースを次のように変更します。
      1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
      1. （[!UICONTROL Public] および [!UICONTROL On Demand] のインベントリ） **[!UICONTROL View by Source]** または **[!UICONTROL View by Feed]** をクリックして、ソースのリスト方法を変更します。
      1. （該当する場合）必要に応じて在庫をフィルタリングします。
      1. 含めるソースと除外するソースを指定します。
         * [!UICONTROL Public] または [!UICONTROL On Demand] インベントリの場合：
            * ソースを含めるには、ソース名の横にある「**[!UICONTROL Include]**」をクリックします。
            * ソースを除外するには、ソース名の横にある「**[!UICONTROL Exclude]**」をクリックします。
         * 在庫 [!UICONTROL Private] 場合：
            * 「[!UICONTROL Deals]」タブで、次の操作を行います。
               * すべての在庫を取引に含めるには、取引名の横にある「**[!UICONTROL Include all]**」をクリックします。
               * 個別の在庫ソースを含めるには、取引名を展開し、ソース名の横にあるチェックボックスをクリックします。
            * 「[!UICONTROL Deal Lists]」タブで、取引リスト名の横にあるチェックボックスをクリックします。
   1. （オプション）ターゲット情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
   1. 「**[!UICONTROL Save]**」をクリックします。

>[!TIP]
>
>[!UICONTROL On Demand] の在庫を購読しても、ターゲットとするパブリッシャーや取引が見つからない場合は、取引のステータスを確認します。 ステータスについて詳しくは、[About [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md) を参照してください。

**[!UICONTROL Video targeting]:** 在庫属性別のターゲット（除外ではない）在庫。 同じビデオ属性に対して複数の値をターゲットにする場合、選択した属性のいずれかをターゲットにすることができます（例えば、\[ プレーヤーサイズ =大またはプレーヤーサイズ = HD\]）。 複数の属性をターゲットにする場合は、指定した属性がそれぞれ存在している必要があります（例えば、\[ 期間= 30～60 分 ]、\[ プレーヤーサイズ =大またはプレーヤーサイズ = HD\]）。

* **[!UICONTROL Player size]:** プレーヤーサイズ別のターゲット（除外は除かない）インベントリ。 設定は、プレロールプレースメント、モバイル標準のプレロールプレースメント、デスクトップ環境およびモバイル環境用のユニバーサルビデオプレースメントに適用されます。 デフォルトでは、すべてのサイズが対象となります。 ターゲットを絞り込むには、特定のターゲットサイズや *不明* を選択します。

* **[!UICONTROL Playback mode]：再生の開始方法に基づいてターゲットのインベントリを** します（除外はしません）。 設定は、プレロールプレースメント、モバイル標準のプレロールプレースメント、デスクトップ環境およびモバイル環境用のユニバーサルビデオプレースメントに適用されます。 デフォルトでは、すべてのモードがターゲットに設定されます。 ターゲットを絞り込むには、特定のターゲットモードまたは *不明* を選択します。

* **[!UICONTROL Skippability]:** スキップ可能かどうかに応じて、ターゲットの在庫（除外は除きません）。 設定は、プリロール、モバイル標準プリロール、コネクテッド TV、ユニバーサルビデオプレースメントなど、あらゆる VAST/VPAID プレースメントに適用されます。 デフォルトでは、すべてのオプションがターゲットになります。 ターゲットを絞り込むには、特定のターゲットや *不明* を選択します。

**[!UICONTROL Position targeting]:** 広告位置ごとのターゲット（除外ではない）在庫。 設定は、プリロール、モバイル標準プリロール、コネクテッド TV、ユニバーサルビデオプレースメントなど、あらゆる VAST/VPAID プレースメントに適用されます。 デフォルトでは、すべてのポジションがターゲットになります。 ターゲットを絞り込むには、特定のターゲット位置や *不明* を選択します。

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** ターゲットにするトラフィックのタイプ。 オプションには、**[!UICONTROL Websites]** と **[!UICONTROL Apps]** があります。

**[!UICONTROL Tier]:** （**[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]* の場合に使用可能）ターゲットにするトラフィックの品質。 階層 1～3 はすべてブランドセーフであり、DSPマッピングチームによって承認されています。

* *[!UICONTROL Tier 1]:* 全国的に認識できる Premium サイトおよびアプリケーション。

* *[!UICONTROL Tier 2]:* は、Tier 1 をターゲットとし、Tier 1 よりも広く知られていない品質の高いサイトやアプリケーションもターゲットにします。

* *[!UICONTROL Tier 3]:* ターゲット階層 1～2 に加えて、ニッチなオーディエンスに対応する、正当でブランドに安全なサイトとアプリケーション。 リーチまたはデータターゲティング購入には階層 3 を使用します。

* *[!UICONTROL All Sites or Apps]:* ターゲット階層 1～3 およびスクリーニングまたは分類されていない新規在庫で、リーチに使用できます。

>[!NOTE]
>
>在庫は、プレースメント内の広告単位に固有です。

>[!TIP]
>
>パフォーマンスキャンペーンの場合、ベストプラクティスは *[!UICONTROL All Sites]* を選択することです。

**[!UICONTROL Site or App Categories]:** （オプション。**[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]* の場合に使用可能）選択したサイト階層内のサイト カテゴリをターゲットとして含めるか除外（両方ではない）します。 件名に基づいてDSPがマッピングした垂直方向のサイトリストから選択します。

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 含めるか除外するサイト カテゴリを指定します。
   * サイト カテゴリを含めるには：
      1. 「**[!UICONTROL Include categories]**」をクリックします。
      1. ターゲットにする各カテゴリの横にあるチェックボックスをオンにします。
   * サイト カテゴリを除外するには：
      1. 「**[!UICONTROL Exclude categories]**」をクリックします。
      1. 除外する各カテゴリの横にあるチェックボックスをオンにします。
1. （オプション）ターゲット情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. 「**[!UICONTROL Save]**」をクリックします。

**[!UICONTROL Exclude Sites or Apps]:** （オプション。**[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL Off]* の場合に使用可能）除外するサイト/アプリおよび [URL リスト ](/help/dsp/resources/lists-url-manage.md)。 「[!UICONTROL Paste URL]」タブでは、サイトを検索して選択したり、ドメイン名を入力または貼り付けたりできます。 「[!UICONTROL URL Lists]」タブから、URL リストを選択できます。

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. サイトを指定します。
   * 「[!UICONTROL Paste URL]」タブで、次の操作を行います。
      * サイトを検索するには：
         1. 「**[!UICONTROL Search]**」をクリックします。
         1. キーワードを入力するか、サイト層を選択するか、サイト カテゴリを選択します。
         1. 検索結果で、除外するサイトを選択します。
            * 個々のサイトを除外するには、隣のチェックボックスをオンにします。
            * （50 を超える結果がある場合）最初の 50 件の結果を除外するには、「**[!UICONTROL Exclude these 50]**」をクリックします。 すべての検索結果を除外するには、[**[!UICONTROL Exclude these \<*NN *\>]**] をクリックします。
      * ドメイン名を入力するには：
         1. 「**[!UICONTROL Paste]**」をクリックします。
         1. 1 つ以上のドメイン名を別々の行に入力します。
         1. 「**[!UICONTROL Exclude All]**」をクリックします。
   * 「[!UICONTROL URL Lists]」タブで、次の操作を行います。
      1. （オプション）検索フィールドにリスト名の全部または一部を入力して、URL リストを検索します。
      1. 除外する各 URL リストの横にあるチェックボックスをオンにします。
1. 完了したら「**[!UICONTROL Done]**」をクリックします。

>[!NOTE]
>
>* 広告に対して安全でないと見なされるサイトを含むDSP[ グローバルにブロックされたサイトリスト ](/help/dsp/introduction/features/brand-safety-media-quality.md) に加えて、アカウントレベルおよび広告主レベルのブロックされたサイトリストも適用されます。
>* ブロックされたサイト リストは、ターゲットのサイト リストおよびサイト リストを常に上書きします。 プレースメントに、広告に対して同じターゲットが含まれず、除外される場合、そのターゲットは除外されます。

**[!UICONTROL Language]:** （任意）ターゲットとする単一の言語。

**[!UICONTROL Site or app list preview]:** （読み取り専用）アカウントレベル、広告主レベル、DSPのグローバルブロックサイトリストのサイト/アプリを含む、プレースメントのすべてのターゲットサイト/アプリおよびブロックされたサイト/アプリ。

オプションで、ターゲットサイトとブロックされたサイトのリストをコンマ区切り値（CSV）ファイルとして書き出すことができます。 リストをエクスポートするには、[**[!UICONTROL Export full site list]**] をクリックし、ブラウザの通常の手順に従ってファイルを開くか保存します。

**[!UICONTROL Allow unscreened sites]:** （標準の表示配置のみ）監査されていないサイトでの広告配信を有効にします。 プレースメントがプライベートインベントリをターゲットにする場合、このオプションは、ブロックされたサイトに広告を配信する場合があります。

**[!UICONTROL Paste list of targeted sites]:** 特定のサイトのみをターゲットにすることができます。 このオプションを有効にすると、他のサイトのターゲティングオプションは無効になります。

**[!UICONTROL Sites or Apps]:** （**[!UICONTROL Paste list of targeted sites]** が *[!UICONTROL On]* の場合に使用可能）ターゲットにするサイト。 「[!UICONTROL Paste URL]」タブでは、サイトを検索して選択したり、ドメイン名を入力または貼り付けたりできます。 「[!UICONTROL URL Lists]」タブから、URL リストを選択できます。

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. サイトを指定します。
   * 「[!UICONTROL Paste URL]」タブで、次の操作を行います。
      * サイトを検索するには：
         1. 「**[!UICONTROL Search]**」をクリックします。
         1. キーワードを入力するか、サイト層を選択するか、サイト カテゴリを選択します。
         1. 検索結果で、含めるサイトを選択します。
            * 個々のサイトを含めるには、隣のチェックボックスをオンにします。
            * （50 を超える結果がある場合）最初の 50 件の結果を含めるには、「**[!UICONTROL Include these 50]**」をクリックします。 すべての検索結果を含めるには、[**[!UICONTROL Include these \<*NN *\>]**] をクリックします。
      * ドメイン名を入力するには：
         1. 「**[!UICONTROL Paste]**」をクリックします。
         1. 1 つ以上のドメイン名を別々の行に入力します。
         1. 「**[!UICONTROL Include All]**」をクリックします。
   * 「[!UICONTROL URL Lists]」タブで、次の操作を行います。
      1. （オプション）検索フィールドにリスト名の全部または一部を入力して、URL リストを検索します。
      1. 含める各 URL リストの横にあるチェックボックスをオンにします。
1. 完了したら「**[!UICONTROL Done]**」をクリックします。

>[!NOTE]
>
>* 広告に対して安全でないと見なされるサイトを含むDSP[ グローバルにブロックされたサイトリスト ](/help/dsp/introduction/features/brand-safety-media-quality.md) に加えて、アカウントレベルおよび広告主レベルのブロックされたサイトリストも適用されます。
>* ブロックされたサイト リストは、ターゲットのサイト リストおよびサイト リストを常に上書きします。 プレースメントに、広告に対して同じターゲットが除外および含まれる場合、そのターゲットは除外されます。サイトを検索して選択するか、ドメイン名を入力または貼り付けることができます。

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** [ サードパーティセグメント、ファーストパーティセグメント、Adobe セグメント、カスタムセグメント、保存済みオーディエンス ](/help/dsp/audiences/audience-settings.md) など、プレースメントの任意のオーディエンスターゲット。 選択したすべてのセグメントと保存されたオーディエンスにわたる、重複排除されたアクティブなオーディエンスの合計サイズも表示されます。 既存のオーディエンスを選択し、後で再利用できるオーディエンスを作成するか、特定のオーディエンスセグメントを選択できます。

* 既存のオーディエンスを選択するには、「[!UICONTROL Included Audiences]」の横にある ![ 選択 ](/help/dsp/assets/chevron-down.png) をクリックし、オーディエンスを選択します。
* オーディエンスを作成するには、「オーディエンス」の横にある ![ 選択 ](/help/dsp/assets/chevron-down.png) をクリックし、「[!UICONTROL Included Audiences]」を選択し **[!UICONTROL + Create Audience]** す。 手順については、手順 3 から [ 再利用可能なオーディエンスの作成 ](/help/dsp/audiences/reusable-audience-create.md) を参照してください。
* 特定のオーディエンスセグメントを選択するには、「選 **[!UICONTROL Select segments for this placement only]**」をクリックします。 セグメントロジックを選択します。手順については、「[ 再利用可能なオーディエンスの作成 ](/help/dsp/audiences/reusable-audience-create.md) の手順 6 を参照してください。 完了したら、「**保存**」をクリックします。

**[!UICONTROL Excluded Audiences]:** プレースメント用に除外するオーディエンス。例えば、[ サードパーティセグメント、ファーストパーティセグメント、Adobe セグメント、カスタムセグメント、保存済みオーディエンス ](/help/dsp/audiences/audience-settings.md) を含みます。 除外されたすべてのオーディエンスの合計およびアクティブな重複排除されたオーディエンスサイズも表示されます。 既存のオーディエンスを選択するか、新しいオーディエンスを作成して後で再利用できます。

* 既存のオーディエンスを選択するには、「[!UICONTROL Excluded Audiences]」の横にある ![ 選択 ](/help/dsp/assets/chevron-down.png) をクリックし、オーディエンスを選択します。

* オーディエンスを作成するには、「オーディエンス ![ の横にある ](/help/dsp/assets/chevron-down.png) 選択 [!UICONTROL Excluded Audiences] をクリックし、「**+ オーディエンスを作成**」を選択します。 手順については、手順 3 から [ 再利用可能なオーディエンスの作成 ](/help/dsp/audiences/reusable-audience-create.md) を参照してください。

**[!UICONTROL Targeting]:** ターゲットとするユーザー ID のタイプ。 プレースメントがライブになった後（つまり、フライトが開始された後）は、この設定を変更できません。

レガシー ID とユニバーサル ID の両方を選択する場合、入札の環境設定がユニバーサル ID に指定されます。

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*:（デフォルト） Cookie、モバイル広告 ID または接続テレビ（CTV） ID に基づいてユーザーをターゲットに設定します。 ID は、ブラウザー、アプリ内または CTV インベントリに基づいて選択されます。

* *[!UICONTROL Universal ID Beta]*：ユーザープライバシーに焦点を当てた ID をターゲットにします。ID タイプを 1 つ選択します。 使用可能なオプションは、[!UICONTROL Geo-Targeting] のセクションで選択した地理的ターゲットによって決まります。 [[!DNL RampID] DSPに直接読み込まれたセグメント ](/help/dsp/audiences/sources/source-import-liveramp-segments.md)、[DSPが PII をユニバーサル ID に変換するセグメント ](/help/dsp/audiences/sources/source-about.md)、または [ ユニバーサル ID を追跡するカスタムセグメント ](/help/dsp/audiences/custom-segment-create.md) で使用します。

   * *[!UICONTROL ID5]*：メールアドレス [!DNL ID5] その他のシグナルから確率的に作成された ID のターゲット。<!-- What countries/geos are these available for? Everywhere?--> ID5 ID は無料でご利用いただけます。 **メモ：[!DNL Eyeota] のサードパーティセグメントには、ID5 ID が含まれる場合が** ります。

   * *[!UICONTROL RampID]*：メールアドレス [!DNL LiveRamp] 使用してサイトにログインしたユーザーの [!DNL RampIDs] をターゲットに設定します。<!-- Verify --> [!DNL RampIDs] は、北米、オーストラリア、ニュージーランドのユーザーが利用できます。

   * *[!UICONTROL Unified ID2.0]*：メールアドレスを使用してサイトにログインしたユーザーの ID をター [!DNL Unified ID2.0] ット（UID2）でターゲットに設定します。<!-- Verify -->[!DNL UID2 IDs] は、欧州経済地域および一部の国のユーザーは利用できません。 [ 禁止国のリスト ](/help/policies/universal-id-policy.md#prohibited-countries-uid2) をご覧ください。

  **[!UICONTROL Terms of service]**：ユニバーサル ID を使用するためのサービス利用契約の条件。 データを新しい ID タイプに変換するには、DSP アカウントの別のユーザーが条件に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、「**>**」をクリックします。 条件に同意するには、条件の下部までスクロールし、「**[!UICONTROL Accept]**」をクリックします。

**[!UICONTROL Cross Device Targeting]:** （[ キャンペーンが人物ベースのクロスデバイスターゲティングに対して設定されている場合に使用できます ](/help/dsp/campaign-management/campaigns/campaign-settings.md) 従来の ID のみをターゲットにし（ユニバーサル ID は使用できません）、少なくとも 1 つのセグメントまたはオーディエンスを選択します。 を使用すると、指定されたセグメントに含まれていないデバイスも含め、個人の既知のすべてのデバイス（キャンペーン設定で指定されたデバイスグラフごと）にターゲティングを拡張できます。 キャンペーンに指定されたグラフによって料金が発生する場合があります。 デバイスグラフデータは、北米でのみ使用できます。

**[!UICONTROL Placement Cap]:** （任意）一意のデバイス、ユニバーサル ID またはユーザー（キャンペーンに指定された [!UICONTROL Cross Device Level] とプレースメントの [!UICONTROL Targeting] 設定に応じて）がプレースメントから広告を提供できる回数。 オプションには、1 日、1 週間または 1 か月あたりの *[!UICONTROL Unlimited]* 数または特定の金額が含まれます。

>[!NOTE]
>
> フリークエンシーキャップは、キャンペーン、パッケージ、プレースメントの各レベルで設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。

**[!UICONTROL Secondary Cap]:** （オプション。数値 [!UICONTROL Placement Cap] を含める場合に使用可能） プライマリ配置キャップの範囲内での追加の制限。 インプレッション数と期間（12 時間あたり 3 件など）を選択します。

**[!UICONTROL Day Parting]:** （任意）広告を実行できる特定の曜日および時刻。 日分割間隔を指定するには

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 該当するタイムゾーンを選択します。
1. 間隔を指定します。
   * プリセット間隔を選択するには、いずれかの間隔ボタンをクリックします。 オプションには、*[!UICONTROL Weekends]**、*[!UICONTROL Weekdays]*、*[!UICONTROL Morning]*、*[!UICONTROL Lunch]*、*[!UICONTROL Dinner]*、*[!UICONTROL Prime]* （primetime）があります。
   * 間隔を手動で選択するには、セル内をクリックし、必要に応じてドラッグして間隔を選択します。
1. 「**[!UICONTROL Save]**」をクリックします。

**[!UICONTROL Topic Targeting]:** （任意。[!DNL Proximic by Comscore] セグメントで設定された広告主が使用できます） ターゲットとして含める [!DNL Proximic by Comscore] の特定のセグメント名または ID。 この機能には追加料金が発生する場合があります。 この機能をアクティベートしてトピックセグメントを設定するには、Adobe アカウントチームにお問い合わせください。

トピックのターゲティングを指定するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. ターゲットにするセグメントを指定します。
   1. 左の列で、パートナー（*[!UICONTROL Comscore]* を選択します。
   1. 入力フィールドに、セグメント名またはセグメント ID を入力します。
1. （オプション）トピック情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. 「**[!UICONTROL Save]**」をクリックします。

>[!TIP]
>
>* トピックターゲティングは、プレースメントが入札できる在庫を制限するので、全体の購入のごく一部に対してのみトピックターゲティングを使用します。
>
>* [!DNL Proximic by Comscore] のセグメント内で負のターゲティングを設定します。

**[!UICONTROL Device Targeting]:** （任意）デバイスの種類、製造元、オペレーティングシステム、ブラウザー、接続の種類などの特定のデバイス情報。ターゲットとして含めたり除外したりできます。 タイプは、プレースメントのタイプによって異なります。 デバイスのターゲティングを指定するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 含めるおよび除外するデバイスの詳細を指定します：
   1. 左の列で、カテゴリを選択します。
   1. ターゲティングを指定：
      * 値を含めるには、値名の横にある「**[!UICONTROL Include]**」をクリックします。
      * 値を除外するには、値名の横にある「**[!UICONTROL Exclude]**」をクリックします。
1. （オプション）デバイスのターゲット情報を含んだ CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. 「**[!UICONTROL Save]**」をクリックします。

**[!UICONTROL ISP Targeting]:** （任意）ターゲットとして含めるか除外する（ただし両方にしない）特定のインターネットサービスプロバイダー（ISP）。 ISP ターゲティングを指定するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 含める、または除外する ISP を指定してください：
   * ISP を組み込むには：
      1. 「**[!UICONTROL Include ISPs]**」をクリックします。
      1. （オプション）キーワードでリストをフィルタリングします。
      1. ターゲットにする各 ISP の横にあるチェックボックスをオンにします。
   * ISP を除外するには：
      1. 「**[!UICONTROL Exclude ISPs]**」をクリックします。
      1. （オプション）キーワードでリストをフィルタリングします。
      1. 除外する各 ISP の横にあるチェックボックスをオンにします。
1. （オプション） ISP のターゲット情報が記載された CSV ファイルをブラウザーのダウンロード場所にダウンロードするには、「**[!UICONTROL Export]**」をクリックします。
1. 「**[!UICONTROL Save]**」をクリックします。

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** （オプション。[!DNL DoubleVerify] 顧客のみ。デスクトッププリロール、標準およびクリックトゥプレイのディスプレイ、ネイティブのディスプレイおよびビデオのプレースメントでのみ使用できます。[ 契約に対するプログラムによるデフォルトの保証されたプレースメント ](/help/dsp/inventory/programmatic-guaranteed-about.md)）ではサポートされていません。プレースメントに使用する組織の [!DNL DoubleVerify] アカウントに関連付けられた [!DNL DoubleVerify Authentic Brand Safety] セグメント ID。 ID を指定すると、指定したセグメント ID に設定されたカスタムブランドセーフティルールを使用して、入札後のインプレッションがブロックされます。 DSPは、セグメント ID の使用に対してアカウントに請求します。

ID は「51」で始まり、8 桁で構成する必要があります。 デフォルトでは、広告主アカウント設定でセグメント ID が指定されている場合、広告主レベルの ID が入力されますが、別のセグメントを使用するように ID を変更したり、ID を削除して機能を無効にしたりできます。

**[!UICONTROL Contextual filtering]:** （デスクトップおよびモバイル web ディスプレイ、ネイティブおよびビデオ広告に適用）適用する [!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science] および [!DNL Peer39] のコンテキストフィルターのタイプ。 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （オプション）デフォルトでブロックする 1 つ以上のタイプのインベントリコンテキスト。 追加料金がかかる場合があります。

* [!UICONTROL Peer 39]:

   * **ターゲットとなるサイト：** （オプション）デフォルトでターゲットにする 1 つ以上のタイプのインベントリ属性。 追加料金がかかる場合があります。

* [!UICONTROL ComScore]:

   * **次のサイトをブロック：** （オプション）デフォルトでブロックする 1 つ以上のタイプのインベントリ属性。 追加料金がかかる場合があります。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （任意）デフォルトで広告をブロックする成人向けコンテンツの程度です。*[!UICONTROL Do Not Block]* （デフォルト）、*[!UICONTROL Standard]*、*[!UICONTROL Strict]* のいずれかです。 追加料金がかかる場合があります。

   * **[!UICONTROL Alcohol Content]:** （任意）デフォルトで広告をブロックするアルコール度数。*[!UICONTROL Do Not Block]* （デフォルト）、*[!UICONTROL Standard]*、*[!UICONTROL Strict]* のいずれかです。 追加料金がかかる場合があります。

**[!UICONTROL Pre-bid fraud blocking]:** [!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39] を通じて測定された不正なトラフィックや疑わしいアクティビティに基づいてブロックされるサイトのタイプ。 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。

* [!UICONTROL DoubleVerify]: （デスクトップおよびモバイル web ディスプレイ、ネイティブ、ビデオ、標準の接続された TV 広告に適用）

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、は、新しいプレースメントに対して、ハイジャックされたデバイス上のトラフィックを含むすべての 100% 無効なトラフィックをブロックします。 追加料金がかかる場合があります。

   * **[!UICONTROL Also block sites with]:** （任意）DSPがデフォルトで広告をブロックする原因となる、追加の不正トラフィックおよび無効なトラフィックのレベル。*[!UICONTROL None]* （デフォルト。追加のトラフィックをブロックしません）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]* または *[!UICONTROL >25% Average Fraud/IVT levels]* です。 追加料金がかかる場合があります。

* [!UICONTROL Peer 39]: （デスクトップおよびモバイル web ディスプレイ、ネイティブおよびビデオ広告に適用）

   * **[!UICONTROL Block sites that are]:** （任意）DSPがデフォルトで広告をブロックする原因となる 1 つ以上の不正。*[!UICONTROL Fraud]* （不正を行うすべてのサイトをブロックする）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、*[!UICONTROL Fraud: Zero Ads]* のいずれかです。 追加料金がかかる場合があります。

* [!UICONTROL Integral Ad Science]: （デスクトップおよびモバイル web ディスプレイ、ネイティブおよびビデオ広告に適用）

   * **[!UICONTROL Block sites that are]:** （任意）DSPがデフォルトで広告をブロックする原因となる、疑わしい web サイトまたはアプリアクティビティの一種。*[!UICONTROL None]* （デフォルト。疑わしいアクティビティに基づく広告をブロックしません）、*[!UICONTROL Suspicious Activity - High Risk]*、*[!UICONTROL Suspicious Activity - High or Moderate Risk]* のいずれかです。 追加料金がかかる場合があります。

**[!UICONTROL Pre-bid viewability]:** （デスクトップおよびモバイルの web ディスプレイ、ネイティブおよびビデオ広告に適用） [!DNL DoubleVerify] ーザーごとに事前入札ビューアビリティがフィルターされ、プレースメントに適用で [!DNL Integral Ad Science] ます。 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。 追加料金がかかる場合があります。

**[!UICONTROL Ads.txt filtering]:** （デスクトップおよびモバイルの Web ディスプレイ、ネイティブ、ビデオ、オーディオ広告に適用可能）各パブリッシャーの認定デジタルセラーのリストを適用して使用する [Ads.txt](https://iabtechlab.com/ads-txt-about/) 事前入札フィルタリングのレベル。 新しいプレースメントには広告主レベルのデフォルトが選択されますが、設定は変更できます。

* *[!UICONTROL Opt out of ads.txt (default)]*：すべてのセラーから在庫を購入する場合。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：ドメインの承認済み直販業者および再販業者からの購買在庫を優先順位付けする手順です。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済み直販業者および再販業者からのみ在庫を購入する場合。
* *[!UICONTROL Ads.txt sellers only]*：ドメインの承認済ダイレクト・セラーからのみ在庫を購入する場合。

**[!UICONTROL Attention Targeting]:** （デスクトップおよびモバイルの web ディスプレイ、ビデオ、標準で接続されたテレビ広告に適用）指定されたサイト、形式、広告サイズに基づいて、特定の注意レベル（高、中、低）でセグメントの事前入札を [!DNL Adelaide] うターゲット。 セグメントは毎週更新されます。 **注意：**&#x200B;[!DNL Adelaide] セグメントをターゲティングに使用すると、[!DNL Adelaide] のアテンションターゲティングで配信されるインプレッションごとにCPM料金が発生します。この料金は、[ アテンション測定 ](/help/dsp/campaign-management/campaigns/campaign-settings.md) の料金とは別です。 インタラクティブなプレロールプレースメントの場合、膨大なインプレッションに対してのみ請求されます。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>（[!DNL Roku] のプレースメント） [!DNL Roku] によって承認されたサードパーティトラッキングベンダーには、[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk] および [!DNL Research Now] が含まれます。

**[!UICONTROL Event Pixels]:** （任意）プレースメント内のすべての新規広告にデフォルトで添付されるサードパーティイベントトラッキングピクセル。 イベントのピクセルを指定するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 次のいずれかの操作をおこないます。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * ピクセルを作成するには：
      1. 「**[!UICONTROL Create]**」をクリックします。
      1. 次の情報を入力します。
         * **[!UICONTROL Pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを識別しやすい名前を使用します。
         * **[!UICONTROL Pixel event fires on]:** 発生するピクセルをトリガーするイベント。 使用できるイベントは、広告タイプによって異なります。
         * **[!UICONTROL Pixel type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、*[!UICONTROL HTML]*、*[!UICONTROL JavaScript URL]* のどれであるかを示します。
         * **[!UICONTROL Pixel URL]:** ピクセル画像の URL。
      1. 「**[!UICONTROL Create and attach]**」をクリックします。
   1. 「**[!UICONTROL Save]**」をクリックします。

**[!UICONTROL Conversion Pixels]:** （任意）プレースメント内のすべての新規広告にデフォルトで添付されるコンバージョントラッキングピクセル。 変換ピクセルを指定するには：

1. ![ 編集 ](/help/dsp/assets/edit.png) をクリックします。
1. 次のいずれかの操作をおこないます。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * ピクセルを作成するには：
      1. 「**[!UICONTROL Create]**」をクリックします。
      1. 次の情報を入力します。
         * **[!UICONTROL Conversion pixel name]:** ピクセル名。最大長は 500 文字です。 ピクセルを識別しやすい名前を使用します。
         * **[!UICONTROL Conversion category]:** コンバージョンのタイプ。
         * **[!UICONTROL Impression conversion window]:** 広告インプレッションが発生してから、そのインプレッションをコンバージョンに関連付けることができる日数。 デフォルトは 30 日です。
         * **[!UICONTROL Click conversion window]:** クリックをコンバージョンに関連付けることができる広告クリックが発生した後の日数。 デフォルトは 30 日です。
         * **[!UICONTROL Notes]:** （任意）説明またはピクセルに関するその他の情報。
      1. 「**[!UICONTROL Create and attach]**」をクリックします。
      1. 関連する web ページに変換ピクセルを実装します。
         1. メインメニューで、**[!UICONTROL Resources]**/**[!UICONTROL Conversion pixels]** に移動します。
         1. ピクセル行で、「**[!UICONTROL edit]**」をクリックします。
         1. 必要に応じて、「[!UICONTROL HTML Tag]」フィールドと「[!UICONTROL Flash Tag]」フィールドに値をコピーして、広告主または web サイトの連絡先に提供します。

            広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。
   1. 「**[!UICONTROL Save]**」をクリックします。

**[!UICONTROL 3rd-party Fees]:** （任意） 1,000 インプレッションあたりの請求不可コストとして追跡される、静的なサードパーティの料金レート。 異なる値を入力しない限り、新しいプレースメントには、該当する場合、パッケージレベルのデフォルトが自動的に適用されます。

>[!NOTE]
>
>請求可能な料金は、[!UICONTROL Net CPM] の指標に反映されます。

>[!MORELIKETHIS]
>
>* [ プレースメント管理について ](placement-about.md)
>* [ プレースメントの作成 ](placement-create.md)
>* [ プレースメントを編集 ](placement-edit.md)
>* [ プレースメントの入札乗数の管理 ](placement-manage-bid-multipliers.md)
>* [ プレースメントの変更ログを表示 ](placement-change-log.md)
>* [ ショートカットキー ](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Campaign 管理に関する FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
