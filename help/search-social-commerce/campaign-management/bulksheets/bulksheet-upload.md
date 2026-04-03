---
title: バルクシートまたは修正されたエラーファイルのアップロード
description: バルクシート ファイルを手動でアップロードする方法と、修正されたランディングページ検証エラーファイルをアップロードする方法について説明します。
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/3dJ14x6JFvS-ig5s6ElT0Vv-Kzd5KWQu0JiItdrG3ZA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 800
ht-degree: 0%

---

# バルクシートまたは修正されたエラーファイルのアップロード

[&#x200B; サポートされている広告ネットワーク &#x200B;](bulksheet-about.md#bulksheet-functionality-by-network)のバルクシート ファイル、修正されたランディングページ検証エラーファイル、およびその他の修正されたエラーファイルを、お使いのデバイスまたはネットワークからアップロードできます。 ファイルをアップロードすると、ファイル内のカスタム列はすべて削除されます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Upload Bulksheet]**&#x200B;をクリックします。

1. [[!UICONTROL Upload Bulksheet]設定](#bulksheet-upload-settings)で情報を入力または選択します。

1. **[!UICONTROL Apply]**&#x200B;をクリックします。

タスクが開始されると、ファイルは[!UICONTROL Bulksheets] ビューに表示されます。 ファイルが完了すると、ファイルへのリンクを記載したメール通知が送信されます。 収集されたデータ量によっては、メール通知に数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルが[!UICONTROL Bulksheets] ビューに表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>バルクシート データを広告ネットワークに投稿すると、[!UICONTROL Progress] ビューの[!UICONTROL Bulksheets]列でファイルの進行状況を確認できます。 大量のデータを投稿するには時間がかかります。

## バルクシートと修正されたエラーファイルの設定をアップロードする {#bulksheet-upload-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL File to Upload] | アップロードするファイル。 ファイルを指定するには、フルパスとファイル名を入力するか、<b>[!UICONTROL Browse]</b>をクリックしてデバイスまたはネットワーク上のファイルを検索します。<br><br> バルクシートファイルは、最大2.5 GB （約250万行）までで、次のいずれかのファイル拡張子を持つ必要があります：<i>[!UICONTROL .tsv]</i> （タブ区切り値の場合）、<i>[!UICONTROL .txt]</i> （Unicode準拠のASCII テキストの場合）、<i>[!UICONTROL .csv]</i> （コンマ区切り値の場合）、または<i>[!UICONTROL .zip]</i> （圧縮されたZIP形式の場合、TSV ファイルに展開）。 ファイル名に次の文字を含めることはできません。`# % &amp; * \| \ : " < > . ? /`<br><br><b> ヒント：</b>国際文字を含むデータの場合は、TSVまたはTXT形式のファイルを使用します。 |
| [!UICONTROL Single Account] | ファイルが1つのアカウントに適用されるかどうか：<i>[!UICONTROL Yes]</i> （1つのアカウントの場合）または<i>[!UICONTROL No]</i> （複数のアカウントの場合）。 |
| [!UICONTROL Account (Search Engine)] | （ファイルが1つのアカウントに適用される場合）データをアップロードするアカウント。 |
| [!UICONTROL Search Engine] | （ファイルが複数のアカウントに適用される場合）データをアップロードする広告ネットワーク。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを投稿するタイミングまたは場合：<ul><li><i>[!UICONTROL Post to ad network now]</i> （既定値）: データの投稿をすぐに開始します。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i>指定された日時にデータの投稿を開始します。デフォルトは明日の02:00 （午前2時）です。 日付を変更するには、日付をDD/MM/YYYYまたはD/M/YYYY形式で入力するか、![&#x200B; カレンダー](/help/search-social-commerce/assets/calendar.png " カレンダー")をクリックしてカレンダーを開き、[日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)します。 時間を変更するには、HH/MMまたはH/M形式で時間を入力するか、リストから時間（15分間隔）を選択します。</li><li><i>[!UICONTROL Preview only]:</i> データをアドネットワークに投稿せずにSearch, Social, &amp; Commerceにファイルをアップロードする場合、後でファイルを投稿できます。 バルクシートファイルが10 MBを超えて2 GB未満の場合、ファイルはZIP形式になります。投稿するためにファイルを解凍する必要はありません。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを含むアカウントにトラッキングテンプレートとランディングページのサフィックス（該当する広告ネットワークの場合）を含めるか、宛先URLを含むアカウントにトラッキングコードを埋め込む宛先URLを含めるか、投稿のすべてのキーワード、広告、プレースメント、サイトリンク、および[!DNL Google Ads]製品グループについて、<i>[!UICONTROL Yes]</i> （デフォルト）または<i>[!UICONTROL No]</i>です。 入札単位がポートフォリオにあるかどうかは関係ありません。<br><br> 「<i>[!UICONTROL Yes]</i>」を選択すると、関連するアカウント設定またはキャンペーン設定の「[!UICONTROL Tracking Methods]」セクションのパラメーターに従ってURLが生成されます。 デフォルトでは、トラッキング URLが存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードマッチタイプ、広告テキスト、関連アカウントのトラッキングパラメーターが変更された場合など）。<br><br> 「<i>[!UICONTROL No]</i>」を選択した場合でも、アップロードしたファイルを手動で投稿することで、後でトラッキング URLを生成できます。<br><br><b>注：</b>広告主がAdobe Advertising コンバージョントラッキングを使用しており、ベース URLが変更された場合、トラッキング URLを自動生成してアップロードするようにアカウントが設定されていない限り、新しいトラッキング URLを生成する必要があります。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータにもとづいて、最適化されたポートフォリオでキャンペーンの予算を変更できます。 デフォルトでは、このオプションは選択されていません。 このオプションを選択すると、最適化機能で予算を再配分する必要があると判断されるまで、指定したキャンペーン予算の変更が適用されます（通常は次の入札サイクルで）。<br><br><b> メモ：</b>最適化されていないポートフォリオのキャンペーンに関する投稿データに起因する予算変更は、ファイルの投稿時に発生します。 変更は、翌日のキャンペーン管理ビューに表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれるキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日までバルクシートのデータに基づく入札変更を許可します。 このオプションを選択した場合は、**[!UICONTROL Hold bulksheet bids until]** フィールドに1 ～ 7日後の終了日を指定します。 |

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](bulksheet-download.md)
>* [&#x200B; バルクシートの投稿またはエラーファイルの修正](bulksheet-post.md)
>* [&#x200B; バルクシート ファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシート ファイルを書き出す](bulksheet-export.md)
