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
source-git-commit: 41d3ab985831a1432e775277384661643a9f55c4
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%
---
# Advertising DSPのAI アシスタントについて

DSPのAI アシスタントは、DSPで利用可能なあらゆるエージェント型ワークフローを、単一のチャットボックスから実行できる会話型インターフェイスです。 新しいタスクを作成したり、以前のタスクを続行するために助けを求めたりできます。

会話の履歴は、すべてのワークフローに対して保持され、会話ごとに自動的に名前が付けられます。 クエリは他のユーザーと共有されません。

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## サポートされているワークフロー

次のワークフローは、より効果的に作業を達成するのに役立ちます。

<!-- And links to all sections/pages -->

| 機能 | 説明 | 回答数 |
| --- | --- | --- |
| [ トラブルシューティング ](troubleshooting-agent.md) | （Beta機能）ライブパッケージとプレースメントのパフォーマンスと配信の問題を診断します。 | 応答には、パフォーマンスを制限する要因が含まれ、問題を解決するためのステップバイステップの指示と推奨事項が提供されます。 |
| [ インサイト ](insights-agent.md) | （Betaの機能） レポートを手動で作成することなく、キャンペーンの指標と完全なレポートを取得します。 結果はCSV ファイルとしてダウンロードできます。 | レポートの最初の数行が表示され、レポート全体をプレビューするためのリンクと、レポートを[!DNL Microsoft Excel] コンマ区切りの値ファイル （.csv）としてダウンロードするためのリンクが表示されます。 |
| [製品ドキュメント検索](documentation-search.md) | [Advertising DSP ガイド ](/help/dsp/home.md)で概念的なコンテンツとハウツーのコンテンツを検索し、Advertising Creativeを使用している広告主については、[Advertising Creative ガイド ](/help/creative/home.md)を検索します。 | 応答には、インラインの引用と下部の拡張可能な[!UICONTROL Documentation Sources] リストが含まれています。 任意の引用またはソースリストをクリックして、関連するページを開きます。<br><br>応答には、質問を絞り込み、詳細な情報を見つけるのに役立つフォローアップの質問や提案が含まれる場合もあります。 |

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
