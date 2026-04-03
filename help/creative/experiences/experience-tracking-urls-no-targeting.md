---
title: ターゲティングなしでエクスペリエンスのトラッキング URLをカスタマイズする
description: 決定木ターゲティングを使用せずに、エクスペリエンスの各クリエイティブのトラッキング URLをカスタマイズする方法を説明します。
feature: Creative Experiences
exl-id: 03a10285-c0df-4bc3-92c7-c1c2ea3f8129
TQID: https://experienceleague.adobe.com/0NvlDveOyfCjAIIXJ-lgdOQbI56tLvvutOaXrUu9fCk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# 決定木ターゲティングを使用しないエクスペリエンスのトラッキング URLをカスタマイズする

決定木ターゲティングを使用しないエクスペリエンスの場合、広告体験タグに使用するクリエイティブごとに、最大5つのカスタムインプレッション追跡URL、5つのカスタムクリックトラッキング URL、1つのカスタムランディングページ URLを作成できます。 トラッキング URLは、[!UICONTROL Tag Manager]内からカスタマイズできます。

カスタム URLは、広告エクスペリエンスタグから作成された広告にのみ使用され、[!UICONTROL Creative Libraries]の基本クリエイティブ設定には保存されません。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Tag Manager]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Tag Manager]**&#x200B;をクリックします。

1. （広告サイズのタグが存在しない場合）該当するクリエイティブサイズのタグを作成します。

   エクスペリエンスに使用するクリエイティブサイズごとに1つ以上のタグを作成できます。

   1. 右上の「**[!UICONTROL Create Tag]**」をクリックします。

   1. 一意の&#x200B;**[!UICONTROL Tag name]**&#x200B;を入力し、**[!UICONTROL Tag size]**&#x200B;を選択します。

      エクスペリエンスのデフォルトクリエイターのサイズによって、使用可能なサイズが決まります。

   1. **[!UICONTROL Create]**&#x200B;をクリックします。

1. 該当する広告タグの行の上にカーソルを置き、![&#x200B; トラッキング URLの編集](/help/creative/assets/edit-gray.png " トラッキング URLの編集") **[!UICONTROL Tracking URLs]**&#x200B;をクリックします。<!-- For targeted experiences, this is "EDIT Tracking URLs"  Tag Manager has only a list view, but no card view, as of 2/2. -->

   「[!UICONTROL Click Tracking URLs]」、「[!UICONTROL Impression Tracking URLs]」、「[!UICONTROL Landing URLs]」タブには、割り当てられたバンドル内の該当するサイズのすべてのクリエイターの名前が一覧表示されます。 エクスペリエンスの既定のクリエイターのサイズによって、使用可能なサイズが決まります。<!-- There's no distinct "Creative Sizes" setting. -->

1. **[!UICONTROL Click Tracking URLs]**、**[!UICONTROL Impression Tracking URLs]**、**[!UICONTROL Landing URLs]**&#x200B;の各タブで、必要に応じて各クリエイティブについて次の操作を行います。

   1. クリエイティブの行を展開します。

   1. 次のいずれかの操作を行います。

      * カスタム URLを追加または編集するには、入力フィールドにURLを入力します。

      * 別のカスタム URLを追加するには、**[!UICONTROL +]**&#x200B;をクリックし、入力フィールドにURLを入力します。

      * カスタム URLを削除するには、クリエイティブ行の上にカーソルを置き、![削除](/help/creative/assets/delete.png "削除")をクリックします。

      最大5つのカスタムインプレッショントラッキング URL、5つのカスタムクリックトラッキング URL、1つのカスタムランディングページ URLを含めることができます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; ターゲティングせずにエクスペリエンス用の広告タグにクリエイターを割り当てる](experience-tag-assign-creatives.md)
>* [決定木ターゲティングを使用したエクスペリエンスのトラッキング URLをカスタマイズする](experience-tracking-urls-targeting.md)
