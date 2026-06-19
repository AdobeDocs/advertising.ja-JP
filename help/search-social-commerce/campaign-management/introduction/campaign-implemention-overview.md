---
title: 広告ネットワークアカウントとキャンペーンの実装の概要
description: 広告ネットワークアカウントの設定、同期、管理に関するタスクについて説明します。
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/bAXUxseeAb6zMrnFa6gXEe1ES-3BlDMM-3a-vLzeFoY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 992
ht-degree: 0%

---

# 広告ネットワークアカウントとキャンペーンの実装の概要

Adobeは、各広告主と連携して、広告ネットワークアカウントとキャンペーンを設定します。 これには、Search, Social, &amp; Commerceを設定して広告主のアカウントと連携および同期させる、必要に応じて新しいキャンペーンおよびキャンペーンコンポーネントを作成する、コンポーネント広告のトラッキングを設定する、オプションでキャンペーンをポートフォリオに追加してSearch, Social, &amp; Commerceが広告の入札を最適化できるようにする、初期費用、クリック、収益データを検証することが含まれます。

施策がアクティベートされ、オプションでポートフォリオに追加された後、Adobeのアカウント管理チーム、代理店チーム、または広告主（service level agreementの条件によって異なります）は、各キャンペーンを監視し、広告主の目標を達成するために必要に応じて関連コンポーネントや設定を変更する必要があります。

このページには、同期アカウントのキャンペーン構造の設定方法など、すべてのアカウントタイプに関する情報が含まれます。 [!DNL Naver]のトラッキング専用アカウントの設定に関する追加の手順については、「[実装 [!DNL Naver]  トラッキング専用アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)」を参照してください。

## アカウントとキャンペーンの初期設定タスク

[!DNL Adobe]およびお客様の代理店が協力して次の作業を行います：

1. （新しい広告主アカウント）管理アカウントの設定：

   1. 広告主のアカウントを設定する。

   1. （必要に応じて）広告主がキャンペーンデータを表示および管理し、レポートを生成するためのユーザーアカウントを作成します。

1. （一部の広告ネットワーク）検索、ソーシャル、Commerceの権限を取得し、広告ネットワークのAPIと検索、ソーシャル、Commerceのユーザーインターフェイスを使用して各アカウントにアクセスします。

