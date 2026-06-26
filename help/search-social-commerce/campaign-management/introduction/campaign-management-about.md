---
title: Search, Social, & Commerceのキャンペーン管理について
description: Search, Social, & Commerceのキャンペーン管理機能について説明します。
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tgoMzw4DbEY5evC2s1f6mQHfJYYb7DJzMfFUnc-06Bk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 33f9b15eae29023aaee3644d7a78c09c5ab1429a
workflow-type: tm+mt
source-wordcount: 822
ht-degree: 0%

---

# Search, Social, &amp; Commerceのキャンペーン管理について

Search, Social, &amp; Commerceを使用すると、検索、表示/コンテンツ、ソーシャル、ショッピング、オーディエンス、パフォーマンスの最大数キャンペーンを1か所で追跡および/または管理できます。 広告ネットワークとキャンペーンのタイプに応じて、利用可能な機能には、広告ネットワークとの同期、機能の作成と編集、トラッキングとコンバージョンのアトリビューション、レポート、入札と予算の最適化などがあります。 各広告ネットワークで使用できる機能について詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

[!UICONTROL Campaigns] ビューでキャンペーンデータを追加および編集すると、Search, Social, &amp; Commerceは、データの変更を直ちに広告ネットワークにプッシュします。 Search, Social, &amp; Commerceでは、同期された[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントからキャンペーン構造データを取得し、1時間ごとにデータをクリックしたり、同期されたその他の広告ネットワークアカウントを毎日クリックしたりします。新しいキャンペーンが検出されたときに多くの場合があります。 同期されているすべての広告ネットワークに対して、必要に応じてアカウントをオンデマンドで同期することもできます。

## 広告ネットワークアカウントへのアクセスの設定

広告主の広告ネットワークアカウント内の広告のパフォーマンスを追跡するため（および広告の入札を行う可能性がある）、Adobe アカウントチーム [は、Search, Social, &amp; Commerceで対応するアカウントレコード &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)を作成します。 アカウントレコードには、トラッキングオプションが含まれます。

広告ネットワークのAPIを介して同期されているアカウントの場合、アカウントレコードにはアカウントアクセス資格情報も含まれます。 アカウントが有効になると、アカウントデータが広告ネットワークから取得されます。 その後、既存のアカウントデータを表示したり、キャンペーン構造や広告データを作成および編集したりできます。

## クリックをコンバージョンに結び付けるトラッキング

Adobe Advertising コンバージョントラッキングサービスを使用する場合は、ランディングページのサフィックス、トラッキングテンプレート、広告、キーワード、プレースメント、サイトリンク、商品リストの最終版/宛先URLに、検索、ソーシャル、Commerceのクリックトラッキングコードを含める必要があります。 キャンペーン設定が「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」を含む[&#x200B; サポートされている広告ネットワークおよびキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)の場合、レコードを保存すると、Search, Social, &amp; Commerceは独自のリダイレクトコードとトラッキングコードを自動的に追加するため、手動で追加する必要はありません。 それ以外の場合は、トラッキングテンプレートまたは最終的なURLにコードを手動で追加する必要があります。

トラッキングについて詳しくは、「トラッキング」の章を参照してください。

## 入札と予算管理の自動化

[&#x200B; サポートされている広告ネットワークとキャンペーンの種類](/help/search-social-commerce/introduction/supported-inventory.md)の場合、キャンペーンをポートフォリオにグループ化し、それぞれに特定のビジネス目標と特定の予算またはパフォーマンス目標を設定できます。 Search, Social, &amp; Commerceは、標準的なポートフォリオにおいて、CPCのキーワード入札とキャンペーン予算を最適化します。 ハイブリッド型のポートフォリオは、検索やソーシャル、Commerceなどの最適化テクノロジーと、アドネットワークを組み合わせたものです。

使用可能なポートフォリオオプションとポートフォリオの設定方法について詳しくは、Search, Social, &amp; Commerce内から使用できる「ポートフォリオ」に関する最適化ガイドの章を参照してください。<!-- verify convention for referencing Optimization Guide here -->

## キャンペーン管理ビューでは

キャンペーン管理ビューを使用すると、検索アカウントを監視および管理できます。 次のビューを使用できます。

* **[!UICONTROL Campaigns]** — [!UICONTROL Campaigns] ビューには、接続されている各広告ネットワークアカウントのデータが表示されます。 すべての広告ネットワークアカウントおよび個々のアカウント、キャンペーン、広告グループ、キーワード、広告、ショッピング製品グループ、プレースメント、自動ターゲット（動的検索ターゲット）、オーディエンス、広告拡張ライブラリおよび関連するアカウントエンティティをまたいで、コスト、クリック、インプレッション、および収益データを表示できます。 サポートされている広告ネットワーク [でサポートされているキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)の場合、個々のキャンペーンとキャンペーンコンポーネントのデータをインターフェイスで直接作成および編集できます。 オプションとして、ほとんどのサブビューのデータをスプレッドシートファイルに書き出すことができます。

  >[!NOTE]
  >
  >広告レベルのデータは、[!DNL Google Ads]件の動的検索広告（DSA）、パフォーマンスの最大値、スマートショッピング、および[!DNL YouTube]件のキャンペーンでは利用できません。

* **[!UICONTROL Products]** — [!UICONTROL Products] ビューには、同期されている[[!DNL Google] または [!DNL Microsoft]  マーチャント センターの各アカウントのデータが表示されます](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。 デフォルトの[!UICONTROL Accounts] サブビューには、同期されたすべてのアカウントが一覧表示されます。一部のユーザータイプでは、このビューから新しいアカウントを追加できます。 [!UICONTROL Products] サブビューには、アカウント内の各製品が一覧表示されます。

* **[!UICONTROL Advanced (ACM)]** — [!DNL Advanced] （[!DNL AMC]、高度なキャンペーン管理）ビューから、作成した広告ネットワーク固有の広告テンプレートと、FTPの場所にアップロードした[!DNL Google Merchant Center] アカウントまたは在庫データファイルの内容に従って、在庫[&#128279;](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)の各項目をターゲットとする動的な広告とキーワードを作成する自動プロセスを設定できます。 サブビューには、広告主の各フィードテンプレートに関する詳細と、フィードテンプレートを通じて伝播されたが広告ネットワークに投稿されなかったフィードに含まれる各キャンペーン、広告グループ、キーワード、および広告に関する詳細が表示されます。

* **[!UICONTROL Bulksheets]** - [!UICONTROL Bulksheets] ビューを使用して、[&#x200B; サポートされている広告ネットワーク &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)上のアカウントに必要な量のデータを含む[&#x200B; バルクシート ファイル &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を作成し、広告ネットワークに投稿します。

* **[!UICONTROL Audiences]** — [&#x200B; [!UICONTROL Audiences] ビュー](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)には、様々なタイプのユーザーリストから生成されたすべての[!DNL Google Ads]および[!DNL Microsoft Advertising] オーディエンスが一覧表示されます。 既存のAdobe CX Enterprise オーディエンスと顧客メールリストから[!DNL Google Ads]個のオーディエンスを作成できます。 また、[!DNL Google Ads]および[!DNL Microsoft Advertising]広告のオーディエンスのターゲットと除外を表示および管理することもできます。

* **[!UICONTROL Label Classifications]** – このビューを使用して[&#x200B; ラベル分類](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)を作成および削除します。これにより、ラベルを意味のあるセットにグループ化できます。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスを監視および管理](monitor-performance-campaigns.md)
>* Search, Social, &amp; Commerceの[Google Ads コンバージョンデータ &#x200B;](google-conversion-data.md)
