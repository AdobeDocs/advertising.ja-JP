---
title: カスタムレポートの管理
description: クロスエクスペリエンス [!UICONTROL Custom Creative Report] ールを生成および管理する方法について説明します。
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

カスタムレポートの作成、複製、編集、実行、ダウンロード、削除を行うことができます。

## カスタムレポートの作成 {#report-create}

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. 右上で、「**[!UICONTROL Create]**」をクリックします。

1. [ レポート設定 ](#report-settings) を指定します。

1. 「**[!UICONTROL Create Custom Report]**」をクリックします。

## カスタムレポートの複製

カスタムレポートを複製して、同様の設定で新しいレポートを作成します。

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. レポート名の横で、**[!UICONTROL ...]**/**[!UICONTROL Copy]** をクリックします。

1. （任意）必要に応じて [ レポート設定 ](#report-settings.md) を編集します。

   レポート名は、デフォルトで「\&lt;*existing report name*\> \#2」（またはシーケンス内の次の番号）になります。

## カスタムレポートの編集 {#report-edit}

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. レポート名の横で、**[!UICONTROL ...]**/**[!UICONTROL Edit]** をクリックします。

1. [ レポート設定 ](#report-settings.md) を編集します。

1. 「**[!UICONTROL Edit Custom Report]**」をクリックします。

## カスタムレポートの実行 {report-run-now}

有効期限が切れていない、または現在実行されていないレポートを実行できます。

>[!NOTE]
>
>また、カスタムレポートは、[ 作成 ](#report-create) または [ 編集 ](#report-edit) するときに実行することもできます。

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. レポート名の横で、**[!UICONTROL ...]**/**[!UICONTROL Run Now]** をクリックします。

   レポートが完了すると、レポート設定で指定した宛先に送信されます。

## カスタムレポートのダウンロード

過去 4 か月間に完了した任意のレポートインスタンスをダウンロードできます。このインスタンスのステータスは「[!UICONTROL Ready to Download]」または「[!UICONTROL Completed]」です。

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. レポート行の [!UICONTROL Download Report] 列で、次の操作を行います。

   * レポートの最新のインスタンスをダウンロードするには、[**[!UICONTROL Download]**] をクリックします。

   * （複数のインスタンスが存在するレポート） ![ の横にある ](/help/dsp/assets/chevron-down.png " 下矢印 ") 下矢印 [!UICONTROL Download] をクリックし、ダウンロードするレポートの完了日をクリックします。 ダウンロード可能なレポートインスタンスには、ダウンロードアイコン（![ダウンロードアイコン](/help/dsp/assets/indicator-downloadable.png "ダウンロードアイコン")）が表示されます。

     使用可能なインスタンスが多数ある場合は、必要に応じてリストの下部にある「**[!UICONTROL Load More]**」をクリックします。

     1 つのレポートを同じ日に複数回実行すると、その日のレポートインスタンスが時系列で表示され、最新のインスタンスが上位に表示されます。

     失敗したレポートジョブにはエラーアイコン（![ エラーインジケーター ](/help/dsp/assets/indicator-critical.png " エラーインジケーター ")）が表示され、ダウンロードできません。 エラーの説明を表示するには、エラーアイコンの上にカーソルを置きます。

## カスタムレポートの削除

1. メインメニューで、**[!UICONTROL Reports]**/**[!UICONTROL Custom Reports]** をクリックします。

1. レポート名の横で、**[!UICONTROL ...]**/**[!UICONTROL Delete]** をクリックします。

1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

## レポート設定 {#report-settings}

**[!UICONTROL Name]:** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]:** レポートのタイプ。

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
  >また、[ ビューから ](#report-run-now) いつでもカスタムレポートを実行 [!UICONTROL Reports] することもできます。

* *[!UICONTROL On]\&lt;Date\>:* アカウントのタイムゾーンで 09:00 までに完了するように、指定された日付にレポートを実行します。

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

**[!UICONTROL Select To Add As Report Headers]:** レポートに含めるデータ列（ヘッダー）。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスをオンにします。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして、順序をカスタマイズできます。

**[!UICONTROL Format]:** レポートを *[!UICONTROL CSV]* （コンマ区切り値）形式または *[!UICONTROL Tab]* （タブ区切り値）形式のどちらで生成するか。

**[!UICONTROL Headers]:** 列ヘッダーを *[!UICONTROL Include]* 示するか *[!UICONTROL Do Not Include]* うかを指定します。

### [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:** 設定はレポートタイプによって異なります。

* **\[Rule Type\]:** （Adobe Advertising コンバージョントラッキングを使用した広告主のみ）レポート内で、コンバージョンにつながる一連のイベントにおけるコンバージョンデータの属性化方法。 ルール間の違いを比較する場合は、複数のルールを選択できます。

  >[!NOTE]
  >
  >コンバージョンパスには、[!DNL Advertising Search, Social, & Commerce] で設定された、広告主のインプレッションまたはクリックのルックバックウィンドウ内のインプレッション数とクリック数が含まれます。 クリック数は、コンバージョンアトリビューション中にインプレッション数より優先されます。 コンバージョンパスでのクリックは、アトリビューションルールに基づいて完全なクレジットを受け取ります。 インプレッションは、コンバージョンパスでクリックが追跡されなかった場合にのみクレジットを受け取ります。

   * *[!UICONTROL Last Event]:* 変換パス内の最後のクリックまたはインプレッションに変換される属性。

   * *[!UICONTROL Weight Last More]:* コンバージョンパス内のすべてのイベントに対するコンバージョンの属性を設定し、最後のイベントに最も重みを与え、後続のイベントに対する重みを少なくします。

   * *[!UICONTROL Even Distribution]:* コンバージョンパス内の各イベントに等しくコンバージョンされる属性。

   * *[!UICONTROL Weight First More]:* コンバージョンパス内のすべてのイベントに対するコンバージョンの属性を設定しますが、最初のイベントに最も重みを与え、後続のイベントに対しては順次少ない重みを与えます。

   * *[!UICONTROL First Event]:* 変換パスの最初のクリックまたはインプレッションに変換される属性。

   * *[!UICONTROL U-shaped]:* コンバージョンパス内のすべてのイベントにコンバージョンの属性を設定しますが、最初と最後のイベントに最も重みを与え、コンバージョンパスの途中のイベントには順次少ない重みを与えます。

   * *[!UICONTROL Display Only]:* コンバージョンパス内の最後のDSPのクリックまたはインプレッションに対する属性の変換。 これには、ビデオ広告や接続されたテレビ広告が含まれ、[!DNL Advertising Search, Social, & Commerce] 広告のクリックは含まれません。

   * *[!UICONTROL Social Only]:* 古い

「[Adobe Advertisingのアトリビューションルールの計算方法 ](/help/search-social-commerce/reports/attribution-rules.md) も参照してください。

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


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [ エクスペリエンスレベルのパフォーマンスレポート ](/help/creative/experiences/experience-performance-details.md)
>* [DSP カスタムレポートについて ](/help/dsp/reports/report-about.md){target="_blank"}
>* [[!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} について
