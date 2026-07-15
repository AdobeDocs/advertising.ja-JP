---
title: （新しいUI）通知の管理
description: プッシュ通知やNotification Center web アプリケーションなど、Search、Social、およびCommerce通知を表示、設定、管理する方法について説明します。
feature: Search Notifications
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# （新しいUI）通知の管理

*Beta機能*

様々な種類のアラートを購読または購読解除するように通知設定を設定できます。 通知は、次のいずれかの方法で表示できます。

* ![通知](/help/search-social-commerce/assets/notifications.png "通知")の右上にある[!UICONTROL Notifications] パネルから。 パネルから、リストをフィルターしたり、通知設定を編集したり、[!UICONTROL Notification Center]を開いたりできます。

* Search, Social, &amp; Commerce以外の別のウィンドウで開く[!UICONTROL Notification Center]から。 [!UICONTROL Notifications] パネルから[!UICONTROL Notification Center]を開くには、**[!UICONTROL View All]**&#x200B;をクリックします。

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

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: [ バルクシート操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)が完了または失敗したことを通知します。<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**:Search、Social、およびCommerceに[ad network manager アカウント ](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)の資格情報が不足していることを知らせる通知。これは、重要な機能を正しく設定するために必要です。<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**：バックグラウンドで実行されたジョブが完了または失敗したことを通知します。 ジョブタイプには、[ バルクシートジョブ ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->、データテーブル内の一括編集ジョブ、またはツールバー、エンティティ割り当てジョブ、ユーザーインターフェイス内のその他のアクション（広告ネットワークとの同期、行のペースト、エンティティの名前の変更など）が含まれます。 エンティティの割り当ては、任意のエンティティに[ ラベル分類値](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)を割り当てたり割り当てを解除したり、キャンペーンをポートフォリオに割り当てたり、[入札制約をエンティティに割り当てたり割り当てを解除したりします](/help/search-social-commerce/new-ui/goals/constraints-manage.md)。

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: アカウント データ ファイルがアップロードされたか、アカウント データのアップロードに失敗したという通知が、[ アカウント データの手動アップロード ](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md)を介して送信されました。<!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**：アカウントデータファイルがアップロードされたか、アカウントデータのアップロードに失敗したという通知（[ アカウントデータを [!DNL Amazon] [!DNL S3] バケットにアップロード ](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md)経由）。<!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：資格情報が無効であるか、認証トークンが無効または期限切れであることが原因で、Search, Social, &amp; Commerceが[ad network account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)にアクセスできなかったことを知らせる通知。

      * **[!UICONTROL Account Missing]**: Search, Social, &amp; Commerceに[広告ネットワークアカウント ](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)の資格情報が欠落していることを知らせる通知。

      * **[!UICONTROL Manager Account Auth Error]**：無効な資格情報または無効または期限切れの認証トークンが原因で、Search, Social, &amp; Commerceが[ad network manager アカウント ](/help/search-social-commerce/admin/manager-accounts.md)と同期できなかったことを知らせる通知。<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md)が完了または失敗したことを通知します。

   * **[!UICONTROL Custom Alerts]**: アラートテンプレートに対して[ アラートインスタンス ](/help/search-social-commerce/new-ui/alerts-manage.md)がトリガーされたという通知。

   * **[!UICONTROL Spreadsheet Feeds]**: [ スプレッドシート フィード ](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)が完了または失敗したことを通知します。

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**：特定のビューからのデータビューレポート（[!UICONTROL Camapigns] ビューのデータテーブルの内容など）が完了または失敗したことの通知。

      * **[!UICONTROL Reports]**: [ カスタムレポートまたはスケジュール済みレポート ](/help/search-social-commerce/new-ui/reports/management/report-manage.md)が完了または失敗したことを通知します。

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**：日内最適化が無効になっている場合の通知。

      * **[!UICONTROL Simulation Report]**: [ シミュレーションジョブ ](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md)に関する通知。

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**: キャンペーンコンバージョン目標の自動割り当ての成功および失敗に関する広告主レベルの通知。

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**: キャンペーンコンバージョン目標の自動割り当ての成功および失敗に関するポートフォリオレベルの通知。

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**: [ ポートフォリオ一括編集ジョブに関する通知をバルクシート ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md)経由で送信します。

         * **[!UICONTROL Portfolio Settings]**: ポートフォリオ設定の[変更](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md)に関する通知。

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## 使用可能なアクション

