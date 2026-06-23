---
title: 広告ネットワークデータの手動同期
description: サポートされている広告ネットワークに対して、キャンペーン構造とキャンペーンエンティティの同期を手動でトリガーする方法について説明します。
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/3X49sKMCu3P0X1CUUEpkmTXv4fdoeKk0sBAty5MBd8Y
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3111796b54e2e633ca734c7141efbc2d82f3087d
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 0%

---

# 広告ネットワークデータの手動同期

*[!DNL Google Ads]、[!DNL LY Ads] （旧称[!DNL Yahoo! Japan Ads]）、[!DNL Microsoft Advertising] （旧称[!DNL Bing Ads]）、[!DNL Yandex]、および既存の[!DNL Baidu] アカウントのみ*

同期とは、[ サポートされている広告ネットワーク ](/help/search-social-commerce/introduction/supported-inventory.md)上の各広告主の接続された広告ネットワークアカウントに関する更新情報をSearch, Social, &amp; Commerceが収集するプロセスです。 このデータには、広告主のキャンペーン構造とキャンペーンエンティティ（Search, Social, &amp; Commerceで管理または報告されているほとんどの属性を含む）が含まれます。 クリックデータは含まれず、Search, Social, &amp; Commerceの外部に入力された入札額や入札修飾子も含まれません。

Search, Social, &amp; Commerceは、広告ネットワークのアカウントと毎日のように自動的に同期します。また、広告ネットワークの1つで新しいキャンペーンが検出されるたびに同期します。 さらに、検索、ソーシャル、Commerce内から作成されたキャンペーンデータへのあらゆる変更が、広告ネットワークにすぐに送信されます。

指定したアカウントまたは特定のアクティブおよび一時停止したキャンペーンのすべてのアクティブおよび一時停止キャンペーンの同期を手動でリクエストできます。 このタスクは、広告ネットワーク上の新しいエンティティまたは変更されたエンティティを収集します。

「[!UICONTROL Auto Upload]」オプションを持つキャンペーンの場合、同期操作は、トラッキングテンプレートまたは宛先URLに欠落している、または変更する必要があるトラッキングコードを生成して投稿します。 URLは、アカウント設定またはキャンペーンのトラッキング設定のパラメーターに従って生成されます。 関連するアイテムにトラッキング URLが存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードマッチタイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）。

>[!NOTE]
>
>[ バルクシートを作成するときはいつでも](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)、オプションでバルクシートを作成する前に広告ネットワークと同期できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]>[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Accounts]**&#x200B;を選択して特定のアカウントのすべてのキャンペーンを同期するか、**[!UICONTROL Campaigns]**&#x200B;を選択して特定のキャンペーンを同期します。

1. （オプション）リストをフィルタリングして、特定のアカウントまたはキャンペーンを含めます。

1. 同期する各アカウントまたはキャンペーンの横にあるチェックボックスをオンにします。 一度に最大50件のキャンペーンを同期できます。 一度に5つ以上のアカウントを同期すると、ジョブはそれぞれ最大5つのアカウントのバッチに分割されます。

1. ツールバーの&#x200B;![**詳細**](/help/search-social-commerce/assets/more.png "&#x200B;詳細")をクリックし、**[!UICONTROL Sync]**&#x200B;を選択します。

同期ジョブのステータスは、[!UICONTROL Workspace] ビューで確認できます。 その仕事はかかるかもしれない
1時間以上表示されます。

>[!MORELIKETHIS]
>
>* [ バルクシート ファイルのダウンロードと作成](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
