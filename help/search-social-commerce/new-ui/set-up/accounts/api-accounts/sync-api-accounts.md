---
title: （新しい UI）広告ネットワークデータの手動同期
description: サポートされる広告ネットワークのキャンペーン構造とキャンペーンエンティティの同期を新しい UI から手動でトリガーする方法について説明します。
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# （新しい UI） API 接続を使用した、広告ネットワークデータの手動同期

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （旧称 [!DNL Bing Ads]）、[!DNL Yahoo! Japan Ads]、[!DNL Yandex] および既存の [!DNL Baidu] アカウントのみ*

同期とは、検索、ソーシャル、Commerceが、[ サポートされている広告ネットワーク ](/help/search-social-commerce/introduction/supported-inventory.md) 上で接続されている各広告主の広告ネットワークアカウントに関する更新情報を収集するプロセスです。 このデータには、広告主のキャンペーン構造とキャンペーンエンティティが含まれ、検索、ソーシャル、Commerceで管理またはレポートされる属性のほとんどが含まれます。 クリックデータや、検索、ソーシャル、Commerceの外部で入力された入札および入札修飾子は含まれません。これらは個別に収集されます。

検索、ソーシャル、Commerceは、1 日に 1 回、および広告ネットワークの 1 つに新しいキャンペーンが検出されるたびに、広告ネットワークアカウントと自動的に同期（同期）します。 さらに、検索、ソーシャル、Commerce内で作成されたキャンペーンデータに対するすべての変更を、即座に広告ネットワークに送信します。

指定したアカウント内のアクティブなキャンペーンと一時停止されたキャンペーンすべての同期を手動でリクエストできます <!--Not available as of 2/23:  or in specific active and paused campaigns --> このタスクは、広告ネットワーク上の新しいエンティティまたは変更されたエンティティを収集します。

「[!UICONTROL Auto Update]」オプションを使用するキャンペーンの場合、同期操作は、トラッキングテンプレートまたは宛先 URL にない、または変更する必要があるトラッキングコードを生成して投稿します。 URL は、アカウント設定またはキャンペーンのトラッキング設定のパラメーターに従って生成されます。 関連する項目のトラッキング URL が存在する場合、新しい URL が必要ない限り（キーワード一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。

>[!NOTE]
>
>[ バルクシートを作成 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) する際はいつでも、バルクシートを作成する前に広告ネットワークと同期できます。

## 広告ネットワークアカウントでキャンペーンを同期

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. アカウント名の横にあるチェックボックスをオンにします。

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. 一括アクションツールバーで、**[!UICONTROL ... More Actions]**/**[!UICONTROL Sync]** をクリックします。

   * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

同期ジョブのステータスは、[!UICONTROL Workspace] 表示で確認できます。 仕事にかかる時間は
1 時間以上表示される。

>[!MORELIKETHIS]
>
>* [ バルクシートファイルのダウンロード/作成 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
