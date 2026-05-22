---
title: '[!UICONTROL Channel Assist Report]'
description: '[!UICONTROL Channel Assist Report]について説明します。'
feature: Search Reports, Search Assist Reports
source-git-commit: ba0f5e80168cd1d576d800e9499b07d48248a789
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# ザ [!UICONTROL Channel Assist Report]

*検索、ソーシャル、およびCommerceのクリック追跡と、Adobe AdvertisingとAdobe Analyticsのコンバージョン追跡を備えた広告主（[!DNL Analytics]統合）、またはトークン（`ef_id`）のみを使用したフィードで提供された広告主*

[!UICONTROL Channel Assist Report]は、様々なマーケティングチャネル（検索、ソーシャル、Commerceの検索またはソーシャル、Advertising DSPのディスプレイまたはビデオ）がコンバージョンのプロセスをどのように支援したかを示しています。 このレポートでは、1つ以上のコンバージョンにつながったイベントタイプの各パターンが、全体的なコンバージョンにどのように貢献しているのかを明らかにします。 例えば、ユーザーが最初にディスプレイ広告のインプレッションを見て、次に検索広告をクリックしてから注文した際にコンバージョンが発生した回数や、ユーザーが10回以上の広告を操作した後にコンバージョンが発生した回数などを確認できます。 イベントタイプには、検索クリック、表示インプレッションとクリック、動画インプレッションとクリック、その他のインプレッションと他のクリックが含まれます。<!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

レポート結果には、広告主の[ クリックのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)と[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生した、コンバージョンパスのイベントタイプの各パターン（最も古いN個のイベントタイプまで）に関する集計データが含まれます。 例えば、パスサイズを5 （5）に設定すると、レポートには、最も早い5つのイベントを含むコンバージョンパスが含まれ、追跡されるイベントタイプのパターンごとに1行が含まれます（「検索クリック」、「インプレッションを表示」など）。 各行には、パスの最初のイベントとコンバージョンの原因となった最後のイベントを含む、イベントの1つのパターンが表示されます（最後のイベントが指定されたパスサイズを超えている場合でも）。 デフォルトでは、行はパス内のイベント数で昇順になります。

オプションで、各行の集約コンバージョンデータを含めることができます。 レポートにコンバージョン/収益の列を含めると、各コンバージョンタイプは4つの列で表され、a）コンバージョンの合計数、b）そのイベントパターンに起因するコンバージョン全体の割合、c）最初のイベントからコンバージョンまでの平均待ち時間、d）最後のイベントからコンバージョンまでの平均待ち時間を示します。 コンバージョンパスに指定されたパスサイズよりも多くのイベントが含まれる場合、レポートには、イベントの数が多いコンバージョンのデータを集計する追加の行が含まれます（6つのイベントタイプを含むすべてのパターンなど）。

過去18か月間のデータを表示できます。

## 使用可能な列

以下は、各レポートで使用できる列です。 デフォルトの列は、デフォルトで自動的に含まれます。 レポート設定の「列」セクションから、使用可能なカスタム列を追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] ～ [!UICONTROL 5th Event] | Default | 広告主の[ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)と[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内の5つの最も初期のイベントタイプ。 |
| [!UICONTROL Path Size] | Default | 広告主の[ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)および[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内のイベントタイプの数。 |
| [!UICONTROL First Event Type] | Default | コンバージョンパスの最初の（最も早い）イベントのイベントタイプ。 |
| [!UICONTROL Last Event Type] | Default | コンバージョンに至った最後のイベントのイベントタイプ（最後のイベントが指定されたパスサイズを超えている場合でも）。 |
| \[広告主固有のカスタム（派生）指標\] | カスタム | 既存の指標から計算された、作成したカスタム指標の値。 |
| \[Advertiser-specific conversion metrics\] | カスタム | 指定されたコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| [!UICONTROL % of Total] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます） イベントパターンに起因するポートフォリオ全体のコンバージョンの割合。 |
| [!UICONTROL 6th Event] ～ [!UICONTROL 30th Event] | カスタム | 広告主の[ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)と[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパスの6番目から30番目のイベントタイプ。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます）最初のイベントからコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベントからコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Path Frequency] | カスタム | この行のパスが変換前に発生した回数。 |

>[!MORELIKETHIS]
>
>* [ アシストレポートについて](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [ レポート設定の支援](assist-report-settings.md)
>* [ スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
