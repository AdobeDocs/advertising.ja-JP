---
title: '[!UICONTROL Custom Creative Report]'
description: クロスエクスペリエンス [!UICONTROL Custom Creative Report] ークフローを生成する方法を説明します。
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: c5ce127f9a9573962939539c6c449b83715d2e4c
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*クローズドベータ版*

[!UICONTROL Custom Creative Report] を使用すると、すべての広告エクスペリエンスに対するレポートデータのコンテンツと配信をカスタマイズできます。

レポートを 1 回生成することも、指定した基準（15 日ごと、毎月 1 日など）に従って、指定したタイムゾーンで毎日、毎週、毎月 3 時に生成するようにスケジュールすることもできます。 レポートが生成されたら、[!UICONTROL Reports] / [!UICONTROL Custom Reports] または次のタイプのリンクされた [ レポートの宛先 ](/help/dsp/reports/report-destinations/report-destination-about.md) からダウンロードできます。

* [!DNL Amazon Simple Storage Service] （[!DNL S3]）
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

## [!UICONTROL Custom Creative Report] の作成

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. 右上で、「**[!UICONTROL Create]**」をクリックします。

1. [ レポート設定 ](#report-settings) を指定します。

1. 「**[!UICONTROL Create Custom Report]**」をクリックします。

## レポート設定 {#report-settings}

**[!UICONTROL Name]:** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]:** レポートのタイプ：*[!UICONTROL Custom Creative Beta]*。

### [!UICONTROL Report Range] セクション

このセクションは、レポートに含めるデータを決定します。 レポートスケジュールの日付を設定するには、「[!UICONTROL Report run schedule]」の節を参照してください。

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** レポートされた時間に夏時間を考慮します。

**範囲：** データを生成する日付範囲。 使用可能な日数は、レポートや選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Previous Calendar Week]:** 前のカレンダー週のデータが含まれます。

* **[!UICONTROL Previous Calendar Month]:** 前月のデータが含まれます。

* **[!UICONTROL Custom Range]:** 特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートするには、「**[!UICONTROL Present]**」を選択します。

### [!UICONTROL Report Run schedule] セクション

このセクションは、レポートが実行される日付を決定します。 レポートデータを含める日付を設定するには、「[!UICONTROL Report range]」の節を参照してください。

**\[ スケジュール\]:** レポートを生成するタイミング：

* *[!UICONTROL Immediately]*：直ちにレポートをレポートキューに追加します。

  >[!NOTE]
  >
  >また、[!UICONTROL Reports] ビューから [ いつでもカスタムレポートを実行 ](/help/dsp/reports/report-run-now.md) することもできます。

* *[!UICONTROL On]\&lt;Date\>:* 指定した完了日に、アカウントのタイムゾーンで 09:00 までにレポートを実行します。

* *[!UICONTROL Recurring]:* 指定した期間のスケジュールに従ってレポートを実行します。

   * **\[Schedule\]:** レポートの実行頻度：

      * *毎日*:N 日ごとにレポートを実行します。 例えば、レポートを 2 週間（14 日）ごとに実行するには、このオプションを選択して「**14**」と入力します。

      * *毎週*：指定した曜日にレポートを実行します。 たとえば、レポートを毎週月曜日と金曜日に実行する場合は、このオプションを選択し、**月曜日** および **金曜日** の横にあるチェック ボックスをオンにします。

      * *毎月* 1 日から 30 日の特定の数値日にレポートを実行します。 例えば、毎月 1 日にレポートを実行する場合は、このオプションを選択して「**1**」と入力します。

   * **開始日**: レポートを実行できる最初の日付。 指定したスケジュールに応じて、この日付以降に最初のレポートインスタンスが実行される場合があります。

   * **期限**: レポートの有効期限。最大 4 か月先の日付を指定できます。 レポートの有効期限が切れる前に、指定したすべてのメール宛先に、有効期限の 7 日前と 1 日前にメールアラートが届きます。 レポートの期間を延長するには、この日付を変更します。

### [!UICONTROL Apply Filters] セクション

