---
title: フィードから広告ネットワークにキャンペーン データを投稿
description: 在庫データフィードから生成されたデータを広告ネットワークに投稿する方法を説明します。
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 2cf15dbab3dc00ec88a41e4f7d8b5b3646b843e8
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# フィードから広告ネットワークにキャンペーン データを投稿

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] （削除アクションのみ）、 [!DNL Yandex] アカウントのみ*

フィードから生成されたキャンペーンデータを、関連するテンプレートを介してデータを伝播するとき、または別のプロセスとして投稿できます。 データを POST すると、既存の伝播されたデータはすべて [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] リスト。

投稿が成功するには、すべての広告グループをキャンペーンに割り当て、すべてのキーワードと広告を広告グループに割り当てる必要があります。また、必要なすべての情報を長さ違反なく含める必要があります。

* オプションを使用して「[!UICONTROL Propagate and Preview],&quot; then [生成されたバルクシートファイルの投稿](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) （の名前は）`<feed file name>_<template name>```）から [!UICONTROL Bulksheets] 表示。

  以前に追加していない場合 [ランディングページの検証](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)ファイルを投稿する前に行うことができます。

* オプションを使用して「[!UICONTROL Propagate only]」に移動すると、コンポーネント用に生成されたデータを [[!UICONTROL New] ステータス](propagated-data-status.md) からのキャンペーン階層内の表示 [!UICONTROL Templates] タブ。

  >[!NOTE]
  >
  >アクティブまたは削除されたコンポーネントには、新規のサブコンポーネントが含まれる場合があり、データが有効な場合は、サブコンポーネントを投稿できます。

  >[!TIP]
  >
  >以前にランディングページを検証したことがない場合に検証するには、次の手順を実行します [データの伝播とプレビュー](feed-data-propagate.md) から [!UICONTROL Bulksheets] 広告ネットワークに投稿する代わりに表示します。 これにより、以下のことが可能になります [url を検証](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) 手動でファイルを広告ネットワークに投稿する前に。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

   1. テンプレートの横にあるチェックボックスをオンにします。

   1. ツールバーで、 **[!UICONTROL Post]**.

   1. 転記の設定で、フィールドに情報を入力または選択し、 **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** どのアカウントコンポーネントが投稿されるか。

      * **[!UICONTROL Scheduling]:** ファイルを投稿するタイミング：

         * *[!UICONTROL Post to search engine now]* （デフォルト）：伝達されたフィードデータからバルクシートファイルを作成し、すぐに投稿を開始します。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* バルクシート ファイルを作成し、後でポストします。 次の内容を指定します。

            * **[!UICONTROL Start Time]:** バルクシート ファイルが広告ネットワークに投稿される将来の日時。 デフォルトでは、ファイルは翌日の 00:00 （午前 12:00）に送信されます。 **注意：** 処理に時間のかかる大きなファイルの場合、投稿されたデータは、キャンペーン管理ビュー内またはネットワークの広告マネージャー内ではすぐに使用できません。

            * **[!UICONTROL End Time]:** 投稿された広告が一時停止または削除される可能性がある将来の日時。 [フィードデータ設定](feed-settings-manage.md#feed-data-settings) の場合[!UICONTROL When the Scheduled End Date is reached].」と入力します。 デフォルトでは、終了時刻は今日から 30 日後の 00:00 （午前 12:00）です。 を選択 **[!UICONTROL None]** データを無期限に（またはテンプレートに新しいデータが反映されるまで）アクティブのままにするか、日時を指定します。

              日付を指定するには、形式 DD/MM/YYYY または D/M/YYYY を使用するか、をクリックします ![カレンダー](/help/search-social-commerce/assets/calendar.png "カレンダー") カレンダーを開くには [日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 時間を変更するには、24 時間形式（HH/MM または H/M）で時間を入力するか、リストから時間（30 分間隔）を選択します。

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** から使用可能なバルクシートファイルを作成します [!UICONTROL Search] > [!UICONTROL Bulksheets] 表示。 必要に応じて、ここからファイルを投稿できます。

           作成されるバルクシートファイルが 2 MB を超える場合、ファイルは ZIP 形式です。 投稿するためにファイルを展開する必要はありません。

      * **[!UICONTROL Generate Tracking URLs]:** バルクシートファイルにキーワードおよび広告バリエーションのトラッキング URL を含めるかどうか： *[!UICONTROL Yes]* （デフォルト）または *[!UICONTROL No]*.

        を選択する場合 *[!UICONTROL Yes]*&#x200B;に続いて、以下に従ってキーワードおよび広告のベース URL から URL が生成されます。 [!UICONTROL Tracking Methods] のパラメーター [アカウント設定](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) または、データを既存のキャンペーンにマッピングしている場合は、 [!UICONTROL Tracking Methods] 既存ののパラメーター [キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        関連する項目のトラッキング URL が存在する場合、新しい URL が必要ない限り（キーワード一致タイプ、クリエイティブテキスト、アカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。

      * **[!UICONTROL Bulksheet Name]:** 伝達されたフィードデータから作成するバルクシートファイルの名前。 デフォルトでは、ファイルの名前はです `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. ファイル名は必要に応じて変更できますが、ファイル拡張子は次のいずれかにする必要があります。 `.tsv` （タブ区切り値の場合）、 `.txt` （ASCII テキストの場合） `.csv` （コンマ区切り値の場合）、 `.zip` （圧縮 TSV ファイル用）。 国際文字を含むデータの場合は、TSV または TXT 形式を使用します。

        投稿されたファイルは、 [!UICONTROL Bulksheets] 広告ネットワークに投稿したかどうかに関わらず、30 日間表示します。

「[!UICONTROL Last Prop. Status]「列には、該当するテンプレートのジョブステータスが表示されます。

バルクシートが作成されると、にリストされます。 [!UICONTROL Bulksheets] 表示。 ファイルが投稿されると、ファイルへのリンクを含むメール通知が送信されます。 ただし、データの全部または一部が投稿できない場合は、エラーファイルが [!UICONTROL Bulksheets] 表示すると、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 選択したスケジュールオプションに関係なく、指定したデータは [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] リスト。
>* 大量のデータを処理するには、より長い時間がかかります。 処理中にファイルの進行状況を追跡できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの対象となります。
>* バルクシート ファイルを投稿する前に、次の操作を行うことができます [転記のキャンセル](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから生成されたデータを編集](propagated-data-edit.md)
>* [在庫フィード データの転記ジョブを停止します](stop-job.md)
>* [フィードから生成されたデータのステータス](propagated-data-status.md)
