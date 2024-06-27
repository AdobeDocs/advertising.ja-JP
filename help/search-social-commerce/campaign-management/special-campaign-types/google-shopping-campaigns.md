---
title: 実装方法 [!DNL Google Ads] 買い物キャンペーン
description: 設定のワークフローについて説明します [!DNL Google Ads] ショッピングキャンペーン。
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 3c702a01df1186e74c4f329a08199ce829be0827
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 実装方法 [!DNL Google Ads] 買い物キャンペーン

買い物キャンペーンの広告では、既存の製品に関するデータが使用されます [!DNL Google Merchant Center] キーワードの代わりに製品フィードを使用して、広告の表示方法と表示場所を決定します。

[!DNL Google Ads] キャンペーンのターゲットは [!DNL Google Shopping Network] の使用 [!UICONTROL Campaign Type] “[!UICONTROL Shopping Network].」と入力します。 の設定 [!DNL Google Shopping] キャンペーンに優先度（[!UICONTROL High], [!UICONTROL Medium]、または [!UICONTROL Low]）に設定します。 オプションで、キャンペーンレベルの設定を使用して、ショッピング広告にローカルの在庫情報を表示できます。

マルチレベルを設定することで、ショッピング広告に表示する製品を制御できます *[製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 広告グループレベルで。 製品グループは、任意の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID およびカスタムラベル）に基づいており、最大 7 つのレベルの製品グループを作成して、入札に含めたり入札から除外したりできます。 一致するすべての製品に同じ入札を使用して、製品グループの最下位レベルに入札を設定できます。 同じ製品が複数のキャンペーンに含まれている場合、 [!DNL Google Ads] では、最初にキャンペーンレベルの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を判断します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

## の設定手順 [!DNL Google Ads] 買い物キャンペーン

以下を使用してショッピングキャンペーンを設定できます [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) （用） [!DNL Google Shopping]を使用する [バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、または個別に。 以下の手順には、個々のエンティティの作成へのリンクが含まれます。

1. の設定 [!DNL Google Merchant Center] アカウントに製品データを入力します。

1. [から検索、ソーシャル、Commerceにデータをダウンロードできるようにする [!DNL Google Merchant Center] アカウント](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [キャンペーンの作成](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) ショッピングネットワーク上で。

1. [広告グループの作成](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) キャンペーン内で、すべての広告のデフォルト入札を設定します。

   個々の製品グループのデフォルト入札を上書きできます。

1. 広告グループの製品グループを作成します。

   1. [「すべての製品」製品グループの作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （オプション） [子製品グループの作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >ショッピング広告を作成する必要はありません。 広告グループに広告エンティティが含まれていない場合でも、 [!DNL Google Ads] 引き続き商品の広告を表示します。

1. （任意）広告に対するクリックを追跡するには、 [トラッキング URL ツールを使用したトラッキング URL の生成](/help/search-social-commerce/tools/click-tracking-url-generate.md)次に、アカウント、キャンペーンまたは製品グループの設定に追加します。

1. パフォーマンスの監視基準 [生成， [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) および [この [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 必要に応じて、

   1. [キャンペーン設定の編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) キャンペーン予算を調整します。

      キャンペーンがポートフォリオの一部である場合は、ポートフォリオ設定「[!UICONTROL Auto adjust campaign budget limits]」を使用すると、検索、ソーシャルおよびCommerceで、ポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. [既存の製品グループの最大入札額の調整](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [製品グループの削除](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) 今後広告を作成または追加しないプロジェクト [新しい「すべての製品」製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)）または [新しい子製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) 追加製品の広告を作成する場合。

>[!NOTE]
>
>* の管理に必要なフィールドを参照してください。 [!DNL Google Shopping] を使用したキャンペーンと製品グループ [バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) および [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* 詳しくは、 [!DNL Google Shopping] キャンペーン、「」を参照 [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/2454022).
