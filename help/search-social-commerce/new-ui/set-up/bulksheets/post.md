---
title: （新しいUI）バルクシートの後またはエラーファイルの修正
description: 新しいSearch, Social, & Commerce UIで、バルクシートファイルを広告ネットワークに投稿する方法について説明します。
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# （新しいUI）バルクシートの後またはエラーファイルの修正

既存のバルクシートファイルまたは修正されたエラーファイルを、[&#x200B; サポートされている広告ネットワーク &#x200B;](about.md#bulksheet-functionality-by-network)の関連アカウントに投稿できます。 ファイルがZIP形式の場合は、最初に解凍する必要はありません。

バルクシートファイルとエラーファイルは、アップロードまたは生成されてから30日後に自動的に削除されます。

>[!NOTE]
>
>ファイルをアップロードする際に、バルクシート ファイルまたはエラーファイルを投稿することもできます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. 投稿する各ファイルの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Post]**&#x200B;をクリックします。

1. [[!UICONTROL Post Bulksheet]設定](#bulksheet-post-settings)で情報を入力または選択し、**[!UICONTROL Post]**&#x200B;をクリックします。

   同じ設定が、投稿するすべてのファイルに適用されます。

タスクが開始されると、行のステータスとスケジュールされた投稿日が[!UICONTROL Bulksheets] ビューで更新されます。 バルクシートのメール通知が[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/new-ui/notifications-manage.md)内で有効になっている場合、ファイルの投稿時に、ファイルへのリンクを含むメール通知が送信されます。 収集されたデータ量によっては、メール通知に数分以上かかる場合があります。 いずれかのデータを投稿できない場合は、エラーファイルが[!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>* 大量のデータを投稿するには時間がかかります。 ファイルの進行状況は、[!UICONTROL Bulksheets] ビューの[!UICONTROL Progress]列で確認できます。
>* 投稿されたすべてのデータは、ネットワークの編集プロセスの対象となります。
>* バルクシートファイルを投稿する前に、投稿をキャンセルできます。

## バルクシートと修正されたエラーファイルの投稿設定 {#bulksheet-post-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL Account (Search Engine)] | データが投稿される広告ネットワークアカウント。 複数のファイルを同時に投稿する場合、または複数のアカウントに適用される1つのファイルを投稿する場合、値は&#x200B;*Multiple Accounts Selected*&#x200B;です。<br><br>広告ネットワーク名の最初の文字は、アカウント名の後ろに括弧で囲まれます（[!DNL Google Ads] アカウントの「Acme Realty （G）」など）。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを投稿する場合：<ul><li>*[!UICONTROL Post to ad network now]* （既定値）: データの投稿をすぐに開始します。</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:*&#x200B;指定された日時にデータの投稿を開始します。デフォルトは明日の02:00 （午前2時）です。 日付を変更するには、DD/MM/YYYY形式で日付を入力するか、カレンダーアイコンをクリックしてカレンダーを開き、日付を選択します。 時間を変更するには、リストから時間（15分間隔）を選択します。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを含むアカウントにトラッキングテンプレートとランディングページのサフィックス（該当する広告ネットワークの場合）を含めるか、宛先URLを含むアカウントにトラッキングコードを埋め込む宛先URLを含めるか、投稿のすべてのキーワード、広告、プレースメント、サイトリンク、および[!DNL Google Ads]製品グループについて、*[!UICONTROL Yes]* （デフォルト）または&#x200B;*[!UICONTROL No]*&#x200B;です。 入札単位がポートフォリオにあるかどうかは関係ありません。<br><br> 「*[!UICONTROL Yes]*」を選択すると、関連するアカウント設定またはキャンペーン設定の「[!UICONTROL Tracking Methods]」セクションのパラメーターに従ってURLが生成されます。 デフォルトでは、トラッキング URLが存在する場合は、新しいURLが必要でない限り再生成されません（キーワードマッチタイプ、広告テキスト、関連アカウントのトラッキングパラメーターが変更された場合など）。<br><br> アップロードされたファイルを手動で投稿することで、後でトラッキング URLを生成できます。<br><br>**メモ：**&#x200B;広告主がAdobe Advertising コンバージョントラッキングを使用しており、ベース URLが変更されている場合は、アカウントが自動生成およびトラッキング URL アップロードをアップロード作成しない必要です。*[!UICONTROL No]* |
| [!UICONTROL Replace Media Optimizer Tracking] | （[!UICONTROL Generate Tracking URLs]が&#x200B;*[!UICONTROL Yes]*&#x200B;の場合に使用可能）アップロードされたファイルのURLにある既存のAdobe Advertising トラッキングを、新しく生成されたトラッキングに置き換えます。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータにもとづいて、最適化されたポートフォリオでキャンペーンの予算を変更できます。 デフォルトでは、このオプションは選択されていません。 このオプションを選択すると、最適化機能が（通常は次の入札サイクルで）予算を再割り当てする必要があると判断するまで、指定されたキャンペーン予算の変更が適用されます。<br><br>**注意：**&#x200B;最適化されていないポートフォリオのキャンペーンに関する投稿データから生じる予算変更は、ファイルの投稿時に発生します。 変更は、翌日のキャンペーン管理ビューに表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれるキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日までバルクシートのデータに基づく入札変更を許可します。 このオプションを選択した場合は、**[!UICONTROL Hold bulksheet bids until]** フィールドに1 ～ 7日後の終了日を指定します。 |

>[!MORELIKETHIS]
>
>* [&#x200B; （新しいUI）バルクシートを使用したキャンペーンデータの管理について](about.md)
>* [&#x200B; （新しいUI） バルクシート ファイルのダウンロードと作成](download.md)
>* [&#x200B; （新しいUI） バルクシートまたは修正されたエラーファイルをアップロード &#x200B;](upload.md)
>* [&#x200B; （新しいUI）バルクシート ファイルのランディングページを検証](validate-landing-pages.md)
>* [&#x200B; （新しいUI） アップロードされたバルクシートとエラーファイルを削除](delete.md)
