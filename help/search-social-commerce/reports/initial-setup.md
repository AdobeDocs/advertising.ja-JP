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

* Adobe Advertisingが広告主に対してトラッキングしているコンバージョン指標 [&#x200B; レポートやその他のビューで使用できます &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) を設定し、必要に応じて、列見出しに表示されている [ 任意のコンバージョン指標の名前を変更 ] （/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md）を読みやすくします。

  トランザクションプロパティは、特に指定しない限り、レポートでは使用できません。

  後で新しいコンバージョン指標の追跡を開始する場合は、このタスクを繰り返す必要があります。

* （オプション）レポート生成の自動化：

   * 先週や過去 30 日間の [!UICONTROL Campaign Report] など、特定の増分で定期的にレポートデータを生成する場合は、[&#x200B; レポートテンプレート &#x200B;](/help/search-social-commerce/reports/automation/templates/template-about.md) を設定し、毎日または週や月の特定の日に実行するようにスケジュールできます。 レポートの実行がスケジュールされるたびに、新しいレポートが生成されます。 [!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/notifications/notification-about.md) で設定された notification 設定に基づいて、レポートが完了したら、特定の検索、ソーシャル、Commerceのユーザーのメールアドレスに通知することができます。

   * カスタム・フォーマットのスプレッドシートに最新の日次レポート・データを表示する場合、ピボット・テーブルおよび追加の列の有無にかかわらず、さらに計算を実行する必要がある場合は、日次 [&#x200B; スプレッドシート・フィード &#x200B;](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) を設定できます。 スプレッドシートフィードは、最新のパフォーマンスデータで毎日更新され、以前の日付のデータが引き続き保持されます。 スプレッドシートフィードを設定するには、まず [!DNL Microsoft Excel] でカスタマイズされたスプレッドシートテンプレートを作成する必要があります。 [!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/notifications/notification-about.md) で設定された notification 設定に基づいて、フィードファイルが使用可能な場合、特定の検索、ソーシャル、Commerceユーザーのメールアドレスに通知するオプションがあります。

   * FTP の場所で基本レポートや高度なレポートを受信する場合は、FTP アカウントを要求し、特定の命名規則を使用してレポートテンプレートを設定することで、基本レポートや高度なレポートへの [FTP アクセス &#x200B;](/help/search-social-commerce/reports/automation/ftp-reports.md) を設定できます。

>[!MORELIKETHIS]
>
>* [&#x200B; レポートについて &#x200B;](report-about.md)
>* [&#x200B; 報告書に用いるデータ &#x200B;](data-used-for-reports.md)
