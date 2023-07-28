---
title: 実装方法 [!DNL Google Ads] 動的検索広告
description: 設定のワークフローについて説明します [!DNL Google Ads] 動的検索広告。
exl-id: 4c806824-b582-46dc-8d88-85c73bfb0944
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# 実装方法 [!DNL Google Ads] 動的検索広告

*[!DNL Google Ads]クリエイティブレベルまたはキーワードレベルおよびクリエイティブレベルの追跡のみを含む検索のみのキャンペーン*

動的検索広告は、広告を表示するタイミングを決定するために、キーワードの代わりに Web サイトのコンテンツを使用します。 広告グループに対して個別の動的検索ターゲットを設定するか、Web サイトのコンテンツを使用して広告をターゲットにするキャンペーンレベルの設定を選択することで、動的検索広告のターゲットにコンテンツを使用するページを定義できます。

動的検索広告は、個別に設定することも、一括送信シートを使用して設定することもできます。 以下の手順には、個々のエンティティを作成するためのリンクが含まれています。

## 設定の手順 [!DNL Google Ads] 動的検索広告

1. [キャンペーンの作成](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 動的検索広告の場合：

   1. 最初に、キャンペーンの予算を、検索キャンペーンの日別支出の 10%に設定します。

      広告がその価値を証明した後で、予算を増やすことができます。

   1. ( 必要に応じて [!DNL Google Ads] web サイトのコンテンツに基づいて動的検索広告を表示するには ) [!UICONTROL DSA Options] 」セクションに表示されます。

      >[!NOTE]
      >
      >ドメインは、 [!DNL Google Ads] ターゲットとするオーガニック検索インデックス。 また、ドメインに複数の言語のページが含まれ、それらすべてをターゲットにする場合は、言語ごとに個別のキャンペーンを作成します。

      Web サイトドメインを使用して広告をターゲット設定しない場合は、各広告グループに対して動的検索ターゲットを作成します（手順 4 を参照）。 ターゲットを作成できます。 [個別に](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) または [バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. キャンペーンで、検索チャネルと [!DNL Google Ads] ネットワークを検索します（ディスプレイネットワークではありません）。 これらの設定は、 [!UICONTROL Networks and Devices] タブをクリックします。

   1. （オプション） [!UICONTROL Negatives] タブをクリックします。

   1. （オプション）アカウントレベルのトラッキングテンプレートを上書きするが、下位レベルで上書きできる、キャンペーンレベルのトラッキングテンプレートを設定します。

      ( サーバーサイドトラッキングを使用しないAdobe Analyticsの広告主 )Search、Social、および Commerce から Analytics へのリバースフィードのトラッキングを含める場合、s_kwcid トラッキングコードをアカウントレベルの追加パラメーターに追加し、コードを最終 URL に追加します。 参照：[s_kwcid トラッキングパラメーター](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [広告グループの作成](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) 次の手順を含む、キャンペーン内の次の手順に従います。

   1. を設定します。 [!UICONTROL Ad Group Type] から **[!UICONTROL Search Dynamic].**

   1. すべての広告に対するデフォルトの入札額を設定します。

      設定した場合、個々の動的検索ターゲットのデフォルト入札額を上書きできます。

   1. （オプション）広告グループレベルのトラッキングテンプレートを設定します。このテンプレートは、上位レベルのトラッキングテンプレートを上書きしますが、広告レベルで上書きできます。

      キャンペーンレベルでAdobe Analyticsトラッキングを追加し、広告グループに含める場合は、ここに追加します。 手順 1e を参照してください。

1. [各動的検索広告の作成](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) を広告グループ内に追加します。

   [!DNL Google Ads] 各広告のヘッドライン、表示 URL、ランディングページ URL を動的に生成します。 オプションで、広告レベルのトラッキングテンプレートにリダイレクトとトラッキングを追加できます。このテンプレートは、上位レベルのトラッキングテンプレートを上書きします。
広告レベルの追跡を使用して、より高いレベルでAdobe Analyticsの追跡を上書きする場合は、ここに追加します。 手順 1e と 2c を参照してください。

1. （キャンペーン設定の「DSA Options」セクションにドメインのルートドメインと言語を含めない場合は必須。含めない場合はオプション）作成する [動的検索ターゲット](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) （広告グループ用） オプションで、広告グループレベルの入札をターゲットレベルの入札で上書きできます。

   ターゲットは、動的検索広告をターゲットにするために、広告ネットワークが Web サイト内のページのすべてを使用するか、サブセットを使用するかを定義します。 パフォーマンスを最も高く追跡するには、動的検索ターゲットごとに 1 つの広告グループでキャンペーンを設定し、すべての条件をターゲットにする広告グループを含めます。

1. 必要に応じて、 [キャンペーン設定の編集](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) ：キャンペーンから追加のキーワードを除外して、キャンペーンの予算を調整し、トラフィックを絞り込むため。
