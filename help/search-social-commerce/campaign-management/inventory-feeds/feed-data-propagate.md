---
title: テンプレートを使用した在庫フィードデータの伝播
description: 広告テンプレートを通じてインベントリフィードからデータを伝播し、アカウント構造を管理して動的広告を配信する方法について説明します。
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# テンプレートを使用した在庫フィードデータの伝播

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

広告ネットワーク固有のフィードテンプレートを作成してフィードファイル、[!DNL Google] または [!DNL Microsoft] のマーチャントセンターアカウントを関連付けると、[ フィードデータ設定 ](feed-settings-manage.md) に従ってテンプレートを通じてフィードデータを伝播することで、広告を動的に作成できます。 伝達中、テンプレートが特に指定しない限り、テンプレートの列名はフィードのデータ値に置き換えられ、生成されたキャンペーンとそのコンポーネントにはデフォルト設定が使用されます。 テンプレートオプションに応じて、検索、ソーシャル、Commerceで、広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成するか、広告を既存のアカウント構造にマッピングします。

新しいフィードデータに項目の新しいデータ値が含まれている場合、またはテンプレートが変更された場合、既存の広告は削除され、新しい広告が作成されます。 パラメータ 1 とパラメータ 2[!DNL Google Ads] 指定だけが変更されている場合、これらの値だけが更新されます。 重複した広告（同じ広告コピーとランディングページ）は作成されません。

データを伝達する際は、オプションで、生成されたデータをキャンペーン階層ビューでプレビューしたり、レビュー用にバルクシートファイルを生成したり、広告ネットワークにすぐに投稿できるようにバルクシートファイルを生成したりできます。 各伝播処理が完了すると、伝播の要約が「伝播」タブに追加され、伝播に基づいて作成、一時停止または削除された各エンティティ・タイプの数が示されます。 データをすぐに投稿しない場合は、データをプレビューして後で投稿できます。

## 「[!UICONTROL Templates]」タブからのフィードファイルの伝達

1. メインメニューで、**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

1. 伝達するテンプレートの横にあるチェックボックスをオンにします。

1. ツールバーの「**[!UICONTROL Propagate]**」をクリックして、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および [!UICONTROL Ads] タブに反映されたデータを表示します。 後から「[!UICONTROL Templates]」タブから、任意のコンポーネントとそのサブコンポーネントのデータを投稿できます。

   * **[!UICONTROL Propagate and Preview]:** バルクシート ファイル（「`<feed file name>_<template name>`」という名前）を作成します。このファイルは、[!UICONTROL Bulksheets] ビューでレビューできます（[[!UICONTROL Campaigns]]、[[!UICONTROL Ad Groups]]、[[!UICONTROL Keywords]]、[[!UICONTROL Ads]] タブでは使用できません）。 後で [!UICONTROL Bulksheets] ビューからバルクシート ファイルをポストできます。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。 投稿するためにファイルを展開する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:** 広告ネットワークに投稿するために直ちにキューに入れられるバルクシート ファイル （「`<feed file name>_<template name>`」という名前）を作成します。 バルクシート ファイルは [!UICONTROL Bulksheets] ビューで使用できますが、[[!UICONTROL Campaigns]]、[[!UICONTROL Ad Groups]]、[[!UICONTROL Keywords]]、および [[!UICONTROL Ads]] タブでは使用できません。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。

   「前回の小道具。 「ステータス」列には、該当するテンプレートのジョブステータスが表示されます。

   各伝播処理が完了すると、伝播の要約が「[!UICONTROL Propagations]」タブに追加され、伝播に基づいて作成、一時停止または削除された各エンティティ・タイプの数が示されます。 この見積もりには、広告ネットワーク独自の広告エディター内で行われた変更は含まれていません。

## フ [!UICONTROL Feeds] ームリストからのフィードファイルの伝達

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Advanced (ACM)]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Feeds]**] をクリックします。

1. フィードファイルの横にあるチェックボックスをオンにします。

1. データ テーブルの上の [**[!UICONTROL Propagate/Post Feed Data]**] をクリックし、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および [!UICONTROL Ads] タブに反映されたデータを表示します。 後から「[!UICONTROL Templates]」タブから、任意のコンポーネントとそのサブコンポーネントのデータを投稿できます。

   * **[!UICONTROL Propagate and Preview]:** バルクシート ファイル（「`<feed file name>_<template name>`」という名前）を作成します。このファイルは、[!UICONTROL Bulksheets] ビューでレビューできます（[[!UICONTROL Campaigns]]、[[!UICONTROL Ad Groups]]、[[!UICONTROL Keywords]]、[[!UICONTROL Ads]] タブでは使用できません）。 後で [!UICONTROL Bulksheets] ビューからバルクシート ファイルをポストできます。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。 投稿するためにファイルを展開する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:** 広告ネットワークに投稿するために直ちにキューに入れられるバルクシート ファイル （「`<feed file name>_<template name>`」という名前）を作成します。 バルクシート ファイルは [!UICONTROL Bulksheets] ビューで使用できますが、[[!UICONTROL Campaigns]]、[[!UICONTROL Ad Groups]]、[[!UICONTROL Keywords]]、および [[!UICONTROL Ads]] タブでは使用できません。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。

1. ポップアップ ウィンドウで、フィード ファイルからデータを伝達する各テンプレートの横にあるチェック ボックスをオンにし、[**[!UICONTROL Propagate Feed]**] をクリックします。

   ファイルに関連付けられているすべてのテンプレートが一覧表示されます。

「[!UICONTROL Templates]」タブが開き、「[!UICONTROL Last Prop. Status]」列に該当するテンプレートのジョブステータスが表示されます。

各伝播処理が完了すると、伝播の要約が「[!UICONTROL Propagations]」タブに追加され、伝播に基づいて作成、一時停止または削除された各エンティティ・タイプの数が示されます。 この見積もりには、広告ネットワーク独自の広告エディター内で行われた変更は含まれていません。

## 伝播の要約の表示

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Advanced (ACM)]** をクリックします。

1. 「**[!UICONTROL Propagations]**」タブをクリックします。

1. テンプレート名の横にある ![ 設定を表示/編集アイコン ](/help/search-social-commerce/assets/settings.png " 設定を表示/編集アイコン ") をクリックします。

## 伝播ジョブの停止

ジョブがまだキューに入っている間に、インベントリ フィード データの伝達ジョブを停止できます。

1. メインメニューで、**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

1. テンプレート名の横にある「[!UICONTROL Last Prop. Status]」列で、「**[!UICONTROL Cancel]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 在庫フィードについて ](inventory-feeds-about.md)
>* [ 在庫フィードの広告テンプレートの管理 ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [ フィードから生成されたデータを表示 ](propagated-data-view.md)
>* [ フィードから生成されたデータを編集 ](propagated-data-edit.md)
>* [ フィードから広告ネットワークにキャンペーンデータを投稿する ](propagated-data-post.md)
>* [ 在庫フィード データの転記ジョブを停止 ](stop-job.md)
>* [ フィードから生成されたデータのステータス ](propagated-data-status.md)
