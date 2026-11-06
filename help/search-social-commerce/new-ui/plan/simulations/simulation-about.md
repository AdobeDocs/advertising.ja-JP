---
title: シミュレーションについて
description: ポートフォリオシミュレーションの詳細。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
TQID: 'https://experienceleague.adobe.com/9B4gKrZnnUmgj0LzxwM2CIkJsIO9Pe9R8RDR4mAmIwo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '1241'
ht-degree: 0%
---
# シミュレーションについて

*Beta機能*

シミュレーションレポートには、さまざまなレベルの支出（コスト）および対応する日々の予算やその他の目標でポートフォリオに期待できる限界費用対目標額、コスト、クリック数、および目標値の見積もりが表示されます。 オプションで[ ビューをカスタマイズ ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)して、追加のトラフィック指標、シミュレーション設定、特定のシミュレーションタイプ （[!UICONTROL Weekly]または[!UICONTROL Custom]）のみを表示できます。

<!--
 Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## シミュレーションの種類

* 週次シミュレーションの自動化

* カスタムのユーザー生成シミュレーション

### 週次シミュレーションの自動化

Search, Social, &amp; Commerceでは、現在のポートフォリオ設定を使用して、毎週シミュレーションレポートが自動的に実行されます。 毎週の自動シミュレーションは、ポートフォリオが[最適化またはアクティブ ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)である期間にのみ使用できます。

