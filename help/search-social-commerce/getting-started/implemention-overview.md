---
title: Search, Social, & Commerce導入の概要
description: ポートフォリオを起動および管理するための一般的なワークフローについて説明します。
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# Search, Social, &amp; Commerce導入の概要

[!DNL Adobe]またはそのアフィリエイトエージェンシーは、各広告主と協力してオンライン広告ポートフォリオを立ち上げ、追加の広告キャンペーンを追跡します。 最初のローンチ後、継続的な追加作業により、広告主の目標を継続的に達成できます。

Search, Social, &amp; Commerceを実装および使用するための一般的なワークフローを以下に示します。

## 初回起動

[!DNL Adobe]およびお客様の代理店が協力して次の操作を行います：

1. 上位レベルのビジネス目標を評価し、それを達成するための戦略を考案します。

   1. ビジネスモデルとマーケティング目標の設定。

   1. コンバージョン追跡要件の特定

   1. 既存のオンラインおよびアカウントの構造を分析。

   1. ポートフォリオの最適化とレポート作成のための指標を特定する。

1. （管理者またはアカウントマネージャーユーザー）管理アカウントを設定します。

   1. 広告主のアカウントを設定する。 代理店が広告主のデータを管理する場合、広告主のアカウントは代理店アカウントに関連付けられている必要があります。

   1. （必要に応じて）広告主がキャンペーンデータを表示および管理し、レポートを生成するためのユーザーアカウントを作成します。

   管理者と協力して、Adobe Admin Consoleと適切な製品プロファイルを使用してアクセス権を設定します。 「[Search, Social, &amp; Commerce](/help/search-social-commerce/user-administration.md)」のユーザー管理を参照してください。

