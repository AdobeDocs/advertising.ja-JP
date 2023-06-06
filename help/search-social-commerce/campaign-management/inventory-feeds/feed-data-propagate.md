---
title: テンプレートを使用して在庫フィードデータを伝達
description: アカウント構造を管理し、動的な広告を配信するために、広告テンプレートを通じて在庫フィードからデータを伝播する方法について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# テンプレートを使用して在庫フィードデータを伝達

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

広告ネットワーク固有のフィードテンプレートを作成し、フィードファイルまたは [!DNL Google] または [!DNL Microsoft®] merchant center アカウントを使用し、 [フィードデータ設定](feed-settings-manage.md). 伝播中に、テンプレート内の列名がフィード内のデータ値に置き換えられ、生成されたキャンペーンとそのコンポーネントには、テンプレートで別途指定されていない限り、デフォルト設定が適用されます。 検索、ソーシャル、コマースは、テンプレートオプションに応じて、広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成するか、広告を既存のアカウント構造にマッピングします。

新しいフィードデータに項目の新しいデータ値が含まれる場合、またはテンプレートが変更されると、既存の広告は削除され、新しい広告が作成されます。 変更が [!DNL Google Ads] Param 1 と Param 2 の場合、これらの値のみが更新されます。 重複した広告（同じ広告コピーとランディングページ）は作成されません。

データを伝播する際に、オプションでキャンペーン階層ビュー内で生成されたデータをプレビューしたり、レビュー用のバルクシートファイルを生成したり、広告ネットワークに即座に投稿するためのバルクシートファイルを生成したりできます。 各伝播アクションが完了すると、伝播の要約が「伝播」タブに追加され、伝播に基づいて作成、一時停止または削除された各エンティティ・タイプの数が示されます。 すぐにデータを投稿しない場合は、プレビューして後で投稿できます。

## フィードファイルを [!UICONTROL Templates] タブ

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;は、 [!UICONTROL Templates] タブをクリックします。

1. 伝播するテンプレートの横にあるチェックボックスを選択します。

1. ツールバーで、 **[!UICONTROL Propagate]**&#x200B;をクリックし、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** 伝播されたデータを [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ 後から [!UICONTROL Templates] タブをクリックします。

   * **[!UICONTROL Propagate and Preview]:** バルクシートファイル (「`<feed file name>_<template name>`&quot;) で、 [!UICONTROL Bulksheets] レビュー用に表示 ( ただし、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] 」タブ ) を参照してください。 後で、 [!UICONTROL Bulksheets] 表示

      生成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式になります。 ファイルを解凍して投稿する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:** バルクシートファイル (「`<feed file name>_<template name>`&quot;) 広告ネットワークへの投稿用のキューに入れられます。 bulksheet ファイルは [!UICONTROL Bulksheets] ビューには表示されますが、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ

      生成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式になります。
   「最後の prop。 「ステータス」列には、該当するテンプレートのジョブステータスが表示されます。

   各伝播アクションが完了すると、伝播の要約が [!UICONTROL Propagations] タブに表示され、伝播に基づいて作成、一時停止または削除された各エンティティタイプの数を示します。 この推定には、広告ネットワーク独自の広告エディター内でおこなわれた変更は含まれません。

## フィードファイルを [!UICONTROL Feeds] リスト

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Feeds]**.

1. フィードファイルの横にあるチェックボックスを選択します。

1. データテーブルの上にある **[!UICONTROL Propagate/Post Feed Data]**&#x200B;をクリックし、次のいずれかのオプションを選択します。

   * **[!UICONTROL Propagate Only]:** 伝播されたデータを [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ 後から [!UICONTROL Templates] タブをクリックします。

   * **[!UICONTROL Propagate and Preview]:** バルクシートファイル (「`<feed file name>_<template name>`&quot;) で、 [!UICONTROL Bulksheets] レビュー用に表示 ( ただし、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] 」タブ ) を参照してください。 後で、 [!UICONTROL Bulksheets] 表示

      生成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式になります。 ファイルを解凍して投稿する必要はありません。

   * **[!UICONTROL Propagate and Post to SE]:** バルクシートファイル (「`<feed file name>_<template name>`&quot;) 広告ネットワークへの投稿用のキューに入れられます。 bulksheet ファイルは [!UICONTROL Bulksheets] ビューには表示されますが、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ

      生成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式になります。

1. ポップアップウィンドウで、フィードファイルからのデータの伝達に使用する各テンプレートの横にあるチェックボックスを選択し、 **[!UICONTROL Propagate Feed]**.

   そのファイルに関連するすべてのテンプレートが表示されます。

この [!UICONTROL Templates] タブが開き、「[!UICONTROL Last Prop. Status]」列には、該当するテンプレートのジョブステータスが表示されます。

各伝播アクションが完了すると、伝播の要約が [!UICONTROL Propagations] タブに表示され、伝播に基づいて作成、一時停止または削除された各エンティティタイプの数を示します。 この推定には、広告ネットワーク独自の広告エディター内でおこなわれた変更は含まれません。

## 伝播の概要の表示

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 次をクリック： **[!UICONTROL Propagations]** タブをクリックします。

1. テンプレート名の横にある ![設定を表示/編集アイコン](/help/search-social-commerce/assets/settings.png "設定を表示/編集アイコン") .

## 伝播ジョブの停止

ジョブがキューに入れられている間に、在庫フィードデータの伝播ジョブを停止できます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;は、 [!UICONTROL Templates] タブをクリックします。

1. 「[!UICONTROL Last Prop. Status]&quot;テンプレート名の横の列で、 **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [在庫フィード用の広告テンプレートの管理](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから生成されたデータを編集](propagated-data-edit.md)
>* [フィードから広告ネットワークに生成されたキャンペーンデータを投稿](propagated-data-post.md)
>* [在庫フィードデータの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)