**[!UICONTROL Filter by]:** （オプション）ディメンションがレポートに列として含まれているかどうかに関わらず、データをフィルタリングするための追加のディメンション。 使用可能なフィルターは、レポートタイプによって異なり、*[!UICONTROL Advertiser]*、*[!UICONTROL Experience]*、*[!UICONTROL Creative Library]*、*[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->などがあります。

1 つ以上のフィルターを適用するには、次の手順を実行します。

* ディメンションを選択し、演算子（*次に等しい* または *次に等しくない*）を選択して、該当する値を選択します。 例えば、プリロール広告のみのデータを返すには、「[!UICONTROL Ad Type equals Preroll]」と指定します。
* （任意）フィルターに条件を追加します。
* （任意）さらにフィルターを追加し、各フィルターに 1 つ以上の条件を指定します。

### [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:** レポートに含めるデータ列（ヘッダー）。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスをオンにします。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。 すべてのオプションの説明は、[ 使用可能なレポート列 ](#report-custom-creative-columns)」を参照してください。

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして、順序をカスタマイズできます。

**[!UICONTROL Format]:** レポートを *[!UICONTROL CSV]* （コンマ区切り値）形式または *[!UICONTROL Tab]* （タブ区切り値）形式のどちらで生成するか。

**[!UICONTROL Headers]:** 列ヘッダーを *[!UICONTROL Include]* 示するか *[!UICONTROL Do Not Include]* うかを指定します。

### [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:** 設定はレポートタイプによって異なります。

* **\[Attribution Type\]:** （Adobe Advertisingコンバージョントラッキングを使用する広告主のみ）レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータを属性化する方法を示します。

   * *[!UICONTROL Unique]:* （デフォルト）ディメンション値（デバイスや配置など）が変換されるパス上にあった回数をカウントします。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* コンバージョンへのパス上でのディメンション値（デバイスや配置など）の発生頻度に基づいて、各コンバージョンのクレジットを配分します。 例えば、コンバージョン前に合計 10 件のインプレッションがあり、CTV に 8 件、モバイルに 2 件あった場合、クレジットの 80% （0.8）が CTV 画面に、0.2 がモバイルに与えられます。

* **\[Rule Type\]:** （Adobe Advertisingコンバージョントラッキングを使用した広告主のみ）レポート内で、コンバージョンにつながる一連のイベントにおけるコンバージョンデータの属性化方法。 ルール間の違いを比較する場合は、複数のルールを選択できます。

  >[!NOTE]
  >
  >コンバージョンパスには、[!DNL Advertising Search, Social, & Commerce] で設定された、広告主のインプレッションまたはクリックのルックバックウィンドウ内のインプレッション数とクリック数が含まれます。 クリック数は、コンバージョンアトリビューション中にインプレッション数より優先されます。 コンバージョンパスでのクリックは、アトリビューションルールに基づいて完全なクレジットを受け取ります。 インプレッションは、コンバージョンパスでクリックが追跡されなかった場合にのみクレジットを受け取ります。

   * *[!UICONTROL Last Event]:* 変換パス内の最後のクリックまたはインプレッションに変換される属性。

   * *[!UICONTROL Weight Last More]:* コンバージョンパス内のすべてのイベントに対するコンバージョンの属性を設定し、最後のイベントに最も重みを与え、後続のイベントに対する重みを少なくします。

   * *[!UICONTROL Even Distribution]:* コンバージョンパス内の各イベントに等しくコンバージョンされる属性。

   * *[!UICONTROL Weight First More]:* コンバージョンパス内のすべてのイベントに対するコンバージョンの属性を設定しますが、最初のイベントに最も重みを与え、後続のイベントに対しては順次少ない重みを与えます。

   * *[!UICONTROL First Event]:* 変換パスの最初のクリックまたはインプレッションに変換される属性。

   * *[!UICONTROL U-shaped]:* コンバージョンパス内のすべてのイベントにコンバージョンの属性を設定しますが、最初と最後のイベントに最も重みを与え、コンバージョンパスの途中のイベントには順次少ない重みを与えます。

   * *[!UICONTROL Display Only]:* コンバージョンパス内の最後のDSP クリックまたはインプレッションに対する属性のコンバージョン。 これには、ビデオ広告や接続されたテレビ広告が含まれ、[!DNL Advertising Search, Social, & Commerce] 広告のクリックは含まれません。

   * *[!UICONTROL Social Only]:* 古い

「[Adobe Advertisingに関するアトリビューションルールの計算方法 ](/help/search-social-commerce/reports/attribution-rules.md)」も参照してください。

**[!UICONTROL Paths as Columns]:** 同じデバイスで以前のイベントが発生した場合にレポートするコンバージョンのタイプ。 最大 3 つのタイプを含めることができます。 選択したタイプごとに、コンバージョン指標ごとに個別の列が含まれ、指定したサフィックス（[!UICONTROL (tl)]、[!UICONTROL (ct)] または [!UICONTROL (vt)]）が追加されます。

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーの CT）およびインプレッション数（ビュースルーの VT）に起因するコンバージョンを含みます。 インプレッション数に起因するコンバージョンは、指定されたビュースルーの重み付けで乗算されます。 デフォルトのビュースルーの重み付けは 100% です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の 100% としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリック数に起因するコンバージョンのみを含みます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったことが原因で、インプレッション数に起因するコンバージョンのみが含まれます。

### [!UICONTROL Add Report Destinations] セクション

**[!UICONTROL Destination Type]:** 完了したレポートとエラー通知の配信先。 レポートを保存した後は、宛先のタイプを変更できません。

>[!NOTE]
>
>完了したレポートは、[!UICONTROL Reports] / [!UICONTROL Custom Reports] ビューからいつでもダウンロードできます。

* *[!UICONTROL None]:* レポートまたは通知を配信しない。

* *[!UICONTROL S3]:* 完成したレポートを 1 つ以上の [!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]）の場所に送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL sFTP]:* 完成したレポートを 1 つ以上の SFTP ロケーションに送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL FTP]:* 完成したレポートを 1 つ以上の FTP ロケーションに送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL FTP SSL]（現在はBetaにあります）:* 完成したレポートを 1 つ以上の FTP SSL ロケーションに送信するには、「**[!UICONTROL Destination Name]**」フィールドを選択する必要があります。

