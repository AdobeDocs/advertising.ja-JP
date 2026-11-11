---
title: （新しいUI） ポートフォリオの変更履歴と入札変更履歴を表示する
description: Adobe Advertising Search, Social, & Commerceで、ポートフォリオの変更と入札変更履歴を表示する方法、日付範囲を変更する方法、ポートフォリオの変更をフィルタリングする方法、履歴レポートを生成、ダウンロード、削除する方法について説明します。
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# （新しいUI） ポートフォリオの変更履歴と入札変更履歴を表示する

*Beta機能*

任意の日付範囲でポートフォリオに加えられた変更のログを表示できます。 ログに記録されるアクションには、ポートフォリオの作成、ポートフォリオの設定へのすべての変更、ポートフォリオに割り当てられたまたは割り当てられていないすべてのキャンペーン、ポートフォリオの入札単位に適用または削除されたすべての制約、期限切れのポートフォリオの入札単位に関するすべての制約、およびポートフォリオに影響を与えるその他のアクションが含まれます。

[!UICONTROL Change History] ダイアログには、ポートフォリオの変更用の[!UICONTROL Portfolio Change History] タブと入札履歴の[!UICONTROL Portfolio Bid Change History] タブが含まれています。 デフォルトでは、両方のタブに過去180日間が表示され、昨日終了します。

ポートフォリオの変更をカテゴリ別にフィルタリングしたり、いずれかのタブの日付範囲を変更したりできます。 データをスプレッドシート ファイルにダウンロードすることもできます。

## ポートフォリオの変更履歴の表示 {#portfolio-change-history}

各変更の情報には、[!UICONTROL Change Date]、[!UICONTROL Changed By]、[!UICONTROL Change Type]、[!UICONTROL Description]が含まれます。 変更点は、新しい順に表示されます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Portfolios]**&#x200B;をクリックします。

1. ポートフォリオ行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Change History]**&#x200B;をクリックします。

1. [!UICONTROL Change History] ダイアログで、「**[!UICONTROL Portfolio Change History]**」タブを表示します。

1. （オプション）表示される情報を変更します。

   * 「![ カレンダー](/help/search-social-commerce/assets/calendar-new.png " カレンダー")」をクリックして、レポートの日付範囲を変更します。

   * 「![ フィルター](/help/search-social-commerce/assets/filter-new.png " フィルター")」をクリックして、データをカテゴリ別にフィルタリングします：[!UICONTROL All]、[!UICONTROL Objective]、[!UICONTROL Campaign]、[!UICONTROL Target]、[!UICONTROL Constraints]、[!UICONTROL Optimization Levers]、または[!UICONTROL Others]。

## ポートフォリオの入札変更履歴の表示 {#portfolio-bid-change-history}

1. [ ポートフォリオの変更履歴を開きます](#portfolio-change-history)。

1. 「**[!UICONTROL Portfolio Bid Change History]**」タブをクリックします。

1. （オプション）「![ カレンダー](/help/search-social-commerce/assets/calendar-new.png " カレンダー")」をクリックして、日付範囲を変更します。

1. （オプション）日付列の見出しをクリックして、リストを昇順または降順で日付順に並べ替えます。

個々の入札単位の履歴を表示するには、[ ポートフォリオのパフォーマンスの詳細](portfolio-details.md#bid-unit-history)から入札単位の詳細を開きます。 [!UICONTROL Bid Unit ID]列が使用可能な場合は、[!UICONTROL Keywords] ビュー](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history)から入札単位履歴を[開くこともできます。

## ポートフォリオ変更履歴のレポートの管理

ポートフォリオの変更履歴に関する追加情報を、[!DNL Microsoft Excel] ワークブック （XLSX ファイル）形式のファイルにダウンロードできます。 レポートには、数値の変更ID、古い値と新しい値、変更タイプ（「追加」または「変更」など）、アクションタイプ（「予算」または「Portfolio名」など）、該当する場合のサブタイプ、時間、ユーザー名が含まれます。

また、[!UICONTROL Portfolio Bid Change History] タブからレポートを生成、ダウンロード、削除することもできます。 レポート設定のタイトルは、ポートフォリオの変更の場合は[!UICONTROL Portfolio History]、入札履歴の場合は[!UICONTROL Portfolio Bid History]です。

### フィルタリングされたデータ行を含むレポートを生成する

1. [ ポートフォリオの変更履歴](#portfolio-change-history)を開き、データをダウンロードするタブをクリックします。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Portfolio History]または[!UICONTROL Portfolio Bid History]の設定で、デフォルトのレポート名をそのまま使用するか、一意のレポート名を入力して、**[!UICONTROL Generate]**&#x200B;をクリックします。

   デフォルトでは、レポート名には、「portfolioChangeHistory_20260402_1326」など、`YYYYMMDD_HHmm`形式の履歴タイプと日時が含まれます。 名前が既に存在する場合は、数値サフィックスが追加されます。

   ファイルが[!UICONTROL Recently Generated] リストに追加されます。

1. （オプション）完了したファイルをダウンロードするには、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完成したレポートをダウンロード

1. [ ポートフォリオの変更履歴](#portfolio-change-history)を開き、レポートを生成したタブをクリックします。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Portfolio History]または[!UICONTROL Portfolio Bid History]設定の[!UICONTROL Recently Generated] リストで、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完了済みレポートの削除

1. [ ポートフォリオの変更履歴](#portfolio-change-history)を開き、レポートを生成したタブをクリックします。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Portfolio History]または[!UICONTROL Portfolio Bid History]設定の[!UICONTROL Recently Generated] リストで、ファイル名の横にある![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

>[!MORELIKETHIS]
>
>* [ ポートフォリオを作成](portfolio-create.md)
>* [ （新しいUI） ポートフォリオの編集](portfolio-edit.md)
>* [ （新しいUI） ポートフォリオパフォーマンスの詳細を表示](portfolio-details.md)
>* [ （新しいUI） [!UICONTROL Portfolios] ビューでデータをダウンロード ](portfolio-view-report.md)
>* [ ポートフォリオについて](portfolio-about.md)
