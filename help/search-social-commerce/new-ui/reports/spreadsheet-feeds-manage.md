---
title: （新しいUI）スプレッドシートのレポートフィードの管理
description: カスタム形式のスプレッドシートで日々のパフォーマンスデータを配信するスプレッドシートレポートフィードを作成、設定、更新、表示、削除する方法について説明します。
feature: Search Reports
source-git-commit: 38ee8dfbaf82d8f1d212a931956398444e61060f
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# （新しいUI）スプレッドシートのレポートフィードの管理

*基本レポートおよびモデル精度レポートのみ*

<!-- Update link to notifications once available -->

スプレッドシート フィードは、すべての基本レポートとモデル精度レポートの毎日のパフォーマンスデータを、[!DNL Microsoft Excel] XLSXのカスタム スプレッドシート形式で提供します。 通常のレポートテンプレートから作成した特殊な形式の[!DNL Excel] スプレッドシート テンプレートを使用して、スプレッドシート フィードを設定できます。 毎日、スプレッドシートは、毎日集計された新しい生データで、指定された時間に自動的に更新されます。 生データは、スプレッドシート テンプレートに含まれている列とグラフに入力されます。 スプレッドシート フィード ファイルが使用可能になったり、ファイルの生成に失敗したりすると、レポートテンプレートの各メール受信者は、ユーザーがレポート用に設定した[通知設定](/help/search-social-commerce/notifications/notification-about.md)に基づいて通知を受け取ります。

過去90日間のデータを更新するようにフィードを設定でき、以前のすべての既存のデータが残り、引き続き蓄積されます。

[!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds] ビューには、作成したすべてのスプレッドシート フィードが一覧表示されます。 このビューでは、スプレッドシート フィードを作成したり、フィードを手動で更新したり、フィードを削除したりできます。

## 使用可能なアクション

