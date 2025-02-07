---
title: ターゲティングを使用しないエクスペリエンス用のトラッキング URL のカスタマイズ
description: 決定ツリーターゲティングを使用せずに、エクスペリエンスで各クリエイティブのトラッキング URL をカスタマイズする方法を説明します。
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# デシジョンツリーのターゲット設定を使用しないエクスペリエンス用のトラッキング URL のカスタマイズ

*クローズドベータ版*

決定ツリーターゲティングのないエクスペリエンスの場合、[!UICONTROL Tag Manager] 内から広告エクスペリエンスタグに使用するクリエイティブごとに、最大 5 つのカスタムインプレッショントラッキング URL、5 つのカスタムクリックトラッキング URL、1 つのカスタムランディングページ URL を作成できます。

カスタム URL は、広告エクスペリエンスタグから作成された広告にのみ使用され、[!UICONTROL Creative Libraries] のベースのクリエイティブ設定には保存されません。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Tag Manager]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Tag Manager]** をクリックします

1. （広告サイズのタグが存在しない場合）該当するクリエイティブサイズのタグを作成します。

   エクスペリエンスに使用するクリエイティブサイズごとに 1 つ以上のタグを作成できます。

   1. 右上で、「**[!UICONTROL Create Tag]**」をクリックします。

   1. 一意の **[!UICONTROL Tag name]** を入力し、**[!UICONTROL Tag size]** を選択します。

      使用可能なサイズは、エクスペリエンスのデフォルト画像クリエイティブのサイズによって決まります。

   1. 「**[!UICONTROL Create]**」をクリックします。

1. 該当する広告タグの行の上にカーソルを置き、![ トラッキング URL を編集 ](/help/creative/assets/edit-gray.png " トラッキング URL を編集 ")**[!UICONTROL Tracking URLs]** をクリックします。 <!-- For targeted experiences, this is "EDIT Tracking URLs" -->&lt;!— 2/2 現在、タグマネージャーにはリスト表示しかありませんが、カード表示はありません。>

   「[!UICONTROL Click Tracking URLs]」、「[!UICONTROL Impression Tracking URLs]」および「[!UICONTROL Landing URLs]」タブには、割り当てられたバンドル内の該当するサイズのすべてのクリエイティブの名前が一覧表示されます。 適用可能なサイズは、エクスペリエンスのデフォルト画像クリエイティブのサイズによって決まります。<!-- There's no distinct "Creative Sizes" setting. -->

1. 「**[!UICONTROL Click Tracking URLs]**」、「**[!UICONTROL Impression Tracking URLs]**」、「**[!UICONTROL Landing URLs]**」の各タブで、必要に応じてクリエイティブごとに次の操作を行います。

   1. クリエイティブの行を展開します。

   1. 次のいずれかの操作をおこないます。

      * カスタム URL を追加または編集するには、入力フィールドに URL を入力します。

      * 別のカスタム URL を追加するには、「**[!UICONTROL +]**」をクリックし、入力フィールドに URL を入力します。

      * カスタム URL を削除するには、クリエイティブ行の上にカーソルを置き、「![ 削除 ](/help/creative/assets/delete.png " 削除 ")」をクリックします。

      最大 5 つのカスタムインプレッショントラッキング URL、5 つのカスタムクリックトラッキング URL、1 つのカスタムランディングページ URL を含めることができます。

1. 「**[!UICONTROL Save]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ ターゲティングを行わないエクスペリエンスの広告タグへのクリエイティブの割り当て ](experience-tag-assign-creatives.md)
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンス用のトラッキング URL のカスタマイズ ](experience-tracking-urls-targeting.md)
