---
title: スケジュール済みレポートの管理
description: スケジュールレポートの管理方法を説明します。
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# スケジュール済みレポートの管理

パフォーマンスレポートを使用すると、ポートフォリオ、広告ネットワーク、広告ネットワークアカウントエンティティのパフォーマンスを、必要に応じて詳細に追跡および管理できます。 多くのレポートでは、各マーケティングチャネルの広告がコンバージョン率に与える影響を包括的に把握できます。

レポートのデータは、レポートを実行するたびに動的にコンパイルされます。 必要に応じて、既存のレポートから新しいレポートを生成できます。 使用可能なレポートパラメーターは、レポートタイプによって異なります。 ほとんどのレポートでは、レポート全体を生成する代わりに、最初の50行をプレビューするオプションがあります。 レポートを生成すると、レポートの完了時に、1つ以上の電子メールアドレスにダウンロードリンクを含む通知を送信でき、受信者は[で通知を管理できます（[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)）。

完成したすべてのレポートは、[!UICONTROL Reports] ビューの[!UICONTROL Latest Reports] セクションで利用できます。ブラウザーウィンドウでテーブル形式で表示するか、ファイルとして開いたりダウンロードしたりできます。

## 使用可能なレポートカテゴリ

次のレポートカテゴリは、[!UICONTROL Reports] ビューから利用できます。 それらのすべてにアクセスできない場合があります。使用可能なレポートと生成されるデータは、お客様の役割と顧客アカウントの設定方法によって決まります。

| レポートカテゴリ | 説明 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [すべてのユーザーが利用できる基本レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)では、ポートフォリオ、広告ネットワークアカウント、特定の広告ネットワークアカウント、キャンペーン、広告グループ、広告、広告、キーワード、製品グループ、ラベル分類とラベル値、入札単位の制約、およびネットワークの制約の実際のコストとクリックデータを表示します。 該当する広告ネットワークから請求されるクリック数に基づいています。オプションで、コンバージョンデータや作成した他の指標を含めることができます。 |
| [!UICONTROL Advanced Reports] | [高度なレポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)では、広告の設定にinsightが追加されています。これにより、地理的なターゲティングやネットワークの設定を変更することで、どのようなメリットを得られるかを特定できます。 また、キャンペーンおよびポートフォリオ管理ビューにおけるコンバージョンデータや、広告主の内部コンバージョン追跡データに対するレポートの検証にも役立ちます。 |
| [!UICONTROL Assist Reports] | [&#x200B; アシストレポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md)は、広告主のすべてのキーワードと広告のコンバージョンパスに関するインサイトを提供します。 Adobe Advertisingコンバージョントラッキングサービスを通じて取得したデータを使用し、サービスを提供する広告主に対してのみ生成できます。 |
| [!UICONTROL Specialty Reports] | [特殊レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md)は、（Adobe Advertising トラッキングではなく）広告ネットワークによって収集されたデータで構成されます。 |
| [!UICONTROL Model Accuracy Reports] | [&#x200B; モデル精度レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md)は、ポートフォリオの入札、キャンペーン予算、入札戦略目標の最適化に使用されるコストと収益モデルの精度を示します。 |

## レポートの自動作成

次のいずれかの方法または両方で、カスタマイズされたレポートを自動的に生成するようにスケジュールします。

* [&#x200B; レポートテンプレート &#x200B;](/help/search-social-commerce/reports/automation/templates/template-about.md)を使用して、毎日、または特定の曜日または月にレポートを自動生成します。

  オプションで、テンプレートを使用する基本レポートと詳細レポート [&#128279;](/help/search-social-commerce/new-ui/reports/ftp-reports.md)のFTP配信を設定できます。

* [&#x200B; スプレッドシート フィード &#x200B;](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)を使用して、カスタマイズしたスプレッドシート テンプレートを毎日のパフォーマンスデータで更新し続けます。

## [!UICONTROL Scheduled Reports] ビュー

[!UICONTROL Reports] > [!UICONTROL Scheduled Reports] ビューでは、レポートとレポートテンプレートを作成および管理できます。

* 「**[!UICONTROL Latest Reports]**」タブには、手動で削除されたレポートを除き、利用可能なすべてのレポートが一覧表示されます。デフォルトでは、最新のレポートが上部に表示されます。 <!-- Doesn't seem to be true: that were requested in the last seven days -->各レポートに表示される情報には、レポートを実行するスケジュール（該当する場合）、データが生成されたか生成される開始日と終了日、レポートを作成したユーザー、レポートのステータス （*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*、または&#x200B;*[!UICONTROL Error]*）が含まれます。

  各レポートの横にあるリンクを使用すると、レポートを[!DNL Microsoft Excel] ワークブック （XLS）、タブ区切り値（TSV） ファイル、またはコンマ区切り値（CSV） ファイルとして開いたり保存したりできます。 一部のレポートタイプは、該当するキャンペーンごとに個別のワークシートを含む[!UICONTROL Excel] ワークブックとして保存することもできます。

  このタブから、新しいレポートを作成し（オプションでテンプレートとして使用できます）、既存のレポートの設定またはレポートテンプレートを使用して新しいレポートを作成し、利用可能な進行中のレポートを削除してキャンセルし、利用可能な完成したレポートを削除することもできます。

* 「**[!UICONTROL Templates]**」タブには、関連するスケジュールに関する情報を含め、利用可能なすべての保存された基本および詳細レポートテンプレートが一覧表示されます。 デフォルトでは、最新のテンプレートが一番上にあります。

  このタブから、新しいテンプレートを作成し、作成したテンプレート（スケジュールの追加、変更、削除を含む）を編集し、テンプレートからレポートを生成し、使用可能なテンプレートを削除します。

## レポートの活用方法

| 目的 | レポート |
| ---- | ---- |
| パフォーマンス監視 | <ul><li>[The [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[The [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[The [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[The [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[The [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[The [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| パフォーマンスのトラブルシューティングとトレンド分析 | <ul><li>[The [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[The [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[The [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[The [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[The [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) and [The [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>&quot;[!UICONTROL Compare with]&quot;機能を使用して2つの時間ウィンドウを比較する基本レポート</li></ul> |
| ビジネス成長機会の特定 | <ul><li>（Adobe Advertising コンバージョントラッキングを使用する広告主のみ） [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>（Adobe Advertising コンバージョントラッキングを使用する広告主のみ） [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>（[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=ja)の広告主） Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |
| 分析 | <ul><li>（Adobe Advertising コンバージョントラッキングを使用する広告主のみ） [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>（[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=ja)の広告主） Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |

## レポートの生成

### 新しいレポートを生成

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;をクリックします。

1. **[!UICONTROL Create Report]**&#x200B;をクリックし、左側のパネルでレポートカテゴリをクリックしてから、レポートタイプを選択します。<!-- Add link to list of report categories and report types --> **[!UICONTROL Proceed]**&#x200B;をクリックします。

1. （オプション） [!UICONTROL Create Report] ウィンドウで、[基本レポートおよび詳細レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)、[&#x200B; アシストレポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md)、[&#x200B; モデル精度レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md)、および[特殊レポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md)のデフォルトのレポート設定を変更します。

   1. （オプション）レポートとテンプレートのカスタム名を入力します（レポートをテンプレートとして保存する場合）。

   1. （オプション）レポート設定をテンプレートとして保存するには、**[!UICONTROL Save as template]**&#x200B;設定を有効にします。

   1. （オプション）同じレポートカテゴリ内の別のレポート **[!UICONTROL Type]**&#x200B;を選択します。

   1. （オプション）「**[!UICONTROL Basic Settings]**」タブで、使用する既存のレポートテンプレートを選択するか、レポートのデフォルトの基本設定を変更します。

   1. （オプション）「**[!UICONTROL Columns]**」タブをクリックし、レポートのデフォルトの列（列の順序を含む）を変更します。

      デフォルトでは、レポート内のすべての金銭的データは、米ドルの形式（1,000.00など）で表示されます。 正しい通貨形式で値を表示するには（ただし、CSVおよびTSV形式で通貨記号を使用しない）、「[!UICONTROL Currency]」列をレポートに追加します。 レポートに異なる通貨を持つアカウントのデータが含まれる場合、通貨に関係なく、「[!UICONTROL Total]」の金銭的値は、列のすべての数値の合計になります。

   1. （一部のレポートタイプ、オプション）「**[!UICONTROL Filters & Attribution]**」タブまたは「**[!UICONTROL Filters]**」タブをクリックしてデータフィルターを追加し、（一部のレポートタイプ）レポート結果に特定のラベル分類のみを含めるように制限し、デフォルトのアトリビューションルールとコンバージョンアトリビューション設定を変更します。

   1. （オプション）「**[!UICONTROL Scheduling]**」タブをクリックし、デフォルトのスケジュール設定と配信オプションを変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

レポートスケジュールを指定しなかった場合、レポートはすぐに実行されます。指定したスケジュールに従って実行されます。 レポート名が[[!UICONTROL Latest Reports] ビュー](/help/search-social-commerce/reports/report-about.md)に追加されます。 レポートをテンプレートとして保存すると、[[!UICONTROL Templates] ビュー](/help/search-social-commerce/reports/report-about.md)にも追加されます。 レポートが完了すると、ファイルを開いたり保存したりできます。テンプレートはすぐに利用できます。

通知に電子メールアドレスを入力した場合、ユーザーの[&#x200B; レポート用に設定された通知設定](/help/search-social-commerce/notifications/notification-edit.md)に基づいて、各受信者はレポートジョブが完了または失敗したときに通知を受け取ります。

### 既存のレポートからのレポートの生成

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;をクリックすると、**[!UICONTROL Latest Reports]** タブが開きます。

1. 次のいずれかの操作を行います。

   * レポート行の上にカーソルを置き、**...** > **[!UICONTROL Duplicate]**&#x200B;をクリックします。

   * レポートの横にあるチェックボックスをオンにします。 一括アクションツールバーで、[複製](/help/search-social-commerce/assets/duplicate.png "重複")をクリックします。

1. 必要に応じて、レポート設定を編集します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

### 既存のテンプレートからのレポートの生成

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. 次のいずれかの操作を行います。

   * テンプレート行の上にカーソルを置き、**...** > **[!UICONTROL Duplicate]**&#x200B;をクリックします。

   * 既存のテンプレートの横にあるチェックボックスをオンにします。 一括操作ツールバーで、[複製](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**&#x200B;をクリックします。

1. （オプション）テンプレートの名前を変更し、必要に応じてレポート設定を編集します。

   **[!UICONTROL Next]**&#x200B;をクリックして、設定セクション間を移動します。

1. **[!UICONTROL Save as Template]**&#x200B;設定を有効にします。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## レポートのプレビューまたは保存

Web ブラウザーでレポートをプレビューするか、レポートデータを[!DNL Microsoft Excel] ワークブック、タブ区切り値（TSV） ファイル、コンマ区切り値（CSV） ファイル、または（一部のレポートタイプ）タブ付きワークブックとして開いたり保存したりできます。[!DNL Microsoft Excel]

>[!NOTE]
>
>Adobe アカウントチームのメンバーと一部の管理者ユーザーは、広告主や代理店のユーザーが作成したレポートを表示できます。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;をクリックすると、**[!UICONTROL Latest Reports]** タブが開きます。

1. 次のいずれかの操作を行います。

   * （Web ブラウザーでレポートを表示するには）次のいずれかの操作を行います。

      * テンプレート行の上にカーソルを置き、**...** > **[!UICONTROL Preview]**&#x200B;をクリックします。

      * 既存のテンプレートの横にあるチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL Preview]**&#x200B;をクリックします。

   * （ファイル内のレポートデータを開いたり保存したりするには） レポート名の横にある[!UICONTROL Export]列で、形式の名前をクリックし、ブラウザーの通常の手順に従ってファイルを開いたり保存したりします。

      * **[!UICONTROL XLS]:**&#x200B;単一のワークシート （XLSX形式）を持つ[!DNL Excel] ワークブックの場合。 このレポートには、上部にパラメーターのラベルが付いた1つのワークシートが含まれており、コンポーネントのデータが使用可能な場合に各コンポーネントに1行がレポートされます。 データのない行は省略されます。

        基本レポートには、各数値列の合計が含まれます。

      * TSV ファイルの&#x200B;**[!UICONTROL TSV]:**。 レポートには、レポートされる各コンポーネントのパラメーターと1行が含まれます。

      * **[!UICONTROL CSV]:** CSV ファイルの場合。 レポートには、レポートされる各コンポーネントのパラメーターと1行が含まれます。

## レポートの削除

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;をクリックすると、**[!UICONTROL Latest Reports]** タブが開きます。

1. 次のいずれかの操作を行います。

   * （1つのレポートを削除するには）:

      1. レポート行の上にカーソルを置き、**...** > **[!UICONTROL Run]**&#x200B;をクリックします。

      1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

   * （1つ以上のレポートを削除するには）:

      1. 削除する各レポートの横にあるチェックボックスをオンにします。

      1. 一括操作ツールバーで、[削除](/help/search-social-commerce/assets/delete-new.png "削除") **[!UICONTROL Delete]**&#x200B;をクリックします。

      1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
