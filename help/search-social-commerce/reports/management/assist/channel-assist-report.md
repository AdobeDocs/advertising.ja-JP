---
title: '[!UICONTROL Channel Assist Report]'
description: '[!UICONTROL Channel Assist Report] について説明します。'
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# [!UICONTROL Channel Assist Report]

*検索、ソーシャル、Commerceのクリックのトラッキングと、Adobe Advertising、Adobe Analyticsからのコンバージョントラッキング（[!DNL Analytics] 統合を使用）またはフィードでトークン（`ef_id`）のみを使用して提供される広告主*

[!UICONTROL Channel Assist Report] は、様々なマーケティングチャネル（検索、ソーシャル、Commerceからの検索やソーシャル、Advertising DSPからのディスプレイやビデオ）がコンバージョンプロセスにどのように役立ったかを示します。 このレポートには、1 つ以上のコンバージョンに至ったイベントタイプの各パターンが、全体的なコンバージョンにどのように貢献したかが表示されます。 例えば、ユーザーがディスプレイ広告のインプレッションを初めて表示し、検索広告をクリックして、注文した際に発生したコンバージョン数を確認できます。または、ユーザーが 10 を超える広告を操作した後に発生したコンバージョン数を確認できます。 イベントタイプには、検索クリック数、表示インプレッション数およびクリック数、ビデオインプレッション数およびクリック数、その他のインプレッション数およびその他のクリック数が含まれます。<!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

レポート結果には、広告主の [&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d) および [&#x200B; インプレッションルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j) 内で発生した、コンバージョンパスのイベントタイプのパターンごとに（最も古い N 個のイベントタイプまで）集計データが含まれます。 例えば、パスサイズを 5 に設定した場合、レポートには最大 5 つの最も古いイベントを含むコンバージョンパスが含まれ、追跡されるイベントタイプのパターン（「検索クリック」に続いて「インプレッションを表示」など）ごとに 1 行が含まれます。 各行には、パスの最初のイベントと、（最後のイベントが指定されたパスサイズ外であった場合でも）コンバージョンを発生させた最後のイベントを含め、イベントのパターンが 1 つ表示されます。 デフォルトでは、行はパス内のイベント数の昇順になります。

オプションで、各行にコンバージョンデータを集計を含めることができます。 レポートにコンバージョン/売上高の列を含めると、各コンバージョンタイプは 4 つの列で表され、a） コンバージョンの合計数、b）そのイベントパターンに起因するコンバージョン全体の割合、c）最初のイベントからコンバージョンまでの平均待ち時間（日）、および d）最後のイベントからコンバージョンまでの平均待ち時間（日）を示します。 コンバージョンパスに指定したパスサイズを超えるイベントが含まれている場合、レポートには、多数のイベント（6 つのイベントタイプを含むすべてのパターンなど）から生成されたコンバージョンのデータを集計した追加の行が含まれます。

過去 18 か月のデータを表示できます。

## 使用可能な列

各レポートで使用できる列は次のとおりです。 デフォルトの列は、デフォルトで自動的に含まれます。 レポート設定の「列」セクションから、使用可能なカスタム列を追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] ～ [!UICONTROL 5th Event] | デフォルト | 広告主の [&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d) および [&#x200B; インプレッションルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j) 内で発生したコンバージョンパスの 5 つの最も古いイベントタイプ。 |
| [!UICONTROL Path Size] | デフォルト | 広告主の [&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d) および [&#x200B; インプレッションルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j) 内で発生したコンバージョンパスのイベントタイプの数。 |
| [!UICONTROL First Event Type] | デフォルト | コンバージョンパスの最初（最も古い）のイベントのイベントタイプ。 |
| [!UICONTROL Last Event Type] | デフォルト | コンバージョンに至った最後のイベントのイベントタイプ （最後のイベントが、指定されたパスサイズを超えている場合も含む）。 |
| \[ 広告主固有のカスタム （派生）指標\] | カスタム | 既存の指標から計算された、作成したカスタム指標の値。 |
| \[ 広告主固有のコンバージョン指標\] | カスタム | 指定したコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| [!UICONTROL % of Total] \[ コンバージョン指標\] | 自動 | （レポート設定では利用できませんが、含まれる各コンバージョン指標のレポート出力には自動的に含まれます） イベントパターンに起因したポートフォリオ全体のコンバージョンの割合。 |
| [!UICONTROL 6th Event] ～ [!UICONTROL 30th Event] | カスタム | 広告主の [&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d) および [&#x200B; インプレッションルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j) 内で発生したコンバージョンパスの 6 ～ 30 番目のイベントタイプ。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[ コンバージョン指標\] | 自動 | （レポート設定では利用できませんが、各コンバージョン指標のレポート出力に自動的に含まれます）最初のイベントからコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[ コンバージョン指標\] | 自動 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベントからコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Path Frequency] | カスタム | 変換前にこの行のパスが発生した回数。 |

>[!MORELIKETHIS]
>
>* [&#x200B; アシストレポートについて &#x200B;](assist-report-about.md)
>* [[!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [[!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [&#x200B; レポート設定の支援 &#x200B;](assist-report-settings.md)
>* [&#x200B; アシストレポートの生成 &#x200B;](assist-report-generate.md)
