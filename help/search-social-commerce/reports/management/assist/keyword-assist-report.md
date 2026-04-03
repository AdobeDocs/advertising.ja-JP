---
title: '[!UICONTROL Keyword Assist Report]'
description: '[!UICONTROL Keyword Assist Report]について説明します。'
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
TQID: https://experienceleague.adobe.com/LO6nDisgA7981cjrGw31tJcy4VR6lesl-wvwU7uGlK4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 781
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
| [!UICONTROL 1st Keyword] ～ [!UICONTROL 5th Keyword] | Default | 広告主の[ クリックのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)と[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパスで、最も初期の5つの有料検索キーワードまたはプレースメントクリック。<br><br><b>注：</b> レポートにコンテンツ対応の検索キャンペーンのプレースメントが含まれている場合（キーワードが含まれていない場合）、これらの列には、代わりに「（adgroup コンテンツ）広告グループ名」など、該当する広告グループ名が表示されます。 |
| [!UICONTROL Path Size] | Default | 広告主の[ クリックルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)および[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパス内のキーワードおよび/またはプレースメントの数。 |
| [!UICONTROL First Keyword] | Default | コンバージョンパスの最初のキーワードまたはプレースメント。 |
| [!UICONTROL Last Keyword] | Default | コンバージョンに至った最後のキーワードまたはプレースメント（最後のキーワードが指定したパスサイズを超えている場合でも）。 |
| \[広告主固有のカスタム（派生）指標\] | カスタム | 既存の指標から計算された、作成したカスタム指標の値。 |
| \[Advertiser-specific conversion metrics\] | カスタム | 指定されたコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| [!UICONTROL % of Total] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます） キーワードや配置パターンに起因するポートフォリオ全体のコンバージョンの割合。 |
| [!UICONTROL 6th Keyword] ～ [!UICONTROL 10th Keyword] | カスタム | 広告主の[ クリックのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#c-d)と[ インプレッションのルックバックウィンドウ ](/help/search-social-commerce/glossary.md#i-j)内で発生したコンバージョンパスの6番目から10番目までの有料検索キーワードまたはプレースメントクリック。<br><br><b>注：</b> レポートにコンテンツ対応の検索キャンペーンのプレースメントが含まれている場合（キーワードが含まれていない場合）、これらの列には、代わりに「（adgroup コンテンツ）広告グループ名」など、該当する広告グループ名が表示されます。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、含まれるコンバージョン指標ごとにレポート出力に自動的に含まれます）最初のイベント（最初のキーワードまたはプレースメント）からコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[ コンバージョン指標] | 自動型 | （レポート設定では使用できませんが、レポート出力に自動的に含まれます）最後のイベント（最後のキーワードまたはプレースメント）からコンバージョンまでの平均待ち時間（日数）です。 |
| [!UICONTROL Path Frequency] | カスタム | この行のパスが変換前に発生した回数。 |

>[!MORELIKETHIS]
>
>* [ アシストレポートについて](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [ レポート設定の支援](assist-report-settings.md)
>* [ アシストレポートを生成](assist-report-generate.md)
