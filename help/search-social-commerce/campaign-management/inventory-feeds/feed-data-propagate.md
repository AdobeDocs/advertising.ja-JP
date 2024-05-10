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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] （削除アクションのみ）、 [!DNL Yandex] アカウントのみ*

広告ネットワーク固有のフィードテンプレートを作成してフィードファイルまたはを関連付けた後 [!DNL Google] または [!DNL Microsoft] merchant center アカウントを使用すると、に従ってテンプレートを通じてフィードデータを伝播させることで、広告を動的に作成できます [フィードデータ設定](feed-settings-manage.md). 伝達中、テンプレートが特に指定しない限り、テンプレートの列名はフィードのデータ値に置き換えられ、生成されたキャンペーンとそのコンポーネントにはデフォルト設定が使用されます。 テンプレートオプションに応じて、検索、ソーシャル、Commerceで、広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成するか、広告を既存のアカウント構造にマッピングします。

新しいフィードデータに項目の新しいデータ値が含まれている場合、またはテンプレートが変更された場合、既存の広告は削除され、新しい広告が作成されます。 唯一の変更が以下の指定である場合 [!DNL Google Ads] パラメーター 1 とパラメーター 2 を選択すると、これらの値のみが更新されます。 重複した広告（同じ広告コピーとランディングページ）は作成されません。

データを伝達する際は、オプションで、生成されたデータをキャンペーン階層ビューでプレビューしたり、レビュー用にバルクシートファイルを生成したり、広告ネットワークにすぐに投稿できるようにバルクシートファイルを生成したりできます。 各伝播処理が完了すると、伝播の要約が「伝播」タブに追加され、伝播に基づいて作成、一時停止または削除された各エンティティ・タイプの数が示されます。 データをすぐに投稿しない場合は、データをプレビューして後で投稿できます。

## からフィードファイルを伝達 [!UICONTROL Templates] タブ

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

1. 伝達するテンプレートの横にあるチェックボックスをオンにします。

1. ツールバーで、 **[!UICONTROL Propagate]**&#x200B;を選択し、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** で伝播されたデータを表示するには、次の手順に従います [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ。 後で任意のコンポーネントとそのサブコンポーネントのデータを、 [!UICONTROL Templates] タブ。

   * **[!UICONTROL Propagate and Preview]:** バルクシート ファイル（「」という名前）を作成するには`<feed file name>_<template name>`&quot;）に作成する必要があります。このファイルは、 [!UICONTROL Bulksheets] レビュー用に表示（ただし [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ）。 後で、からバルクシートファイルを投稿できます。 [!UICONTROL Bulksheets] 表示。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。 投稿するためにファイルを展開する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:** バルクシート ファイル（「」という名前）を作成するには`<feed file name>_<template name>`&quot;）に設定した場合は、広告ネットワークへの投稿のために直ちにキューに入れられます。 バルクシートファイルは、次の場所で使用できます [!UICONTROL Bulksheets] 表示されますが、では利用できません [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。

   「前回の小道具。 「ステータス」列には、該当するテンプレートのジョブステータスが表示されます。

   各伝播処理が完了すると、伝播要約が [!UICONTROL Propagations] タブ。伝播に基づいて作成、一時停止または削除された、または予定の各エンティティ・タイプの数を示します。 この見積もりには、広告ネットワーク独自の広告エディター内で行われた変更は含まれていません。

## からフィードファイルを伝達 [!UICONTROL Feeds] list

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データ テーブルの上にあるツールバーで、 **[!UICONTROL Feeds]**.

1. フィードファイルの横にあるチェックボックスをオンにします。

1. データ テーブルの上で、 **[!UICONTROL Propagate/Post Feed Data]**&#x200B;を選択し、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** で伝播されたデータを表示するには、次の手順に従います [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ。 後で任意のコンポーネントとそのサブコンポーネントのデータを、 [!UICONTROL Templates] タブ。

   * **[!UICONTROL Propagate and Preview]:** バルクシート ファイル（「」という名前）を作成するには`<feed file name>_<template name>`&quot;）に作成する必要があります。このファイルは、 [!UICONTROL Bulksheets] レビュー用に表示（ただし [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ）。 後で、からバルクシートファイルを投稿できます。 [!UICONTROL Bulksheets] 表示。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。 投稿するためにファイルを展開する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:** バルクシート ファイル（「」という名前）を作成するには`<feed file name>_<template name>`&quot;）に設定した場合は、広告ネットワークへの投稿のために直ちにキューに入れられます。 バルクシートファイルは、次の場所で使用できます [!UICONTROL Bulksheets] 表示されますが、では利用できません [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ。

     作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。

1. ポップアップウィンドウで、フィードファイルからデータを伝達する各テンプレートの横にあるチェックボックスをオンにして、をクリックします **[!UICONTROL Propagate Feed]**.

   ファイルに関連付けられているすべてのテンプレートが一覧表示されます。

この [!UICONTROL Templates] タブが開き、「[!UICONTROL Last Prop. Status]「列には、該当するテンプレートのジョブステータスが表示されます。

各伝播処理が完了すると、伝播要約が [!UICONTROL Propagations] タブ。伝播に基づいて作成、一時停止または削除された、または予定の各エンティティ・タイプの数を示します。 この見積もりには、広告ネットワーク独自の広告エディター内で行われた変更は含まれていません。

## 伝播の要約の表示

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 「」をクリックします **[!UICONTROL Propagations]** タブ。

1. テンプレート名の横にある ![設定を表示/編集アイコン](/help/search-social-commerce/assets/settings.png "設定を表示/編集アイコン") .

## 伝播ジョブの停止

ジョブがまだキューに入っている間に、インベントリ フィード データの伝達ジョブを停止できます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

1. が「[!UICONTROL Last Prop. Status]テンプレート名の横にある「列」をクリックし、 **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [在庫フィードの広告テンプレートの管理](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから生成されたデータを編集](propagated-data-edit.md)
>* [フィードから広告ネットワークにキャンペーン データを投稿](propagated-data-post.md)
>* [在庫フィード データの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)
