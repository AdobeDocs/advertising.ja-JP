---
title: '[!DNL Google Analytics]のコンバージョン指標の同期について'
description: 最適化とレポート用に[!DNL Google Analytics]のコンバージョン指標を同期する方法について説明します。
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: 'https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: ''
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 1003789d-7feb-5a2f-a02d-3182fd0ceb8a
    internal-label: Search Admin
  - id: 9bd4e165-792f-5324-bcaa-eee38dc8b8e9
    internal-label: Search Data Sources
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
    internal-label: Data sources
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%
---
# [!DNL Google Analytics]のコンバージョン指標の同期について

Search, Social, &amp; Commerceでは、特定の[!DNL Google Analytics] アカウント、プロパティ、ビューの組み合わせのコンバージョン指標を同期して、最適化とレポートを行うことができます。 [&#x200B; ページビュー](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews)、[&#x200B; セッション &#x200B;](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions)、[直帰率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) （バウンス/セッションとして計算）、[&#x200B; セッション期間](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration)が自動的に含まれます。 データソースごとに最大16個の追加指標を含めることができます。

>[!NOTE]
>
>Advertising DSPでは、コンバージョン指標をカスタム目標として使用したり、レポートで使用したりできます。

データ転送のすべてのAPI使用状況は、該当する[!DNL Google Analytics] アカウントのプロジェクトに評価されます。 このプロジェクトの割り当てを[the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)で表示できます。 レポート API リクエストの[割り当てと呼び出し制限](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)について詳しくは、[!DNL Google Analytics]のドキュメントを参照してください。

次の手順では、[!DNL Google Analytics]からコンバージョンデータを同期するプロセスの概要を説明します。

1. [前提条件のタスクの実行](data-source-prerequisites.md)

   * 該当するすべての広告アカウントのランディングページ URLにAdobe Advertising トークン（`ef_id` クエリ文字列パラメーター）を実装します。

   * [!DNL Google Analytics]の[!DNL Custom Dimension]にAdobe Advertising トークン （`ef_id` クエリ文字列パラメーター）をキャプチャします。

1. （代理店アカウント管理者、代理店アカウントマネージャー、[!DNL Adobe] アカウントマネージャー、および管理者ユーザーのみ） [&#x200B; アカウント、プロパティ、ビューの組み合わせごとに1つのデータソースを作成](data-source-configure.md)。 [!DNL Google Analytics] 

   複数のプロパティまたは1つのプロパティの複数のビューの指標を統合するには、それぞれに個別のデータソースを設定します。

   データソースを設定したら、Search, Social, &amp; Commerceを利用して、広告主のタイムゾーンである05:00から毎日データを取得します。 指標が利用可能になると、キャンペーンビューやポートフォリオ管理ビューやレポートに指標を含め、必要に応じて最適化目標に使用することができます。

>[!MORELIKETHIS]
>
>* [&#x200B; データソースを設定するための前提条件 [!DNL Google Analytics] &#x200B;](data-source-prerequisites.md)
>* [&#x200B; データソースとして [!DNL Google Analytics]  ビューを設定](data-source-configure.md)
>* [&#x200B; データソースの編集 [!DNL Google Analytics] &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期を一時停止](data-source-pause.md)
>* [&#x200B; データソースを再認証 [!DNL Google Analytics] します](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定](data-source-settings.md)
>* [付録 – 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
