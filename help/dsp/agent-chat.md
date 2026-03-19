---
title: AI 支援チャットを使用して製品ドキュメントを検索
description: AI 支援チャットを使用してAdobe Advertising DSPとドキュメ  [!DNL Creative]  トを検索する方法を説明します。 引用と推奨されるフォローアッププロンプトで回答を得ます。
feature: DSP Introduction, Creative Introduction
hidefromtoc: true
hide: true
exl-id: 30feb866-cc8c-4760-af94-2b2e08ebb361
source-git-commit: 7f9b118ffe0b8e972296f79b19f6dcd2a9dedabe
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# AI を利用したチャットインターフェースで製品ドキュメントを検索

*Beta機能*

*英語のみのサポート*

<!-- How will this work once we have unified shell, which has its own version of AI Assistant? -->

AI チャットインターフェイスを使用して、[Advertising Creative ガイドおよび（Advertising Creativeを使用する広告主 &#x200B;](/help/dsp/home.md) [Advertising DSP ガイド &#x200B;](/help/creative/home.md) 全体の概念コンテンツとハウツーコンテンツを検索します。 回答は、[Experience League](https://experienceleague.adobe.com/en/docs/advertising) のこれらの製品に関してドキュメントに記載されている内容にのみ基づいています。

回答には、引用に加え、クエリを絞り込んで詳細情報を見つけるのに役立つ追加のプロンプトとフォローアップの質問が含まれます。 チャットの履歴は保持され、クエリは他のユーザーと共有されません。

>[!NOTE]
>
>クエリは、キャンペーン、取引、オーディエンスの設定、ステータス、パフォーマンスなど、お使いのアカウントに関するデータを返しません。 また、問題のトラブルシューティングにも役立ちません。

![&#x200B; クエリと応答の例 &#x200B;](/help/dsp/assets/agent-chat-response.png " クエリと応答の例 ")

>[!IMPORTANT]
>
>AI によって生成された応答は、不正確であったり、誤解を招く可能性があります。 コストや労力に影響を与える決定に使用する前に、常に回答とソースを検証します。

## クエリの例

キャンペーン管理、最適化、オーディエンス管理、取引、レポートおよびその他の製品機能について確認できます。 例えば、次のようなものがあります。

* 広告をプレースメントに添付するにはどうすればよいですか？

* プレースメント設定で様々なペーシングオプションを使用すると、どのような結果になりますか？

* 各タイプの最適化目標を使用するのは、どのような場合ですか？

* プログラム保証（PG）プレースメントがインプレッションを提供しないのはなぜですか？

* 世帯レベルのデータを含むレポートはどれですか？

* [!DNL Creative] でのターゲット設定されたエクスペリエンスと、ターゲット設定されていないエクスペリエンスの違いは何ですか？

* [!DNL Creative] エクスペリエンス用の広告タグを作成するにはどうすればよいですか？

## クエリの送信

複数の質問を 1 つのメッセージで行うことができますが、一度に行えるのは 1 つのメッセージのみです。 別の応答を送信する前に応答を待ちます。

1. ページの右上で、「![Agentic Chat](/help/dsp/assets/agent-chat.png "Agentic chat")」をクリックします。

1. クエリを入力し、「![&#x200B; プロンプトの送信 &#x200B;](/help/dsp/assets/submit-prompt.png " プロンプトの送信 ") をクリックします。

   詳しくは、「[&#x200B; プロンプトの書き込み &#x200B;](#writing-prompts)」を参照してください。

   応答には、下部にインラインの引用文と **[!UICONTROL Documentation Sources]** リストが含まれます。 フォローアップの質問や提案も表示される場合があります。

1. （オプション）データソースとして使用するページを開くには、次のいずれかの操作を行います。

   * 番号付き引用をクリックします。

   * 「**[!UICONTROL Documentation Sources]**」をクリックして応答で引用されたすべてのページのリストを表示し、ページリンクをクリックします。

## 応答に関するフィードバックを提供

<!-- Not actionable in terms of improving page content -->

* [!UICONTROL Documentation Sources] リストの横：

   * 役に立つ回答については、![&#x200B; サムズアップ &#x200B;](/help/dsp/assets/thumbs-up.png " サムズアップ ") をクリックしてください。

   * 役に立たない回答については、「![&#x200B; サムズダウン &#x200B;](/help/dsp/assets/thumbs-down.png " サムズダウン ")」をクリックします。

## プロンプトの記述の基本 {#writing-prompts}

* **明確かつ具体的にする。** 完全な質問（「オンデマンド在庫を購入するにはどうすればよいですか？」）、タスクフレーズ（「オンデマンド在庫を購入する」）、またはトピックフレーズ（「オンデマンド在庫」）を使用します。

* 製品機能（「キャンペーン」や「取引」など **で可能な場合は、** UI 用語を一致させる」。

  一般的なアクション（「追加」、「添付」、「割り当て」など）では、同義語を使用できます。

* 結果を絞り込んだり広げたりする **詳細を追加**。 必要に応じて、フォローアップの質問で調整します。

* **句読点や大文字の使用について心配する必要はありません。ただし** 意味に影響が出る場合を除きます。
