---
title: カスタムレポートの設定
description: カスタムレポート設定の説明を参照してください。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '1257'
ht-degree: 0%

---

# カスタムレポートの設定

**[!UICONTROL Name]** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]** レポートのタイプ： *[!UICONTROL Custom]* （利用可能なオプションのほとんどが含まれます）。 *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*、または *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** レポートされた時間に夏時間を考慮します。

**\[ 日付範囲\]:** データを生成する日付範囲。 使用可能な日数は、レポートや選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Previous N days]:** 今日より前の特定の日数のデータが含まれます。

* **[!UICONTROL Custom]:** 特定の開始日と終了日の間のデータを含めます。 前日までのデータをレポートするには、次のオプションを選択します： **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** 先月のデータが含まれます。

**[!UICONTROL Add Filters]:** （オプション）ディメンションがレポートに列として含まれているかどうかに関わらず、データをフィルタリングするための追加のディメンション。 使用可能なフィルターは、レポートタイプによって異なり、次のものが含まれる場合があります。 *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*、および *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* は、組織が用に設定されている場合にのみ、次のレポートタイプで使用できます [クロスアカウントレポート](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]、および [!UICONTROL Conversion]. クロスアカウントレポートについて詳しくは、Adobeアカウントチームにお問い合わせください。

1 つ以上のフィルターを適用するには、次の手順を実行します。

* ディメンションを選択し、演算子（*等しい* または *次と等しくない*）を選択してから、該当する値を選択します。 例えば、プリロール広告のみのデータを返すには、「」と指定します[!UICONTROL Ad Type equals Preroll].」と入力します。
* （任意）フィルターに条件を追加します。
* （任意）さらにフィルターを追加し、各フィルターに 1 つ以上の条件を指定します。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:**  レポートに含めるデータ列またはヘッダー。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスをオンにします。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になります。 使用可能なデータカテゴリを次に示します。

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > この [!UICONTROL Household Reach & Frequency] レポートに含めることができるディメンションは 1 つだけです。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >この [!UICONTROL Household Reach & Frequency] レポートには、重複指標または重複以外の指標のいずれかを含めることができますが、両方を含めることはできません。

* [!UICONTROL Conversion Metrics] （広告主順）

* [!UICONTROL Custom Goals] （広告主順）

参照先」[使用可能なレポート列](report-columns.md)」と表示されます（すべてのオプションの説明）。

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして、順序をカスタマイズできます。

**[!UICONTROL Format]:** でレポートを生成するかどうか *[!UICONTROL CSV]* （コンマ区切り値）または *[!UICONTROL Tab]* （タブ区切り値）の形式。

**[!UICONTROL Headers]:** 対象 *[!UICONTROL Include]* または *[!UICONTROL Do Not Include]* 列ヘッダー。

## [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:** 設定は、レポートタイプによって異なります。

* **\[ 属性タイプ\]:** （[!UICONTROL Household Conversion] を使用したレポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列：Adobe Advertisingコンバージョントラッキングを使用している広告主のみ）レポート内で、コンバージョンにつながる一連のイベントでコンバージョンデータを関連付ける方法を示します。

   * *[!UICONTROL Unique]:* （デフォルト）ディメンション値（デバイスや配置など）がコンバージョンへのパス上にあった回数をカウントします。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:*  コンバージョンへのパス上でのディメンション値（デバイスや配置など）の発生頻度に基づいて、各コンバージョンのクレジットを配分します。 例えば、コンバージョン前に合計 10 件のインプレッションがあり、CTV に 8 件、モバイルに 2 件あった場合、クレジットの 80% （0.8）が CTV 画面に、0.2 がモバイルに与えられます。

* **\[ 規則の種類\]:** （すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]、および [!UICONTROL Site] を使用したレポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列：Adobe Advertisingコンバージョントラッキングを使用している広告主のみ）レポート内で、コンバージョンにつながる一連のイベントでコンバージョンデータを関連付ける方法を示します。 ルール間の違いを比較する場合は、複数のルールを選択できます。

  >[!NOTE]
  >
  >コンバージョンパスには、広告主のインプレッションまたはクリックルックバックウィンドウ内のインプレッションとクリックが含まれます。このウィンドウの設定は、 [!DNL Advertising Search, Social, & Commerce]. クリック数は、コンバージョンアトリビューション中にインプレッション数より優先されます。 コンバージョンパスでのクリックは、アトリビューションルールに基づいて完全なクレジットを受け取ります。 インプレッションは、コンバージョンパスでクリックが追跡されなかった場合にのみクレジットを受け取ります。

   * *[!UICONTROL Last Event]:* コンバージョンパス内の最後のクリックまたはインプレッションに対するコンバージョンを属性に設定します。

   * *[!UICONTROL Weight Last More]:* コンバージョンパス内のすべてのイベントへのコンバージョンを属性に設定しますが、最後のイベントに最も重みを与え、先行するイベントに連続的に重みを減らします。

   * *[!UICONTROL Even Distribution]:* コンバージョンパス内の各イベントへのコンバージョンを均等に属性にします。

   * *[!UICONTROL Weight First More]:* コンバージョンパス内のすべてのイベントへのコンバージョンを属性に設定しますが、最初のイベントに最も多くの重み付けを行い、後続のイベントに対しては順に少ない重み付けを行います。

   * *[!UICONTROL First Event]:* コンバージョンパスの最初のクリックまたはインプレッションへのコンバージョンを属性に設定します。

   * *[!UICONTROL U-shaped]:* コンバージョンパス内のすべてのイベントにコンバージョンが関連付けられますが、最初と最後のイベントに最も重みを与え、コンバージョンパスの途中のイベントには順に少ない重みを与えます。

   * *[!UICONTROL Display Only]:*  コンバージョンパス内の最後のDSP クリックまたはインプレッションへのコンバージョンを属性に設定します。 これには、ビデオおよび接続されたテレビ広告が含まれ、のクリックは含まれません [!DNL Advertising Search, Social, & Commerce] 広告。

   * *[!UICONTROL Social Only]:* 廃止

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **ルックバック :** （[!UICONTROL Household Conversion] を使用したレポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列：Adobe Advertisingのコンバージョントラッキングを使用している広告主のみ）レポート内で、コンバージョンイベントの属性をインプレッションイベントから取得できる最大日数です。 デフォルトはです *[!UICONTROL 30 days]*、最大 92 日です。

