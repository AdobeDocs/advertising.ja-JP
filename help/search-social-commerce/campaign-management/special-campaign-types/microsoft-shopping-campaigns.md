---
title: 実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン
description: 設定のワークフローについて説明します [!DNL Microsoft® Advertising] 買い物キャンペーン。
exl-id: 3fb19b92-5bc0-414e-9234-68310082d0ed
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# 実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン

ショッピングキャンペーンの広告は、既存の [!DNL Microsoft® Merchant Center] 広告の表示方法と表示場所を決定するために、キーワードの代わりに製品フィードを使用します。

[!DNL Microsoft®] 買い物キャンペーンのターゲット： [!DNL Microsoft® Advertising Shopping Network]. 買い物キャンペーンの設定には、商品が販売される特定の国と優先度 ([!DNL High], [!DNL Medium]または [!DNL Low]) をクリックします。 オプションで、特定の属性を持つ製品を宣伝し、特定の場所やデバイスタイプをターゲットにしたり除外したりするために、在庫をフィルタリングできます。

複数レベルのを設定することで、ショッピング広告に表示される製品を制御できます *[製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 広告グループレベルに設定されます。 製品グループは、任意の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID、カスタムラベル）に基づいており、最大 7 レベルの製品グループを作成して、「[!DNL Add Products].&quot; 一致するすべての製品に対して同じ入札を使用して、最も低いレベルの製品グループで入札を設定できます。 複数のキャンペーンに同じ製品が含まれている場合、 [!DNL Microsoft® Advertising] は、最初にキャンペーンレベルの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンが同じ優先順位の場合、最も入札額の高いキャンペーンが適格になります。

## 設定の手順 [!DNL Microsoft® Advertising] 買い物キャンペーン

買い物キャンペーンは、 [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 対象： [!DNL Microsoft® Advertising]、を使用して [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)または個別に。 以下の手順には、個々のエンティティを作成するためのリンクが含まれています。

1. を設定します。 [!DNL Microsoft® Merchant Center] アカウントを作成し、製品データを入力します。

1. [検索、ソーシャル、コマースで [!DNL Microsoft® Merchant Center] アカウント](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [キャンペーンの作成](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 買い物ネットワーク上で

1. [広告グループの作成](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) キャンペーン内で、すべての広告に対するデフォルトの入札額を設定します。

個々の製品グループのデフォルト入札額を上書きできます。

1. 広告グループの製品グループの作成：

   1. [「すべての製品」製品グループを作成する](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （オプション） [子製品グループの作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. 作成 [製品広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 次を使用 [各ショッピング広告に含まれる可能性があるプロモーションライン](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) を広告グループ内に追加します。

      Microsoft® Advertising は、広告のコピーとランディングページの URL を各広告に動的に生成します。

      >[!NOTE]
      >
      >広告グループに広告エンティティが含まれていない場合でも、 [!DNL Microsoft® Advertising] は、製品の広告を表示します。

1. （オプション）広告のクリックを追跡するには、 [トラッキング URL ツールを使用してトラッキング URL を生成します](/help/search-social-commerce/tools/click-tracking-url-generate.md). ベストプラクティスは、トラッキング URL を [!UICONTROL Tracking Template] アカウント、キャンペーンまたは製品グループの設定の「 」フィールド。 メンテナンスを容易にするには、できる限り高いレベルで追加します。

   または、 [!DNL Microsoft® Merchant Center] アカウント。 これをおこなうには、トラッキング URL を、必要に応じて「link」または「mobile_link」フィールドの値と共に、カスタム列に含めます。[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)」と入力します。 「bingads_redirect」フィールドの値は、「link」フィールドと「mobile_link」フィールドの値を置き換えます。 このメソッドを使用して生成される URL には、検索、ソーシャル、コマースのアカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

1. 次の基準でパフォーマンスを監視： [の生成 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 必要に応じて、次の手順に従います。

   1. [キャンペーン設定の編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) ：キャンペーン予算を調整します。

      キャンペーンがポートフォリオに含まれている場合、ポートフォリオ設定&quot;[!UICONTROL Auto adjust campaign budget limits]「検索、ソーシャル、コマースで、ポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. 既存の製品グループの最大入札額を調整したり、広告を作成しなくなった製品グループを削除したり、新しい「すべての製品」製品グループまたは新しい子製品グループを追加して、追加の製品の広告を作成したりします。

>[!NOTE]
>
>* 管理に必要なフィールドを参照してください。 [!DNL Microsoft® Shopping] キャンペーンと製品グループを使用 [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) および [在庫フィードテンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* 詳しくは、 [!DNL Microsoft® Shopping] キャンペーンについては、 [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/50903).
