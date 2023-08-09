---
title: レポートの初期設定タスク
description: レポートで指標を使用できるようにする方法と、レポートを自動化する方法について説明します。
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# レポートの初期設定タスク

新規ユーザーは、次の初期設定タスクを実行する必要があります。

* 広告主のためにAdobe Advertisingが追跡しているコンバージョン指標の作成 [レポートおよび他のビューで使用可能](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)（オプション） [任意のコンバージョン指標の名前を変更する](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) を読みやすくするために、列見出しに表示されます。

  トランザクションプロパティは、特に使用可能にしない限り、レポートでは使用できません。

  後で新しいコンバージョン指標の追跡を開始する場合は、このタスクを繰り返す必要があります。

* （オプション）レポート生成の自動化：

   * 特定の時間の増分に合わせてレポートデータを定期的に生成する場合 ( [!UICONTROL Campaign Report] 過去 1 週間または過去 30 日間、 [レポートテンプレート](/help/search-social-commerce/reports/automation/templates/template-about.md) また、毎日または特定の曜日または月の特定の日に実行するようにスケジュールします。 レポートの実行がスケジュールされるたびに、新しいレポートが生成されます。 レポートが完成したときに、 [で設定された通知設定 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 日次レポートの最新データをカスタム書式のスプレッドシートで表示する場合は、ピボットテーブルと追加の計算を行う必要がある列があるかどうかに関わらず、日次レポートを設定できます [スプレッドシートフィード](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). スプレッドシートフィードは、最新のパフォーマンスデータで毎日更新され、引き続き以前の日付のデータが保持されます。 スプレッドシートフィードを設定するには、まず [!DNL Microsoft Excel]. フィードファイルが使用可能になったとき、電子メールアドレスに対して、 [で設定された通知設定 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * FTP の場所で基本レポートと高度なレポートを受け取る場合は、 [基本レポートと高度なレポートへの FTP アクセス](/help/search-social-commerce/reports/automation/ftp-reports.md) FTP アカウントをリクエストし、特定の命名規則を使用してレポートテンプレートを設定する。

>[!MORELIKETHIS]
>
>* [レポートについて](report-about.md)
>* [レポートに使用するデータ](data-used-for-reports.md)
