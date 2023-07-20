---
title: カスタムレポート設定
description: カスタムレポート設定の説明を参照してください。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 54e60a47c54eaac687fd0b385a94b25818b66b71
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# カスタムレポート設定

**[!UICONTROL Name]** レポート名。 最大長は 180 文字です。

**[!UICONTROL Report Type]** レポートのタイプ： *[!UICONTROL Custom]* （利用可能な最も多くのオプションを含む） *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*&#x200B;または *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] セクション

**[!UICONTROL Timezone]:** レポートのタイムゾーン。

**[!UICONTROL Observe Daylight Savings Time]:** 報告された時間で夏時間を考慮します。

**\[ 日付範囲\]:** データを生成する日付範囲。 使用できる日数は、レポートおよび選択したディメンションによって異なります。 次のいずれかを選択します。

* **[!UICONTROL Previous N days]:** 今日までの特定の日数のデータが含まれます。

* **[!UICONTROL Custom]:** 特定の開始日と終了日の間のデータが含まれます。 前日までのデータをレポートする場合は、 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** 前月のデータが含まれます。

**[!UICONTROL Add Filters]:** （オプション）ディメンションがレポートの列として含まれているかどうかに関わらず、データをフィルタリングする追加のディメンション。 使用可能なフィルターは、レポートタイプによって異なり、次のものが含まれます。 *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*、および *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* は、組織が [クロスアカウントレポート](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]、および [!UICONTROL Conversion]. クロスアカウントレポートの詳細については、Adobeのアカウントチームにお問い合わせください。

1 つ以上のフィルターを適用するには、次の手順を実行します。

* ディメンションを選択し、演算子 (*次と等しい* または *等しくない*) をクリックし、適用可能な値を選択します。 例えば、プリロール広告のデータのみを返すには、「[!UICONTROL Ad Type equals Preroll].&quot;
* （オプション）フィルターに条件を追加します。
* （オプション）フィルターを追加し、それぞれに 1 つ以上の条件を設定します。

## [!UICONTROL Build Your Report] セクション

**[!UICONTROL Select To Add As Report Headers]:**  レポートに含めるデータ列（ヘッダー）。 列を追加するには、カテゴリを展開し、列名の横にあるチェックボックスをオンにします。 使用可能な列はレポートによって異なり、使用できない指標はすべて無効になっています。 使用可能なデータカテゴリは次のとおりです。

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > この [!UICONTROL Household Reach & Frequency] レポートに含めることができるディメンションは 1 つだけです。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >この [!UICONTROL Household Reach & Frequency] レポートには、重複指標または重複しない指標のどちらか一方のみが含まれます。

* [!UICONTROL Conversion Metrics] （広告主別に並べ替え）

* [!UICONTROL Custom Goals] （広告主別に並べ替え）

参照：[使用可能なレポート列](report-columns.md)」を参照してください。

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列ヘッダーの順序。 任意の列をドラッグ&amp;ドロップして順序をカスタマイズできます。

**[!UICONTROL Format]:** でレポートを生成するかどうか *[!UICONTROL CSV]* （コンマ区切り値）または *[!UICONTROL Tab]* （タブ区切り値）形式を使用します。

**[!UICONTROL Headers]:** 次を実行するかどうか *[!UICONTROL Include]* または *[!UICONTROL Do Not Include]* 列ヘッダー。

## [!UICONTROL Multi-Touch Conversion Options] セクション

**[!UICONTROL Attribution Rule Settings]:** 設定は、レポートタイプによって異なります。