[!UICONTROL Portfolios] ビュー](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations)から選択した実行日の最大100個のポートフォリオに対して毎週シミュレーションを[ ダウンロードするか、[!UICONTROL Simulations] ビュー](simulation-download.md)から個別のシミュレーションを[ ダウンロードできます。

#### 週次シミュレーションのダウンロード

毎週のシミュレーションを個別のワークブックとしてダウンロードしたり、1つのワークブックに組み合わせたりできます。 各シミュレーションのレポートには、20のステップレベルのそれぞれの目標と、対応する目標に基づいて、目標の予測コスト、クリック数、加重収益（目標値）、コンバージョン指標が含まれます。 シミュレーションでは、制約のない最初の20個のデータ行と、制約のある残りのデータ行が計算されます。

#### 画面上の週次シミュレーションの詳細

画面上のシミュレーションの詳細では、ポートフォリオレベルの視覚的および表形式のインサイトが表示されます。 キャンペーン、広告グループ、入札単位、またはデバイス別のデータの場合は、代わりに[ シミュレーションをダウンロード ](simulation-download.md)してください。

##### グラフビュー

グラフ ビューには、20の各支出レベルの支出目標に対する期待目標値またはその他の指定された指標（[!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->）が表示されます。 グラフはターゲットの中間点を識別します。オプションでターゲットの中間点を変更して、その値を使用して予測データを表示できます。 グラフ内の任意のポイントにカーソルを合わせると、そのポイントのデータが表示されます。

制約を含むデータ、制約を含まないデータ、またはその両方を表示できます。 制約を含むデータを表示すると、グラフの上にある制約がビューによって識別されます。

##### テーブルビュー

テーブルビューには、20の各支出レベルの目標支出が表示されます。 また、各支出レベルに対するポートフォリオの目標には、対応する見積もりコスト、目標値までの限界費用、クリック数、目標値、コンバージョン指標が含まれます。 表はターゲット中間点を識別します。オプションで、その値を使用して予測データを表示するようにターゲット中間点を変更できます。

制約を含むデータ、制約を含まないデータ、またはその両方を表示できます。 制約を含むデータを表示すると、グラフの上にある制約がビューによって識別されます。

##### シミュレーション設定

ビューには、グラフまたはテーブルの下に読み取り専用のシミュレーション設定が表示されます。

##### Portfolioの設定

該当するポートフォリオの読み取り専用の設定を表示するには、右上の「**[!UICONTROL Portfolio Settings]**」をクリックします。

### カスタムのユーザー生成シミュレーション

現在のポートフォリオ設定を使用するか、入札単位レベルの制約が適用されている場合とない場合に、カスタムポートフォリオ設定を使用して、単一の[最適化またはアクティブな](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) ポートフォリオのカスタムシミュレーションレポートを作成し、これらの設定が実際に変更せずに生成する結果を確認できます。 例えば、カスタムシミュレーションを作成して、ポートフォリオの入札単位に関するアクティブな制約を考慮せずに、異なる支出戦略や学習予算を使用した効果を確認できます。 ポートフォリオ、キャンペーン、入札単位、およびデバイスレベルで推定パフォーマンスを表示できます。

#### カスタムシミュレーションのダウンロード

カスタムシミュレーションは、個別のワークブックとしてダウンロードすることも、1つのワークブックに組み合わせることもできます。 各シミュレーションのレポートには、そのレベルでデータが使用可能な場合に指定するエンティティ レベル（ポートフォリオ、キャンペーン、広告グループ、入札単位）ごとに1つのワークシートが含まれます。 デバイスレベルのデータを指定すると、各ワークシートには[!UICONTROL Device]列が含まれます。 各ワークシートには、該当するエンティティごとに1行が含まれ、デバイスレベルのデータをリクエストする場合、20のステップごとに1行ずつデバイスタイプが含まれます（例：キャンペーンごとに1行）。 各行のデータには、対応するターゲットに基づいて、予測される限界売上原価、コスト、クリック数、加重収益（目標値）、デバイスタイプ、および目標内のコンバージョン指標が含まれます。 ポートフォリオレベルのワークシートには、ステップレベルのターゲットも含まれ、エンティティレベルのワークシートには、広告ネットワーク、アカウント、キャンペーン、および（該当する場合）広告グループも含まれます。  <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### 画面上のカスタムシミュレーションの詳細

画面上のシミュレーションの詳細では、ポートフォリオレベルの視覚的および表形式のインサイトが表示されます。 キャンペーン、広告グループ、入札単位、またはデバイス別のデータの場合は、代わりに[ シミュレーションをダウンロード ](simulation-download.md)してください。

#### グラフビュー

グラフ ビューには、シミュレーションに指定された費用レベル （ステップ）の費用ターゲットの予想目標値またはその他の指定された指標（[!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->）が表示されます。 このグラフはターゲットの中間点を示しています。 グラフ内の任意のポイントにカーソルを合わせると、そのポイントのデータが表示されます。

シミュレーションで制約が考慮される場合、ビューはグラフの上の制約を識別します。

##### テーブルビュー

テーブルビューには、シミュレーションに指定された支出レベル（ステップ）の各支出の目標支出が表示されます。 また、各支出レベルに対するポートフォリオの目標に、対応する見積もりコスト、目標値への限界費用、クリック数、目標値、コンバージョン指標が表示されます。 この表は、ターゲットの中間点を示しています。

シミュレーションで制約が考慮される場合、ビューはグラフの上の制約を識別します。

##### シミュレーション設定

ビューには、グラフまたはテーブルの下に読み取り専用のシミュレーション設定が表示されます。

##### Portfolioの設定

該当するポートフォリオの読み取り専用の設定を表示するには、右上の「**[!UICONTROL Portfolio Settings]**」をクリックします。

## [!UICONTROL Simulations] ビュー

[!UICONTROL Simulations] ビューには、週次シミュレーションとカスタムシミュレーションが一覧表示されます。 管理者と他のユーザーの種類<!-- Verify which -->は、他のユーザーが作成したカスタム シミュレーションを表示できます。 他のすべてのユーザーは、作成したカスタムシミュレーションのみを表示できます。

データテーブルには、各シミュレーションの進行状況、各行の[!UICONTROL Target Midpoint]、コスト/インプレッション/クリック/目標値の予測、実際の値、精度の列が表示されます。 必要に応じて、カスタム列を追加できます（実際の目標値をコストで割ったリフト指標を含む）。

### 使用可能なアクション {#simulations-actions}

* [予測インプレッション、実際のコスト、クリック数、インプレッション数、目標値、コスト対目標値、コストの正確性、クリック精度、目標値の正確性、予測値と実際の目標値と目標値の差分（差分）などの追加指標を含めるように、ビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)をカスタマイズします。 ほとんどのシミュレーション設定とシミュレーションの種類（[!UICONTROL Custom]または[!UICONTROL Weekly]）の列を含めることもできます。

* [ ポートフォリオの現在の設定をデフォルトとして使用して、単一のポートフォリオのカスタムシミュレーション ](simulation-create.md#simulation-create)を生成します。

* [既存の設定で最大10件のシミュレーションを再実行します](simulation-create.md#rerun-a-simulation-with-the-existing-settings)。 Search, Social, &amp; Commerceは、ステータスが[!UICONTROL Queued]または[!UICONTROL In Progress]のシミュレーションをスキップします。

* [週ごとのシミュレーションまたはカスタムシミュレーションを画面に表示](simulation-view.md)。

* [最大10個の週次およびカスタムシミュレーション ](simulation-download.md)を1つの[!DNL Microsoft Excel] ワークブックとして、またはZIP ファイル内の個別のワークブックとしてダウンロードできます。

* [!UICONTROL Spend Planner] ボタンを使用して、従来の予算分配の推奨ツールを開きます。これは、ポートフォリオ全体で最適な予算配分を特定するのに役立ちます。

## ベストプラクティス

次の状況でシミュレーションレポートを監視します。

* ポートフォリオを起動する前に、対応するポートフォリオ設定で期待できるパフォーマンスを見積もることができます。少なくとも2週間のデータを使用してください。 シミュレーション結果が、含まれるキャンペーンの過去データに基づいて予想よりもパフォーマンスが低いことを示している場合は、ポートフォリオを起動する前に、問題を調査して解決します。

* キャンペーンの追加や目的の変更など、ポートフォリオに大きな変更があった後。 ポートフォリオのモデリング開始日、コンバージョン指標の重み付け、目標のクリック値に変更を加えた場合は、17:00 PST後の次の日まで待って、更新されたコストと収益モデルが使用可能な場合にシミュレーションを実行します。

* コンバージョン指標レベルでパフォーマンスの傾向を定期的に監視します。

>[!MORELIKETHIS]
>
>* [ シミュレーションの実行または再実行](simulation-create.md)
>* [ シミュレーションの詳細を表示](simulation-view.md)
>* [ シミュレーションのダウンロード ](simulation-download.md)
