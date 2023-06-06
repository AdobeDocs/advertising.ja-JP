---
title: レポートの初期設定タスク
description: レポートで指標を使用できるようにする方法と、レポートを自動化する方法について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# レポートの初期設定タスク

新規ユーザーは、次の初期設定タスクを実行する必要があります。

* 広告主に対してAdobe広告がトラッキングしているトランザクションプロパティの作成 [レポートおよび他のビューで使用可能](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md)（オプション） [プロパティ名の名前を変更する](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 列見出しに表示され、読みやすくなります。

   トランザクションプロパティは、特に使用可能にしない限り、レポートでは使用できません。

   後で新しいトランザクションプロパティの追跡を開始する場合は、このタスクを繰り返す必要があります。

* （オプション）レポート生成の自動化：

   * 特定の時間の増分に合わせてレポートデータを定期的に生成する場合 ( [!UICONTROL Campaign Report] 過去 1 週間または過去 30 日間、 [レポートテンプレート](/help/search-social-commerce/reports/automation/templates/template-about.md) また、毎日または特定の曜日または月の特定の日に実行するようにスケジュールします。 レポートの実行がスケジュールされるたびに、新しいレポートが生成されます。 レポートが完成したら、 [通知設定 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 日次レポートの最新データをカスタム書式のスプレッドシートで表示する場合は、ピボットテーブルと追加の計算を行う必要がある列の有無を問わず、日次レポートを設定できます [スプレッドシートフィード](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). スプレッドシートフィードは、最新のパフォーマンスデータで毎日更新され、引き続き以前の日付のデータが保持されます。 スプレッドシートフィードを設定するには、まず [!DNL Microsoft Excel]. フィードファイルが使用可能になったとき、電子メールアドレスに対して、 [通知設定 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * FTP の場所で基本レポートと高度なレポートを受け取る場合は、 [基本レポートと高度なレポートへの FTP アクセス](/help/search-social-commerce/reports/automation/ftp-reports.md) FTP アカウントをリクエストし、特定の命名規則を使用してレポートテンプレートを設定する。

>[!MORELIKETHIS]
>
>* [レポートについて](report-about.md)
>* [レポートに使用するデータ](data-used-for-reports.md)

