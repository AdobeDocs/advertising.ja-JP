---
title: 同期について [!DNL Google Analytics] コンバージョン指標
description: 同期の詳細 [!DNL Google Analytics] 最適化およびレポート用のコンバージョン指標。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 同期について [!DNL Google Analytics] コンバージョン指標

検索、ソーシャル、コマースで、特定の [!DNL Google Analytics] 最適化とレポートのためのアカウント、プロパティ、ビューの組み合わせ。 [ページビュー数](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [セッション](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [バウンス率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) （バウンス/セッションとして計算） [セッション時間](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) が自動的に含まれます。 1 つのデータソースにつき最大 16 個の指標を追加できます。

>[!NOTE]
>
>Advertising DSPユーザーは、コンバージョン指標をカスタム目標として、またレポートで使用できます。

データ転送のすべての API 使用状況は、該当する [!DNL Google Analytics] アカウント このプロジェクトのクォータは、で表示できます。 [の [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). 詳しくは、 [!DNL Google Analytics] 詳細に関するドキュメント [レポート API リクエストの割り当てと呼び出し制限](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

以下の手順は、からコンバージョンデータを同期するプロセスの概要を示しています。 [!DNL Google Analytics].

1. [前提条件のタスクを実行します](data-source-prerequisites.md)

   * Adobe広告トークン (`ef_id` クエリー文字列パラメーター ) を含める必要があります。

   * Adobe広告トークン (`ef_id` クエリー文字列パラメーター ) [!DNL Custom Dimension] in [!DNL Google Analytics].

1. ( 代理アカウント管理者、代理アカウント管理者 [!DNL Adobe] アカウントマネージャー、および管理者ユーザーのみ ) [次の時間ごとに 1 つのデータソースを作成 [!DNL Google Analytics] アカウント、プロパティ、ビューの組み合わせ](data-source-configure.md).

   単一のプロパティに対して複数のプロパティの指標や複数の表示の指標を統合するには、それぞれに個別のデータソースを設定します。

   データソースが設定されると、Search、Social、&amp; Commerce は、広告主のタイムゾーンの 05:00 から毎日データを取り込みます。 指標が使用可能になったら、必要に応じて、キャンペーンおよびポートフォリオ管理ビューとレポートに含め、最適化目標に使用できます。

>[!MORELIKETHIS]
>
>* [の設定の前提条件 [!DNL Google Analytics] データソース](data-source-prerequisites.md)
>* [の設定 [!DNL Google Analytics] データソースとして表示](data-source-configure.md)
>* [の編集 [!DNL Google Analytics] データソース](data-source-edit.md)
>* [データソースの同期を一時停止する](data-source-pause.md)
>* [の再認証 [!DNL Google Analytics] データソース](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] データソース設定](data-source-settings.md)
>* [付録 — 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)

