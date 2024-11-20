---
title: カスタムレポートの設定
description: カスタムレポート設定の説明を参照してください。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 73641f1a3cd1729ccb978739e9888cf2ff58d16f
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 0%

---

# カスタムレポートの設定

**[!UICONTROL Name]:** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]:** レポートのタイプ。*[!UICONTROL Custom]* （利用可能な最も多くのオプションを含む）、*[!UICONTROL Billing]*、*[!UICONTROL Conversion]*、*[!UICONTROL Device]*、*[!UICONTROL Frequency (by Impression)]*、*[!UICONTROL Frequency (by App/Site)]*、*[!UICONTROL Geo]*、*[!UICONTROL Margin]*、*[!UICONTROL Media Performance]*、*[!UICONTROL Segment]*、*[!UICONTROL Site]*、*[!UICONTROL Household Reach & Frequency]*、*[!UICONTROL Household Conversions]*、*[!UICONTROL Path to Conversions Beta]*、*[!UICONTROL Path Length Beta]* または *[!UICONTROL Time to Conversion Beta]*。

## [!UICONTROL Report Range] セクション

このセクションは、レポートに含めるデータを決定します。 レポートスケジュールの日付を設定するには、「[!UICONTROL Report run schedule]」の節を参照してください。

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** レポートされた時間に夏時間を考慮します。

**範囲：** データを生成する日付範囲。 使用可能な日数は、レポートや選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Last Calendar Week]:** 前のカレンダー週のデータが含まれます。

* **[!UICONTROL Last Calendar Month]:** 前月のデータが含まれます。

* **[!UICONTROL Custom Range]:** 特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートするには、「**[!UICONTROL Present]**」を選択します。

## [!UICONTROL Report Run schedule] セクション

このセクションは、レポートが実行される日付を決定します。 レポートデータを含める日付を設定するには、「[!UICONTROL Report range]」の節を参照してください。

**\[ スケジュール\]:** レポートを生成するタイミング：

* *[!UICONTROL Immediately]*：直ちにレポートをレポートキューに追加します。

  >[!NOTE]
  >
  >また、[!UICONTROL Reports] ビューから [ いつでもカスタムレポートを実行 ](report-run-now.md) することもできます。

* *[!UICONTROL On]\&lt;Date\>:* 指定した完了日に、アカウントのタイムゾーンで 09:00 までにレポートを実行します。

* *[!UICONTROL Recurring]:* 指定した期間のスケジュールに従ってレポートを実行します。

   * **\[Schedule\]:** レポートの実行頻度：

      * *毎日*:N 日ごとにレポートを実行します。 例えば、レポートを 2 週間（14 日）ごとに実行するには、このオプションを選択して「**14**」と入力します。

      * *毎週*：指定した曜日にレポートを実行します。 たとえば、レポートを毎週月曜日と金曜日に実行する場合は、このオプションを選択し、**月曜日** および **金曜日** の横にあるチェック ボックスをオンにします。

      * *毎月* 1 日から 30 日の特定の数値日にレポートを実行します。 例えば、毎月 1 日にレポートを実行する場合は、このオプションを選択して「**1**」と入力します。

   * **開始日**: レポートを実行できる最初の日付。 指定したスケジュールに応じて、この日付以降に最初のレポートインスタンスが実行される場合があります。

   * **期限**: レポートの有効期限。最大 4 か月先の日付を指定できます。 レポートの有効期限が切れる前に、指定したすべてのメール宛先に、有効期限の 7 日前と 1 日前にメールアラートが届きます。 レポートの期間を延長するには、この日付を変更します。

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Filter by]:** （オプション）ディメンションがレポートに列として含まれているかどうかに関わらず、データをフィルタリングするための追加のディメンション。 使用可能なフィルターは、レポートタイプによって異なり、*[!UICONTROL Account]*\*、*[!UICONTROL Ad Type]*、*[!UICONTROL Ads]*、*[!UICONTROL Advertiser]*、*[!UICONTROL Campaign]*、*[!UICONTROL Country]*、* *[!UICONTROL Package]*、*[!UICONTROL Placement]*、*[!UICONTROL Video]* および *[!UICONTROL Video Duration]* などがあります。

