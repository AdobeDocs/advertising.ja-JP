---
title: プライベート取引のプレースメントと広告の指定
description: 追加のプレースメントと広告でプライベート契約を使用する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
TQID: https://experienceleague.adobe.com/ZCFqnc6cQLEqahDoElttE7DzeZCR3IRx2lkyyb3BPMs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 278
ht-degree: 0%

---

# プライベート取引のプレースメントと広告の指定

保証されていない取引の場合は、[!UICONTROL Placements] ビューから、新しいプレースメントの在庫ターゲットとして取引を指定できます。

プログラマティック保証（PG）取引の場合、[!UICONTROL Deals] ビューから、指定した広告を含むプレースメントを作成できます。

PGおよび保証されていない契約に関連するプレースメント [に](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)広告を添付することもできます。

## プレースメントの在庫目標として、保証されていない取引を指定します

* [ プレースメントを[!UICONTROL Placements] ビュー](/help/dsp/campaign-management/placements/placement-create.md)から作成します。 [!UICONTROL Inventory Targeting]設定で、プライベート契約を選択します。

## PG取引へのプレースメントと広告の添付

1. メインメニューで、**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**&#x200B;をクリックします

1. 取引行で、**[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**&#x200B;をクリックします。

1. [!UICONTROL Ad & Campaign Selection]設定で、プレースメントに使用する広告を選択します。

       1.広告主、キャンペーン、広告タイプを選択します。 オプションで、広告をフィルタリングする広告ステータスを選択します。
       
       1。 利用可能な広告のリストから、取引に使用する各広告の横にあるチェックボックスを選択します。
       
       1。 **[!UICONTROL Apply]**
をクリックします   
   1. プレースメント設定画面で、次の操作を行います。

      1. プレースメント名を入力します。

      1. （オプション） [ プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)を編集します。これには、取引のCPM値が自動的に入力されるデフォルト入札額の上書き、日付範囲の変更、追加の広告の添付などが含まれます。

      取引は、「在庫目標」セクションで自動的にターゲット設定されます。 その他のターゲティングオプションは適用できません。

      1. **[!UICONTROL Create placement]**&#x200B;をクリックします。

プレースメントは、パブリッシャーがPG取引IDをアクティブ化した後に実行を開始します。

>[!NOTE]
>
> 確認のために契約タグをパブリッシャーに送信する必要はありません。

>[!MORELIKETHIS]
>
>* [ プライベートインベントリについて](private-inventory-about.md)
>* [非公開取引のプレースメントと広告のリスト ](/help/dsp/inventory/private-deal-view-placements.md)
>* [取引IDの詳細を手動で作成する](deal-id-create.md)
>* [取引情報IDの手動設定](deal-id-settings.md)
>* [ プログラム的な保証契約の設定](programmatic-guaranteed-set-up.md)
