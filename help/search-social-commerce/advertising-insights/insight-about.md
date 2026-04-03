---
title: '[!UICONTROL Advertising Insights]について'
description: 使用可能な[!UICONTROL Advertising Insights]の種類について説明します。
exl-id: e6eec71e-04ab-4180-95f2-da31a26e5c1a
feature: Search Advertising Insights
TQID: https://experienceleague.adobe.com/AgAYE5bBGkWgk70jeKCTxzEOINvfsWXK9tnjytRc83c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1354
ht-degree: 0%

---

# [!UICONTROL Advertising Insights]について

アクティブなキャンペーンを含む、最適化されたアクティブなポートフォリオに関する視覚的で実用的なデータを[!UICONTROL Advertising Insights]件ご提示ください。

各insightはオンデマンドで生成され、出力はダウンロード可能なファイルまたは画面上のレポートです。 生成されたinsight ファイルのインスタンスを削除できます。

## [!UICONTROL Advertising Insights]の種類

| Insight | 説明 |
| --- | --- |
| [!UICONTROL AMO-AA Tracking Discrepancy] | （Adobe AdvertisingとAdobe Analyticsの統合を持つ広告主のみ）トラッキングの問題を特定します。この問題は、通常のバリエーションの外にあるクリックトゥインスタンスの比率または20%以上のバリエーションを持つ日数で特徴づけられます。 レポートには以下が含まれます。<ul><li>データの分散の概要を含む[!DNL Microsoft PowerPoint] ファイル、最もトラッキングの問題があるキャンペーンのキャンペーンごとの分散を示す表とトレンドチャート、トラブルシューティングの提案、レポート手法の説明。</li><li>ポートフォリオの各キャンペーンの概要データと、各キャンペーンの過去1か月の日別データが含まれた[!DNL Microsoft Excel] ファイル。</li></ul> |
| [!UICONTROL Attribution Analysis] | （[!DNL PowerPoint] プレゼンテーション形式）別のアトリビューションモデルが、単一のポートフォリオの収益モデルと最適化を改善できるタイミングを示します。 |
| [!UICONTROL Campaign Caps] | （[!DNL PowerPoint] プレゼンテーション形式）過去30日間の1つのポートフォリオの支出がキャンペーン予算上限によって制限されたかどうかを示し、最適な投資収益率を達成するためにポートフォリオ設定を調整することを推奨します。 |
| [!UICONTROL Day of Week] | （[!DNL PowerPoint] プレゼンテーション形式）過去30日間の曜日（DOW）ごとの単一のポートフォリオのパフォーマンスを示し、投資収益率を高めるためにDOWの支出目標を推奨します。<br><br>**メモ：**&#x200B;十分な支出がないポートフォリオ、または過去2日間にターゲットに使用できなかったポートフォリオは、insightでは利用できません。 |
| [!UICONTROL Delayed Revenue] | ポートフォリオのコンバージョンラグ（広告クリックとその後のコンバージョンの間に経過した時間）を測定し、ラグによる加重収益（現在は「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれています）、ROI、モデル精度の違いを示します。 この分析では、クリック日に起因するパフォーマンス指標の最近の変更を検出し、クリック日とトランザクション日によるレポートの影響を確認できます。<br><br>insightには、[!DNL Excel]個のワークブックが含まれており、重み付けされた売上（現在では「目標値」と呼ばれています）、売上の正確性、ラグ要因に関する個別のシートが含まれています。 また、様々なグラフを含む[!DNL Powerpoint] ファイルも含まれます。 |
| [!UICONTROL Event Path] | イベントパスとマルチタッチコンバージョンを分析することで、さまざまなチャネルやキャンペーンがどのようにコンバージョンを促進しているのかを特定できます。 XLSXおよびZIP （圧縮XLSX）形式でファイルをアップロードし、a）イベントを抽出するか、b）分類されたイベントを分析できます。 |
| [!UICONTROL Google Account Audit] | （[!DNL Google Ads] アカウントの場合、プリセールスに最も便利）アカウントのパフォーマンスの概要を提供し、欠陥部分を強調表示して、そのアカウントが効果的に管理されていることを示します。 監査には、入札、照合タイプ、予算上限、曜日のパフォーマンス、モバイルパフォーマンスなどに関する情報が含まれます。 Insightを生成するには、[!DNL Google Ads] web ユーザーインターフェイスから1） [!DNL Google Ads] キャンペーン、キーワード、変更履歴レポートをアカウントにアップロードし、b） [!DNL Google Ads Editor] アプリケーションからアカウントのバルクシート ファイルをアップロードする必要があります。 すべてのファイルは、CSV、TSV、TXT、またはZIP （圧縮CSV、TSV、またはTXT）形式である必要があります。<br><br>このinsightは、Search, Social, &amp; Commerceを利用して、潜在顧客がパフォーマンスを向上させ、分析で強調された欠陥に対処する方法を理解するのに役立ちます。 また、Adobe アカウントチームは、insightを使用して、お客様が正式にオンボーディングする前にアカウントを評価することもできます。 |
| [!UICONTROL Impression Share Lost] | （[!DNL PowerPoint] プレゼンテーション形式）ポートフォリオの予算で[!DNL Google Ads] キャンペーンのインプレッションのシェアが制限されている場合を示し、それに応じて予算とキャンペーン「[!UICONTROL Multiple]」設定の変更を推奨します。 |
| [!UICONTROL Location Target Performance] | （[!DNL Google Ads] キャンペーンの場合；[!DNL Excel] スプレッドシート形式） 1つのポートフォリオ内の各場所ターゲットの入札調整、クリック数、コスト、および加重収益（現在は「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれます）です。 過去90日以内であれば、あらゆる日付範囲のデータを利用でき、各キャンペーンの日々の結果や概要を確認できます。 |
| [!UICONTROL Match Type] | 過去90日間までの単一のポートフォリオのマッチタイプ間のコストと重み付けされた収益（現在は「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれています）の画面チャート。 |
| [!UICONTROL Mobile Optimization] | （[!DNL PowerPoint] プレゼンテーション形式）過去30日間のデバイスタイプ別の単一ポートフォリオのパフォーマンスを表示し、モバイル固有の最適化機能の現在の設定を評価し、設定の調整を推奨します。 |
| [!UICONTROL Model Accuracy] | Search, Social, &amp; Commerceが、単一のアクティブなポートフォリオまたは最適化されたポートフォリオの支出と収益をどの程度予測できるかを特定し、モデルの不正確さの原因を特定します。 レポートには以下が含まれます。<ul><li>過去7日間の予測および実際のコスト、クリック単価（CPC）、クリック単価（RPC）、収益、クリック単価（RPC）、投資収益率（ROI）の概要を含む[!DNL PowerPoint] ファイル。前月の過剰支出および過小支出の入札単位に関するデータを集約したトレンド チャート。コストモデルの精度、収益モデルの精度、および前月の予測コスト、クリック単価、収益、RPC、ROIを示すトレンド チャート。</li><li>各キーワードのモデル精度と日別モデル精度を含む[!DNL Excel] ファイル。</li></ul>このinsightでは、[!UICONTROL Portfolios] ビューから利用できるポートフォリオレベルのモデル精度レポートよりも詳細が提供されます。 |
| [!UICONTROL Normalized Sim (Combined)] | 複数のポートフォリオについて、指定された数のターゲット支出レベル（ステップ）に対する最適な支出配分を返します。 このinsightは、指定された期間の週次シミュレーションに基づいて、正規化された加重収益（現在は「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれます）を使用します。 選択したポートフォリオごとに個別のシミュレーションを生成することも、同じ目的と通貨を持つ複数のポートフォリオにまたがる単一のシミュレーションを生成することもできます。 シミュレーションはスプレッドシートに表示されます。<br><br>単一のマルチポートフォリオシミュレーションの場合、スプレッドシートには2つのシートが含まれます。1）各目標支出レベル（ステップ）の正規化された加重収益（「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれます）を示すトレンドチャートと、2）該当する支出レベル（ステップ）ごとに1行を示すテーブル。 個々のポートフォリオシミュレーションの場合、スプレッドシートには、1）該当するすべてのポートフォリオと期間を一覧表示する概要シートと2）各ポートフォリオに対する2つのシートが含まれます。a）目標支出レベルごとに正規化された加重収益（現在は「[目標値](/help/search-social-commerce/glossary.md#o-p)」と呼ばれます）を示すトレンドチャート（step）とb）該当する支出レベルごとに1つの行を示すテーブル（step）。 |
| [!UICONTROL Portfolio Launch] | （[!DNL PowerPoint] プレゼンテーション形式）ポートフォリオを起動する準備ができているかどうか（「最適化」ステータスに変更）を識別します。 このレポートには、予測パフォーマンスと実際のパフォーマンスの比較、推奨されるポートフォリオ開始日とコストと収益の予測から除外する日付のリスト、コスト、収益、コストあたりの収益、コンバージョンのキーワードの推移、過去2週間に支出が上限に達したキャンペーンに関する情報、ローンチまたはローンチしない推奨事項が含まれます。 |
| [!UICONTROL Quality Score] | 過去90日間のインプレッション数が[!DNL Google Ads]または[!DNL Microsoft Advertising]のキーワードの品質スコアの傾向を表示します。 これには、a） [!DNL PowerPoint] ファイルとb） [!DNL Excel] ファイルが含まれ、最も費用の高い100 キーワードと、品質スコアの低い上位100 キーワード（該当する場合）が含まれます。<br><br>**メモ：**<ul><li>ポートフォリオに20,000個を超える入札ユニットがある場合、過去30日間（90日間ではなく）にクリック数が1回を超えたキーワードのみが含まれます。</li><li>多くのキーワードでデータを使用したインサイトは、生成に時間がかかります。</li></ul> |
| [!UICONTROL Query Cross Matching] | （[!DNL Google Ads] アカウント）は、[!DNL Google Ads]が複数のキーワードに一致する検索クエリのインスタンスを識別し、トラフィックの転送先に関する提案を提供します。 提案を使用して、キーワードパフォーマンスを向上させ、その結果、モデルの精度を向上させます。<br><br>insightには、一致するクエリ、一致したキーワード、パフォーマンス データのスプレッドシート、一致するクエリとキーワードの関係を視覚化するネットワーク図、基になる検索クエリ レポート、データの解釈方法に関する情報が含まれています。 |
| [!UICONTROL Settings Audit] | ポートフォリオがベストプラクティスごとに設定されているかどうかを示します。 次の内容を含みます。<ul><li>すべてのポートフォリオとそのコンポーネントキャンペーンの主要な設定がベストプラクティスごとに構成されているかどうか、キャンペーンがポートフォリオに割り当てられていないかどうか、ベストプラクティスからの逸脱の結果を示す[!DNL PowerPoint] ファイル。</li><li>キーポートフォリオ設定とキーキャンペーン設定ごとに個別のタブを持つ[!DNL Excel] ファイル。 データには、各ポートフォリオのポートフォリオ設定と、ベストプラクティスを満たさない各キャンペーンのキャンペーン設定が含まれます。</li></ul> |
| [!UICONTROL Time-of-day Analysis] | （検索、ディスプレイ、またはショッピングキャンペーンが[!DNL Google Ads]件あるポートフォリオにのみ適用） 1つのポートフォリオの時間単位のパフォーマンスに基づいて、1日の異なる時間に対して[!DNL Google Ads]個のキャンペーンレベルの入札修飾子（広告スケジュール入札修飾子）を提案します。<br><br>insightには、[!DNL Excel] （施策ごとの時間間隔によるパフォーマンス）および[!UICONTROL Detailed Performance] （施策ごとに推奨される広告スケジュール）の個別のシートを含む[!UICONTROL Recommended TBAs] ワークブックが含まれています。 [!UICONTROL Recommended TBAs] シートを直接[!DNL Google Ads] エディターに書き出すことができます。 Insightには、データと説明をサポートする[!UICONTROL Powerpoint] ファイルも含まれています。 |

>[!MORELIKETHIS]
>
>* [を生成 [!DNL Advertising Insight]](insight-generate.md)
>* [を表示または保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [を削除 [!DNL Advertising Insight]](insight-delete.md)
