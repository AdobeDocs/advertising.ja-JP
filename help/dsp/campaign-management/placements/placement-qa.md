---
title: スプレッドシートを使用した配置設定の確認と編集
description: スプレッドシートを使用して主要なプレースメント設定を確認および編集する方法について説明します。
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# スプレッドシートを使用した配置設定の確認と編集

レビュー用に 1 つ以上のプレースメントまたはキャンペーン内のすべてのプレースメントの設定を XLSX （Excel スプレッドシート）形式でダウンロードできます。 この機能を使用すると、次のような詳細をすばやく確認できます。

* キャンペーンのターゲットとなるオーディエンス。
* プレースメントが配信を開始するタイミングと停止するタイミング。
* プレースメントに添付されている広告。

その後、フィールドを選択して変更を加え、それらを一度にDSPにアップロードして戻すことができます。 編集可能なフィールドには、プレースメント名、ステータス、入札、予算、ペーシング戦略、フリークエンシーキャップが含まれます。

>[!TIP]
>
>1 つ以上のプレースメントの複数のフィールドを編集するには、「[ プレースメントの編集 ](/help/dsp/campaign-management/placements/placement-edit.md) を参照してください。

## キャンペーン内のすべてのプレースメントの設定をダウンロード

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * キャンペーン名の横で、**[!UICONTROL ...]**/**[!UICONTROL Download Excel QA sheet]** をクリックします。

   * キャンペーン名をクリックすると、キャンペーンの詳細が表示されます。 右上で、**[!UICONTROL ...]**/**[!UICONTROL Download Excel QA sheet]** をクリックします。

   通知メッセージは、ファイルのダウンロードが可能なタイミングを示します。

1. 次のいずれかの操作をおこないます。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

   ファイルはブラウザーのダウンロードフォルダーに保存されます。 含まれる列のリストについては、[ ダウンロードまたはアップロードされたスプレッドシートの列 ](#qa-sheet-columns)」を参照してください。

## 1 つ以上のプレースメントの設定のダウンロード

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]** をクリックします。

1. 設定をダウンロードする各プレースメントの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Download Edit in Excel Sheet]** をクリックします。

ファイルはブラウザーのダウンロードフォルダーに自動的に保存されます。 含まれる列のリストについては、[ ダウンロードまたはアップロードされたスプレッドシートの列 ](#qa-sheet-columns)」を参照してください。

## キャンペーン内のすべてのプレースメントの設定をアップロード

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * キャンペーン名の横で、**[!UICONTROL ...]**/**[!UICONTROL Upload Excel QA sheet]** をクリックします。

   * キャンペーン名をクリックすると、キャンペーンの詳細が表示されます。 右上で、**[!UICONTROL ...]**/**[!UICONTROL Upload Excel QA sheet]** をクリックします。

1. [!UICONTROL Edit in Excel] ダイアログで、次の手順を実行します。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. 「**[!UICONTROL Upload]**」をクリックします。

1. （オプション）更新が処理されたことを確認するには、上部のメニューバーの右側にある ![ ジョブ ](/help/dsp/assets/downloads.png) をクリックします。

## 1 つ以上のプレースメントの設定のアップロード

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]** をクリックします。

1. 設定をアップロードする各プレースメントの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Upload Edit in Excel Sheet]** をクリックします。

