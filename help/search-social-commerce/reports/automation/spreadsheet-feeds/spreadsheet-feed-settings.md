---
title: スプレッドシートレポートフィードの設定
description: スプレッドシート フィードの設定について説明します。
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# スプレッドシートレポートフィードの設定

| フィールド | 説明 |
|---|---|
| [!UICONTROL Feed Name] | スプレッドシートフィードの名前。 |
| [!UICONTROL Report Template] | 必要なレポートデータを指定するレポートテンプレート。レポートテンプレートの作成に使用したレポー [!DNL Excel] テンプレートを選択します。 すべての基本レポートテンプレートが表示されます。<br><br><b> 注意：</b> レポートに使用するレポート・テンプレートを変更する場合、またはテンプレート内の列を更新する場合は、新しい [!DNL Excel] レポート・テンプレートを作成してアップロードする必要があります。 |
| [!UICONTROL Excel Template] | .XLSX 形式で作成した特別にフォーマットされた [!DNL Excel] テンプレート。レポートテンプレートで指定されたデータに適用されます。 フルパスとファイル名を入力するか、「<b>[!UICONTROL Browse]</b>」をクリックしてデバイスまたはネットワーク上のファイルを探し、アップロードするファイルを指定します。 |
| [!UICONTROL Back Fill From] | 「[!UICONTROL RAW]」タブ上の既存のデータが更新される開始日（過去の日数で表されます）。 90 日までの値を入力します。デフォルトは 7 日です。<br><br> 例えば、値が 7 で、今日が 3 月 7 日である場合、3 月 1 日から始まる [[!UICONTROL RAW]] タブの既存のデータが（[!UICONTROL Back Fill Until] パラメーターで指定された終了日まで）更新されます。 3 月 1 日より前の日付の既存のデータ行は削除されませんが、更新はされません。 |
| [!UICONTROL Back Fill Until] | 「[!UICONTROL RAW]」タブの既存のデータが更新される終了日（過去の日数で表されます）。 デフォルト値は 1 日です。<br><br> 例えば、この値が 1 で、今日が 3 月 7 日である場合、「[!UICONTROL RAW]」タブの既存のデータは 3 月 6 日（[!UICONTROL Back Fill From] パラメーターで指定された開始日から始まる）まで更新されます。 この値が 1 で、[!UICONTROL Back Fill Until] のパラメーターが 7 で、今日が 3 月 7 日の場合、[!UICONTROL RAW] タブの既存のデータは 3 月 1 日から 3 月 6 日に更新されます。 どちらの例でも、3 月 6 日（PT）以降の日付の既存のデータ行は削除されませんが、更新されません。 |
| [!UICONTROL Email Recipients] | レポートが更新されるたびに、またはテンプレートにスケジュールが含まれている場合にレポートが実行されるたびに通知を送信するメールアドレス。 デフォルトでは、ユーザーアカウントのアドレスが入力されます。 複数のアドレスを指定する場合は、コンマ、スペース、改行で区切ります。 |
| [!UICONTROL Schedule Time] | スプレッドシートフィードが更新される時間。08:00 か、広告主のタイムゾーンの 10:00 ～ 23:00 の任意の時間です。 新しいスプレッドシートフィードのデフォルトは 10:00 です。<br><br><b> 注意：</b> パフォーマンス上の理由から、他のレポートの生成時に 09:00 にスプレッドシートフィードを更新することはできません。 |
| [!UICONTROL Email Notification] | （メールの受信者を指定した場合）指定したアドレスへのメール通知に含める内容：<ul><li><i> フィードを添付 </i> — XLSX 形式で完成したレポートのコピーを送信します。 ファイルが 10 MB を超える場合、通知に添付ファイルは含まれません。</li><li><i> 通知のみ </i> （デフォルト） – レポートへのリンクを含む、レポートの完了または失敗の通知のみを送信します。</li></ul> |

>[!MORELIKETHIS]
>
>* [ スプレッドシートレポートフィードについて ](spreadsheet-feed-about.md)
>* [ スプレッドシートレポートフィードの作成 ](spreadsheet-feed-create.md)
>* [ スプレッドシートレポ  [!DNL Excel]  トフィード用のテンプレートの作成 ](spreadsheet-feed-create-excel-template.md)
>* [ スプレッドシートレポートフィード設定の編集 ](spreadsheet-feed-edit.md)
>* [ スプレッドシートレポートフィードファイルの表示または保存 ](spreadsheet-feed-view-or-save.md)
>* [ スプレッドシートレポートフィードを手動で更新 ](spreadsheet-feed-refresh.md)
>* [ スプレッドシートレポートフィードの削除 ](spreadsheet-feed-delete.md)
