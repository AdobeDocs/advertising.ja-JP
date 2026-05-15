---
title: 配置の設定
description: 使用可能なプレースメント設定の説明を参照してください。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
TQID: https://experienceleague.adobe.com/V9gGiuXBnP2TBFUY3ZB7EkZ2TNeBttOgr-qzHUSdMmk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fdc899fcc763a963e5878b2fcf313174b8f5a74b
workflow-type: tm+mt
source-wordcount: 4499
ht-degree: 0%

---

# 配置の設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** プレースメント名。

>[!TIP]
>状況に合った命名規則を使用します。 推奨される命名規則の1つは、「*\&lt; キャンペーン名\>: \&lt;広告ユニット\>: \&lt;期間\>: \&lt; ターゲット\>*」です。

**[!UICONTROL Status]:** プレースメント ステータス：*[!UICONTROL Active]* （既定値）または&#x200B;*[!UICONTROL Paused]*。

>[!TIP]
>ベストプラクティスは、プレースメントを起動する準備が整うまで一時停止することです。

**[!UICONTROL Details]:** （読み取り専用）該当する広告タイプ、プレースメントを作成または作成しているアカウント、および親キャンペーン。 詳細を表示するには、**[!UICONTROL Show more]**&#x200B;をクリックしてください。

**[!UICONTROL Templates]:**&#x200B;既存の配置テンプレートのリストを開きます。 テンプレートからターゲティング設定を自動入力するには：

1. 次のいずれかの操作を行います。

   * テンプレートからすべてのターゲットを再利用するには、テンプレート名の横にあるチェックボックスをオンにします。

   * テンプレートから個々のターゲットタイプを再利用するには、テンプレート名を展開し、再利用するターゲットタイプの横にあるチェックボックスを選択します。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。

**[!UICONTROL Ad specs for forecast]:** （ビデオ広告フォーマットのみ）右側の予測予測の計算に使用される広告期間および/または広告の仕様。 フィールドは広告タイプによって異なります。

**[!UICONTROL Environment]:** （ユニバーサル ビデオ広告フォーマットのみ）プレースメントにターゲットとして含めるデバイス環境（デスクトップ、モバイル、コネクテッド TV）。 少なくとも1つ指定してください。

カスタムレポートでは、プレースメントレベルのディメンション「デバイス環境」がターゲット環境を示します。

**[!UICONTROL Placement tags]:** （オプション）このプレースメントを見つけるのに役立つキーワードまたはニックネーム。

## 目標

**[!UICONTROL Package]:** （オプション）プレースメントが割り当てられているパッケージ。 ![編集](/help/dsp/assets/edit.png)をクリックして、既存のパッケージを選択するか、パッケージを作成します。 プレースメントをパッケージに割り当てると、[!UICONTROL Goals] セクションが更新され、パッケージのフライト日、配達目標、予算が表示されます。

**[!UICONTROL Flight Dates]:** プレースメントの開始日と終了日。 承認された広告は、プレースメントがアクティブで、アクティブなパッケージまたはキャンペーンに割り当てられている場合、フライト中に実行できる資格があります。

パッケージ（該当する場合）またはキャンペーンの日付は、デフォルトで自動入力されます。

>[!NOTE]
>
>* フライト日は、キャンペーンのフライト日とパッケージのフライト日に含める必要があります。

### パッケージレベルのペーシングでパッケージに割り当てられたプレースメント

**[!UICONTROL Placement Funding]:**&#x200B;配置の予算化方法：

* *[!UICONTROL Optimize based on performance]:* パッケージレベルで予算を制御します。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:*&#x200B;最小および/または最大プレースメント予算を設定できます。 少なくとも1つのタイプの予算を指定します。

   * *[!UICONTROL Maximum Budget]*：値と期間（*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*）を入力します。

   * *[!UICONTROL Minimum Budget]*: パッケージ予算に対する最小予算の割合。 間隔キャップを指定すると、最小予算値は常に間隔キャップのパーセンテージとして計算されます。 それ以外は、パッケージ予算に対する割合として計算されます。

**[!UICONTROL Max Bid]:** インプレッション数1000に対する支払い上限です。

**[!UICONTROL Min Bid]:** （プライベートおよび[!DNL On-Demand]件の取引のみ）在庫タイプに基づく最低入札額。 オプションを選択します。

* *[!UICONTROL None]*：どの在庫タイプにも最低入札額はありません。 計算された入札額が対象となる取引の固定価格/最低価格よりも低い場合、DSPは入札しません。 これはスケールに影響を与える可能性があります。

* *[!UICONTROL Fixed/floor price for Private deals only]*: アルゴリズムで計算された入札額が少ない場合でも、DSPは、ターゲットとなるプライベート取引に対して少なくとも固定価格/最低価格を入札します。 これはパフォーマンスに影響を与える可能性があります。

* *[!UICONTROL Fixed/floor price for On-demand deals only]*: アルゴリズムで計算された入札額が少ない場合でも、DSPは、ターゲットとなる[!DNL On-Demand]件の取引に対して少なくとも固定/最低価格を入札します。 これはパフォーマンスに影響を与える可能性があります。

* *[!UICONTROL Fixed/floor price for both Private and On-demand deals]*: アルゴリズムで計算された入札額が少ない場合でも、DSPは、ターゲットとなるプライベートおよび[!DNL On-Demand]件の取引に対して少なくとも固定/床価格を入札します。 これはパフォーマンスに影響を与える可能性があります。

**[!UICONTROL Placement Pre-bid Filters]:**&#x200B;入札を行うには、最大5つのKPIしきい値（最小表示率やクリックスルー率など）を満たす必要があります。 入札前のフィルターを最適化戦術として使用できますが、各ルールによって、このプレースメントで入札できる機会が制限される場合があることを理解してください。 フィルターを追加または編集するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 次のいずれかの操作を行います。
   * フィルターを追加するには：
      1. **[!UICONTROL Add Filter]**&#x200B;をクリックします。
      1. **[!UICONTROL Only bid if]**&#x200B;の横にある指標を選択し、値を入力します。
   * フィルターを削除するには、フィルター行の&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

