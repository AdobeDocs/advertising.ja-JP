---
title: バルクシートを使用した Campaign コンポーネント設定のレビューと編集
description: スプレッドシートを使用して、主要なパッケージ、プレースメント、広告設定を一括でレビューおよび編集する方法を説明します。
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# バルクシートを使用した Campaign コンポーネント設定のレビューと編集

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

1 つのキャンペーンでパッケージ、プレースメント、広告の設定を XLSX （[!DNL Microsoft Excel] スプレッドシート）形式でダウンロードして、レビューできます。 デフォルトでは、ダウンロードしたファイルには、パッケージ設定、パッケージフライト情報、プレースメント設定、プレースメント広告スケジュール用の別々のタブが含まれています。 オプションで、一部のキャンペーンコンポーネントタイプの設定を除外できます。

複数の設定を一度に更新するには、変更を含む有効なバルクシートファイルをアップロードします。 バルクシートを作成するには、キャンペーンコンポーネントのタイプごとにタブが含まれた空のバルクシートテンプレートをダウンロードし、新しい設定または更新された設定をテンプレートファイルに入力または貼り付けてから、ファイルを保存してアップロードします。 編集可能なフィールドには、通常は編集可能なほとんどの設定が含まれています。

>[!NOTE]
>
>特定のパッケージと特定のプレースメントのみの設定をダウンロードして編集することもできます。 「[ バルクシートを使用したパッケージ設定のレビューと編集 ](/help/dsp/campaign-management/packages/package-qa.md)」および「[ バルクシートを使用したプレースメント設定のレビューと編集 ](/help/dsp/campaign-management/placements/placement-qa.md)」を参照してください。

