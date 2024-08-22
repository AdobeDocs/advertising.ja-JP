---
title: スプレッドシートを使用したパッケージ設定の確認と編集
description: スプレッドシートを使用して主要なパッケージ設定を確認および編集する方法を説明します。
feature: DSP Packages
source-git-commit: ad00092c4ef5d44c364ab0593826220054f715c3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# スプレッドシートを使用したパッケージ設定の確認と編集

1 つ以上のパッケージの設定を XLSX （[!DNL Microsoft Excel] スプレッドシート）形式でダウンロードして確認できます。 スプレッドシートには、フライト情報を含む別のタブが含まれています。 その後、両方のタブのフィールドを選択して変更を加え、データを一度にDSPにアップロードできます。 編集可能なフィールドには、通常は編集可能なほとんどの設定が含まれています。

>[!TIP]
>
>1 つ以上のパッケージの複数のフィールドを編集するには、「[ パッケージの編集 ](/help/dsp/campaign-management/packages/package-edit.md) を参照してください。

## 1 つ以上のパッケージのダウンロード設定

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Packages]** をクリックします。

1. 設定をダウンロードする各パッケージの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Download Edit in Excel Sheet]** をクリックします。

ファイルはブラウザーのダウンロードフォルダーに自動的に保存されます。 含まれる列のリストについては、「[ ダウンロードまたはアップロードされたスプレッドシートの列をパッケージ化 ](#qa-sheet-columns-packages)」を参照してください。

## 1 つ以上のパッケージの設定をアップロード

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Packages]** をクリックします。

1. 設定をアップロードする各パッケージの横にあるチェックボックスを選択します。

1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Upload Edit in Excel Sheet]** をクリックします。

1. [!UICONTROL Edit in Excel] ダイアログで、次の手順を実行します。

   1. ファイルをボックスにドラッグ&amp;ドロップするか、ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. 「**[!UICONTROL Upload]**」をクリックします。

1. （オプション）更新が処理されたことを確認するには、上部のメニューバーの右側にある ![ ジョブ ](/help/dsp/assets/downloads.png) をクリックします。

## ダウンロードまたはアップロードされたスプレッドシートのパッケージ設定列{#qa-sheet-columns-packages}

>[!TIP]
>
> ダウンロードしたスプレッドシートでは、編集可能なすべての列が青でハイライト表示されます。

### 「[!UICONTROL Package]」タブ

| セクション | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | パッケージの数値 ID。 | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | パッケージの名前。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL Status] | パッケージのステータス：*[!UICONTROL active]* または *[!UICONTROL inactive]*。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL Description] | パッケージの説明（オプション）。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | 静的なサードパーティの料金レートで、1,000 インプレッション数あたり請求不可コストとしてトラッキングされます（該当する場合）。 | はい |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | サードパーティの料金レートのオプション説明（該当する場合）。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | パッケージの開始日。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | パッケージの終了日。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | パッケージ内のプレースメントのペースとキャップを設定するレベル（*[!UICONTROL Package]* または *[!UICONTROL Placement]*）。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | パッケージ予算。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | 予算間隔：&lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*、*[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | オプションの予算間隔キャップ。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | オプションの予算間隔の上限の間隔：&lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*、または *[!UICONTROL All Time]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | パッケージの目的。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | 目標のターゲット値。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | （「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ） [ カスタム目標 ](/help/dsp/optimization/custom-goal.md)。CPA または ROAS 指標の計算に使用される収益またはコンバージョンイベントが含まれます。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | （オプション、「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ）広告費用対効果または獲得あたりのコストの計算に使用する最終的なコンバージョンイベントまたは収益イベント/販売額。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | （カスタムの最適化目標を持つパッケージのみ） パッケージの目的。パッケージの最適化方法（*[!UICONTROL Prospecting]*、*[!UICONTROL Retargeting]*、*[!UICONTROL Other]*）を決定するのに役立ちます。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | （カスタム最適化目標を持つパッケージのみ）履歴データがパッケージを最適化するための入力として使用される、別のパッケージのパッケージ ID。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | （カスタム最適化目標を持つパッケージのみ）パッケージを最適化するための入力として履歴データが使用される別のパッケージ。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | パッケージが *[!UICONTROL budget]* または *[!UICONTROL primary_goal]* に向かってペーシングされているかどうか（インプレッション数）。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | （インプレッション数でパッケージのペースを調整する場合）指定した期間内のインプレッション数の目標値。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | （インプレッション数でパッケージのペースを調整する場合）目標インプレッション数の時間間隔。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | パッケージのフライトペーシング戦略：*[!UICONTROL Even]*、*[!UICONTROL slightly ahead]*、*[!UICONTROL frontload]*、*[!UICONTROL aggressive frontload]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | パッケージの日中ペーシング戦略：*[!UICONTROL Even]* または *[!UICONTROL ASAP]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | 指定した [!UICONTROL Frequency Cap Interval] 間のパッケージのプライマリ周波数キャップ。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | プライマリ周波数キャップの間隔：*[!UICONTROL Day]*、*[!UICONTROL Week]* または *[!UICONTROL Month]*。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | プライマリ [!UICONTROL Frequency Cap] が適用される週、日、時間または分。 例えば、プライマリキャップが 1 か月あたりのインプレッション数 12 の場合、この値は `12` になります。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | 指定された [!UICONTROL Secondary Frequency Cap Interval] 間のパッケージのセカンダリ周波数キャップ | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | 2 番目のフリークエンシーキャップの間隔の種類：*[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*、または *[!UICONTROL Minute]*。 該当する週、日、時間、分の数は、[!UICONTROL Secondary Frequency Cap Interval Value] で示されます。 | はい |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap] が適用される週、日、時間または分。 例えば、セカンダリキャップが 6 時間あたり 3 つのインプレッションである場合、この値は `6` になります。 | はい |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | package *T* （true）または *F* （false）に対して均等ではないペーシングフライトを作成するかどうかを指定します。 カスタムライティングを有効にしてパッケージを保存すると、カスタムライティングを無効にしたり、パッケージの開始日を編集したりできなくなります。 | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | （[!UICONTROL Activate Custom Flighting] のオプションが有効な場合にのみ使用可能）前のフライトの残りの予算を次のフライトの既存の予算に自動的に追加するかどうかを示します。*T* （true）または *F* （false）。 | はい |
| [!UICONTROL Error] | [!UICONTROL Error] | 関連するエラー。 | — |

### 「[!UICONTROL Package_Flights]」タブ

| セクション | 列 | 説明 | 編集可能？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | パッケージの数値 ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | フライトの数値 ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | フライトの最初の日付。 | はい |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | フライトの最終日。 | はい |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | フライトのターゲット支出目標。 | はい |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | （「[!UICONTROL Automatically rollover remaining flight budget to next flight]」オプションが有効になっていない既存のパッケージ）次のフライトに追加する、費やされていない可能性のある予算。 | はい |

>[!MORELIKETHIS]
>
>* [ パッケージの編集 ](/help/dsp/campaign-management/packages/package-edit.md)
>* [ パッケージ設定 ](/help/dsp/campaign-management/packages/package-settings.md)
