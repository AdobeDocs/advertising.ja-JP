---
title: （新しいUI） ポートフォリオの変更履歴の表示
description: ポートフォリオの変更履歴を表示する方法を説明します。
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 081453404883619e0a70bba080c857bf7e3136cc
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# （新しいUI） ポートフォリオの変更履歴の表示

*Beta機能*

任意の日付範囲でポートフォリオに加えられた変更のログを表示できます。 ログに記録されるアクションには、ポートフォリオの作成、ポートフォリオの設定に対するすべての変更、ポートフォリオに割り当てられたまたはポートフォリオから割り当てられていないすべてのキャンペーン、ポートフォリオの入札単位に適用または削除されたすべての制約、期限切れのポートフォリオの入札単位に関するすべての制約、およびポートフォリオに影響を与えるその他のアクションが含まれます

データは、カテゴリ <!-- Not available as of 5-14: and by the user who performed the action -->でフィルタリングできます。 リストを昇順または降順で日付順に並べ替えることもできます。

データをスプレッドシート ファイルにダウンロードすることもできます。

## （新しいUI） ポートフォリオの変更履歴の表示 {#portfolio-change-history}

各変更の情報には、日付、変更を行ったユーザーのユーザー名、変更タイプ、変更された値が含まれます。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

1. ポートフォリオ行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Change History]**&#x200B;をクリックします。

1. （オプション）表示される情報を変更します。

   * 「![ カレンダー](/help/search-social-commerce/assets/calendar-new.png " カレンダー")」をクリックして、レポートの日付範囲を変更します。

   * ![ フィルター](/help/search-social-commerce/assets/filter-new.png " フィルター")をクリックして、変更タイプでデータをフィルタリングします。<!-- Not available as of 5-14: and by the user who performed the action -->。

   * 「![並べ替え](/help/search-social-commerce/assets/sort.png "並べ替え")」をクリックして、リストを日付で昇順または降順に並べ替えます。


## 変更履歴のパフォーマンスデータレポートを管理する

ポートフォリオの変更履歴に関する追加情報を、[!DNL Microsoft Excel] ワークブック （XLSX ファイル）形式のファイルにダウンロードできます。 レポートには、数値の変更ID、古い値と新しい値、変更タイプ（「追加」または「変更」など）、アクションタイプ（「予算」または「Portfolio名」など）、該当する場合のサブタイプ、時間、ユーザー名が含まれます。

### フィルタリングされたデータ行を含むレポートを生成する

1. [ ポートフォリオの変更履歴を開きます](#portfolio-change-history)。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Grid Reports]設定で、一意のレポート名を入力し、**[!UICONTROL Generate]**&#x200B;をクリックします。

   デフォルトでは、ファイル名は「portfolioChangeHistory_YYYYMMDD_NNNNN」で、「NNNN」は順次ジョブ番号（「portfolioChangeHistory_20260402_1326」など）です。

   ファイルが[!UICONTROL Recently Generated] リストに追加されます。

1. （オプション）完了したファイルをダウンロードするには、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完成したレポートをダウンロード

1. [ ポートフォリオの変更履歴を開きます](#portfolio-change-history)。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完了済みレポートの削除

1. [ ポートフォリオの変更履歴を開きます](#portfolio-change-history)。

1. 右上の「![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ")」をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

>[!MORELIKETHIS]
>
>* [ ポートフォリオを作成](portfolio-create.md)
>* [ （新しいUI） ポートフォリオの編集](portfolio-edit.md)
>* [ （新しいUI） ポートフォリオパフォーマンスの詳細を表示](portfolio-details.md)
>* [ （新しいUI） [!UICONTROL Portfolios] ビューでデータをダウンロード ](portfolio-view-report.md)
>* [ ポートフォリオについて](portfolio-about.md)
