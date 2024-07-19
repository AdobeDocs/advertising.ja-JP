---
title: 広告ネットワークアカウントとキャンペーンの実装の概要
description: 広告ネットワークアカウントの設定、同期および管理に関連するタスクについて説明します。
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# 広告ネットワークアカウントとキャンペーンの実装の概要

Adobeは各広告主と連携して、広告ネットワークアカウントとキャンペーンを設定します。 これには、広告主のアカウントと接続して同期するための検索、ソーシャル、Commerceの設定、必要に応じてキャンペーンとキャンペーンコンポーネントの新規作成、コンポーネント広告のトラッキングの設定、オプションでキャンペーンをポートフォリオに追加して検索、ソーシャルおよびCommerceで広告への入札を最適化、初期コスト、クリック数および売上高のデータの検証が含まれます。

キャンペーンをアクティブ化し、オプションでポートフォリオに追加した後、Adobeアカウント管理チーム、エージェンシーチームまたは広告主（サービスレベル契約の条件によって異なります）は、各キャンペーンをモニタリングし、広告主の目標を達成するために必要に応じて関連するコンポーネントと設定を変更する必要があります。

このページでは、同期されたアカウントのキャンペーン構造を設定する方法など、すべてのアカウントタイプに関する情報を提供します。 [!DNL Naver] のトラッキング専用アカウントの設定に関する追加手順については、「[ トラッキング専用アカウントの実装  [!DNL Naver]  を参照 ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) てください。

## アカウントとキャンペーンの初期設定タスク

お客様と [!DNL Adobe] または代理店が連携して、以下の作業を行います。

1. （新しい広告主アカウント）管理アカウントを設定します。

   1. 広告主のアカウントを設定します。

   1. （必要に応じて）広告主がキャンペーンデータの表示と管理およびレポートの生成を行うためのユーザーアカウントを作成します。

1. （一部の広告ネットワーク）検索、ソーシャル、Commerceの認証を取得し、広告ネットワークの API と検索、ソーシャル、Commerceのユーザーインターフェイスを使用して、各アカウントにアクセスします。

1. 広告ネットワークアカウントごとに、次の手順を実行します。

   1. （必要に応じて）広告ネットワークにアカウントを設定します。

   1. 検索、ソーシャル、Commerceで、アカウントのアクセス資格情報とトラッキングオプションを含む [ 対応するアカウントレコードを作成 ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) してアカウントと統合し、アカウントステータスを有効に設定します。

      検索、ソーシャル、Commerceが広告ネットワークと同期されます。 アカウントに既にキャンペーンデータが含まれている場合、データは約 24 時間以内に使用可能になります。

   1. [ （作成/編集できる広告タイプ ](/help/search-social-commerce/introduction/supported-inventory.md) 検索、ソーシャル、Commerce）アカウントにキャンペーンデータがまだ含まれていない場合は、広告タイプで使用可能な次のいずれかの方法で、検索、ソーシャル、Commerce内からキャンペーン構造とキャンペーンコンポーネントを作成します。

      * （Google広告、Microsoft Advertising、Yahoo! 広告、および Yandex アカウントのみ） [ 作成した広告ネットワーク固有の広告テンプレートと FTP の場所にアップロードする在庫データファイルの内容に従って ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) インベントリ内の各項目をターゲットとした動的広告とキーワードを作成する自動プロセスを設定します。

      * （Baidu、Google広告、MicrosoftAdvertising、Yahoo! 日本の広告、および Yandex アカウントのみ）アカウントに必要な量のデータを含む [ バルクシートファイル ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) をアップロードしてから、広告ネットワークに投稿します。

      * （Baidu、Google広告、MicrosoftAdvertising、Yahoo! 日本広告、Yandex アカウントのみ）個々のコンポーネントのデータをインターフェイスに直接入力します。 ほとんどのキャンペーンタイプと広告タイプでは、キャンペーンレベル、広告グループレベル、個々のキーワード、プレースメント、広告レベルでデータを作成できます。

      ただし、一部のキャンペーンタイプや広告タイプでは一意のワークフローが必要です。 [[!DNL Microsoft Advertising]  ショッピングキャンペーン ](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)、[[!DNL Google Ads]  動的検索広告 ](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md)、[[!DNL Google Ads]  パフォーマンス最大化キャンペーン ](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md) および [[!DNL Google Ads]  ショッピングキャンペーン ](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md) の設定手順を参照してください。

   1. （[!DNL Naver] トラッキング専用アカウントの場合のみ）既存のキャンペーン、広告グループおよびキーワードを [!DNL Naver] に投稿せずに検索、ソーシャル、Commerceにレプリケートするには、データを含んだ [ バルクシートファイル ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) をアップロードします。

