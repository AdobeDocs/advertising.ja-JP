---
title: バルクシートを使用したパッケージ設定のレビューと編集
description: スプレッドシートを使用して、主要なパッケージ設定を一括で確認および編集する方法について説明します。
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Bulksheets を使用したパッケージ設定のレビューと編集

確認のために、XLSX ([!DNL Microsoft Excel] スプレッドシート) の 1 つ以上のパッケージの設定を形式ダウンロードするできます。 スプレッドシートには、フライト情報を含む別のタブが含まれています。

複数の設定を一度に更新するには、次のいずれかを実行します。

* フィールドの選択を変更し、ファイルを保存し、編集したバルクシートファイルをDSPにアップロードして戻します。

* 追加のパッケージや、任意のプレースメントまたは広告の設定を変更するには、キャンペーンコンポーネントのタイプごとにタブが含まれている空のバルクシートテンプレートをダウンロードするか、新しい設定または更新された設定を入力またはテンプレートファイルに貼り付けてから、ファイルをアップロードして変更を行います。 手順については、「[ バルクシートを使用した Campaign コンポーネント設定の確認と編集 ](/help/dsp/campaign-management/campaign-components-review-edit.md) を参照してください。

編集可能なフィールドには、通常は編集可能なほとんどの設定が含まれています。

>[!TIP]
>
>1 つ以上のパッケージの複数のフィールドをすばやく編集するには、「[ パッケージの編集 ](/help/dsp/campaign-management/packages/package-edit.md) を参照してください。

## キャンペーン内のすべてのパッケージの設定をダウンロード

キャンペーン内のすべてのパッケージの設定をダウンロードする場合、スプレッドシートにはパッケージ設定とフライト情報について別々のタブが含まれます。 オプションで、パッケージに関連付けられるプレースメントおよび広告の設定を含めることができます。プレースメントおよび広告設定用の追加のタブも含まれます。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. 右上で、**[!UICONTROL ...]**/**[!UICONTROL Download QA sheet]** をクリックします。

1. [!UICONTROL QA Sheet Download]ダイアログボックスで、ダウンロードしたファイルから設定を除外するキャンペーンコンポーネントの選択を解除し、「**[!UICONTROL Download]**」をクリックします。

デフォルトでは、パッケージに関連付けられているすべての配置と広告の設定が選択されています。

通知メッセージが表示され、ファイルがダウンロードするできるようになるタイミングが示されます。

1. ファイルダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある **[!UICONTROL Download]** をクリックします。

     ファイルはブラウザーの ダウンロード フォルダーに保存されます。 含まれる列のリストについては、「[ダウンロード/アップロードされたスプレッドシートの配置列](#qa-sheet-columns)」を参照してください。

>[!NOTE]
>
>キャンペーンレベルの QA シートを編集して再度アップロードすることはできません。 これらのファイルの campaign コンポーネント設定を変更するには、個別のバルクシートテンプレートをダウンロードし、QA シートからバルクシートテンプレートに行を入力または貼り付けてファイルを保存し、入力されたバルクシートをアップロードします。 手順については、「[ バルクシートを使用した Campaign コンポーネント設定の確認と編集 ](/help/dsp/campaign-management/campaign-components-review-edit.md) を参照してください。

## 1 つ以上のパッケージのダウンロード設定

特定のパッケージの設定ダウンロードする場合、バルクシート ファイルにはパッケージ設定用とフライト情報用の個別のタブが含まれ、ファイルは編集可能です。

1. メインメニューで、「 **[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、「 **[!UICONTROL Packages]**」をクリックします。

1. バルクアクションツールバーで、「 **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**」をクリックします。

   通知メッセージは、バルクシートファイルがいつダウンロードする可能になるかを示します。

1. バルクシートをダウンロードするには、次のいずれかの操作を行います。

   * 通知メッセージで、「**[!UICONTROL Download].**」をクリックします。

   * 上部のメニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。 ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

     ファイルはブラウザーのダウンロードフォルダーに保存されます。 含まれる列のリストについては、[ ダウンロードまたはアップロードされたスプレッドシートのプレースメント列 ](#qa-sheet-columns)」を参照してください。

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## パッケージ設定を含むバルクシートのアップロード {#upload-bulksheet-package}

パッケージの設定（パッケージに関連付けられたプレースメントや広告など）をバルクシートファイルにアップロードできます。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. 右上で、**[!UICONTROL ...]**/**[!UICONTROL Upload Bulksheet]** をクリックします。

1. [!UICONTROL Upload Bulksheet] ダイアログで、次の手順を実行します。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. [ **[!UICONTROL Upload]**] をクリックします。

