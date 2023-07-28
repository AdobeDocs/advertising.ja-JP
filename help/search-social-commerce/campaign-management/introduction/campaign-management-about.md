---
title: 検索、ソーシャル、コマースでのキャンペーン管理について
description: 検索、ソーシャル、コマースのキャンペーン管理機能について説明します。
exl-id: e6fca48d-1f6c-4d36-a10d-e1a5db859a37
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 検索、ソーシャル、コマースでのキャンペーン管理について

検索、ソーシャル、コマースでは、検索、表示/コンテンツ、ソーシャル、ショッピング、オーディエンス、パフォーマンスの最大キャンペーンを 1 か所で追跡および管理できます。 広告ネットワークとキャンペーンのタイプに応じて、使用可能な機能には、広告ネットワークとの同期、機能の作成と編集、トラッキングとコンバージョン属性、レポート、入札と予算の最適化が含まれます。 各広告ネットワークで使用できる機能について詳しくは、[サポートされている在庫](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

でキャンペーンデータを追加および編集する際、 [!UICONTROL Campaigns] 表示数、検索、Social および Commerce は、データの変更を広告ネットワークに即座にプッシュします。 また、Search, Social, &amp; Commerce は、キャンペーン構造データを取り込み、同期された広告ネットワークアカウントのデータを 1 日 1 回（新しいキャンペーンが検出された場合はより頻繁に）、リクエストに応じてクリックします。

## 広告ネットワークアカウントへのアクセスの設定

広告主の広告ネットワークアカウントで広告のパフォーマンスを追跡する（および場合によっては広告の入札を配置する）には、Adobeアカウントチーム [対応するアカウントレコードを作成します](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) 検索、ソーシャル、コマースの 3 つのアイコンを使用します。 アカウントレコードには、トラッキングオプションが含まれます。

広告ネットワークの API を介して同期されたアカウントの場合、アカウントレコードにはアカウントのアクセス資格情報も含まれます。 アカウントが有効になると、アカウントデータが広告ネットワークでから取得されます。 その後、既存のアカウントデータを表示し、キャンペーン構造と広告データを作成および編集できます。

## クリックの追跡でクリックをコンバージョンに結び付ける

Adobe Advertisingコンバージョントラッキングサービスを使用する場合、広告、キーワード、プレースメント、サイトリンク、製品リストのランディングページサフィックス、トラッキングテンプレート、最終/宛先 URL に検索、ソーシャル、コマースのクリックトラッキングコードを含める必要があります。 の場合 [サポートされる広告ネットワークとキャンペーンのタイプ](/help/search-social-commerce/introduction/supported-inventory.md) キャンペーン設定に「[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、自動的に独自のリダイレクトとトラッキングコードを追加するので、手動で追加する必要はありません。 それ以外の場合は、トラッキングテンプレートまたは最終 URL にコードを手動で追加する必要があります。

トラッキングについて詳しくは、「トラッキング」の章を参照してください。

## 入札と予算管理の自動化

の場合 [サポートされる広告ネットワークとキャンペーンのタイプ](/help/search-social-commerce/introduction/supported-inventory.md)を使用すると、キャンペーンをポートフォリオにグループ化し、それぞれに特定のビジネス目標と特定の予算またはパフォーマンス目標を設定できます。 標準のポートフォリオでは、検索、ソーシャル、コマースで CPC キーワード入札とキャンペーン予算を最適化します。 ハイブリッドポートフォリオは、検索、ソーシャル、コマースおよび広告ネットワークの最適化テクノロジーを組み合わせたものです。

使用可能なPortfolioオプションとポートフォリオの設定方法の詳細については、Search、Social、&amp;Commerce から利用できる「ポートフォリオの管理」の「最適化ガイド」の章を参照してください。<!-- verify convention for referencing Optimization Guide here -->

## キャンペーン管理ビュー

キャンペーン管理ビューを使用すると、検索アカウントを監視および管理できます。 次のビューを使用できます。

* **[!UICONTROL Campaigns]** — [!UICONTROL Campaigns] ビューは、接続された各広告ネットワークアカウントからのデータを表示します。 すべての広告ネットワークアカウント、および個々のアカウント、キャンペーン、広告グループ、キーワード、広告、買い物製品グループ、プレースメント、自動ターゲット（動的検索ターゲット）、オーディエンス、広告拡張ライブラリと関連するアカウントエンティティにわたって、コスト、クリック、インプレッション、売上高のデータを表示できます。 の場合 [サポートされる広告ネットワークでサポートされるキャンペーンタイプ](/help/search-social-commerce/introduction/supported-inventory.md)を使用すると、個々のキャンペーンおよびキャンペーンコンポーネントのデータをインターフェイスで直接作成および編集できます。 必要に応じて、ほとんどのサブビューのデータをスプレッドシートファイルに書き出すことができます。

  >[!NOTE]
  >
  >広告レベルのデータは [!DNL Google Ads] 動的検索広告 (DSA)、パフォーマンスの最大値、スマートショッピング、 [!DNL YouTube] キャンペーン。

* **[!UICONTROL Products]** — [!UICONTROL Products] ビューは、それぞれのデータを表示します [[!DNL Google] or [!DNL Microsoft] 同期されたマーチャントセンターアカウント](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). デフォルト [!UICONTROL Accounts] サブビューには、すべての同期されたアカウントが一覧表示されます。一部のユーザータイプは、このビューから新しいアカウントを追加できます。 The [!UICONTROL Products] サブビューには、アカウント内の各製品が一覧表示されます。

* **[!UICONTROL Advanced (ACM)]** — [!DNL Advanced] ([!DNL AMC]( 高度なCampaign Managementの場合 ) 表示では、自動プロセスを設定して、 [在庫内の各品目をターゲットにした動的な広告およびキーワード](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 作成する広告ネットワーク固有の広告テンプレートと、 [!DNL Google Merchant Center] FTP の場所にアップロードするアカウントまたは在庫データファイル。 サブビューは、フィードテンプレートを通じて伝播されたが広告ネットワークには投稿されていない、フィードに含まれている広告主の各フィードテンプレートと、広告グループ、キーワードおよび広告に関する詳細を表示します。

* **[!UICONTROL Bulksheets]**  — 次を使用します。 [!UICONTROL Bulksheets] 作成するビュー [bulksheet ファイル](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) のアカウントに必要な数のデータを含む [サポートされている広告ネットワーク](/help/search-social-commerce/introduction/supported-inventory.md)をクリックし、広告ネットワークに投稿します。

* **[!UICONTROL Audiences]** — [The [!UICONTROL Audiences] ビュー](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) に、 [!DNL Google Ads] および [!DNL Microsoft Advertising] 様々なタイプのユーザーリストから生成されるオーディエンス。 次の項目を作成できます。 [!DNL Google Ads] オーディエンスを既存のAdobe Experience Cloudオーディエンスおよび顧客の電子メールリストから取得する。 また、 [!DNL Google Ads] および [!DNL Microsoft Advertising] 広告。

* **[!UICONTROL Label Classifications]**  — このビューを使用して、 [ラベルの分類](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)：ラベルを意味のあるセットにグループ化するのに役立ちます。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスの監視と管理](monitor-performance-campaigns.md)
>* [Search、Social、および Commerce のGoogle Ads コンバージョンデータ](google-conversion-data.md)
