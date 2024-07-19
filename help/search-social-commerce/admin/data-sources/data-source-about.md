---
title: 同期  [!DNL Google Analytics]  コンバージョン指標について
description: 最適化およびレポートのための同期  [!DNL Google Analytics]  コンバージョン指標について説明します。
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# コンバージョン指標 [!DNL Google Analytics] 同期について

検索、ソーシャルおよびCommerceでは、特定の [!DNL Google Analytics] アカウント、プロパティ、ビューの組み合わせのコンバージョン指標を同期して、最適化とレポートを実現できます。 [ ページビュー数 ](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews)、[ セッション数 ](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions)、[ バウンス率 ](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) （バウンス/セッションとして計算）、[ セッション時間 ](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) が自動的に含まれます。 データソースごとに最大 16 個の追加指標を含めることができます。

>[!NOTE]
>
>Advertising DSP ユーザーは、コンバージョン指標をカスタム目標およびレポートとして使用できます。

データ転送のすべての API 使用状況は、該当する [!DNL Google Analytics] アカウントのプロジェクトに対して評価されます。 このプロジェクトの割り当て量は、[the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas) で確認できます。 [ レポート API リクエストのクォータと呼び出し制限 ](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) について詳しくは、[!DNL Google Analytics] のドキュメントを参照してください。

次の手順は、[!DNL Google Analytics] からコンバージョンデータを同期するプロセスの概要を示しています。

1. [前提条件タスクの実行](data-source-prerequisites.md)

   * 該当するすべて `ef_id` 広告アカウントのランディングページ URL にAdobe Advertisingトークン（クエリ文字列パラメーター）を実装します。

   * [!DNL Google Analytics] の [!DNL Custom Dimension] にAdobe Advertisingトークン（クエリ文字列パラメーター `ef_id`）を取り込みます。

1. （代理店アカウント管理者、代理店アカウントマネージャー、[!DNL Adobe] ーザーアカウントマネージャー、管理者ユーザーのみ） [ アカウント、プロパティ  [!DNL Google Analytics]  ビューの組み合わせごとに 1 つのデータソースを作成 ](data-source-configure.md) ます。

   複数のプロパティまたは単一のプロパティの複数のビューの指標を統合するには、それぞれに個別のデータソースを設定します。

   データソースが設定されると、検索、ソーシャルおよびCommerceは、広告主のタイムゾーンの 05:00 から毎日データを取り込みます。 指標が使用可能になったら、必要に応じて、キャンペーン管理ビューやポートフォリオ管理ビューおよびレポートに指標を含め、最適化目標で使用できます。

>[!MORELIKETHIS]
>
>* [ データソースを設定するため  [!DNL Google Analytics]  前提条件 ](data-source-prerequisites.md)
>* [ データソースとして  [!DNL Google Analytics]  ビューを設定する ](data-source-configure.md)
>* [ データソース  [!DNL Google Analytics]  編集 ](data-source-edit.md)
>* [ データソースの同期の一時停止 ](data-source-pause.md)
>* [ データソース  [!DNL Google Analytics]  再認証 ](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定 ](data-source-settings.md)
>* [ 付録 – 利用可能  [!DNL Google Analytics]  指標 ](data-source-ga-metrics.md)
