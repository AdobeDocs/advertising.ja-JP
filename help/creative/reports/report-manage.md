---
title: カスタムレポートの管理
description: クロスエクスペリエンス [!UICONTROL Custom Creative Report]を生成および管理する方法について説明します。
feature: Creative Reporting
exl-id: fecdfc82-1260-46e4-82f3-c37fad6d77e4
TQID: https://experienceleague.adobe.com/w746p31oJoThLGvkaVKBEK00dUho0zSBZtVv8yfkmUo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1485
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

カスタムレポートを作成、複製、編集、実行、ダウンロード、削除できます。

## カスタムレポートの作成 {#report-create}

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**&#x200B;をクリックします。

1. 右上の「**[!UICONTROL Create]**」をクリックします。

1. [&#x200B; レポート設定](#report-settings)を指定します。

1. **[!UICONTROL Create Custom Report]**&#x200B;をクリックします。

## カスタムレポートの複製

カスタムレポートを複製して、同様の設定を持つ新しいレポートを作成します。

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**&#x200B;をクリックします。

1. レポート名の横で、**[!UICONTROL ...]** > **[!UICONTROL Copy]**&#x200B;をクリックします。

1. （オプション）必要に応じて[&#x200B; レポート設定](#report-settings.md)を編集します。

   デフォルトでは、レポート名は「\&lt;*既存のレポート名*\> \#2」（またはシーケンス内の次の番号）です。

## カスタムレポートの編集 {#report-edit}

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**&#x200B;をクリックします。

1. レポート名の横で、**[!UICONTROL ...]** > **[!UICONTROL Edit]**&#x200B;をクリックします。

1. [&#x200B; レポート設定](#report-settings.md)を編集します。

1. **[!UICONTROL Edit Custom Report]**&#x200B;をクリックします。

## カスタムレポートの実行 {#report-run-now}

有効期限が切れていない、現在実行されていないレポートを実行できます。

>[!NOTE]
>
>[作成](#report-create)または[編集](#report-edit)時にカスタムレポートを実行することもできます。

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**&#x200B;をクリックします。

1. レポート名の横で、**[!UICONTROL ...]** > **[!UICONTROL Run Now]**&#x200B;をクリックします。

   レポートが完了すると、レポート設定で指定された宛先に送信されます。

## カスタムレポートをダウンロード

過去4か月間に完了したレポートインスタンスをダウンロードできます。このインスタンスのステータスは「[!UICONTROL Ready to Download]」または「[!UICONTROL Completed]」です。

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**&#x200B;をクリックします。

1. レポート行の[!UICONTROL Download Report]列で、次の操作を行います。

   * レポートの最新のインスタンスをダウンロードするには、**[!UICONTROL Download]**&#x200B;をクリックします。

   * （複数のインスタンスを含むレポート） [!UICONTROL Download]の横にある![下向き矢印](/help/dsp/assets/chevron-down.png "下向き矢印")をクリックし、ダウンロードするレポートの完了日をクリックします。 ダウンロード可能なレポートインスタンスには、ダウンロードアイコン （![ダウンロードアイコン](/help/dsp/assets/indicator-downloadable.png "ダウンロードアイコン")）が表示されます。

     多数のインスタンスが使用可能な場合は、必要に応じて、リストの下部にある&#x200B;**[!UICONTROL Load More]**&#x200B;をクリックします。

     レポートが同じ日に複数回実行されると、その日のレポートインスタンスが時系列でリストされ、最新のインスタンスが上に表示されます。

     失敗したレポートジョブには、エラーアイコン（![&#x200B; エラーインジケーター](/help/dsp/assets/indicator-critical.png " エラーインジケーター")）が表示され、ダウンロードできません。 エラーアイコンの上にカーソルを置くと、エラーの説明が表示されます。

## カスタムレポートの削除

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**&#x200B;をクリックします。

1. レポート名の横で、**[!UICONTROL ...]** > **[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## レポート設定 {#report-settings}

**[!UICONTROL Name]:** レポート名。 最大長は180文字です。

**[!UICONTROL Report Type]:** レポートの種類。

### [!UICONTROL Report Range] セクション

このセクションでは、レポートに含まれるデータを決定します。 レポートスケジュールの日付を設定するには、「[!UICONTROL Report run schedule]」の節を参照してください。

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:**&#x200B;は、報告された時間に夏時間を考慮します。

**範囲：** データを生成する日付範囲。 使用可能な日数は、レポートと選択したディメンションによって異なります。 1つを選択：

* **[!UICONTROL Previous Calendar Week]:**&#x200B;前週のデータが含まれます。

* **[!UICONTROL Previous Calendar Month]:**&#x200B;前月のデータが含まれます。

* **[!UICONTROL Custom Range]:**&#x200B;特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートするには、**[!UICONTROL Present]**&#x200B;を選択します。

### [!UICONTROL Report Run schedule] セクション

このセクションでは、レポートを実行する日付を指定します。 レポートデータを含める日付を設定するには、「[!UICONTROL Report range]」の節を参照してください。

**\[ スケジュール\]:** レポートを生成するタイミング：

* *[!UICONTROL Immediately]*: レポートをすぐにレポートキューに追加します。

  >[!NOTE]
  >
  >[!UICONTROL Reports] ビューから[いつでも](#report-run-now) カスタムレポートを実行することもできます。

* *[!UICONTROL On]\&lt;日付\>:* アカウントのタイムゾーンで、指定された完了日にレポートを実行します（09:00）。

* *[!UICONTROL Recurring]:*&#x200B;指定した期間内に、スケジュールに従ってレポートを実行します。

   * **\[ スケジュール\]:** レポートを実行する頻度：

      * *日単位*:N日単位でレポートを実行します。 例えば、2週間（14日）ごとにレポートを実行するには、このオプションを選択し、**14**&#x200B;と入力します。

      * *毎週*&#x200B;を使用して、指定した曜日にレポートを実行します。 例えば、毎週月曜日と金曜日にレポートを実行するには、このオプションを選択し、**月曜日**&#x200B;と&#x200B;**金曜日**&#x200B;の横にあるチェックボックスをオンにします。

      * *月単位*&#x200B;で、1から30までの特定の日付にレポートを実行します。 例えば、毎月最初の日にレポートを実行するには、このオプションを選択し、**1**&#x200B;と入力します。

   * **送信元**: レポートを実行できる最初の日付。 指定したスケジュールによっては、最初のレポートインスタンスがこの日付以降に発生する場合があります。

   * **まで**: レポートの有効期限（最大4か月後まで）。 レポートの有効期限が切れる前に、指定されたすべてのメール宛先に、有効期限の7日前と1日前にメールアラートが送信されます。 レポートを長く保持するには、この日付を変更します。

### [!UICONTROL Apply Filters] セクション

**[!UICONTROL Filter by]:** （オプション）ディメンションがレポートに列として含まれているかどうかを問わず、データをフィルタリングする追加ディメンション。 使用できるフィルターはレポートの種類によって異なり、次のものが含まれます：*[!UICONTROL Advertiser]*、*[!UICONTROL Experience]*、*[!UICONTROL Creative Library]*、および&#x200B;*[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->。

1つ以上のフィルターを適用するには、次の操作を行います。

* ディメンションを選択し、演算子（*次と等しい*&#x200B;または&#x200B;*次と等しくない*）を選択してから、該当する値を選択します。 例えば、プリロール広告のみのデータを返すには、「[!UICONTROL Ad Type equals Preroll]」を指定します。
* （オプション）フィルターに条件を追加します。
* （オプション）フィルターを追加し、各フィルターに1つ以上の条件を追加します。

### [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:** レポートに含めるデータ列またはヘッダー。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスを選択します。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:**&#x200B;列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして、順序をカスタマイズできます。

**[!UICONTROL Format]:** レポートを&#x200B;*[!UICONTROL CSV]* （コンマ区切り）形式または&#x200B;*[!UICONTROL Tab]* （タブ区切り値）形式で生成するかどうか。

**[!UICONTROL Headers]:**&#x200B;列ヘッダーが&#x200B;*[!UICONTROL Include]*&#x200B;か&#x200B;*[!UICONTROL Do Not Include]*&#x200B;か否か。

### [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:**&#x200B;設定はレポートタイプによって異なります：

* **\[Rule Type\]:** （Adobe Advertising コンバージョントラッキングを使用する広告主のみ）コンバージョンにつながる一連のイベントのコンバージョンデータに属する方法をレポート内で説明します。 ルール間の差異を比較する場合は、複数のルールを選択できます。

  >[!NOTE]
  >
  >コンバージョンパスには、広告主のインプレッションまたはクリックバックウィンドウ内のインプレッションとクリックが含まれ、[!DNL Advertising Search, Social, & Commerce]に設定されています。 コンバージョンのアトリビューションでは、クリック数はインプレッション数に優先されます。 コンバージョンパス内のクリックに対しては、アトリビューションルールにもとづいて完全なクレジットを獲得します。 インプレッションは、コンバージョンパスでクリックが追跡されない場合にのみクレジットを受け取ります。

   * *[!UICONTROL Last Event]:* コンバージョンパスの最後のクリックまたはインプレッションにコンバージョンを属性します。

   * *[!UICONTROL Weight Last More]:*&#x200B;は、コンバージョンパス内のすべてのイベントにコンバージョンを割り当てますが、最後のイベントに最も多くの重みを割り当て、前のイベントに対する重みを連続して減らします。

   * *[!UICONTROL Even Distribution]:* コンバージョンパスの各イベントにコンバージョンを均等に属性します。

   * *[!UICONTROL Weight First More]:*&#x200B;は、コンバージョンパス内のすべてのイベントにコンバージョンを割り当てますが、最初のイベントに最も多くの重みを割り当て、次のイベントに対する重みを連続して減らします。

   * *[!UICONTROL First Event]:* コンバージョンパスの最初のクリックまたはインプレッションにコンバージョンを属性します。

   * *[!UICONTROL U-shaped]:* コンバージョンは、コンバージョンパス内のすべてのイベントに属しますが、最初と最後のイベントに最も多くの重みを与え、コンバージョンパスの中央にあるイベントに対する重みが順次減ります。

   * *[!UICONTROL Display Only]:* コンバージョンパス内の最後のDSPのクリックまたはインプレッションへのコンバージョンを属性します。 これには、ビデオ広告やコネクテッド TV広告が含まれ、[!DNL Advertising Search, Social, & Commerce]広告のクリックは含まれません。

   * *[!UICONTROL Social Only]:*&#x200B;が廃止されました

「[Adobe Advertisingのアトリビューションルールの計算方法](/help/search-social-commerce/reports/attribution-rules.md)」も参照してください。

**[!UICONTROL Paths as Columns]:**&#x200B;同じデバイスで以前のイベントが発生したときに報告するコンバージョンの種類。 3種類まで含めることができます。 選択したタイプごとに、コンバージョン指標ごとに別の列が含まれ、指定されたサフィックス（[!UICONTROL (tl)]、[!UICONTROL (ct)]、または[!UICONTROL (vt)]）が追加されます。

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック （クリックスルーの場合はCT）とインプレッション （ビュースルーの場合はVT）に起因するコンバージョンが含まれます。 インプレッションに起因するコンバージョンに、指定されたビュースルーの重みが掛けられます。 デフォルトのビュースルーの重みは100%です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の100%としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリックに関連付けられたコンバージョンのみが含まれます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されていないため、インプレッションに起因するコンバージョンのみが含まれます。

### [!UICONTROL Add Report Destinations] セクション

**[!UICONTROL Destination Type]:**&#x200B;完了したレポートとエラー通知の配信先。 レポートを保存すると、宛先タイプを変更することはできません。

>[!NOTE]
>
>完了済みレポートは、[!UICONTROL Reports] > [!UICONTROL Custom Reports] ビューからいつでもダウンロードできます。

* *[!UICONTROL None]:* レポートまたは通知を配信しない

* *[!UICONTROL S3]:*&#x200B;完成したレポートを1つ以上の[!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]）の場所に送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL sFTP]:*&#x200B;完了したレポートを1つ以上のSFTPの場所に送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL FTP]:*&#x200B;完了したレポートを1つ以上のFTP場所に送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL FTP SSL]（現在Beta内）:*&#x200B;完了したレポートを1つ以上のFTP SSL ロケーションに送信するには、**[!UICONTROL Destination Name]** フィールドで選択する必要があります。

* *[!UICONTROL Email]:* エラーが原因でレポートがキャンセルされた場合に、完了したレポートまたは通知を送信する電子メールアドレスを指定します。

**[!UICONTROL Email]:** （電子メールの宛先タイプのみ）各アドレスについて、アドレスを入力し、**+**&#x200B;をクリックします。

**[!UICONTROL Destination Name]:** （S3、FTP、sFTP、およびFTP SSL宛先タイプのみ）カスタムレポートを送信する[&#x200B; レポート宛先](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. 「**新しい宛先を追加**」をクリックします。

   1. [&#x200B; レポートの宛先設定](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"}を入力し、**保存**&#x200B;をクリックします。

   1. レポート設定に戻り、**宛先名を更新をクリックします。**

      新しい宛先が既存の宛先のリストから使用可能になり、オプションでレポートに追加できます。


<!--
 This needs a lot of updating for new report:

## Available report columns {#report-custom-creative-columns}

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
>* [&#x200B; エクスペリエンスレベルのパフォーマンスレポート &#x200B;](/help/creative/experiences/experience-performance-details.md)
>* [DSP カスタムレポートについて](/help/dsp/reports/report-about.md){target="_blank"}
>* [&#x200B; レポートの宛先について](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