* [スプレッドシート レポートフィード用の [!DNL Excel]  テンプレートの作成](#spreadsheet-feed-create-excel-template)

* [スプレッドシートレポートフィードの作成](#spreadsheet-feed-create)

* [スプレッドシート レポート フィード設定の編集](#spreadsheet-feed-edit)

* [スプレッドシート レポート フィード ファイルの表示または保存](#spreadsheet-feed-view-or-save)

* [スプレッドシートレポートフィードを手動で更新する](#spreadsheet-feed-refresh)

* [スプレッドシート レポート フィードの削除](#spreadsheet-feed-delete)

## スプレッドシート レポート フィード用の[!DNL Excel] テンプレートの作成 {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

スプレッドシート フィードを作成するには、まず、通常のレポートテンプレートを使用して、特殊な形式の[!DNL Microsoft Excel] スプレッドシート テンプレートを作成する必要があります。 必要に応じて、[!DNL Excel] スプレッドシートをカスタマイズして、列とグラフを追加できます。

1. **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;で、「[!UICONTROL Daily]」の[!UICONTROL Date Aggregation] ユニットと、必要な他のすべてのデータパラメーターを使用して、目的のレポートタイプを生成し、レポートをテンプレートとして保存します。

   >[!NOTE]
   >
   > * [!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword]、および[!UICONTROL Forecast Accuracy]のレポート用のスプレッドシート フィードを作成できます。 [!UICONTROL Ad Group Report]を使用する場合は、より迅速な結果を得るために含める広告グループの数を制限してください。
   > * テンプレートで定義されている[!UICONTROL Date Range] ユニットは使用されていません。 スプレッドシート フィードを後で設定する際に、データを更新する日付を定義します。

1. レポートを生成したら、**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;に移動し、レポート出力のTSVまたはXLS バージョンをファイルに書き出します。

1. [!DNL Excel]で、レポート用のカスタムテンプレートを作成します。

   1. [!DNL Excel]でレポートファイルを開きます。

   1. ワークブックを準備します。

      1. レポートパラメーターを表示する一番上の行を削除します。 XLS ファイルの場合は、「[!UICONTROL Total]」行も削除します。 必要に応じて、データ行の一部を削除できますが、a）元の順序のすべての列を含むデータヘッダー行とb）少なくとも1つのデータ行を保持します。 手動でデータを追加しないでください。

         >[!NOTE]
         >
         > 最後の列には、ゼロ以外の値を含める必要があります。

      1. 開始日で昇順にデータを並べ替えます（最も古いものから最も新しいものまで）。

      1. ワークシートのタブ名を&quot;[!UICONTROL Sheet1]&quot;から&quot;[!UICONTROL RAW]&quot;に変更します。

         この特定のタブ名を使用すると、データを更新できます。

      1. （オプション）必要に応じて、レポートテンプレートの列の右側にカスタム列を追加します。

   1. （オプション）別のワークシートで、ピボットテーブルを作成します。 完了したら、ピボットテーブルの任意のセルを右クリックして&#x200B;**[!UICONTROL Pivot Table Options]**&#x200B;を選択し、「**[!UICONTROL Data]**」タブをクリックしてから「**[!UICONTROL Refresh data when opening the file]**」を選択します。

   1. ファイルを.XLSX形式の[!DNL Excel] スプレッドシートとして保存します。

## スプレッドシートレポートフィードの作成 {#spreadsheet-feed-create}

1. [ レポートデータを入力する [!DNL Excel]  テンプレートを作成します](#spreadsheet-feed-create-excel-template)。

1. スプレッドシート フィードを作成します。

   1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**&#x200B;をクリックします。

   1. 右上の「**[!UICONTROL Create Spreadsheet]**」をクリックします。

   1. **[!UICONTROL Create Spreadsheet Feed]** ダイアログで、[ スプレッドシート フィード設定](#spreadsheet-feed-settings)を指定します。

   1. **[!UICONTROL Submit]**&#x200B;をクリックします。

   1. （オプション）フィードの[!UICONTROL Update Status]が&#x200B;*[!UICONTROL Finished]*&#x200B;になったら、フィードの横にある&#x200B;**[!UICONTROL XLSX]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

      >[!NOTE]
      >
      >フィードに関連付けられているレポートテンプレートが後で削除された場合、フィードも削除されます。

      スプレッドシート フィードは、設定された[!UICONTROL Schedule Time]で毎日自動的に更新されます。 レポートテンプレートにメール受信者のアドレスが含まれている場合、スプレッドシートが更新されたときに、それらのアドレスに通知が送信されます。

## スプレッドシート レポート フィード設定の編集 {#spreadsheet-feed-edit}

>[!NOTE]
>
> レポートテンプレートの列を編集するか、新しいレポートテンプレートまたは更新されたレポートテンプレートを使用する場合は、それに応じて[!DNL Excel] テンプレートを更新し、再度アップロードする必要があります。

1. （オプション）スプレッドシート フィードに使用されているレポートテンプレートまたは[!DNL Excel] テンプレートを更新するには、次の手順を実行します。

   * （オプション）フィードに別のレポートテンプレートまたは更新されたレポートテンプレートを使用するには、[ レポートテンプレート ](#spreadsheet-feed-create-excel-template)用に新しい [!DNL Excel]  テンプレートを作成します。

     次の手順では、レポートテンプレートと新しい[!DNL Excel] ファイルの両方をアップロードします。

   * （オプション）カスタム列を[!DNL Excel] テンプレートに追加するには、レポートテンプレートから列の右側に列を挿入し、ファイルを[!DNL Excel] スプレッドシートとして.XLSX形式で保存します。 次の手順で、新しい[!DNL Excel] ファイルをアップロードする必要があります。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**&#x200B;をクリックします。

1. スプレッドシートのフィード設定を変更します。

   1. スプレッドシートのフィード名の横にあるチェックボックスをオンにします。

   1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

   1. [!UICONTROL Create Spreadsheet Feed]<!-- sic --> ダイアログで、[ スプレッドシート フィード設定](#spreadsheet-feed-settings)を変更します。

   1. **[!UICONTROL Submit]**&#x200B;をクリックします。

   1. （オプション）フィードの[!UICONTROL Update Status]が&#x200B;*[!UICONTROL Finished]*&#x200B;になったら、フィードの横にある&#x200B;**[!UICONTROL XLSX]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

   >[!NOTE]
   >
   > フィードに関連付けられているレポートテンプレートが後で削除された場合、フィードも削除されます。

   スプレッドシート フィードは、広告主のタイムゾーンで毎日08:00に自動的に更新されます。 レポートテンプレートにメール受信者のアドレスが含まれている場合、スプレッドシートが更新されたときに、それらのアドレスに通知が送信されます。

## スプレッドシートレポートフィード設定 {#spreadsheet-feed-settings}

| フィールド | 説明 |
|---|---|
| [!UICONTROL Feed Name] | スプレッドシート フィードの名前。 |
| [!UICONTROL Report Template] | 必要なレポートデータを指定するレポートテンプレートです。[!DNL Excel] テンプレートの作成に使用したレポートテンプレートを選択してください。 すべての基本レポートテンプレートが一覧表示されます。<br><br><b>注：</b> レポートに使用するレポートテンプレートを変更するか、テンプレートの列を更新した場合は、新しい[!DNL Excel] テンプレートを作成してアップロードする必要があります。 |
| [!UICONTROL Excel Template] | レポートテンプレートで指定されたデータに適用される.XLSX形式で作成した、特別に書式設定された[!DNL Excel] テンプレート。 アップロードするファイルを指定するには、フルパスとファイル名を入力するか、<b>[!UICONTROL Browse]</b>をクリックしてデバイスまたはネットワーク上のファイルを探します。 |
| [!UICONTROL Back Fill From] | [!UICONTROL RAW] タブ上の既存のデータが更新される開始日。過去の日数で表されます。 最大90日の値を入力します。デフォルトは7日です。<br><br>例えば、値が7で、今日が3月7日の場合、3月1日から始まる[!UICONTROL RAW] タブの既存のデータが更新されます（[!UICONTROL Back Fill Until] パラメーターで指定された終了日まで）。 3月1日より前の日付の既存のデータ行は削除されませんが、更新されません。 |
| [!UICONTROL Back Fill Until] | [!UICONTROL RAW] タブの既存のデータが更新される終了日。過去の日数で表されます。 デフォルト値は1日（1）です。<br><br>例えば、この値が1で、今日が3月7日の場合、[!UICONTROL RAW] タブの既存のデータは3月6日まで（および[!UICONTROL Back Fill From] パラメーターで指定された開始日から）更新されます。 この値が1で、[!UICONTROL Back Fill Until] パラメーターが7で、今日が3月7日の場合、[!UICONTROL RAW] タブの既存のデータは3月1日から3月6日の間に更新されます。 いずれの例でも、3月6日以降の日付の既存のデータ行は削除されませんが、更新されません。 |
| [!UICONTROL Email Recipients] | レポートが更新されるたびに、またはテンプレートにスケジュールが含まれている場合にレポートが実行されるたびに、通知を送信する電子メールアドレス。 デフォルトでは、ユーザーアカウントのアドレスが入力されます。 複数のアドレスを指定するには、コンマ、スペース、または新しい行で区切ります。 |
| [!UICONTROL Schedule Time] | スプレッドシート フィードが更新される時間：広告主のタイムゾーンの08:00または10:00 ～ 23:00の間の任意の時間。 新しいスプレッドシート フィードのデフォルトは10:00です。<br><br><b>注：</b> パフォーマンス上の理由から、他のレポートが生成される場合、09:00でスプレッドシート フィードを更新することはできません。 |
| [!UICONTROL Email Notification] | （メール受信者が指定されている場合）指定されたアドレスへのメール通知に含めるもの：<ul><li><i>[!UICONTROL Attach feed]</i>  – 完成したレポートのコピーをXLSX形式で送信します。 ファイルが10 MBを超える場合、通知には添付ファイルは含まれません。</li><li><i>[!UICONTROL Notification Only]</i> （既定値） – レポートへのリンクを含む、レポートの完了または失敗の通知のみを送信します。</li></ul> |

## スプレッドシート レポート フィード ファイルの表示または保存 {#spreadsheet-feed-view-or-save}

生成されたスプレッドシート フィードを表示したり、ファイルに保存したりできます。 スプレッドシート フィード ファイルは[!DNL Microsoft Excel] XLSX形式です。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**&#x200B;をクリックします。

1. フィードの横にある「**[!UICONTROL XLSX]**」をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

## スプレッドシートレポートフィードを手動で更新する {#spreadsheet-feed-refresh}

>[!NOTE]
>
>スプレッドシート フィードは、毎日08:00にローカル タイム ゾーンで自動的に更新されます。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**&#x200B;をクリックします。

1. 更新する各フィードの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Run Spreadsheet]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

1. （オプション）フィードの[!UICONTROL Update Status]が&#x200B;*[!UICONTROL Finished]*&#x200B;になったら、フィードの横にある&#x200B;**[!UICONTROL XLSX]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルを開くか保存します。

## スプレッドシート レポート フィードの削除 {#spreadsheet-feed-delete}

>[!NOTE]
>
>フィードに関連付けられているレポートテンプレートが削除されると、フィードは自動的に削除されます。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**&#x200B;をクリックします。

1. 削除する各フィードの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。
