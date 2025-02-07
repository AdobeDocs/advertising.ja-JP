---
title: エクスペリエンスのプレビュー
description: 広告エクスペリエンスでクリエイティブをプレビューする方法を説明します。
feature: Creative Experiences
source-git-commit: 14d972044d485ead5101f1c383d2726bb6fd9d25
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# エクスペリエンスのプレビュー

*クローズドベータ版*

特定の広告サイズを持つクリエイティブを、ターゲットビューアに表示されるエクスペリエンス（すべてのハイパーリンクを含む）でプレビューできます。 デシジョンツリーのターゲット設定を使用したエクスペリエンスの場合は、1 つのクリエイティブ、特定のブランチ（ターゲットタイプ）のクリエイティブまたはエクスペリエンス内のすべてのクリエイティブをプレビューできます。 決定ツリーのターゲティングを持たないエクスペリエンスの場合は、1 つのクリエイティブをプレビューできます。<!-- verify -->

* エクスペリエンスまたは特定のブランチのすべてのクリエイティブをプレビューすると、該当するすべてのクリエイティブが表示されます。

* 1 つのクリエイティブをプレビューし、条件に一致する複数のクリエイティブを表示すると、プレビューを更新するたびに表示されるクリエイティブは、エクスペリエンスの広告のローテーション設定に基づきます。

   * アルゴリズム広告のローテーションの場合、クリエイティブは最適化目標に基づいて選択されます。

   * 重み付けされた広告のローテーションの場合、クリエイティブは指定された重み付け（クリエイティブ A が表示される 80% のチャンス、クリエイティブ B が表示される 20% のチャンスなど）に基づいて毎回選択されます。

   * スケジュールされた広告ローテーションの場合、最初にスケジュールの最初のクリエイティブが表示され、引き続きプレビューを更新して、シーケンスを続行できます。<!-- Refresh isn't there as of 2/3 -->

## 意思決定ツリーのターゲット設定を使用したエクスペリエンスでのクリエイティブのプレビュー

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のエクスペリエンスを含めます。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Preview]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Preview]** をクリックします。

1. プレビューするクリエイティブを選択：

   * 1 つのクリエイティブをプレビューするには：

      1. 「**[!UICONTROL Creative]**」をクリックします。

      1. 広告サイズを選択します。

      1. 「[!UICONTROL Decision Tree Targeting]」セクションで、クリエイティブターゲットを選択します。

   * 特定のブランチのクリエイティブをプレビューするには：

      1. 「**[!UICONTROL Particular branch]**」をクリックします。

      1. 広告サイズを選択します。

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. クリエイティブターゲットを選択します。

   * エクスペリエンス内のすべてのクリエイティブをプレビューするには、「**[!UICONTROL Entire Tree]**」をクリックします。

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. （オプション）クリエイティブの名前、クリエイティブのタイプとサイズ、ランディングページの URL またはクリック URL、各クリエイティブの下にある柔軟な属性を含めるには、「**[!UICONTROL Display Creative Metadata]**」を選択します。

1. 「**[!UICONTROL Preview]**」をクリックします。

1. （クリエイティブによるプレビューのみ。オプション）ツールバーの「**[!UICONTROL Refresh]**」をクリックし、広告の回転設定に従って、表示される可能性のある追加のクリエイティブをプレビューします。<!-- I don't see this as of 2/3 -->

1. （任意）エクスペリエンスのデモ URL をコピーして、[!DNL Creative] へのログインなしで他のユーザーと共有するには、次のようにします。

   1. プレビューの右上にある「![ 共有 ](/help/creative/assets/share.png " 共有 ")」をクリックします。

   1. [!UICONTROL Share Demo URL] ダイアログで、「**[!UICONTROL Copy]**」をクリックして URL をクリップボードにコピーし、他のユーザーと共有できるようにします。


## デシジョンツリーのターゲット設定を使用しないエクスペリエンスでのクリエイティブのプレビュー

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のエクスペリエンスを含めます。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Preview]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Preview]** をクリックします。

1. （任意）特定のクリエイティブサイズを選択して、クリエイティブのリストを制限します。

   デフォルトでは、すべてのサイズのクリエイティブが一覧表示されます。

1. 広告タグの名前をクリックして行を展開し、クリエイティブをプレビューします。

1. （任意）エクスペリエンスのデモ URL をコピーして、[!DNL Creative] へのログインなしで他のユーザーと共有するには、次のようにします。

   1. プレビューの右上にある「![ 共有 ](/help/creative/assets/share.png " 共有 ")」をクリックします。

   1. [!UICONTROL Share Demo URL] ダイアログで、「**[!UICONTROL Copy]**」をクリックして URL をクリップボードにコピーし、他のユーザーと共有できるようにします。

>[!MORELIKETHIS]
>
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ デシジョンツリーのターゲット設定を使用しないエクスペリエンスの作成 ](/help/creative/experiences/experience-create-no-targeting.md)
