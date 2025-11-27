---
title: バルクシートまたは修正されたエラーファイルのアップロード
description: バルクシートファイルまたは修正されたランディングページ検証エラーファイルを手動でアップロードする方法を説明します。
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# バルクシートまたは修正されたエラーファイルのアップロード

[&#x200B; サポートされている広告ネットワーク &#x200B;](bulksheet-about.md#bulksheet-functionality-by-network) 用に、バルクシートファイル、修正されたランディングページ検証エラーファイル、その他の修正されたエラーファイルを、デバイスまたはネットワークからアップロードできます。 ファイルをアップロードすると、ファイル内のカスタム列はすべて削除されます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Bulksheets]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Upload Bulksheet]**] をクリックします。

1. [[!UICONTROL Upload Bulksheet] 設定 &#x200B;](#bulksheet-upload-settings) で情報を入力または選択します。

1. 「**[!UICONTROL Apply]**」をクリックします。

タスクが開始されると、ファイルが [!UICONTROL Bulksheets] ビューに一覧表示されます。 ファイルが完成すると、ファイルへのリンクが記載されたメール通知が送信されます。 コンパイルされたデータの量に応じて、メール通知は数分以上かかる場合があります。 ただし、ファイルの生成に失敗した場合は、エラーファイルが [!UICONTROL Bulksheets] ビューに一覧表示され、エラーファイルへのリンクを含むメール通知が送信されます。

>[!NOTE]
>
>バルクシート データを広告ネットワークに投稿すると、[!UICONTROL Progress] ビューの [!UICONTROL Bulksheets] 列でファイルの進行状況を追跡できます。 大量のデータがポストされるまでに時間がかかる。

## バルクシートおよび修正されたエラーファイルの設定のアップロード {#bulksheet-upload-settings}

| パラメーター | 説明 |
|----|----|
| [!UICONTROL File to Upload] | アップロードするファイル。 フルパスとファイル名を入力するか、「<b>[!UICONTROL Browse]</b>」をクリックしてデバイスまたはネットワーク上のファイルを探し、ファイルを指定します。<br><br> バルクシートファイルの拡張子は、最大 2.5 GB （約 2.5 万行）で、<i>[!UICONTROL .tsv]</i> （タブ区切り値の場合）、<i>[!UICONTROL .txt]</i> （Unicode 準拠の ASCII テキストの場合）、<i>[!UICONTROL .csv]</i> （コンマ区切り値の場合）、<i>[!UICONTROL .zip]</i> （圧縮された ZIP 形式の場合、TSV ファイルに解凍）のいずれかである必要があります。 ファイル名に次の文字を含めることはできません：`# % &amp; * \| \ : " < > . ? /`<br><br><b> ヒント：</b> 国際文字を含むデータの場合は、TSV または TXT 形式のファイルを使用します。 |
| [!UICONTROL Single Account] | ファイルが 1 つのアカウントに適用されるかどうか：<i>[!UICONTROL Yes]</i> （1 つのアカウントの場合）または <i>[!UICONTROL No]</i> （複数のアカウントの場合）。 |
| [!UICONTROL Account (Search Engine)] | （ファイルが 1 つのアカウントに適用される場合） データのアップロード先のアカウント。 |
| [!UICONTROL Search Engine] | （ファイルが複数のアカウントに適用される場合） データのアップロード先の広告ネットワーク。 |
| [!UICONTROL Scheduling] | 指定した広告ネットワークにファイルを POST する場合または POST する場合：<ul><li><i>[!UICONTROL Post to ad network now]</i> （デフォルト）：データの投稿を直ちに開始します。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> 指定した日時にデータの投稿を開始します。デフォルトは明日の午前 2 時 :00 す。 日付を変更するには、DD/MM/YYYY または D/M/YYYY の形式で日付を入力するか、「![&#x200B; カレンダー &#x200B;](/help/search-social-commerce/assets/calendar.png " カレンダー ")」をクリックしてカレンダーを開き、[&#x200B; 日付を選択 &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md) します。 時間を変更するには、HH/MM または H/M の形式で時間を入力するか、リストから時間（15 分間隔）を選択します。</li><li><i>[!UICONTROL Preview only]:</i> 広告ネットワークにデータを投稿せずに、検索、ソーシャル、Commerceにファイルをアップロードするには、後でファイルを投稿できます。 バルクシートファイルが 10 MB を超えて 2 GB 未満の場合、ファイルは ZIP 形式です。投稿するためにファイルを解凍する必要はありません。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | トラッキングテンプレートを使用するアカウントにトラッキングテンプレートおよびランディングページのサフィックス（該当する広告ネットワークの場合）を含めるか、宛先 URL を使用するアカウントにトラッキングコードが埋め込まれた宛先 URL を含めるか（すべてのキーワード、広告、プレースメント、サイトリンク、[!DNL Google Ads] 製品グループの場合）、<i>[!UICONTROL Yes]</i> （デフォルト）または <i>[!UICONTROL No]</i>。 入札単位がポートフォリオ内にあるかどうかは関係ありません。<br><br> 「<i>[!UICONTROL Yes]</i>」を選択すると、関連するアカウント設定またはキャンペーン設定の「[!UICONTROL Tracking Methods]」セクションのパラメーターに従って URL が生成されます。 デフォルトでは、トラッキング URL が存在する場合、新しい URL が必要でない限り（キーワード一致タイプ、広告テキスト、関連するアカウントのトラッキングパラメーターが変更された場合など）、トラッキング URL は再生成されません。<br><br> 「<i>[!UICONTROL No]</i>」を選択した場合でも、アップロードされたファイルを手動で投稿することで、後でトラッキング URL を生成できます。<br><br><b> メモ：</b> 広告主がAdobe Advertisingのコンバージョントラッキングを使用し、ベース URL が変更された場合、トラッキング URL を自動生成してアップロードするようにアカウントが設定されていない限り、新しいトラッキング URL を生成する必要があります。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 投稿されたデータに基づいて、最適化されたポートフォリオのキャンペーンに対して予算を変更できます。 デフォルトでは、このオプションは選択されていません。 このオプションを選択した場合、最適化機能によって予算を再割り当てする必要があると判断されるまで（通常は次の入札サイクルで）、指定したキャンペーン予算の変更がすべて適用されます。<br><br><b> 注意：</b> 最適化されていないポートフォリオのキャンペーンの投稿データに起因する予算の変更は、ファイルの投稿時に発生します。 翌日、キャンペーン管理ビューに変更が表示されます。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 含まれているキャンペーンコンポーネントが最適化されたポートフォリオにある場合、この機能は最適化戦略を上書きし、指定された終了日まで、バルクシートのデータに基づいた入札変更を許可します。 このオプションを選択した場合は、「終了日」フィールドに 1～7 日の間 **[!UICONTROL Hold bulksheet bids until]** 終了日を指定します。 |

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用した Campaign データの管理について &#x200B;](bulksheet-about.md)
>* [&#x200B; バルクシートファイルのダウンロード/作成 &#x200B;](bulksheet-download.md)
>* [&#x200B; ポストバルクシートまたは修正されたエラーファイル &#x200B;](bulksheet-post.md)
>* [&#x200B; バルクシートファイル内のランディングページの検証 &#x200B;](bulksheet-validate-landing-pages.md)
>* [&#x200B; 生成またはアップロードされたバルクシートファイルのエクスポート &#x200B;](bulksheet-export.md)
