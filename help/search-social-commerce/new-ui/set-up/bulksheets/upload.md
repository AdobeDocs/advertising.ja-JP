---
title: （新しいUI）バルクシートまたは修正されたエラーファイルのアップロード
description: 新しいSearch, Social, & Commerce UIで、バルクシートファイルまたは修正されたランディングページ検証エラーファイルを手動でアップロードする方法について説明します。
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
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# （新しいUI）バルクシートまたは修正されたエラーファイルのアップロード

[&#x200B; サポートされている広告ネットワーク &#x200B;](about.md#bulksheet-functionality-by-network)のバルクシート ファイル、修正されたランディングページ検証エラーファイル、およびその他の修正されたエラーファイルを、お使いのデバイスまたはネットワークからアップロードできます。 ファイルをアップロードすると、ファイル内のカスタム列はすべて削除されます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. ツールバーで、**[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**&#x200B;をクリックします。

1. [[!UICONTROL Upload Bulksheet]設定](#bulksheet-upload-settings)で情報を入力または選択します。

1. **[!UICONTROL Upload]**&#x200B;をクリックします。

タスクが開始されると、ファイルは[!UICONTROL Bulksheets] ビューに表示されます。 バルクシートのメール通知が[!UICONTROL Notification Center] [&#128279;](/help/search-social-commerce/new-ui/notifications/notification-manage.md)内で有効になっている場合、ジョブが完了すると、ファイルへのリンク付きのメール通知が送信されます。 収集されたデータ量によっては、メール通知に数分以上かかる場合があります。 ファイルの生成に失敗した場合、エラーファイルが[!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>バルクシート データを広告ネットワークに投稿すると、[!UICONTROL Bulksheets] ビューの[!UICONTROL Progress]列でファイルの進行状況を確認できます。 大量のデータを投稿するには時間がかかります。

## バルクシートと修正されたエラーファイルの設定をアップロードする {#bulksheet-upload-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL File to Upload] | アップロードするファイル。 デバイスまたはネットワーク上のファイルを見つけるには、**[!UICONTROL Choose File]**&#x200B;をクリックしてファイルを指定します。<br><br> バルクシートファイルは、最大2.5 GB （約250万行）までで、次のいずれかのファイル拡張子を持つ必要があります：*[!UICONTROL .tsv]* （タブ区切り値の場合）、*[!UICONTROL .txt]* （Unicode準拠のASCII テキストの場合）、*[!UICONTROL .csv]* （コンマ区切り値の場合）、または&#x200B;*[!UICONTROL .zip]* （圧縮されたZIP形式の場合、TSV ファイルに展開）。 ファイル名に次の文字を含めることはできません。`# % & * \| \ : " < > . ? /`<br><br>**ヒント：**&#x200B;国際文字を含むデータの場合は、TSVまたはTXT形式のファイルを使用します。 |
| [!UICONTROL Single Account] | ファイルが1つのアカウントに適用されるかどうか：*[!UICONTROL Yes]* （1つのアカウントの場合）または&#x200B;*[!UICONTROL No]* （複数のアカウントの場合）。 |
| [!UICONTROL Account (Search Engine)] | （ファイルが1つのアカウントに適用される場合）データをアップロードするアカウント。 |
| [!UICONTROL Search Engine] | （ファイルが複数のアカウントに適用される場合）データをアップロードする広告ネットワーク。<br><br>**注：**&#x200B;最適化されたポートフォリオのキーワードの入札変更は、複数アカウントのバルクシートではサポートされていません。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを投稿するタイミングまたは場合：<ul><li>*[!UICONTROL Post to search engine now]* （既定値）: データの投稿をすぐに開始します。</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:*&#x200B;指定された日時にデータの投稿を開始します。デフォルトは明日の02:00 （午前2時）です。 日付を変更するには、DD/MM/YYYY形式で日付を入力するか、カレンダーアイコンをクリックしてカレンダーを開き、日付を選択します。 時間を変更するには、リストから時間（15分間隔）を選択します。</li><li>*[!UICONTROL Preview only]:* データをアドネットワークに投稿せずに、ファイルをSearch、Social、およびCommerceにアップロードします。後でファイルを投稿することもできます。 バルクシートファイルが10 MBを超えて2 GB未満の場合、ファイルはZIP形式になります。投稿するためにファイルを解凍する必要はありません。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを含むアカウントにトラッキングテンプレートとランディングページのサフィックス（該当する広告ネットワークの場合）を含めるか、宛先URLを含むアカウントにトラッキングコードを埋め込む宛先URLを含めるか、投稿のすべてのキーワード、広告、プレースメント、サイトリンク、および[!DNL Google Ads]製品グループについて、*[!UICONTROL Yes]* （デフォルト）または&#x200B;*[!UICONTROL No]*&#x200B;です。 入札単位がポートフォリオにあるかどうかは関係ありません。<br><br> 「*[!UICONTROL Yes]*」を選択すると、関連するアカウント設定またはキャンペーン設定の「[!UICONTROL Tracking Methods]」セクションのパラメーターに従ってURLが生成されます。 デフォルトでは、トラッキング URLが存在する場合は、新しいURLが必要でない限り再生成されません（キーワードマッチタイプ、広告テキスト、関連アカウントのトラッキングパラメーターが変更された場合など）。<br><br> アップロードされたファイルを手動で投稿することで、後でトラッキング URLを生成できます。<br><br>**メモ：**&#x200B;広告主がAdobe Advertising コンバージョントラッキングを使用しており、ベース URLが変更されている場合は、アカウントが自動生成およびトラッキング URL アップロードをアップロード作成しない必要です。*[!UICONTROL No]* |
| [!UICONTROL Replace Media Optimizer Tracking] | （[!UICONTROL Generate Tracking URLs]が&#x200B;*[!UICONTROL Yes]*&#x200B;の場合に使用可能）アップロードされたファイルのURLにある既存のAdobe Advertising トラッキングを、新しく生成されたトラッキングに置き換えます。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータにもとづいて、最適化されたポートフォリオでキャンペーンの予算を変更できます。 デフォルトでは、このオプションは選択されていません。 このオプションを選択すると、最適化機能が（通常は次の入札サイクルで）予算を再割り当てする必要があると判断するまで、指定されたキャンペーン予算の変更が適用されます。<br><br>**注意：**&#x200B;最適化されていないポートフォリオのキャンペーンに関する投稿データから生じる予算変更は、ファイルの投稿時に発生します。 変更は、翌日のキャンペーン管理ビューに表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれるキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日までバルクシートのデータに基づく入札変更を許可します。 このオプションを選択した場合は、**[!UICONTROL Hold bulksheet bids until]** フィールドに1 ～ 7日後の終了日を指定します。 |

>[!MORELIKETHIS]
>
>* [&#x200B; （新しいUI）バルクシートを使用したキャンペーンデータの管理について](about.md)
>* [&#x200B; （新しいUI） バルクシート ファイルのダウンロードと作成](download.md)
>* [&#x200B; （新しいUI）バルクシートの投稿またはエラーファイルの修正](post.md)
>* [&#x200B; （新しいUI）バルクシート ファイルのランディングページを検証](validate-landing-pages.md)
