---
title: レポートの初期設定タスク
description: レポートで指標を利用できるようにする方法と、レポートを自動化する方法について説明します。
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
TQID: https://experienceleague.adobe.com/N50b-O0oFBV6ZMXcFx8gRvLs3M1hN696d43VGlgkg44
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# レポートの初期設定タスク

新規ユーザーは、次の初期設定タスクを実行する必要があります。

* Adobe Advertisingが広告主に対してトラッキングしているコンバージョン指標をレポートやその他のビュー[で使用できるようにし、オプションで](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)読みやすくするために列見出しに表示されているコンバージョン指標[ （/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md）の名前を任意に変更します。]

  トランザクションプロパティは、特に使用可能にしない限り、レポートでは使用できません。

  後で新しいコンバージョン指標の追跡を開始する場合は、このタスクを繰り返す必要があります。

* （オプション）レポート生成の自動化：

   * 先週または過去30日間の[!UICONTROL Campaign Report]など、特定の時間増分のレポートデータを定期的に生成する場合は、[&#x200B; レポートテンプレート &#x200B;](/help/search-social-commerce/reports/automation/templates/template-about.md)を設定し、毎日または特定の曜日または月に実行するようにスケジュールできます。 レポートの実行スケジュールが設定されるたびに、新しいレポートが生成されます。 [で設定された[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)通知設定に基づいて、レポートが完了したときに、特定のSearch、Social、およびCommerce ユーザーの電子メールアドレスに通知するオプションがあります。

   * カスタム形式のスプレッドシートで最新の日次レポートデータを表示し、ピボットテーブルの有無にかかわらず、さらに計算を実行するために必要な追加の列を表示する場合は、日次[&#x200B; スプレッドシートのフィード &#x200B;](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)を設定できます。 スプレッドシートフィードは、最新のパフォーマンスデータを使用して毎日更新され、以前の日付のデータを引き続き保持します。 スプレッドシート フィードを設定するには、まず[!DNL Microsoft Excel]でカスタマイズされたスプレッドシート テンプレートを作成する必要があります。 [で設定された[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)通知設定に基づいて、フィード ファイルが利用可能になったときに、特定のSearch、Social、およびCommerce ユーザーの電子メールアドレスに通知するオプションがあります。

   * FTPの場所で基本レポートと詳細レポートを受け取る場合は、FTP アカウントをリクエストし、特定の命名規則を使用してレポートテンプレートを設定することで、[基本レポートと詳細レポート &#x200B;](/help/search-social-commerce/reports/automation/ftp-reports.md)へのFTP アクセスを設定できます。

>[!MORELIKETHIS]
>
>* [&#x200B; レポートについて](report-about.md)
>* [&#x200B; レポートに使用されるデータ &#x200B;](data-used-for-reports.md)
