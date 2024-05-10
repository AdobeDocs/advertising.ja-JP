---
title: 広告ネットワークデータの手動同期
description: サポートされる広告ネットワークのキャンペーン構造とキャンペーンエンティティの同期を手動でトリガーする方法について説明します。
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 広告ネットワークデータの手動同期

*[!DNL Google Ads], [!DNL Microsoft Advertising] （formerly [!DNL Bing Ads]）、 [!DNL Yahoo! Japan Ads], [!DNL Yandex]、および既存 [!DNL Baidu] アカウントのみ*

同期とは、検索、ソーシャル、Commerceが、接続された各広告主の広告ネットワークアカウントに関する最新情報を収集するプロセスです [サポートされる広告ネットワーク](/help/search-social-commerce/introduction/supported-inventory.md). このデータには、広告主のキャンペーン構造とキャンペーンエンティティが含まれ、検索、ソーシャル、Commerceで管理またはレポートされる属性のほとんどが含まれます。 クリックデータや、検索、ソーシャル、Commerceの外部で入力された入札および入札修飾子は含まれません。これらは個別に収集されます。

検索、ソーシャル、Commerceは、1 日に 1 回、および広告ネットワークの 1 つに新しいキャンペーンが検出されるたびに、広告ネットワークアカウントと自動的に同期（同期）します。 さらに、検索、ソーシャル、Commerce内で作成されたキャンペーンデータに対するすべての変更を、即座に広告ネットワークに送信します。

指定したアカウントまたは特定のアクティブなキャンペーンと一時停止されたキャンペーンにある、アクティブなキャンペーンと一時停止されたキャンペーンすべての同期を手動でリクエストできます。 このタスクは、広告ネットワーク上の新しいエンティティまたは変更されたエンティティを収集します。

「」を使用したキャンペーンの場合[!UICONTROL Auto Upload]「」オプションを選択すると、同期操作によって、トラッキングテンプレートまたは宛先 URL に見つからないか、変更する必要があるトラッキングコードも生成および投稿されます。 URL は、アカウント設定またはキャンペーンのトラッキング設定のパラメーターに従って生成されます。 関連する項目のトラッキング URL が存在する場合、新しい URL が必要ない限り（キーワード一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。

>[!NOTE]
>
>いつでも [バルクシートの作成](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)バルクシートを作成する前に、オプションで広告ネットワークと同期することもできます。

1. メインメニューで、 **[!UICONTROL Search]>[!UICONTROL Campaigns]**. サブメニューで、次のいずれかを選択します **[!UICONTROL Accounts]** 特定のアカウントですべてのキャンペーンを同期するには **[!UICONTROL Campaigns]** 特定のキャンペーンを同期します。

1. （任意）リストをフィルタリングして、特定のアカウントやキャンペーンを含めます。

1. 同期する各アカウントまたはキャンペーンの横にあるチェックボックスを選択します。 一度に 50 件までのキャンペーンを同期できます。 一度に 5 つを超えるアカウントを同期する場合、ジョブは最大 5 つのアカウントのバッチに分割されます。

1. クリック **![詳細](/help/search-social-commerce/assets/more.png "詳細")** ツールバーのを選択し、 **[!UICONTROL Sync]**.

同期ジョブのステータスは、 [!UICONTROL Workspace] 表示。 ジョブが表示されるまでに 1 時間以上かかる場合があります。

>[!MORELIKETHIS]
>
>* [バルクシートファイルのダウンロードと作成](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
