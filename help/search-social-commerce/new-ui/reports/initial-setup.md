---
title: （新しいUI）レポートの初期設定タスク
description: レポートで指標を利用できるようにする方法と、レポートを自動化する方法について説明します。
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# （新しいUI）レポートの初期設定タスク

新規ユーザーは、次の初期設定タスクを実行する必要があります。

* Adobe Advertisingが広告主向けにトラッキングしているコンバージョン指標をレポートやその他のビューで使用できるようにし、必要に応じて、列見出しに表示されるコンバージョン指標の名前を変更して読みやすくします。 「[広告主のコンバージョン指標の管理](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)」を参照してください。

  トランザクションプロパティは、特に使用可能にしない限り、レポートでは使用できません。

  後で新しいコンバージョン指標の追跡を開始する場合は、このタスクを繰り返す必要があります。

* （オプション）レポート生成の自動化：

   * 先週または過去30日間の[!UICONTROL Campaign Report]など、特定の時間増分のレポートデータを定期的に生成する場合は、[&#x200B; レポートテンプレート &#x200B;](report-templates-manage.md)を設定し、毎日または特定の曜日または月に実行するようにスケジュールできます。 レポートの実行スケジュールが設定されるたびに、新しいレポートが生成されます。 [!UICONTROL Notification Center]&rbrack;[Manage custom alerts] （/help/search-social-commerce/new-ui/notifications-manage.md）で設定された&lbrack;通知設定に基づいて、レポートが完了したときに、特定のSearch、Social、およびCommerce ユーザーの電子メールアドレスに通知するオプションがあります。

   * カスタム形式のスプレッドシートで最新の日次レポートデータを表示し、ピボットテーブルの有無にかかわらず、さらに計算を実行するために必要な追加の列を表示する場合は、日次[&#x200B; スプレッドシートのフィード &#x200B;](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)を設定できます。 スプレッドシートフィードは、最新のパフォーマンスデータを使用して毎日更新され、以前の日付のデータを引き続き保持します。 スプレッドシート フィードを設定するには、まず[!DNL Microsoft Excel]でカスタマイズされたスプレッドシート テンプレートを作成する必要があります。 [!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/new-ui/notifications-manage.md)で設定された通知設定に基づいて、フィード ファイルが利用可能になったときに、特定のSearch、Social、およびCommerce ユーザーの電子メールアドレスに通知するオプションがあります。

   * FTPの場所で基本レポートと詳細レポートを受け取る場合は、FTP アカウントをリクエストし、特定の命名規則を使用してレポートテンプレートを設定することで、[基本レポートと詳細レポート &#x200B;](/help/search-social-commerce/new-ui/reports/ftp-reports.md)へのFTP アクセスを設定できます。

>[!MORELIKETHIS]
>
>* [&#x200B; レポートについて](report-about.md)
>* [&#x200B; レポートに使用されるデータ &#x200B;](data-used-for-reports.md)