1. (オプション)更新が処理されたことを確認するには、上部のメニュー バーの右側にある [ ![ジョブ](/help/dsp/assets/downloads.png) をクリックします。

## ダウンロード/アップロードされたスプレッドシートでのパッケージ設定列{#qa-sheet-columns-packages}

>[!TIP]
>
> ダウンロードしたスプレッドシートでは、編集可能なすべての列が青色で強調表示されます。

### 「[!UICONTROL Package]」タブ

| セクション | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | パッケージの数値 ID。 | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | パッケージの名前。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL Status] | パッケージのステータス：*[!UICONTROL active]* または *[!UICONTROL inactive]*。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL Description] | パッケージの説明（オプション）。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | 該当する場合、1,000 インプレッションあたりの請求対象外のコストとして追跡される、静的なサードパーティ手数料率。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | サードパーティ手数料率に関するオプションの説明(該当する場合)。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | パッケージの開始日。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | パッケージの終了日。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | パッケージ内のプレースメントのペースとキャップを設定するレベル（*[!UICONTROL Package]* または *[!UICONTROL Placement]*）。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | パッケージ予算。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | 予算間隔：&lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*、*[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | オプションの予算間隔キャップ。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | オプションの予算間隔キャップの間隔: &lt;i[!UICONTROL >Daily]*、 *[!UICONTROL Weekly]*、 *[!UICONTROL Monthly]*&#x200B;または *[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | パッケージの目的。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | 目標のターゲット値。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | （「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ） [ カスタム目標 ](/help/dsp/optimization/custom-goal.md)。CPA または ROAS 指標の計算に使用される収益またはコンバージョンイベントが含まれます。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | （オプション、「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ）広告費用対効果または獲得あたりのコストの計算に使用する最終的なコンバージョンイベントまたは収益イベント/販売額。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (カスタム最適化目標を持つパッケージのみ)パッケージの目的。パッケージの最適化方法を決定します。 *[!UICONTROL Prospecting]*、 *[!UICONTROL Retargeting]*&#x200B;または *[!UICONTROL Other]* 。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (カスタム最適化目標を持つパッケージのみ)パッケージを最適化するための入力として履歴データを使用する別のパッケージのパッケージ ID。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (カスタム最適化目標を持つパッケージのみ)パッケージを最適化するための入力として履歴データが使用される別のパッケージ。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | パッケージが *[!UICONTROL budget]* または *[!UICONTROL primary_goal]* に向かってペーシングされているかどうか（インプレッション数）。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | （インプレッション数でパッケージのペースを調整する場合）指定した期間内のインプレッション数の目標値。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | （インプレッション数でパッケージのペースを調整する場合）目標インプレッション数の時間間隔。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | パッケージのフライトペーシング戦略: *[!UICONTROL Even]*、 *[!UICONTROL slightly ahead]*、 *[!UICONTROL frontload]*&#x200B;または *[!UICONTROL aggressive frontload]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | パッケージの日中ペーシング戦略：*[!UICONTROL Even]* または *[!UICONTROL ASAP]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | 指定した [!UICONTROL Frequency Cap Interval] 間のパッケージのプライマリ周波数キャップ。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | プライマリ頻度キャップの間隔: *[!UICONTROL Day]*、 *[!UICONTROL Week]*&#x200B;または *[!UICONTROL Month]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | プライマリ [!UICONTROL Frequency Cap] を適用する週数、日数、時間数または分数。 たとえば、プライマリキャップが 1 か月あたり 12 インプレッションの場合、この値は `12` になります。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | 指定された [!UICONTROL Secondary Frequency Cap Interval] 間のパッケージのセカンダリ周波数キャップ | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | 2 番目のフリークエンシーキャップの間隔の種類：*[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*、または *[!UICONTROL Minute]*。 該当する週、日、時間、分の数は、[!UICONTROL Secondary Frequency Cap Interval Value] で示されます。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap] が適用される週、日、時間または分。 例えば、セカンダリキャップが 6 時間あたり 3 つのインプレッションである場合、この値は `6` になります。 | はい |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | package *T* （true）または *F* （false）に対して均等ではないペーシングフライトを作成するかどうかを指定します。 カスタムライティングを有効にしてパッケージを保存すると、カスタムライティングを無効にしたり、パッケージの開始日を編集したりできなくなります。 | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | （[!UICONTROL Activate Custom Flighting] のオプションが有効な場合にのみ使用可能）前のフライトの残りの予算を次のフライトの既存の予算に自動的に追加するかどうかを示します。*T* （true）または *F* （false）。 | はい |
| [!UICONTROL Error] | [!UICONTROL Error] | 関連するエラー。 | — |

### [!UICONTROL Package_Flights] タブ {#qa-sheet-columns-package-flights}

| 節 | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | パッケージの数値 ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | フライトの数値 ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | フライトの最初の日付。 | はい |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | フライトの最終日。 | はい |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | そのフライトのご利用ターゲット目標。 | はい |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (「[!UICONTROL Automatically rollover remaining flight budget to next flight]」オプションが有効になっていない既存のパッケージ)次のフライトに追加する未使用の可能性のある予算額。 | はい |

>[!MORELIKETHIS]
>
>* [ バルクシートを使用した Campaign コンポーネント設定のレビューと編集 ](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [ パッケージの編集 ](/help/dsp/campaign-management/packages/package-edit.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