1. 広告ネットワークアカウントごとに：

   1. （必要に応じて）広告ネットワーク上のアカウントを設定します。

   1. アカウントへのアクセス資格情報とトラッキングオプションを含むSearch, Social, &amp; Commerceで[対応するアカウントレコード &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account)を作成してアカウントと連携し、アカウントステータスを「有効」に設定します。

      Search, Social, &amp; Commerceは、広告ネットワークと同期します。 アカウントにキャンペーンデータが既に含まれている場合、そのデータは約24時間以内に利用できます。

   1. （[広告タイプを作成/編集できます](/help/search-social-commerce/introduction/supported-inventory.md) in Search, Social, &amp; Commerce） アカウントにキャンペーンデータがまだ含まれていない場合は、広告タイプで使用できる次のいずれかの方法で、Search, Social, &amp; Commerce内からキャンペーン構造とキャンペーンコンポーネントを作成します。

      * （Google Ads、Microsoft Advertising、Yahoo! 広告、およびYandex アカウントのみ）作成した広告ネットワーク固有の広告テンプレートと、FTPの場所にアップロードした在庫データファイルの内容に従って、在庫内の各項目をターゲットとする動的な広告とキーワードを作成する[自動プロセスを設定します](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)。

      * （Baidu、Google Ads、[!DNL LY Ads]、Microsoft Advertising、およびYandex アカウントのみ）アカウントに必要な量のデータを含む[&#x200B; バルクシート ファイル &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)をアップロードしてから、アドネットワークに投稿します。

      * （Baidu、Google Ads、[!DNL LY Ads]、Microsoft Advertising、およびYandex アカウントのみ）個々のコンポーネントのデータをインターフェイスに直接入力します。 ほとんどのキャンペーンと広告タイプでは、キャンペーンレベル、広告グループレベル、個々のキーワード、プレースメント、広告レベルでデータを作成できます。

      ただし、一部のキャンペーンや広告タイプでは、独自のワークフローが必要です。 [[!DNL Microsoft Advertising]  ショッピングキャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)、[[!DNL Google Ads] 動的検索広告](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md)、[[!DNL Google Ads]  パフォーマンスの最大キャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md)および[[!DNL Google Ads]  ショッピングキャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)の設定に関する手順を参照してください。

   1. （[!DNL Naver]件のトラッキング専用アカウントのみ）データを含む[&#x200B; バルクシートファイル &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)をアップロードして、Search, Social, &amp; Commerceの既存のキャンペーン、広告グループ、キーワードを[!DNL Naver]に投稿せずに複製します。

1. Adobe Advertisingがコンバージョンをトラッキングするすべての広告にトラッキングを設定します。

   1. （Adobe Advertising コンバージョントラッキングサービスを使用する広告主）必要に応じて、検索、ソーシャル、およびCommerceのクリックトラッキング URLを生成してアップロードすることで、広告のクリックトラッキング [&#128279;](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)を設定し、オプションでキーワード、プレースメント、および広告拡張機能を設定します。

      パフォーマンスの最大キャンペーン [!DNL Google Ads]件について、[件のキャンペーンのトラッキング設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)ですべてのトラッキングを設定します。

1. トラッキングのみのキャンペーンの場合は、バルクシートを使用して宛先URLを生成し、生成された宛先URLを広告ネットワークのネイティブエディターを使用して関連するエンティティに追加する必要があります。

   1. コンバージョン追跡の設定。 実装に応じて、これには、広告主のweb ページにコンバージョン追跡タグを追加したり、広告主が個別に収集したコンバージョンデータの毎日のフィードドロップを設定したりすることが含まれます。

      Adobe Advertising コンバージョントラッキングサービスを使用している場合は、Search, Social, &amp; Commerce内で[&#x200B; コンバージョントラッキングタグ &#x200B;](/help/search-social-commerce/tools/conversion-tag-generate.md)を生成するか、Adobe Experience Platform[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) （旧Adobe Experience Platform Launch）から タグを使用できます。

   1. 追跡されたデータを検証します。

   トラッキングの設定について詳しくは、「トラッキング」の章を参照してください。

1. （Adobe Analyticsを使用している広告主） [Adobe AdvertisingとAnalytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)を統合してデータを交換できるようにします。

1. （Search, Social, &amp; Commerceで入札、キャンペーン予算、および/またはキャンペーン入札戦略のターゲットを最適化できるようにするには、[&#x200B; サポートされているキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)のみ） [&#x200B; キャンペーンをポートフォリオに割り当てます](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md)。

   ポートフォリオがまだ開始されていない場合（入札や予算の最適化）は、最適化機能で十分なデータを収集し、コストと収益モデルを構築できるようにして、ポートフォリオのベースラインパフォーマンスを確立してから開始します。

   ポートフォリオが既に起動されている場合は、ポートフォリオの学習を有効にします。 詳しくは、「ポートフォリオ戦略の調整」を参照してください。 最適化機能がキャンペーンの入札単位に関するデータを収集する一方で、新しいキャンペーンを追加した後は、ポートフォリオが不安定になることが予想されます。 入札は1～3週間以内に自動的に調整されます。

   ポートフォリオについて詳しくは、Search, Social, &amp; Commerce内から入手できる最適化ガイドを参照してください。<!-- verify convention for referencing Optimization Guide here -->

1. （広告主が新しいコンバージョンを追跡する場合） [&#x200B; レポート、キャンペーン管理ビュー、ポートフォリオ目標でコンバージョンを利用できるようにします](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)。

1. 各キャンペーンについて、Search, Social, &amp; Commerceが広告ネットワークからクリック数とコスト数のデータを受け取っていることを確認し、Search, Social, &amp; Commerceに表示される収益データと広告主自身の収益データを検証します。

1. （オプション）レポートテンプレート、スプレッドシートのフィード、スケジュールされたレポートのFTP配信を設定して、レポートを自動化します。

   手順については、「レポート」の章を参照してください。

>[!MORELIKETHIS]
>
>* [Search, Social, &amp; Commerceでのキャンペーン管理について](campaign-management-about.md)
>* [広告ネットワークキャンペーンのパフォーマンスを監視および管理](monitor-performance-campaigns.md)
>* Search, Social, &amp; Commerceの[Google Ads コンバージョンデータ &#x200B;](google-conversion-data.md)
>* [&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)
