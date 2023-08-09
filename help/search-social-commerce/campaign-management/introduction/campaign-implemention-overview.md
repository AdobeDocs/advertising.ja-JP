---
title: 広告ネットワークアカウントとキャンペーンの実装の概要
description: 広告ネットワークアカウントの設定、同期、管理に関するタスクについて説明します。
exl-id: 401c5ebb-258c-4614-96e8-ca604fc698c0
feature: Search Campaign Management
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# 広告ネットワークアカウントとキャンペーンの実装の概要

Adobeは、各広告主と連携して、広告ネットワークアカウントとキャンペーンを設定します。 これには、広告主のアカウントと接続して同期するための Search、Social、&amp;Commerce の設定、必要に応じて新しいキャンペーンとキャンペーンコンポーネントの作成、コンポーネント広告の追跡の設定、オプションでポートフォリオへのキャンペーンの追加、広告の入札の最適化、初期コスト、クリック、売上高データの検証が含まれます。

キャンペーンを有効化し、必要に応じてポートフォリオに追加した後、Adobeアカウント管理チーム、代理店チーム、広告主（SLA の条件に応じて）は、各キャンペーンを監視し、広告主の目標に合わせて必要なコンポーネントと設定を変更します。

このページには、同期されたアカウント用のキャンペーン構造の設定方法を含む、すべてのアカウントタイプに関する情報が含まれています。 トラッキング専用アカウントの設定手順については、 [!DNL Naver]を参照してください。[実装方法 [!DNL Naver] トラッキング専用アカウント](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## アカウントおよびキャンペーンの初期設定タスク

[!DNL Adobe] または、お客様の代理店が以下の作業を行います。

1. （新しい広告主アカウント）管理アカウントを設定します。

   1. 広告主のアカウントを設定します。

   1. （必要に応じて）広告主のキャンペーンデータを表示および管理し、レポートを生成するためのユーザーアカウントを作成します。

1. （一部の広告ネットワーク）広告ネットワークの API と検索、ソーシャル、コマースのユーザーインターフェイスを使用して、各アカウントにアクセスするための検索、ソーシャル、コマースの認証を取得します。

1. 各広告ネットワークアカウントに対して、次の操作を実行します。

   1. （必要に応じて）広告ネットワーク上でアカウントを設定します。

   1. 次の方法でアカウントと統合 [対応するアカウントレコードの作成](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) アカウントアクセス資格情報とトラッキングオプションを含む Search、Social、および Commerce で、アカウントのステータスを「有効」に設定します。

      検索、Social、およびコマースが、広告ネットワークと同期します。 アカウントに既にキャンペーンデータが含まれている場合、データは約 24 時間で利用できます。

   1. ([作成/編集できる広告タイプ](/help/search-social-commerce/introduction/supported-inventory.md) 検索、ソーシャル、コマースで ) アカウントにキャンペーンデータがまだ含まれていない場合は、広告タイプで使用できる次の方法のいずれかで、検索、ソーシャル、コマース内からキャンペーン構造とキャンペーンコンポーネントを作成します。

      * (Google Ads、Microsoft Advertising、Yahoo! 広告および Yandex アカウントのみ ) [在庫内の各品目をターゲットにした動的な広告およびキーワードを作成する自動プロセス](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 作成する広告ネットワーク固有の広告テンプレートと、FTP の場所にアップロードするインベントリデータファイルの内容に従って。

      * (Baidu、Google Ads、Microsoft Advertising、Yahoo! Japan Ads、および Yandex アカウントのみ ) のアップロード [bulksheet ファイル](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) アカウントに必要な数のデータを含み、それらを広告ネットワークに投稿します。

      * (Baidu、Google Ads、Microsoft Advertising、Yahoo! Japan Ads および Yandex アカウントのみ ) 個々のコンポーネントのデータを直接インターフェイスに入力します。 ほとんどのキャンペーンおよび広告タイプでは、キャンペーンレベル、広告グループレベル、個々のキーワード、配置、広告レベルでデータを作成できます。

      ただし、一部のキャンペーンおよび広告タイプでは、一意のワークフローが必要です。 の設定手順を参照してください。 [[!DNL Microsoft Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] 動的検索広告](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] 最大パフォーマンスキャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md)、および [[!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] トラッキング専用アカウントのみ ) のアップロード [bulksheet ファイル](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 検索、ソーシャル、コマースの既存のキャンペーン、広告グループ、キーワードをレプリケートするデータ（投稿先には送信しない） [!DNL Naver].

1. Adobe Advertisingがコンバージョンを追跡するすべての広告に対して、トラッキングを設定します。

   1. ( 必要に応じて、Adobe Advertisingコンバージョントラッキングサービスを利用する広告主 ) [クリックの追跡を設定する](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) 広告の場合、およびオプションで検索、Social、&amp; Commerce のクリック追跡 URL を生成してアップロードすることによって、キーワード、プレースメント、広告の拡張機能の場合に使用します。

      の場合 [!DNL Google Ads] パフォーマンスの最大キャンペーン、すべてのトラッキングを [キャンペーンのトラッキング設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. トラッキングのみのキャンペーンの場合は、一括送信シートを使用してリンク先 URL を生成し、その後、広告ネットワークのネイティブエディターを使用して、生成したリンク先 URL を関連エンティティに追加する必要があります。

   1. コンバージョントラッキングを設定します。 実装によっては、広告主の Web ページにコンバージョントラッキングタグを追加したり、広告主が別途収集したコンバージョンデータの日別フィードドロップを設定したりします。

      コンバージョントラッキングサービスを使用する場合は、Adobe Advertisingトラッキングタグを生成することができます。 [検索、ソーシャル、コマース内](/help/search-social-commerce/tools/conversion-tag-generate.md) または [Adobe Experience Platformの使用](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. 追跡したデータを検証します。

   トラッキングの設定について詳しくは、「トラッキング」の章を参照してください。

1. (Adobe Analytics広告主 ) [Adobe Advertisingと Analytics の統合](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) データを交換できるように。

1. ( 検索、ソーシャル、コマースで、入札およびキャンペーンの予算を最適化できるようにする。 [サポートされるキャンペーンタイプ](/help/search-social-commerce/introduction/supported-inventory.md) のみ ) [キャンペーンをポートフォリオに割り当てる](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   ポートフォリオがまだ開始されていない場合（入札や予算の最適化）、最適化機能は、ポートフォリオを起動する前にコストと売上高モデルを構築できる十分なデータを収集し、ポートフォリオのベースラインパフォーマンスを確立できます。

   ポートフォリオが既に起動されている場合は、ポートフォリオの学習を有効にします。 詳細は、「ポートフォリオ戦略の調整」を参照してください。 新しいキャンペーンを追加した後、ポートフォリオが揮発性であると想定し、最適化機能でキャンペーンの入札単位に関するデータを収集します。 入札は 1 ～ 3 週間以内に自動的に調整されます。

   ポートフォリオの詳細については、Search、Social、および Commerce から利用できる『最適化ガイド』を参照してください。<!-- verify convention for referencing Optimization Guide here -->

1. （広告主の新しいコンバージョンが追跡される場合） [コンバージョンを利用可能にする](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) レポート、キャンペーン管理ビュー、ポートフォリオの目標について説明します。

1. キャンペーンごとに、検索、ソーシャル、コマースが広告ネットワークからクリック数およびコスト数のデータを受け取っていることを確認し、広告主独自の売上高データを使用して検索、ソーシャル、コマースに表示される売上高データを検証します。

1. （オプション）レポートテンプレート、スプレッドシートフィード、予定レポートの FTP 配信を設定して、レポートを自動化します。

   手順については、「レポート」の章を参照してください。

>[!MORELIKETHIS]
>
>* [検索、ソーシャル、コマースでのキャンペーン管理について](campaign-management-about.md)
>* [広告ネットワークキャンペーンのパフォーマンスの監視と管理](monitor-performance-campaigns.md)
>* [Search、Social、および Commerce のGoogle Ads コンバージョンデータ](google-conversion-data.md)
>* [サポートされる在庫](/help/search-social-commerce/introduction/supported-inventory.md)
