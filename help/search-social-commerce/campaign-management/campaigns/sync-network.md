---
title: 広告ネットワークデータを手動で同期する
description: サポートされているトリガーネットワーク用に、キャンペーン構造とキャンペーンエンティティの同期を手動でサポートする方法を説明します。
exl-id: da437f37-800a-4c56-b5c1-7c985ddd45c8
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 広告ネットワークデータを手動で同期する

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising] ( 以前の [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads]、および [!DNL Yandex] アカウントのみ*

同期とは、Search、Social、および Commerce が、次の場所にある各広告主の広告ネットワークアカウントに関する更新された情報を収集するプロセスです。 [サポートされる広告ネットワーク](/help/search-social-commerce/introduction/supported-inventory.md). このデータには、広告主のキャンペーン構造とキャンペーンエンティティが含まれ、Search、Social、&amp;Commerce で管理またはレポートされるほとんどの属性も含まれます。 クリックデータや、検索、ソーシャル、コマースの外部で入力された入札修飾子や入札修飾子は含まれず、これらは個別に収集されます。

Social および Commerce は、1 日 1 回、および広告ネットワークの 1 つで新しいキャンペーンを検出するたびに、広告ネットワークアカウントと自動的に同期（同期）します。 さらに、検索、ソーシャル、コマース内でおこなわれたキャンペーンデータに対するすべての変更が、直ちに広告ネットワークに送信されます。

指定したアカウント内のすべてのアクティブなキャンペーンと一時停止したキャンペーン、または特定のアクティブなキャンペーンと一時停止したキャンペーンの同期を手動でリクエストできます。 このタスクでは、新規または変更されたエンティティが広告ネットワーク上で収集されます。

次を含むキャンペーンの場合：[!UICONTROL Auto Upload]」オプションを指定すると、トラッキングテンプレートまたはリンク先 URL にない、または変更する必要があるトラッキングコードが生成および投稿されます。 URL は、アカウント設定またはキャンペーンのトラッキング設定のパラメーターに従って生成されます。 関連する項目のトラッキング URL が存在する場合、キーワードの一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など、新しい URL が必要になる場合を除き、URL は再生成されません。

>[!NOTE]
>
>いつでも [バルクシートを作成する](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)を使用すると、オプションで、バルクシートを作成する前に広告ネットワークと同期できます。

1. メインメニューで、 **[!UICONTROL Search]>[!UICONTROL Campaigns]**. サブメニューで、次のいずれかを選択します。 **[!UICONTROL Accounts]** 特定のアカウントまたは **[!UICONTROL Campaigns]** 特定のキャンペーンを同期します。

1. （オプション）リストをフィルタリングして、特定のアカウントやキャンペーンを含めます。

1. 同期する各アカウントまたはキャンペーンの横にあるチェックボックスをオンにします。 一度に最大 50 個のキャンペーンを同期できます。 一度に 5 つを超えるアカウントを同期すると、ジョブは最大 5 アカウントずつのバッチに分類されます。

1. クリック **![その他](/help/search-social-commerce/assets/more.png "その他")** をクリックし、 **[!UICONTROL Sync]**.

同期ジョブのステータスは、 [!UICONTROL Workspace] 表示。 ジョブが表示されるまでに 1 時間以上かかる場合があります。

>[!MORELIKETHIS]
>
>* [バルクシートファイルをダウンロード/作成する](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