## キャンペーン内のパッケージ、プレースメントおよび広告の設定のダウンロード

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 右上で、**[!UICONTROL ...]**/**[!UICONTROL Download QA sheet]** をクリックします。

1. [!UICONTROL QA Sheet Download] ダイアログボックスで、ダウンロードしたファイルから設定を除外する Campaign コンポーネントの選択を解除し、「**[!UICONTROL Download]**」をクリックします。

デフォルトでは、すべてのキャンペーンコンポーネントの設定が選択されます。

通知メッセージは、ファイルのダウンロードが可能なタイミングを示します。

1. ファイルをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

     ファイルはブラウザーのダウンロードフォルダーに保存されます。 含まれる列のリストについては、[ ダウンロードまたはアップロードされたスプレッドシートのプレースメント列 ](#qa-sheet-columns)」を参照してください。

>[!NOTE]
>
>キャンペーンレベルの QA ファイルを編集して再アップロードすることはできません。 これらのファイルの campaign コンポーネント設定を変更するには、[ 別の設定テンプレートファイル（設定ファイル）をダウンロード ](#download-template) [、QA ファイルの行をテンプレートに入力または貼り付けて保存し、入力されたテンプレートファイルをアップロード ](#upload-bulksheet-campaign-components) します。

## キャンペーン用バルクシートテンプレートのダウンロード {#download-template}

キャンペーンコンポーネントのタイプごとのタブを含んだ空白のバルクシートテンプレートをダウンロードします。 後からテンプレートの任意のタブに行を追加し、[ 編集したファイルをアップロード ](##upload-bulksheet-campaign-components) て、Campaign コンポーネントを変更できます。

1. キャンペーンの名前をクリックします。

1. 右上で、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

1. [!UICONTROL Upload Bulksheet] ダイアログで、「**[!UICONTROL Bulksheet Template].**」をクリックします。

   ファイルはブラウザーのダウンロードフォルダーに保存されます。 含まれる列のリストについては、[ ダウンロードまたはアップロードされたスプレッドシートのプレースメント列 ](#qa-sheet-columns)」を参照してください。

## パッケージ、プレースメント、広告設定を含んだキャンペーン用バルクシートのアップロード{#upload-bulksheet-campaign-components}

1 つのキャンペーンのパッケージ、プレースメントおよび広告の設定を、入力されたバルクシートに一度にアップロードします。

1. [ バルクシートテンプレートをダウンロード ](#download-template) 必要に応じて、バルクシートテンプレートの関連タブでパッケージ、プレースメント、広告設定を入力または貼り付け、デバイスまたはネットワークにファイルを保存します。

   以下の利用可能な設定を参照してください。

1. メインメニューで、「 **[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. 右上の [ **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**] をクリックします。

1. [!UICONTROL Upload Bulksheet]ダイアログで、以下の操作を実行します。

   1. ファイルをボックスにドラッグアンドドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. 「**[!UICONTROL Upload]**」をクリックします。

1. （オプション）更新が処理されたことを確認するには、上部のメニューバーの右側にある ![ ジョブ ](/help/dsp/assets/downloads.png) をクリックします。

## ダウンロード/アップロードしたスプレッドシートのプレースメント設定列{#qa-sheet-columns}

>[!TIP]
>
> ダウンロードしたスプレッドシートでは、編集可能なすべての列が青でハイライト表示されます。

### キャンペーンレベルのスプレッドシート

| セクション | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | プレースメントの数値 ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | プレースメントの名前。 | はい |
| [!UICONTROL Basic] | [!UICONTROL Labels] | レポート用に適用されたラベル。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 配置を編集モードで開くためのリンク。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | プレースメントのステータス：*[!UICONTROL active]* または *[!UICONTROL inactive]*。 | はい |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | プレースメントのタイプ。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 親パッケージの名前（該当する場合）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | プレースメントの開始日。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | プレースメントの終了日。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 日分割が *[!UICONTROL ON]* であるか *[!UICONTROL OFF]* であるかどうか。<br><b> 注：</b> 実際の日分割スケジュールを確認するには、DSPでプレースメント設定を開きます。 | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | プレースメントの予算（存在する場合）。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 予算間隔：&lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*、*[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | パッケージの目的。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目標のターゲット値。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | プレースメントが *[!UICONTROL Budget]* に向かってペーシングされているか、*[!UICONTROL Impressions]* に向かってペーシングされているか。 | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | プレースメントの最大入札額。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | プレースメントのフライトペーシング戦略：*[!UICONTROL Even]*、*[!UICONTROL slightly ahead]*、*[!UICONTROL frontload]*、*[!UICONTROL aggressive frontload]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | プレースメントの日中ペーシング戦略：*[!UICONTROL Even]* または *[!UICONTROL ASAP]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | 適用する入札前フィルター条件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 入札ルール（非推奨）が *[!UICONTROL ON]* か *[!UICONTROL OFF]* か。 | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 指定した [!UICONTROL Frequency Cap Interval] 間のプレースメントの主なフリークエンシーキャップ。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | プライマリ周波数キャップの間隔：*[!UICONTROL Day]*、*[!UICONTROL Week]* または *[!UICONTROL Month]*。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 指定した [!UICONTROL Secondary Frequency Cap Interval] 間のプレースメントの 2 番目の周波数キャップ | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | セカンダリ頻度キャップの間隔のタイプ: *[!UICONTROL Week]*、 *[!UICONTROL Day]*、 *[!UICONTROL Hour]*&#x200B;または *[!UICONTROL Minute]*。 該当する週数、日数、時間数、または分数は、 [!UICONTROL Secondary Frequency Cap Interval Value]で示されます。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]を適用する週数、日数、時間数または分数。例えば、セカンダリキャップが 6 時間あたり 3 インプレッションの場合、この値は `6` になります。 | はい |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | ターゲットとなる地理的な場所、*[!UICONTROL All]* または *[!UICONTROL None]* の数。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | ターゲットとなる地理的な場所（セミコロンまたは *[!UICONTROL All Locations]* で区切る）。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 除外された地理的な場所または *[!UICONTROL None]* の数。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 除外された地理的な場所（セミコロンまたは *[!UICONTROL None]* で区切る）。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | ターゲットの公開在庫取引の数（指定されている場合）、*[!UICONTROL All]* または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 除外された公開在庫取引の数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | ターゲットを絞ったプライベート在庫取引の数(指定されている場合、 *[!UICONTROL All]*&#x200B;数、または *[!UICONTROL None]*&#x200B;数)。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 除外された非公開在庫取引の数 (指定されている場合) または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | ターゲットを絞った [!UICONTROL On-Demand Inventory] 取引の数(指定されている場合、 *[!UICONTROL All]*&#x200B;または *[!UICONTROL None]*)。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 除外されたオンデマンド在庫取引の数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | ターゲットタイプのトラフィック：*[!UICONTROL Website]* または *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | アウトストリームトラフィックを除外する在庫のターゲティングオプションが &lt;i[!UICONTROL >ON]*であるか *[!UICONTROL OFF]* であるかどうか。<br> アウトストリーム広告は、通常、ビデオプレーヤーの通常のビデオ広告ではなく、ポップアップとして、またはコンテンツに詰め込まれた（ネイティブエクスペリエンスの）コンテンツ上に表示されます。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | ターゲットとするサイトの品質：*[!UICONTROL Tier 1]*、*[!UICONTROL Tier 2]*、*[!UICONTROL Tier 3]* または *[!UICONTROL All Sites]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | ターゲット サイト カテゴリの数（指定されている場合）または *[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 除外されたサイト カテゴリの数（指定されている場合）、または *[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 除外されたサイト（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | ターゲットサイトの言語。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （標準の表示配置のみ）監査されていないサイトでの広告配信を許可するかどうか：*[!UICONTROL ON]* または *[!UICONTROL OFF]*。 プレースメントがプライベートインベントリをターゲットにする場合、このオプションは、ブロックされたサイトに広告を配信する場合があります。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | ターゲットサイトの数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | ターゲットオーディエンス（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 除外されたオーディエンス（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | プレースメント（およびキャンペーン内 [!DNL Comscore] 他のプレースメント）に対してデモグラフィックセグメントが有効になっているかどうか（*[!UICONTROL ON]* または *[!UICONTROL OFF]*）。 この機能は、[!DNL Audience Verification] 機能が [!DNL Nielsen] や [!DNL Comscore] に対して有効になっているキャンペーンに対してのみ有効にできます。  追加料金がかかります。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 広告ターゲティングをデバイス（*[!UICONTROL ON]* または *[!UICONTROL OFF]*）間で拡張するかどうか。 クロスデバイスターゲティングは、キャンペーン設定で指定されたデバイスグラフに従って、ユーザーの既知のすべてのデバイスにわたってターゲティングを拡張します。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] – 含まれる# | 指定されている場合は対象のトピック コードの数、または *[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 除外するトピック コードの数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | ターゲットデバイスターゲットの数（指定されている場合）または *[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 除外されたデバイス ターゲットの数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | ターゲットの ISP プロバイダーの数（指定されている場合）または*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 除外された ISP プロバイダーの数（指定されている場合）、または *[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 適用されたブランドセーフティフィルターの数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 適用された事前入札詐欺ブロッキング フィルターの数（指定されている場合）、または *[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 適用された pre-bid viewability フィルターの数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | [ サイトの安全ブロック ] が有効になっているかどうか：*[!UICONTROL ON]* または *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | プレースメントに添付されたサードパーティのイベントトラッキングのピクセル数（*[!UICONTROL None]*）。 | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | プレースメントに関連付けられたコンバージョントラッキングピクセルの数、または *[!UICONTROL None]*。 | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 該当する場合、1,000 インプレッションあたりの請求対象外のコストとして追跡される、静的なサードパーティ手数料率。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 配置に添付されている広告の数(添付されている場合)または *[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | プレースメントに添付された広告の名前、または *[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | DSPで生成される、プレースメントに添付されている広告の一意の広告 ID （セミコロンで区切る）。 [!UICONTROL Ads] ビューから広告名および関連する広告 ID のリストをダウンロードするには、[!UICONTROL Ad ID] の指標を含むカスタムビューを作成してから [ データを書き出し ](/help/dsp/campaign-management/reports/campaign-export-data.md) します。 | はい |

>[!MORELIKETHIS]
>
>* [ バルクシートを使用したパッケージ設定のレビューと編集 ](/help/dsp/campaign-management/packages/package-qa.md)
>* [ バルクシートを使用した配置設定の確認と編集 ](/help/dsp/campaign-management/placements/placement-qa.md)
