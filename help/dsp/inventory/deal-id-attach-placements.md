---
title: プライベート取引のプレースメントと広告の指定
description: 追加のプレースメントや広告とプライベート取引を使用する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# プライベート取引のプレースメントと広告の指定

保証されていない取引の場合、から新しいプレースメントの在庫ターゲットとして取引を指定できます [!UICONTROL Placements] 表示。

プログラム保証（PG）取引の場合は、から指定された広告を使用してプレースメントを作成できます [!UICONTROL Deals] 表示。

以下の手順でも可能です [プレースメントに広告を添付](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) pg および保証されていない取引にいつでも関連付けられます。

## プレースメントの在庫ターゲットとしての保証されていない取引の指定

* [からプレースメントを作成 [!UICONTROL Placements] 表示](/help/dsp/campaign-management/placements/placement-create.md). が含まれる [!UICONTROL Inventory Targeting] 設定で、プライベート取引を選択します。

## PG 取引へのプレースメントと広告の添付

1. メインメニューで、 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 取引行で、  **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. が含まれる [!UICONTROL Ad & Campaign Selection] 設定で、プレースメントに使用する広告を選択します。

       1.広告主、キャンペーンおよび広告タイプを選択します。 必要に応じて、広告をフィルタリングするための広告ステータスを選択します。
       
       1. 使用可能な広告のリストから、取引に使用する各広告の横にあるチェックボックスを選択します。
       
       1. Click **[!UICONTROL Apply]**。
   
   1. プレースメント設定画面で、次の操作を行います。

      1. 配置名を入力します。

      1. （オプション）を編集します [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)（デフォルトの入札の上書き（契約の CPM 値が自動的に入力される）、日付範囲の変更、広告の添付など）。

      取引は「在庫ターゲット」セクションで自動的にターゲットされます。 その他のターゲティングオプションはすべて適用されません。

      1. クリック **[!UICONTROL Create placement]**.

パブリッシャーが PG 取引 ID をアクティベートすると、プレースメントの実行が開始されます。

>[!NOTE]
>
> 検証のために契約タグをパブリッシャーに送信する必要はありません。

>[!MORELIKETHIS]
>
>* [プライベートインベントリについて](private-inventory-about.md)
>* [プライベート取引のプレースメントと広告のリスト](/help/dsp/inventory/private-deal-view-placements.md)
>* [取引 ID の詳細の手動作成](deal-id-create.md)
>* [手動の取引 ID 設定](deal-id-settings.md)
>* [プログラムで保証された取引の設定](programmatic-guaranteed-set-up.md)
