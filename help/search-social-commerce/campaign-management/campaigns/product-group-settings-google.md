---
title: '[!DNL Google Ads] 製品グループ設定'
description: 商品グループを買い物するため  [!DNL Google Ads]  設定を参照します。
exl-id: 2cfef9de-b265-4fa5-b1bd-84e6cba79914
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Google Ads] 製品グループ設定

## 「すべての製品」製品グループ

**[!UICONTROL Condition]:** （読み取り専用）すべての製品

**[!UICONTROL Bid]:** （製品グループを含む場合のみ）広告クリックの支払いに最も高いクリック単価（CPC）。 この値は、子製品グループを持たないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

このテンプレートは、上位レベルのテンプレートをオーバーライドし、子製品グループを持たないユニットにのみ使用されます。

## その他すべての製品グループ

**[!UICONTROL Condition/Value]:** （既存の製品グループの場合は読み取り専用）ターゲットにする製品分析コード。 新製品グループの場合、製品のターゲットとするディメンション、および選択した情報カテゴリの選定属性（ブランド別のターゲット設定を行う場合は「Acme」、条件でターゲット設定を行う場合は「新規」など）を入力します。

特定の商品ディメンション（「すべての商品」ではない）の商品グループを作成したら、検索、ソーシャルおよびCommerceは、「その他すべて」の商品グループを自動的に作成します。

使用可能な製品ディメンションのリストについては、「[ ショッピングキャンペーン製品フィルター ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)」を参照してください。 ディメンションのリストは、キャンペーンの [!UICONTROL Inventory Filter] 設定に基づいて制限される場合があります。

**[!UICONTROL Excluded]:** （新しい製品グループの場合はオプション、既存の製品グループの場合は読み取り専用）一致する製品の広告の入札を除外します。

**[!UICONTROL Bid]:** （製品グループを含む場合のみ）広告クリックの支払いに最も高いクリック単価（CPC）。 この値は、子製品グループを持たないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

このテンプレートは、上位レベルのテンプレートをオーバーライドし、子製品グループを持たないユニットにのみ使用されます。

>[!MORELIKETHIS]
>
>* [ ショッピング商品グループについて ](product-group-about.md)
>* [ ショッピング商品グループの管理 ](product-group-manage.md)
>* [ 買い物キャンペーン製品フィルター ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [ 買い物キャンペ  [!DNL Google Ads]  ンの実装 ](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