* [通知を表示](#notification-view)

* [通知設定の編集](#notification-edit)

* [通知を既読または未読としてマーク](#notification-mark-read-unread)

* [通知の削除](#notification-delete)

* [プッシュ通知を有効または無効にする](#notification-push-enable-disable)

* [[!UICONTROL Notification Center] web アプリケーションをインストールしてアンインストールします](#notification-app-install-uninstall)

## 通知を表示 {#notification-view}

アカウント認証エラー、トリガーされるカスタムアラート、生成される[!UICONTROL Advertising Insights]に関する通知[購読している場合は、[!UICONTROL Notifications] パネルまたは[!UICONTROL Notification Center]で通知を表示できます。](#notification-edit)

### [!UICONTROL Notifications] パネル内の通知の表示

1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

1. （オプション）次のいずれかの操作を行います。

   * 通知の詳細を表示するには、通知名をクリックします。

     一部の通知では、[!UICONTROL Action Recommended] セクションに、影響を受けるエンティティまたは責任あるエンティティのフィルタービューを開くリンクが含まれている場合があります。

   * 通知を&#x200B;*読み取り*&#x200B;または&#x200B;*未読*&#x200B;としてマークするには、アラート名の上にカーソルを置き、![既読または未読としてマーク ](/help/search-social-commerce/assets/notifications-read-unread.png "既読または未読としてマーク ")をクリックします。

     *読み取り*&#x200B;とマークされた通知は、明るい色のテキストですが、削除するまで利用できます。

     ![読み取り/未読の通知](/help/search-social-commerce/assets/notifications-read-vs-unread.png "読み取り/未読の通知")

   * 通知タイプのサブスクリプション設定を変更するには、通知の横にある![設定](/help/search-social-commerce/assets/settings-nc.png "設定")をクリックし、設定を変更してから&#x200B;**[!UICONTROL Save]**&#x200B;をクリックします。

   * 通知を削除するには、通知の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

   * [!UICONTROL Notification Center]を開くには、**[!UICONTROL View All]**&#x200B;をクリックします。

### [!UICONTROL Notification Center]内の通知を表示

1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

1. **[!UICONTROL View All]**&#x200B;をクリックします。

1. （オプション）通知をタイプ別にフィルタリングするには、*[!UICONTROL Notices]、[!UICONTROL Recommendations]、[!UICONTROL Warnings]、または[!UICONTROL Issues]*&#x200B;をクリックします。

1. （オプション）次のいずれかの操作を行います。

   * 通知の詳細を表示するには、通知名をクリックします。

     一部の通知では、[!UICONTROL Action Recommended] セクションに、影響を受けるエンティティまたは責任あるエンティティのフィルタービューを開くリンクが含まれている場合があります。

   * 通知を&#x200B;*読み取り*&#x200B;または&#x200B;*未読*&#x200B;としてマークするには、アラート名の上にカーソルを置き、![既読または未読としてマーク ](/help/search-social-commerce/assets/notifications-read-unread.png "既読または未読としてマーク ")をクリックします。

     *読み取り*&#x200B;とマークされた通知は、明るい色のテキストですが、削除するまで利用できます。

   * 通知タイプのサブスクリプション設定を変更するには、通知の横にある![設定](/help/search-social-commerce/assets/settings-nc.png "設定")をクリックし、設定を変更してから&#x200B;**[!UICONTROL Save]**&#x200B;をクリックします。

   * 通知を削除するには、通知の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

## 通知設定の編集 {#notification-edit}

アカウント認証エラー、トリガーされるすべてのカスタムアラート、生成する[!UICONTROL Advertising Insights]の完了に関するメールおよびweb通知をオプションで購読または購読解除できます。

1. 次のいずれかの方法で通知設定を開きます。

   * 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックして、[!UICONTROL Notifications] パネルを開きます。 右上の「![設定](/help/search-social-commerce/assets/settings-nc.png "設定")」をクリックします。

   * 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックし、**[!UICONTROL View All]**」をクリックして[!UICONTROL Notification Center]を開き、左側のメニューで「![設定](/help/search-social-commerce/assets/settings-nc.png "設定")」をクリックします。

1. 上記の通知カテゴリの設定を変更します。

   * 通知を購読または購読解除するには、[!UICONTROL Subscribe]列のスライダーを移動します。

      * すべての通知タイプの購読を解除するには、スライダーを左（無効）に移動します。

      * 1つ以上の通知タイプを購読するには、スライダーを右（有効）に移動します。

   * （[!UICONTROL Subscribe]が有効になっている場合）電子メール通知を購読するには、**[!UICONTROL Email]**&#x200B;列のチェックボックスをオンにします。

   * （[!UICONTROL Subscribe]が無効になっている場合） Search, Social, &amp; Commerce内のweb通知を購読し、ブラウザーで有効になっている場合はプッシュ通知を行うには、**[!UICONTROL Web]**&#x200B;列のチェックボックスをオンにします。

     Web通知は、[ プッシュ通知](#notification-push-enable-disable)をブラウザーに対して有効にした場合にのみ配信されます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 通知を既読または未読としてマーク {#notification-mark-read-unread}

通知を&#x200B;*読み取り*&#x200B;または&#x200B;*未読*&#x200B;とマークすると、各ページの上部にある[!UICONTROL Notifications] リンクに表示されている未読の通知の数が変更されます（未読の通知カウンターを含む![通知アイコン ](/help/search-social-commerce/assets/notifications-unread.png "未読の通知カウンター")など）。

*読み取り*&#x200B;とマークされた通知は、明るい色のテキストですが、削除するまで利用できます。

![読み取り/未読の通知](/help/search-social-commerce/assets/notifications-read-vs-unread.png "読み取り/未読の通知")

1. [通知パネルまたは通知センター](#notification-view)を開きます。

1. アラート名の上にカーソルを置き、![既読または未読としてマーク ](/help/search-social-commerce/assets/notifications-read-unread.png "既読または未読としてマーク ")をクリックします。

## 通知の削除 {#notification-delete}

### [!UICONTROL Notifications] パネル内の通知の削除

1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

1. 通知の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

### [!UICONTROL Notification Center]以内に通知を削除

1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

1. **[!UICONTROL View All]**&#x200B;をクリックします。

1. （オプション）通知をタイプ別にフィルタリングするには、*[!UICONTROL Notices]*、*[!UICONTROL Recommendations]*、*[!UICONTROL Warnings]*、または&#x200B;*[!UICONTROL Issues]*&#x200B;をクリックします。

1. 通知の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

## プッシュ通知を有効または無効にする {#notification-push-enable-disable}

Search、Social、およびCommerce内で通知を有効にし、ブラウザーの通知規則に従って表示することができます。 [!DNL Microsoft Windows]を使用しているデバイスでは、通知が画面（システムトレイ）の右下に表示されます。 [!DNL Apple Mac]台のデバイスでは、右側のメニューに通知が表示されます。

プッシュ通知は、次のブラウザーで使用できます。

* [!DNL Google Chrome] 40以上

* [!DNL Microsoft Edge] 17以降

* [!DNL Mozilla Firefox] 44以降

プッシュ通知は、ブラウザーの標準手順に従って無効にできます。

### プッシュ通知を有効にする

1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

1. **[!UICONTROL View All]**&#x200B;をクリックします。

1. 右下の「![ プッシュ通知を有効にする](/help/search-social-commerce/assets/notifications-push.png " プッシュ通知を有効にする")」をクリックします。

1. 確認メッセージで、**[!UICONTROL Enable]**&#x200B;をクリックします。

1. [!UICONTROL Notification Center] `https://alert-center-ui-na.efrontier.com`からの通知を許可するようにブラウザーを設定します。

   デフォルトの通知設定はブラウザーによって異なり、a） [!UICONTROL Notification Center]からの通知を許可するオプションが自動的に表示されるか、b）通知設定を手動で管理する必要があります。 例えば、[!DNL Microsoft Edge]では、ブラウザーツールバーから[!UICONTROL Notification Center]からの通知を許可できます。 ブラウザーのヘルプの手順を参照してください。

   ![Microsoft Edgeの通知設定を管理する場所](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Microsoft Edgeの通知設定を管理する場所")

1. [通知設定](#notification-edit)で、プッシュするアラートタイプの[!UICONTROL Web]通知を有効にします。

### プッシュ通知を無効にする

ブラウザーの通知マネージャー内の`https://alert-center-ui-na.efrontier.com`から通知を削除します。 例えば、[!DNL Google Chrome]では、`chrome://settings/content/notifications`に指定したサイトから通知を削除またはブロックできます。

ブラウザーのヘルプの手順を参照してください。

## [!UICONTROL Notification Center] web アプリケーションをインストールしてアンインストールします {#notification-app-install-uninstall}

[!UICONTROL Notification Center] web アプリケーションをインストールすることで、ブラウザー外で通知を受信および管理できます。 アプリケーションの外観は同じで、Search, Social, &amp; Commerce内の[!UICONTROL Notification Center]と同じ機能を備えています。 アプリケーションは、[!DNL Google Chrome] 40以降または[!DNL Microsoft Edge] 17以降で使用できます。

[!UICONTROL Notification Center] アプリケーションをインストールすると、ブラウザーのアプリケーション マネージャーで自動的に有効になり、ウィンドウ サイズに基づいてレイアウトが動的に配置される別のウィンドウとして読み込まれます。 ブラウザーのアプリケーションマネージャーからアプリケーションを開いて閉じるか、オペレーティングシステムのタスクバーまたはドックに固定できます。 アプリケーションが自動的に更新されます。

![Microsoft Windows タスクバーの通知センターアイコン ](/help/search-social-commerce/assets/windows-taskbar.png "Microsoft Windows タスクバーの通知センターアイコン ")

ブラウザーのアプリケーションマネージャーからアプリケーションを無効にしたり、アンインストールしたりできます。 Web アプリケーションの管理について詳しくは、ブラウザーのヘルプを参照してください。

### [!DNL Google Chrome]の[!UICONTROL Notification Center] Web アプリケーションをインストールします

1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

1. **[!UICONTROL View All]**&#x200B;をクリックします。

1. 右下の「![通知センターweb アプリのインストール ](/help/search-social-commerce/assets/notifications-install-app.png "通知センターweb アプリのインストール ")」をクリックします。

1. 確認メッセージで、**[!UICONTROL Add]**&#x200B;をクリックします。

1. インストールアプリで？ メッセージ、「**[!UICONTROL Install]**」をクリックします。

### [!DNL Microsoft Edge]の[!UICONTROL Notification Center] Web アプリケーションをインストールします

* Search, Social, &amp; Commerceから：

   1. 任意のページの右上にある「![通知](/help/search-social-commerce/assets/notifications.png "通知")」をクリックします。

   1. **[!UICONTROL View All]**&#x200B;をクリックします。

   1. 右下の「![通知センターweb アプリのインストール ](/help/search-social-commerce/assets/notifications-install-app.png "通知センターweb アプリのインストール ")」をクリックします。

   1. 確認メッセージで、**[!UICONTROL Add]**&#x200B;をクリックします。

   1. [!UICONTROL Install Notification Center] アプリ メッセージで、**[!UICONTROL Install]**&#x200B;をクリックします。

* [!DNL Edge] メインメニューから：

   1. ブラウザーのツールバーで、**...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**&#x200B;をクリックします。

   1. [!UICONTROL Install Notification Center] アプリ メッセージで、**[!UICONTROL Install]**&#x200B;をクリックします。

### [!DNL Google Chrome]の[!UICONTROL Notification Center] Web アプリケーションをアンインストールします

* [!DNL Chrome]で、`chrome://apps`に移動し、**[!UICONTROL notification-center]**&#x200B;を右クリックして、**[!UICONTROL Remove from Chrome]**&#x200B;をクリックします。

### [!DNL Microsoft Edge]の[!UICONTROL Notification Center] Web アプリケーションをアンインストールします

1. [!DNL Edge] ブラウザーのツールバーで、**...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**&#x200B;をクリックします。 または、`edge://apps`に移動します。

1. **[!UICONTROL Notification Center]**&#x200B;を右クリックし、**[!UICONTROL Uninstall]**&#x200B;をクリックします。
