---
title: バルクシートまたは修正されたエラーファイルの投稿
description: バルクシートファイルを広告ネットワークに投稿する方法を説明します。
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# バルクシートまたは修正されたエラーファイルの投稿

既存のバルクシートファイルまたは修正されたエラーファイルを、（サポートされている広告ネットワーク [ の関連アカウントに投稿でき ](bulksheet-about.md#bulksheet-functionality-by-network) す。 ファイルが ZIP 形式の場合は、最初に解凍する必要はありません。

バルクシートファイルとエラーファイルは、アップロードまたは生成されてから 30 日後に自動的に削除されます。

>[!NOTE]
>また、バルクシートファイルやエラーファイルをアップロード時に投稿することもできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Bulksheets]** をクリックします。

1. 投稿する各ファイルの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Post]**] をクリックします。

1. ダイアログ ボックスで、[[!UICONTROL Post Bulksheet] 設定の情報を入力または選択し ](#bulksheet-post-settings) [**[!UICONTROL Post]**] をクリックします。

   投稿するすべてのファイルに同じ設定が適用されます。

タスクが開始されると、その行のステータスとスケジュールされた転記日が [!UICONTROL Bulksheets] ビューで変更されます。 ファイルが投稿されると、ファイルへのリンクを含むメール通知が送信されます。 コンパイルされたデータの量に応じて、メール通知は数分以上かかる場合があります。 ただし、データを投稿できない場合は、エラーファイルが [!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 大量のデータがポストされるまでに時間がかかる。 [!UICONTROL Bulksheets] ビューの [!UICONTROL Progress] 列で、ファイルの進行状況を追跡できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの対象となります。
>* バルクシート ファイルを投稿する前に、投稿をキャンセルできます。

## バルクシートおよび修正されたエラーファイルの POST 設定 {#bulksheet-post-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL Account (Search Engine)] | データが投稿される広告ネットワークアカウント。 複数のファイルを同時に投稿する場合、または複数のアカウントに適用される 1 つのファイルを投稿する場合、値は <i> 複数のアカウントが選択されました </i> になります。<br><br> 広告ネットワーク名の最初の文字は、アカウント名の後の括弧内にあります（[!DNL Google Ads] アカウントの場合は「Acme Realty （G）」など）。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを POST するタイミング：<ul><li><i>[!UICONTROL Post to ad network now]</i> （デフォルト）：データの投稿を直ちに開始します。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> 指定した日時にデータの投稿を開始します。デフォルトは明日の午前 2 時です。 日付を変更するには、DD/MM/YYYY または D/M/YYYY の形式で日付を入力するか、「![ カレンダー ](/help/search-social-commerce/assets/calendar.png " カレンダー ")」をクリックしてカレンダーを開き、[ 日付を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md) します。 時間を変更するには、HH/MM または H/M の形式で時間を入力するか、リストから時間（15 分間隔）を選択します。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを使用するアカウントにトラッキングテンプレートおよびランディングページのサフィックス（該当する広告ネットワークの場合）を含めるか、宛先 URL を使用するアカウントにトラッキングコードが埋め込まれた宛先 URL を含めるか（すべてのキーワード、広告、プレースメント、サイトリンク、[!DNL Google Ads] 製品グループの場合）、<i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>。 入札単位がポートフォリオ内にあるかどうかは関係ありません。<br><br> 「<i>[!UICONTROL Yes]</i>」を選択すると、関連するアカウント設定またはキャンペーン設定の「[!UICONTROL Tracking Methods]」セクションのパラメーターに従って URL が生成されます。 デフォルトでは、トラッキング URL が存在する場合、新しい URL が必要でない限り（キーワード一致タイプ、広告テキスト、関連するアカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。<br><br> 「<i>[!UICONTROL No]</i>」を選択した場合でも、アップロードされたファイルを手動で投稿することで、後でトラッキング URL を生成できます。<br><br><b> メモ：</b> 広告主がAdobe Advertisingのコンバージョントラッキングを使用し、ベース URL が変更された場合、トラッキング URL を自動生成してアップロードするようにアカウントが設定されていない限り、新しいトラッキング URL を生成する必要があります。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータに基づいて、最適化されたポートフォリオのキャンペーンに対して予算を変更できます。 デフォルトでは、このオプションは選択されていません。 このオプションを選択した場合、最適化機能によって予算を再割り当てする必要があると判断されるまで（通常は次の入札サイクルで）、指定したキャンペーン予算の変更がすべて適用されます。<br><br><b> 注意：</b> 最適化されていないポートフォリオのキャンペーンの投稿データに起因する予算の変更は、ファイルの投稿時に発生します。 翌日、キャンペーン管理ビューに変更が表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれているキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日まで、バルクシートのデータに基づいた入札変更を許可します。 このオプションを選択した場合は、「終了日」フィールドに 1～7 日の間 **[!UICONTROL Hold bulksheet bids until]** 終了日を指定します。 |

>[!MORELIKETHIS]
>
>* [ バルクシートを使用した Campaign データの管理について ](bulksheet-about.md)
>* [ バルクシートファイルのダウンロード/作成 ](bulksheet-download.md)
>* [ バルクシートまたは修正されたエラーファイルのアップロード ](bulksheet-upload.md)
>* [ バルクシートファイル内のランディングページの検証 ](bulksheet-validate-landing-pages.md)
>* [ 生成またはアップロードされたバルクシートファイルのエクスポート ](bulksheet-export.md)
