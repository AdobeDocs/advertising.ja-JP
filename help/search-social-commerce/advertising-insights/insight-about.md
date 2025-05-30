---
title: '[!UICONTROL Advertising Insights] について'
description: 利用可能な [!UICONTROL Advertising Insights] の様々なタイプについて説明します。
exl-id: e6eec71e-04ab-4180-95f2-da31a26e5c1a
feature: Search Advertising Insights
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---

# [!UICONTROL Advertising Insights] について

アクティブなキャンペーン [!UICONTROL Advertising Insights] 含む、最適化されたアクティブなポートフォリオに関するアクションにつながる視覚的なデータを表示します。

各インサイトはオンデマンドで生成され、出力はダウンロード可能なファイルまたはオンスクリーンレポートになります。 インサイトファイルの生成されたインスタンスを削除できます。

## [!UICONTROL Advertising Insights] のタイプ

| インサイト | 説明 |
| --- | --- |
| [!UICONTROL AMO-AA Tracking Discrepancy] | （Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主）トラッキングの問題を識別します。この問題は、クリック対インスタンスの割合が標準平方偏差を超えている日か、平方偏差が 20% 以上ある日によって特徴付けられます。 このレポートの内容は次のとおりです。<ul><li>データの相違の概要を含む [!DNL Microsoft PowerPoint] ファイル、最もトラッキングの問題が多いキャンペーンに関するキャンペーンごとの相違を示すテーブルとトレンドグラフ、トラブルシューティングの提案、レポート方法の説明。</li><li>ポートフォリオ内の各キャンペーンの概要データと、各キャンペーンの過去の月の日別データを含む [!DNL Microsoft Excel] ファイル。</li></ul> |
| [!UICONTROL Attribution Analysis] | （[!DNL PowerPoint] プレゼンテーション形式）異なるアトリビューションモデルが、単一のポートフォリオの収益モデルと最適化を向上できるタイミングを示します。 |
| [!UICONTROL Campaign Caps] | （[!DNL PowerPoint] プレゼンテーション形式）過去 30 日間の単一ポートフォリオの支出がキャンペーン予算の上限によって制限されているかどうかを示し、最適な投資回収率を達成するために、ポートフォリオ設定の調整を推奨します。 |
| [!UICONTROL Day of Week] | （[!DNL PowerPoint] プレゼンテーション形式）過去 30 日間のポートフォリオの日別パフォーマンス（DOW）を示し、投資収益率を高めるために DOW の支出目標を推奨します。<br><br>**メモ：** 十分な費用がないPortfolioや、過去 2 日間にターゲットを設定するために費用をかけることができなかったアセットは、インサイトでは使用できません。 |
| [!UICONTROL Delayed Revenue] | ポートフォリオのコンバージョンラグ（広告クリックと後続のコンバージョンの間の経過時間）を測定し、ラグによる加重収益（「目標値 [ と呼ばれるようになりました）、ROI](/help/search-social-commerce/glossary.md#o-p) およびモデル精度の違いを表示します。 この分析により、クリック日に関連付けられたパフォーマンス指標の最近の変更を検出し、クリック日とトランザクション日の比較でレポートの影響を確認できます。<br><br> インサイトには、重み付け収益（「目標値」と呼ばれるようになりました）、収益の精度、ラグ係数に関する個々のシートを持つ [!DNL Excel] ワークブックが含まれています。 また、様々なグラフを持つ [!DNL Powerpoint] ファイルも含まれています。 |
| [!UICONTROL Event Path] | イベントパスとマルチタッチコンバージョンを分析することで、様々なチャネルとキャンペーンがどのようにコンバージョンを促進するかを特定します。 XLSX および ZIP （圧縮 XLSX）形式のファイルをアップロードし、a） イベントを抽出するか、b）分類されたイベントを分析できます。 |
| [!UICONTROL Google Account Audit] | （[!DNL Google Ads] アカウントの場合。プリセールスで最も役立つ）アカウントのパフォーマンスの概要と問題点を示し、アカウントがどのくらい効果的に管理されているかを示します。 監査には、入札、一致タイプ、予算のキャッピング、曜日のパフォーマンス、モバイルのパフォーマンスなどに関する情報が含まれます。 インサイトを生成するには、1） [!DNL Google Ads] web ユーザーインターフェイスからアカウントの [!DNL Google Ads] キャンペーン、キーワード、変更履歴レポートをアップロードし、b） [!DNL Google Ads Editor] アプリケーションからアカウントのバルクシートファイルをアップロードする必要があります。 すべてのファイルは、CSV、TSV、TXT、または ZIP （圧縮された CSV、TSV、TXT）形式である必要があります。<br><br> このインサイトは、見込み客が検索、ソーシャル、Commerceによってパフォーマンスを向上させる方法と、分析で明らかになった欠陥に対処する方法を理解するのに役立ちます。 Adobeアカウントチームは、お客様に正式にオンボーディングする前に、インサイトを使用してアカウントを評価する場合もあります。 |
| [!UICONTROL Impression Share Lost] | （[!DNL PowerPoint] 表示形式）ポートフォリオの予算によって [!DNL Google Ads] キャンペーンのインプレッションシェアが制限された場合に、それに応じて予算とキャンペーン「[!UICONTROL Multiple]」設定の変更が推奨されます。 |
| [!UICONTROL Location Target Performance] | （[!DNL Google Ads] キャンペーンの場合、[!DNL Excel] スプレッドシート形式）単一のポートフォリオ内の各場所目標の入札調整、クリック数、コストおよび重み付け収益（現在は「[ 目標値 ](/help/search-social-commerce/glossary.md#o-p)」と呼ばれています）。 データは、過去 90 日間の任意の日付範囲で使用でき、毎日の結果や各キャンペーンの概要を表示できます。 |
| [!UICONTROL Match Type] | 過去 90 日間にわたって、1 つのポートフォリオ内の一致タイプをまたいだコストと重み付け収益（現在は「[ 目標値 ](/help/search-social-commerce/glossary.md#o-p)」と呼ばれています）のオンスクリーングラフ。 |
| [!UICONTROL Mobile Optimization] | （[!DNL PowerPoint] プレゼンテーション形式）過去 30 日間のデバイスタイプ別の単一ポートフォリオのパフォーマンスを表示し、モバイル固有の最適化機能の現在の設定を評価して、設定の調整を推奨します。 |
| [!UICONTROL Model Accuracy] | 検索、ソーシャル、Commerceが、1 つのアクティブまたは最適化されたポートフォリオの支出と売上高をどの程度予測するかを特定し、モデルの不正確さの原因を特定します。 このレポートの内容は次のとおりです。<ul><li>過去 7 日間の予測および実際のコスト、クリック数、クリック単価（CPC）、収益、クリック単価（RPC）および投資回収率（ROI）の概要、前月のコストモデルの精度、収益モデルの精度、前月の予測コスト、クリック数、CPC、収益、RPC および ROI と実際の値の比較を示すトレンドグラフ、クリックレベル別のモデル精度、支出の上限または超過入札単価、モデルのを改善する推奨事項のの [!DNL PowerPoint] ファイル。</li><li>各キーワードのモデル精度と日別のモデル精度を記載した [!DNL Excel] ファイル。</li></ul>このインサイトでは、[!UICONTROL Portfolios] ビューから利用できるポートフォリオレベルのモデル精度レポートよりも詳細な情報を提供します。 |
| [!UICONTROL Normalized Sim (Combined)] | 複数のポートフォリオに対して、指定された数のターゲット支出レベル（ステップ）の最適な支出配分を返します。 このインサイトでは、指定された期間の週別シミュレーションに基づいて、正規化された重み付け収益（現在は「[ 目標値 ](/help/search-social-commerce/glossary.md#o-p)」と呼ばれています）を使用します。 a）選択したポートフォリオごとに個別のシミュレーション、または b）同じ目的と通貨を持つ複数のポートフォリオをまたいだ単一のシミュレーションを生成できます。 シミュレーションは、スプレッドシートで表示されます。<br><br> 単一の複数ポートフォリオのシミュレーションの場合、スプレッドシートには、次の 2 つのシートが含まれています。1）各ターゲット支出レベル（ステップ）の正規化された加重収益（「[ 目標値 ](/help/search-social-commerce/glossary.md#o-p)」と呼ばれるようになりました）を示すトレンドグラフ、および 2）各適用可能な支出レベル（ステップ）の 1 行を示すテーブル。 個々のポートフォリオシミュレーションの場合、スプレッドシートには、（1）該当するすべてのポートフォリオと期間をリストした概要シート、（2）各ポートフォリオに対する 2 つのシート、（a）ターゲット支出レベル（ステップ）ごとに正規化された加重収益（「目標値 [&#128279;](/help/search-social-commerce/glossary.md#o-p)」と呼ばれるようになった ）を示すトレンドグラフ、（b）各該当する支出レベル（ステップ）に対して 1 行を示すテーブルが含まれています。 |
| [!UICONTROL Portfolio Launch] | （[!DNL PowerPoint] プレゼンテーション形式）ポートフォリオの起動準備ができているか（「最適化済み」ステータスに変更されているか）を識別します。 レポートには、予測されるパフォーマンスと実際のパフォーマンスの比較、推奨されるポートフォリオ開始日とコストおよび収益の予測から除外する必要がある日付のリスト、コスト、収益、コストあたりの収益および時間の経過に伴うコンバージョンキーワード、過去 2 週間に費用が制限されたキャンペーンに関する情報、ローンチまたはローンチ以外の推奨が含まれます。 |
| [!UICONTROL Quality Score] | 過去 90 日間に [!DNL Google Ads] または [!DNL Microsoft Advertising] のインプレッション数を含むキーワードの品質スコアのトレンドを表示します。 これには、a） [!DNL PowerPoint] ファイル、b）最も費用が高い 100 件のキーワードと（該当する場合）品質スコアが低い上位 100 件のキーワードを含む [!DNL Excel] ファイルが含まれます。<br><br>**注：**<ul><li>ポートフォリオに 20,000 を超える入札単位がある場合、過去 30 日間（90 日間ではなく）に複数のクリックが含まれているキーワードのみが含まれます。</li><li>多くのキーワードのデータを含むインサイトの生成に時間がかかる。</li></ul> |
| [!UICONTROL Query Cross Matching] | （[!DNL Google Ads] アカウント）複数のキーワードに一致す [!DNL Google Ads] 検索クエリのインスタンスを識別し、トラフィックを誘導する場所の候補を提供します。 提案を使用して、キーワードのパフォーマンスを向上させ、その結果、モデルの精度を向上させます。<br><br> インサイトには、クロス一致クエリ、一致したキーワード、パフォーマンスデータのスプレッドシート、クロス一致クエリとキーワードの関係を視覚化するのに役立つネットワーク図、基になる検索クエリレポート、データの解釈方法に関する情報が含まれています。 |
| [!UICONTROL Settings Audit] | ポートフォリオがベストプラクティスに従って設定されているかどうかを示します。 これには以下が含まれます。<ul><li>すべてのポートフォリオとそのコンポーネントキャンペーンの主要な設定がベストプラクティスに従って設定されているかどうか、キャンペーンがポートフォリオに割り当てられていないかどうか、ベストプラクティスからの逸脱の結果を示す [!DNL PowerPoint] ファイル。</li><li>主要なポートフォリオ設定と主要なキャンペーン設定ごとに個別のタブが付いた [!DNL Excel] ファイル。 データには、各ポートフォリオのポートフォリオ設定と、ベストプラクティスを満たさない各キャンペーンのキャンペーン設定が含まれます。</li></ul> |
| [!UICONTROL Time-of-day Analysis] | （検索、表示またはショッピングキャンペーンのみを含むポートフォリオ [!DNL Google Ads] のみ適用）は、単一のポートフォリオの時間別パフォーマンスに基づいて、1 日の異なる時間に対してキャンペーンレベルの入札修飾子を [!DNL Google Ads] 案（広告スケジュール入札修飾子）します。<br><br> インサイトには、[!UICONTROL Detailed Performance] （キャンペーンごとの時間間隔によるパフォーマンス）と [!UICONTROL Recommended TBAs] （キャンペーンごとの推奨広告スケジュール）の個々のシートを含む [!DNL Excel] ワークブックが含まれています。 [!UICONTROL Recommended TBAs] シートを [!DNL Google Ads] エディターに直接書き出すことができます。 インサイトには、サポートデータと説明を含む [!UICONTROL Powerpoint] ファイルも含まれています。 |

>[!MORELIKETHIS]
>
>* [ 生成  [!DNL Advertising Insight]](insight-generate.md)
>* [ アセットの表示または保存  [!DNL Advertising Insight]](insight-view-save.md)
>* [ を削除  [!DNL Advertising Insight]](insight-delete.md)
