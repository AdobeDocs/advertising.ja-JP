---
title: カスタムレポートの設定
description: カスタムレポート設定の説明を参照してください。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# カスタムレポートの設定

**[!UICONTROL Name]** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]** レポートのタイプ：*[!UICONTROL Custom]* （利用可能な最も多くのオプションを含む）、*[!UICONTROL Billing]*、*[!UICONTROL Conversion]*、*[!UICONTROL Device]*、*[!UICONTROL Frequency (by Impression)]*、*[!UICONTROL Frequency (by App/Site)]*、*[!UICONTROL Geo]*、*[!UICONTROL Margin]*、*[!UICONTROL Media Performance]*、*[!UICONTROL Segment]*、*[!UICONTROL Site]*、*[!UICONTROL Household Reach & Frequency]* または *[!UICONTROL Household Conversions]*。

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** レポートされた時間に夏時間を考慮します。

**\[ 日付範囲\]:** データを生成する日付範囲。 使用可能な日数は、レポートや選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Previous N days]:** 今日より前の特定の日数のデータが含まれます。

* **[!UICONTROL Custom]:** 特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートするには、「**[!UICONTROL Present]**」を選択します。

* **[!UICONTROL Last Calendar Month]:** 前月のデータが含まれます。

**[!UICONTROL Add Filters]:** （オプション）ディメンションがレポートに列として含まれているかどうかに関わらず、データをフィルタリングするための追加のディメンション。 使用可能なフィルターは、レポートタイプによって異なり、*[!UICONTROL Account]*\*、*[!UICONTROL Ad Type]*、*[!UICONTROL Ads]*、*[!UICONTROL Advertiser]*、*[!UICONTROL Campaign]*、*[!UICONTROL Country]*、* *[!UICONTROL Package]*、*[!UICONTROL Placement]*、*[!UICONTROL Video]* および *[!UICONTROL Video Duration]* などがあります。

