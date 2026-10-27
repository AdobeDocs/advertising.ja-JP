---
title: AI アシスタントを使用してレポートを作成する
description: Adobe Advertising DSP AI アシスタントのインサイトエージェントを使用して、キャンペーン指標のクエリ、レポートの生成、CSV ファイルのダウンロードを行う方法について説明します。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%
---
# AI アシスタントを使用してレポートを作成する

*Beta機能*

AI アシスタントのインサイトエージェントを使用すると、レポートを手作業で作成することなく、キャンペーン、キャンペーンコンポーネント、Advertising Creativeエクスペリエンス、広告主、広告目標に関する指標や詳細なレポートを取得できます。 キャンペーンの費用やCPAなど、特定の指標に関する簡単な質問をしたり、特定のディメンション（単一のキャンペーンやオーディエンスなど）やディメンション全体（キャンペーンや広告主ごとの内訳）に関する、より複雑なレポートを要求したりできます。 結果はCSV ファイルとしてダウンロードできます。

>[!IMPORTANT]
>
>AIによる回答は、不正確または誤解を招く可能性があります。 コストや労力に影響を与える意思決定に役立つ回答や情報源を常に確認しましょう。

## クエリの例

* [ キャンペーン名]は先週いくら費やしましたか？

* 今月[ キャンペーン名]はコンバージョン数を取得しましたか？

* [ キャンペーン名]のパッケージ別CPAを表示します。

* 20%以上遅れている企業はどれか？

* 過去15日間のすべてのキャンペーンとパッケージの純支出を比較します。

## クエリを送信

一度に1つのメッセージで複数の質問を行うことはできますが、一度に1つのメッセージのみ行うことができます。 別の応答を送信する前に、応答を待ちます。

1. 任意のページの右上にある「![&#x200B; エージェント型チャット &#x200B;](/help/dsp/assets/agent-chat.png " エージェント型チャット ")」をクリックします。

1. クエリを作成します。

   1. 次のいずれかの操作を行います。

      * 独自のクエリを入力します。

      * クエリの例を確認するには：

        1. **[!UICONTROL Insights]**&#x200B;をクリックしてセクションを展開します。

        1. （オプション）サンプルクエリのテキストを入力フィールドにコピーするには、次の手順を実行します。

           1. 例をクリックします。

           1. （オプション）ニーズに合わせてテキストを編集します。

   1. （オプション）特定のディメンション値（特定のキャンペーンなど）にクエリをフォーカスするには、ディメンション値を表示する場所にカーソルをオプションで挿入し、![&#x200B; エンティティのメンション &#x200B;](/help/dsp/assets/prompt-entity.png " エンティティのメンション ")をクリックし、ディメンションを選択して、ディメンション値を選択します。

      例えば、ディメンション [!UICONTROL Campaign]の場合、すべてのキャンペーンのリストからレポート対象を選択できます。

      使用可能なディメンションは次のとおりです。

      * キャンペーンエンティティ：[!UICONTROL Campaign]、[!UICONTROL Package]、[!UICONTROL Placement]、[!UICONTROL Ad]
      * 広告主：[!UICONTROL Advertiser]
      * Advertising Creative エンティティ：[!UICONTROL Experience]
      * 広告目標：[!UICONTROL Audience]、[!UICONTROL City]、[!UICONTROL Country]、[!UICONTROL State]、[!UICONTROL DMA]、[!UICONTROL Retargeting Pixel]、[!UICONTROL Device OS]、[!UICONTROL Device Browser]、[!UICONTROL Device Type]、[!UICONTROL Zip Code]

   クエリについて詳しくは、「[&#x200B; クエリとプロンプトの作成に関するベストプラクティス &#x200B;](ai-assistant-about.md#writing-queries)」を参照してください。

1. ![&#x200B; クエリを送信](/help/dsp/assets/submit-prompt.png " クエリを送信")をクリックするか、キーボードの&#x200B;**Enter** キーを押します。 担当者が追加情報を要求する場合は、必要な情報を提供します。

   レポートの最初の数行が表示され、レポート全体をプレビューおよびダウンロードするためのリンクが表示されます。

   生成されたレポートの数行が表示されます。

>[!TIP]
>
>別の問題、または別のパッケージまたはプレースメントについて質問するには、[新しい会話を開始します](#conversation-new)。

## チャットボックスからレポート全体をダウンロードまたはプレビューする

* レポート全体のコピーをダウンロードするには、![書き出し](/help/dsp/assets/download.png "書き出し")をクリックします。

  ファイルは、ブラウザーの通常の手順に従って、[!DNL Microsoft Excel]個のコンマ区切り値ファイル（.csv）としてダウンロードされます。 ファイル名は「DSP_Insights_Report_&lt;job_number>」です。

* サイドパネルでレポート全体をプレビューするには、![&#x200B; プレビュー](/help/dsp/assets/agent-chat-preview.png " プレビュー")をクリックします。 プレビューからレポートをダウンロードするには、![書き出し](/help/dsp/assets/download.png "書き出し")をクリックします。

  レポートをダウンロードすると、ブラウザーの通常の手順に従って、[!DNL Microsoft Excel]個のコンマ区切り値ファイル（.csv）としてダウンロードされます。 ファイル名は「DSP_Insights_Report_&lt;job_number>」です。

## 新しい会話を始める {#conversation-new}

会話（クエリスレッド）ごとに個別に保存されるため、以前の会話を区別できます。

1. [&#x200B; チャットボックス &#x200B;](#ai-assistant-open)の上部で、![新しい会話を開始](/help/dsp/assets/new-selection.png "新しい会話を開始")をクリックします。

1. [&#x200B; クエリを送信](#query-submit)。

## チャットボックスの拡大と最小化

1. [&#x200B; チャットボックス &#x200B;](#ai-assistant-open)の上部にある「![&#x200B; フルスクリーンに入る](/help/dsp/assets/fullscreen.png " フルスクリーンに入る")」をクリックして、フルスクリーンモードに入ります。

1. チャットボックスをパネルモードに戻すには、**[!UICONTROL < Back>]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising DSPのAI アシスタントについて](ai-assistant-about.md)
>* [以前のAI アシスタントの会話を操作](previous-conversations.md)
