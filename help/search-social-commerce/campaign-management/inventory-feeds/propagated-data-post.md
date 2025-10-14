---
title: フィードから広告ネットワークにキャンペーン データを投稿
description: 在庫データフィードから生成されたデータを広告ネットワークに投稿する方法を説明します。
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# フィードから広告ネットワークにキャンペーン データを投稿

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

フィードから生成されたキャンペーンデータを、関連するテンプレートを介してデータを伝播するとき、または別のプロセスとして投稿できます。 データを POST すると、既存の伝播されたデータが [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords] および [!UICONTROL Ads] の各リストから削除されます。

投稿が成功するには、すべての広告グループをキャンペーンに割り当て、すべてのキーワードと広告を広告グループに割り当てる必要があります。また、必要なすべての情報を長さ違反なく含める必要があります。

* オプションを「[!UICONTROL Propagate and Preview]」に使用した場合は、生成されたバルクシートファイル [&#128279;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) 「`<feed file name>_<template name>`」という名前）を [!UICONTROL Bulksheets] ビューから  投稿」します。

  以前に [&#x200B; ランディングページの検証 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) を行ったことがない場合は、ファイルを投稿する前に行うことができます。

* オプションを「[!UICONTROL Propagate only]」に使用した場合は、[[!UICONTROL New] ステータスのコンポーネントに対して生成されたデータを &#x200B;](propagated-data-status.md) 「[!UICONTROL Templates]」タブのキャンペーン階層ビュー内に投稿できます。

  >[!NOTE]
  >
  >アクティブまたは削除されたコンポーネントには、新規のサブコンポーネントが含まれる場合があり、データが有効な場合は、サブコンポーネントを投稿できます。

  >[!TIP]
  >
  >以前にランディングページを検証したことがなく、その検証を行う場合は、広告ネットワークに投稿する代わりに、[!UICONTROL Bulksheets] ビューから [&#x200B; データを反映してプレビュー &#x200B;](feed-data-propagate.md) します。 その後、手動でファイルを広告ネットワークに投稿する前に [&#128279;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)URL を検証  できます。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

   1. テンプレートの横にあるチェックボックスをオンにします。

   1. ツールバーの「**[!UICONTROL Post]**」をクリックします。

   1. 転記の設定で、フィールドに情報を入力または選択し、[**[!UICONTROL Post]**] をクリックします。

      * **[!UICONTROL Selection]:** 投稿されるアカウントのコンポーネント。

      * **[!UICONTROL Scheduling]:** ファイルをポストするタイミング：

         * *[!UICONTROL Post to search engine now]* （デフォルト）：伝達されたフィードデータからバルクシートファイルを作成し、すぐに投稿を開始します。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* バルクシート ファイルを作成し、後でポストします。 次の内容を指定します。

            * **[!UICONTROL Start Time]:** バルクシート ファイルが広告ネットワークに投稿される将来の日時。 デフォルトでは、ファイルは翌日の 00:00 （午前 12:00）に送信されます。 **メモ：** 処理に時間のかかる大きなファイルの場合、投稿されたデータはキャンペーン管理ビュー内またはネットワークの広告マネージャー内ですぐに使用することはできません。

            * **[!UICONTROL End Time]:** 「[!UICONTROL When the Scheduled End Date is reached]」の [&#x200B; フィードデータ設定 &#x200B;](feed-settings-manage.md#feed-data-settings) に基づいて、投稿された広告が一時停止または削除される将来の日時。 デフォルトでは、終了時刻は今日から 30 日後の 00:00 （午前 12:00）です。 データを無期限に（またはテンプレートに新しいデータが反映されるまで）アクティブのままにする場合は「**[!UICONTROL None]**」を選択し、日付と時刻を指定します。

              日付を指定するには、DD/MM/YYYY または D/M/YYYY の形式を使用するか、「![&#x200B; カレンダー &#x200B;](/help/search-social-commerce/assets/calendar.png " カレンダー ")」をクリックしてカレンダーを開き、[&#x200B; 日付を選択 &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md) します。 時間を変更するには、24 時間形式（HH/MM または H/M）で時間を入力するか、リストから時間（30 分間隔）を選択します。

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets] ビューで使用できるバルクシートファイルを作成します。 必要に応じて、ここからファイルを投稿できます。

           作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。 投稿するためにファイルを展開する必要はありません。

      * **[!UICONTROL Generate Tracking URLs]:** バルクシート ファイルにキーワードおよび広告バリエーションのトラッキング URL を含めるかどうか：*[!UICONTROL Yes]* （既定値）または *[!UICONTROL No]*。

        「*[!UICONTROL Yes]* [!UICONTROL Tracking Methods]」を選択すると、キーワードおよび広告のベース URL から生成される URL は、[&#x200B; アカウント設定 &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) または既存のキャンペーンにデータをマッピングしている場合は既存の [&#x200B; キャンペーン設定 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) の [!UICONTROL Tracking Methods] パラメーターに従います。

        関連する項目のトラッキング URL が存在する場合、新しい URL が必要ない限り（キーワード一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。

      * **[!UICONTROL Bulksheet Name]:** 伝達されたフィードデータから作成するバルクシートファイルの名前。 デフォルトでは、ファイルの名前は `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt` です。 ファイル名は任意に変更できますが、ファイル拡張子は `.tsv` （タブ区切り値の場合）、`.txt` （ASCII テキストの場合）、`.csv` （コンマ区切り値の場合）、`.zip` （圧縮 TSV ファイルの場合）のいずれかで終わる必要があります。 国際文字を含むデータの場合は、TSV または TXT 形式を使用します。

        投稿されたファイルは、広告ネットワークに投稿したかどうかに関係なく、[!UICONTROL Bulksheets] ビューで 30 日間利用できます。

「[!UICONTROL Last Prop. Status]」列には、該当するテンプレートのジョブステータスが表示されます。

バルクシートが作成されると、[!UICONTROL Bulksheets] ビューに表示されます。 ファイルが投稿されると、ファイルへのリンクを含むメール通知が送信されます。 ただし、データの全部または一部が投稿できない場合は、エラーファイルが [!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 選択したスケジュール オプションに関係なく、指定したデータは [[!UICONTROL Campaigns]]、[[!UICONTROL Ad Groups]]、[[!UICONTROL Keywords]]、および [[!UICONTROL Ads]] リストから削除されます。
>* 大量のデータを処理するには、より長い時間がかかります。 処理中にファイルの進行状況を追跡できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの対象となります。
>* バルクシート ファイルを投稿する前に、[&#x200B; 投稿をキャンセル &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md) できます。

>[!MORELIKETHIS]
>
>* [&#x200B; 在庫フィードについて &#x200B;](inventory-feeds-about.md)
>* [&#x200B; フィードから生成されたデータを表示 &#x200B;](propagated-data-view.md)
>* [&#x200B; フィードから生成されたデータを編集 &#x200B;](propagated-data-edit.md)
>* [&#x200B; 在庫フィード データの転記ジョブを停止 &#x200B;](stop-job.md)
>* [&#x200B; フィードから生成されたデータのステータス &#x200B;](propagated-data-status.md)