* *[!UICONTROL Email]:* 完了したレポートまたはエラーが原因でレポートがキャンセルされた場合に通知を送信する電子メール アドレスを指定します。

**[!UICONTROL Email]:** （電子メールの宛先タイプのみ）各アドレスに対して、アドレスを入力し、**+** をクリックします。

**[!UICONTROL Destination Name]:** （S3、FTP、sFTP および FTP SSL 宛先タイプのみ）カスタムレポートの送信先 [ レポート宛先 ](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. **新しい宛先を追加** をクリックします。

   1. [ レポート宛先設定 ](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} を入力し、「**保存**」をクリックします。

   1. レポート設定に戻り、「**宛先名を更新**」をクリックします。

      これで、既存の宛先のリストから新しい宛先を使用できるようになり、オプションでレポートに追加できます。

## 使用可能なレポート列 {#report-custom-creative-columns}

<!-- Need to finish these definitions -->

| 指標タイプ | サブタイプ | 列名 | 説明 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | 公開済み広告のディメンション。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | 提供された広告がエクスペリエンスのデフォルトの画像広告だったかどうか。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | 広告が相対的な重み付けに従って回転されたか（*重み付け*）アルゴリズム的に回転されたか（*アルゴリズム*）。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | クリエイティブ [!UICONTROL Creative] 割り当てられた ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | クリエイティブの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | クリエイティブのタイプ（[!UICONTROL HTML5] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | 親クリエイティブ [!UICONTROL Creative] 割り当てられた ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | 親クリエイティブの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | 親クリエイティブのタイプ（[!UICONTROL HTML5] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | 。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | クリックタイプ。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | 広告が表示されたブラウザー（[!UICONTROL Chrome] や [!UICONTROL Firefox] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | 広告が表示されたオペレーティングシステム（[!UICONTROL Windows] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | 広告が表示されたデバイスのタイプ（[!UICONTROL Desktop] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Ad ID] | 広告の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Creative ID] | クリエイティブの ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | 広告が実行されたプレースメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Buy ID] | 広告プレースメントの購入 ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP ID] | 広告が実行されたDSPの ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | 広告が実行されたDSPの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | 広告が実行されたサイトの ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | 広告が実行されたサイトの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | 広告が実行されたプレースメントの ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | 広告が実行されたプレースメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | 広告主の名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | エクスペリエンス [!UICONTROL Creative] 割り当てられた ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | エクスペリエンスの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | ターゲット。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | イベントの日時。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | 広告エクスペリエンスタグ [!UICONTROL Creative] 割り当てられた ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | レポートされたデータが関連付けられている市区町村。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | レポートされたデータが関連付けられる国の国コード。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | レポートされたデータの帰属先となる指定マーケットエリア（DMA）。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | レポートされたデータの帰属先の州の州コード。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | レポートされたデータの帰属先の郵便番号。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | （動的広告）ターゲット製品カテゴリ ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | （動的広告）ターゲットの製品カテゴリ名。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | （動的広告）ターゲット製品 ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | （動的広告）ターゲットの製品名。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | （動的広告）最初のクリエイティブ属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | （動的広告） 2 つ目のクリエイティブ属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | （動的広告） 3 つ目のクリエイティブ属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | （動的広告） 4 つ目のクリエイティブ属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | （ダイナミック広告） 5 番目のクリエイティブ属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | レポートされたデータの帰属先となるオーディエンスセグメントのセグメント ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | レポートされたデータの帰属先となるオーディエンスセグメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | レポートされたデータの帰属先となるオーディエンスセグメントの属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | レポートされたデータの帰属先オーディエンスセグメントの ID。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | 広告のすべてのクリックの合計。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | クリックスルー率（クリックの割合を広告インプレッション数で割った値）。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 提供された広告でのインタラクションの数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | ユーザーエンゲージメントにつながった、インプレッション数の割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 広告インプレッションの合計数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | 製品の広告におけるすべてのコンバージョンの合計。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | コンバージョンにつながった商品の広告上のの割合。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | 製品の広告のすべてのクリックの合計。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | 製品の広告のクリックスルー率（クリックの割合を広告インプレッション数で割った値）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | 商品のインプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | 製品で提供された広告の合計売上高。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | 提供済み広告の合計売上高。 |
| [!UICONTROL Conversion Metrics] | [ レポート設定で広告主別にグループ化 ] | [ 広告主固有のコンバージョン ] | 指定した広告主固有のコンバージョン指標またはAdobe Analytics イベントの合計。 |
| [!UICONTROL Custom Goals] | [ レポート設定で広告主別にグループ化 ] | [ 広告主固有のカスタム目標 ] | 指定した [ カスタム目標 ](/help/dsp/optimization/custom-goal.md) に含まれるすべてのコンバージョンの重み付き合計。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [ エクスペリエンスレベルのパフォーマンスレポート ](/help/creative/experiences/experience-performance-details.md)
