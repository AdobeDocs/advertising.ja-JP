---
title: カスタム指標の作成
description: 標準指標から計算されるカスタム指標を設定する方法について説明します。
exl-id: a9ce503a-67ee-477e-8f79-31b4a9c6e51a
feature: Search Common Tasks, Search Custom Metrics
TQID: 'https://experienceleague.adobe.com/g-J8AlulQ20I-vxQrPkPaP-Ap66bBIng0eKDPqhV9U4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: a1695a4d-41fb-5bb6-a22a-9e7a1b3222d7
    internal-label: Search Custom Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 9837cac1a920b1b3b88b04b150cb604832209eaf
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%
---
# カスタム指標の作成

## （新しいUI）管理ビューからカスタム指標を作成する

*ほとんどのエンティティ ビューで[!UICONTROL Manage] メニュー、<!-- [!UICONTROL Plan] > [!UICONTROL Simulations],-->で利用できます [!UICONTROL Setup] > [!UICONTROL Label Classifications]、[!UICONTROL Goals] > [!UICONTROL Objectives] and [!UICONTROL Constraints]、[!UICONTROL Targeting] > [!UICONTROL Placements]*

1. データテーブルの上で、次のいずれかの操作を行います。

   * 現在適用されているビューの名前（![&#x200B; ビュー](/help/search-social-commerce/assets/view.png " ビュー")）をクリックします。 編集可能なビューの名前の上にカーソルを置き、![Edit](/help/search-social-commerce/assets/edit-new.png "Edit")をクリックしてビュー設定を開きます。

     作成したカスタム指標は、すべてのビューで使用できるようになります。

   * ![&#x200B; カスタム列](/help/search-social-commerce/assets/custom-columns-new.png " カスタム列")をクリックして、列構成設定を開きます。

1. 開いた列リストの下で、![&#x200B; カスタム指標の作成](/help/search-social-commerce/assets/add.png " カスタム指標の作成") **[!UICONTROL Create Custom Metric]**&#x200B;をクリックします。

1. [&#x200B; カスタム指標設定](custom-metric-settings.md)を指定します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## （新しいUI）レポートまたはレポートテンプレート設定からカスタム指標を作成する {#create-from-report-settings}

1. レポートまたはレポートテンプレートの設定内で、**[!UICONTROL Columns]** ステップに移動します。

1. 「**[!UICONTROL Custom Metrics]**」セクションで、指標の設定を指定します。

   * **[!UICONTROL Custom Metric Name]:**&#x200B;指標の名前を入力します。

   * **[!UICONTROL Format]:** **[!UICONTROL Currency]**、**[!UICONTROL Number to 2 Decimal Places]**、**[!UICONTROL Number to 3 Decimal Places]**、**[!UICONTROL Number w/out Decimal Places]**&#x200B;または&#x200B;**[!UICONTROL Percentage]**&#x200B;を選択してください。

   * **[数式入力フィールド ]:**&#x200B;指標を&#x200B;**[!UICONTROL Insert Metric]**&#x200B;から選択し、オペレーターボタン （`+`、`-`、`*`、`/`、`(`、および`)`）をクリックして数式を作成します。 数式を手動で入力することもできます。 各指標または演算子を挿入する場所にカーソルを置きます。

1. **[!UICONTROL Add Metric]**&#x200B;をクリックします。

   指標が正常に作成されると、使用可能な列のリストが指標の名前でフィルタリングされます。 指標を作成しても、レポートに自動的に含まれるわけではありません。

1. レポートに指標を含めるには、使用可能な列リストで指標を選択し、![右向き矢印](/help/search-social-commerce/assets/arrow-right-customize.png "右向き矢印")をクリックして、選択済み列リストに移動します。

## （レガシーUI）キャンペーン管理ビューからカスタム指標を作成する

1. データテーブルの上で、次のいずれかの操作を行います。

   * デフォルトのビューまたはカスタムビューの名前をクリックして、ビュー設定を開きます。

   * ![&#x200B; カスタム列](/help/search-social-commerce/assets/custom-columns.png " カスタム列")をクリックして、列構成設定を開きます。

1. 開いた列リストの下で、![新しいカスタム指標を作成](/help/search-social-commerce/assets/add.png "新しいカスタム指標を作成") **[!UICONTROL Create New Custom Metric]**&#x200B;をクリックします。

1. [&#x200B; カスタム指標設定](custom-metric-settings.md)を指定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## （従来のUI） レポートまたはレポートテンプレートフォームからカスタム指標を作成する

1. レポートまたはレポートテンプレートフォーム内で、「**[!UICONTROL Columns]**」タブに移動します。

1. 右側のセクションで、**[!UICONTROL Create]**&#x200B;をクリックします。

1. [&#x200B; カスタム指標設定](custom-metric-settings.md)を指定します。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

## （レガシーUI） [!UICONTROL Portfolios] ビューからカスタム指標を作成する

1. データテーブルの上で、![選択したビューを編集](/help/search-social-commerce/assets/view-settings.png "選択したビューを編集")をクリックします。

1. 「**[!UICONTROL Columns]**」タブをクリックします。

1. 右側のセクションで、**[!UICONTROL Create]**&#x200B;をクリックします。

1. [&#x200B; カスタム指標設定](custom-metric-settings.md)を指定します。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; カスタム指標について](custom-metric-about.md)
>* [&#x200B; カスタム指標を編集](custom-metric-edit.md)
>* [&#x200B; カスタム指標を削除](custom-metric-delete.md)
>* [&#x200B; カスタム指標設定](custom-metric-settings.md)
