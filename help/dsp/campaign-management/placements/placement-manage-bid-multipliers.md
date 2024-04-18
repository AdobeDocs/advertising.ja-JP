---
title: プレースメントの入札乗数の管理
description: 指定したプレースメント ターゲットの入札乗数を作成および編集する方法を説明します。
feature: DSP Placements
source-git-commit: b3932c066e0ecd29e57152f0654ee4b0d9e0dda1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 3%

---

# プレースメントの入札乗数の管理

この機能を使用して、既存のプレースメントターゲットの入札乗数を変更できます。 入札乗数は、一度に 1 つのプレースメントについて管理できます。<!-- remove that line once we can edit multiple -->

プレースメントの選択したターゲットを変更するには、「」を参照してください[プレースメントの編集](/help/dsp/campaign-management/placements/placement-edit.md).」と入力します。

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. プレースメント名の横にある「」をクリックします  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. それぞれへ移動 [ターゲット固有のタブ](#bid-multiplier-by-target) （[!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]、および [!UICONTROL Brand Safety]）を選択して、プレースメントターゲットの既存の値を編集します。 ほとんどのターゲットカテゴリには、左側にサブカテゴリが一覧表示されます。 該当する場合は、サブカテゴリをクリックし、そのサブカテゴリの入札乗数を管理します。

   デフォルトでは、ターゲットの入札乗数は 1.00 です。つまり、そのターゲットに対する入札は調整されません。 値の範囲は 0.10 ～ 10.00 です。例えば、入札修飾子が 0.5 の場合、6 米ドルの入札は 3 米ドル（0.5 x 6）に減ります。 入札修飾子は、最大入札値を超えて入札を増加させることはありません。

   オークションが複数の入札モディファイアに該当する場合、適用可能な入札モディファイアがすべて乗算されます。

   に入札乗数（1.00 以外の値）を設定できます。 [限られたターゲット数](#bid-multiplier-limits-by-target).

1. 右上のをクリック **[!UICONTROL Save]**.

## 入札乗数に適格なターゲット・タイプ {#bid-multiplier-by-target}

入札修飾子は、除外されたターゲットではなく、含まれたターゲットに対してのみ設定できます。

* **ジオターゲット**：地域（国、州、都市）、郵便番号、DMA

* **在庫ターゲット**：公開インベントリおよび用のソースとフィード [!UICONTROL On Demand] 在庫

* **サイトのターゲット：** ターゲット（ただし除外はしない）サイト/アプリ、サイトカテゴリ

* **オーディエンスターゲット :** セグメント、視聴時間帯、およびトピック

* **ads.txt ターゲット：** （すべての販売者から在庫を購入できる ads.txt をオプトアウトする場合） ads.txt seller only、ads.txt direct seller、および ads.txt seller plus sites without ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## ターゲットタイプ別の最大入札乗数 {#bid-multiplier-limits-by-target}

ターゲット数に制限がある場合は、入札乗数（1.00 以外の値）を設定できます。 例えば、最大 20 の国のターゲットに入札乗数を設定できます。 入札乗数を持つことのできる各ターゲットタイプのターゲットの最大数を以下に示します。

| カテゴリ | パラメーター | 最大数 |
| -------- | --------- | ----- |
| 地域 | 国 | 20 |
| 地域 | 都道府県 | 100 |
| 地域 | 市区町村 | 100 |
| 地域 | メトロ | 100 |
| 地域 | 郵便番号 | 100 |
| 在庫 | ソース | 100 |
| 在庫 | フィード | 100 |
| Sites | サイトカテゴリ | 100 |
| Sites | サイト / アプリ | 100 |
| オーディエンス | セグメント | 500 |
| オーディエンス | トピック | 100 |
| ブランドセーフティ | Ads.txt | 該当なし |

>[!MORELIKETHIS]
>
>* [プレースメント管理について](placement-about.md)
>* [プレースメントの編集](placement-edit.md)
>* [プレースメントの変更ログの表示](placement-change-log.md)
>* [プレースメント設定](placement-settings.md)
