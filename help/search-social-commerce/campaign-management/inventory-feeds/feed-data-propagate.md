---
title: テンプレートを通じて在庫フィード データを伝達する
description: 広告テンプレートを通じて在庫フィードからデータを伝播させ、アカウント構造を管理し、動的な広告を配信する方法について説明します。
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/2MCDHOgRqhAgwKuT-drdVZCHZJhSYxX3F3wLAVnpXT0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 876
ht-degree: 0%

---

# テンプレートを通じて在庫フィード データを伝達する

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除操作のみ）、[!DNL Yandex] アカウントのみ*

広告ネットワーク固有のフィード テンプレートを作成し、フィード ファイルまたは[!DNL Google]または[!DNL Microsoft]のマーチャント センターのアカウントを関連付けると、[&#x200B; フィード データ設定](feed-settings-manage.md)に従ってテンプレートを通じてフィード データを伝搬することにより、広告を動的に作成できます。 伝播中は、テンプレート内の列名がフィード内のデータ値に置き換えられ、テンプレートで特に指定されていない限り、生成されたキャンペーンとそのコンポーネントにはデフォルトの設定が適用されます。 Search, Social, &amp; Commerceでは、テンプレートオプションに応じて、広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成するか、広告を既存のアカウント構造にマッピングします。

新しいフィードデータに項目の新しいデータ値が含まれている場合、またはテンプレートが変更された場合、既存の広告は削除され、新しい広告が作成されます。 唯一の変更が[!DNL Google Ads] パラメーター1とパラメーター2の指定である場合、それらの値のみが更新されます。 重複した広告（同じ広告コピーとランディングページ）は作成されません。

データを伝播する場合は、オプションとして、キャンペーン階層ビュー内で生成されたデータをプレビューしたり、レビュー用のバルクシートファイルを生成したり、広告ネットワークに即座に投稿するためのバルクシートファイルを生成したりできます。 各伝播アクションが完了すると、「伝播」タブに伝播の要約が追加され、伝播に基づいて作成、一時停止、または削除された各エンティティタイプの数が示されます。 データをすぐに投稿しない場合は、プレビューして後で投稿できます。

## [!UICONTROL Templates] タブからフィード ファイルを伝達

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックすると、[!UICONTROL Templates] タブが開きます。

1. 適用するテンプレートの横にあるチェックボックスをオンにします。

1. ツールバーで「**[!UICONTROL Propagate]**」をクリックし、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads] タブに反映されたデータを表示します。 後で[!UICONTROL Templates] タブから、任意のコンポーネントとそのサブコンポーネントのデータを投稿できます。

   * **[!UICONTROL Propagate and Preview]:** バルクシート ファイル （「`<feed file name>_<template name>`」という名前）を作成します。このファイルは、[!UICONTROL Bulksheets] ビューでレビュー用に利用できます（[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads] タブでは利用できません）。 後で[!UICONTROL Bulksheets] ビューからバルクシート ファイルを投稿できます。

     結果のバルクシート ファイルが2 MBを超える場合、ファイルはZIP形式になります。 投稿するためにファイルを解凍する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:**&#x200B;広告ネットワークへの投稿のために直ちにキューに入れられるバルクシート ファイル （「`<feed file name>_<template name>`」という名前）を作成します。 バルクシートファイルは[!UICONTROL Bulksheets] ビューで利用できますが、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および[!UICONTROL Ads] タブでは利用できません。

     結果のバルクシート ファイルが2 MBを超える場合、ファイルはZIP形式になります。

   「最後の小道具」 「ステータス」列には、該当するテンプレートのジョブステータスが表示されます。

   各伝播アクションが完了すると、伝播の概要が[!UICONTROL Propagations] タブに追加され、伝播に基づいて作成、一時停止、または削除された各エンティティタイプの数が示されます。 この見積もりには、広告ネットワークの広告エディター内で行われた変更は含まれていません。

## [!UICONTROL Feeds] リストからフィード ファイルを反映

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Feeds]**&#x200B;をクリックします。

1. フィード ファイルの横にあるチェックボックスをオンにします。

1. データテーブルの上で、**[!UICONTROL Propagate/Post Feed Data]**&#x200B;をクリックし、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads] タブに反映されたデータを表示します。 後で[!UICONTROL Templates] タブから、任意のコンポーネントとそのサブコンポーネントのデータを投稿できます。

   * **[!UICONTROL Propagate and Preview]:** バルクシート ファイル （「`<feed file name>_<template name>`」という名前）を作成します。このファイルは、[!UICONTROL Bulksheets] ビューでレビュー用に利用できます（[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads] タブでは利用できません）。 後で[!UICONTROL Bulksheets] ビューからバルクシート ファイルを投稿できます。

     結果のバルクシート ファイルが2 MBを超える場合、ファイルはZIP形式になります。 投稿するためにファイルを解凍する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:**&#x200B;広告ネットワークへの投稿のために直ちにキューに入れられるバルクシート ファイル （「`<feed file name>_<template name>`」という名前）を作成します。 バルクシートファイルは[!UICONTROL Bulksheets] ビューで利用できますが、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および[!UICONTROL Ads] タブでは利用できません。

     結果のバルクシート ファイルが2 MBを超える場合、ファイルはZIP形式になります。

1. ポップアップウィンドウで、フィードファイルからデータを伝達する各テンプレートの横にあるチェックボックスを選択し、**[!UICONTROL Propagate Feed]**&#x200B;をクリックします。

   ファイルに関連付けられているすべてのテンプレートが一覧表示されます。

「[!UICONTROL Templates]」タブが開き、「[!UICONTROL Last Prop. Status]」列に該当するテンプレートのジョブステータスが表示されます。

各伝播アクションが完了すると、伝播の概要が[!UICONTROL Propagations] タブに追加され、伝播に基づいて作成、一時停止、または削除された各エンティティタイプの数が示されます。 この見積もりには、広告ネットワークの広告エディター内で行われた変更は含まれていません。

## 伝播の概要の表示

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックします。

1. 「**[!UICONTROL Propagations]**」タブをクリックします。

1. テンプレート名の横にある「![設定の表示/編集アイコン &#x200B;](/help/search-social-commerce/assets/settings.png "設定の表示/編集アイコン ")」をクリックします。

## 伝播ジョブの停止

ジョブがまだキューに入っている間に、在庫フィード データの伝搬ジョブを停止できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックすると、[!UICONTROL Templates] タブが開きます。

1. テンプレート名の横にある「[!UICONTROL Last Prop. Status]」列で、**[!UICONTROL Cancel]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [在庫フィードの広告テンプレートを管理](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [&#x200B; フィードから生成されたデータを表示](propagated-data-view.md)
>* [&#x200B; フィードから生成されたデータを編集](propagated-data-edit.md)
>* [&#x200B; フィードから生成されたキャンペーンデータを広告ネットワークに投稿](propagated-data-post.md)
>* [在庫フィード データの投稿ジョブを停止](stop-job.md)
>* フィードから生成されたデータの[&#x200B; ステータス &#x200B;](propagated-data-status.md)
