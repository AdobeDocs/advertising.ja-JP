---
title: 個人契約のプレースメントと広告の指定
description: 追加の配置と広告を使用して個人取引を使用する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: d6d295119bc974a87840e757877c1507237a6fa2
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# 個人契約のプレースメントと広告の指定

保証されていない契約の場合、新しい配置の在庫ターゲットとして契約を指定できます： [!UICONTROL Placements] 表示。

プログラム的に保証された (PG) 取引の場合、 [!UICONTROL Deals] 表示。

また、 [配置に広告を付加する](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) PG と保証されていない契約といつでも関連しています。

## 配置の在庫ターゲットとしての保証されていない契約の指定

* [からの配置の作成 [!UICONTROL Placements] 表示](/help/dsp/campaign-management/placements/placement-create.md). Adobe Analytics の [!UICONTROL Inventory Targeting] 「settings」で、「private deal」を選択します。

## PG 契約へのプレースメントと広告の付加

1. メインメニューで、 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. ディール行で、「  **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Adobe Analytics の [!UICONTROL Ad & Campaign Selection] 設定で、プレースメントに使用する広告を選択します。

       1.広告主、キャンペーン、広告のタイプを選択します。 オプションで、広告のフィルターに使用する広告ステータスを選択します。
       
       1. 使用可能な広告のリストから、契約に使用される各広告の横にあるチェックボックスを選択します。
       
       1. クリック**[!UICONTROL Apply]**.
   
   1. 配置設定画面で、次の操作をおこないます。

      1. 配置名を入力します。

      1. （オプション） [配置設定](/help/dsp/campaign-management/placements/placement-settings.md)デフォルトの入札額の上書き、契約の CPM 値が自動的に入力される、日付範囲の変更、広告の付加を含む。

      この契約は、「在庫ターゲット」セクションで自動的にターゲットになります。 その他のすべてのターゲット設定オプションは適用できません。

      1. クリック **[!UICONTROL Create placement]**.

配置は、パブリッシャーが PG 契約 ID をアクティブ化した後に実行を開始します。

>[!NOTE]
>
> 契約タグを発行者に送信して検証する必要はありません。

>[!MORELIKETHIS]
>
>* [プライベート在庫について](private-inventory-about.md)
>* [プライベート契約のプレースメントと広告のリスト](/help/dsp/inventory/private-deal-view-placements.md)
>* [Deal ID の詳細の手動作成](deal-id-create.md)
>* [手動の Deal ID 設定](deal-id-settings.md)
>* [プログラム的に保証された契約の設定](programmatic-guaranteed-set-up.md)
