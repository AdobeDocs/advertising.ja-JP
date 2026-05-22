---
title: '[!UICONTROL Keyword Assist Report]'
description: '[!UICONTROL Keyword Assist Report]について説明します。'
feature: Search Reports, Search Assist Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 0%

---

# ザ [!UICONTROL Keyword Assist Report]

*検索、ソーシャル、およびCommerceのクリック追跡と、Adobe AdvertisingとAdobe Analyticsのコンバージョン追跡を備えた広告主（[!DNL Analytics]統合）、またはトークン（`ef_id`）のみを使用したフィードで提供された広告主*

[!UICONTROL Keyword Assist Report]は、クリックを促進するキーワードまたはプレースメントを示します。 このレポートには、コンバージョンパスのクリック数を受け取った有料検索キーワードまたは配置の各パターンが表示され、そのパターンがコンバージョン全体にどのように貢献しているのかを示しています。 例えば、ユーザーが「革靴」のキーワード検索から生じた広告を最初にクリックし、「スエードシューズ」のキーワード検索から広告をクリックしてから注文を行った際に、コンバージョンが何回発生したかを確認できます。また、ユーザーが10以上のキーワードから生じた広告をクリックした後に、コンバージョンが何回発生したかを確認できます。

レポート結果には、広告主の検索内で発生したコンバージョンパス内のN番目の初期の有料検索キーワードまたはプレースメントクリックまでの集計データが含まれます
「ルックバック」および「インプレッションのルックバックウィンドウ」をクリックします。 例えば、パスサイズを5個（5）に設定した場合、レポートは、クリックを受け取った最も古い5つのキーワードまたはプレースメントを含むコンバージョンパスで構成され、追跡されたクリックのパターンごとに1行が表示されます。 各行には、パスの最初のキーワードまたはプレースメントと、コンバージョンに至った最後のキーワードまたはプレースメントが含まれます（最後のキーワードが指定されたパスサイズを超えている場合でも）。 デフォルトでは、行はパス内のイベント数で昇順になります。

>[!NOTE]
>
>レポートにコンテンツ対応の検索キャンペーンのプレースメントが含まれている場合（キーワードが含まれていない場合）、[!UICONTROL Keyword]列には、該当する広告グループ名（「（adgroup content） Your Ad Group Name」など）が表示されます。

オプションで、各行の集約コンバージョンデータを含めることができます。 レポートにコンバージョン/収益の列を含めると、各コンバージョンタイプは4つの列で表され、a）コンバージョンの合計数、b）そのキーワードパターンに起因するコンバージョン全体の割合、c）最初のイベント（最初のキーワード）からコンバージョンまでの平均待ち時間、d）最後のイベント（最後のキーワード）からコンバージョンまでの平均待ち時間を示します。 コンバージョンパスに指定されたパスサイズよりも多くのキーワードが含まれる場合、レポートには、より多くのキーワード数（6つのキーワードのクリックを含むすべてのパターンなど）に起因するコンバージョンのデータを集計する追加の行が含まれます。

過去18か月間のデータを表示できます。

## 使用可能な列

以下は、各レポートで使用できる列です。 デフォルトの列は、デフォルトで自動的に含まれます。 レポート設定の「列」セクションから、使用可能なカスタム列を追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] ～ [!UICONTROL 5th Keyword] | Default | 広告主の[&#x200B; クリックのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)および[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内の5つの最も初期の有料検索キーワードまたはプレースメントクリック。<br><br><b>注：</b> レポートにコンテンツが有効な検索キャンペーンのプレースメントが含まれている場合（キーワードが含まれていない）、これらの列には該当する広告グループ名（「（adgroup content） Your Ad Group Name）」など）がです。」 |
| [!UICONTROL Path Size] | Default | 広告主の[&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)および[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内のキーワードおよび/またはプレースメントの数。 |
| [!UICONTROL First Keyword] | Default | コンバージョンパスの最初のキーワードまたはプレースメント。 |
| [!UICONTROL Last Keyword] | Default | コンバージョンに至った最後のキーワードまたはプレースメント（最後のキーワードが指定したパスサイズを超えている場合でも）。 |
| \[広告主固有のカスタム（派生）指標\] | カスタム | 既存の指標から計算された、作成したカスタム指標の値。 |
| \[Advertiser-specific conversion metrics\] | カスタム | 指定されたコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| [!UICONTROL % of Total] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます） キーワードや配置パターンに起因するポートフォリオ全体のコンバージョンの割合。 |
| [!UICONTROL 6th Keyword] ～ [!UICONTROL 10th Keyword] | カスタム | 広告主の[&#x200B; クリックのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)および[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパスで、6番目から10番目までの有料検索キーワードまたはプレースメントのクリック。<br><br><b>注：</b> レポートにコンテンツが有効な検索キャンペーンのプレースメントが含まれている場合（キーワードが含まれていない）、これらの列には該当する広告グループ名（「広告グループ名」など）。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます）最初のイベント（最初のキーワードまたはプレースメント）からコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベント（最後のキーワードまたはプレースメント）からコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Path Frequency] | カスタム | この行のパスが変換前に発生した回数。 |

>[!MORELIKETHIS]
>
>* [&#x200B; アシストレポートについて](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [&#x200B; レポート設定の支援](assist-report-settings.md)
>* [&#x200B; スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
