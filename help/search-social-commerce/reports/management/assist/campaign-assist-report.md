---
title: "[!UICONTROL Campaign Assist Report]"
description: 詳しくは、 [!UICONTROL Campaign Assist Report].
source-git-commit: e2df0116f912ca9cbf3d140dec4da57536b929bd
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# この [!UICONTROL Campaign Assist Report]

*検索、ソーシャル、コマースのクリック追跡およびAdobe Advertising、Adobe Analytics( [!DNL Analytics] 統合 )、またはトークン (`ef_id`) のみ*

この [!UICONTROL Campaign Assist Report] どのキャンペーンがコンバージョンプロセスを支援したかを示します。 広告が 1 つ以上のコンバージョンにつながったキャンペーンの各パターンが、全体的なコンバージョンにどの程度貢献したかをレポートします。 例えば、ユーザーがキャンペーン A から広告を最初に表示し、キャンペーン B から広告をクリックしてから注文した後に、コンバージョンが何回発生したかを確認できます。 同様に、ユーザーが 10 を超えるキャンペーンの広告とやり取りした後に発生したコンバージョン数を確認できます。

レポートの結果には、コンバージョンパス内のキャンペーンのパターン（最も早い順に N 個まで）で、広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). 例えば、パスサイズを 5(5) に選択した場合、最も早い 5 つのキャンペーンを含むコンバージョンパスがレポートに表示され、イベントが追跡されたキャンペーンのパターンごとに 1 行が表示されます。 各行には、（最後のキャンペーンが指定されたパスサイズの外にある場合でも）パスの最初のキャンペーンと、コンバージョンにつながった最後のキャンペーンを含む、1 つのキャンペーンパターンが表示されます。 デフォルトでは、行はパス内のキャンペーン数の昇順に表示されます。

オプションで、各行にカスタム指標を含む集計コンバージョンデータを含めることができます。 レポートにコンバージョン/売上高の列を含めると、各コンバージョンタイプが 4 つの列に表示され、a) コンバージョンの合計数、b) キャンペーンパターンに属するコンバージョン全体の割合、c) 最初のイベント（最初のキャンペーン）からコンバージョンまでの日数の平均待ち時間。 コンバージョンパスに指定したパスサイズを超えるキャンペーンが含まれる場合、レポートには、多数のキャンペーン（6 つのキャンペーンを含むすべてのパターンなど）から得られたコンバージョンのデータを集計した追加の行が含まれます。

また、オプションで、キャンペーン名の後に広告ネットワークやイベントタイプ ( 例： `<campaign name> (Google) click`.

過去 18 ヶ月のデータを表示できます。

>[!TIP]
>
>ブランドキーワードが汎用キーワードとは異なるキャンペーンに含まれている場合、レポートは、ブランドキーワードがコンバージョンに貢献しているかどうかを示します。

## 使用可能な列

次に、各レポートで使用できる列を示します。 デフォルトの列は、デフォルトで自動的に含まれます。 使用可能なカスタム列は、レポート設定の「列」セクションから追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] から [!UICONTROL 5th Campaign] | デフォルト | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j).<br><br>エンティティ名の後に広告ネットワーク、アカウント名、イベントタイプを示すレポートオプションを含めた場合、その情報はキャンペーン名の後に含まれます ( 例： `"<"campaign name> [Google] [Account1] [impression]`&quot;) です。 |
| [!UICONTROL Path Size] | デフォルト | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | デフォルト | コンバージョンパスの最初のキャンペーン。 |
| [!UICONTROL Last Campaign] | デフォルト | コンバージョンにつながった最後のキャンペーン（最後のキーワードが指定されたパスサイズの外にある場合も含む）。<br><br>エンティティ名の後に広告ネットワーク、アカウント名、イベントタイプを示すレポートオプションを含めた場合、その情報はキャンペーン名の後に含まれます ( 例： `"<"campaign name> [Google] [Account1] [impression]`&quot;) です。 |
| \[ 広告主固有のカスタム（派生）指標\] | カスタム | 作成した、既存の指標から計算されたカスタム指標の値。 |
| \[ 広告主固有のトランザクションプロパティ\] | カスタム | 指定したトランザクションプロパティまたはサイトエンゲージメント指標に対するコンバージョンの数。 |
| [!UICONTROL % of Total] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、含まれる各トランザクションプロパティのレポート出力に自動的に含まれます）キャンペーンパターンに起因する、指定したトランザクションプロパティのコンバージョン数。 |
| [!UICONTROL 6th Campaign] から [!UICONTROL 20th Campaign] | カスタム | 広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j).<br><br>エンティティ名の後に広告ネットワーク、アカウント名、イベントタイプを示すレポートオプションを含めた場合、その情報はキャンペーン名の後に含まれます ( 例： `"<"campaign name> [Baidu] [Account1] [click]`&quot;) です。 |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、含まれる各トランザクションプロパティのレポート出力に自動的に含まれます）最初のイベント（最初のキャンペーン）からコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[ トランザクションプロパティ\] | 自動 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）前回のイベント（前回のキャンペーン）からコンバージョンまでの平均待ち時間（日数）。 |
| [!UICONTROL EF Campaign ID] | カスタム | Search、Social および Commerce がキャンペーンに割り当てる数値 ID。 |
| [!UICONTROL EF Portfolio Group ID] | カスタム | ポートフォリオが属するポートフォリオグループの数値 ID。 |
| [!UICONTROL EF Search Engine ID] | カスタム | Search、Social および Commerce が広告ネットワークに割り当てる数値 ID。 <i>[!UICONTROL 3]</i> 対象 [!DNL Google Ads], <i>[!UICONTROL 10]</i> 対象 [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> 対象 [!DNL Meta], <i>[!UICONTROL 86]</i> 対象 [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> 対象 [!DNL Naver], <i>[!UICONTROL 88]</i> 対象 [!DNL Baidu], <i>[!UICONTROL 90]</i> 対象 [!DNL Yandex], <i>[!UICONTROL 94]</i> 対象 [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> 対象 [!DNL Yahoo Native] （非推奨）または <i>[!UICONTROL 106]</i> 対象 [!DNL Pinterest] （非推奨）。 |
| [!UICONTROL Portfolio ID] | 数値のポートフォリオ ID。 |
| [!UICONTROL User SE Account ID] | Search、Social および Commerce が広告ネットワークに割り当てる数値 ID。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [アシストレポートについて](assist-report-about.md)
>* [この [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [この [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [レポート設定の支援](assist-report-settings.md)
>* [アシストレポートの生成](assist-report-generate.md)