* **\[ 属性タイプ\]:** ([!UICONTROL Household Conversion] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列；(Adobe Advertisingコンバージョントラッキングのみ ) レポート内で、コンバージョンにつながる一連のイベント内のコンバージョンデータを関連付ける方法を次のように指定します。

   * *[!UICONTROL Unique]:* （デフォルト）ディメンション値（デバイスや配置など）がコンバージョンへのパス上にあった回数をカウントします。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:*  コンバージョンへのパスでのディメンション値（デバイスや配置など）の発生頻度に基づいて、各コンバージョンのクレジットを配分します。 例えば、コンバージョン前に合計 10 件のインプレッションがあり、CTV で 8 件、モバイルで 2 件があった場合、クレジットの 80%(0.8) が CTV 画面に、0.2 がモバイルに割り当てられます。

* **\[ ルールタイプ\]:** ( すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]、および [!UICONTROL Site] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列；Adobe Advertisingコンバージョントラッキングのみを使用する広告主 ) レポート内で、コンバージョンにつながる一連のイベントにコンバージョンデータを関連付ける方法を説明します。 ルール間の違いを比較する場合は、複数のルールを選択できます。

  >[!NOTE]
  >
  >コンバージョンパスには、広告主のインプレッションまたはクリックのルックバックウィンドウ内のインプレッション数およびクリック数が含まれます。これらは、 [!DNL Advertising Search, Social, & Commerce]. コンバージョン属性中のインプレッション数よりも、クリック数の方が優先されます。 コンバージョンパス内のクリックは、アトリビューションルールに基づいてフルクレジットを受け取ります。 インプレッションは、コンバージョンパスでクリックが追跡されない場合にのみクレジットを受け取ります。

   * *[!UICONTROL Last Event]:* コンバージョンパスの最後のクリックまたはインプレッションにコンバージョンを関連付けます。

   * *[!UICONTROL Weight Last More]:* コンバージョンパス内のすべてのイベントに対してコンバージョンを属性付けますが、最後のイベントに対して最も大きな重み付けを与え、前のイベントに対する重み付けを徐々に小さくします。

   * *[!UICONTROL Even Distribution]:* コンバージョンを、コンバージョンパスの各イベントに等しく関連付けます。

   * *[!UICONTROL Weight First More]:* コンバージョンパス内のすべてのイベントに対してコンバージョンを関連付けますが、最初のイベントに対して最も重み付けが適用され、次のイベントに対しては引き続き重み付けが少なくなります。

   * *[!UICONTROL First Event]:* コンバージョンパスの最初のクリックまたはインプレッションにコンバージョンを関連付けます。

   * *[!UICONTROL U-shaped]:* コンバージョンパス内のすべてのイベントにコンバージョンをアトリビュートしますが、最初と最後のイベントに最も重み付けを適用し、コンバージョンパスの途中にあるイベントに対する重み付けを徐々に軽減します。

   * *[!UICONTROL Display Only]:*  コンバージョンパスの最後のDSPクリックまたはインプレッションにコンバージョンを関連付けます。 これには、ビデオおよび接続されたテレビ広告が含まれ、クリック数は除外されます。 [!DNL Advertising Search, Social, & Commerce] 広告。

   * *[!UICONTROL Social Only]:* 廃止

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **ルックバック：** ([!UICONTROL Household Conversion] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列；Adobe Advertisingコンバージョンを追跡している広告主のみ ) レポート内で、コンバージョンイベントを発生させるインプレッションイベントの後の最大日数。 デフォルトはです。 *[!UICONTROL 30 days]*&#x200B;の場合、最大の日数は 92 日です。

