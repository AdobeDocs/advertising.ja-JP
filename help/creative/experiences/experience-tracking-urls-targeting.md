---
title: エクスペリエンスのトラッキング URLのカスタマイズ
description: 決定木ターゲティングを使用して、エクスペリエンスの各クリエイティブのトラッキング URLをカスタマイズする方法について説明します。
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%
---
# デジジョンツリーのターゲティング機能により、エクスペリエンス内のクリエイターのトラッキング URLをカスタマイズ

*既存のクリエイターのみを含むTarget ノード*

デジジョンツリーのターゲティングを使用するエクスペリエンスでは、エクスペリエンスに使用する個々のクリエイティブに対して、最大5つのカスタムインプレッション追跡URLと5つのカスタムクリックトラッキング URLを作成できます。 ランディングページの上書きが可能な場合は、1つのカスタムランディングページ URLを指定することもできます。 トラッキング URLは、任意のディシジョンツリーエディター内からカスタマイズできます。

カスタム URLは、エクスペリエンスから作成された広告にのみ使用され、[!UICONTROL Creative Libraries]の基本クリエイティブ設定には保存されません。

ランディングページの上書きは、標準のエクスペリエンスと、デフォルトのクリエイティブを使用するノードで使用できます。 割り当てられた動的バンドルの場合、ランディングページはフィードによって決まり、「ランディングページ」タブは表示されません。

## AI ドリブン型エディターの使用（Beta） {#ai-editor}

エクスペリエンスを[作成中](experience-create-targeting.md#ai-editor)または[編集中](experience-edit-targeting.md#ai-editor)に、キャンバス コントロールを使用します。

1. ターゲットノードの下にあるクリエイティブなリーフ ノードで、**[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**&#x200B;をクリックします。

1. 「**[!UICONTROL Click Tracking URLs]**」、「**[!UICONTROL Impression Tracking URLs]**」または「（使用可能な場合） **[!UICONTROL Landing URL]**」タブを選択します。

   クリエイターはバンドルでグループ化されます。 エクスペリエンスのデフォルトのクリエイティブサイズによって、使用可能なクリエイティブサイズが決まります。

1. 編集するクリエイティブを展開し、次のいずれかの操作を行います。

   * カスタム URLを追加または編集するには、入力フィールドにURLを入力します。

   * 別のカスタムトラッキング URLを追加するには、**[!UICONTROL Add URL]**&#x200B;をクリックし、入力フィールドにURLを入力します。

   * カスタム URLを削除するには、**[!UICONTROL Delete URL]**&#x200B;をクリックします。

   編集したフィールドの外側をクリックし、保存する前に検証エラーを修正します。

1. ダイアログで「**[!UICONTROL Save]**」をクリックして、作業ツリーを更新します。

1. [&#x200B; ツリーヘッダーからエクスペリエンス &#x200B;](#save)を保存します。

## 手動エディターの使用 {#manual-editor}

[次の手順に従う前に、手動エディター](experience-edit-targeting.md#experience-open)を開きます。

1. ターゲットノードの下にあるクリエイティブなリーフ ノードで、**[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**&#x200B;をクリックします。

1. 「**[!UICONTROL Click Tracking URLs]**」、「**[!UICONTROL Impression Tracking URLs]**」または「（使用可能な場合） **[!UICONTROL Landing URLs]**」タブを選択します。

   タブには、割り当てられたバンドル内のクリエイターが一覧表示されます。 エクスペリエンスの既定のクリエイティブ サイズによって、使用可能なクリエイティブ サイズが決まります。<!-- There's no distinct "Creative Sizes" setting. -->

1. 編集するクリエイティブを展開し、次のいずれかの操作を行います。

   * カスタム URLを追加または編集するには、入力フィールドにURLを入力します。

   * 別のカスタムトラッキング URLを追加するには、**[!UICONTROL +]**&#x200B;をクリックし、入力フィールドにURLを入力します。

   * カスタム URLを削除するには、クリエイティブ行の上にカーソルを置き、![削除](/help/creative/assets/delete.png "削除")をクリックします。

1. ダイアログで「**[!UICONTROL Save]**」をクリックして、作業ツリーを更新します。

1. [&#x200B; ツリーヘッダーからエクスペリエンス &#x200B;](#save)を保存します。

## エクスペリエンスを保存 {#save}

次の手順は、両方のエディターに適用されます。 トラッキング URL ダイアログを単独で保存しても、エクスペリエンスは保存または公開されません。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [決定木ターゲティングを使用しないエクスペリエンスのトラッキング URLをカスタマイズする](experience-tracking-urls-no-targeting.md)
