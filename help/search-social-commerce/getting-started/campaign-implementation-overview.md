---
title: 広告ネットワークアカウントとキャンペーンの設定
description: 広告ネットワーク接続、キャンペーン、トラッキング、コンバージョン指標、オプションのポートフォリオ最適化の設定ワークフローに従います。
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# 広告ネットワークアカウントとキャンペーンの設定

*Beta機能*

[!DNL Adobe]様と代理店が協力して、広告ネットワークアカウントの接続、キャンペーンの準備、トラッキングの設定、パフォーマンスデータの検証を行います。 Search, Social, &amp; Commerceで対象となるキャンペーンを最適化する場合は、ワークフローにポートフォリオ設定も含まれます。

このチェックリストでは、より広範な[実装ワークフロー](implemention-overview.md)のアカウントとキャンペーンの詳細を提供します。 実行できるタスクは、権限と、各広告ネットワークとキャンペーンの種類[&#128279;](/help/search-social-commerce/introduction/supported-inventory.md)でサポートされている機能によって異なります。

## ワークフローの設定

1. **アクセスとアカウントの要件を確認します。**

   管理者と協力して、適切な広告主へのアクセスと、タスクに必要な権限を確認します。 「[Search, Social, &amp; Commerce](/help/search-social-commerce/user-administration.md)」のユーザー管理を参照してください。

   必要に応じて、広告ネットワークのweb サイトで実際の広告ネットワークアカウントを作成します。 Search, Social, &amp; Commerceでアカウントレコードを作成しても、広告ネットワークでアカウントが作成されることはありません。

1. **各広告ネットワークアカウントを接続または登録します。**

   [!UICONTROL Manage] > [!UICONTROL Accounts]で、[&#x200B; アカウントタイプ &#x200B;](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)のワークフローを使用します。

   * **API接続：** [&#x200B; アカウントの詳細を作成し](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)、ネットワーク固有の認証を完了し、トラッキングオプションを設定し、アカウントを有効にします。 [認証とアクセス状態](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status)を確認します。認証が成功しても、必要なすべての権限が付与されているとは限りません。

   * **データのアップロード：** [&#x200B; アカウントの詳細を作成し、キャンペーンとパフォーマンスのデータをアップロード &#x200B;](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)。 これらのアカウントは、広告ネットワークと同期しないか、ポートフォリオ最適化をサポートしません。

   * **[!DNL Naver]トラッキング専用：** [&#x200B; トラッキング専用アカウントのワークフロー](/help/search-social-commerce/manage/accounts/template-account-manage.md)に従います。 バルクシートを使用してトラッキング URLを生成し、広告ネットワークのエディターに適用します。アカウントは同期しないか、ポートフォリオ最適化をサポートしていません。

1. **キャンペーン構造をレビューまたは作成します。**

   API接続アカウントの場合は、同期されたキャンペーンとそのコンポーネントを確認します。 [必要に応じて手動同期](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md)をリクエストします。

   サポートされているキャンペーンの種類については、[!UICONTROL Manage] > [!UICONTROL Campaigns]を使用して[&#x200B; キャンペーンを作成または編集](/help/search-social-commerce/manage/campaigns/campaign-manage.md)します。 必要な[広告グループ &#x200B;](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md)、[広告](/help/search-social-commerce/manage/ads/ad-manage.md)およびその他のサポートされているコンポーネントを作成します。 サポートされている一括操作には、[&#x200B; バルクシート &#x200B;](/help/search-social-commerce/set-up/bulksheets/about.md)を使用することもできます。

   キャンペーンをアクティブ化する前に、必要なネットワーク固有の設定を完了します。 広告ネットワーク独自のインターフェイスで、サポートされていないコンポーネントを管理します。

1. **起動前にトラッキングを設定および検証します。**

   実装に一致する[&#x200B; コンバージョン トラッキング メソッド &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-about.md)を選択します。 必要に応じて、[&#x200B; クリックトラッキング URLを生成して適用](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)および[&#x200B; コンバージョントラッキングタグを生成](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md)します。

   必要な[統合](/help/integrations/home.md)または[&#x200B; コンバージョンフィード &#x200B;](/help/search-social-commerce/tracking/tracking-about.md)を設定し、コンバージョンが期待どおりに帰属することを検証します。 トラッキングのみのキャンペーンの場合は、生成されたトラッキング URLを広告ネットワークのエディターに適用します。

1. **コンバージョン指標を確認します。**

   [!UICONTROL Goals] > [!UICONTROL Conversions]で、[追跡された指標を確認し、管理ビュー、レポート、および目的に必要な指標を表示](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available)します。 指標を区別するために、必要に応じて表示名を変更します。

1. **（オプション） ポートフォリオ最適化を準備します。**

   キャンペーンとその入札戦略が[&#x200B; ポートフォリオ最適化の対象であることを確認します](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)。

   [適切なコンバージョン指標を使用する目標](/help/search-social-commerce/goals/objectives/objective-about.md)を作成または選択します。 [!UICONTROL Manage] > [!UICONTROL Portfolios]で、[&#x200B; ポートフォリオを作成](/help/search-social-commerce/manage/portfolios/portfolio-create.md)または[既存のポートフォリオを編集](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)し、目的、支出戦略、および最適化設定を行います。

   [&#x200B; キャンペーンをポートフォリオに割り当てます](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)。 各キャンペーンは1つのポートフォリオにのみ属することができ、ポートフォリオ内のすべてのキャンペーンは同じ通貨を使用する必要があります。

1. **キャンペーンデータを検証し、パフォーマンスのベースラインを確立します。**

   各キャンペーンにコスト、クリック、コンバージョンのデータが利用可能であることを確認します。 コンバージョンデータを、適切なソース（該当する場合は[!DNL Google Ads]および[!DNL Microsoft Advertising]を含む）と比較します。 レポートを比較する際には、一貫した日付範囲とアトリビューション設定を使用します。

   新しいポートフォリオの場合は、[それをアクティブ化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)してデータを収集し、モデル化します。 最適化を有効にする前に、データとポートフォリオの設定を検証します。

1. **（オプション）ポートフォリオ最適化を開始します。**

   ポートフォリオの準備ができたら、[&#x200B; ステータスを最適化に変更します](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)。前提条件と確認メッセージを確認します。 Search, Social, &amp; Commerceは、設定とサポートされている入札戦略に従ってポートフォリオを最適化します。

1. **継続的な監視とレポートを設定します。**

   [&#x200B; データビューをカスタマイズ &#x200B;](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)、[&#x200B; カスタムアラートを設定](/help/search-social-commerce/common-tasks/alerts-manage.md)、[&#x200B; スケジュール済みレポートを生成](/help/search-social-commerce/reports/management/report-manage.md)。 必要に応じて、[&#x200B; レポートテンプレート &#x200B;](/help/search-social-commerce/reports/report-templates-manage.md)および[&#x200B; スプレッドシートフィード &#x200B;](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md)を使用してレポートを自動化します。

   起動後も[&#x200B; キャンペーンとポートフォリオの監視と調整を続行](/help/search-social-commerce/manage/manage-about.md#monitor-performance)。

>[!MORELIKETHIS]
>
>* [Search、Social、およびCommerceの実装の概要](implemention-overview.md)
>* [&#x200B; キャンペーンとポートフォリオの管理について](/help/search-social-commerce/manage/manage-about.md)
>* Search, Social, &amp; Commerceの[[!DNL Google Ads]  コンバージョンデータ &#x200B;](/help/search-social-commerce/tracking/google-conversion-data.md)
>* Search, Social, &amp; Commerceの[[!DNL Microsoft Advertising]  コンバージョンデータ &#x200B;](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
