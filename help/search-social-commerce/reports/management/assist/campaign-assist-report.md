---
title: '[!UICONTROL Campaign Assist Report]'
description: '[!UICONTROL Campaign Assist Report] について説明します。'
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# [!UICONTROL Campaign Assist Report]

*検索、ソーシャル、Commerceのクリックのトラッキングと、Adobe Advertising、Adobe Analyticsからのコンバージョントラッキング（[!DNL Analytics] 統合を使用）またはフィードでトークン（`ef_id`）のみを使用して提供される広告主*

[!UICONTROL Campaign Assist Report] は、どのキャンペーンがコンバージョンプロセスを支援したかを示します。 このレポートでは、広告から 1 つ以上のコンバージョンが導かれたキャンペーンの各パターンが、コンバージョン全体にどのように貢献したかが報告されます。 例えば、ユーザーがキャンペーン A で広告を最初に見て、キャンペーン B で広告をクリックし、注文した際に発生したコンバージョン数を確認できます。 同様に、ユーザーが 10 を超えるキャンペーンの広告を操作した後に発生したコンバージョン数を確認できます。

レポート結果には、広告主の [ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d) および [ インプレッションルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j) 内で発生したイベントに関する、コンバージョンパス内のキャンペーンのパターンごとの集計データが、（N 個の最も古いキャンペーンまで）含まれます。 例えば、パスサイズを 5 つまで選択した場合、レポートには最大 5 つの最も古いキャンペーンを含んだコンバージョンパスが含まれ、イベントが追跡されたキャンペーンのパターンごとに 1 行が含まれます。 各行には、1 つのパターンのキャンペーンが表示されます。パス内の最初のキャンペーンと、コンバージョンが発生した最後のキャンペーンが含まれます（最後のキャンペーンが指定されたパスサイズに含まれない場合も含む）。 デフォルトでは、行はパス内のキャンペーン数の昇順になります。

オプションで、カスタム指標を含めた集計コンバージョンデータを各行に含めることができます。 レポートにコンバージョン/売上高の列を含めると、各コンバージョンタイプは 4 つの列で表され、a） コンバージョンの合計数、b）そのキャンペーンパターンに起因するコンバージョン全体の割合、c）最初のイベント（最初のキャンペーン）からコンバージョンまでの平均待ち時間（日数）、d）最後のイベント（最後のキャンペーン）からコンバージョンまでの平均待ち時間（日数）を示します。 指定したパスサイズを超えるキャンペーンがコンバージョンパスに含まれている場合、レポートには、多数のキャンペーン（6 つのキャンペーンを含むすべてのパターンなど）から生成されたコンバージョンのデータを集計した追加の行が含まれます。

オプションで、キャンペーン名の後に広告ネットワークやイベントタイプ（`<campaign name> (Google) click` など）を含めることもできます。

過去 18 か月のデータを表示できます。

>[!TIP]
>
>ブランドキーワードが汎用キーワードと異なるキャンペーンにある場合は、そのブランドキーワードがコンバージョンに貢献しているかどうかをレポートが示します。

## 使用可能な列

各レポートで使用できる列は次のとおりです。 デフォルトの列は、デフォルトで自動的に含まれます。 レポート設定の「列」セクションから、使用可能なカスタム列を追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] ～ [!UICONTROL 5th Campaign] | デフォルト | 広告主の [ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d) および [ インプレッションルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j) 内で発生したコンバージョンパスの最も古い 5 つのキャンペーン。<br><br> エンティティ名の後に広告ネットワーク、アカウント名またはイベントタイプを示すレポートオプションを含めた場合、その情報はキャンペーン名の後に含まれます（例：「`"<"campaign name> [Google] [Account1] [impression]`」）。 |
| [!UICONTROL Path Size] | デフォルト | 広告主の [ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d) および [ インプレッションルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j) 内で発生したコンバージョンパス内のキャンペーンの数。 |
| [!UICONTROL First Campaign] | デフォルト | コンバージョンパスの最初のキャンペーン。 |
| [!UICONTROL Last Campaign] | デフォルト | コンバージョンに至った最後のキャンペーン（最後のキーワードが指定されたパスサイズを超えている場合も含む）。<br><br> エンティティ名の後に広告ネットワーク、アカウント名またはイベントタイプを示すレポートオプションを含めた場合、その情報はキャンペーン名の後に含まれます（例：「`"<"campaign name> [Google] [Account1] [impression]`」）。 |
| \[ 広告主固有のカスタム （派生）指標\] | カスタム | 既存の指標から計算された、作成したカスタム指標の値。 |
| \[ 広告主固有のコンバージョン指標\] | カスタム | 指定したコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| [!UICONTROL % of Total] \[ コンバージョン指標\] | 自動 | （レポート設定では使用できませんが、各コンバージョン指標のレポート出力には自動的に含まれます） キャンペーンパターンによって生じた、指定されたコンバージョン指標のコンバージョン数。 |
| [!UICONTROL 6th Campaign] ～ [!UICONTROL 20th Campaign] | カスタム | 広告主の [ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d) および [ インプレッションルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j) 内で発生したコンバージョンパスの 6 ～ 20 番目のキャンペーン。<br><br> エンティティ名の後に広告ネットワーク、アカウント名またはイベントタイプを示すレポートオプションを含めた場合、その情報はキャンペーン名の後に含まれます（例：「`"<"campaign name> [Baidu] [Account1] [click]`」）。 |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[ コンバージョン指標\] | 自動 | （レポート設定では利用できませんが、各コンバージョン指標のレポート出力に自動的に含まれます）最初のイベント（最初のキャンペーン）からコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[ コンバージョン指標\] | 自動 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベント（最後のキャンペーンで）からコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL EF Campaign ID] | カスタム | 検索、ソーシャルおよびCommerceがキャンペーンに割り当てる数値 ID。 |
| [!UICONTROL EF Portfolio Group ID] | カスタム | ポートフォリオが属しているポートフォリオグループの数値 ID。 |
| [!UICONTROL EF Search Engine ID] | カスタム | 検索、ソーシャル、およびCommerceによって広告ネットワークに割り当てられる数値 ID。[!DNL Google Ads] の場合は <i>[!UICONTROL 3]</i>、[!DNL Microsoft Advertising] の場合は <i>[!UICONTROL 10]</i>、[!DNL Meta] の場合は <i>[!UICONTROL 45]</i>、[!DNL Yahoo! Display Network]<i>[!UICONTROL 87]</i> の場合は <i>[!UICONTROL 86]</i>、[!DNL Naver] の場合は <i>[!UICONTROL 88]</i>、[!DNL Baidu] の場合は <i>[!UICONTROL 90]</i> [!DNL Yandex]、[!DNL Yahoo! Japan Ads] の場合は <i>[!UICONTROL 94]</i>、[!DNL Yahoo Native] の場合は <i>[!UICONTROL 105]</i>、[!DNL Pinterest] の場合は <i>[!UICONTROL 106]</i> （非推奨）です。 |
| [!UICONTROL Portfolio ID] | 数値ポートフォリオ ID。 |
| [!UICONTROL User SE Account ID] | 検索、ソーシャルおよびCommerceが広告ネットワークに割り当てる数値 ID。 |

>[!MORELIKETHIS]
>
>* [ アシストレポートについて ](assist-report-about.md)
>* [[!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [[!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [ レポート設定の支援 ](assist-report-settings.md)
>* [ アシストレポートの生成 ](assist-report-generate.md)
