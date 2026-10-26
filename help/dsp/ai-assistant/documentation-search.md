---
title: AI アシスタントを使用して製品ドキュメントを検索する
description: DSP AI アシスタントを使用してAdobe Advertising DSPと[!DNL Creative]件のドキュメントを検索する方法について説明します。 引用や提案されたフォローアップクエリを確認して、疑問の答えを見つけることができます。
feature: DSP Introduction, Creative Introduction
exl-id: 30feb866-cc8c-4760-af94-2b2e08ebb361
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d05f5093-0b42-5b61-81cc-b438107ef814
    internal-label: DSP Introduction
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: ba946348-465d-45f3-8d28-c42d0a2599c5
    internal-label: Creative introduction
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%
---
# AI アシスタントを使用して製品ドキュメントを検索する

*英語のみサポート*

DSP用AI アシスタントを使用して、チャットインターフェイスを使用して、[Advertising DSP ガイド &#x200B;](/help/dsp/home.md)および[Advertising Creative ガイド &#x200B;](/help/creative/home.md)の ガイド および（Advertising Creativeを使用している広告主）全体の概念とハウツーコンテンツを検索します。 回答は、[Experience League](https://experienceleague.adobe.com/ja/docs/advertising)に記載されている商品に関する情報に基づいています。

回答には、引用だけでなく、追加のクエリやフォローアップの質問も含まれており、クエリを絞り込んで詳細を確認するのに役立ちます。

![&#x200B; クエリと応答の例](/help/dsp/assets/agent-chat-response.png " クエリと応答の例")

>[!IMPORTANT]
>
>AIによる回答は、不正確または誤解を招く可能性があります。 コストや労力に影響を与える意思決定に役立つ回答や情報源を常に確認しましょう。

## クエリの例

キャンペーン管理、最適化、オーディエンス管理、セール情報、レポートなど、製品の機能について質問することができます。 次に例を示します。

* プレースメントに広告を添付するにはどうすればよいですか？

* Adobe DSPにはどのようなターゲティングオプションがありますか？

* 配置設定で様々なペーシングオプションを使用した場合の結果は何ですか？

* 世帯レベルのデータを含むレポートは？

* [!DNL Creative] エクスペリエンスの広告タグを作成するにはどうすればよいですか？

## クエリを送信

一度に1つのメッセージで複数の質問を行うことはできますが、一度に1つのメッセージのみ行うことができます。 別の応答を送信する前に、応答を待ちます。

1. 任意のページの右上にある「![&#x200B; エージェント型チャット &#x200B;](/help/dsp/assets/agent-chat.png " エージェント型チャット ")」をクリックします。

1. クエリを作成します。

   * 独自のクエリを入力します。

   * クエリの例を表示するには、**[!UICONTROL Learn]**&#x200B;をクリックしてセクションを展開します。

     1. （オプション）サンプルクエリのテキストを入力フィールドにコピーするには、次の手順を実行します。

        1. 例をクリックします。

        1. （オプション）ニーズに合わせてテキストを編集します。

   クエリについて詳しくは、「[&#x200B; クエリとプロンプトの作成に関するベストプラクティス &#x200B;](ai-assistant-about.md#writing-queries)」を参照してください。

1. ![&#x200B; クエリを送信](/help/dsp/assets/submit-prompt.png " クエリを送信")をクリックするか、キーボードの&#x200B;**Enter** キーを押します。

   応答には、インラインの引用と下部の&#x200B;**[!UICONTROL Documentation Sources]** リストが含まれています。 フォローアップの質問や提案が表示されることもあります。

1. AI アシスタントから追加情報の提供を求められた場合は、情報を提供します。

1. 応答のデータソースとして使用されるページを開くには、次のいずれかの操作を行います。

   * 番号付きの引用をクリックします。

   * **[!UICONTROL Documentation Sources]**&#x200B;をクリックして、応答で引用されたすべてのページのリストを表示し、ページリンクをクリックします。

>[!TIP]
>
>別の問題、または別のパッケージまたはプレースメントについて質問するには、[新しい会話を開始します](#conversation-new)。

## 新しい会話を始める {#conversation-new}

会話（クエリスレッド）ごとに個別に保存されるため、以前の会話を区別できます。

1. [&#x200B; チャットボックス &#x200B;](#ai-assistant-open)の上部で、![新しい会話を開始](/help/dsp/assets/new-selection.png "新しい会話を開始")をクリックします。

1. [&#x200B; クエリを送信](#query-submit)。

<!-- 

Not there as of 10/22/26. Anyway, this feature isn't actionable in terms of improving page content.

## Provide feedback about a response

* Next to the [!UICONTROL Documentation Sources] list:

  * For helpful responses, click ![Thumbs up](/help/dsp/assets/thumbs-up.png "Thumbs up").

  * For unhelpful responses, click ![Thumbs down](/help/dsp/assets/thumbs-down.png "Thumbs down").

 -->

<!--

## Best practices for writing queries {#writing-queries}

* **Be clear and specific.** Use full questions ("How do I subscribe to On-demand inventory?"), task phrases ("subscribe to On-demand inventory"), or topic phrases ("On-demand inventory").

* **Match UI terms** when possible for product features (such as "campaigns" or "deals").

  For common actions (such as "add," "attach," or "assign"), you can use synonyms.

* **Add detail** to narrow or broaden results. Refine with follow-up questions as needed.

* **Don't worry about punctuation and capitalization** except when they affect meaning.

-->

## チャットボックスの拡大と最小化

1. [&#x200B; チャットボックス &#x200B;](#ai-assistant-open)の上部にある「![&#x200B; フルスクリーンに入る](/help/dsp/assets/fullscreen.png " フルスクリーンに入る")」をクリックして、フルスクリーンモードに入ります。

1. チャットボックスをパネルモードに戻すには、**[!UICONTROL < Back>]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising DSPのAI アシスタントについて](ai-assistant-about.md)
>* [以前のAI アシスタントの会話を操作](previous-conversations.md)
