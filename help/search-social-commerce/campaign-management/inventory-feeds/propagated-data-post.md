---
title: フィードから広告ネットワークに生成されたキャンペーンデータを投稿します
description: 在庫データフィードから生成されたデータを広告ネットワークに投稿する方法を説明します。
exl-id: 14ce377c-9b71-48ac-8ead-cada9c06d52f
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# フィードから広告ネットワークに生成されたキャンペーンデータを投稿します

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

フィードから生成されたキャンペーンデータを、関連するテンプレートを通じて、または別のプロセスで、データを反映しながら投稿できます。 データを投稿すると、既存の反映済みデータが [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] リスト。

投稿を成功させるには、すべての広告グループをキャンペーンに割り当て、すべてのキーワードと広告を広告グループに割り当て、必要な情報をすべて長さ違反なしで含める必要があります。

* このオプションを[!UICONTROL Propagate and Preview],」、その後 [生成された bulksheet ファイルを投稿します。](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) ( 名前付き&quot;`<feed file name>_<template name>`」) を [!UICONTROL Bulksheets] 表示。

  以前に [ランディングページの検証](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)を含めない場合は、ファイルを投稿する前に設定できます。

* このオプションを[!UICONTROL Propagate only]」と表示された場合、 [[!UICONTROL New] ステータス](propagated-data-status.md) キャンペーン階層ビュー内で、 [!UICONTROL Templates] タブをクリックします。

  >[!NOTE]
  >
  >アクティブなコンポーネントまたは削除されたコンポーネントには、新規のサブコンポーネントが含まれる場合があります。データが有効な場合は、サブコンポーネントを投稿できます。

  >[!TIP]
  >
  >ランディングページを以前に検証していない場合は、 [データをプロパゲートし、プレビューします。](feed-data-propagate.md) から [!UICONTROL Bulksheets] 広告ネットワークに投稿する代わりに表示します。 次の操作が可能です。 [URL の検証](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) 広告ネットワークに手動でファイルを投稿する前に。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**（が開きます） [!UICONTROL Templates] タブをクリックします。

   1. テンプレートの横にあるチェックボックスをオンにします。

   1. ツールバーで、 **[!UICONTROL Post]**.

   1. 投稿設定で、フィールドに情報を入力または選択し、 **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** どのアカウントコンポーネントが転記されるか。

      * **[!UICONTROL Scheduling]:** ファイルを投稿するタイミング：

         * *[!UICONTROL Post to search engine now]* （デフォルト）：反映されたフィードデータからバルクシートファイルを作成し、直ちに投稿を開始します。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* バルクシートファイルを作成し、後で投稿します。 以下を指定します。

            * **[!UICONTROL Start Time]:** 広告ネットワークにバルクシートファイルが投稿される将来の日時。 デフォルトでは、ファイルは翌日の 0 時（午前 12 時）に送信されます。 **注意：** 処理時間を長くする必要がある大きなファイルの場合、投稿されたデータは、キャンペーン管理ビュー内、またはネットワークの広告マネージャー内ですぐには使用できません。

            * **[!UICONTROL End Time]:** 投稿された広告が、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings) &quot;の[!UICONTROL When the Scheduled End Date is reached].&quot; デフォルトでは、終了時間は、今日から 30 日間、00:00（午前 12:00）です。 選択 **[!UICONTROL None]** 無期限に（またはテンプレートに新しいデータが反映されるまで）データをアクティブに保つ場合は、日時を指定します。

              日付を指定するには、DD/MM/YYYY または D/M/YYYY の形式を使用するか、 [カレンダー](/help/search-social-commerce/assets/calendar.png "カレンダー") カレンダーを開き、 [日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 時刻を変更するには、24 時間形式（HH/MM または H/M）で時刻を入力するか、リストから時刻を（30 分間隔で）選択します。

         * *[!UICONTROL Preview in Bulksheet Management Area only, post later]:**から使用可能なバルクシートファイルを作成します。 [!UICONTROL Search] > [!UICONTROL Bulksheets] 表示。 必要に応じて、そこからファイルを投稿できます。

           生成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式になります。 ファイルを解凍して投稿する必要はありません。

      * **[!UICONTROL Generate Tracking URLs]:** bulksheet ファイルでキーワードおよび広告バリエーションのトラッキング URL を含めるかどうかを指定します。 *[!UICONTROL Yes]* （デフォルト）または *[!UICONTROL No]*.

        次を選択した場合、 *[!UICONTROL Yes]*&#x200B;に設定されている場合、URL は、 [!UICONTROL Tracking Methods] パラメーターを [アカウント設定](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) データを既存のキャンペーンにマッピングしている場合は、 [!UICONTROL Tracking Methods] 既存のパラメーター [キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        関連する項目のトラッキング URL が存在する場合、キーワードの一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など、新しい URL が必要な場合は再生成されません。

      * **[!UICONTROL Bulksheet Name]:** 伝播されたフィードデータから作成するバルクシートファイルの名前。 デフォルトでは、ファイルの名前はです。 `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. ファイルの名前は自由に変更できますが、ファイルの拡張子は次のいずれかにする必要があります。 `.tsv` （タブ区切り値の場合）、 `.txt` （ASCII テキストの場合）、 `.csv` （コンマ区切り値の場合）または `.zip` （圧縮 TSV ファイルの場合）。 国際文字を含むデータの場合は、TSV または TXT 形式を使用します。

        投稿されたファイルは、 [!UICONTROL Bulksheets] 広告ネットワークに投稿するかどうかを 30 日間表示します。

「[!UICONTROL Last Prop. Status]」列には、該当するテンプレートのジョブステータスが表示されます。

バルクシートを作成すると、 [!UICONTROL Bulksheets] 表示。 ファイルが投稿されると、そのファイルへのリンクを含む電子メール通知が送信されます。 ただし、データの一部または全部を投稿できない場合は、 [!UICONTROL Bulksheets] 表示すると、エラーファイルへのリンクが記載された電子メール通知が送信されます。

>[!NOTE]
>
>* 選択したスケジュールオプションに関係なく、指定したデータは [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] リスト。
>* 大量のデータの処理に時間がかかります。 処理中に、ファイルの進行状況を確認できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの影響を受けます。
>* バルクシートファイルを投稿する前に、 [投稿をキャンセル](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから生成されたデータを編集](propagated-data-edit.md)
>* [在庫フィードデータの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)