1 つ以上のフィルターを適用するには、次の手順を実行します。

* ディメンションを選択し、演算子（*次に等しい* または *次に等しくない*）を選択して、該当する値を選択します。 例えば、プリロール広告のみのデータを返すには、「[!UICONTROL Ad Type equals Preroll]」と指定します。
* （任意）フィルターに条件を追加します。
* （任意）さらにフィルターを追加し、各フィルターに 1 つ以上の条件を指定します。

\* *[!UICONTROL Account]* は、組織が [ クロスアカウントレポート ](report-about.md#cross-account-reporting) 用に設定されている場合にのみ使用できます：[!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)] および [!UICONTROL Conversion]。 クロスアカウントレポートについて詳しくは、Adobeアカウントチームにお問い合わせください。

**[!UICONTROL Include data from Adobe Advertising SSC]:** （「コンバージョンまでのパス」、「コンバージョンまでのパス長」および「コンバージョンまでの時間」レポートのみ）指定したAdvertising検索、ソーシャルおよびCommerceの各キャンペーンに対する検索広告のクリック数に関するデータが含まれます。 このオプションを選択した場合：

1. **フィルターで絞り込む」フィルターを使用して、検索、ソーシャル、Commerceの各アカウント[!UICONTROL SSC Account]** 選択します。

1. **フィルターを使用してキャンペーン[!UICONTROL SSC Campaign]** 選択します。

   複数のキャンペーンを選択するには、2 回目以降のキャンペーンの **[!UICONTROL Add Criteria]** をクリックします。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:** レポートに含めるデータ列（ヘッダー）。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスをオンにします。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。 利用可能なデータカテゴリには、次のものが含まれます。

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > [!UICONTROL Household Reach & Frequency] および [!UICONTROL Path to Conversion] レポートには、ディメンションを 1 つだけ含めることができます。
  > [!UICONTROL Path Length] と [!UICONTROL Time to Conversion] のレポートには、ディメンションは含まれていません。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >[!UICONTROL Household Reach & Frequency] レポートには、重複指標または重複以外の指標のいずれかを含めることができますが、両方を含めることはできません。

* [!UICONTROL Conversion Metrics] （広告主順）

* [!UICONTROL Custom Goals] （広告主順）

すべてのオプションの説明は、[ 使用可能なレポート列 ](report-columns.md)」を参照してください。

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして、順序をカスタマイズできます。

**[!UICONTROL Format]:** レポートを *[!UICONTROL CSV]* （コンマ区切り値）形式または *[!UICONTROL Tab]* （タブ区切り値）形式のどちらで生成するか。

**[!UICONTROL Headers]:** 列ヘッダーを *[!UICONTROL Include]* 示するか *[!UICONTROL Do Not Include]* うかを指定します。

## [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:** 設定はレポートタイプによって異なります。

* **\[Attribution Type\]:** （[!UICONTROL Conversion Metrics] 列または [!UICONTROL Custom Goals] 列の [!UICONTROL Household Conversion] レポート、Adobe Advertisingコンバージョントラッキングのみを使用する広告主） レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータを属性化する方法：

   * *[!UICONTROL Unique]:* （デフォルト）ディメンション値（デバイスや配置など）が変換されるパス上にあった回数をカウントします。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* コンバージョンへのパス上でのディメンション値（デバイスや配置など）の発生頻度に基づいて、各コンバージョンのクレジットを配分します。 例えば、コンバージョン前に合計 10 件のインプレッションがあり、CTV に 8 件、モバイルに 2 件あった場合、クレジットの 80% （0.8）が CTV 画面に、0.2 がモバイルに与えられます。

* **\[Rule Type\]:** （[!UICONTROL Conversion Metrics] 列または [!UICONTROL Custom Goals] 列のすべての [!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment] および [!UICONTROL Site] レポート。Adobe Advertisingコンバージョントラッキングのみを使用する広告主）レポート内で、コンバージョンにつながる一連のイベントのコンバージョンデータを属性化する方法。 ルール間の違いを比較する場合は、複数のルールを選択できます。

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

* **ルックバック：** （[!UICONTROL Conversion Metrics] 列または [!UICONTROL Custom Goals] 列を含む [!UICONTROL Household Conversion] レポートおよび [!UICONTROL Conversion Metrics] 列のみを含む [!UICONTROL Path to Conversion]、[!UICONTROL Path Length] または [!UICONTROL Time to Conversion] レポート。Adobe Advertisingコンバージョントラッキングのみを含む広告主）レポート内で、コンバージョンイベントまたはそのイベントに起因する可能性のあるクリックイベント（[!UICONTROL Path to Conversion]、[!UICONTROL Path Length] または [!UICONTROL Time to Conversion] レポートの場合）後の最大日数。 デフォルトは *[!UICONTROL 30 days]* で、最大 92 日です。

  >[!TIP]
  >
  >[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する場合は、[!DNL Analytics] で使用するのと同じルックバックウィンドウを使用します。

**[!UICONTROL Paths as Columns]:** （すべての [!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment] および [!UICONTROL Site] レポート（[!UICONTROL Conversion Metrics] 列または [!UICONTROL Custom Goals] 列）同じデバイスで以前のイベントが発生した場合にレポートするコンバージョンのタイプ。 最大 3 つのタイプを含めることができます。 選択したタイプごとに、コンバージョン指標ごとに個別の列が含まれ、指定したサフィックス（[!UICONTROL (tl)]、[!UICONTROL (ct)] または [!UICONTROL (vt)]）が追加されます。

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーの CT）およびインプレッション数（ビュースルーの VT）に起因するコンバージョンを含みます。 インプレッション数に起因するコンバージョンは、指定されたビュースルーの重み付けで乗算されます。 デフォルトのビュースルーの重み付けは 100% です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の 100% としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリック数に起因するコンバージョンのみを含みます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったことが原因で、インプレッション数に起因するコンバージョンのみが含まれます。

**[!UICONTROL Conversion Reporting Based On]:** コンバージョンデータのレポート方法

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）変換は、変換日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* コンバージョンは、指定された [!UICONTROL Attribution Rule Settings] によって決定された、コンバージョンの原因となったインプレッションまたはクリックの日付に基づいてレポートされます。

## [!UICONTROL Add Report Destinations] セクション

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

**[!UICONTROL Destination Name]:** （S3、FTP、sFTP および FTP SSL 宛先タイプのみ）カスタムレポートの送信先となるレポート宛先の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. **新しい宛先を追加** をクリックします。

   1. [ レポート宛先設定 ](/help/dsp/reports/report-destinations/report-destination-settings.md) を入力し、「**保存**」をクリックします。

   1. レポート設定に戻り、「**宛先名を更新**」をクリックします。

      これで、既存の宛先のリストから新しい宛先を使用できるようになり、オプションでレポートに追加できます。

>[!MORELIKETHIS]
>
>* [ カスタムレポートについて ](/help/dsp/reports/report-about.md)
>* [ カスタムレポートの作成 ](/help/dsp/reports/report-create.md)
>* [ カスタムレポートの複製 ](/help/dsp/reports/report-copy.md)
>* [ カスタムレポートの編集 ](/help/dsp/reports/report-edit.md)
>* [ カスタムレポートのダウンロード ](/help/dsp/reports/report-download.md)
>* [ カスタムレポートの実行 ](/help/dsp/reports/report-run-now.md)
>* [ カスタムレポートの設定 ](/help/dsp/reports/report-settings.md)
>* [ レポートの宛先について ](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [ 使用可能なレポート列 ](/help/dsp/reports/report-columns.md)
