---
title: カスタムレポート設定
description: カスタムレポート設定の説明を参照してください。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
TQID: https://experienceleague.adobe.com/4b95Ua1HlD3KnjH0A4ZWIxvFAouU3bxJWrVysM5xnUU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 9c0a1de4a3514cbb28856250b76e79e1b7913963
workflow-type: tm+mt
source-wordcount: 1535
ht-degree: 0%

---

# カスタムレポート設定

**[!UICONTROL Name]:** レポート名。 最大長は180文字です。

**[!UICONTROL Report Type]:** レポートの種類：*[!UICONTROL Custom]* （最も使用可能なオプションを含む）、*[!UICONTROL Billing]*、*[!UICONTROL Conversion]*、*[!UICONTROL Device]*、*[!UICONTROL Frequency (by Impression)]*、*[!UICONTROL Frequency (by App/Site)]*、*[!UICONTROL Geo]*、*[!UICONTROL Margin]*、*[!UICONTROL Media Performance]*、*[!UICONTROL Segment]*、*[!UICONTROL Site]*、*[!UICONTROL Household Reach & Frequency]*、*[!UICONTROL Household Conversions]*、**、*[!UICONTROL Path Length]*&#x200B;または&#x200B;*[!UICONTROL Time to Conversion]*。

## [!UICONTROL Report Range] セクション

このセクションでは、レポートに含まれるデータを決定します。 レポートスケジュールの日付を設定するには、「[!UICONTROL Report run schedule]」の節を参照してください。

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:**&#x200B;は、報告された時間に夏時間を考慮します。

**範囲：** データを生成する日付範囲。 使用可能な日数は、レポートと選択したディメンションによって異なります。 1つを選択：

* **[!UICONTROL Previous Calendar Week]:**&#x200B;前週のデータが含まれます。

* **[!UICONTROL Previous Calendar Month]:**&#x200B;前月のデータが含まれます。

* **[!UICONTROL Custom Range]:**&#x200B;特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートするには、**[!UICONTROL Present]**&#x200B;を選択します。

## [!UICONTROL Report Run schedule] セクション

このセクションでは、レポートを実行する日付を指定します。 レポートデータを含める日付を設定するには、「[!UICONTROL Report range]」の節を参照してください。

**\[ スケジュール\]:** レポートを生成するタイミング：

* *[!UICONTROL Immediately]*: レポートをすぐにレポートキューに追加します。

  >[!NOTE]
  >
  >[!UICONTROL Reports] ビューから[いつでも](report-run-now.md) カスタムレポートを実行することもできます。

* *[!UICONTROL On]\&lt;日付\>:* アカウントのタイムゾーンで、指定された完了日にレポートを実行します（09:00）。

* *[!UICONTROL Recurring]:*&#x200B;指定した期間内に、スケジュールに従ってレポートを実行します。

   * **\[ スケジュール\]:** レポートを実行する頻度：

      * *日単位*:N日単位でレポートを実行します。 例えば、2週間（14日）ごとにレポートを実行するには、このオプションを選択し、**14**&#x200B;と入力します。

      * *毎週*&#x200B;を使用して、指定した曜日にレポートを実行します。 例えば、毎週月曜日と金曜日にレポートを実行するには、このオプションを選択し、**月曜日**&#x200B;と&#x200B;**金曜日**&#x200B;の横にあるチェックボックスをオンにします。

      * *月単位*&#x200B;で、1から30までの特定の日付にレポートを実行します。 例えば、毎月最初の日にレポートを実行するには、このオプションを選択し、**1**&#x200B;と入力します。

   * **送信元**: レポートを実行できる最初の日付。 指定したスケジュールによっては、最初のレポートインスタンスがこの日付以降に発生する場合があります。

   * **まで**: レポートの有効期限（最大4か月後まで）。 レポートの有効期限が切れる前に、指定されたすべてのメール宛先に、有効期限の7日前と1日前にメールアラートが送信されます。 レポートを長く保持するには、この日付を変更します。

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Filter by]:** （オプション）ディメンションがレポートに列として含まれているかどうかを問わず、データをフィルタリングする追加ディメンション。 使用できるフィルターはレポートの種類によって異なり、*[!UICONTROL Account]*、*[!UICONTROL Ad Type]*、*[!UICONTROL Ads]*、*[!UICONTROL Advertiser]*、*[!UICONTROL Campaign]*、*[!UICONTROL Country]*、*[!UICONTROL Deal]*、*[!UICONTROL Package]*、*[!UICONTROL Placement]*、*[!UICONTROL Traffic Type]*、*[!UICONTROL Video]*、および&#x200B;*[!UICONTROL Video Duration]*&#x200B;が含まれる場合があります。

