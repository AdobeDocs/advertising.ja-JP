---
title: '[!UICONTROL Keyword Assist Report]'
description: 詳しくは、 [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
feature: Search Reports, Search Assist Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# The [!UICONTROL Keyword Assist Report]

*検索、ソーシャル、コマースのクリック追跡およびAdobe Advertising、Adobe Analytics( [!DNL Analytics] 統合 )、またはトークン (`ef_id`) のみ*

The [!UICONTROL Keyword Assist Report] クリックを引き起こすキーワードまたは配置を示します。 このレポートは、コンバージョンパスでクリックを受け取った有料検索キーワードまたはプレースメントの各パターンを示し、そのパターンが全体的なコンバージョンにどのように貢献したかを示します。 例えば、ユーザーがキーワード検索で「革靴」を検索した広告を最初にクリックし、キーワード検索で広告をクリックして注文した場合に、コンバージョンが何回発生したかを確認できます。

レポートの結果には、広告主のクリックルックバックウィンドウとインプレッションのルックバックウィンドウ内で発生したコンバージョンパスでの最も早い有料検索キーワードまたは配置クリック数に関する集計データが含まれます。 例えば、パスサイズを 5(5) に選択した場合、レポートは、クリックを受け取った最も古い 5 つのキーワードまたはプレースメントを含むコンバージョンパスで構成され、クリックのパターンごとに 1 行が追跡されます。 各行には、（最後のキーワードが指定されたパスサイズの外にある場合でも）コンバージョンにつながった最後のキーワードまたは配置の最初のキーワードまたは配置が含まれます。 デフォルトでは、行はパス内のイベント数の昇順に表示されます。

>[!NOTE]
>
>レポートにコンテンツ対応検索キャンペーン（キーワードを除く）のプレースメントが含まれる場合、 [!UICONTROL Keyword] 列には、該当する広告グループ名が表示されます (「(adgroup content) 広告グループ名」など )。

オプションで、各行の集計コンバージョンデータを含めることができます。 レポートにコンバージョン/売上高の列を含めると、各コンバージョンタイプは 4 つの列で表され、a) コンバージョンの合計数、b) そのキーワードパターンに属するコンバージョン全体の割合、c) 最初のイベントからコンバージョンまでの日数の平均待ち時間、d) コンバージョンパスに指定したパスサイズを超えるキーワードが含まれる場合、レポートには、高いキーワード数（6 つのキーワードをクリックしたすべてのパターンなど）によるコンバージョンのデータを集計した追加の行が含まれます。

過去 18 ヶ月のデータを表示できます。

## 使用可能な列

次に、各レポートで使用できる列を示します。 デフォルトの列は、デフォルトで自動的に含まれます。 使用可能なカスタム列は、レポート設定の「列」セクションから追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] から [!UICONTROL 5th Keyword] | デフォルト | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j).<br><br><b>注意：</b> レポートに（キーワードを含まない）コンテンツ対応検索キャンペーンのプレースメントが含まれる場合、これらの列には、「(adgroup content) お使いの広告グループ名」など、該当する広告グループ名が表示されます。 |
| [!UICONTROL Path Size] | デフォルト | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | デフォルト | コンバージョンパス内の最初のキーワードまたは配置。 |
| [!UICONTROL Last Keyword] | デフォルト | （最後のキーワードが指定されたパスサイズの外にある場合でも）コンバージョンにつながった最後のキーワードまたは配置。 |
| \[ 広告主固有のカスタム（派生）指標\] | カスタム | 作成した、既存の指標から計算されたカスタム指標の値。 |
| \[ 広告主固有のトランザクションプロパティ\] | カスタム | 指定したトランザクションプロパティまたはサイトエンゲージメント指標に対するコンバージョンの数。 |
| [!UICONTROL % of Total] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、含まれる各トランザクションプロパティのレポート出力に自動的に含まれます）ポートフォリオ全体のコンバージョンのうち、キーワードや配置パターンに関連付けられた割合。 |
| [!UICONTROL 6th Keyword] から [!UICONTROL 10th Keyword] | カスタム | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j).<br><br><b>注意：</b> レポートに（キーワードを含まない）コンテンツ対応検索キャンペーンのプレースメントが含まれる場合、これらの列には、「(adgroup content) お使いの広告グループ名」など、該当する広告グループ名が表示されます。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、含まれる各トランザクションプロパティのレポート出力に自動的に含まれます）最初のイベント（最初のキーワードまたは配置）からコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）前回のイベント（最後のキーワードまたは配置）からコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Path Frequency] | カスタム | この行のパスが変換前に発生した回数。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [アシストレポートについて](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [レポート設定の支援](assist-report-settings.md)
>* [アシストレポートの生成](assist-report-generate.md)