各入札前フィルターの説明については、「[&#x200B; プレースメントレベルの入札前フィルターとその使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md)」を参照してください。

### その他すべてのプレースメント

**[!UICONTROL Budget Goal]:**&#x200B;総予算上限と予算間隔（*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*）。

**[!UICONTROL Gross Budget Goal]:** （利益管理を含むキャンペーンでのプレースメントのみ）総予算上限と予算間隔（*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*）。

**[!UICONTROL Optimization Goal]:** パッケージの最適化目標。 各最適化目標の説明については、「[最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md)」を参照してください。

**[!UICONTROL Target Goal]:** パフォーマンスの追跡に使用されるターゲット目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、意思決定には使用されません。

**[!UICONTROL Pace on]:** ペーシングの基準：

* **[!UICONTROL Budget goal]:** （デフォルト）このオプションは、割り当てられた予算内で可能な限り多くのインプレッションを提供します。

* **[!UICONTROL Impressions]:**&#x200B;このオプションは、指定した間隔で指定した数量に達するまでインプレッションを配信します。 このオプションを選択する場合、インプレッション数と間隔を指定します：*[!UICONTROL All time]、*、*[!UICONTROL Daily]、*、*[!UICONTROL Monthly]、*、または&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Max Bid]:** インプレッション数1000に対する支払い上限です。

**[!UICONTROL Flight pacing]:** （プレースメントレベルのペーシングを含むプレースメントのみ）広告配信のペースを設定する方法：

* *[!UICONTROL Even]:* （既定値）各フライト全体に配信を均等に配置し、フライトの前半の配信の50%を目標とします。

* *[!UICONTROL Slightly Ahead]:* （既定値）配信を高速化して、フライト期間の途中で55 ～ 65%が完了するようにします。

* *[!UICONTROL Frontload]:*&#x200B;は、フライトの途中で65 ～ 75%が完了するように配信を高速化します。

* *[!UICONTROL Aggressive Frontload]:*&#x200B;は、フライトの途中で75 ～ 85%が完了するように配信を高速化します。

**[!UICONTROL Intraday pacing]:** （プレースメントレベルのペーシング付きのプレースメントのみ）フライト内の各日に広告の配信をペースアップする方法：

* *[!UICONTROL Even]:* （既定値）在庫の空き状況に基づいて配信を拡大します。 一般的に、オークション数が多い日中に1時間あたりの広告が増え、朝や夕方に配信される広告が少なくなります。

* *[!UICONTROL ASAP]:* （既定値）配信を&#x200B;*均等*&#x200B;の2倍の速度に高速化します。

  >[!CAUTION]
  >
  >このオプションはパフォーマンスに悪影響を及ぼす可能性があります。 配信と支出の優先順位がパフォーマンスの最適化よりも高い場合にのみ使用してください。

**[!UICONTROL Placement Pre-bid Filters]:** （オプション）入札を行うには、最大5つのフィルターを満たす必要があります。 入札前のフィルターを最適化戦術として使用できますが、各ルールでは、このプレースメントで入札できる機会が制限される場合があることに注意してください。 フィルターを追加または編集するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 次のいずれかの操作を行います。
   * フィルターを追加するには：
      1. **[!UICONTROL Add Filter]**&#x200B;をクリックします。
      1. **[!UICONTROL Only bid if]**&#x200B;の横にある指標を選択し、値を入力します。
   * フィルターを削除するには、フィルター行の&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （オプション）プレースメントに広告を含める、または除外する特定の場所。 場所を指定しない場合は、すべての場所がターゲットになります。

>[!NOTE]
>
>Roku プレースメントでは、市区町村とDMAの場所は使用できません。

場所を指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 次のいずれかの操作を行います。
   * 国、州、市、DMA、連邦立法地区または州立法地区を含めるまたは除外するには：
      1. 左側の列で場所の種類を選択します。
      1. （必要に応じて）場所をクリックして展開します。
      1. 場所の横にある「*[!UICONTROL Include]*」をクリックしてターゲットとして含めるか、「*[!UICONTROL Exclude]*」をクリックしてターゲットとして除外します。
   * 郵便番号を検索し、選択したすべての結果を含めるまたは除外するには：
      1. **[!UICONTROL Search Postal Code]**&#x200B;をクリックします。
      1. 国を選択します。
      1. 市区町村名を入力し、![編集](/help/dsp/assets/search.png)をクリックします。
      1. 正しい検索結果をクリックします。
      1. すべての場所をターゲットとして含めるには、*[!UICONTROL Include All]*&#x200B;をクリックし、すべての場所をターゲットとして除外するには&#x200B;*[!UICONTROL Exclude All]*&#x200B;をクリックします。
   * 郵便番号を入力またはペーストし、すべての郵便番号を含めるまたは除外するには：
      1. **[!UICONTROL Paste Postal Code]**&#x200B;をクリックします。
      1. 国を選択します。
      1. 1000件までの郵便番号を入力または貼り付けます。
1行につき1つの郵便番号を含めるか、コンマまたはタブで区切った複数の値を入力します。
      1. すべての場所をターゲットとして含めるには、*[!UICONTROL Include All]*&#x200B;をクリックし、すべての場所をターゲットとして除外するには&#x200B;*[!UICONTROL Exclude All]*&#x200B;をクリックします。
   * [!UICONTROL Included]または[!UICONTROL Excluded] リストから場所を削除するには、右側の列の場所の横にある&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。
1. **[!UICONTROL Done]**&#x200B;をクリックします。

>[!NOTE]
>
>* すべての国に州、都市、郵便番号の場所があるわけではありません。
>* DMA （指定マーケットエリア）、連邦立法地区、州立法地区は、米国の地域でのみ利用可能です。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** ターゲットとして含めるか除外するインベントリ ソース。 ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれています。 [!DNL Roku]件のプレースメントの場合は、在庫タイプとソースを指定する必要があります。 次の種類の在庫から選択できます。

* [!UICONTROL Public]: （Rokuを除くすべてのプレースメントタイプ） DSPがアクセスできるオープンなExchange インベントリです。 公開在庫を含めることも除外することもできます。

  ソース別またはフィード別にリストを表示できます。 フィードでリストを表示する場合、フィード名、フィード キー、または選択した特性タグで検索できます。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:DSPで設定したパブリッシャーとの既存のプライベート取引（または[!DNL Roku]件のプレースメントの既存のプライベート [!DNL Roku]件の取引）、および既存の[&#x200B; プライベート取引リスト &#x200B;](/help/dsp/inventory/lists-deals-manage.md)。 公開在庫は含めることができますが、除外することはできません。

  「[!UICONTROL Deals]」タブで、キーワード、キー、取引ID、またはカスタムタグでリストを検索できます。 「[!UICONTROL Deal Lists]」タブで、取引リスト名または取引リスト IDでリストを検索できます。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: [!DNL DSP]で購読したすべての[&#x200B; プレミアム、保証されていない[!UICONTROL On Demand]在庫](/help/dsp/inventory/on-demand-inventory-about.md) （または[!DNL Roku] プレースメントの[!UICONTROL On Demand] [!DNL Roku]件の取引）です。 [!UICONTROL On Demand]在庫を含めることも除外することもできます。

  ソース別またはフィード別にリストを表示できます。 フィード別にリストを表示する場合、フィード名、フィード キー、または選択したパブリッシャー地域、カテゴリタグ、または特性タグで検索できます。

在庫のターゲティングを指定するには：

* 在庫タイプを除外するには、名前の横にあるチェックボックスをオフにします。
* 在庫タイプをターゲットにするには：
   1. 在庫タイプ名の横にあるチェックボックスをオンにします。
   1. （オプション）ソースを次のように変更します。
      1. ![編集](/help/dsp/assets/edit.png)をクリックします。
      1. （[!UICONTROL Public]および[!UICONTROL On Demand] インベントリ）ソースの表示方法を変更するには、**[!UICONTROL View by Source]**&#x200B;または&#x200B;**[!UICONTROL View by Feed]**&#x200B;をクリックします。
      1. （該当する場合）必要に応じて在庫をフィルタリングします。
      1. 含めるソースと除外するソースを指定します。
         * [!UICONTROL Public]または[!UICONTROL On Demand]在庫の場合：
            * ソースを含めるには、ソース名の横にある「**[!UICONTROL Include]**」をクリックします。
            * ソースを除外するには、ソース名の横にある「**[!UICONTROL Exclude]**」をクリックします。
         * [!UICONTROL Private] インベントリの場合：
            * 「[!UICONTROL Deals]」タブ：
               * すべての在庫を取引に含めるには、取引名の横にある&#x200B;**[!UICONTROL Include all]**&#x200B;をクリックします。
               * 個々の在庫ソースを含めるには、取引名を展開し、ソース名の横にあるチェックボックスをクリックします。
            * 「[!UICONTROL Deal Lists]」タブで、取引リスト名の横にあるチェックボックスをクリックします。
   1. （オプション）ターゲティング情報を含むCSV ファイルをブラウザーのダウンロード場所にダウンロードするには、**[!UICONTROL Export]**&#x200B;をクリックします。
   1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!TIP]
>
>[!UICONTROL On Demand]のインベントリを購読したが、ターゲットとするパブリッシャーや取引が見つからない場合は、取引のステータスを確認してください。 ステータスについて詳しくは、[概要 [!DNL On Demand]  プレミアム在庫](/help/dsp/inventory/on-demand-inventory-about.md)を参照してください。

**[!UICONTROL Video targeting]:** インベントリ属性でインベントリをターゲットにする（ただし、除外しない）。 同じビデオ属性に複数の値をターゲットする場合、選択した属性のいずれかをターゲットにすることができます（例：\[Player size = large OR Player size = HD\]）。 複数の属性をターゲットにする場合、指定された各属性が存在する必要があります（例：\[Duration = 30-60 min] AND \[Player size = large OR Player size = HD\]）。

* **[!UICONTROL Player size]:** プレーヤーのサイズ別のターゲット （ただし、除外はしません） インベントリ。 この設定は、プリロールのプレースメント、モバイル標準のプリロールのプレースメント、およびデスクトップ環境とモバイル環境用のユニバーサルビデオのプレースメントに適用されます。 デフォルトでは、すべてのサイズがターゲットになっています。 ターゲットを絞り込むには、特定のターゲットサイズまたは&#x200B;*不明*&#x200B;を選択します。

* **[!UICONTROL Playback mode]:**&#x200B;再生の開始方法によってインベントリをターゲットします（ただし、除外しません）。 この設定は、プリロールのプレースメント、モバイル標準のプリロールのプレースメント、およびデスクトップ環境とモバイル環境用のユニバーサルビデオのプレースメントに適用されます。 デフォルトでは、すべてのモードがターゲットになっています。 ターゲットを絞り込むには、特定のターゲットモードまたは&#x200B;*不明*&#x200B;を選択します。

* **[!UICONTROL Skippability]:** スキップ可能かどうかに応じて、インベントリをターゲットに設定します（ただし、除外しません）。 この設定は、プリロール、モバイル標準プリロール、コネクテッド TV、ユニバーサルビデオプレースメントなど、すべてのVAST/VPAID プレースメントに適用されます。 デフォルトでは、すべてのオプションがターゲットになっています。 ターゲットを絞り込むには、特定のターゲットまたは&#x200B;*不明*&#x200B;を選択します。

**[!UICONTROL Position targeting]:**&#x200B;広告ポジション別の在庫をターゲットにする（ただし除外しない）。 この設定は、プリロール、モバイル標準プリロール、コネクテッド TV、ユニバーサルビデオプレースメントなど、すべてのVAST/VPAID プレースメントに適用されます。 デフォルトでは、すべてのポジションがターゲットになります。 ターゲットを絞り込むには、特定のターゲット位置または&#x200B;*不明*&#x200B;を選択します。

## [!UICONTROL Site or App and Keyword Targeting]

**[!UICONTROL Traffic type]:** ターゲットにするトラフィックの種類。 オプションには&#x200B;**[!UICONTROL Websites]**&#x200B;と&#x200B;**[!UICONTROL Apps]**&#x200B;が含まれます。

**[!UICONTROL Tier]:** （**[!UICONTROL Toggle for Sites or Apps Tiering]**&#x200B;が&#x200B;*[!UICONTROL On]*&#x200B;の場合に使用可能）ターゲットにするトラフィックの品質。 Tier 1～3はすべてブランドセーフであり、DSP マッピングチームによって承認されています。

* *[!UICONTROL Tier 1]:*&#x200B;全国的に認識できるプレミアムサイトとアプリケーション。

* *[!UICONTROL Tier 2]:*&#x200B;は、Tier 1だけでなく、Tier 1よりも広く知られていない質の高いサイトやアプリケーションをターゲットにしています。

* *[!UICONTROL Tier 3]:*&#x200B;は、Tier 1 ～ 2に加えて、ニッチなオーディエンスに対応する合法的でブランドの安全性が高いサイトとアプリケーションをターゲットにしています。 リーチまたはデータターゲティングの購入にTier 3を使用する。

* *[!UICONTROL All Sites or Apps]:*&#x200B;は、スクリーニングまたは分類されていないTier 1 ～ 3と新しいインベントリをターゲットにして、リーチに使用できます。

>[!NOTE]
>
>在庫は、プレースメントの広告ユニットに固有です。

>[!TIP]
>
>パフォーマンスキャンペーンの場合、ベストプラクティスは&#x200B;*[!UICONTROL All Sites]*&#x200B;を選択することです。

**[!UICONTROL Site or App Categories]:** （オプション）選択したトラフィックタイプ内のサイトカテゴリと、ターゲットとして含めるか除外する（ただし両方を含まない）サイト層（指定された場合）をサイト層にします。 DSPが被写体に基づいてマッピングした垂直方向のサイトリストから選択します。

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 含める、または除外するサイト カテゴリを指定します。
   * サイトカテゴリを含めるには：
      1. **[!UICONTROL Include categories]**&#x200B;をクリックします。
      1. ターゲットにする各カテゴリの横にあるチェックボックスをオンにします。
   * サイトカテゴリを除外するには：
      1. **[!UICONTROL Exclude categories]**&#x200B;をクリックします。
      1. 除外する各カテゴリの横にあるチェックボックスをオンにします。
1. （オプション）ターゲティング情報を含むCSV ファイルをブラウザーのダウンロード場所にダウンロードするには、**[!UICONTROL Export]**&#x200B;をクリックします。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

**[!UICONTROL Exclude Sites or Apps]:** （オプション、**[!UICONTROL Toggle for Sites or Apps Tiering]**&#x200B;が&#x200B;*[!UICONTROL On]*&#x200B;の場合に使用可能） サイト/アプリと[URL リスト &#x200B;](/help/dsp/resources/lists-url-manage.md)を除外できます。 「[!UICONTROL Paste URL]」タブでは、サイトを検索して選択したり、ドメイン名を入力または貼り付けたりできます。 「[!UICONTROL URL Lists]」タブから、URL リストを選択できます。

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. サイトを指定します。
   * 「[!UICONTROL Paste URL]」タブから：
      * サイトを検索するには：
         1. **[!UICONTROL Search]**&#x200B;をクリックします。
         1. キーワードを入力し、サイト階層を選択するか、サイト カテゴリを選択します。
         1. 検索結果で、除外するサイトを選択します。
            * 個々のサイトを除外するには、隣接するチェックボックスをオンにします。
            * （50件を超える結果が使用可能な場合）最初の50件の結果を除外するには、**[!UICONTROL Exclude these 50]**&#x200B;をクリックします。 すべての検索結果を除外するには、**[!UICONTROL Exclude these \<*NN *\>]**&#x200B;をクリックします。
      * ドメイン名を入力するには：
         1. **[!UICONTROL Paste]**&#x200B;をクリックします。
         1. 1つ以上のドメイン名を別々の行に入力します。
         1. **[!UICONTROL Exclude All]**&#x200B;をクリックします。
   * 「[!UICONTROL URL Lists]」タブから：
      1. （オプション）検索フィールドにリスト名の全部または一部を入力して、URL リストを検索します。
      1. 除外する各URL リストの横にあるチェックボックスをオンにします。
1. 完了したら、**[!UICONTROL Done]**&#x200B;をクリックします。

>[!NOTE]
>
>* DSP [&#x200B; グローバルにブロックされるサイトリスト &#x200B;](/help/dsp/introduction/features/brand-safety-media-quality.md)に加えて、アカウントレベルと広告主レベルのブロックされたサイトリストも適用されます。このサイトには、広告にとって安全でないと見なされるサイトが含まれます。
>* ブロックされたサイトリストは、常にターゲットサイトとサイトリストを上書きします。 プレースメントの両方が除外され、広告に同じターゲットが含まれる場合、そのターゲットは除外されます。

**[!UICONTROL Context of Sites or App]:** （オプション）ターゲットまたは除外するコンテキスト ターゲット セグメント。 次のLから選択します

* **[!UICONTROL Marketplace]** タブ：指定された料金ですべてのユーザーが利用できる[!DNL Peer39] セグメントを一覧表示します。

* **[!UICONTROL Custom Segments]** タブ：組織の[!DNL Peer39] カスタムセグメントを一覧表示します。

* **[!UICONTROL Paste Segments]** タブ：（組織が[!DNL Comscore]のパートナーシップを持つ広告主。Adobe アカウントチームからアクティベート後に利用可能）組織の[!DNL Comscore] コンテキストのセグメントに1つ以上のセグメント IDまたはセグメント名を入力します。 複数の値をコンマ（Segment1、Segment2、Segment3など）で区切ります。

**[!UICONTROL Language]:** （オプション）ターゲットとなる単一の言語。

**[!UICONTROL Site or app list preview]:** （読み取り専用、および&#x200B;**[!UICONTROL Toggle for Sites or Apps Tiering]**&#x200B;が&#x200B;*[!UICONTROL On]*&#x200B;の場合に使用可能）アカウントレベル、広告主レベル、DSP グローバルブロック済みサイトリストのサイト/アプリを含む、プレースメント用のすべてのターゲティングおよびブロックされたサイト/アプリ。

必要に応じて、ターゲットサイトとブロックされたサイトのリストをコンマ区切り値（CSV）ファイルとして書き出すことができます。 リストをエクスポートするには、**[!UICONTROL Export full site list]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

**[!UICONTROL Allow unscreened sites]:** （標準表示配置のみ）監査を受けていないサイトでの広告配信を有効にします。 プレースメントがプライベート在庫をターゲットにしている場合、このオプションはブロックされたサイトに広告を配信する場合があります。

**[!UICONTROL Toggle for Sites or Apps Tiering]:**&#x200B;を使用すると、ターゲットまたは除外するサイトまたはアプリの階層を指定できます。

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** [&#x200B; サードパーティセグメント、ファーストパーティセグメント、Adobe セグメント、カスタムセグメント、保存済みオーディエンス &#x200B;](/help/dsp/audiences/audience-settings.md)など、プレースメントのオーディエンスターゲティング。 選択したすべてのセグメントおよび保存されたオーディエンスの合計およびアクティブな重複排除オーディエンスサイズも表示されます。 既存のオーディエンスを選択したり、後で再利用できるオーディエンスを作成したり、特定のオーディエンスセグメントを選択したりできます。

* 既存のオーディエンスを選択するには、[!UICONTROL Included Audiences]の横にある![選択](/help/dsp/assets/chevron-down.png)をクリックし、オーディエンスを選択します。
* オーディエンスを作成するには、[!UICONTROL Included Audiences]の横にある![選択](/help/dsp/assets/chevron-down.png)をクリックし、**[!UICONTROL + Create Audience]**&#x200B;を選択します。 手順については、[手順3から始まる再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)を参照してください。
* 特定のオーディエンスセグメントを選択するには、**[!UICONTROL Select segments for this placement only]**&#x200B;をクリックします。 セグメントロジックを選択します。手順については、「[再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md)」の手順6を参照してください。 完了したら、**保存**&#x200B;をクリックします。

>[!NOTE]
>
>アクティブなプレースメント、スケジュールされたプレースメント、または一時停止されたプレースメントにアタッチされていないファーストパーティのRampID セグメントは一時停止されます。 セグメントは、「自動一時停止」としてセグメントリストに表示されます。

**[!UICONTROL Excluded Audiences]:** [&#x200B; サードパーティセグメント、ファーストパーティセグメント、Adobe セグメント、カスタムセグメント、保存済みオーディエンス &#x200B;](/help/dsp/audiences/audience-settings.md)を含む、プレースメントで除外するオーディエンス。 除外されたすべてのオーディエンスの合計およびアクティブな重複排除オーディエンスサイズも表示されます。 既存のオーディエンスを選択するか、後で再利用できる新しいオーディエンスを作成できます。

* 既存のオーディエンスを選択するには、[!UICONTROL Excluded Audiences]の横にある![選択](/help/dsp/assets/chevron-down.png)をクリックし、オーディエンスを選択します。

* オーディエンスを作成するには、[!UICONTROL Excluded Audiences]の横にある![選択](/help/dsp/assets/chevron-down.png)をクリックし、**+ オーディエンスを作成**&#x200B;を選択します。 手順については、[手順3から始まる再利用可能なオーディエンスの作成](/help/dsp/audiences/reusable-audience-create.md)を参照してください。

**[!UICONTROL Targeting]:** ターゲットにするユーザーIDの種類。 プレースメントの公開後（つまり、フライトの開始後）に、この設定を変更することはできません。

レガシーIDとユニバーサル IDの両方を選択すると、入札設定がユニバーサル IDに与えられます。

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: （既定値） Cookie、モバイル広告ID、コネクテッド TV （CTV） IDに基づいてユーザーをターゲティングします。 IDは、ブラウザー、アプリ内、CTVのインベントリにもとづいて選択されます。

* *[!UICONTROL Universal ID Beta]*: ユーザーのプライバシーに焦点を当てたIDをターゲットにします。1つのID タイプを選択してください。 使用可能なオプションは、[!UICONTROL Geo-Targeting] セクションで選択した地理的目標によって決まります。 [[!DNL RampID] 個のセグメントをDSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md)に直接読み込み、DSPがPIIをユニバーサル ID[&#128279;](/help/dsp/audiences/sources/source-about.md)に変換する[個のセグメント、またはユニバーサル ID](/help/dsp/audiences/custom-segment-create.md)をトラッキングする個のカスタムセグメントで使用します。

   * *[!UICONTROL ID5]*: ターゲット [!DNL ID5] IDは、電子メールアドレスおよびその他のシグナルから確率的に作成されました。<!-- What countries/geos are these available for? Everywhere?--> ID5 IDは無料でご利用いただけます。 **注：** [!DNL Eyeota]のサードパーティセグメントには、ID5 IDが含まれる場合があります。

   * *[!UICONTROL RampID]*: メールアドレスを使用してサイトにログインしたユーザーの[!DNL LiveRamp] [!DNL RampIDs]をターゲットにします。<!-- Verify --> [!DNL RampIDs]は、北米、オーストラリア、ニュージーランドのユーザーが利用できます。

   * *[!UICONTROL Unified ID2.0]*：電子メールアドレスを使用してサイトにログインしたユーザーの[!DNL Unified ID2.0] （UID2） IDをターゲットにします。<!-- Verify -->[!DNL UID2 IDs] 欧州経済領域およびその他の一部の国では、ユーザーは利用できません。 [禁止国の一覧](/help/policies/universal-id-policy.md#prohibited-countries-uid2)を参照してください。

  **[!UICONTROL Terms of service]**：ユニバーサル IDを使用するための利用条件。 お客様またはDSP アカウント内の他のユーザーは、データを新しいID タイプに変換する前に、条件に1回同意する必要があります。 マネージドサービス契約を締結しているお客様には、Adobeアカウントチームが同意を得て、組織の代わりに条件に同意します。 条件を読むには、**>**&#x200B;をクリックします。 条件に同意するには、条件の一番下までスクロールして「**[!UICONTROL Accept]**」をクリックします。

**[!UICONTROL Cross Device Targeting]:** （[&#x200B; キャンペーンがピープルベースのクロスデバイスターゲティング用に設定されている場合に使用できます](/help/dsp/campaign-management/campaigns/campaign-settings.md)、レガシーIDのみをターゲットにし（ユニバーサル IDではない）、少なくとも1つのセグメントまたはオーディエンスを選択します。 指定したセグメントに含まれていないデバイスも含め、ユーザーの既知のすべてのデバイス（キャンペーン設定で指定したデバイスグラフごと）にターゲティングを拡張できます。 料金は、キャンペーンに指定されたグラフによって適用される場合があります。 デバイスグラフデータは北米でのみ利用可能です。

**[!UICONTROL Placement Cap]:** （オプション）一意のデバイス、ユニバーサル ID、またはユーザー（キャンペーン用に指定された[!UICONTROL Cross Device Level]とプレースメントの[!UICONTROL Targeting]設定に応じて）がプレースメントから広告を配信できる回数。 オプションには、1日、週、または月あたりの特定の金額&#x200B;*[!UICONTROL Unlimited]*&#x200B;が含まれます。

>[!NOTE]
>
> 広告の表示頻度の上限は、キャンペーン、パッケージ、プレースメントレベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップを尊重しています。

**[!UICONTROL Secondary Cap]:** （オプション。数値[!UICONTROL Placement Cap]が含まれている場合に使用可能）プライマリプレースメントキャップの境界内に追加の制限があります。 インプレッションの数と期間（12時間あたり3時間など）を選択します。

**[!UICONTROL Day Parting]:** （オプション）広告を掲載する曜日と時間帯を指定します。 日分割の間隔を指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 該当するタイムゾーンを選択します。
1. 間隔を指定します。
   * プリセット間隔を選択するには、間隔ボタンのいずれかをクリックします。 オプションには、*[!UICONTROL Weekends]**、*[!UICONTROL Weekdays]*、*[!UICONTROL Morning]*、*[!UICONTROL Lunch]*、*[!UICONTROL Dinner]*&#x200B;または&#x200B;*[!UICONTROL Prime]* （primetime）が含まれます。
   * 間隔を手動で選択するには、セル内をクリックし、オプションでドラッグして間隔を選択します。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

**[!UICONTROL Topic Targeting]:** （オプション、[!DNL Proximic by Comscore] セグメントで構成された広告主が利用できます） [!DNL Proximic by Comscore]の特定のセグメント名またはIDをターゲットとして含めます。 この機能には追加料金が適用される場合があります。 この機能を有効にしてトピックセグメントを設定するには、Adobe アカウントチームにお問い合わせください。

トピックターゲティングを指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. ターゲットにするセグメントを指定します。
   1. 左側の列で、パートナー（*[!UICONTROL Comscore]*）を選択します。
   1. 入力フィールドに、セグメント名またはセグメント IDを入力します。
1. （オプション）トピック情報を含むCSV ファイルをブラウザーのダウンロード場所にダウンロードするには、**[!UICONTROL Export]**&#x200B;をクリックします。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!TIP]
>
>* トピックターゲティングでは、プレースメントの対象となる在庫を制限するため、トピックターゲティングは、購入全体のごく一部に対してのみ使用します。
>
>* [!DNL Proximic by Comscore]のセグメント内で否定的なターゲティングを設定します。

**[!UICONTROL Device Targeting]:** （オプション） デバイスの種類、製造元、オペレーティングシステム、ブラウザー、接続の種類など、ターゲットとして含めたり除外したりするための特定のデバイス情報。 種類は配置タイプによって異なります。 デバイスターゲティングを指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 含めるデバイスの詳細を指定し、除外します。
   1. 左側の列で、カテゴリを選択します。
   1. ターゲティングの指定：
      * 値を含めるには、値の名前の横にある&#x200B;**[!UICONTROL Include]**&#x200B;をクリックします。
      * 値を除外するには、値の名前の横にある&#x200B;**[!UICONTROL Exclude]**&#x200B;をクリックします。
1. （オプション）デバイスのターゲティング情報を含むCSV ファイルをブラウザーのダウンロード場所にダウンロードするには、**[!UICONTROL Export]**&#x200B;をクリックします。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

**[!UICONTROL ISP Targeting]:** （オプション）特定のインターネットサービスプロバイダー（ISP）が、ターゲットとして含めるか除外する（両方を含まない）。 ISP ターゲティングを指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 含めるISPまたは除外するISPを指定します。
   * ISPを含めるには：
      1. **[!UICONTROL Include ISPs]**&#x200B;をクリックします。
      1. （オプション）キーワードでリストをフィルタリングします。
      1. ターゲットにする各ISPの横にあるチェックボックスをオンにします。
   * ISPを除外するには：
      1. **[!UICONTROL Exclude ISPs]**&#x200B;をクリックします。
      1. （オプション）キーワードでリストをフィルタリングします。
      1. 除外する各ISPの横にあるチェックボックスをオンにします。
1. （オプション） ISP ターゲティング情報を含むCSV ファイルをブラウザーのダウンロード場所にダウンロードするには、**[!UICONTROL Export]**&#x200B;をクリックします。
1. **[!UICONTROL Save]**&#x200B;をクリックします。

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** （オプション、[!DNL DoubleVerify]のお客様のみ。デスクトッププレロール、標準およびクリックトゥプレイ表示、ネイティブのディスプレイとビデオの配置でのみ使用できます。[&#x200B; ディールのデフォルトのプログラマティック保証配置](/help/dsp/inventory/programmatic-guaranteed-about.md)ではサポートされていません）組織の[!DNL DoubleVerify] アカウントに関連付けられた[!DNL DoubleVerify Authentic Brand Suitability] セグメント IDは、配置に使用します。 IDを指定すると、指定したセグメント ID用に設定されたカスタムブランド安全ルールを使用して、入札後のインプレッションがブロックされます。 DSPは、セグメント IDの使用状況についてアカウントに請求します。

IDは「51」で始まり、8桁で構成されている必要があります。 デフォルトでは、広告主アカウント設定でセグメント IDが指定されている場合、広告主レベルのIDが入力されますが、IDを変更して別のセグメントを使用したり、IDを削除して機能を無効にしたりできます。

**[!UICONTROL Contextual filtering]:** （デスクトップおよびモバイルのweb ディスプレイ、ネイティブ、ビデオ広告に適用可能） [!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]および[!DNL Peer39]のコンテキストフィルターの種類を適用します。 広告主レベルのデフォルトは、新しいプレースメントに対して選択されますが、設定は次のように変更できます。

<!--
 Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （オプション）既定でブロックする1つ以上の種類のインベントリ コンテキスト。 追加料金が適用される場合があります。

* [!UICONTROL Peer 39]:

   * **デフォルトでターゲットにするインベントリ属性の種類を**&#x200B;個または複数指定するサイトをターゲットにします。 追加料金が適用される場合があります。

* [!UICONTROL ComScore]:

   * **次のサイトをブロック：** （オプション）既定でブロックする1つ以上の種類のインベントリ属性。 追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （オプション）デフォルトで広告をブロックするアダルトコンテンツの程度：*[!UICONTROL Do Not Block]* （デフォルト）、*[!UICONTROL Standard]*、または&#x200B;*[!UICONTROL Strict]*。 追加料金が適用される場合があります。

   * **[!UICONTROL Alcohol Content]:** （オプション）既定で広告をブロックするアルコール コンテンツの程度：*[!UICONTROL Do Not Block]* （既定）、*[!UICONTROL Standard]*、または&#x200B;*[!UICONTROL Strict]*。 追加料金が適用される場合があります。

**[!UICONTROL Pre-bid fraud blocking]:**&#x200B;詐欺トラフィックと[!DNL DoubleVerify]、[!DNL Integral Ad Science]、[!DNL Peer39]を通じて測定された疑わしいアクティビティに基づいて、ブロックするサイトの種類。 広告主レベルのデフォルトは、新しいプレースメントに対して選択されますが、設定は次のように変更できます。

* [!UICONTROL DoubleVerify]: （デスクトップおよびモバイル web ディスプレイ、ネイティブ、ビデオ、および標準のコネクテッド TV広告に適用可能）

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** デフォルトでは、新しいプレースメント用に、ハイジャックされたデバイス上のトラフィックを含む、100%無効なすべてのトラフィックをブロックします。 追加料金が適用される場合があります。

   * **[!UICONTROL Also block sites with]:** （オプション）DSPがデフォルトで広告をブロックする原因となる追加レベルの不正行為および無効なトラフィック：*[!UICONTROL None]* （デフォルトでは、追加のトラフィックがブロックされません）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]*、または&#x200B;*[!UICONTROL >25% Average Fraud/IVT levels]*。 追加料金が適用される場合があります。

* [!UICONTROL Peer 39]: （デスクトップおよびモバイル web ディスプレイ、ネイティブ、ビデオ広告に適用可能）

   * **[!UICONTROL Block sites that are]:** （オプション） DSPがデフォルトで広告をブロックする原因となる1つ以上の種類の不正行為：*[!UICONTROL Fraud]* （不正行為を伴うすべてのサイトをブロック）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;または&#x200B;*[!UICONTROL Fraud: Zero Ads]*。 追加料金が適用される場合があります。

* [!UICONTROL Integral Ad Science]: （デスクトップおよびモバイル web ディスプレイ、ネイティブ、ビデオ広告に適用可能）

   * **[!UICONTROL Block sites that are]:** （オプション）DSPがデフォルトで広告をブロックする不審なweb サイトまたはアプリのアクティビティのタイプ：*[!UICONTROL None]* （デフォルトでは、不審なアクティビティに基づいて広告をブロックしません）、*[!UICONTROL Suspicious Activity - High Risk]*、または&#x200B;*[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 追加料金が適用される場合があります。

**[!UICONTROL Pre-bid viewability]:** （デスクトップおよびモバイルのweb ディスプレイ、ネイティブ、ビデオ広告に適用）入札前にプレースメントを申し込むビューアビリティフィルター：[!DNL DoubleVerify]、および[!DNL Integral Ad Science]。 広告主レベルのデフォルトは、新しいプレースメントに対して選択されますが、設定は変更できます。 追加料金が適用される場合があります。

**[!UICONTROL Ads.txt filtering]:** （デスクトップおよびモバイル web ディスプレイ、ネイティブ、ビデオ、オーディオ広告に適用）各発行者の承認済みデジタル販売者リストを適用して使用する[Ads.txt](https://iabtechlab.com/ads-txt-about/)入札前フィルタリングのレベル。 広告主レベルのデフォルトは、新しいプレースメントに対して選択されますが、設定を変更できます。

* *[!UICONTROL Opt out of ads.txt (default)]*：すべての販売者から在庫を購入します。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: ドメインの承認済みの直接販売者と再販者から購入在庫を優先します。
* *[!UICONTROL Ads.txt sellers only]*: ドメインの承認済みの直接販売者と再販者からのみ在庫を購入する場合。
* *[!UICONTROL Ads.txt sellers only]*: ドメインの承認済みの直接販売者からのみ在庫を購入する場合。

**[!UICONTROL Attention Targeting]:** （デスクトップおよびモバイル web ディスプレイ、ビデオ、標準のコネクテッド TV広告に適用）指定したサイト、形式、広告サイズに基づいて、特定の注意レベル（高、中、低）の[!DNL Adelaide]の入札前セグメントをターゲットにします。 セグメントは毎週更新されます。 **注：** ターゲティングに[!DNL Adelaide] セグメントを使用すると、[!DNL Adelaide]件のアテンションのターゲティングで配信されたインプレッションごとにCPMの料金が発生します。この料金は、[&#x200B; アテンションの測定](/help/dsp/campaign-management/campaigns/campaign-settings.md)の料金とは別です。 インタラクティブなプレロールのプレースメントの場合、膨大なインプレッションに対してのみ課金されます。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>（[!DNL Roku] プレースメント） [!DNL Roku]によって承認されたサードパーティの追跡ベンダーには、[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]、および[!DNL Research Now]が含まれます。

**[!UICONTROL Event Pixels]:** （オプション） プレースメント内のすべての新しい広告にデフォルトで添付するサードパーティのイベントトラッキングピクセル。 イベントピクセルを指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * ピクセルを作成するには：
      1. **[!UICONTROL Create]**&#x200B;をクリックします。
      1. 次の情報を入力します。
         * **[!UICONTROL Pixel name]:** ピクセル名。最大長は500文字です。 ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Pixel event fires on]:** ピクセルをトリガーして起動するイベント。 利用可能なイベントは、広告の種類によって異なります。
         * **[!UICONTROL Pixel type]:** ピクセルが&#x200B;*[!UICONTROL IMG URL]* （1x1 ピクセル画像ファイル）、*[!UICONTROL HTML]*、または&#x200B;*[!UICONTROL JavaScript URL]*&#x200B;のいずれであるか。
         * **[!UICONTROL Pixel URL]:** ピクセル画像のURL。
      1. **[!UICONTROL Create and attach]**&#x200B;をクリックします。
   1. **[!UICONTROL Save]**&#x200B;をクリックします。

**[!UICONTROL Conversion Pixels]:** （オプション） プレースメント内のすべての新しい広告にデフォルトで添付するコンバージョントラッキングピクセル。 コンバージョンピクセルを指定するには：

1. ![編集](/help/dsp/assets/edit.png)をクリックします。
1. 次のいずれかの操作を行います。
   * 既存のピクセルを選択するには、ピクセル行のチェックボックスをオンにします。
   * ピクセルを作成するには：
      1. **[!UICONTROL Create]**&#x200B;をクリックします。
      1. 次の情報を入力します。
         * **[!UICONTROL Conversion pixel name]:** ピクセル名。最大長は500文字です。 ピクセルを簡単に識別できる名前を使用します。
         * **[!UICONTROL Conversion category]:** コンバージョンの種類。
         * **[!UICONTROL Impression conversion window]:**&#x200B;広告インプレッションが発生してから、インプレッションがコンバージョンに起因する可能性がある日数。 デフォルトは30日です。
         * **[!UICONTROL Click conversion window]:**&#x200B;広告のクリックが発生してからクリックするまでの日数。クリックがコンバージョンに起因する可能性があります。 デフォルトは30日です。
         * **[!UICONTROL Notes]:** （オプション） ピクセルに関する説明またはその他の情報。
      1. **[!UICONTROL Create and attach]**&#x200B;をクリックします。
      1. 関連するweb ページにコンバージョンピクセルを実装します。
         1. メインメニューで、**[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**&#x200B;に移動します。
         1. ピクセル行で、**[!UICONTROL edit]**&#x200B;をクリックします。
         1. 必要に応じて、[!UICONTROL HTML Tag]および[!UICONTROL Flash Tag] フィールドの値をコピーして、広告主またはweb サイトの連絡先に提供します。

            広告主のIT部門やその他のグループは、タグのデプロイメントをスケジュールする、または情報を得る必要がある場合があります。
   1. **[!UICONTROL Save]**&#x200B;をクリックします。

**[!UICONTROL 3rd-party Fees]:** （オプション） 1000 インプレッションあたりの請求不可コストとして追跡される、静的なサードパーティ料金率。 パッケージレベルのデフォルトは、別の値を入力しない限り、該当する場合、新しいプレースメントに自動的に適用されます。

>[!NOTE]
>
>請求可能な手数料は、[!UICONTROL Net CPM]指標に反映されます。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのプレースメント管理について](placement-about.md)
>* [&#x200B; プレースメントの作成](placement-create.md)
>* [&#x200B; プレースメントを編集](placement-edit.md)
>* [&#x200B; プレースメントの入札乗数を管理](placement-manage-bid-multipliers.md)
>* [&#x200B; プレースメントの変更ログを表示](placement-change-log.md)
>* [&#x200B; キーボードショートカット &#x200B;](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* キャンペーン管理に関する[FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
