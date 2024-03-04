---
title: バルクシートまたは修正済みエラーファイルのアップロード
description: バルクシートファイルを手動でアップロードする方法、または修正されたランディングページ検証エラーファイルをアップロードする方法について説明します。
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: e5102132a1e4ce25adb297f863db439b583b3ebe
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# バルクシートまたは修正済みエラーファイルのアップロード

バルクシートファイル、修正済みのランディングページ検証エラーファイル、およびその他の修正済みのエラーファイルを、次の用途でお使いのデバイスまたはネットワークからアップロードできます。 [サポートされる広告ネットワーク](bulksheet-about.md#bulksheet-functionality-by-network). ファイル内のカスタム列は、ファイルをアップロードすると削除されます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Upload Bulksheet]**.

1. 情報を [[!UICONTROL Upload Bulksheet] 設定](#bulksheet-upload-settings).

1. クリック **[!UICONTROL Apply]**.

タスクが開始されると、ファイルが [!UICONTROL Bulksheets] 表示。 ファイルが完成すると、そのファイルへのリンクが記載された電子メール通知が送信されます。 コンパイルされたデータの量に応じて、電子メール通知には数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルが [!UICONTROL Bulksheets] 表示すると、エラーファイルへのリンクが記載された電子メール通知が送信されます。

>[!NOTE]
>
>一括送信シートデータを広告ネットワークに投稿する場合は、 [!UICONTROL Progress] 列の [!UICONTROL Bulksheets] 表示。 大量のデータの投稿には時間がかかります。

## バルクシートの設定をアップロードし、修正されたエラーファイルをアップロードします {#bulksheet-upload-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL File to Upload] | アップロードするファイル。 フルパスとファイル名を入力するか、「 <b>[!UICONTROL Browse]</b> をクリックして、お使いのデバイスまたはネットワーク上でファイルを見つけます。<br><br>バルクシートファイルは、最大 2.5 GB（約 250 万行）で、次のファイル拡張子のいずれかを持つ必要があります。 <i>[!UICONTROL .tsv]</i> （タブ区切り値の場合）、 <i>[!UICONTROL .txt]</i> （Unicode 準拠の ASCII テキストの場合）、 <i>[!UICONTROL .csv]</i> （コンマ区切り値の場合）または <i>[!UICONTROL .zip]</i> （圧縮 ZIP 形式の場合。TSV ファイルに解凍します）。 ファイル名に次の文字を含めることはできません： `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>ヒント：</b> 国際文字を含むデータの場合は、TSV 形式または TXT 形式のファイルを使用します。 |
| [!UICONTROL Single Account] | ファイルを 1 つのアカウントに適用するかどうか： <i>[!UICONTROL Yes]</i> （1 件のアカウントの場合）または <i>[!UICONTROL No]</i>（複数のアカウントの場合）。 |
| [!UICONTROL Account (Search Engine)] | （ファイルが単一のアカウントに適用される場合）データのアップロード先のアカウント。 |
| [!UICONTROL Search Engine] | （ファイルが複数のアカウントに適用される場合）データのアップロード先の広告ネットワーク。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを投稿するタイミングまたは場合：<ul><li><i>[!UICONTROL Post to ad network now]</i> （デフォルト）：データの投稿を直ちに開始します。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> 指定した日時にデータの投稿を開始します。デフォルトは明日の 02:00（午前 2 時）です。 日付を変更するには、DD/MM/YYYY または D/M/YYYY の形式で日付を入力するか、 ![カレンダー](/help/search-social-commerce/campaign-management/bulksheets/assets/calendar.png "カレンダー") カレンダーを開き、 [日付を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 時間を変更するには、HH/MM または H/M の形式で時間を入力するか、（15 分間隔で）リストから時間を選択します。</li><li><i>[!UICONTROL Preview only]:</i> データを広告ネットワークに投稿せずに Search、Social、および Commerce にファイルをアップロードする場合は、後でファイルを投稿することができます。 バルクシートファイルが 10 MB を超え、2 GB 未満の場合、ファイルは ZIP 形式になるので、投稿するためにファイルを解凍する必要はありません。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを使用するアカウントに（適用可能な広告ネットワークに対して）トラッキングテンプレートとランディングページのサフィックスを含めるか、すべてのキーワード、広告、プレースメント、サイトリンク、 [!DNL Google Ads] 掲示中の製品グループ： <i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>. 入札単位がポートフォリオに含まれているかどうかは関係ありません。<br><br>次を選択した場合、 <i>[!UICONTROL Yes]</i>を指定した場合、 [!UICONTROL Tracking Methods] 」セクションに追加します。 デフォルトでは、トラッキング URL が存在する場合、新しい URL が必要な場合（キーワードの一致タイプ、広告テキスト、関連するアカウントのトラッキングパラメーターが変更された場合など）を除き、再生成されません。<br><br>次を選択した場合、 <i>[!UICONTROL No]</i>その場合でも、アップロードしたファイルを手動で投稿することで、後でトラッキング URL を生成できます。<br><br><b>注意：</b> 広告主がAdobe Advertisingコンバージョントラッキングを使用し、ベース URL が変更された場合、トラッキング URL を自動的に生成してアップロードするようにアカウントが設定されていない限り、新しいトラッキング URL を生成する必要があります。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータに基づいて最適化されたポートフォリオのキャンペーンに予算の変更を許可します。 デフォルトでは、このオプションは選択されていません。 このオプションを選択した場合、指定したキャンペーン予算の変更は、最適化機能が予算を（通常は次の入札サイクルで）再割り当てする必要があると判断するまで、適用されます。<br><br><b>注意：</b> 最適化されていないポートフォリオのキャンペーンの転記済データに起因する予算の変更は、ファイルの転記時に発生します。 変更は翌日にキャンペーン管理ビューに表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれるキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日まで、バルクシート内のデータに基づいて入札の変更を許可します。 このオプションを選択した場合は、「 **[!UICONTROL Hold bulksheet bids until]** フィールドに入力します。 |

>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [バルクシートファイルをダウンロード/作成する](bulksheet-download.md)
>* [バルクシートの投稿または修正されたエラーファイル](bulksheet-post.md)
>* [バルクシートファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [生成またはアップロードされたバルクシートファイルのエクスポート](bulksheet-export.md)
