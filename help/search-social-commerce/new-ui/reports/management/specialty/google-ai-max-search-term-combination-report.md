---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: '[!UICONTROL Google AI Max Search Term Combination Report]について説明します。'
feature: Search Reports, Search Specialty Reports
source-git-commit: a595c7d6245fa5d65e704e88230f2eab0a336e72
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*AIの最大数*&#x200B;に対してキャンペーンが有効になっている[!DNL Google Ads] アカウントに適用可能

[!UICONTROL Google AI Max Search Term Combination Report]は、特定の検索クエリが、AIが生成した見出しと動的なランディングページ、および指定されたアカウント内の[!DNL Google Ads AI Max]対応キャンペーンの広告のコンバージョンアクションにどのようにマッピングされるかを示しています。 本報告書は以下の2頁から構成されています。

* [!UICONTROL AI Max Search Term] シート：検索ネットワーク内での検索に基づく、特定の広告の組み合わせとランディングページのパフォーマンス。 このシートには、インプレッション、クリック、コストのデータと、レポート設定で指定された任意の[!DNL Google Ads] トラッキングされたコンバージョン指標が含まれます。 デフォルトでは、データには、指定されたデータ範囲で少なくとも1つのインプレッションを受け取った各検索語、見出し、およびランディングページの組み合わせごとに1つの行が含まれます。 行は、デフォルトでキャンペーンによって昇順に並べられ、次に選択した別の列によって昇順に並べられます。

  このシートを使用して、クエリごとに結果として得られる広告要素の意図とパフォーマンスを分析し、強固な負のキーワードリストを構築できるようにします。

* &#x200B;<!-- [!UICONTROL Search Term x Conversion Action] sheet? -->[!UICONTROL AI Max Search Term #1] シート：[!DNL Google Ads]は、各検索語句と一致タイプのコンバージョンアクションによって追跡されたコンバージョンデータです。 各行には、コンバージョンアクション、コンバージョン数、コンバージョン値、およびレポート設定で指定されたその他のオプションの[!DNL Google Ads]追跡されたコンバージョン指標が含まれます。 デフォルトでは、データには、指定したデータ範囲の各検索語とコンバージョンアクションの組み合わせごとに1行が含まれます。 行は、最初のシートの行と同じ順序になります。

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  このシートでは、各検索語がどのようにコンバージョンを促進したのかを、コンバージョンアクション別に説明します。

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## デフォルトの列

すべてのデフォルト列とカスタム列について詳しくは、「[特殊レポートのレポート列](specialty-report-columns.md)」を参照してください。

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] （明示的に含めない場合でも、[!UICONTROL AI Max Search Term #1] シートに自動的に含まれます）
* [!UICONTROL Conversions] （明示的に含めない場合でも、[!UICONTROL AI Max Search Term #1] シートに自動的に含まれます）
* [!UICONTROL Conversions Value] （明示的に含めない場合でも、[!UICONTROL AI Max Search Term #1] シートに自動的に含まれます）

>[!MORELIKETHIS]
>
>* [専門性レポートについて](specialty-report-about.md)
>* [&#x200B; スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [特殊レポート設定](specialty-report-settings.md)
>* [専門性レポートのレポート列](specialty-report-columns.md)
