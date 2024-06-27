---
title: 実装方法 [!DNL Microsoft Advertising] 買い物キャンペーン
description: 設定のワークフローについて説明します [!DNL Microsoft Advertising] ショッピングキャンペーン。
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 実装方法 [!DNL Microsoft Advertising] 買い物キャンペーン

買い物キャンペーンの広告では、既存の製品に関するデータが使用されます [!DNL Microsoft Merchant Center] キーワードの代わりに製品フィードを使用して、広告の表示方法と表示場所を決定します。

[!DNL Microsoft] ショッピングキャンペーンのターゲット [!DNL Microsoft Advertising Shopping Network]. ショッピングキャンペーンの設定には、商品が販売される指定された国と優先度（[!DNL High], [!DNL Medium]、または [!DNL Low]）に設定します。 オプションで、在庫をフィルタリングして、特定の属性を持つ製品を広告したり、特定の場所やデバイスタイプをターゲットまたは除外したりできます。

マルチレベルを設定することで、ショッピング広告に表示する製品を制御できます *[製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 広告グループレベルで。 製品グループは、任意の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID およびカスタムラベル）に基づいており、最大 7 つのレベルの製品グループを作成して、次を含まない入札に含めたり入札から除外したりできます[!DNL Add Products].」と入力します。 一致するすべての製品に同じ入札を使用して、製品グループの最下位レベルに入札を設定できます。 同じ製品が複数のキャンペーンに含まれている場合、 [!DNL Microsoft Advertising] では、最初にキャンペーンレベルの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を判断します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

## の設定手順 [!DNL Microsoft Advertising] 買い物キャンペーン

以下を使用してショッピングキャンペーンを設定できます [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) （用） [!DNL Microsoft Advertising]を使用する [バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、または個別に。 以下の手順には、個々のエンティティの作成へのリンクが含まれます。

1. の設定 [!DNL Microsoft Merchant Center] アカウントに製品データを入力します。

1. [から検索、ソーシャル、Commerceにデータをダウンロードできるようにする [!DNL Microsoft Merchant Center] アカウント](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [キャンペーンの作成](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) ショッピングネットワーク上で。

1. [広告グループの作成](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) キャンペーン内で、すべての広告のデフォルト入札を設定します。

   個々の製品グループのデフォルト入札を上書きできます。

1. 広告グループの製品グループを作成します。

   1. [「すべての製品」製品グループの作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （オプション） [子製品グループの作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. 作成 [製品広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) （を使用） [各ショッピング広告に含める可能性のあるプロモーション明細行](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) 広告グループ内。

      Microsoft Advertisingは、各広告の広告コピーとランディングページ URL を動的に生成します。

      >[!NOTE]
      >
      >広告グループに広告エンティティが含まれていない場合でも、 [!DNL Microsoft Advertising] 引き続き商品の広告を表示します。

1. （任意）広告に対するクリックを追跡するには、 [トラッキング URL ツールを使用したトラッキング URL の生成](/help/search-social-commerce/tools/click-tracking-url-generate.md). ベストプラクティスは、トラッキング URL をに追加することです。 [!UICONTROL Tracking Template] アカウント、キャンペーンまたは製品グループの設定のフィールド。 メンテナンスを容易にするには、可能な限り最高のレベルで追加します。

   または、製品データにトラッキング URL を追加することもできます [!DNL Microsoft Merchant Center] アカウント。 これをおこなうには、トラッキング URL を値と共に「link」または「mobile_link」フィールドの値を（必要に応じて）カスタム列に含めます」[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)製品フィード内。 「bingads_redirect」フィールドの値は、「link」および「mobile_link」フィールドの値を置き換えます。 この方法で生成される URL には、検索、ソーシャル、Commerceの各アカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

1. パフォーマンスの監視基準 [生成， [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 必要に応じて、

   1. [キャンペーン設定の編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) キャンペーン予算を調整します。

      キャンペーンがポートフォリオの一部である場合は、ポートフォリオ設定「[!UICONTROL Auto adjust campaign budget limits]」を使用すると、検索、ソーシャルおよびCommerceで、ポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. 既存の製品グループの最大入札額を調整するか、広告を作成する必要がなくなった製品グループを削除するか、新しい「すべての製品」製品グループまたは新しい子製品グループを追加して、追加の製品の広告を作成します。

>[!NOTE]
>
>* の管理に必要なフィールドを参照してください。 [!DNL Microsoft Shopping] を使用したキャンペーンと製品グループ [バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) および [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* 詳しくは、 [!DNL Microsoft Shopping] キャンペーン、「」を参照 [[!DNL Microsoft Advertising] 詳細を見る](https://help.ads.microsoft.com/#apex/3/en/50903).
