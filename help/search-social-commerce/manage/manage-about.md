---
title: キャンペーンとポートフォリオの管理について
description: 広告ネットワークアカウント、キャンペーン、トラッキング、ポートフォリオ最適化の連携の仕組み、パフォーマンスの監視および改善方法について説明します。
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# キャンペーンとポートフォリオの管理について

*Beta機能*

Search, Social, &amp; Commerceは、キャンペーン管理、パフォーマンスレポート、ポートフォリオ最適化をひとつのインターフェイスにまとめます。 広告ネットワークとキャンペーンのタイプに応じて、キャンペーンデータの同期、キャンペーンコンポーネントの作成と編集、コンバージョンの追跡、入札、予算、入札戦略のターゲットの最適化を行うことができます。 各広告ネットワークで利用できる機能については、[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)を参照してください。

[!UICONTROL Manage] メニューでは、アカウント、キャンペーン、広告グループ、広告、キーワード、製品グループ、ポートフォリオにアクセスできます。 権限によって、使用可能なビューとアクションが決まります。 メニューの完全な整理については、「[ ユーザーインターフェイスの整理の方法](/help/search-social-commerce/getting-started/user-interface.md)」を参照してください。

## アカウント、施策、ポートフォリオを連携する方法

* **広告ネットワークアカウント**&#x200B;は、広告主のデータをSearch, Social, &amp; Commerceに接続します。 [ アカウントタイプ ](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)には、API接続で同期されたアカウント、データをアップロードするアカウント、テンプレートベースのトラッキング専用アカウントが含まれます。 アカウントタイプは、データの同期、キャンペーンの管理、ポートフォリオ最適化の使用のいずれができるかを決定します。

* **キャンペーン**&#x200B;には、広告の配信に使用される広告やその他のコンポーネントが含まれています。 サポートされているキャンペーンの種類については、[ キャンペーン ](/help/search-social-commerce/manage/campaigns/campaign-manage.md)とそのコンポーネントを[!UICONTROL Manage] ビューから作成および管理できます。 サポートされている一括操作には、[ バルクシート ](/help/search-social-commerce/set-up/bulksheets/about.md)を使用することもできます。

* **ポートフォリオ**&#x200B;は、共通のビジネス目標と予算またはパフォーマンス目標に向けてキャンペーンを最適化するために、対象となるキャンペーンをグループ化します。 キャンペーンは1つのポートフォリオにのみ属することができ、ポートフォリオ内のすべてのキャンペーンは同じ通貨を使用する必要があります。 「[ ポートフォリオについて](/help/search-social-commerce/manage/portfolios/portfolio-about.md)」を参照してください。

Portfolioの割り当てはオプションです。 キャンペーンをポートフォリオに割り当てることなく、キャンペーンを追跡し、レポートを作成できます。 すべての広告ネットワーク、キャンペーンの種類、入札戦略がポートフォリオの最適化をサポートしているわけではありません。

## キャンペーンデータの同期

APIを介して接続されたアカウントの場合、Search, Social, &amp; Commerceは、広告ネットワークからサポートされているキャンペーン構造とパフォーマンスデータを取得します。 Search、Social、およびCommerceでサポートされているキャンペーンコンポーネントに加えた変更は、広告ネットワークに送信されます。

必要に応じて、[手動同期をリクエストできます](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md)。 アカウントの同期が停止した場合は、その[認証とアクセス状態](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status)を確認します。

データアップロードアカウントとトラッキング専用アカウントが広告ネットワークと同期しない。 [ アカウントタイプ ](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)のワークフローに従って、キャンペーンとパフォーマンスデータを提供します。

## トラッキングと最適化の設定

[ トラッキング ](/help/search-social-commerce/tracking/tracking-about.md)は、キャンペーンアクティビティを、ビジネスにとって重要なコンバージョンに結び付けます。 コンバージョンデータは、導入によって、Adobe Advertisingタグ、Adobe Analyticsとの統合、ネットワークトラッキング、データフィードなどから取得される場合があります。 クリックの追跡とコンバージョンの追跡を実装に必要に応じて設定し、データを検証してから最適化に使用します。

