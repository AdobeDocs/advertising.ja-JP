---
title: （新しいUI）ポートフォリオについて
description: ポートフォリオの詳細。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
TQID: https://experienceleague.adobe.com/w-NpuD1q3atytkO8AL-ekUWzwhX3NHH-byW9ZIY7WdU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebef6e6f-6552-40b6-b842-0c5256698a4e
source-git-commit: 235ba59f2d9e37259431b415c2e34c0da8209ef9
workflow-type: tm+mt
source-wordcount: 729
ht-degree: 0%

---

# （新しいUI）ポートフォリオについて

*Beta機能*

ポートフォリオ（投資ポートフォリオと同様）を使用して、広告キャンペーンを包括的に管理できます。 ポートフォリオとは、関連するキーワードや広告など、単一のビジネス目標に合わせて最適化された、一連の広告キャンペーンや広告セットを指します。 目標には、複数の重み付けされたコンバージョンと、単一の予算目標やパフォーマンスターゲット（月次予算やターゲット ROIなど）が含まれます。 個々のキャンペーン/広告セット、キーワード、広告のパフォーマンスは互いに異なる場合があります（たとえば、異なる金額を費やしたり、異なるROIを達成したりする場合があります）。そのため、最適化機能では、AIを活用したモデルを使用して、ポートフォリオ全体を統括し、ターゲットを達成することができます。 ポートフォリオ内のキャンペーンはすべて同じ通貨を使用します。

一部のユーザーの役割では、ポートフォリオを作成および設定できます。 ポートフォリオのタイプに応じて、ポートフォリオ設定には、ポートフォリオ目標、割り当てられたキャンペーン、支出戦略、ポートフォリオレベルの入札制約、モデリングおよび最適化パラメーターが含まれます。 Search, Social, &amp; Commerceでポートフォリオの最適化を開始する準備ができたら、ステータスを「最適化」に変更します。

オプションでポートフォリオを[&#x200B; ポートフォリオグループ &#x200B;](portfolio-group-manage.md)にグループ化して、グループ全体の複合データを表示できます。

役割によっては、パフォーマンス シミュレーションを生成できる場合があります。予測モデリングを使用して、最適な支出項目と詳細な予測精度レポートを特定します。<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## 入札戦略による最適化サポート {#optimization-by-bid-strategy}

キャンペーンは、キャンペーンまたは広告グループの入札戦略に基づいて最適化の対象となります。

>[!NOTE]
>
>「スマート入札」と「自動入札」はよく同じ意味で使われますが、同じものではありません。 スマート入札とは、オークション時の入札を使用する[!DNL Google Ads]および[!DNL Microsoft Advertising]の自動入札戦略のみを指します。つまり、広告ネットワークは、各オークション時のコンバージョンまたはコンバージョン値に対して最適化されます。

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| 入札戦略 | スマート入札とは？ | キーワード/商品グループレベルの入札ですか？ | サポートレベル | 目標タイプ | 入札単位 | Adobeは何を設定しますか？ | 広告ネットワークは何を設定しますか？ |
|---|---|---|---|---|---|---|---|
| 手動CPC （[!DNL Google Ads]専用オプション） | — | はい | 作成、編集、最適化 | 任意の重み値を持つ単一またはマルチプロパティの目標 | キーワード +一致タイプ + キャンペーン | キーワード入札、キャンペーン予算、入札調整値 | なし |
| ECPC （Enhanced CPC） | はい | はい | 作成、編集、最適化 | 任意の重み値を持つ単一またはマルチプロパティの目標 | キーワード +一致タイプ + キャンペーン | キーワード入札、キャンペーン予算 | 入札をリアルタイムで調整 |
| クリック数を最大化[^1] | — | — | 作成、編集、最適化 | なし。クリックのみに最適化 | キャンペーン | キャンペーン予算 | 予算内のクリック数を最大化するために、入札額をリアルタイムで調整します |
| コンバージョンの最大化<br> （TCPAの有無） | はい | — | 作成、編集、最適化 | 1の重みを使用した単一プロパティの目標 | キャンペーンまたは広告グループ （[!DNL Google Ads]） <br> キャンペーンのみ（[!DNL Microsoft Advertising]） | キャンペーン予算、設定された場合のターゲット CPA<br>TCPAは、[!DNL Microsoft Advertising]の単独入札戦略にできます） | 予算の中で注文やリードを最大化し、目標が設定されているときにCPA目標を達成するために、入札をリアルタイムで調整します |
| コンバージョン値を最大化<br> （TROASの有無） | はい | — | 作成、編集、最適化 | 任意の重み値を持つ複数プロパティの目標、または重み値が1より大きい単一プロパティの目標（金銭的価値を表すために） | キャンペーンまたは広告グループ （[!DNL Google Ads]） <br> キャンペーンのみ（[!DNL Microsoft Advertising]） | キャンペーンの予算、設定された場合のターゲット ROAS<br>TROASは、[!DNL Microsoft Advertising]のスタンドアロン入札戦略にできます） | 予算の中で収益/利益を最大化し、目標が設定されたときにROAS目標を達成するために、リアルタイムで入札を調整します |
| ターゲットインプレッション共有 | — | — | 作成、編集 | なし | なし | n/a - ポートフォリオに割り当てることはできません | インプレッション共有の目標を達成するために、入札額をリアルタイムで調整します |

[^1]：広告ネットワークの[!UICONTROL Maximize Clicks]入札戦略の設定が、検索、ソーシャル、およびCommerceの目標[!UICONTROL Maximize Clicks]と同じではありません。 入札戦略が[!UICONTROL Maximize Clicks]の場合、キーワードレベルの最適化を含むポートフォリオではなく、キャンペーンレベルまたは広告グループレベルの最適化を含むポートフォリオにのみ割り当てる必要があります。

## Portfolio ステータス {#portfolio-status}

ポートフォリオには、次のステータスを設定できます。

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## [!UICONTROL Portfolios] ビュー

[!UICONTROL Portfolios] ビューには、フィルターされたビュー内の既存のポートフォリオがすべて一覧表示され、カスタマイズ可能なパフォーマンスデータが表示されます。 [&#x200B; ビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)内の列をカスタマイズし、データをフィルタリングして、ツールバー[または](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)列見出し[から特定のポートフォリオ &#x200B;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)を含めることができます。

データテーブルの上では、指定した日付範囲のビュー内のすべてのポートフォリオをまたいで合計される最大3つの指標を含むパフォーマンスグラフを開くことができます。

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### 使用可能なアクション

<!-- Update with any new options -->

<!--
 within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [ポートフォリオの作成](portfolio-create.md)

* [ポートフォリオの複製](portfolio-duplicate.md)

* [ポートフォリオ設定の編集](portfolio-edit.md)

* [バルクシートファイルを使用したポートフォリオ設定の一括編集](portfolio-bulksheets.md)

* [ビュー内のすべてのポートフォリオのパフォーマンスグラフを表示](portfolio-view-performance-graph.md)

* [ポートフォリオパフォーマンスの詳細の表示](portfolio-details.md)

* [&#x200B; データを[!UICONTROL Portfolios] ビューでダウンロード &#x200B;](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [&#x200B; ポートフォリオを作成](portfolio-create.md)
>* [&#x200B; ポートフォリオを複製](portfolio-duplicate.md)
>* [&#x200B; ポートフォリオの編集](portfolio-edit.md)
>* [[!UICONTROL Portfolios] ビュー](portfolio-view-report.md)からデータビューレポートを管理
