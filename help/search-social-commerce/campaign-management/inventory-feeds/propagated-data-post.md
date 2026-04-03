---
title: フィードから広告ネットワークに生成されたキャンペーンデータの投稿
description: 在庫データフィードから生成されたデータを広告ネットワークに投稿する方法について説明します。
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/TOTmjFuRPfH1vnyHwFvLBzlu7zBRQ3xHqKnG9TUC6IE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 846
ht-degree: 0%

---

# フィードから広告ネットワークに生成されたキャンペーンデータの投稿

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除操作のみ）、[!DNL Yandex] アカウントのみ*

フィードから生成されたキャンペーンデータを投稿するには、関連するテンプレートを通じて、または別のプロセスとしてデータを伝搬します。 データを投稿すると、既存の伝播されたデータが[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および[!UICONTROL Ads] リストから削除されます。

投稿を成功させるには、すべての広告グループをキャンペーンに割り当て、すべてのキーワードと広告を広告グループに割り当て、必要なすべての情報を長さ違反なしに含める必要があります。

* このオプションを「[!UICONTROL Propagate and Preview]」に使用した場合は、生成されたバルクシート ファイル [ （「](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md)」という名前）を`<feed file name>_<template name>` ビューから[!UICONTROL Bulksheets]投稿します。

  以前に[ ランディングページの検証](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)を行っていない場合は、ファイルを投稿する前に検証できます。

* このオプションを「[!UICONTROL Propagate only]」に使用した場合は、[[!UICONTROL New] タブからキャンペーン階層ビュー内で、](propagated-data-status.md) ステータス [!UICONTROL Templates]のコンポーネントに対して生成されたデータを投稿できます。

  >[!NOTE]
  >
  >アクティブまたは削除されたコンポーネントには、新しいサブコンポーネントが含まれている場合があり、データが有効な場合はサブコンポーネントを投稿できます。

  >[!TIP]
  >
  >以前にランディングページを検証しておらず、検証する場合は、広告ネットワークに投稿する代わりに、[ データを伝播して](feed-data-propagate.md) ビューから[!UICONTROL Bulksheets] プレビューします。 その後、ファイルを広告ネットワークに手動で投稿する前に、[URLを検証できます](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックすると、[!UICONTROL Templates] タブが開きます。

   1. テンプレートの横にあるチェックボックスをオンにします。

   1. ツールバーで、**[!UICONTROL Post]**&#x200B;をクリックします。

   1. 投稿設定で、フィールドに情報を入力または選択し、**[!UICONTROL Post]**&#x200B;をクリックします。

      * **[!UICONTROL Selection]:**&#x200B;どのアカウントコンポーネントが投稿されているか。

      * **[!UICONTROL Scheduling]:** ファイルを投稿するタイミング：

         * *[!UICONTROL Post to search engine now]* （既定値）：伝播されたフィード データから一括シート ファイルを作成し、すぐに投稿を開始します。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:*&#x200B;は、バルクシート ファイルを作成し、後で投稿します。 次の項目を指定します。

            * **[!UICONTROL Start Time]:** バルクシート ファイルを広告ネットワークに投稿する日時を指定します。 デフォルトでは、ファイルは翌日の00:00 （午前12:00）に送信されます。 **注意：**&#x200B;長い処理が必要な大きなファイルの場合、投稿されたデータは、キャンペーン管理ビュー内やネットワークの広告マネージャー内ですぐに利用できません。

            * **[!UICONTROL End Time]:** 「[」の](feed-settings-manage.md#feed-data-settings) フィード データ設定[!UICONTROL When the Scheduled End Date is reached]に基づいて、投稿された広告を一時停止または削除できる今後の日時。 デフォルトでは、終了時刻は今日から30日後の00:00 （午前12:00）です。 データを無期限に（またはテンプレート用に新しいデータを反映するまで）アクティブにするか、日時を指定するには、**[!UICONTROL None]**&#x200B;を選択します。

              日付を指定するには、DD/MM/YYYYまたはD/M/YYYY形式を使用するか、![ カレンダー](/help/search-social-commerce/assets/calendar.png " カレンダー")をクリックしてカレンダーを開き、[日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)します。 時間を変更するには、時間を24時間形式HH/MMまたはH/Mで入力するか、リストから時間（30分間隔）を選択します。

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:**&#x200B;は、[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets] ビューで使用できる一括シート ファイルを作成します。 オプションで、そこからファイルを投稿できます。

           結果のバルクシート ファイルが2 MBを超える場合、ファイルはZIP形式になります。 投稿するためにファイルを解凍する必要はありません。

      * **[!UICONTROL Generate Tracking URLs]:** キーワードおよび広告バリエーションのトラッキング URLをバルクシート ファイルに含めるかどうか：*[!UICONTROL Yes]* （デフォルト）または&#x200B;*[!UICONTROL No]*。

        *[!UICONTROL Yes]*&#x200B;を選択すると、URLは、[!UICONTROL Tracking Methods] アカウント設定[の](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) パラメーターに従ってキーワードと広告のベース URLから生成されます。また、データを既存のキャンペーンにマッピングしている場合は、既存の[!UICONTROL Tracking Methods] キャンペーン設定[の](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) パラメーターに生成されます。

        関連するアイテムにトラッキング URLが存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードマッチタイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）。

      * **[!UICONTROL Bulksheet Name]:**&#x200B;伝播されたフィード データから作成するバルクシート ファイルの名前。 デフォルトでは、ファイルの名前は`<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`です。 ファイルの名前は必要に応じて変更できますが、ファイルの拡張子は`.tsv` （タブ区切り値の場合）、`.txt` （ASCII テキストの場合）、`.csv` （コンマ区切り値の場合）、または`.zip` （圧縮TSV ファイルの場合）のいずれかである必要があります。 国際文字を含むデータの場合は、TSVまたはTXT形式を使用します。

        投稿されたファイルは、広告ネットワークに投稿するかどうかに関係なく、30日間、[!UICONTROL Bulksheets] ビューで利用できます。

「[!UICONTROL Last Prop. Status]」列には、該当するテンプレートのジョブステータスが表示されます。

バルクシートを作成すると、[!UICONTROL Bulksheets] ビューに表示されます。 ファイルが投稿されると、ファイルへのリンクを含むメール通知が送信されます。 ただし、データの全部または一部を投稿できない場合は、エラーファイルが[!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 選択したスケジュール設定オプションに関係なく、指定されたデータは[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、および[!UICONTROL Ads] リストから削除されます。
>* 大量のデータを処理するには時間がかかります。 プロセス中にファイルの進行状況を確認できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの対象となります。
>* バルクシート ファイルを投稿する前に、投稿を[ キャンセルできます](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md)。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [ フィードから生成されたデータを表示](propagated-data-view.md)
>* [ フィードから生成されたデータを編集](propagated-data-edit.md)
>* [在庫フィード データの投稿ジョブを停止](stop-job.md)
>* フィードから生成されたデータの[ ステータス ](propagated-data-status.md)
