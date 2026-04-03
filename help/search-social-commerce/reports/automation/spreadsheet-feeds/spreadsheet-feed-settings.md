---
title: スプレッドシートレポートフィード設定
description: スプレッドシート フィードの設定について説明します。
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
TQID: https://experienceleague.adobe.com/4JPflN5lVXkNf2nWszh-LznW2xNaMkQMGPOxo6Ac2WU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 0%

---

# スプレッドシートレポートフィード設定

| フィールド | 説明 |
|---|---|
| [!UICONTROL Feed Name] | スプレッドシート フィードの名前。 |
| [!UICONTROL Report Template] | 必要なレポートデータを指定するレポートテンプレートです。[!DNL Excel] テンプレートの作成に使用したレポートテンプレートを選択してください。 すべての基本レポートテンプレートが一覧表示されます。<br><br><b>注：</b> レポートに使用するレポートテンプレートを変更するか、テンプレートの列を更新した場合は、新しい[!DNL Excel] テンプレートを作成してアップロードする必要があります。 |
| [!UICONTROL Excel Template] | レポートテンプレートで指定されたデータに適用される.XLSX形式で作成した、特別に書式設定された[!DNL Excel] テンプレート。 アップロードするファイルを指定するには、フルパスとファイル名を入力するか、<b>[!UICONTROL Browse]</b>をクリックしてデバイスまたはネットワーク上のファイルを探します。 |
| [!UICONTROL Back Fill From] | [!UICONTROL RAW] タブ上の既存のデータが更新される開始日。過去の日数で表されます。 最大90日の値を入力します。デフォルトは7日です。<br><br>例えば、値が7で、今日が3月7日の場合、3月1日から始まる[!UICONTROL RAW] タブの既存のデータが更新されます（[!UICONTROL Back Fill Until] パラメーターで指定された終了日まで）。 3月1日より前の日付の既存のデータ行は削除されませんが、更新されません。 |
| [!UICONTROL Back Fill Until] | [!UICONTROL RAW] タブの既存のデータが更新される終了日。過去の日数で表されます。 デフォルト値は1日（1）です。<br><br>例えば、この値が1で、今日が3月7日の場合、[!UICONTROL RAW] タブの既存のデータは3月6日まで（および[!UICONTROL Back Fill From] パラメーターで指定された開始日から）更新されます。 この値が1で、[!UICONTROL Back Fill Until] パラメーターが7で、今日が3月7日の場合、[!UICONTROL RAW] タブの既存のデータは3月1日から3月6日の間に更新されます。 いずれの例でも、3月6日以降の日付の既存のデータ行は削除されませんが、更新されません。 |
| [!UICONTROL Email Recipients] | レポートが更新されるたびに、またはテンプレートにスケジュールが含まれている場合にレポートが実行されるたびに、通知を送信する電子メールアドレス。 デフォルトでは、ユーザーアカウントのアドレスが入力されます。 複数のアドレスを指定するには、コンマ、スペース、または新しい行で区切ります。 |
| [!UICONTROL Schedule Time] | スプレッドシート フィードが更新される時間：広告主のタイムゾーンの08:00または10:00 ～ 23:00の間の任意の時間。 新しいスプレッドシート フィードのデフォルトは10:00です。<br><br><b>注：</b> パフォーマンス上の理由から、他のレポートが生成される09:00時点でスプレッドシート フィードを更新することはできません。 |
| [!UICONTROL Email Notification] | （メール受信者が指定されている場合）指定されたアドレスへのメール通知に含めるもの：<ul><li><i> フィードを添付</i>  – 完成したレポートのコピーをXLSX形式で送信します。 ファイルが10 MBを超える場合、通知には添付ファイルは含まれません。</li><li><i>通知のみ</i> （デフォルト） – レポートへのリンクを含む、レポートの完了または失敗の通知のみを送信します。</li></ul> |

>[!MORELIKETHIS]
>
>* [&#x200B; スプレッドシート レポート フィードについて](spreadsheet-feed-about.md)
>* [&#x200B; スプレッドシート レポート フィードの作成](spreadsheet-feed-create.md)
>* [&#x200B; スプレッドシート レポート フィード用の [!DNL Excel]  テンプレートを作成](spreadsheet-feed-create-excel-template.md)
>* [&#x200B; スプレッドシート レポート フィード設定の編集](spreadsheet-feed-edit.md)
>* [&#x200B; スプレッドシート レポート フィード ファイルを表示または保存する](spreadsheet-feed-view-or-save.md)
>* [&#x200B; スプレッドシート レポート フィードを手動で更新する](spreadsheet-feed-refresh.md)
>* [&#x200B; スプレッドシート レポート フィードを削除](spreadsheet-feed-delete.md)
