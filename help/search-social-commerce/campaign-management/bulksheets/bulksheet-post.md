---
title: バルクシートの後またはエラーファイルの修正
description: バルクシート ファイルを広告ネットワークに投稿する方法について説明します。
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/N2xYU3CSbNaftsEOKKyXDjDQRYeqhYOolhf5ZyCPiGA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 0%

---

# バルクシートの後またはエラーファイルの修正

既存のバルクシートファイルまたは修正されたエラーファイルを、[&#x200B; サポートされている広告ネットワーク &#x200B;](bulksheet-about.md#bulksheet-functionality-by-network)の関連アカウントに投稿できます。 ファイルがZIP形式の場合は、最初に解凍する必要はありません。

バルクシートファイルとエラーファイルは、アップロードまたは生成されてから30日後に自動的に削除されます。

>[!NOTE]
>ファイルをアップロードする際に、バルクシート ファイルまたはエラーファイルを投稿することもできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. 投稿する各ファイルの横にあるチェックボックスをオンにします。

1. データテーブルの上のツールバーで、**[!UICONTROL Post]**&#x200B;をクリックします。

1. ダイアログボックスで、[[!UICONTROL Post Bulksheet]設定](#bulksheet-post-settings)に情報を入力または選択し、**[!UICONTROL Post]**&#x200B;をクリックします。

   同じ設定が、投稿するすべてのファイルに適用されます。

タスクが開始されると、行のステータスとスケジュールされた投稿日が[!UICONTROL Bulksheets] ビューで変更されます。 ファイルが投稿されると、ファイルへのリンクを含むメール通知が送信されます。 収集されたデータ量によっては、メール通知に数分以上かかる場合があります。 ただし、いずれかのデータを投稿できない場合は、エラーファイルが[!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 大量のデータを投稿するには時間がかかります。 ファイルの進行状況は、[!UICONTROL Progress] ビューの[!UICONTROL Bulksheets]列で確認できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの対象となります。
>* バルクシートファイルを投稿する前に、投稿をキャンセルできます。

## バルクシートと修正されたエラーファイルの投稿設定 {#bulksheet-post-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL Account (Search Engine)] | データが投稿される広告ネットワークアカウント。 複数のファイルを同時に投稿する場合、または複数のアカウントに適用される1つのファイルを投稿する場合、値は<i>複数のアカウントが選択されています</i>。<br><br>広告ネットワーク名の最初の文字は、アカウント名の後に括弧で囲まれます（[!DNL Google Ads] アカウントの「Acme Realty （G）」など）。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを投稿する場合：<ul><li><i>[!UICONTROL Post to ad network now]</i> （既定値）: データの投稿をすぐに開始します。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i>指定された日時にデータの投稿を開始します。デフォルトは明日の02:00 （午前2時）です。 日付を変更するには、日付をDD/MM/YYYYまたはD/M/YYYY形式で入力するか、![&#x200B; カレンダー](/help/search-social-commerce/assets/calendar.png " カレンダー")をクリックしてカレンダーを開き、[日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)します。 時間を変更するには、HH/MMまたはH/M形式で時間を入力するか、リストから時間（15分間隔）を選択します。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを含むアカウントにトラッキングテンプレートとランディングページのサフィックス（該当する広告ネットワークの場合）を含めるか、宛先URLを含むアカウントにトラッキングコードを埋め込む宛先URLを含めるか、投稿のすべてのキーワード、広告、プレースメント、サイトリンク、および[!DNL Google Ads]製品グループについて、<i>[!UICONTROL Yes]</i> （デフォルト）または<i>[!UICONTROL No]</i>です。 入札単位がポートフォリオにあるかどうかは関係ありません。<br><br> 「<i>[!UICONTROL Yes]</i>」を選択すると、関連するアカウント設定またはキャンペーン設定の「[!UICONTROL Tracking Methods]」セクションのパラメーターに従ってURLが生成されます。 デフォルトでは、トラッキング URLが存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードマッチタイプ、広告テキスト、関連アカウントのトラッキングパラメーターが変更された場合など）。<br><br> 「<i>[!UICONTROL No]</i>」を選択した場合でも、アップロードしたファイルを手動で投稿することで、後でトラッキング URLを生成できます。<br><br><b>注：</b>広告主がAdobe Advertising コンバージョントラッキングを使用しており、ベース URLが変更された場合、トラッキング URLを自動生成してアップロードするようにアカウントが設定されていない限り、新しいトラッキング URLを生成する必要があります。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータにもとづいて、最適化されたポートフォリオでキャンペーンの予算を変更できます。 デフォルトでは、このオプションは選択されていません。 このオプションを選択すると、最適化機能で予算を再配分する必要があると判断されるまで、指定したキャンペーン予算の変更が適用されます（通常は次の入札サイクルで）。<br><br><b> メモ：</b>最適化されていないポートフォリオのキャンペーンに関する投稿データに起因する予算変更は、ファイルの投稿時に発生します。 変更は、翌日のキャンペーン管理ビューに表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれるキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日までバルクシートのデータに基づく入札変更を許可します。 このオプションを選択した場合は、**[!UICONTROL Hold bulksheet bids until]** フィールドに1 ～ 7日後の終了日を指定します。 |

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](bulksheet-download.md)
>* [&#x200B; バルクシートのアップロードまたはエラーファイルの修正](bulksheet-upload.md)
>* [&#x200B; バルクシート ファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシート ファイルを書き出す](bulksheet-export.md)
