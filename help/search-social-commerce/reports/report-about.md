---
title: レポートについて
description: 使用可能な様々なレポートタイプやレポートの自動化方法など、パフォーマンスレポートについて説明します。
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# レポートについて

パフォーマンスレポートを使用すると、ポートフォリオ、広告ネットワーク、広告ネットワークアカウントエンティティのパフォーマンスを、必要な精度で追跡および管理できます。 ほとんどのレポートでは、各マーケティングチャネルの広告が全体的なコンバージョン率にどのように貢献しているかを完全に把握できます。

レポートのデータは、レポートを実行するたびに動的にコンパイルされます。 必要に応じて、既存のレポートから新しいレポートを生成できます。 使用可能なレポートパラメーターは、レポートタイプによって異なります。 ほとんどのレポートでは、レポート全体を生成する代わりに、最初の 50 行をプレビューするオプションがあります。 レポートの生成時に、レポートが完了したときに 1 つ以上のメールアドレスへのダウンロードリンクを含む通知を送信でき、受信者は [[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md) で通知を管理できます。

完了したレポートはすべて、[!UICONTROL Reports] ビューの [!UICONTROL Latest Reports] セクションで使用できます。また、ブラウザーウィンドウでテーブル形式で表示したり、ファイルとして開いたりダウンロードしたりできます。

## 使用可能なレポートカテゴリ

[!UICONTROL Reports] ビューでは次のレポートカテゴリを使用できます。 すべてのレポートにはアクセスできない場合があります。使用可能なレポートとそのレポートで生成されるデータは、ユーザーの役割と顧客アカウントの設定方法によって異なります。

| レポートカテゴリ | 説明 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [ 基本レポート ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) は、すべてのユーザーが使用でき、ポートフォリオ、広告ネットワークアカウント、特定の広告ネットワークアカウント、キャンペーン、広告グループ、広告、キーワード、製品グループ、ラベルの分類とラベルの値、入札単位の制約、ネットワークの制約に関する実際のコストとクリックデータを表示します。 該当する広告ネットワークから請求されるクリック数に基づいており、オプションでコンバージョンデータやユーザーが作成したその他の指標を含めることができます。 |
| [!UICONTROL Advanced Reports] | [ 詳細レポート ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) は、広告設定に関する追加のインサイトを提供し、地理的ターゲティングやネットワーク設定を変更することでメリットが得られる場所を特定するのに役立ちます。 また、キャンペーンおよびポートフォリオ管理ビューでコンバージョンデータを検証し、広告主の内部コンバージョントラッキングデータに対してレポートを作成するのにも役立ちます。 |
| [!UICONTROL Assist Reports] | [ アシストレポート ](/help/search-social-commerce/reports/management/assist/assist-report-about.md) は、広告主のすべてのキーワードと広告のコンバージョンパスに関するインサイトを提供します。 Adobe Advertisingコンバージョントラッキングサービスを通じて取得したデータを使用し、サービスを利用する広告主に対してのみ生成できます。 |
| [!UICONTROL Specialty Reports] | [ 専門レポート ](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) は、（Adobe Advertisingトラッキングではなく）広告ネットワークによって収集されたデータで構成されます。 |
| [!UICONTROL Model Accuracy Reports] | [ モデル精度レポート ](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) は、ポートフォリオの入札、キャンペーン予算および入札戦略目標の最適化に使用されるコストおよび収益モデルの精度を示します。 |

## レポートの自動処理

次のどちらか一方または両方の方法で、カスタマイズされたレポートが自動的に生成されるようにスケジュールを設定します。

* [ レポートテンプレート ](/help/search-social-commerce/reports/automation/templates/template-about.md) を使用して、毎日または特定の曜日にレポートを自動的に生成します。

  オプションで、テンプレートを使用する [ 基本レポートと詳細レポートの FTP 配信 ](/help/search-social-commerce/reports/automation/ftp-reports.md) を設定できます。

* [ スプレッドシートフィード ](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) を使用して、カスタマイズしたスプレッドシートテンプレートを毎日のパフォーマンスデータで更新し続けます。

## レポートビュー

[!UICONTROL Search]/[!UICONTROL Insights & Reports]/[!UICONTROL Reports] の [!UICONTROL Reports] ビューでは、レポート、テンプレートおよびスプレッドシートフィードを作成および管理できます。 ビューには、次の 2 つのタブがあります。

* 「**[!UICONTROL Latest Reports]**」タブには、過去 7 日間にリクエストされたレポートのうち、手動で削除されたものを除いて使用可能なすべてのレポートがリストされます。デフォルトでは、最新のレポートが先頭に表示されます。 各レポートに表示される情報には、実行されるスケジュール（該当する場合）、データが生成された、または生成される開始日と終了日、レポートのステータス（*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*、*[!UICONTROL Error]*）が含まれます。

  各レポートの横にあるリンクを使用すると、レポートを Web ブラウザで表示したり、[!DNL Microsoft Excel] ワークブック （XLS）またはタブ区切り値（TSV） ファイルとして開いたり保存したりできます。一部のレポート タイプは、適用可能なキャンペーンごとに個別のワークシートを持つ [!UICONTROL Excel] ワークブックとして保存することもできます。

  このタブでは、新しいレポートの作成（オプションでテンプレートとして使用できます）、既存のレポートの設定に基づく新しいレポートの作成、進行中のレポートの削除によるキャンセル、利用可能な完了済みのレポートの削除を行うこともできます。 7 日を経過したレポートは、自動的に削除されます。

* 「**[!UICONTROL Templates]**」タブには、使用可能なすべての保存済みの基本および詳細レポートテンプレートがリストされます。これには、関連するスケジュールに関する情報も含まれます。 デフォルトでは、最新のテンプレートが先頭に表示されます。

  このタブから、新しいテンプレートを作成し、作成したテンプレートを編集（スケジュールの追加、変更、削除を含む）、テンプレートからレポートを生成し、使用可能なテンプレートを削除します。

## レポートの使用方法

| 目的 | 報告書 |
| ---- | ---- |
| パフォーマンスの監視 | <ul><li>[[!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[[!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[[!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[[!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[[!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[[!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| パフォーマンスのトラブルシューティングとトレンド分析 | <ul><li>[[!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[[!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[[!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[[!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) と [[!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>「[!UICONTROL Compare with]」機能を使用して 2 つの期間を比較する基本レポート</li></ul> |
| ビジネスの成長の機会の特定 | <ul><li>（Adobe Advertisingコンバージョントラッキングを使用している広告主のみ） [[!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>（Adobe Advertisingコンバージョントラッキングを使用している広告主のみ） [[!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>（[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) を使用する広告主）Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |
| Analytics | <ul><li>（Adobe Advertisingコンバージョントラッキングを使用している広告主のみ） [[!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>（[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) を使用する広告主）Adobe Analytics Analysis Workspace内のカスタマイズされたレポート</li></ul> |

>[!MORELIKETHIS]
>
>* [ 報告書に用いるデータ ](data-used-for-reports.md)
>* [ レポートの初期設定タスク ](initial-setup.md)
>* [ 基本レポートまたは詳細レポートの生成 ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [ モデル精度レポートの生成 ](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [ 専門レポートの生成 ](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [ アシストレポートの生成 ](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
