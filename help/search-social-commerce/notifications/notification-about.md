---
title: 通知について
description: 様々なタイプやカテゴリを含む通知について説明します。
exl-id: a21dae13-b948-48e0-922a-d865f86e72f8
source-git-commit: f3cc5ffae0d5d19c8542a46ffdb49478efa14522
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 通知について

*ベータ版機能*

異なる種類のアラートを購読または購読解除するように、通知設定を構成できます。 通知は、次のいずれかの方法で表示できます。

* 次の [!UICONTROL Notifications] パネル ( ![通知](/help/search-social-commerce/assets/notifications-panel.png "通知").

* 送信者 [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* から [!UICONTROL Notification Center] 開く web アプリケーション [!UICONTROL Notification Center] を使用して、Search、Social、および Commerce 以外の別のウィンドウに表示します。

  アプリケーションは、通常のブラウザーバージョンよりも高速に読み込まれ、自動的に更新されます。 アプリケーションをインストールし、ブラウザーのアプリマネージャーを使用して管理できます。

* プッシュ通知からブラウザーに送信します。

  プッシュ通知を有効にすると、ブラウザーの通知規則に従って通知が表示されます。

通知の表示、通知の既読または未読としてのマーク、通知の削除を行うことができます。

## 通知タイプ

* **[!UICONTROL Notices]**:リリース、ダウンタイム、その他の変更管理に関する注意事項。

* **[!UICONTROL Recommendations]**:パフォーマンスの向上、ベストプラクティスの実装などを実現するオポチュニティを特定。

* **[!UICONTROL Warnings]**:注意を払う必要があるが、最適化や管理にとって重要でない問題。

* **[!UICONTROL Issues]**:すぐに注意を払う必要のある重大な問題。 アカウント認証エラー通知が含まれます。

## 通知カテゴリ

* [!UICONTROL Campaign Management]

   * **[!UICONTROL UI Actions]**:バックグラウンドで実行されたジョブが完了した、または失敗したことを示す通知。 ジョブタイプには以下が含まれます [バルクシートジョブ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)、データテーブル内のジョブ、またはユーザーインターフェイス内のツールバー、エンティティ割り当てジョブ、その他のアクション（広告ネットワークとの同期、行の貼り付け、エンティティの名前変更など）を使用して、ジョブを一括編集できます。 エンティティの割り当てには、 [ラベル分類値](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) 任意のエンティティに対して、キャンペーンをポートフォリオに割り当て、ポートフォリオに制約を割り当てたり、割り当てを解除したりします。<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * **[!UICONTROL Bulksheets]**:通知 [バルクシート操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) が完了したか、失敗しました。

   * **[!UICONTROL Manager Account Missing]**:検索、ソーシャル、コマースに次の項目の資格情報がない場合の通知： [ad network manager アカウント](/help/search-social-commerce/admin/manager-accounts.md)：重要な関数を正しく設定するためのものです。

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect s_kwcid template; or it's overridden at a lower level by an incorrect value.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are for the correct setup of critical functions.
  -->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Manager Account Auth Error]**:検索、ソーシャル、コマースが [ad network manager アカウント](/help/search-social-commerce/admin/manager-accounts.md) 認証トークンが無効か、無効か期限切れです。

      * **[!UICONTROL Account Auth Error]**:検索、ソーシャル、コマースで [広告ネットワークアカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) 認証トークンが無効か、無効か期限切れです。

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**:クローズドベータ版に使用

      * **[!UICONTROL File Upload to Cloud Storage]**:クローズドベータ版に使用

<!--
* [!UICONTROL Optimization]
-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Custom Alerts]**:通知 [アラートインスタンス](/help/search-social-commerce/alerts/alert-about.md) は、アラートテンプレートに対してトリガーされました。

   * **[!UICONTROL Spreadsheet Feeds]**:通知 [スプレッドシートフィード](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) が完了したか、失敗しました。

   * **[!UICONTROL Reports]**:通知 [カスタムレポートまたは予定レポート](/help/search-social-commerce/reports/report-about.md) が完了したか、失敗しました。

   * **[!UICONTROL Advertising Insights]**:通知 [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) が完了したか、失敗しました。

<!--
* [!UICONTROL System]
-->

>[!MORELIKETHIS]
>
>* [通知を表示する](notification-view.md)
>* [通知を既読または未読としてマーク](notification-mark-read-unread.md)
>* [通知の削除](notification-delete.md)
>* [通知設定を編集](notification-edit.md)
>* [次のプッシュ通知を有効/無効にする： [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [をインストールしてアンインストールします。 [!UICONTROL Notification Center] web アプリケーション](notification-app-install-uninstall.md)
