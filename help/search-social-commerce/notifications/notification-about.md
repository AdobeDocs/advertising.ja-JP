---
title: 通知について
description: 様々なタイプやカテゴリを含む通知について説明します。
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
TQID: https://experienceleague.adobe.com/5WmRMJeZPQ8QDsgwRV0s1-50lkIr0LZqzPo2Ttv7kns
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 0%

---

# 通知について

*Beta機能*

様々な種類のアラートを購読または購読解除するように通知設定を設定できます。 通知は、次のいずれかの方法で表示できます。

* [!UICONTROL Notifications]通知![通知](/help/search-social-commerce/assets/notifications-panel.png "のメインメニューから使用できる") パネルから。

* [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta]から。

* Search, Social, &amp; Commerce以外の別のウィンドウで[!UICONTROL Notification Center]を開く[!UICONTROL Notification Center] Web アプリケーションから。

  アプリケーションは通常のブラウザーバージョンよりも高速に読み込まれ、自動的に更新されます。 アプリケーションをインストールし、ブラウザーのアプリマネージャーを使用して管理できます。

* プッシュ通知からブラウザーへ。

  プッシュ通知を有効にすると、プッシュ通知はブラウザーの通知規則に従って表示されます。

通知を表示したり、通知を既読または未読としてマークしたり、通知を削除したりできます。

## 通知タイプ

* **[!UICONTROL Notices]**: リリース、ダウンタイム、その他の変更管理に関する通知。

* **[!UICONTROL Recommendations]**: パフォーマンスを改善したり、ベストプラクティスを実装したりするために特定された機会です。

* **[!UICONTROL Warnings]**：注意が必要ですが、最適化または管理に重要ではない問題。

* **[!UICONTROL Issues]**：直ちに対処する必要がある重大な問題。 アカウント認証エラー通知が含まれます。

## 通知カテゴリ

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: [&#x200B; バルクシート操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)が完了または失敗したことを通知します。

   * **[!UICONTROL Manager Account Missing]**: Search, Social, &amp; Commerceに[ad network manager アカウント &#x200B;](/help/search-social-commerce/admin/manager-accounts.md)の資格情報が欠落していることを知らせる通知。重要な機能を正しく設定するために必要です。

   * **[!UICONTROL UI Actions]**：バックグラウンドで実行されたジョブが完了または失敗したことを通知します。 ジョブタイプには、[&#x200B; バルクシートジョブ &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、データテーブル内の一括編集ジョブ、またはツールバー、エンティティ割り当てジョブ、ユーザーインターフェイス内のその他のアクション（広告ネットワークとの同期、行のペースト、エンティティの名前の変更など）が含まれます。 エンティティの割り当ては、任意のエンティティに[&#x200B; ラベル分類値](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)を割り当てまたは割り当て解除すること、ポートフォリオにキャンペーンを割り当てること、ポートフォリオに制約を割り当てまたは割り当て解除することを含みます。<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：クローズド ベータ版に使用

      * **[!UICONTROL File Upload to Cloud Storage]**：クローズド ベータ版に使用

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：資格情報が無効であるか、認証トークンが無効または期限切れであることが原因で、Search, Social, &amp; Commerceが[ad network account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)にアクセスできなかったことを知らせる通知。

      * **[!UICONTROL Account Missing]**: Search, Social, &amp; Commerceに[広告ネットワークアカウント &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)の資格情報が欠落していることを知らせる通知。

      * **[!UICONTROL Manager Account Auth Error]**：資格情報が無効であるか、認証トークンが無効または期限切れであることが原因で、Search, Social, &amp; Commerceが[ad network manager アカウント &#x200B;](/help/search-social-commerce/admin/manager-accounts.md)と同期できなかった通知。

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md)が完了または失敗したことを通知します。

   * **[!UICONTROL Custom Alerts]**: アラートテンプレートに対して[&#x200B; アラートインスタンス &#x200B;](/help/search-social-commerce/alerts/alert-about.md)がトリガーされたという通知。

   * **[!UICONTROL Reports]**: [&#x200B; カスタムレポートまたはスケジュール済みレポート &#x200B;](/help/search-social-commerce/reports/report-about.md)が完了または失敗したことを通知します。

   * **[!UICONTROL Spreadsheet Feeds]**: [&#x200B; スプレッドシート フィード &#x200B;](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)が完了または失敗したことを通知します。

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [通知を表示](notification-view.md)
>* [通知を既読または未読としてマーク &#x200B;](notification-mark-read-unread.md)
>* [通知を削除](notification-delete.md)
>* [通知設定を編集](notification-edit.md)
>* [&#x200B; プッシュ通知を[!UICONTROL Notification Center]](notifications-push-enable-disable.md)から有効または無効にする
>* [Web アプリケーション [!UICONTROL Notification Center]をインストールしてアンインストールする](notification-app-install-uninstall.md)
