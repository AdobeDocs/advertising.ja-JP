---
title: ' [!DNL Google Ads] 個のショッピング キャンペーンを実装'
description: 'ショッピング キャンペーンを設定するためのワークフローについて説明します。 [!DNL Google Ads] '
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/9xk2sCRBNJdRI1az99RyUkAlL-8P9s3OD70Htmnt4r8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# [!DNL Google Ads]件のショッピング キャンペーンを実装

ショッピング キャンペーンの広告では、既存の[!DNL Google Merchant Center]製品フィードの製品に関するデータを使用して、広告を表示する方法と場所を決定します。

[!DNL Google Ads] キャンペーンは、[!DNL Google Shopping Network] 「[!UICONTROL Campaign Type]」を使用して[!UICONTROL Shopping Network]をターゲットにできます。 [!DNL Google Shopping] キャンペーンの設定には、優先度（[!UICONTROL High]、[!UICONTROL Medium]、または[!UICONTROL Low]）が含まれます。 キャンペーンレベルの設定を使用して、ショッピング広告にローカルインベントリ情報を表示することもできます。

広告グループレベルでマルチレベル *[商品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)*&#x200B;を設定することで、ショッピング広告に表示する商品を制御できます。 製品グループは、あらゆる製品属性（カテゴリ、製品タイプ、ブランド、条件、製品ID、カスタムラベル）に基づいています。入札に含めたり除外したりするには、最大7つのレベルの製品グループを作成できます。 最も低いレベルの製品グループに入札を設定し、一致するすべての製品に同じ入札を使用できます。 同じ製品が複数のキャンペーンに含まれている場合、[!DNL Google Ads]は、最初にキャンペーンレベルの優先順位を使用して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを判断します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。

## [!DNL Google Ads]件のショッピング キャンペーンを設定する手順

[の](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)在庫フィード テンプレート [!DNL Google Shopping]を使用するか、[ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用するか、個別にショッピング キャンペーンを設定できます。 次の手順には、個々のエンティティを作成するためのリンクが含まれています。

1. [!DNL Google Merchant Center] アカウントを設定し、製品データを入力します。

1. [Search、Social、およびCommerceが [!DNL Google Merchant Center]  アカウント ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)からデータをダウンロードできるようにします。

1. [ ショッピング ネットワークでキャンペーン ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)を作成します。

1. [ キャンペーン内で広告グループ ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)を作成し、すべての広告のデフォルト入札を設定します。

   個々の製品グループのデフォルト入札を上書きできます。

1. 広告グループの製品グループを作成します。

   1. [すべての製品グループを作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （オプション） [子製品グループを作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   >[!NOTE]
   >ショッピング広告を作成する必要はありません。 広告グループに広告エンティティが含まれていない場合でも、[!DNL Google Ads]には製品の広告が表示されます。

1. （オプション）広告のクリックを追跡するには、[ トラッキング URL ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)を使用してトラッキング URLを生成し、アカウント、キャンペーン、製品グループの設定に追加します。

1. [によって[!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)と[が生成され、[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)のパフォーマンスを監視します。

1. 必要に応じて：

   1. [ キャンペーン設定を編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)して、キャンペーン予算を調整します。

      キャンペーンがポートフォリオの一部である場合、ポートフォリオ設定「[!UICONTROL Auto adjust campaign budget limits]」を使用すると、Search, Social, &amp; Commerceでポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. [広告を作成する必要がなくなった既存の製品グループ ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)、[製品グループを削除](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)するか、新しい[新しい「すべての製品」製品グループ ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)）または[新しい子製品グループ ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)を追加して、追加製品の広告を作成します。

>[!NOTE]
>
>* [!DNL Google Shopping] バルクシート [と](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)在庫フィード テンプレート [を使用して](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) キャンペーンと製品グループを管理するための必須フィールドを参照してください。
>* [!DNL Google Shopping] キャンペーンについて詳しくは、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/2454022)を参照してください。
