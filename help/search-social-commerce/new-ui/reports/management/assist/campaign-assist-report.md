---
title: '[!UICONTROL Campaign Assist Report]'
description: '[!UICONTROL Campaign Assist Report]について説明します。'
feature: Search Reports, Search Assist Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 1%

---

# ザ [!UICONTROL Campaign Assist Report]

*検索、ソーシャル、およびCommerceのクリック追跡と、Adobe AdvertisingとAdobe Analyticsのコンバージョン追跡を備えた広告主（[!DNL Analytics]統合）、またはトークン（`ef_id`）のみを使用したフィードで提供された広告主*

[!UICONTROL Campaign Assist Report]は、コンバージョン プロセスを支援したキャンペーンを示します。 レポートは、1つ以上のコンバージョンにつながった広告のキャンペーンの各パターンが、全体的なコンバージョンにどのように貢献したかを示します。 例えば、ユーザーがキャンペーン Aの広告を初めて見て、キャンペーン Bの広告をクリックして注文した際に、コンバージョンがいくつか発生したかを確認できます。 同様に、10以上のキャンペーンの広告に対してユーザーがインタラクションした後に、どれだけのコンバージョンが発生したかを確認できます。

レポート結果には、広告主の[&#x200B; クリックのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)と[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したイベントについて、コンバージョンパスのキャンペーンの各パターン（最も早いN個のキャンペーンまで）に関する集計データが含まれます。 例えば、パスサイズを5 （5）に設定すると、レポートには、最も初期の5つのキャンペーンを含むコンバージョンパスが含まれ、イベントが追跡されたキャンペーンのパターンごとに1行が表示されます。 各行には、パスの最初のキャンペーンと、コンバージョンにつながる最後のキャンペーンを含む、キャンペーンの1つのパターンが表示されます（最後のキャンペーンが指定されたパスサイズを超えている場合でも）。 デフォルトでは、行はパス内のキャンペーンの数で昇順になります。

必要に応じて、各行にカスタム指標を含む集約コンバージョンデータを含めることができます。 レポートにコンバージョン/収益列を含めると、各コンバージョンタイプは4つの列で表され、a）コンバージョンの合計数、b）そのキャンペーンパターンに起因するコンバージョン全体の割合、c）最初のイベント（最初のキャンペーン）からコンバージョンまでの平均待ち時間、d）最後のイベント（最後のキャンペーン）からコンバージョンまでの平均待ち時間を示します。 コンバージョンパスに指定されたパスサイズよりも多くのキャンペーンが含まれる場合、レポートには、キャンペーンの数が多いコンバージョンのデータを集計する追加の行（6つのキャンペーンを含むすべてのパターンなど）が含まれます。

オプションで、キャンペーン名の後に広告ネットワークやイベントタイプ（`<campaign name> (Google) click`など）を含めることもできます。

過去18か月間のデータを表示できます。

>[!TIP]
>
>ブランドキーワードが、一般的なキーワードと異なるキャンペーン内にある場合、レポートは、ブランドキーワードがコンバージョンに貢献しているかどうかを示します。

## 使用可能な列

以下は、各レポートで使用できる列です。 デフォルトの列は、デフォルトで自動的に含まれます。 レポート設定の「列」セクションから、使用可能なカスタム列を追加できます。

| 列 | デフォルト？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] ～ [!UICONTROL 5th Campaign] | Default | 広告主の[&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)と[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内の5つの初期キャンペーン。<br><br> エンティティ名の後に広告ネットワーク、アカウント名、またはイベントタイプを示すレポートオプションのいずれかを含めた場合、その情報はキャンペーン名の後に含まれます（`"<"campaign name> [Google] [Account1] [impression]`など）。 |
| [!UICONTROL Path Size] | Default | 広告主の[&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)および[&#x200B; インプレッション ルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内のキャンペーンの数。 |
| [!UICONTROL First Campaign] | Default | コンバージョンパスの最初のキャンペーン。 |
| [!UICONTROL Last Campaign] | Default | コンバージョンに至った最後のキャンペーン（最後のキーワードが指定されたパスサイズを超えている場合でも） <br><br> エンティティ名の後に広告ネットワーク、アカウント名、イベントタイプを示すレポートオプションのいずれかを含めた場合、その情報はキャンペーン名の後に含まれます（`"<"campaign name> [Google] [Account1] [impression]`など）。 |
| \[広告主固有のカスタム（派生）指標\] | カスタム | 既存の指標から計算された、作成したカスタム指標の値。 |
| \[Advertiser-specific conversion metrics\] | カスタム | 指定されたコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| [!UICONTROL % of Total] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます） キャンペーンパターンから生じた、指定されたコンバージョン指標のコンバージョン数。 |
| [!UICONTROL 6th Campaign] ～ [!UICONTROL 20th Campaign] | カスタム | 広告主の[&#x200B; クリックルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#c-d)および[&#x200B; インプレッションのルックバックウィンドウ &#x200B;](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパスの6番目から20番目のキャンペーン。<br><br> エンティティ名の後に広告ネットワーク、アカウント名、またはイベントタイプを示すレポートオプションのいずれかを含めた場合、その情報はキャンペーン名の後に含まれます（`"<"campaign name> [Baidu] [Account1] [click]`など）。 |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます）最初のイベント（最初のキャンペーン）からコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベント（最後のキャンペーン）からコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL EF Campaign ID] | カスタム | Search, Social, &amp; Commerceがキャンペーンに割り当てる数値ID。 |
| [!UICONTROL EF Portfolio Group ID] | カスタム | ポートフォリオが属するポートフォリオグループの数値ID。 |
| [!UICONTROL EF Search Engine ID] | カスタム | Search, Social, &amp; Commerceがアドネットワークに割り当てる数値ID: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads] （非推奨）, [!DNL Pinterest] （非推奨）の<i>[!UICONTROL 106]</i><i>[!UICONTROL 105]</i>[!DNL Yahoo Native] |
| [!UICONTROL Portfolio ID] | カスタム | 数値ポートフォリオ ID。 |
| [!UICONTROL User SE Account ID] | カスタム | Search, Social, &amp; Commerceが広告ネットワークに割り当てる数値ID。 |

>[!MORELIKETHIS]
>
>* [&#x200B; アシストレポートについて](assist-report-about.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [&#x200B; レポート設定の支援](assist-report-settings.md)
>* [&#x200B; スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
