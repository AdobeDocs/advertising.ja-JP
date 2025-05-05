---
title: 買い物キャ  [!DNL Google Ads]  ペーンの実装
description: 買い物キャンペーンを設定する際のワークフロー  [!DNL Google Ads]  ついて説明します。
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 買い物キャンペーン [!DNL Google Ads] 実装

買い物キャンペーンの広告では、キーワードの代わりに、既存の [!DNL Google Merchant Center] 製品フィード内の製品に関するデータを使用して、広告の表示方法と表示場所を決定します。

キャンペーン [!DNL Google Ads]、[!UICONTROL Campaign Type] 「[!UICONTROL Shopping Network]」を使用して [!DNL Google Shopping Network] ールをターゲットにすることができます。 キャンペーン [!DNL Google Shopping] 設定には優先度（[!UICONTROL High]、[!UICONTROL Medium]、[!UICONTROL Low]）が含まれます。 オプションで、キャンペーンレベルの設定を使用して、ショッピング広告にローカルの在庫情報を表示できます。

広告グループレベルでマルチレベルの *[製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* を設定することで、ショッピング広告で表示する製品を制御できます。 製品グループは、任意の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID およびカスタムラベル）に基づいており、最大 7 つのレベルの製品グループを作成して、入札に含めたり入札から除外したりできます。 一致するすべての製品に同じ入札を使用して、製品グループの最下位レベルに入札を設定できます。 同じ製品が複数のキャンペーンに含まれる場合、[!DNL Google Ads] は最初にキャンペーンレベルの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

## 買い物キャンペーン [!DNL Google Ads] 設定手順

[ 在庫フィードテンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) を使用するか、[bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用するか、または個別に使用して、ショッピングキャンペーンを設定で [!DNL Google Shopping] ます。 以下の手順には、個々のエンティティの作成へのリンクが含まれます。

1. [!DNL Google Merchant Center] アカウントを設定し、製品データを入力します。

1. [ 検索、ソーシャル、Commerceが  [!DNL Google Merchant Center]  アカウントからデータをダウンロードするのを許可する ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)

1. ショッピングネットワーク上で [ キャンペーンを作成 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) します。

1. キャンペーン内で [ 広告グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) し、すべての広告にデフォルト入札を設定します。

   個々の製品グループのデフォルト入札を上書きできます。

1. 広告グループの製品グループを作成します。

   1. [ 「すべての製品」製品グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （任意） [ 子製品グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) します。

   >[!NOTE]
   >ショッピング広告を作成する必要はありません。 広告グループに広告エンティティが含まれていない場合でも、[!DNL Google Ads] では引き続き製品の広告が表示されます。

1. （任意）広告のクリックをトラッキングするには、[ トラッキング URL ツールを使用してトラッキング URL を生成 ](/help/search-social-commerce/tools/click-tracking-url-generate.md) してアカウント、キャンペーン、製品グループの設定に追加します。

1. [!UICONTROL AdWords Shopping Performance Report][&#128279;](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) と [!UICONTROL Product Group Report][&#128279;](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md) を生成して  パフォーマンスを監視  ます。

1. 必要に応じて、

   1. [ キャンペーン設定を編集 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) して、キャンペーンの予算を調整します。

      キャンペーンがポートフォリオの一部である場合、ポートフォリオ設定「[!UICONTROL Auto adjust campaign budget limits]」を使用すると、検索、ソーシャルおよびCommerceで、ポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. [ 広告を作成する必要がなくなった既存の製品グループの最大入札額を調整 ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)、[ 製品グループを削除 ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)、または [ 新しい「すべての製品」製品グループ ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)）または [ 新しい子製品グループ ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) を追加して、追加の製品の広告を作成します。

>[!NOTE]
>
>* [ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) および [ 在庫フィードテンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) を使用して [!DNL Google Shopping] キャンペーンおよび製品グループを管理するための必須フィールドを参照してください。
>* [!DNL Google Shopping] キャンペーンについて詳しくは、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/2454022) を参照してください。
