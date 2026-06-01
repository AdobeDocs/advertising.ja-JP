---
title: （新しいUI）予定レポートについて
description: 利用可能な様々なレポートタイプやレポートの自動化方法など、スケジュールされたパフォーマンスレポートについて説明します。
feature: Search Reports
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e246c273-d720-4ece-b29b-7aaba7d50169id: c916feea-e212-4773-b673-4daed287b8a3id: adcb1be7-7ed0-464d-a8d4-c905c9d47742id: ff99aaef-142d-4c93-a88c-011e979e3843id: fa0141e5-dc99-4fbd-9c0e-40aff66de606id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664
source-git-commit: bd4246ec79684167254a153d2f3d0b917a493096
workflow-type: tm+mt
source-wordcount: 857
ht-degree: 0%

---

# （新しいUI）予定レポートについて

スケジュールされたパフォーマンスレポートを使用すると、ポートフォリオ、広告ネットワーク、広告ネットワークアカウントエンティティのパフォーマンスを必要に応じて詳細に追跡および管理できます。 多くのレポートでは、各マーケティングチャネルの広告がコンバージョン率に与える影響を包括的に把握できます。

レポートのデータは、レポートを実行するたびに動的にコンパイルされます。 必要に応じて、既存のレポートから新しいレポートを生成できます。 使用可能なレポートパラメーターは、レポートタイプによって異なります。 ほとんどのレポートでは、レポート全体を生成する代わりに、最初の50行をプレビューするオプションがあります。 レポートを生成すると、レポートの完了時に、1つ以上の電子メールアドレスにダウンロードリンクを含む通知を送信でき、受信者は[で通知を管理できます（[!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md)）。

完成したすべてのレポートは、[!UICONTROL Reports] ビューの[!UICONTROL Latest Reports] セクションで利用できます。ブラウザーウィンドウでテーブル形式で表示するか、ファイルとして開いたりダウンロードしたりできます。

## 使用可能なレポートカテゴリ

次のレポートカテゴリは、[!UICONTROL Scheduled Reports] ビューから利用できます。 それらのすべてにアクセスできない場合があります。使用可能なレポートと生成されるデータは、お客様の役割と顧客アカウントの設定方法によって決まります。

| レポートカテゴリ | 説明 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [すべてのユーザーが利用できる基本レポート ](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)では、ポートフォリオ、広告ネットワークアカウント、特定の広告ネットワークアカウント、キャンペーン、広告グループ、広告、広告、キーワード、製品グループ、ラベル分類とラベル値、入札単位の制約、およびネットワークの制約の実際のコストとクリックデータを表示します。 該当する広告ネットワークから請求されるクリック数に基づいています。オプションで、コンバージョンデータや作成した他の指標を含めることができます。 |
| [!UICONTROL Advanced Reports] | [高度なレポート ](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)では、広告の設定にinsightが追加されています。これにより、地理的なターゲティングやネットワークの設定を変更することで、どのようなメリットを得られるかを特定できます。 また、キャンペーンおよびポートフォリオ管理ビューにおけるコンバージョンデータや、広告主の内部コンバージョン追跡データに対するレポートの検証にも役立ちます。 |
| [!UICONTROL Assist Reports] | [ アシストレポート ](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md)は、広告主のすべてのキーワードと広告のコンバージョンパスに関するインサイトを提供します。 Adobe Advertisingコンバージョントラッキングサービスを通じて取得したデータを使用し、サービスを提供する広告主に対してのみ生成できます。 |
| [!UICONTROL Specialty Reports] | [特殊レポート ](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md)は、（Adobe Advertising トラッキングではなく）広告ネットワークによって収集されたデータで構成されます。 |
| [!UICONTROL Model Accuracy Reports] | [ モデル精度レポート ](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md)は、ポートフォリオの入札、キャンペーン予算、入札戦略目標の最適化に使用されるコストと収益モデルの精度を示します。 |

## レポートの自動作成

次のいずれかの方法または両方で、カスタマイズされたレポートを自動的に生成するようにスケジュールします。

* [ レポートテンプレート ](/help/search-social-commerce/new-ui/reports/report-templates-manage.md)を使用して、毎日、または特定の曜日または月にレポートを自動生成します。

  オプションで、テンプレートを使用する基本レポートと詳細レポート ](/help/search-social-commerce/new-ui/reports/ftp-reports.md)の[FTP配信を設定できます。

* [ スプレッドシート フィード ](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)を使用して、カスタマイズしたスプレッドシート テンプレートを毎日のパフォーマンスデータで更新し続けます。

## [!UICONTROL Scheduled Reports] ビュー

[!UICONTROL Reports] > [!UICONTROL Scheduled Reports] ビューでは、レポート、テンプレート、スプレッドシート フィードを作成および管理できます。 ビューには、次の2つのタブがあります。

* 「**[!UICONTROL Latest Reports]**」タブには、過去7日間にリクエストされたすべてのレポートが一覧表示されます。ただし、手動で削除されたものを除きます。デフォルトでは、最新のレポートが上部に表示されます。 各レポートに表示される情報には、実行スケジュール（該当する場合）、データが生成された、または生成される開始日と終了日、レポートのステータス（*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*、または&#x200B;*[!UICONTROL Error]*）が含まれます。

  各レポートの横にあるリンクを使用すると、レポートをweb ブラウザーで表示したり、[!DNL Microsoft Excel] ワークブック （XLS）またはタブ区切り値（TSV）ファイルとして開いたり保存したりできます。一部のレポートタイプは、該当するキャンペーンごとに個別のワークシートを含む[!UICONTROL Excel] ワークブックとして保存することもできます。

  このタブから、新しいレポートを作成し（オプションでテンプレートとして使用できます）、既存のレポートの設定に基づいて新しいレポートを作成し、利用可能な進行中のレポートを削除してキャンセルし、利用可能な完了済みレポートを削除することもできます。 7日を超えるレポートは自動的に削除されます。

* 「**[!UICONTROL Templates]**」タブには、関連するスケジュールに関する情報を含め、利用可能なすべての保存された基本および詳細レポートテンプレートが一覧表示されます。 デフォルトでは、最新のテンプレートが一番上にあります。

  このタブから、新しいテンプレートを作成し、作成したテンプレート（スケジュールの追加、変更、削除を含む）を編集し、テンプレートからレポートを生成し、使用可能なテンプレートを削除します。

## レポートの活用方法

| 目的 | レポート |
| ---- | ---- |
| パフォーマンス監視 | <ul><li>[The [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[The [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[The [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[The [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[The [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[The [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| パフォーマンスのトラブルシューティングとトレンド分析 | <ul><li>[The [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[The [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[The [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[The [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[The [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) and [The [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>&quot;[!UICONTROL Compare with]&quot;機能を使用して2つの時間ウィンドウを比較する基本レポート</li></ul> |
| ビジネス成長機会の特定 | <ul><li>（Adobe Advertising コンバージョントラッキングを使用する広告主のみ） [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>（Adobe Advertising コンバージョントラッキングを使用する広告主のみ） [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>（[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)の広告主） Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |
| 分析 | <ul><li>（Adobe Advertising コンバージョントラッキングを使用する広告主のみ） [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>（[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)の広告主） Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |

>[!MORELIKETHIS]
>
>* [ レポートの初期設定タスク ](initial-setup.md)
>* [ レポートに使用されるデータ ](data-used-for-reports.md)
>* [ スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
