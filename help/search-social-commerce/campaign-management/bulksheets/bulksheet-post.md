---
title: バルクシートの投稿または修正されたエラーファイル
description: 広告ネットワークにバルクシートファイルを投稿する方法を説明します。
exl-id: 8d530c30-3080-45cd-aead-7583b0824111
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# バルクシートの投稿または修正されたエラーファイル

既存のバルクシートファイルを投稿したり、修正されたエラーファイルを関連するアカウントに投稿できます。 [サポートされる広告ネットワーク](bulksheet-about.md#bulksheet-functionality-by-network). ファイルが ZIP 形式の場合は、最初に解凍する必要はありません。

バルクシートファイルとエラーファイルは、アップロードまたは生成後 30 日後に自動的に削除されます。

>[!NOTE]
>また、バルクシートファイルをアップロードする際に、エラーファイルを投稿することもできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. 投稿する各ファイルの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Post]**.

1. ダイアログボックスで、 [[!UICONTROL Post Bulksheet] 設定](#bulksheet-post-settings)をクリックし、 **[!UICONTROL Post]**.

   同じ設定が、投稿するすべてのファイルに適用されます。

タスクが開始されると、行のステータスと予定投稿日が [!UICONTROL Bulksheets] 表示。 ファイルが投稿されると、そのファイルへのリンクを含む電子メール通知が送信されます。 コンパイルされたデータの量に応じて、電子メール通知には数分以上かかる場合があります。 ただし、データを投稿できない場合は、 [!UICONTROL Bulksheets] 表示すると、エラーファイルへのリンクが記載された電子メール通知が送信されます。

>[!NOTE]
>
>* 大量のデータの投稿には時間がかかります。 ファイルの進行状況に従うには、 [!UICONTROL Progress] 列の [!UICONTROL Bulksheets] 表示。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの影響を受けます。
* バルクシートファイルを投稿する前に、投稿をキャンセルできます。

## バルクシートの POST 設定と修正されたエラーファイル {#bulksheet-post-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL Account (Search Engine)] | データが投稿される広告ネットワークアカウント。 複数のファイルを同時に投稿する場合、または複数のアカウントに適用される 1 つのファイルを投稿する場合、値は <i>複数のアカウントが選択されました</i>.<br><br>広告ネットワーク名の最初の文字は、アカウント名の後の括弧内にあります ( 例： [!DNL Google Ads] アカウント )。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを投稿するタイミング：<ul><li><i>[!UICONTROL Post to ad network now]</i> （デフォルト）：データの投稿を直ちに開始します。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> 指定した日時にデータの投稿を開始します。デフォルトは明日の 02:00（午前 2 時）です。 日付を変更するには、DD/MM/YYYY または D/M/YYYY の形式で日付を入力するか、 ![カレンダー](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "カレンダー") カレンダーを開き、 [日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 時間を変更するには、HH/MM または H/M の形式で時間を入力するか、（15 分間隔で）リストから時間を選択します。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを使用するアカウントに（適用可能な広告ネットワークに対して）トラッキングテンプレートとランディングページのサフィックスを含めるか、すべてのキーワード、広告、プレースメント、サイトリンク、 [!DNL Google Ads] 掲示中の製品グループ： <i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>. 入札単位がポートフォリオに含まれているかどうかは関係ありません。<br><br>次を選択した場合、 <i>[!UICONTROL Yes]</i>を指定した場合、 [!UICONTROL Tracking Methods] 」セクションに追加します。 デフォルトでは、トラッキング URL が存在する場合、新しい URL が必要な場合（キーワードの一致タイプ、広告テキスト、関連するアカウントのトラッキングパラメーターが変更された場合など）を除き、再生成されません。<br><br>次を選択した場合、 <i>[!UICONTROL No]</i>その場合でも、アップロードしたファイルを手動で投稿することで、後でトラッキング URL を生成できます。<br><br><b>注意：</b> 広告主がAdobe Advertisingコンバージョントラッキングを使用し、ベース URL が変更された場合、トラッキング URL を自動的に生成してアップロードするようにアカウントが設定されていない限り、新しいトラッキング URL を生成する必要があります。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータに基づいて最適化されたポートフォリオのキャンペーンに予算の変更を許可します。 デフォルトでは、このオプションは選択されていません。 このオプションを選択した場合、指定したキャンペーン予算の変更は、最適化機能が予算を（通常は次の入札サイクルで）再割り当てする必要があると判断するまで、適用されます。<br><br><b>注意：</b> 最適化されていないポートフォリオのキャンペーンの転記済データに起因する予算の変更は、ファイルの転記時に発生します。 変更は翌日にキャンペーン管理ビューに表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれるキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日まで、バルクシート内のデータに基づいて入札の変更を許可します。 このオプションを選択した場合は、「 **[!UICONTROL Hold bulksheet bids until]** フィールドに入力します。 |

>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [バルクシートファイルをダウンロード/作成する](bulksheet-download.md)
>* [バルクシートまたは修正済みエラーファイルのアップロード](bulksheet-upload.md)
>* [バルクシートファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシートファイルのエクスポート](bulksheet-export.md)