<!--
 Add when available:
*[!UICONTROL Deal ID]*, *[!UICONTROL Deal List]*, 
-->

1つ以上のフィルターを適用するには、次の操作を行います。

* ディメンションを選択し、演算子（*次と等しい*&#x200B;または&#x200B;*次と等しくない*）を選択してから、該当する値を選択します。 例えば、プリロール広告のみのデータを返すには、「[!UICONTROL Ad Type equals Preroll]」を指定します。
* （オプション）フィルターに条件を追加します。
* （オプション）フィルターを追加し、各フィルターに1つ以上の条件を追加します。

\* *[!UICONTROL Account]*&#x200B;は、組織が[ クロスアカウントレポート ](report-about.md#cross-account-reporting)用に設定されている場合にのみ、次のレポートタイプで利用できます：[!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]、および[!UICONTROL Conversion]。 クロスアカウントレポートについて詳しくは、Adobe アカウントチームにお問い合わせください。

**[!UICONTROL Include data from Adobe Advertising SSC]:** （[!UICONTROL Path to Conversion]、[!UICONTROL Path Length]、および[!UICONTROL Time to Conversion]件のレポートのみ）指定したAdvertising Search、Social、およびCommerce キャンペーンの検索広告のクリックに関するデータが含まれます。 このオプションを選択すると、次のようになります。

1. 「**フィルターで[!UICONTROL SSC Account]**」フィルターを使用して、検索、ソーシャル、Commerce アカウントを選択します。

1. **フィルター[!UICONTROL SSC Campaign]** フィルターを使用してキャンペーンを選択します。

   複数のキャンペーンを選択するには、2回目以降のキャンペーンの&#x200B;**[!UICONTROL Add Criteria]**&#x200B;をクリックします。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:** レポートに含めるデータ列またはヘッダー。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスを選択します。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。 使用可能なデータカテゴリには、次のようなものがあります。

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > [!UICONTROL Household Reach & Frequency]と[!UICONTROL Path to Conversion]のレポートには、1つのディメンションのみを含めることができます。
  > [!UICONTROL Path Length]と[!UICONTROL Time to Conversion]のレポートにはディメンションが含まれていません。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >[!UICONTROL Household Reach & Frequency] レポートには、重複する指標または重複しない指標のいずれかを含めることができますが、両方を含めることはできません。

* [!UICONTROL Conversion Metrics] （広告主順）

* [!UICONTROL Custom Goals] （広告主順）

すべてのオプションについて詳しくは、「[使用可能なレポート列](report-columns.md)」を参照してください。

**[!UICONTROL Drag to Re-Order Report Headers Below]:**&#x200B;列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして、順序をカスタマイズできます。

**[!UICONTROL Format]:** レポートを&#x200B;*[!UICONTROL CSV]* （コンマ区切り）形式または&#x200B;*[!UICONTROL Tab]* （タブ区切り値）形式で生成するかどうか。

**[!UICONTROL Headers]:**&#x200B;列ヘッダーが&#x200B;*[!UICONTROL Include]*&#x200B;か&#x200B;*[!UICONTROL Do Not Include]*&#x200B;か否か。

## [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:**&#x200B;設定はレポートタイプによって異なります：

* **\[Attribution Type\]:** （[!UICONTROL Conversion Metrics]列または[!UICONTROL Custom Goals]列の[!UICONTROL Household Conversion]件のレポート） レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータを属性にする方法：

   * *[!UICONTROL Unique]:* （既定値）ディメンション値（デバイスやプレースメントなど）がコンバージョンに至るまでのパス上に存在した回数をカウントします。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* コンバージョンへのパス上のディメンション値（デバイスやプレースメントなど）の発生頻度に基づいて、各コンバージョンのクレジットを分配します。 例えば、コンバージョンまでにCTVで8つ、モバイルで2つの、合計10のインプレッションがあった場合、クレジット（0.8）はCTV スクリーン、0.2はモバイルに割り当てられます。

