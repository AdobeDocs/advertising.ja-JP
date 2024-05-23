---
title: プレースメントの入札乗数の管理
description: xxx について
feature: DSP Placements
source-git-commit: 85e1338b841cd9615f7d2881185487ae79743303
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# XXX

## 単一プレースメントの入札乗数の管理

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. プレースメント名の横にある「」をクリックします  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 適格なターゲットの入札乗数を調整します。

   * 入札乗数の値を手動で調整するには、それぞれに移動します [ターゲット固有のタブ](#bid-multiplier-by-target) （[!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]、および [!UICONTROL Brand Safety]）を選択して、プレースメントターゲットの既存の値を編集します。

     ほとんどのターゲットカテゴリには、左側にサブカテゴリが一覧表示されます。 該当する場合は、サブカテゴリをクリックして、そのサブカテゴリの入札乗数を管理します。

   * 入札乗数の値を含む CSV ファイルをアップロードして、既存の値を上書きするには：

      1. クリック **[!UICONTROL CSV File Edit]** 右上

      1. a） クリック **[!UICONTROL Download Template]** ユーザーインターフェイスに表示されているのと同じ構文を使用してターゲットを入力し、対応する入札乗数の値を入力します。または、b）以前にダウンロードしたテンプレートを同じ情報で編集します。 編集したファイルをデバイスまたはネットワークに保存します。

      1. クリック **[!UICONTROL Next]** に移動します [!UICONTROL Upload File] セクションと a）編集したファイルをボックスにドラッグ&amp;ドロップするか、b）ボックス内をクリックしてデバイスまたはネットワークからファイルを選択します。

      1. にアップロードされたデータを検証します。 [!UICONTROL Review & Submit] セクションを選択し、 **[!UICONTROL Save]**.

## 1 つ以上のプレースメントの入札乗数の管理

<!-- verify all and edit accordingly -->

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. 入札乗数を管理する各プレースメントの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、 **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

<!-- Check the following this functionality when available in UAT -->

1. 適格なターゲットの入札乗数を調整します。

   * 入札乗数の値を手動で調整するには、ターゲット固有の各タブ（[!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience]、および[!UICONTROL Brand Safety]）を選択して、プレースメントターゲットの既存の値を編集します。

   同じ変更が、選択したすべてのプレースメントに適用されます。

   * 入札乗数の値が既存の値を上書きする CSV ファイルをアップロードするには：

     >[!NOTE]
     >
     >フィールドを空のままにすると、そのターゲットタイプのすべての値が削除されます。<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there only one data row is applicable for all. -->

      1. クリック **[!UICONTROL CSV Edit]** 右上

      1. a） クリック **[!UICONTROL Download Template]** をクリックして入札乗数の値を編集するか、b）以前にダウンロードしたテンプレートを編集します。 編集したファイルをデバイスまたはネットワークに保存します。

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
