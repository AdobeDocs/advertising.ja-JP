---
title: '[!UICONTROL Change History] レポートを表示'
description: 広告主アカウントに対する最近の変更を表示する方法を説明します。
exl-id: f8744da7-cc7a-49c1-aeac-1e601768f992
feature: Search Reports
TQID: https://experienceleague.adobe.com/nRlvKpVQf3wbMd83plf3CQp1pPYpHVJzMVJN54lryYM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 0%

---

# [!UICONTROL Change History] レポートを表示

（新しいUI） [!UICONTROL History Logs]および（従来のUI） [!UICONTROL Change History] レポートには、過去31日間に広告主アカウントに加えられた変更のログが含まれます。 このレポートには、ユーザー（広告主）、ポートフォリオ、キャンペーン、広告グループ、広告、キーワード、プレースメント、製品ターゲットの種類に対する変更が含まれます。 任意の列でデータを並べ替え、フィルタリングできます。

広告主の履歴ログに関する追加情報を[!DNL Microsoft Excel] ワークブック （XLSX ファイル）形式のファイルにダウンロードできます。 レポートには、古い値と新しい値、および変更が発生した時間が含まれます。

>[!NOTE]
>
>ポートフォリオの変更については、[ ポートフォリオの変更履歴](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-change-history.md)も参照してください。

## （新しいUI） [!UICONTROL History Logs] レポートを表示 {#history-logs-open}

1. メインメニューで、**[!UICONTROL Reports]** > **[!UICONTROL History Logs]**&#x200B;をクリックします。

1. （オプション） [ ビューに含まれるデータを変更](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)。

### [!UICONTROL History Logs]のレポートのダウンロードを管理

#### フィルタリングされたデータ行を含むレポートを生成する

1. [履歴ログを開きます](#history-logs-open)。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Grid Reports]設定で、一意のレポート名を入力し、**[!UICONTROL Generate]**&#x200B;をクリックします。

   デフォルトでは、ファイル名は「allChangeHistory_YYYYMMDD_NNNNN」で、「NNNN」は順次ジョブ番号（「allChangeHistory_20260402_1326」など）です。

   ファイルが[!UICONTROL Recently Generated] リストに追加されます。

1. （オプション）完了したファイルをダウンロードするには、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

#### 完成したレポートをダウンロード

1. [履歴ログを開きます](#history-logs-open)。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

#### 完了済みレポートの削除

1. [履歴ログを開きます](#history-logs-open)。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

## （レガシーUI） [!UICONTROL Change History] レポートを表示

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Change History]**&#x200B;をクリックします。

1. （オプション）次のいずれかの方法で、レポートに含まれるデータを変更します。

   * （列を表示または非表示にするには）列の見出しの右側にある![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")をクリックし、**[!UICONTROL Columns]**&#x200B;を強調表示してから、各列の横にあるチェックボックスを選択して含め、除外する各列の横にあるチェックボックスをオフにします。

     列設定は、すべての広告主のビューに適用されます。

   * （列の値でデータをフィルタリングするには）次のいずれかの操作を行います。

      * [**[!UICONTROL Add Filter]** リンク ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)を使用してフィルターを適用します。

      * [列見出しメニュー](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)からフィルターを適用します。

   * （レポートの日付範囲を変更するには）次の操作を行います。

      1. データテーブルの上で、現在の日付範囲をクリックします。

      1. 範囲を指定します。

         * （プリセット範囲の場合） – 共通の時間増分のリストから選択します。 デフォルトは&#x200B;*[!UICONTROL 2 Days Ago]*&#x200B;です。

         * （特定の範囲の場合） - **[!UICONTROL Custom Date Range]**&#x200B;を選択し、開始日と終了日を指定します。

           MM/DD/YYYYまたはMM-DD-YYYY形式で日付を入力するか、各フィールドの横にある![ カレンダー](/help/search-social-commerce/assets/calendar.png " カレンダー")をクリックしてカレンダーを開き、日付を選択します。 過去31日間のデータのみを含めることができます。

      1. **[!UICONTROL Apply]**&#x200B;をクリックします。

1. （オプション）レポートのコピーをダウンロードします。

   1. データテーブルの上で、**[!UICONTROL Download]**&#x200B;をクリックします。

      レポートが完了すると、[!UICONTROL Download] メニューに表示されます。

   1. （レポートデータをファイルで開いたり保存したりするには） ファイル名の横にある![ レポートをXLSとしてダウンロード ](/help/search-social-commerce/assets/download-spreadsheet2.png " レポートをXLSとしてダウンロード ")をクリックし、ブラウザーの通常の手順に従ってファイルを開いたり保存したりします。

      詳しくは、ブラウザーのオンラインヘルプを参照してください。