1. [!UICONTROL Edit in Excel] ダイアログで、次の手順を実行します。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

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
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | プレースメントを編集モードで開くためのリンク。 | — |
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
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 2 番目のフリークエンシーキャップの間隔の種類：*[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*、または *[!UICONTROL Minute]*。 該当する週、日、時間、分の数は、[!UICONTROL Secondary Frequency Cap Interval Value] で示されます。 | はい |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap] が適用される週、日、時間または分。 例えば、セカンダリキャップが 6 時間あたり 3 つのインプレッションである場合、この値は `6` になります。 | はい |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | ターゲットとなる地理的な場所、*[!UICONTROL All]* または *[!UICONTROL None]* の数。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | ターゲットとなる地理的な場所（セミコロンまたは *[!UICONTROL All Locations]* で区切る）。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 除外された地理的な場所または *[!UICONTROL None]* の数。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 除外された地理的な場所（セミコロンまたは *[!UICONTROL None]* で区切る）。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | ターゲットの公開在庫取引の数（指定されている場合）、*[!UICONTROL All]* または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 除外された公開在庫取引の数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | ターゲットのプライベート在庫取引の数（指定されている場合）、*[!UICONTROL All]*、または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 除外されたプライベート在庫取引の数（指定されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | ターゲットの [!UICONTROL On-Demand Inventory] 取引の数（指定されている場合）、*[!UICONTROL All]* または *[!UICONTROL None]*。 | — |
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
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 静的なサードパーティの料金レートで、1,000 インプレッション数あたり請求不可コストとしてトラッキングされます（該当する場合）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | プレースメントに添付された広告の数（添付されている場合）または *[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | プレースメントに添付された広告の名前、または *[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | DSPで生成される、プレースメントに添付されている広告の一意の広告 ID （セミコロンで区切る）。 [!UICONTROL Ads] ビューから広告名および関連する広告 ID のリストをダウンロードするには、[!UICONTROL Ad ID] の指標を含むカスタムビューを作成してから [ データを書き出し ](/help/dsp/campaign-management/reports/campaign-export-data.md) します。 | はい |

### プレースメントレベルのスプレッドシート

| 列 | 説明 | 編集可能？ |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | プレースメントの数値 ID。 | — |
| [!UICONTROL Placement Name] | プレースメントの名前。 | はい |
| [!UICONTROL Package Name] | 親パッケージの名前（該当する場合）。 | — |
| [!UICONTROL Start Date] | プレースメントの開始日。 | — |
| [!UICONTROL End Date] | プレースメントの終了日。 | — |
| [!UICONTROL Status] | プレースメントのステータス：*[!UICONTROL active]* または *[!UICONTROL inactive]*。 | — |
| [!UICONTROL Max Bid] | プレースメントの最大入札額。 | はい |
| [!UICONTROL Budget] | プレースメントの予算（存在する場合）。 | はい |
| [!UICONTROL Budget Interval] | 予算間隔：&lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*、*[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Primary Frequency Cap] | 指定した [!UICONTROL Primary Frequency Cap Interval] 間のプレースメントの主なフリークエンシーキャップ。 | はい |
| [!UICONTROL Primary Frequency Cap Interval] | プライマリ周波数キャップの間隔：*[!UICONTROL Day]*、*[!UICONTROL Week]* または *[!UICONTROL Month]*。 | はい |
| [!UICONTROL Secondary Frequency Cap] | 指定した [!UICONTROL Secondary Frequency Cap Interval] 間のプレースメントの 2 番目の周波数キャップ | はい |
| [!UICONTROL Secondary Frequency Cap Interval] | 2 番目のフリークエンシーキャップの間隔の種類：*[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*、または *[!UICONTROL Minute]*。 該当する週、日、時間、分の数は、[!UICONTROL Secondary Frequency Cap Interval Value] で示されます。 | はい |
| [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap] が適用される週、日、時間または分。 例えば、セカンダリキャップが 6 時間あたり 3 つのインプレッションである場合、この値は `6` になります。 | はい |
| [!UICONTROL Attached Ad ID] | DSPで生成される、プレースメントに添付されている広告の一意の広告 ID （セミコロンで区切る）。 [!UICONTROL Ads] ビューから広告名および関連する広告 ID のリストをダウンロードするには、[!UICONTROL Ad ID] の指標を含むカスタムビューを作成してから [ データを書き出し ](/help/dsp/campaign-management/reports/campaign-export-data.md) します。 | はい |

>[!MORELIKETHIS]
>
>* [ プレースメントを編集 ](/help/dsp/campaign-management/placements/placement-edit.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
