---
title: 買い物キャ  [!DNL Microsoft Advertising]  ペーンの実装
description: 買い物キャンペーンを設定する際のワークフロー  [!DNL Microsoft Advertising]  ついて説明します。
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 買い物キャンペーン [!DNL Microsoft Advertising] 実装

買い物キャンペーンの広告では、キーワードの代わりに、既存の [!DNL Microsoft Merchant Center] 製品フィード内の製品に関するデータを使用して、広告の表示方法と表示場所を決定します。

買い物キャンペーン [!DNL Microsoft] ター [!DNL Microsoft Advertising Shopping Network] ットをターゲットにします。 買い物キャンペーンの設定には、商品が販売される指定された国と優先度（[!DNL High]、[!DNL Medium] または [!DNL Low]）が含まれます。 オプションで、在庫をフィルタリングして、特定の属性を持つ製品を広告したり、特定の場所やデバイスタイプをターゲットまたは除外したりできます。

広告グループレベルでマルチレベルの *[製品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* を設定することで、ショッピング広告で表示する製品を制御できます。 製品グループは、任意の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID およびカスタムラベル）に基づいており、最大 7 つのレベルの製品グループを作成して、「[!DNL Add Products]」を含めずに、入札に含めたり入札から除外したりできます。 一致するすべての製品に同じ入札を使用して、製品グループの最下位レベルに入札を設定できます。 同じ製品が複数のキャンペーンに含まれる場合、[!DNL Microsoft Advertising] は最初にキャンペーンレベルの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

## 買い物キャンペーン [!DNL Microsoft Advertising] 設定手順

[ 在庫フィードテンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) を使用するか、[bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用するか、または個別に使用して、ショッピングキャンペーンを設定で [!DNL Microsoft Advertising] ます。 以下の手順には、個々のエンティティの作成へのリンクが含まれます。

1. [!DNL Microsoft Merchant Center] アカウントを設定し、製品データを入力します。

1. [ 検索、ソーシャル、Commerceが  [!DNL Microsoft Merchant Center]  アカウントからデータをダウンロードするのを許可する ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)

1. ショッピングネットワーク上で [ キャンペーンを作成 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) します。

1. キャンペーン内で [ 広告グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) し、すべての広告にデフォルト入札を設定します。

   個々の製品グループのデフォルト入札を上書きできます。

1. 広告グループの製品グループを作成します。

   1. [ 「すべての製品」製品グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （任意） [ 子製品グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) します。

   1. [ プロモーションライン ](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) を使用して [ 製品広告 ](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) を作成し、広告グループ内の各ショッピング広告に含める可能性があります。

      Microsoft Advertisingは、各広告の広告コピーとランディングページ URL を動的に生成します。

      >[!NOTE]
      >
      >広告グループに広告エンティティが含まれていない場合でも、[!DNL Microsoft Advertising] では引き続き製品の広告が表示されます。

1. （任意）広告に対するクリックを追跡するには、[ トラッキング URL ツールを使用したトラッキング URL を生成 ](/help/search-social-commerce/tools/click-tracking-url-generate.md) します。 ベストプラクティスは、アカウント、キャンペーンまたは製品グループの設定の「[!UICONTROL Tracking Template]」フィールドにトラッキング URL を追加することです。 メンテナンスを容易にするには、可能な限り最高のレベルで追加します。

   または、トラッキング URL を [!DNL Microsoft Merchant Center] アカウント内の製品データに追加できます。 これを行うには、トラッキング URL を、必要に応じて「link」または「mobile_link」フィールドの値と共に、製品フィード内のカスタム列「[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)」に含めます。 「bingads_redirect」フィールドの値は、「link」および「mobile_link」フィールドの値を置き換えます。 この方法で生成される URL には、検索、ソーシャル、Commerceの各アカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

1. [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md) を生成してパフォーマンス [ 監視します。

1. 必要に応じて、

   1. [ キャンペーン設定を編集 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) して、キャンペーンの予算を調整します。

      キャンペーンがポートフォリオの一部である場合、ポートフォリオ設定「[!UICONTROL Auto adjust campaign budget limits]」を使用すると、検索、ソーシャルおよびCommerceで、ポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. 既存の製品グループの最大入札額を調整するか、広告を作成する必要がなくなった製品グループを削除するか、新しい「すべての製品」製品グループまたは新しい子製品グループを追加して、追加の製品の広告を作成します。

>[!NOTE]
>
>* [ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) および [ 在庫フィードテンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) を使用して [!DNL Microsoft Shopping] キャンペーンおよび製品グループを管理するための必須フィールドを参照してください。
>* [!DNL Microsoft Shopping] キャンペーンについて詳しくは、[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/50903) を参照してください。
