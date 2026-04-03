---
title: ' [!DNL Microsoft Advertising] 個のショッピング キャンペーンを実装'
description: 'ショッピング キャンペーンを設定するためのワークフローについて説明します。 [!DNL Microsoft Advertising] '
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/2SXWaNmPPcXmljB2DUKq9DNWgPv9Qb-0t3SJcdO6aR8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 587
ht-degree: 0%

---

# [!DNL Microsoft Advertising]件のショッピング キャンペーンを実装

ショッピング キャンペーンの広告では、既存の[!DNL Microsoft Merchant Center]製品フィードの製品に関するデータを使用して、広告を表示する方法と場所を決定します。

[!DNL Microsoft]件のショッピング キャンペーンが[!DNL Microsoft Advertising Shopping Network]をターゲットにしています。 ショッピング キャンペーンの設定には、製品が販売される指定された国と優先度（[!DNL High]、[!DNL Medium]、または[!DNL Low]）が含まれます。 オプションで、在庫をフィルタリングして、特定の属性を持つ商品を広告したり、特定の場所やデバイスタイプをターゲットまたは除外したりすることができます。

広告グループレベルでマルチレベル *[商品グループ](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)*&#x200B;を設定することで、ショッピング広告に表示する商品を制御できます。 製品グループは、あらゆる製品属性（カテゴリ、製品タイプ、ブランド、条件、製品ID、およびカスタムラベル）に基づいています。また、「[!DNL Add Products]」を含めずに、入札に含めたり除外したりするための製品グループを最大7 レベルまで作成できます。 最も低いレベルの製品グループに入札を設定し、一致するすべての製品に同じ入札を使用できます。 同じ製品が複数のキャンペーンに含まれている場合、[!DNL Microsoft Advertising]は、最初にキャンペーンレベルの優先順位を使用して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを判断します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。

## [!DNL Microsoft Advertising]件のショッピング キャンペーンを設定する手順

[の](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)在庫フィード テンプレート [!DNL Microsoft Advertising]を使用するか、[ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用するか、個別にショッピング キャンペーンを設定できます。 次の手順には、個々のエンティティを作成するためのリンクが含まれています。

1. [!DNL Microsoft Merchant Center] アカウントを設定し、製品データを入力します。

1. [Search、Social、およびCommerceが [!DNL Microsoft Merchant Center]  アカウント ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)からデータをダウンロードできるようにします。

1. [ ショッピング ネットワークでキャンペーン ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)を作成します。

1. [ キャンペーン内で広告グループ ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)を作成し、すべての広告のデフォルト入札を設定します。

   個々の製品グループのデフォルト入札を上書きできます。

1. 広告グループの製品グループを作成します。

   1. [すべての製品グループを作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （オプション） [子製品グループを作成](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. 広告グループ内の各ショッピング広告[に含める可能性のある](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) プロモーション行を含む[製品広告](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md)を作成します。

      Microsoft Advertisingは、各広告の広告コピーとランディングページのURLを動的に生成します。

      >[!NOTE]
      >
      >広告グループに広告エンティティが含まれていない場合でも、[!DNL Microsoft Advertising]には製品の広告が表示されます。

1. （オプション）広告のクリックを追跡するには、[ トラッキング URL ツールを使用してトラッキング URLを生成します](/help/search-social-commerce/tools/click-tracking-url-generate.md)。 ベストプラクティスは、アカウント、キャンペーン、または製品グループの設定の[!UICONTROL Tracking Template] フィールドにトラッキング URLを追加することです。 メンテナンスを容易にするために、可能な限り高いレベルで追加してください。

   または、[!DNL Microsoft Merchant Center] アカウント内の製品データにトラッキング URLを追加することもできます。 これを行うには、トラッキング URLを、必要に応じて「リンク」または「mobile_link」フィールドの値と共に、製品フィード内のカスタム列「[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)」に含めます。 「bingads_redirect」フィールドの値は、「link」フィールドと「mobile_link」フィールドの値に置き換わります。 この方法で生成されたURLには、Search, Social, &amp; Commerce アカウントまたはキャンペーン設定で指定されたトラッキングパラメーターが含まれていません。

1. [を生成して[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md) パフォーマンスを監視します。

1. 必要に応じて：

   1. [ キャンペーン設定を編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)して、キャンペーン予算を調整します。

      キャンペーンがポートフォリオの一部である場合、ポートフォリオ設定「[!UICONTROL Auto adjust campaign budget limits]」を使用すると、Search, Social, &amp; Commerceでポートフォリオ内のすべてのキャンペーンの予算を最適化できます。

   1. 既存の製品グループの最大入札額を調整するか、広告を作成する必要がなくなった製品グループを削除するか、新しい「すべての製品」製品グループまたは新しい子製品グループを追加して追加製品の広告を作成します。

>[!NOTE]
>
>* [!DNL Microsoft Shopping] バルクシート [と](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)在庫フィード テンプレート [を使用して](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) キャンペーンと製品グループを管理するための必須フィールドを参照してください。
>* [!DNL Microsoft Shopping] キャンペーンについて詳しくは、[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/50903)を参照してください。