**[!UICONTROL Paths as Columns]:**  ( すべて [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]、および [!UICONTROL Site] レポート [!UICONTROL Conversion Metrics] または [!UICONTROL Custom Goals] 列 ) 同じデバイスで以前のイベントが発生した場合にレポートするコンバージョンのタイプ。 最大 3 つのタイプを含めることができます。 選択したタイプごとに、各コンバージョン指標に対して個別の列が追加され、指定したサフィックス ([!UICONTROL (tl)], [!UICONTROL (ct)]または [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* クリック数（クリックスルーの場合は CT）とインプレッション数（ビュースルーの場合は VT）に起因するコンバージョンが含まれます。 インプレッションに属するコンバージョンに、指定したビュースルーの重み付けを掛けます。 デフォルトのビュースルーの重み付けは 100%です。つまり、インプレッションに起因するコンバージョンは、クリックに起因するコンバージョンの値の 100%とカウントされます。

* *[!UICONTROL With Clicks (CT)]:* クリックに起因するコンバージョンのみが含まれます。

* *[!UICONTROL Impressions Only (VT)]:* コンバージョンパスでクリックが追跡されなかったので、インプレッションに起因するコンバージョンのみが含まれます。

**[!UICONTROL Conversion Reporting Based On]:**  コンバージョンデータのレポート方法：

* *[!UICONTROL Conversion Timestamp]:* （デフォルト）コンバージョンは、コンバージョン日に関連付けられます。

* *[!UICONTROL Event Timestamp]:* コンバージョンは、指定した [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] セクション

**[!UICONTROL Destination Type]:** 次のいずれかの宛先タイプを選択します。

* *[!UICONTROL S3]:* 完了したレポートを 1 つ以上のレポートに送信するには [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) の場所 ( **[!UICONTROL Destination Name]** フィールドに入力します。
* *[!UICONTROL sFTP]:* 完了したレポートを 1 つ以上の SFTP の場所に送信する場合は、 **[!UICONTROL Destination Name]** フィールドに入力します。
* *[!UICONTROL FTP]:* 完了したレポートを 1 つ以上の FTP の場所に送信する場合は、 **[!UICONTROL Destination Name]** フィールドに入力します。
* *[!UICONTROL FTP SSL]（現在ベータ版）:* 完了したレポートを 1 つ以上の FTP SSL の場所に送信する場合は、 **[!UICONTROL Destination Name]** フィールドに入力します。
* *[!UICONTROL Email]:* エラーが原因でレポートがキャンセルされた場合に完了したレポートまたは通知を送信する電子メールアドレスを指定する。 複数のアドレスを指定する場合は、コンマまたはスペースで区切ります。

>[!NOTE]
>
> レポートを保存した後は、保存先のタイプを変更できません。

**[!UICONTROL Destination Name]:** （S3、FTP、SFTP、FTP SSL の宛先タイプのみ）カスタムレポートの送信先となるレポートの宛先の名前。

* 既存の宛先を指定するには、リストから宛先名を選択します。 複数の宛先名を個別に選択できます。

* 新しい宛先を作成するには：

   1. クリック **新しい宛先の追加**.

   1. 次を入力します。 [レポートの宛先設定](/help/dsp/reports/report-destinations/report-destination-settings.md)をクリックし、 **保存**.

   1. レポート設定に戻り、 **宛先名を更新します。**

      これで、新しい宛先が既存の宛先のリストから使用できるようになり、オプションでレポートに追加できます。

**[!UICONTROL Frequency]:** ( [!UICONTROL Destination Name] レポートを送信先に送信する頻度： *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*&#x200B;または *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] セクション

**[!UICONTROL Send & Save]:** レポートを送信するタイミング： *[!UICONTROL On Schedule]* または *[!UICONTROL Run Now]*. 予定レポートは、アカウントのタイムゾーンで 09:00 に配信されます。

>[!NOTE]
>
>以下が可能です。 [いつでもカスタムレポートを実行する](report-run-now.md) から [!UICONTROL Reports] 表示

>[!MORELIKETHIS]
>
>* [カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [カスタムレポートの作成](/help/dsp/reports/report-create.md)
>* [カスタムレポートの複製](/help/dsp/reports/report-copy.md)
>* [カスタムレポートの編集](/help/dsp/reports/report-edit.md)
>* [カスタムレポートの実行](/help/dsp/reports/report-run-now.md)
>* [カスタムレポート設定](/help/dsp/reports/report-settings.md)
>* [レポートの宛先について](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