\* *[!UICONTROL Account]* は、組織が [ クロスアカウントレポート ](report-about.md#cross-account-reporting) 用に設定されている場合にのみ使用できます：[!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)] および [!UICONTROL Conversion]。 クロスアカウントレポートについて詳しくは、Adobeアカウントチームにお問い合わせください。

1 つ以上のフィルターを適用するには、次の手順を実行します。

* ディメンションを選択し、演算子（*次に等しい* または *次に等しくない*）を選択して、該当する値を選択します。 例えば、プリロール広告のみのデータを返すには、「[!UICONTROL Ad Type equals Preroll]」と指定します。
* （任意）フィルターに条件を追加します。
* （任意）さらにフィルターを追加し、各フィルターに 1 つ以上の条件を指定します。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:** レポートに含めるデータ列（ヘッダー）。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスをオンにします。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。 使用可能なデータカテゴリを次に示します。

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > [!UICONTROL Household Reach & Frequency] レポートには、ディメンションを 1 つだけ含めることができます。

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

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **ルックバック：** （[!UICONTROL Conversion Metrics] 列または [!UICONTROL Custom Goals] 列の [!UICONTROL Household Conversion] レポート。Adobe Advertisingのコンバージョントラッキングのみを使用する広告主）レポート内で、コンバージョンイベントの属性をインプレッションイベントから取得できる最大日数。 デフォルトは *[!UICONTROL 30 days]* で、最大 92 日です。

**[!UICONTROL Paths as Columns]:** （すべての [!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment] および [!UICONTROL Site] レポート（[!UICONTROL Conversion Metrics] 列または [!UICONTROL Custom Goals] 列）同じデバイスで以前のイベントが発生した場合にレポートするコンバージョンのタイプ。 最大 3 つのタイプを含めることができます。 選択したタイプごとに、コンバージョン指標ごとに個別の列が含まれ、指定したサフィックス（[!UICONTROL (tl)]、[!UICONTROL (ct)] または [!UICONTROL (vt)]）が追加されます。

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーの CT）およびインプレッション数（ビュースルーの VT）に起因するコンバージョンを含みます。 インプレッション数に起因するコンバージョンは、指定されたビュースルーの重み付けで乗算されます。 デフォルトのビュースルーの重み付けは 100% です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の 100% としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリック数に起因するコンバージョンのみを含みます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったことが原因で、インプレッション数に起因するコンバージョンのみが含まれます。

**[!UICONTROL Conversion Reporting Based On]:** コンバージョンデータのレポート方法

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）変換は、変換日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* コンバージョンは、指定された [!UICONTROL Attribution Rule Settings] によって決定された、コンバージョンの原因となったインプレッションまたはクリックの日付に基づいてレポートされます。

## [!UICONTROL Add Report Destinations] セクション

**[!UICONTROL Destination Type]:** 次のいずれかの宛先タイプを選択します。

* *[!UICONTROL S3]:* 完成したレポートを 1 つ以上の [!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]）の場所に送信するには、**[!UICONTROL Destination Name]** フィールドで指定する必要があります。
* *[!UICONTROL sFTP]:* 完成したレポートを 1 つ以上の SFTP の場所に送信するには、**[!UICONTROL Destination Name]** のフィールドにレポートを指定する必要があります。
* *[!UICONTROL FTP]:* 完成したレポートを 1 つ以上の FTP ロケーションに送信するには、**[!UICONTROL Destination Name]** のフィールドにレポートを指定する必要があります。
* *[!UICONTROL FTP SSL]（現在はBetaにあります）:* 完成したレポートを 1 つ以上の FTP SSL 場所に送信するには、**[!UICONTROL Destination Name]** フィールドに指定する必要があります。
* *[!UICONTROL Email]:* 完了したレポートまたはエラーが原因でレポートがキャンセルされた場合に通知を送信する電子メール アドレスを指定します。

>[!NOTE]
>
> レポートを保存した後は、宛先のタイプを変更できません。

**[!UICONTROL Email]:** （電子メールの宛先タイプのみ）各アドレスに対して、アドレスを入力し、**+** をクリックします。

**[!UICONTROL Destination Name]:** （S3、FTP、sFTP および FTP SSL 宛先タイプのみ）カスタムレポートの送信先となるレポート宛先の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. **新しい宛先を追加** をクリックします。

   1. [ レポート宛先設定 ](/help/dsp/reports/report-destinations/report-destination-settings.md) を入力し、「**保存**」をクリックします。

   1. レポート設定に戻り、「**宛先名を更新**」をクリックします。

      これで、既存の宛先のリストから新しい宛先を使用できるようになり、オプションでレポートに追加できます。

**[!UICONTROL Frequency]:** （各 [!UICONTROL Destination Name] に対して）レポートを宛先に送信する頻度：*[!UICONTROL Once]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]* または *[!UICONTROL Monthly]*。

**[!UICONTROL Start Day]:** （[!UICONTROL Frequency] が *[!UICONTROL Weekly]* または *[!UICONTROL Monthly]* の各 [!UICONTROL Destination Name] について） レポートを生成する日。 週別レポートの場合は、曜日を選択します。 月次レポートの場合は、月の特定の日付を選択します。

## [!UICONTROL Save Report] セクション

**[!UICONTROL When to Generate]:** レポートを生成するタイミング：*[!UICONTROL On Schedule]* または *[!UICONTROL Run Now]*。 予定レポートは、アカウントのタイムゾーンで 09:00 までに配信されます。

**[!UICONTROL End Date]:** レポートの有効期限。4 か月以内で設定できます。 レポートの有効期限が切れる前に、指定したすべてのメール受信者は、有効期限の 7 日前と 1 日前にメールアラートを受け取ります。 レポートを長く保持するには、レポート設定で有効期限を変更します。

>[!NOTE]
>
>[!UICONTROL Reports] ビューから [ いつでもカスタムレポートを実行 ](report-run-now.md) できます。

>[!MORELIKETHIS]
>
>* [ カスタムレポートについて ](/help/dsp/reports/report-about.md)
>* [ カスタムレポートの作成 ](/help/dsp/reports/report-create.md)
>* [ カスタムレポートの複製 ](/help/dsp/reports/report-copy.md)
>* [ カスタムレポートの編集 ](/help/dsp/reports/report-edit.md)
>* [ カスタムレポートの実行 ](/help/dsp/reports/report-run-now.md)
>* [ カスタムレポートの設定 ](/help/dsp/reports/report-settings.md)
>* [ レポートの宛先について ](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [ 使用可能なレポート列 ](/help/dsp/reports/report-columns.md)