**[!UICONTROL Paths as Columns]:**  （すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]、および [!UICONTROL Site] を使用したレポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列）同じデバイスで以前のイベントが発生した場合にレポートするコンバージョンのタイプ。 最大 3 つのタイプを含めることができます。 選択したタイプごとに、コンバージョン指標ごとに個別の列が含まれ、指定したサフィックス（[!UICONTROL (tl)], [!UICONTROL (ct)]、または [!UICONTROL (vt)]）:

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーの CT）およびインプレッション数（ビュースルーの VT）に起因するコンバージョンを含みます。 インプレッション数に起因するコンバージョンは、指定されたビュースルーの重み付けで乗算されます。 デフォルトのビュースルーの重み付けは 100% です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の 100% としてカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリックに起因するコンバージョンのみを含める。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったことが原因でインプレッション数に関連付けられたコンバージョンのみを含めます。

**[!UICONTROL Conversion Reporting Based On]:**  コンバージョンデータのレポート方法：

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）コンバージョンはコンバージョン日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* コンバージョンは、コンバージョンの原因となったインプレッションまたはクリックの日付に基づいて、指定によって決定されてレポートされます [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] セクション

**[!UICONTROL Destination Type]:** 次のいずれかの宛先タイプを選択します。

* *[!UICONTROL S3]:* 完成したレポートを 1 つ以上のユーザーに送信するには [!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]）の場所を使用します。 **[!UICONTROL Destination Name]** フィールド。
* *[!UICONTROL sFTP]:* 完成したレポートを 1 つ以上の SFTP ロケーションに送信するには、で指定します。 **[!UICONTROL Destination Name]** フィールド。
* *[!UICONTROL FTP]:* 完成したレポートを 1 つ以上の FTP ロケーションに送信するには、で指定します。 **[!UICONTROL Destination Name]** フィールド。
* *[!UICONTROL FTP SSL]（現在はベータ版）:* 完成したレポートを 1 つ以上の FTP SSL 場所に送信するには、で指定します。 **[!UICONTROL Destination Name]** フィールド。
* *[!UICONTROL Email]:* 完了したレポートまたはエラーが原因でレポートがキャンセルされた場合に通知を送信する電子メールアドレスを指定する

>[!NOTE]
>
> レポートを保存した後は、宛先のタイプを変更できません。

**[!UICONTROL Email]:** （メールの宛先のタイプのみ）アドレスごとに、アドレスを入力し、 **+**.

**[!UICONTROL Destination Name]:** （S3、FTP、sFTP および FTP SSL の宛先タイプのみ）カスタムレポートが送信されるレポート宛先の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. クリック **新しい宛先を追加**.

   1. を入力 [レポートの宛先設定](/help/dsp/reports/report-destinations/report-destination-settings.md)を選択し、 **保存**.

   1. レポート設定に戻り、 **宛先名の更新。**

      これで、既存の宛先のリストから新しい宛先を使用できるようになり、オプションでレポートに追加できます。

**[!UICONTROL Frequency]:** （各 [!UICONTROL Destination Name]）レポートを宛先に送信する頻度： *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*、または *[!UICONTROL Monthly]*.

**[!UICONTROL Start Day]:** （各 [!UICONTROL Destination Name] （を使用） [!UICONTROL Frequency] 件中 *[!UICONTROL Weekly]* または *[!UICONTROL Monthly]*）レポートを生成する日。 週別レポートの場合は、曜日を選択します。 月次レポートの場合は、月の特定の日付を選択します。

## [!UICONTROL Save Report] セクション

**[!UICONTROL When to Generate]:** レポートを生成するタイミング： *[!UICONTROL On Schedule]* または *[!UICONTROL Run Now]*. 予定レポートは、アカウントのタイムゾーンで 09:00 までに配信されます。

**[!UICONTROL End Date]:** レポートの有効期限（最大 4 か月後まで可能）。 レポートの有効期限が切れる前に、指定したすべてのメール受信者は、有効期限の 7 日前と 1 日前にメールアラートを受け取ります。 レポートを長く保持するには、レポート設定で有効期限を変更します。

>[!NOTE]
>
>次のことができます [カスタムレポートはいつでも実行できます](report-run-now.md) から [!UICONTROL Reports] 表示。

>[!MORELIKETHIS]
>
>* [カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [カスタムレポートの作成](/help/dsp/reports/report-create.md)
>* [カスタムレポートの複製](/help/dsp/reports/report-copy.md)
>* [カスタムレポートの編集](/help/dsp/reports/report-edit.md)
>* [カスタムレポートの実行](/help/dsp/reports/report-run-now.md)
>* [カスタムレポートの設定](/help/dsp/reports/report-settings.md)
>* [レポートの宛先について](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
