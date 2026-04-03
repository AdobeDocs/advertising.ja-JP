---
title: ' [!DNL Google Ads] 動的検索広告を実装'
description: ' [!DNL Google Ads] 動的検索広告の設定ワークフローについて説明します。'
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/2HsYFUdcvlEr9-LZHMtgS07jZ5A0DOMEj-byGZlf6aE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 614
ht-degree: 0%

---

# [!DNL Google Ads]件の動的検索広告を実装

クリエイティブレベルまたはキーワードレベルおよびクリエイティブレベルのトラッキングのみを含む&#x200B;*[!DNL Google Ads]件の検索専用キャンペーン*

動的検索広告では、広告を表示するタイミングを決定するために、キーワードではなくweb サイトのコンテンツを使用します。 動的検索広告のターゲティングに使用するコンテンツが含まれるweb サイトのページを定義するには、広告グループに個別の動的検索目標を設定するか、web サイトのコンテンツを使用して広告をターゲティングするキャンペーンレベルの設定を選択します。

動的検索広告は、個別に設定することも、バルクシートを使用して設定することもできます。 次の手順には、個々のエンティティを作成するためのリンクが含まれています。

## [!DNL Google Ads]件の動的検索広告を設定する手順

1. [動的検索広告用のキャンペーン ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)を作成します：

   1. 最初に、キャンペーンの予算を1日の検索キャンペーン費用の10%に設定しました。

      広告の価値が証明されたら、後で予算を増やすことができます。

   1. （Web サイトのコンテンツに基づいて動的検索広告を[!DNL Google Ads]に表示する場合） キャンペーン設定の[!UICONTROL DSA Options] セクションで、ドメインのルートドメインと言語を指定します。

      >[!NOTE]
      >
      >ターゲットにするドメインは、[!DNL Google Ads] オーガニック検索インデックスでインデックス付けする必要があります。 また、ドメインに複数の言語のページが含まれており、そのすべてをターゲットにする場合は、言語別にキャンペーンを作成します。

      web サイトドメインを使用して広告をターゲティングしない場合は、広告グループごとに動的検索ターゲットを作成します（ステップ 4を参照）。 ターゲット [個別](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md)を作成するか、[ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用できます。

   1. キャンペーンが検索チャネルと、[!DNL Google Ads]検索ネットワーク （表示ネットワークではなく）のみをターゲットにしていることを確認してください。 これらの設定は、[!UICONTROL Networks and Devices] タブから利用できます。

   1. （オプション）「[!UICONTROL Negatives]」タブのキーワードを除外します。

   1. （オプション）アカウントレベルのトラッキングテンプレートを上書きしますが、下位レベルで上書きできるキャンペーンレベルのトラッキングテンプレートを設定します。

      （サーバーサイドトラッキングを使用しないAdobe Analyticsを使用する広告主）検索、ソーシャル、およびCommerceからAnalyticsへのリバースフィードのトラッキングを含める場合は、アカウントレベルの追加パラメーターにAMO ID トラッキングコードを追加し、コードを最終URLに追加します。 「[様が使用するAdobe Advertising ID  [!DNL Analytics]](/help/integrations/analytics/ids.md)を参照してください。」

1. 次の手順を含め、キャンペーン内で[広告グループ ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)を作成します。

   1. [!UICONTROL Ad Group Type]を&#x200B;**[!UICONTROL Search Dynamic]に設定します。**

   1. すべての広告のデフォルト入札額を設定します。

      個々の動的検索対象のデフォルト入札額を設定した場合は、その値を上書きできます。

   1. （オプション）広告グループレベルのトラッキングテンプレートを設定します。このテンプレートは、より高いレベルのトラッキングテンプレートを上書きしますが、広告レベルで上書きできます。

      キャンペーンレベルでAdobe Analytics トラッキングを追加し、広告グループに含める場合は、ここに追加します。 手順1eを参照してください。

1. [広告グループ内の各動的検索広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)を作成します。

   [!DNL Google Ads]は、各広告の見出し、表示URL、およびランディングページ URLを動的に生成します。 オプションで、広告レベルのトラッキングテンプレートにリダイレクトとトラッキングを追加できます。これにより、トラッキングテンプレートをより高いレベルで上書きできます。
広告レベルのトラッキングでAdobe Analyticsのトラッキングをより高いレベルで上書きする場合は、ここに追加します。 手順1eおよび2cを参照してください。

1. （キャンペーン設定の「DSA オプション」セクションにドメインのルートドメインと言語を含めない場合は必須です。それ以外の場合はオプション）広告グループの[動的検索ターゲット ](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md)を作成します。 オプションで、広告グループレベルの入札をターゲットレベルの入札で上書きできます。

   ターゲットは、広告ネットワークが動的検索広告のターゲットとしてweb サイト内のページのすべてまたはサブセットを使用するかどうかを定義します。 パフォーマンスを最適に追跡するには、動的検索ターゲットごとに1つの広告グループでキャンペーンを設定し、すべての条件をターゲットとする広告グループを含めます。

1. 必要に応じて、[ キャンペーン設定を編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)して、キャンペーンの予算を調整し、キャンペーンから追加のキーワードを除外してトラフィックを絞り込みます。
