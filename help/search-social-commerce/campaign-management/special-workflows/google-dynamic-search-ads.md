---
title: 動的検索広告  [!DNL Google Ads]  実装
description: 動的検索広告を設定するためのワークフロー  [!DNL Google Ads]  ついて説明します。
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# 動的検索広告 [!DNL Google Ads] 実装

クリエイティブレベルまたはキーワードおよびクリエイティブレベルのトラッキングのみを使用した検索専用キャンペーンを *[!DNL Google Ads]スト* ます。

動的検索広告では、キーワードの代わりに web サイトのコンテンツを使用して、広告を表示するタイミングを決定します。 広告グループに対して個別の動的検索ターゲットを設定するか、web サイトのコンテンツを使用して広告をターゲットにするキャンペーンレベルの設定を選択することで、動的検索広告のターゲットにするコンテンツを使用する web サイトのページを定義できます。

動的検索広告は、個別に設定することも、バルクシートを使用して設定することもできます。 以下の手順には、個々のエンティティの作成へのリンクが含まれます。

## 動的検索広告 [!DNL Google Ads] 設定手順

1. 動的検索広告の [ キャンペーンを作成 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md):

   1. 最初に、キャンペーン予算を毎日の検索キャンペーン費用の 10% に設定します。

      広告が価値を証明した後で、後で予算を増やすことができます。

   1. （Web サイトのコンテンツに基づ [!DNL Google Ads] て動的検索広告を表示する場合）キャンペーン設定の [!UICONTROL DSA Options] セクションで、ドメインのルートドメインと言語を指定します。

      >[!NOTE]
      >
      >ターゲットにする [!DNL Google Ads] オーガニック検索インデックスでドメインのインデックスを作成する必要があります。 また、ドメインに複数の言語のページが含まれ、すべてのページをターゲットにする場合は、言語ごとに個別のキャンペーンを作成します。

      Web サイトドメインを使用して広告をターゲットしない場合は、広告グループごとに動的検索ターゲットを作成します（手順 4 を参照）。 ターゲットは [ 個別に ](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) 作成することも、[ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用して作成することもできます。

   1. キャンペーンが検索チャネルと [!DNL Google Ads] の検索ネットワーク（ディスプレイネットワークではない）のみをターゲットにしていることを確認します。 これらの設定は、「[!UICONTROL Networks and Devices]」タブから使用できます。

   1. （任意）「[!UICONTROL Negatives]」タブでのキーワードの除外。

   1. （オプション）キャンペーンレベルの追跡テンプレートを設定します。このテンプレートはアカウントレベルの追跡テンプレートを上書きしますが、下位レベルで上書きできます。

      （サーバーサイドトラッキングなしのAdobe Analyticsを使用する広告主）検索、ソーシャル、Commerceから Analytics へのリバースフィードのトラッキングを含める場合は、AMO ID トラッキングコードをアカウントレベルの追加パラメーターに追加し、最終的な URL にコードを追加します。 「[ が使用するAdobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)」を参照してください。

1. キャンペーン内で [ 広告グループを作成 ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) します。これには次の手順が含まれます。

   1. [!UICONTROL Ad Group Type] を **[!UICONTROL Search Dynamic].** に設定します。

   1. すべての広告のデフォルト入札を設定します。

      個々の動的検索ターゲットのデフォルト入札は、設定した場合に上書きできます。

   1. （オプション）広告グループレベルの追跡テンプレートを設定します。このテンプレートは、上位レベルにあるすべての追跡テンプレートを上書きしますが、広告レベルで上書きできます。

      キャンペーンレベルでAdobe Analyticsのトラッキングを追加していて、広告グループに含める場合は、ここに追加します。 手順 1e を参照してください。

1. 広告グループ内に [ 各動的検索広告を作成 ](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) します。

   [!DNL Google Ads] は、各広告のヘッドライン、ディスプレイ URL およびランディングページ URL を動的に生成します。 オプションで、広告レベルの追跡テンプレートにリダイレクトと追跡を追加できます。これにより、上位レベルの追跡テンプレートが上書きされます。
上位レベルのAdobe Analytics トラッキングを広告レベルのトラッキングで上書きする場合は、ここに追加します。 手順 1e と 2c を参照してください。

1. （キャンペーン設定の DSA オプション セクションにドメインのルートドメインと言語を含めない場合は必須。それ以外の場合はオプション）広告グループの [ 動的検索ターゲット ](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) を作成します。 オプションで、広告グループレベルの入札をターゲットレベルの入札で上書きできます。

   ターゲットは、広告ネットワークで web サイトのページのすべてを使用するか、サブセットを使用して動的検索広告をターゲットにするかを定義します。 パフォーマンスを最適に追跡するには、動的検索ターゲットごとに 1 つの広告グループでキャンペーンを設定し、すべての条件をターゲットにする広告グループを含めます。

1. 必要に応じて [ キャンペーン設定を編集 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) し、キャンペーンの予算を調整し、キャンペーンから追加のキーワードを除外してトラフィックを絞り込みます。
