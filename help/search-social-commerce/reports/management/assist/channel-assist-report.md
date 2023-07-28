---
title: '[!UICONTROL Channel Assist Report]'
description: 詳しくは、 [!UICONTROL Channel Assist Report].
exl-id: 49616327-72e9-49c6-90b9-91c7486e8417
feature: Search Reports, Search Assist Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# The [!UICONTROL Channel Assist Report]

*検索、ソーシャル、コマースのクリック追跡およびAdobe Advertising、Adobe Analytics( [!DNL Analytics] 統合 )、またはトークン (`ef_id`) のみ*

The [!UICONTROL Channel Assist Report] 様々なマーケティングチャネル ( 検索、Social、およびコマースからの検索またはソーシャル、Advertising DSPからの表示またはビデオ ) がコンバージョンプロセスをどのように支援したかを示します。 このレポートは、1 つ以上のコンバージョンにつながった各イベントタイプのパターンが、全体的なコンバージョンにどのように貢献したかを示します。 例えば、ユーザーが最初にディスプレイ広告のインプレッションを見てから検索広告をクリックして注文したときにコンバージョンが何回発生したか、または、ユーザーが 10 回を超える広告とやり取りした後にコンバージョンが何回発生したかを確認できます。 イベントタイプには、検索クリック数、表示インプレッション数とクリック数、ビデオインプレッション数とクリック数、その他のインプレッション数とその他のクリック数が含まれます。 <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

レポートの結果には、広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). 例えば、パスサイズを 5(5) に選択した場合、レポートには最も早い 5 つのイベントを含むコンバージョンパスが表示され、各イベントタイプのパターンに対して 1 行が追跡されます（「検索クリック」、「インプレッションを表示」など）。 各行には、（最後のイベントが指定されたパスサイズの外にある場合でも）パスの最初のイベントと、コンバージョンにつながった最後のイベントを含む、1 つのイベントパターンが表示されます。 デフォルトでは、行はパス内のイベント数の昇順に表示されます。

オプションで、各行の集計コンバージョンデータを含めることができます。 レポートにコンバージョン/売上高の列を含めると、各コンバージョンタイプが 4 つの列で表され、a) コンバージョンの合計数、b) そのイベントパターンに属するコンバージョン全体の割合、c) 最初のイベントからコンバージョンまでの 1 日の平均待ち時間、d) コンバージョンパスに指定したパスサイズを超えるイベントが含まれる場合、レポートには、より多くのイベント数（6 つのイベントタイプを含むすべてのパターンなど）によって生じたコンバージョンのデータを集計した追加の行が含まれます。

過去 18 ヶ月のデータを表示できます。

## 使用可能な列

次に、各レポートで使用できる列を示します。 デフォルトの列は、デフォルトで自動的に含まれます。 使用可能なカスタム列は、レポート設定の「列」セクションから追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] から [!UICONTROL 5th Event] | デフォルト | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | デフォルト | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | デフォルト | コンバージョンパスの最初（最も古い）イベントのイベントタイプ。 |
| [!UICONTROL Last Event Type] | デフォルト | コンバージョンにつながった最後のイベントのイベントタイプ（最後のイベントが指定されたパスサイズの外にある場合も含む）。 |
| \[ 広告主固有のカスタム（派生）指標\] | カスタム | 作成した、既存の指標から計算されたカスタム指標の値。 |
| \[ 広告主固有のトランザクションプロパティ\] | カスタム | 指定したトランザクションプロパティまたはサイトエンゲージメント指標に対するコンバージョンの数。 |
| [!UICONTROL % of Total] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、含まれる各トランザクションプロパティのレポート出力に自動的に含まれます）ポートフォリオ全体のコンバージョンのうち、イベントパターンに起因する割合。 |
| [!UICONTROL 6th Event] から [!UICONTROL 30th Event] | カスタム | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、含まれる各トランザクションプロパティのレポート出力に自動的に含まれます）最初のイベントからコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベントからコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Path Frequency] | カスタム | この行のパスが変換前に発生した回数。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [アシストレポートについて](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [レポート設定の支援](assist-report-settings.md)
>* [アシストレポートの生成](assist-report-generate.md)
