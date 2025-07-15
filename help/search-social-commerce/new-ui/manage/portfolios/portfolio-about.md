---
title: （新しい UI）ポートフォリオについて
description: ポートフォリオについて説明します。
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# （新しい UI）ポートフォリオについて

*Beta機能*

ポートフォリオ（投資ポートフォリオと同様）を使用して、広告キャンペーンをまとめて管理できます。 ポートフォリオとは、1 つのビジネス目標に最適化された一連の広告キャンペーンまたは広告セット（関連するキーワードや広告を含む）です。 目標には、複数の重み付けコンバージョンと、単一の予算またはパフォーマンス目標（月次予算や目標 ROI など）を含めることができます。 キャンペーン/広告セット、キーワードおよび広告は、個別に異なるパフォーマンスを発揮する（異なる金額を費やす、異なる ROI を達成するなど）可能性があるので、最適化機能では AI 駆動モデルを使用して、ポートフォリオ全体を導き出して目標をまとめて達成します。 ポートフォリオ内のすべてのキャンペーンが同じ通貨を使用します。

一部のユーザーの役割では、ポートフォリオを作成および設定できます。 ポートフォリオのタイプに応じて、ポートフォリオ設定には、ポートフォリオの目的、割り当てられたキャンペーン、支出戦略、ポートフォリオレベルの入札制約、モデリングおよび最適化パラメーターが含まれる場合があります。 検索、ソーシャル、Commerceの準備が整ったら、ポートフォリオの最適化を開始し、ステータスを「最適化済み」に変更します。

オプションで、ポートフォリオをポートフォリオグループにグループ化して、グループ全体のクリックと売上高の複合データを表示できます。 [ レガシー UI](/help/search-social-commerce/getting-started/ui-switch.md) からポートフォリオグループを作成します。

役割によっては、パフォーマンス・シミュレーションを生成できる場合があります。このシミュレーションでは、予測モデリングを使用して、最適な支出ポイントと詳細な予測精度レポートを特定します。<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## 入札戦略による最適化サポート {#optimization-by-bid-strategy}

キャンペーンは、キャンペーンまたは広告グループの入札戦略に基づいて最適化することができます。

>[!NOTE]
>
>「スマート入札」と「自動入札」は同じ意味で使用されることが多いですが、同じものではありません。 スマート入札とは、オークション時の入札を使用する自動入札戦略の [!DNL Google Ads] と [!DNL Microsoft Advertising] のみを指します。つまり、広告ネットワークは、各オークションの際にコンバージョンやコンバージョン値に合わせて最適化します。

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| 入札戦略 | スマートビディング？ | キーワード/製品グループレベルの入札 | サポートレベル | 目標タイプ | 入札単位 | Adobeは何を設定しますか？ | 広告ネットワークは何を設定しますか？ |
|---|---|---|---|---|---|---|---|
| 手動 CPC （[!DNL Google Ads] のみオプション） | — | はい | 作成、編集、最適化 | 任意の重み付け値を持つ単一または複数プロパティの目標 | キーワード +一致タイプ + キャンペーン | キーワード入札、キャンペーン予算、入札調整値 | 該当なし |
| ECPC （拡張 CPC） | はい | はい | 作成、編集、最適化 | 任意の重み付け値を持つ単一または複数プロパティの目標 | キーワード +一致タイプ + キャンペーン | キーワード入札、キャンペーン予算 | リアルタイムで入札を調整します |
| クリック数の最大化 [^1] | — | — | 作成、編集、最適化 | なし。クリックのみに最適化されます | キャンペーン | キャンペーン予算 | リアルタイムで入札を調整して、予算内のクリックを最大化します |
| コンバージョン数 <br> 最大化（TCPA の有無を問わない） | はい | — | 作成、編集、最適化 | 1 の重みを使用した単一プロパティ目標 | キャンペーンまたは広告グループ （[!DNL Google Ads]） <br> キャンペーンのみ（[!DNL Microsoft Advertising]） | キャンペーン予算、設定時のターゲット CPA<br>TCPA は [!DNL Microsoft Advertising] ではスタンドアロンの入札戦略にすることができます） | ターゲットが設定されると CPA 目標を満たすように、リアルタイムで入札を調整し、予算内の注文/リードを最大化します |
| コンバージョン価値 <br> 最大化（TROAS の有無を問わない） | はい | — | 作成、編集、最適化 | 任意の重み値を持つマルチプロパティ目標、または重み値が 1 より大きい単一プロパティ目標（金銭的価値を表す） | キャンペーンまたは広告グループ （[!DNL Google Ads]） <br> キャンペーンのみ（[!DNL Microsoft Advertising]） | キャンペーン予算、設定時の Target ROAS<br>TROAS は [!DNL Microsoft Advertising] のスタンドアロン入札戦略にすることができます） | リアルタイムで入札を調整して、予算内の収益/利益を最大化し、目標が設定されたときに ROAS 目標を達成します |
| ターゲットインプレッション共有 | — | — | 作成、編集 | 該当なし | 該当なし | なし – ポートフォリオに割り当てることはできません | インプレッション共有の目標を満たすためにリアルタイムで入札を調整 |

[^1]：広告ネットワークの [!UICONTROL Maximize Clicks] の入札戦略設定は、検索、ソーシャル、Commerceの目的 [!UICONTROL Maximize Clicks] とは異なります。 入札戦略が [!UICONTROL Maximize Clicks] の場合は、キーワードレベルの最適化を含むポートフォリオではなく、キャンペーンレベルまたは広告グループレベルの最適化を含むポートフォリオにのみ割り当てる必要があります。

## Portfolioステータス {#portfolio-status}

ポートフォリオには、次のステータスがあります。

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## [!UICONTROL Portfolios] ビュー

[!UICONTROL Portfolios] 表示には、カスタマイズ可能なパフォーマンスデータが含まれる既存のポートフォリオが一覧表示されます。 [ ビュー内の列をカスタマイズ ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) したり、データをフィルターして特定のポートフォリオを含めたりできます [ ツールバーから ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) または [ 列見出し ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)。

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### 使用可能なアクション

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [ポートフォリオの作成](portfolio-create.md)

* [ポートフォリオの複製](portfolio-duplicate.md)

* [ポートフォリオ設定の編集](portfolio-edit.md)

* [バルクシートファイルを使用したポートフォリオ設定の一括編集](portfolio-bulksheets.md)

* [ポートフォリオ パフォーマンスの詳細を表示します](portfolio-details.md)

* [[!UICONTROL Portfolios] 表示でのデータのダウンロード ](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [ ポートフォリオの作成 ](portfolio-create.md)
>* [ ポートフォリオの複製 ](portfolio-duplicate.md)
>* [ ポートフォリオの編集 ](portfolio-edit.md)
>* [ データビューからのデータ表示レポ [!UICONTROL Portfolios] トの管理 ](portfolio-view-report.md)