1. 各広告ネットワークアカウントのキャンペーンを同期または作成：

   * API接続アカウントの場合、[&#x200B; アカウントの詳細](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)を[!UICONTROL Manage] > [!UICONTROL Accounts]に作成し、ネットワーク固有の認証を完了し、トラッキングオプションを設定し、アカウントを有効にします。

   * APIをサポートしていないアカウントの場合は、該当する場合、[&#x200B; データアップロード &#x200B;](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)または[&#x200B; トラッキング専用アカウント &#x200B;](/help/search-social-commerce/manage/accounts/template-account-manage.md)のワークフローに従います。 これらのアカウントは、広告ネットワークと同期しないか、ポートフォリオ最適化をサポートしません。

   * アカウントにキャンペーンデータがまだ含まれていない場合は、Search, Social, &amp; Commerce内または広告ネットワーク内から、キャンペーン、広告グループ、キーワード、広告、および配置を追加します。

     設定チェックリストの詳細については、「[広告ネットワークアカウントとキャンペーンの設定](campaign-implementation-overview.md)」を参照してください。 サポートされているキャンペーンの種類については、[!UICONTROL Manage] > [!UICONTROL Campaigns]を使用して[&#x200B; キャンペーンの作成と管理](/help/search-social-commerce/manage/campaigns/campaign-manage.md)を行います。

1. Adobe Advertisingでコンバージョンをトラッキングするすべての広告にトラッキングを設定します。

   1. （必要に応じて） [&#x200B; クリックトラッキング URLを生成してアップロードすることで、広告のクリックトラッキング &#x200B;](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)を設定し、オプションでキーワード、[!DNL Google Ads] プレースメント、[!DNL Google Ads]拡張機能を設定します。

      Adobe Advertising ピクセルベースのコンバージョントラッキングサービスを使用する広告主向けのクリックトラッキング URLには、[!DNL Adobe]台のサーバーへのリダイレクトが含まれています。

   1. [&#x200B; コンバージョン トラッキングを設定](/help/search-social-commerce/tracking/conversion-tracking-about.md)。 実装に応じて、これには、コンバージョン追跡タグを適切なweb ページに追加したり、独自の方法で収集したコンバージョンデータの毎日のフィードドロップを設定したりすることが含まれます。 [Adobe Advertising コンバージョントラッキングタグを](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md)から[!UICONTROL Goals] > [!UICONTROL Conversions]生成できます。

      詳しくは、「[検索、ソーシャル、Commerceのトラッキングについて](/help/search-social-commerce/tracking/tracking-about.md)」を参照してください。

1. その他の製品との統合を設定する：

   1. （Adobe AnalyticsやAdobe Audience Managerの広告主）様々なアカウント間の統合機能を設定して、Adobe Advertisingがデータを交換できるようにします。

      「[CX Enterpriseとの統合](/help/integrations/home.md)」に関するガイドを参照してください。

   1. （広告主、[!DNL Google Analytics]）最適化とレポート用に、[!DNL Google Analytics] アカウント、プロパティ、ビューの組み合わせのコンバージョン指標を同期します。

      この設定では、従来のユーザーインターフェイスを使用します。 「[同期について [!DNL Google Analytics]  コンバージョン指標](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)」を参照し、必要に応じて[従来のインターフェイスに切り替えます](ui-switch.md)。

1. （オプション）ポートフォリオを設定して起動します。

   1. [!UICONTROL Goals] > [!UICONTROL Conversions]で、[&#x200B; コンバージョン指標を確認し、必要な指標を表示します](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available)。 [!UICONTROL Goals] > [!UICONTROL Objectives]で、[最適化する目的](/help/search-social-commerce/goals/objectives/objective-about.md)を作成または選択します。

   1. [!UICONTROL Manage] > [!UICONTROL Portfolios]で、[目的とビジネス目標に合わせて構成されたポートフォリオ &#x200B;](/help/search-social-commerce/manage/portfolios/portfolio-create.md)を作成し、適切な[適格キャンペーン &#x200B;](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)を行います。 [&#x200B; ポートフォリオ &#x200B;](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)をアクティブ化して、データを収集およびモデル化します。 そして、実装チームは、クリック数と収益に関するデータを少なくとも14日間収集して検証し、ポートフォリオ設定を検証します。

      >[!NOTE]
      >
      >Search, Social, &amp; Commerceでは、ポートフォリオに割り当てられていないキャンペーンのデータを追跡、報告しますが、最適化は行われません。

   1. ベースラインを作成するのに十分なデータが利用可能になると、チームは[&#x200B; ポートフォリオステータスを最適化された](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)に変更できます。これにより、Search, Social, &amp; Commerceは、ポートフォリオのタイプとキャンペーン入札戦略に基づいて、ポートフォリオの入札、予算、入札戦略目標を最適化できます。

   最適化のサポートとポートフォリオのステータスについては、「[&#x200B; ポートフォリオについて](/help/search-social-commerce/manage/portfolios/portfolio-about.md)」を参照してください。

1. ポートフォリオのパフォーマンスを監視する：

   1. [!UICONTROL Dashboard] > [!UICONTROL Overview]を使用して[&#x200B; ポートフォリオトレンドを確認](/help/search-social-commerce/dashboard/dashboard-overview.md)し、[&#x200B; ポートフォリオパフォーマンスの詳細を表示](/help/search-social-commerce/manage/portfolios/portfolio-details.md)して、結果とモデルの精度を調査します。

   1. [&#x200B; カスタムアラートを設定](/help/search-social-commerce/common-tasks/alerts-manage.md)および[&#x200B; パフォーマンス監視用にカスタマイズされたレポート &#x200B;](/help/search-social-commerce/reports/management/report-manage.md)を生成します。 必要に応じて、[&#x200B; レポートテンプレート &#x200B;](/help/search-social-commerce/reports/report-templates-manage.md)および[&#x200B; スプレッドシートフィード &#x200B;](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md)を使用してレポートを自動化します。

   詳しくは、「[&#x200B; キャンペーンとポートフォリオパフォーマンスの監視](/help/search-social-commerce/manage/manage-about.md#monitor-performance)」を参照してください。

1. （オプション） [&#x200B; パフォーマンスデータビュー](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)を設定して、表示するデータを表示します。

## 進行中のタスク

初回起動後、次の継続的なタスクが必要です。 エンゲージメント条件に応じて、次のタスクを実行するのは、[!DNL Adobe]、アフィリエイトエージェンシー、または広告主です。

* アラート、各ポートフォリオとそのコンポーネントキャンペーンのパフォーマンスデータ、カスタマイズ可能なレポート、（一部の役割の）シミュレーションを表示することで、各ポートフォリオのパフォーマンスを継続的に監視および分析します。

* ポートフォリオの実際および予測されるパフォーマンスと成長の機会に基づいて、必要に応じて、ポートフォリオセットの管理に使用する様々な戦略と設定を調整します。

  * ポートフォリオ予算、目的、その他の設定を調整します。

  * マーケティング戦略の変更に対応するために、アカウント/キャンペーン構造を調整します。

  * キャンペーンコンポーネントの追加/一時停止/削除。 これには、検索語句分析に基づくキーワードセットの拡張や、広告コピーとランディングページのテストなどが含まれます。

  * 高度なパフォーマンスレポートにもとづいて、位置情報およびサイトターゲティング戦略を更新できます。

  * （オプション）個々の検索キーワードまたは広告グループ、キャンペーン、ポートフォリオ内のすべてのキーワードに入札制限を追加します。

  * 新しいポートフォリオを追加します。

キャンペーンとポートフォリオの監視と設定の調整の手順については、「[&#x200B; キャンペーンとポートフォリオの管理について](/help/search-social-commerce/manage/manage-about.md)」および「[&#x200B; ポートフォリオの詳細を編集](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)」を参照してください。
