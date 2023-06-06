---
title: 実装方法 [!DNL Google Ads] ショッピングキャンペーン
description: 設定のワークフローについて説明します [!DNL Google Ads] 買い物キャンペーン。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 実装方法 [!DNL Google Ads] ショッピングキャンペーン

ショッピングキャンペーンの広告は、既存の [!DNL Google Merchant Center] 広告の表示方法と表示場所を決定するために、キーワードの代わりに製品フィードを使用します。

[!DNL Google Ads] キャンペーンは、 [!DNL Google Shopping Network] の使用 [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; 設定 [!DNL Google Shopping] キャンペーンには優先順位 ([!UICONTROL High], [!UICONTROL Medium]または [!UICONTROL Low]) をクリックします。 オプションで、キャンペーンレベルの設定を使用して、ショッピング広告にローカルの在庫情報を表示できます。

複数レベルのを設定することで、ショッピング広告に表示される製品を制御できます *[製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 広告グループレベルに設定されます。 製品グループは、任意の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID、カスタムラベル）に基づいており、最大 7 レベルの製品グループを作成して入札に含めたり、入札から除外したりできます。 一致するすべての製品に対して同じ入札を使用して、最も低いレベルの製品グループで入札を設定できます。 複数のキャンペーンに同じ製品が含まれている場合、 [!DNL Google Ads] は、最初にキャンペーンレベルの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンが同じ優先順位の場合、最も入札額の高いキャンペーンが適格になります。

## 設定の手順 [!DNL Google Ads] ショッピングキャンペーン

ショッピングキャンペーンは、 [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 対象 [!DNL Google Shopping]、を使用 [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)または個別に。 以下の手順には、個々のエンティティを作成するためのリンクが含まれています。

1. の設定 [!DNL Google Merchant Center] アカウントを作成し、製品データを入力します。

1. [検索、ソーシャル、コマースで [!DNL Google Merchant Center] アカウント](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [キャンペーンの作成](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 買い物ネットワーク上で

1. [広告グループの作成](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) キャンペーン内で、すべての広告に対するデフォルトの入札額を設定します。

個々の製品グループのデフォルト入札額を上書きできます。

1. 広告グループの製品グループの作成：

   1. [「すべての製品」製品グループを作成する](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （オプション） [子製品グループの作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).
   >[!NOTE]
   >買い物広告を作成する必要はありません。 広告グループに広告エンティティが含まれていない場合でも、 [!DNL Google Ads] は、製品の広告を表示します。

1. （オプション）広告のクリックを追跡するには、 [トラッキング URL ツールを使用してトラッキング URL を生成します](/help/search-social-commerce/tools/click-tracking-url-generate.md)をクリックし、アカウント、キャンペーンまたは製品グループの設定に追加します。

1. 次の基準でパフォーマンスを監視 [生成 [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) および [の [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 必要に応じて、次の手順に従います。

   1. [キャンペーン設定の編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) ：キャンペーン予算を調整します。

      キャンペーンがポートフォリオに含まれている場合、ポートフォリオ設定&quot;[!UICONTROL Auto adjust campaign budget limits]「検索、ソーシャル、コマースで、ポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. [既存の製品グループの最大入札額を調整](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [製品グループを削除](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) 広告の作成や追加を停止する [新しい「すべての製品」製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) または [新しい子製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) 追加の製品の広告を作成する場合。

>[!NOTE]
>
>* 管理に必要なフィールドを参照してください。 [!DNL Google Shopping] キャンペーンと製品グループを使用 [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) および [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* 詳しくは、 [!DNL Google Shopping] キャンペーンについては、 [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/2454022).