[!UICONTROL Goals] > [!UICONTROL Conversions]では、広告主が追跡したコンバージョン指標を[ レビューし、その表示を制御できます](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md)。 [目標](/help/search-social-commerce/goals/objectives/objective-about.md)で適切な指標を使用します。

ポートフォリオ最適化を有効にするには、[ ポートフォリオを作成し](/help/search-social-commerce/manage/portfolios/portfolio-create.md)、目的と対象となるキャンペーンを割り当て、支出と最適化の設定を行います。 アクティブなポートフォリオは、パフォーマンスデータを収集し、モデル化します。 データと設定の準備ができたら、[ ポートフォリオステータスを最適化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)に変更して最適化を開始します。 実行されるアクションは、ポートフォリオの種類と[ キャンペーン入札戦略](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)によって異なります。

設定シーケンスの詳細については、「[広告ネットワークアカウントとキャンペーンの設定](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)」を参照してください。

## キャンペーンとポートフォリオのパフォーマンスを監視 {#monitor-performance}

アカウントチーム、代理店、広告主は、SLAの条件に従って、パフォーマンスを監視し、調整を行う責任があります。 ルーティンワーク：

* [!UICONTROL Manage] ビューでキャンペーンとアカウントのパフォーマンスを確認します。 [列、フィルター、日付範囲](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)をカスタマイズして、重要な指標とエンティティに焦点を当てることができます。

* [!UICONTROL Dashboard] > [!UICONTROL Overview]を使用して、[ ポートフォリオの傾向とパフォーマンスの変化を監視します](/help/search-social-commerce/dashboard/dashboard-overview.md)。

* 調査が必要な条件については、[ カスタムアラート ](/help/search-social-commerce/common-tasks/alerts-manage.md)を確認してください。

* [ キャンペーン、キーワード、広告、ポートフォリオのパフォーマンスに関するレポート ](/help/search-social-commerce/reports/management/report-manage.md)を生成します。 ポートフォリオについては、実際のパフォーマンスとモデルの精度を含む[ パフォーマンスの詳細](/help/search-social-commerce/manage/portfolios/portfolio-details.md)を確認します。

* [ シミュレーション ](/help/search-social-commerce/plan/simulations/simulation-about.md)を使用して、様々な支出レベルの予測効果を評価します。

* 報告されたコンバージョンとソースデータの違いを調査します。 関連リンクの[!DNL Google Ads]および[!DNL Microsoft Advertising]のコンバージョンデータに関するガイダンスを参照してください。

## キャンペーンとポートフォリオを調整する

パフォーマンスやビジネス目標の変化にもとづいて、次のことをおこなう必要があります。

* キャンペーン設定の編集、キャンペーンコンポーネントの作成または一時停止、キーワードセットの調整、様々な広告のテストを行えます。 利用できるアクションは、広告ネットワークとキャンペーンのタイプによって異なります。

* 関連する管理ビューとレポートを使用して、地理的、オーディエンス、プレースメントのターゲティングを確認できます。

* 別のポートフォリオでキャンペーンを最適化する必要がある場合は、[ キャンペーンの割り当てを変更](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)します。 キャンペーンを別のポートフォリオに割り当てると、以前のポートフォリオから削除されます。

* [製品プロファイルで許可されている、目的、支出戦略、制約、最適化制御などのポートフォリオ設定](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)を編集します。

* パフォーマンスの変更を調査するときは、[変更履歴](/help/search-social-commerce/reports/history-logs.md)を確認してください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンを設定](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)
>* Search, Social, &amp; Commerceの[[!DNL Google Ads]  コンバージョンデータ ](/help/search-social-commerce/tracking/google-conversion-data.md)
>* Search, Social, &amp; Commerceの[[!DNL Microsoft Advertising]  コンバージョンデータ ](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
