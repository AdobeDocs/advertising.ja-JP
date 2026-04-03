---
title: エクスペリエンスのプレビュー
description: 広告エクスペリエンスでクリエイティブをプレビューする方法について説明します。
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
TQID: https://experienceleague.adobe.com/E8rpr53zbyr6XCVokT1b5OprM1jwdrFhQL5oBsonZQI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 554
ht-degree: 0%

---

# エクスペリエンスのプレビュー

すべてのハイパーリンクを含む、ターゲットビューアがエクスペリエンスに表示する特定の広告サイズのクリエイティブをプレビューできます。 決定木ターゲティングを使用するエクスペリエンスでは、単一のクリエイティブ、特定のブランチのクリエイティブ（ターゲットタイプ）、またはエクスペリエンス内のすべてのクリエイティブをプレビューできます。 決定木のターゲティングがないエクスペリエンスの場合は、1つのクリエイティブをプレビューできます。<!-- verify -->

* エクスペリエンスまたは特定のブランチのすべてのクリエイティブをプレビューすると、該当するすべてのクリエイティブが表示されます。

* 1つのクリエイティブをプレビューし、複数のクリエイティブを条件に合わせてプレビューすると、プレビューを更新するたびに表示されるクリエイティブは、エクスペリエンスの広告ローテーション設定に基づきます。

   * アルゴリズム広告のローテーションでは、最適化目標に基づいてクリエイティブが選択されます。

   * スケジュールされた広告ローテーションの場合、スケジュールの最初のクリエイティブが表示されます。 シーケンスを続行するには、プレビューの更新を続けることができます。

   * 重み付けされた広告のローテーションでは、指定された重み（Creative Aが表示される可能性が80%、Creative Bが表示される可能性が20%など）に基づいてクリエイティブが選択されます。

## 決定木ターゲティングによるエクスペリエンス内のクリエイティブのプレビュー

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. （オプション） [特定のエクスペリエンスを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Preview]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Preview]**&#x200B;をクリックします。

1. プレビューするクリエイティブを選択：

   * 単一のクリエイティブをプレビューするには：

      1. **[!UICONTROL Creative]**&#x200B;をクリックします。

      1. 広告のサイズを選択。

      1. 「[!UICONTROL Decision Tree Targeting]」セクションで、クリエイティブのターゲットを選択します。

   * 特定のブランチのクリエイティブをプレビューするには：

      1. **[!UICONTROL Particular branch]**&#x200B;をクリックします。

      1. 広告のサイズを選択。

     <!--
      I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. クリエイティブターゲットを選択します。

   * エクスペリエンス内のすべてのクリエイターをプレビューするには、**[!UICONTROL Entire Tree]**&#x200B;をクリックします。

     <!--
      I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. （オプション）クリエイティブの名前、クリエイティブのタイプとサイズ、ランディングページのURLまたはクリック URL、各クリエイティブの下の柔軟な属性を含めるには、**[!UICONTROL Display Creative Metadata]**&#x200B;を選択します。

1. **[!UICONTROL Preview]**&#x200B;をクリックします。

1. （クリエイティブによるプレビューのみ。オプション）ツールバーで、**[!UICONTROL Refresh]**&#x200B;をクリックして、広告のローテーション設定に従って、表示される可能性のある追加のクリエイティブをプレビューします。<!-- I don't see this as of 2/3 -->

1. （オプション）エクスペリエンスのデモ URLをコピーして、ログインせずに他のユーザーと共有するには、[!DNL Creative]にアクセスします。

   1. プレビューの右上にある「![共有](/help/creative/assets/share.png "共有")」をクリックします。

   1. [!UICONTROL Share Demo URL] ダイアログで、**[!UICONTROL Copy]**&#x200B;をクリックしてURLをクリップボードにコピーし、他のユーザーと共有できるようにします。

## 決定木のターゲティングなしで、エクスペリエンス内のクリエイティブをプレビュー

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. （オプション） [特定のエクスペリエンスを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Preview]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Preview]**&#x200B;をクリックします。

1. （オプション）特定のクリエイティブサイズを選択して、クリエイターのリストを制限します。

   デフォルトでは、すべてのサイズのクリエイターが一覧表示されます。

1. 広告タグの名前をクリックして行を展開し、クリエイティブをプレビューします。

1. （オプション）クリエイティブのランディングページに移動するには、クリエイティブをクリックします。

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （オプション）エクスペリエンスのデモ URLをコピーして、ログインせずに他のユーザーと共有するには、[!DNL Creative]にアクセスします。

   1. プレビューの右上にある「![共有](/help/creative/assets/share.png "共有")」をクリックします。

   1. [!UICONTROL Share Demo URL] ダイアログで、**[!UICONTROL Copy]**&#x200B;をクリックしてURLをクリップボードにコピーし、他のユーザーと共有できるようにします。

>[!MORELIKETHIS]
>
>* [決定木ターゲティングでエクスペリエンスを作成](experience-create-targeting.md)
>* [決定木ターゲティングを使用せずにエクスペリエンスを作成](/help/creative/experiences/experience-create-no-targeting.md)
