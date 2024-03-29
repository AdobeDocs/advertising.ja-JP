---
title: 通知について
description: 様々なタイプやカテゴリを含む通知について説明します。
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 955f19647d49c31f70b8ec574734b44a9b490d52
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# 通知について

*ベータ版機能*

異なる種類のアラートを購読または購読解除するように、通知設定を構成できます。 通知は、次のいずれかの方法で表示できます。

* 次から： [!UICONTROL Notifications] パネル（のメインメニューから利用可能） ![通知](/help/search-social-commerce/assets/notifications-panel.png "通知").

* 送信者 [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* から [!UICONTROL Notification Center] 開く web アプリケーション [!UICONTROL Notification Center] を使用して、Search、Social、および Commerce 以外の別のウィンドウに表示します。

  アプリケーションは、通常のブラウザーバージョンよりも高速に読み込まれ、自動的に更新されます。 アプリケーションをインストールし、ブラウザーのアプリマネージャーを使用して管理できます。

* プッシュ通知からブラウザーに送信します。

  プッシュ通知を有効にすると、ブラウザーの通知規則に従って通知が表示されます。

通知の表示、通知の既読または未読としてのマーク、通知の削除を行うことができます。

## 通知タイプ

* **[!UICONTROL Notices]**：リリース、ダウンタイム、その他の変更管理に関する注意事項。

* **[!UICONTROL Recommendations]**：パフォーマンスを向上させ、ベストプラクティスを実装するために特定されたオポチュニティ。

* **[!UICONTROL Warnings]**：注意が必要ですが、最適化や管理にとって重要でない問題。

* **[!UICONTROL Issues]**：すぐに対処する必要がある重要な問題。 アカウント認証エラー通知が含まれます。

## 通知カテゴリ

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: [バルクシート操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) が完了したか、失敗しました。

   * **[!UICONTROL Manager Account Missing]**:Search、Social、および Commerce に関する通知に、 [ad network manager アカウント](/help/search-social-commerce/admin/manager-accounts.md)：重要な関数を正しく設定するために必要です。

   * **[!UICONTROL UI Actions]**：バックグラウンドで実行されたジョブが完了した、または失敗したことを示す通知。 ジョブタイプには以下が含まれます。 [バルクシートジョブ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、データテーブル内のジョブ、またはユーザーインターフェイス内のツールバー、エンティティ割り当てジョブ、その他のアクション（広告ネットワークとの同期、行の貼り付け、エンティティの名前変更など）を使用して、ジョブを一括編集できます。 エンティティの割り当てには、 [ラベル分類値](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) 任意のエンティティに対して、キャンペーンをポートフォリオに割り当て、ポートフォリオに制約を割り当てたり、割り当てを解除したりします。<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：クローズ済みベータ版に使用されます。

      * **[!UICONTROL File Upload to Cloud Storage]**：クローズ済みベータ版に使用されます。

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：検索、ソーシャル、コマースで [広告ネットワークアカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) 無効な資格情報、無効な認証トークン、または期限切れの認証トークンが原因です。

      * **[!UICONTROL Account Missing]**:Search、Social、および Commerce に関する通知に、 [広告ネットワークアカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]**：検索、ソーシャル、コマースが [ad network manager アカウント](/help/search-social-commerce/admin/manager-accounts.md) 無効な資格情報、無効な認証トークン、または期限切れの認証トークンが原因です。

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); or it's overridden at a lower level by an incorrect value.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**：通知 [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) が完了したか、失敗しました。

   * **[!UICONTROL Custom Alerts]**：通知 [アラートインスタンス](/help/search-social-commerce/alerts/alert-about.md) は、アラートテンプレートに対してトリガーされました。

   * **[!UICONTROL Reports]**: [カスタムレポートまたは予定レポート](/help/search-social-commerce/reports/report-about.md) が完了したか、失敗しました。

   * **[!UICONTROL Spreadsheet Feeds]**: [スプレッドシートフィード](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) が完了したか、失敗しました。

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
>* [通知を表示する](notification-view.md)
>* [通知を既読または未読としてマーク](notification-mark-read-unread.md)
>* [通知の削除](notification-delete.md)
>* [通知設定を編集](notification-edit.md)
>* [次のプッシュ通知を有効/無効にする： [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [をインストールしてアンインストールします。 [!UICONTROL Notification Center] web アプリケーション](notification-app-install-uninstall.md)
