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

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （旧称 [!DNL Bing Ads]）、[!DNL Yahoo! Japan Ads]、[!DNL Yandex] および既存の [!DNL Baidu] アカウントのみ*

同期とは、検索、ソーシャル、Commerceが、[ サポートされている広告ネットワーク ](/help/search-social-commerce/introduction/supported-inventory.md) 上で接続されている各広告主の広告ネットワークアカウントに関する更新情報を収集するプロセスです。 このデータには、広告主のキャンペーン構造とキャンペーンエンティティが含まれ、検索、ソーシャル、Commerceで管理またはレポートされる属性のほとんどが含まれます。 クリックデータや、検索、ソーシャル、Commerceの外部で入力された入札および入札修飾子は含まれません。これらは個別に収集されます。

検索、ソーシャル、Commerceは、1 日に 1 回、および広告ネットワークの 1 つに新しいキャンペーンが検出されるたびに、広告ネットワークアカウントと自動的に同期（同期）します。 さらに、検索、ソーシャル、Commerce内で作成されたキャンペーンデータに対するすべての変更を、即座に広告ネットワークに送信します。

指定したアカウントまたは特定のアクティブなキャンペーンと一時停止されたキャンペーンにある、アクティブなキャンペーンと一時停止されたキャンペーンすべての同期を手動でリクエストできます。 このタスクは、広告ネットワーク上の新しいエンティティまたは変更されたエンティティを収集します。

「[!UICONTROL Auto Upload]」オプションを使用するキャンペーンの場合、同期操作は、トラッキングテンプレートまたは宛先 URL にない、または変更する必要があるトラッキングコードを生成して投稿します。 URL は、アカウント設定またはキャンペーンのトラッキング設定のパラメーターに従って生成されます。 関連する項目のトラッキング URL が存在する場合、新しい URL が必要ない限り（キーワード一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。

>[!NOTE]
>
>[ バルクシートを作成 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) する際はいつでも、バルクシートを作成する前に広告ネットワークと同期できます。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、「**[!UICONTROL Accounts]**」を選択して特定のアカウントのすべてのキャンペーンを同期するか、「**[!UICONTROL Campaigns]**」を選択して特定のキャンペーンを同期します。

1. （任意）リストをフィルタリングして、特定のアカウントやキャンペーンを含めます。

1. 同期する各アカウントまたはキャンペーンの横にあるチェックボックスを選択します。 一度に 50 件までのキャンペーンを同期できます。 一度に 5 つを超えるアカウントを同期する場合、ジョブは最大 5 つのアカウントのバッチに分割されます。

1. ツールバーの **![その他")** をクリックし ](/help/search-social-commerce/assets/more.png "、**[!UICONTROL Sync]** を選択します。

同期ジョブのステータスは、[!UICONTROL Workspace] 表示で確認できます。 仕事にかかる時間は
1 時間以上表示される。

>[!MORELIKETHIS]
>
>* [ バルクシートファイルのダウンロード/作成 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
