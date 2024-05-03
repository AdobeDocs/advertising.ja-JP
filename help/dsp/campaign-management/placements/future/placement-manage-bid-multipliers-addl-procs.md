---
title: プレースメントの入札乗数の管理
description: 指定したプレースメント ターゲットの入札乗数を作成および編集する方法を説明します。
feature: DSP Placements
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# プレースメントの入札乗数の管理


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

この機能を使用して、既存のプレースメントターゲットの入札乗数を変更できます。

プレースメントの選択したターゲットを変更するには、「」を参照してください[プレースメントを編集](/help/dsp/campaign-management/placements/placement-edit.md).」と入力します。

## 1 つ以上のプレースメントの入札乗数の管理

選択したすべてのプレースメントで、値を手動で編集するか、値を含むスプレッドシートをアップロードできます。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. 入札乗数を管理する各プレースメントの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、 **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 適格なターゲットの入札乗数を手動で調整するか、ターゲット値を含む CSV ファイルをアップロードして調整します。

   * 入札乗数の値を手動で調整するには、ターゲット固有の各タブ（[!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]、および[!UICONTROL Brand Safety]）を選択して、プレースメントターゲットの既存の値を編集します。

   選択したすべてのプレースメントに対して同じ変更が行われます。

   * 入札乗数の値が既存の値を上書きする CSV ファイルをアップロードするには：

     >[!NOTE]
     >
     >フィールドを空のままにすると、そのターゲットタイプのすべての値が削除されます。<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. クリック **[!UICONTROL CSV Edit]** 右上

      1. a） クリック **[!UICONTROL Download Template]** をクリックして入札乗数の値を編集するか、b）以前にダウンロードしたテンプレートを編集します。 編集したファイルをデバイスまたはネットワークに保存します。

      1. a）編集したファイルをボックスにドラッグ&amp;ドロップするか、b） ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

   1. クリック **[!UICONTROL Upload]**.

   デフォルトでは、ターゲットの入札乗数は 1.00 です。つまり、そのターゲットに対する入札は調整されません。 値の範囲は 0.10 ～ 10.00 です。例えば、入札修飾子が 0.5 の場合、6 米ドルの入札は 3 米ドル（0.5 x 6）に減ります。 に入札乗数（1.00 以外の値）を設定できます。 [限られたターゲット数](#bid-multiplier-limits-by-target).

   オークションが複数の入札モディファイアに該当する場合、適用可能な入札モディファイアがすべて乗算されます。

   入札修飾子は、最大入札値を超えて入札を増加させることはありません。

1. クリック **[!UICONTROL Save]**.

-->

## スプレッドシートをアップロードして、単一プレースメントの入札乗数を管理します<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

アップロードしたファイルを変更すると、既存の入札乗数の値が上書きされます。<!-- what if you delete a row? -->

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. プレースメント名の横にある「」をクリックします  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. a） クリック **[!UICONTROL Download Template]** で入札乗数の値を編集するか、b）で以前にダウンロードしたテンプレートを編集します。 編集したファイルをデバイスまたはネットワークに保存します。

   デフォルトでは、ターゲットの入札乗数は 1.00 です。つまり、そのターゲットに対する入札は調整されません。 値の範囲は 0.10 ～ 10.00 です。例えば、入札修飾子が 0.5 の場合、6 米ドルの入札は 3 米ドル（0.5 x 6）に減ります。 に入札乗数（1.00 以外の値）を設定できます。 [限られたターゲット数](#bid-multiplier-limits-by-target).

   オークションが複数の入札モディファイアに該当する場合、適用可能な入札モディファイアがすべて乗算されます。

   入札修飾子は、最大入札値を超えて入札を増加させることはありません。

1. a）編集したファイルをボックスにドラッグ&amp;ドロップするか、b） ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

1. クリック **[!UICONTROL Upload]**.

1. クリック **[!UICONTROL Save]**.

## 入札乗数に適格なターゲット・タイプ {#bid-multiplier-by-target}

ここでは吹き飛ばされない

## ターゲットタイプ別の最大入札乗数 {#bid-multiplier-limits-by-target}

ここでは吹き飛ばされない

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
