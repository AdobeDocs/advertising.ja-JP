---
title: レポートについて
description: 使用可能な様々なレポートタイプやレポートの自動化方法など、パフォーマンスレポートについて説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# レポートについて

パフォーマンスレポートを使用すると、ポートフォリオ、広告ネットワーク、広告ネットワークアカウントエンティティのパフォーマンスを、必要に応じてきめ細かいレベルで追跡および管理できます。 ほとんどのレポートでは、各マーケティングチャネルの広告が全体的なコンバージョン率にどのように貢献しているかを、完全に可視化できます。

レポートのデータは、レポートを実行するたびに動的にコンパイルされます。 オプションで、既存のレポートから新しいレポートを生成できます。 使用可能なレポートパラメーターは、レポートタイプによって異なります。 ほとんどのレポートでは、レポート全体を生成する代わりに、最初の 50 行をプレビューするオプションがあります。 レポートを生成する際には、レポート作成完了時に 1 つ以上の電子メールアドレスにダウンロードリンクの通知を送信できます。また、受信者には [で通知を管理します。 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

完了したレポートは、 [!UICONTROL Latest Reports] セクション [!UICONTROL Reports] を表示し、ブラウザーウィンドウで表形式で表示するか、ファイルとして開く、またはダウンロードできます。

## 使用可能なレポートカテゴリ

次のレポートカテゴリが [!UICONTROL Reports] 表示 すべてのユーザーに対するアクセス権を持っていない可能性があります。生成される使用可能なレポートとデータは、ユーザーの役割と、顧客アカウントの設定方法によって異なります。

| レポートカテゴリ | 説明 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [基本レポート](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)すべてのユーザーが使用できる、ポートフォリオ、広告ネットワークアカウント、特定の広告ネットワークアカウント、キャンペーン、広告グループ、広告、キーワード、製品グループ、ラベル分類およびラベル値、入札単位制約、ネットワーク制約の実際のコストとクリックデータを表示します。 該当する広告ネットワークから請求されたクリック数に基づいています。また、オプションで、コンバージョンデータや作成した他の指標を含めることもできます。 |
| [!UICONTROL Advanced Reports] | [高度なレポート](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) 広告設定に関する詳細なインサイトを提供し、地理的なターゲット設定やネットワーク設定を変更することで、どこでメリットがあるかを特定できます。 また、キャンペーンおよびポートフォリオ管理のビューとレポートで、広告主の内部コンバージョントラッキングデータに対するコンバージョンデータを検証するのに役立ちます。 |
| [!UICONTROL Assist Reports] | [アシストレポート](/help/search-social-commerce/reports/management/assist/assist-report-about.md) は、広告主のすべてのキーワードと広告のコンバージョンパスに関するインサイトを提供します。 Adobe広告コンバージョントラッキングサービスで取得されたデータを使用し、サービスを持つ広告主の場合にのみ生成できます。 |
| [!UICONTROL Specialty Reports] | [特殊レポート](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) は、(Adobe広告トラッキングではなく ) 広告ネットワークで収集されたデータで構成されます。 |
| [!UICONTROL Model Accuracy Reports] | [モデル精度レポート](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) 入札の最適化に使用するコストと売上高のモデルの精度を示します。 |

## レポートの自動化

次のいずれかの方法で、または両方の方法で自動的に生成されるように、カスタマイズされたレポートをスケジュールします。

* を使用して、毎日、または特定の曜日や月のレポートを自動的に生成します。 [レポートテンプレート](/help/search-social-commerce/reports/automation/templates/template-about.md).

   オプションで、 [基本レポートと高度なレポートの FTP 配信](/help/search-social-commerce/reports/automation/ftp-reports.md) テンプレートを使用する

* 次を使用して、カスタマイズしたスプレッドシートテンプレートを毎日のパフォーマンスデータで更新し続けます： [スプレッドシートフィード](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## レポートビュー

この [!UICONTROL Reports] ビュー： [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] では、レポート、テンプレートおよびスプレッドシートフィードを作成および管理できます。 このビューには、次の 2 つのタブが含まれています。

* この **[!UICONTROL Latest Reports]** 「 」タブには、過去 7 日間にリクエストされたすべてのレポートが表示されます。ただし、手動で削除したレポートは除き、最新のレポートがデフォルトで上部に表示されます。 各レポートに表示される情報には、実行するスケジュール（該当する場合）、データが生成された開始日と終了日、レポートのステータス (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]*&#x200B;または *[!UICONTROL Error]*) をクリックします。

   各レポートの横にあるリンクを使用すると、レポートを Web ブラウザーで表示したり、 [!DNL Microsoft Excel] ワークブック (XLS) ファイルまたはタブ区切り値 (TSV) ファイル一部のレポートタイプは、 [!UICONTROL Excel] ワークブックを作成し、該当するキャンペーンごとに個別のワークシートを作成する。

   また、このタブから、新しいレポート（オプションでテンプレートとして使用可能）の作成、既存のレポートの設定に基づく新しいレポートの作成、削除による進行中のレポートのキャンセル、使用可能な完了したレポートの削除を行うこともできます。 7 日を超えるレポートは自動的に削除されます。

* この **[!UICONTROL Templates]** 「 」タブには、使用可能なすべての保存済みの基本レポートテンプレートと詳細レポートテンプレートが一覧表示されます。これには、関連付けられているスケジュールに関する情報も含まれます。 デフォルトでは、最新のテンプレートが一番上に表示されます。

   このタブから、新しいテンプレートを作成し、作成したテンプレート（スケジュールの追加、変更、削除を含む）を編集し、テンプレートからレポートを生成します。をクリックし、使用可能なテンプレートを削除します。

## レポートの使用方法

| 目的 | レポート |
| ---- | ---- |
| パフォーマンス監視 | <ul><li>[この [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[この [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[この [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[この [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[この [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[この [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| パフォーマンスのトラブルシューティングとトレンド分析 | <ul><li>[この [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[この [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[この [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[この [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[この [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) および [この [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>「[!UICONTROL Compare with]&quot;機能&quot;</li></ul> |
| ビジネスの成長機会の特定 | <ul><li>(Adobe広告コンバージョントラッキングのみの広告主 ) [この [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Adobe広告コンバージョントラッキングのみの広告主 ) [この [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>( [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html))Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |
| Analytics | <ul><li>(Adobe広告コンバージョントラッキングのみの広告主 ) [この [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>( [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html))Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |

>[!MORELIKETHIS]
>
>* [レポートに使用するデータ](data-used-for-reports.md)
>* [レポートの初期設定タスク](initial-setup.md)
>* [基本レポートまたは高度なレポートの生成](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [モデル精度レポートの生成](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [特殊なレポートの生成](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [アシストレポートの生成](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)

