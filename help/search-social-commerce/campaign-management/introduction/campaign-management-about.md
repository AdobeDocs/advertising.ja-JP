---
title: 検索、ソーシャル、Commerceでのキャンペーン管理について
description: 検索、ソーシャル、Commerceのキャンペーン管理機能について説明します。
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 検索、ソーシャル、Commerceでのキャンペーン管理について

検索、ソーシャル、Commerceを使用すると、検索、ディスプレイ/コンテンツ、ソーシャル、ショッピング、オーディエンス、Performance MAX の各キャンペーンを 1 か所でトラッキングおよび/または管理できます。 広告ネットワークとキャンペーンのタイプによっては、利用可能な機能に、広告ネットワークとの同期、能力の作成と編集、トラッキングとコンバージョンの属性、レポート、入札と予算の最適化などが含まれる場合があります。 各広告ネットワークで使用できる機能について詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

[!UICONTROL Campaigns] ビューでキャンペーンデータを追加および編集すると、検索、ソーシャルおよびCommerceによって、データの変更内容が直ちに広告ネットワークにプッシュされます。 また、検索、ソーシャル、Commerceでは、キャンペーン構造データを取り込み、同期された広告ネットワークアカウントから 1 日に 1 回（または新しいキャンペーンが検出された場合はより頻繁に）、リクエストに応じてオンデマンドでクリックデータをクリックします。

## 広告ネットワークアカウントへのアクセスの設定

広告主の広告ネットワークアカウントでの広告の効果を追跡する（および広告に入札を行う可能性がある）ために、Adobeアカウントチームは [&#x200B; 対応するアカウントレコードを作成 &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) 検索、ソーシャル、Commerceで行います。 アカウントレコードには、トラッキングオプションが含まれます。

広告ネットワークの API を使用して同期されるアカウントの場合、アカウントレコードにはアカウントアクセス資格情報も含まれます。 アカウントが有効になると、アカウントデータが広告ネットワークから取り込まれます。 その後、既存のアカウントデータを表示し、キャンペーン構造と広告データを作成および編集できます。

## クリック数をコンバージョンに結び付けるクリック数の追跡

Adobe Advertisingコンバージョントラッキングサービスを使用する場合は、広告、キーワード、プレースメント、サイトリンクおよび商品リストのランディングページのサフィックス、トラッキングテンプレート、最終/宛先 URL に、検索、ソーシャル、Commerceのクリックトラッキングコードを含める必要があります。 キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれる [&#x200B; サポートされている広告ネットワークとキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md) の場合、検索、ソーシャルおよびCommerceは、レコードを保存すると独自のリダイレクトおよびトラッキングコードを自動的に追加するので、手動で追加する必要はありません。 そうでない場合は、トラッキングテンプレートまたは最終的な URL に手動でコードを追加する必要があります。

トラッキングの詳細情報については、「トラッキング」の章を参照してください。

## 入札・予算管理の自動化

[&#x200B; サポートされている広告ネットワークとキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md) の場合は、キャンペーンをポートフォリオにグループ化できます。ポートフォリオごとに、特定のビジネス目標と特定の予算またはパフォーマンスの目標を指定できます。 標準ポートフォリオでは、検索、ソーシャルおよびCommerceは、CPC キーワード入札とキャンペーン予算を最適化します。 ハイブリッドポートフォリオでは、検索、ソーシャル、Commerceの最適化テクノロジーと広告ネットワークを組み合わせます。

使用可能なポートフォリオオプションとポートフォリオの設定方法について詳しくは、検索、ソーシャル、Commerce内から使用可能な「Portfolio」に関する最適化ガイドの章を参照してください。<!-- verify convention for referencing Optimization Guide here -->

## キャンペーン管理ビュー

キャンペーン管理ビューでは、検索アカウントを監視および管理できます。 次のビューを使用できます。

* **[!UICONTROL Campaigns]** —[!UICONTROL Campaigns] のビューには、接続された各広告ネットワークアカウントからのデータが表示されます。 すべての広告ネットワークアカウント、個々のアカウント、キャンペーン、広告グループ、キーワード、広告、買い物かごグループ、プレースメント、自動ターゲット （動的検索ターゲット）、オーディエンス、広告拡張機能ライブラリおよびそれらに関連するアカウントエンティティにわたる、コスト、クリック、インプレッションおよび収益データを表示できます。 [&#x200B; サポートされている広告ネットワークでサポートされているキャンペーンタイプ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md) の場合、インターフェイスで直接、個々のキャンペーンおよびキャンペーンコンポーネントのデータを作成および編集できます。 オプションで、ほとんどのサブビューのデータをスプレッドシートファイルに書き出すことができます。

  >[!NOTE]
  >
  >広告レベルのデータは、[!DNL Google Ads] 動的検索広告（DSA）、パフォーマンス最大化、スマートショッピングおよび [!DNL YouTube] キャンペーンでは使用できません。

* **[!UICONTROL Products]** —[!UICONTROL Products] のビューには、同期された各 [[!DNL Google]  またはマーチャントセンターアカウント &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) のデータが表示され  [!DNL Microsoft]  す。 デフォルトの [!UICONTROL Accounts] サブビューには、同期されたすべてのアカウントが一覧表示されます。一部のユーザータイプでは、このビューから新しいアカウントを追加できます。 [!UICONTROL Products] のサブビューには、アカウント内の各製品がリストされます。

* **[!UICONTROL Advanced (ACM)]** - [!DNL Advanced] （[!DNL AMC] [、Advanced Campaign Managementの場合）ビューでは、作成した広告ネットワーク固有の広告テンプレートと、FTP の場所にアップロードしたアカウントまたは在庫データファイルの内容に従って &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) インベントリ内の各項目をターゲット [!DNL Google Merchant Center] した動的広告とキーワード）を作成する自動プロセスを設定できます。 サブビューには、広告主の各フィードテンプレートに関する詳細と、フィードテンプレートを介して生成されたが広告ネットワークには投稿されなかったフィードに含まれる各キャンペーン、広告グループ、キーワードおよび広告が表示されます。

* **[!UICONTROL Bulksheets]** - [!UICONTROL Bulksheets] ビューを使用して [&#x200B; サポートされている広告ネットワーク &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 上のアカウントに必要な数のデータを含む [&#x200B; バルクシート ファイル &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md) を作成し、広告ネットワークに投稿します。

* **[!UICONTROL Audiences]** - [[!UICONTROL Audiences] ビュー &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) には、様々なタイプのユーザーリストから生成されたすべての [!DNL Google Ads] オーディエンスと [!DNL Microsoft Advertising] オーディエンスが一覧表示されます。 既存のAdobe Experience Cloud オーディエンスおよびお客様の電子メールリストから、[!DNL Google Ads] オーディエンスを作成できます。 また、[!DNL Google Ads] および [!DNL Microsoft Advertising] の広告のオーディエンスターゲットと除外を表示および管理することもできます。

* **[!UICONTROL Label Classifications]** – このビューを使用して、ラベルを意味のあるセットにグループ化するのに役立つ [&#x200B; ラベル分類 &#x200B;](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) を作成および削除します。

>[!MORELIKETHIS]
>
>* [&#x200B; 広告ネットワークアカウントとキャンペーンの実装の概要 &#x200B;](campaign-implemention-overview.md)
>* [&#x200B; 広告ネットワークキャンペーンのパフォーマンスの監視と管理 &#x200B;](monitor-performance-campaigns.md)
>* [&#x200B; 検索、ソーシャル、CommerceのGoogle Ads コンバージョンデータ &#x200B;](google-conversion-data.md)
