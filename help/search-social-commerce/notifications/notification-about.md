---
title: 通知について
description: 様々なタイプやカテゴリなど、通知について説明します。
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# 通知について

*Beta機能*

様々なタイプのアラートを購読または購読解除するように、通知設定を設定できます。 通知は、次のいずれかの方法で表示できます。

* ![&#x200B; 通知 &#x200B;](/help/search-social-commerce/assets/notifications-panel.png " 通知 ") のメインメニューから使用できる [!UICONTROL Notifications] パネルから。

* [!UICONTROL Insights & Reports]/[!UICONTROL Notification Center Beta] から。

* 検索、ソーシャル、Commerce以外の別のウィンドウで [!UICONTROL Notification Center] を開く [!UICONTROL Notification Center] Web アプリケーションから。

  このアプリケーションは、通常のブラウザーバージョンよりも高速に読み込まれ、自動的に更新されます。 アプリケーションをインストールし、ブラウザーのアプリマネージャーを使用して管理できます。

* プッシュ通知からブラウザーへ。

  プッシュ通知を有効にすると、ブラウザーの通知規則に従って表示されます。

通知を表示したり、通知を既読または未読としてマークしたり、通知を削除したりできます。

## 通知タイプ

* **[!UICONTROL Notices]**: リリース、ダウンタイムおよびその他の変更管理通知。

* **[!UICONTROL Recommendations]**：パフォーマンスの向上、ベストプラクティスの実装などを目的とした機会が特定されました。

* **[!UICONTROL Warnings]**：注意が必要だが、最適化や管理にとって重要ではない問題。

* **[!UICONTROL Issues]**：即時対応が必要な重大な問題。 アカウント認証エラー通知が含まれています。

## 通知カテゴリ

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: [&#x200B; バルクシート操作 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) が完了または失敗したことを示す通知。

   * **[!UICONTROL Manager Account Missing]**：検索、ソーシャル、Commerceに、重要な機能を正しく設定するために必要な [ad network manager アカウント &#x200B;](/help/search-social-commerce/admin/manager-accounts.md) の資格情報が欠落しているという通知。

   * **[!UICONTROL UI Actions]**：バックグラウンドで実行されるジョブが完了または失敗したことを示す通知。 ジョブタイプには、[&#x200B; バルクシートジョブ &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、データテーブル内の一括編集ジョブ、ツールバーを使用した一括編集ジョブ、エンティティ割り当てジョブ、ユーザーインターフェイス内のその他のアクション（広告ネットワークとの同期、行の貼り付け、エンティティの名前変更など）が含まれます。 エンティティの割り当てには、任意のエンティティへの [&#x200B; ラベル分類値 &#x200B;](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) の割り当てまたは割り当て解除、ポートフォリオへのキャンペーンの割り当て、ポートフォリオへの制約の割り当てまたは割り当て解除が含まれます。<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：クローズドベータ版に使用

      * **[!UICONTROL File Upload to Cloud Storage]**：クローズドベータ版に使用

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：資格情報が無効であるか、認証トークンが無効または期限切れのため、検索、ソーシャル、Commerceが [&#128279;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)ad network account にアクセスできなかったことを示す通知。

      * **[!UICONTROL Account Missing]**：検索、ソーシャル、Commerceに [ad ネットワークアカウント &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) の資格情報がないという通知。

      * **[!UICONTROL Manager Account Auth Error]**：資格情報が無効であるか、認証トークンが無効または期限切れのため、検索、ソーシャル、Commerceが [&#128279;](/help/search-social-commerce/admin/manager-accounts.md)ad network manager アカウント  と同期できなかったことを示す通知。

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) が完了または失敗した通知。

   * **[!UICONTROL Custom Alerts]**：アラートテンプレートに対して [&#x200B; アラートインスタンス &#x200B;](/help/search-social-commerce/alerts/alert-about.md) がトリガーされた通知。

   * **[!UICONTROL Reports]**: [&#x200B; カスタムレポートまたは予定レポート &#x200B;](/help/search-social-commerce/reports/report-about.md) が完了または失敗したことを示す通知。

   * **[!UICONTROL Spreadsheet Feeds]**: [&#x200B; スプレッドシートフィード &#x200B;](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) が完了または失敗したことを示す通知。

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
>* [&#x200B; 通知の表示 &#x200B;](notification-view.md)
>* [&#x200B; 通知を既読または未読としてマーク &#x200B;](notification-mark-read-unread.md)
>* [&#x200B; 通知の削除 &#x200B;](notification-delete.md)
>* [&#x200B; 通知設定の編集 &#x200B;](notification-edit.md)
>* [[!UICONTROL Notification Center]](notifications-push-enable-disable.md) からのプッシュ通知の有効化と無効化
>* [[!UICONTROL Notification Center] Web アプリケーションをインストールしてアンインストールする &#x200B;](notification-app-install-uninstall.md)
