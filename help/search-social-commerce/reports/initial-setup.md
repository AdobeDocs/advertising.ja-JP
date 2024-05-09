---
title: レポートの初期設定タスク
description: レポートで指標を使用できるようにする方法と、レポートを自動化する方法について説明します。
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# レポートの初期設定タスク

新規ユーザーは、次の初期設定タスクを実行する必要があります。

* 広告主がAdobe Advertisingでトラッキングしているコンバージョン指標を作成します [レポートおよび他のビューで使用可能](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)、および（オプション） [いずれかのコンバージョン指標の名前を変更します]（読みやすくするために列見出しに表示される/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md。

  トランザクションプロパティは、特に指定しない限り、レポートでは使用できません。

  後で新しいコンバージョン指標の追跡を開始する場合は、このタスクを繰り返す必要があります。

* （オプション）レポート生成の自動化：

   * レポートデータを、特定の時間だけ定期的に生成する場合（例：） [!UICONTROL Campaign Report] 過去 1 週間または過去 30 日間は、以下を設定できます [レポートテンプレート](/help/search-social-commerce/reports/automation/templates/template-about.md) また、毎日または特定の曜日または月に実行するようにスケジュール設定できます。 レポートの実行がスケジュールされるたびに、新しいレポートが生成されます。 に基づいて、レポートが完了したら、特定の検索、ソーシャル、Commerce ユーザーのメールアドレスに通知するオプションがあります [で設定された通知設定 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * ピボット・テーブルおよび追加の列を含むかどうかにかかわらず、カスタム書式のスプレッドシートで最新の日次レポート・データを表示する場合は、さらに計算を実行する必要があります [スプレッドシートフィード](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). スプレッドシートフィードは、最新のパフォーマンスデータで毎日更新され、以前の日付のデータが引き続き保持されます。 スプレッドシートフィードを設定するには、まず、でカスタマイズされたスプレッドシートテンプレートを作成する必要があります [!DNL Microsoft Excel]. に基づいて、フィードファイルが使用可能な場合、特定の検索、ソーシャル、Commerceユーザーのメールアドレスに通知するオプションがあります [で設定された通知設定 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * FTP の場所で基本レポートや高度なレポートを受信する場合は、次のように設定できます [基本レポートおよび高度なレポートへの FTP アクセス](/help/search-social-commerce/reports/automation/ftp-reports.md) ftp アカウントを要求し、特定の命名規則を使用してレポートテンプレートを設定する

>[!MORELIKETHIS]
>
>* [レポートについて](report-about.md)
>* [レポートに使用するデータ](data-used-for-reports.md)
