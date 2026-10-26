---
title: Advertising DSPのAI アシスタントについて
description: DSP AI アシスタントを使用して、パッケージとプレースメントのトラブルシューティング、レポート、製品使用状況ヘルプの検索を行う方法について説明します。
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
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# Advertising DSPのAI アシスタントについて

DSPのAI アシスタントは、DSPで利用可能なあらゆるエージェント型ワークフローを、単一のチャットボックスから実行できる会話型インターフェイスです。 新しいタスクを作成したり、以前のタスクを続行するために助けを求めたりできます。

会話の履歴は、すべてのワークフローに対して保持され、会話ごとに自動的に名前が付けられます。 クエリは他のユーザーと共有されません。

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## サポートされているワークフロー

次のワークフローは、より効果的に作業を達成するのに役立ちます。

<!-- And links to all sections/pages -->

| 機能 | 説明 | クエリの例 | 回答数 |
| --- | --- | --- | --- |
| [ トラブルシューティング ](troubleshooting-agent.md) | 選択したライブパッケージまたはプレースメントのパフォーマンスと配信の問題を診断します。<ul><li>配置のみ：超過、過支出、および支出の失敗を診断します。 関連するペーシング、入札、ターゲティング、予算上限の要因を評価します。</li><li>パッケージのみ：CPAの上昇やROASの低下など、パフォーマンスの問題を診断します。 CTR、CPC、クリック数、インプレッション数などのエンゲージメント指標は診断されません。</li></ul>各会話は、1つのパッケージまたは配置に対して1つの診断をカバーします。 結果を受け取った後、新しい会話を開始して、別の問題、パッケージ、または配置を診断します。<br><br> エージェントは、設定を変更したり、キャンペーンやキャンペーンコンポーネントを作成または編集したりすることはできません。 また、一時停止、完了、アーカイブ、スケジュールされたパッケージまたはプレースメントを診断することはできません。 | 配置の支出課題：<ul><li>私のプレースメントは、取引がアクティブであるにもかかわらず、昨日過ごすのをやめました。 なぜでしょうか？</li><li>この5日間、なぜこのプレースメントが過小評価されているのですか？</li><li>途中でペースを大幅に遅らせています。 なぜでしょうか？</li></ul>パッケージパフォーマンスの問題：<ul><li>この1週間でこのパッケージのCPAが増加したのはなぜですか？</li><li>このパッケージのROASが低下しているのはなぜですか？</li></ul> | 応答には、パフォーマンスを制限する要因が含まれており、問題を解決するための推奨事項が提供されます。 |
| [ インサイト ](insights-agent.md) | レポートを手作業で作成することなく、キャンペーンの指標と詳細なレポートを取得できます。 キャンペーンの費用やCPAなど、特定の指標に関する簡単な質問をしたり、特定のディメンション（単一のキャンペーン、プレースメント、オーディエンスなど）やディメンション間（キャンペーンや広告主による内訳）に関する、より複雑なレポートを要求したりできます。 結果はCSV ファイルとしてダウンロードできます。 | <ul><li>[ キャンペーン名]は先週いくら費やしましたか？<li>今月[ キャンペーン名]はコンバージョン数を取得しましたか？</li><li>20%以上遅れている企業はどれか？</li></li>[ キャンペーン名]のパッケージ別CPAを表示する</li></ul> | レポートの最初の数行が表示され、レポート全体をプレビューするためのリンクと、レポートを[!DNL Microsoft Excel] コンマ区切りの値ファイル （.csv）としてダウンロードするためのリンクが表示されます。 |
| [製品ドキュメント検索](documentation-search.md) | [Advertising DSP ガイド ](/help/dsp/home.md)で概念的なコンテンツとハウツーのコンテンツを検索し、Advertising Creativeを使用している広告主については、[Advertising Creative ガイド ](/help/creative/home.md)を検索します。 回答は、[Experience League](https://experienceleague.adobe.com/en/docs/advertising)でこれらの製品について文書化されているものだけに基づいています。<br><br> キャンペーン管理、最適化、オーディエンス管理、お得な情報、レポート、その他の製品の機能について質問します。 | <ul><li>プレースメントに広告を添付するにはどうすればよいですか？</li><li>Adobe DSPにはどのようなターゲティングオプションがありますか？</li><li>配置設定で様々なペーシングオプションを使用した場合の結果は何ですか？</li><li>世帯レベルのデータを含むレポートは？</li><li>[!DNL Creative] エクスペリエンスの広告タグを作成するにはどうすればよいですか？</li></ul> | 応答には、インラインの引用と下部の拡張可能な[!UICONTROL Documentation Sources] リストが含まれています。 任意の引用またはソースリストをクリックして、関連するページを開きます。<br><br>応答には、質問を絞り込み、詳細な情報を見つけるのに役立つフォローアップの質問や提案が含まれる場合もあります。 |

## AI アシスタントを開く {#ai-assistant-open}

* 任意のページの右上にある「![ エージェント型チャット ](/help/dsp/assets/agent-chat.png " エージェント型チャット ")」をクリックします。

## チャットボックスを拡大

1. [ チャットボックス ](#ai-assistant-open)の上部にある「![ フルスクリーンに入る](/help/dsp/assets/fullscreen.png " フルスクリーンに入る")」をクリックして、フルスクリーンモードに入ります。

1. チャットボックスをパネルモードに戻すには、**[!UICONTROL < Back>]**&#x200B;をクリックします。

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

## クエリとプロンプトの作成に関するベストプラクティス {#writing-queries}

* **明確かつ具体的に**&#x200B;する。 完全な質問（「オンデマンド在庫の購読方法」）、タスクフレーズ（「オンデマンド在庫の購読」）、またはトピックフレーズ（「オンデマンド在庫」）を使用します。

* **同じ会話に保存する場合を除き、同じクエリ**&#x200B;で異なるタイプのリクエストを組み合わせないでください。

* **関連する日付の範囲**&#x200B;を含めて、必要なデータを絞り込みます。

* **製品の機能（「キャンペーン」や「お得な情報」など）について、可能であればUI用語**&#x200B;を一致させます。

  一般的なアクション（「追加」、「添付」、「割り当て」など）では、類義語を使用できます。

* **詳細**&#x200B;を追加して、結果を絞り込んだり広げたりします。 必要に応じてフォローアップの質問で絞り込むことができます。

* **句読点と大文字の使用について心配する必要はありません**。ただし、意味に影響を与える場合は除きます。

>[!MORELIKETHIS]
>
>* [AI アシスタントを使用してレポートを作成](insights-agent.md)
>* [AI アシスタントを使用したパフォーマンスと配信の問題のトラブルシューティング ](troubleshooting-agent.md)
>* [再利用可能なオーディエンスを作成](/help/dsp/audiences/reusable-audience-create.md)
>* [AI アシスタントを使用して製品ドキュメントを検索](documentation-search.md)
>* [以前のAI アシスタントの会話を操作](previous-conversations.md)