1. Adobe Advertisingがコンバージョンをトラッキングするすべての広告のトラッキングを設定：

   1. （Adobe Advertisingコンバージョントラッキングサービスを使用する広告主）必要に応じて、検索、ソーシャルおよびCommerceのクリック追跡 URL を生成してアップロードすることにより、広告、およびオプションでキーワード、プレースメント、広告拡張に対して [ クリック追跡の設定 ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) を行います。

      パフォーマンス最大化キャンペーンの [!DNL Google Ads] 合は、[ キャンペーンのトラッキング設定 ](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) ですべてのトラッキングを設定します。

1. トラッキング専用キャンペーンの場合は、代わりにバルクシートを使用して宛先 URL を生成し、広告ネットワークのネイティブエディターを使用して、生成された宛先 URL を関連するエンティティに追加する必要があります。

   1. コンバージョントラッキングの設定 実装によっては、コンバージョントラッキングタグを広告主の web ページに追加したり、広告主が個別に収集したコンバージョンデータの毎日のフィードドロップを設定したりすることが含まれる場合があります。

      Adobe Advertisingコンバージョントラッキングサービスを使用する場合は、[ 検索、ソーシャル、Commerce内 ](/help/search-social-commerce/tools/conversion-tag-generate.md) または [Adobe Experience Platformを使用 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html) コンバージョントラッキングタグを生成できます。

   1. 追跡するデータを検証します。

   トラッキング設定の詳細については、「トラッキング」の章を参照してください。

1. （Adobe Analyticsを使用する広告主） [Adobe Advertisingと Analytics を統合して ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) データを交換できるようにします。

1. （検索、ソーシャル、Commerceで入札やキャンペーン予算を最適化できるようにするには、[ サポートされているキャンペーンタイプのみ ](/help/search-social-commerce/introduction/supported-inventory.md)） [ キャンペーンをポートフォリオに割り当てます ](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md)。

   ポートフォリオがまだ開始されていない場合（入札や予算の最適化）、最適化機能でコストと収益のモデルを構築できるだけの十分なデータを収集させて、ポートフォリオを開始する前にポートフォリオのベースラインパフォーマンスを確立できます。

   ポートフォリオが既に起動されている場合は、ポートフォリオの学習を有効にします。 詳しくは、「ポートフォリオ戦略の調整」を参照してください。 新しいキャンペーンを追加すると、ポートフォリオが揮発性になると予想されますが、最適化機能は、キャンペーンの入札単位に関するデータを収集します。 入札は 1～3 週間以内に自動的に調整されます。

   ポートフォリオについて詳しくは、最適化ガイドを参照してください。このガイドは、検索、ソーシャル、Commerce内から利用でき <!-- verify convention for referencing Optimization Guide here --> す。

1. （広告主に対して新しいコンバージョンが追跡される場合） [ レポート、キャンペーン管理ビューおよびポートフォリオ目標でコンバージョンを使用可能にする ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)。

1. キャンペーンごとに、検索、ソーシャル、Commerceが広告ネットワークからクリックとコストのデータを受け取っていることを確認し、検索、ソーシャル、Commerceに表示される売上高データを広告主自身の売上高データで検証します。

1. （オプション）レポートテンプレート、スプレッドシートフィードおよび予定レポートの FTP 配信を設定することで、レポートを自動化します。

   手順については、「レポート」の章を参照してください。

>[!MORELIKETHIS]
>
>* [ 検索、ソーシャル、Commerceでのキャンペーン管理について ](campaign-management-about.md)
>* [ 広告ネットワークキャンペーンのパフォーマンスの監視と管理 ](monitor-performance-campaigns.md)
>* [ 検索、ソーシャル、CommerceのGoogle Ads コンバージョンデータ ](google-conversion-data.md)
>* [ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)
