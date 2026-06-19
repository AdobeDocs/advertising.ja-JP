---
title: （新しいUI）広告ネットワークデータを手動で同期する
description: 新しいUIから、サポートされている広告ネットワークのキャンペーン構造とキャンペーンエンティティの同期を手動でトリガーする方法について説明します。
feature: Search Campaign Management
exl-id: 5e857713-53f0-4d90-8b7a-18a3675d320e
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# （新しいUI） API接続を介した広告ネットワークデータの手動同期

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads]、[!DNL LY Ads] （旧称[!DNL Yahoo! Japan Ads]）、[!DNL Microsoft Advertising] （旧称[!DNL Bing Ads]）、[!DNL Yandex]、および既存の[!DNL Baidu] アカウントのみ*

同期とは、[&#x200B; サポートされている広告ネットワーク &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)上の各広告主の接続された広告ネットワークアカウントに関する更新情報をSearch, Social, &amp; Commerceが収集するプロセスです。 このデータには、広告主のキャンペーン構造とキャンペーンエンティティ（Search, Social, &amp; Commerceで管理または報告されているほとんどの属性を含む）が含まれます。 クリックデータは含まれず、Search, Social, &amp; Commerceの外部に入力された入札額や入札修飾子も含まれません。

Search, Social, &amp; Commerceは、1日に1回、広告ネットワークのアカウントと自動的に同期します。また、広告ネットワークの1つで新しいキャンペーンが検出されるたびに同期します。 さらに、検索、ソーシャル、Commerce内から作成されたキャンペーンデータへのあらゆる変更が、広告ネットワークにすぐに送信されます。

指定したアカウント <!--Not available as of 2/23:  or in specific active and paused campaigns -->のすべてのアクティブなキャンペーンと一時停止したキャンペーンの同期を手動で要求できます。 このタスクは、広告ネットワーク上の新しいエンティティまたは変更されたエンティティを収集します。

「[!UICONTROL Auto Update]」オプションを持つキャンペーンの場合、同期操作は、トラッキングテンプレートまたは宛先URLに欠落している、または変更する必要があるトラッキングコードを生成して投稿します。 URLは、アカウント設定またはキャンペーンのトラッキング設定のパラメーターに従って生成されます。 関連するアイテムにトラッキング URLが存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードマッチタイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）。

>[!NOTE]
>
>[&#x200B; バルクシートを作成するときはいつでも](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)、オプションでバルクシートを作成する前に広告ネットワークと同期できます。

## 広告ネットワークアカウントでのキャンペーンの同期

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. アカウント名の横にあるチェックボックスをオンにします。

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. 一括操作ツールバーで、**[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**&#x200B;をクリックします。

   * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

同期ジョブのステータスは、[!UICONTROL Workspace] ビューで確認できます。 その仕事はかかるかもしれない
1時間以上表示されます。

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシート ファイルのダウンロードと作成](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
