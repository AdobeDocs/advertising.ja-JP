---
title: スプレッドシートレポートフィードの設定
description: スプレッドシートフィードの設定について説明します。
exl-id: 9a7e0a21-5db4-4829-a191-cacaa51f6cb6
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# スプレッドシートレポートフィードの設定

| フィールド | 説明 |
|---|---|
| [!UICONTROL Feed Name] | スプレッドシートフィードの名前。 |
| [!UICONTROL Report Template] | 必要なレポートデータを指定するレポートテンプレート。 [!DNL Excel] テンプレート。 すべての基本レポートテンプレートが表示されます。<br><br><b>注意：</b> レポートに使用するレポートテンプレートを変更する場合、またはテンプレートの列を更新する場合は、新しい [!DNL Excel] テンプレート。 |
| [!UICONTROL Excel Template] | 特別な形式の [!DNL Excel] .XLSX 形式で作成したテンプレート。レポートテンプレートで指定されたデータに適用されます。 アップロードするファイルを指定します。その際には、フルパスとファイル名を入力するか、 <b>[!UICONTROL Browse]</b> をクリックして、お使いのデバイスまたはネットワーク上でファイルを見つけます。 |
| [!UICONTROL Back Fill From] | の既存のデータの開始日 [!UICONTROL RAW] タブが更新され、過去の日数で表されます。 最大 90 日の値を入力します。デフォルトは 7 日です。<br><br>例えば、値が 7 で、今日が 3 月 7 日の場合、 [!UICONTROL RAW] 3 月 1 日から始まるタブが更新されます ( [!UICONTROL Back Fill Until] パラメーター )。 3 月 1 日より前の日付のデータの既存の行は削除されませんが、更新されません。 |
| [!UICONTROL Back Fill Until] | の既存のデータの終了日 [!UICONTROL RAW] タブが更新され、過去の日数で表されます。 デフォルト値は 1 日です。<br><br>例えば、この値が 1 で、今日が 3 月 7 日の場合、 [!UICONTROL RAW] タブは、3 月 6 日まで ( 開始日が [!UICONTROL Back Fill From] パラメーター )。 この値が 1 の場合、 [!UICONTROL Back Fill Until] パラメーターが 7、今日が 3 月 7 日、 [!UICONTROL RAW] 「 」タブが 3 月 1 日から 3 月 6 日まで更新されます。 どちらの例でも、3 月 6 日以降の日付の既存のデータ行は削除されませんが、更新されません。 |
| [!UICONTROL Email Recipients] | レポートが更新されるたびに、またはテンプレートにスケジュールが含まれている場合にレポートが実行されるたびに、通知を送信する電子メールアドレス。 デフォルトでは、ユーザーアカウントのアドレスが入力されます。 複数のアドレスを指定する場合は、コンマ、スペース、または改行で区切ります。 |
| [!UICONTROL Schedule Time] | スプレッドシートフィードが更新される時間：08:00、または広告主のタイムゾーンの 10:00 ～ 23:00 の任意の時間。 新しいスプレッドシートフィードのデフォルトは 10:00 です。<br><br><b>注意：</b> パフォーマンス上の理由から、他のレポートが生成されている場合、09:00 にスプレッドシートフィードを更新することはできません。 |
| [!UICONTROL Email Notification] | （電子メール受信者が指定されている場合）指定されたアドレスへの電子メール通知に含める内容：<ul><li><i>フィードを添付</i>  — 完成したレポートのコピーを XLSX 形式で送信します。 ファイルが 10 MB を超える場合、通知には添付ファイルは含まれません。</li><li><i>通知のみ</i> （デフォルト）：レポートの完了または失敗の通知のみを送信し、レポートへのリンクを含めます。</li></ul> |

>[!MORELIKETHIS]
>
>* [スプレッドシートレポートフィードについて](spreadsheet-feed-about.md)
>* [スプレッドシートレポートフィードの作成](spreadsheet-feed-create.md)
>* [の作成 [!DNL Excel] スプレッドシートレポートフィードのテンプレート](spreadsheet-feed-create-excel-template.md)
>* [スプレッドシートレポートフィード設定の編集](spreadsheet-feed-edit.md)
>* [スプレッドシートレポートフィードファイルの表示または保存](spreadsheet-feed-view-or-save.md)
>* [スプレッドシートレポートフィードを手動で更新](spreadsheet-feed-refresh.md)
>* [スプレッドシートレポートフィードの削除](spreadsheet-feed-delete.md)