* **\[Rule Type\]:** （All [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], [!UICONTROL Site] reports with [!UICONTROL Conversion Metrics]または[!UICONTROL Custom Goals] columns; Adobe Advertising コンバージョントラッキング専用の広告主） レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータをアトリビューションする方法を説明します。 ルール間の差異を比較する場合は、複数のルールを選択できます。

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

* **ルックバック：** （[!UICONTROL Conversion Metrics]列または[!UICONTROL Custom Goals]列の[!UICONTROL Household Conversion]件のレポート、および[!UICONTROL Conversion Metrics]列の[!UICONTROL Path to Conversion]、[!UICONTROL Path Length]または[!UICONTROL Time to Conversion]件のレポート、Adobe Advertising コンバージョントラッキングのみの広告主）レポート内で、インプレッションイベントまたはクリックイベント後の最大日数（[!UICONTROL Path to Conversion]、[!UICONTROL Path Length]、または[!UICONTROL Time to Conversion]件のレポート）。コンバージョンイベントに起因する可能性があります。 デフォルトは&#x200B;*[!UICONTROL 30 days]*&#x200B;で、最大は92日です。

  >[!TIP]
  >
  >[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を使用する場合は、[!DNL Analytics]で使用するのと同じルックバックウィンドウを使用します。

**[!UICONTROL Paths as Columns]:** （すべての[!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment]、および[!UICONTROL Site] レポート （列は[!UICONTROL Conversion Metrics]または[!UICONTROL Custom Goals]）同じデバイスで以前のイベントが発生したときに報告するコンバージョンの種類）。 3種類まで含めることができます。 選択したタイプごとに、コンバージョン指標ごとに別の列が含まれ、指定されたサフィックス（[!UICONTROL (tl)]、[!UICONTROL (ct)]、または[!UICONTROL (vt)]）が追加されます。

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック （クリックスルーの場合はCT）とインプレッション （ビュースルーの場合はVT）に起因するコンバージョンが含まれます。 インプレッションに起因するコンバージョンに、指定されたビュースルーの重みが掛けられます。 デフォルトのビュースルーの重みは100%です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の100%としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリックに関連付けられたコンバージョンのみが含まれます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されていないため、インプレッションに起因するコンバージョンのみが含まれます。

**[!UICONTROL Conversion Reporting Based On]:** コンバージョンデータをレポートする方法：

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）コンバージョンは、コンバージョン日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* コンバージョンは、指定された[!UICONTROL Attribution Rule Settings]によって決定された、コンバージョンの原因となったインプレッションまたはクリックの日付に基づいて報告されます。

## [!UICONTROL Add Report Destinations] セクション

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

**[!UICONTROL Destination Name]:** （S3、FTP、sFTP、およびFTP SSL宛先タイプのみ）カスタムレポートを送信するレポート宛先の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. 「**新しい宛先を追加**」をクリックします。

   1. [ レポートの宛先設定](/help/dsp/reports/report-destinations/report-destination-settings.md)を入力し、**保存**&#x200B;をクリックします。

   1. レポート設定に戻り、**宛先名を更新をクリックします。**

      新しい宛先が既存の宛先のリストから使用可能になり、オプションでレポートに追加できます。

>[!MORELIKETHIS]
>
>* [ カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [ カスタムレポートを作成](/help/dsp/reports/report-create.md)
>* [ カスタムレポートを複製](/help/dsp/reports/report-copy.md)
>* [ カスタムレポートを編集](/help/dsp/reports/report-edit.md)
>* [ カスタムレポートをダウンロード ](/help/dsp/reports/report-download.md)
>* [ カスタムレポートを実行](/help/dsp/reports/report-run-now.md)
>* [ カスタムレポート設定](/help/dsp/reports/report-settings.md)
>* [ レポートの宛先について](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
