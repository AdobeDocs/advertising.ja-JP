---
title: '''[!DNL Microsoft Advertising] 製品グループ設定'
description: の設定を参照します [!DNL Microsoft Advertising] 商品グループの買い物。
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 製品グループ設定

## 「すべての製品」製品グループ

**[!UICONTROL Condition]:** （読み取り専用）すべての製品

**[!UICONTROL Bid]:** （製品グループを含む場合のみ）広告クリックの支払いに最も高いクリック単価（CPC）。 この値は、子製品グループを持たないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

このテンプレートは、上位レベルのテンプレートをオーバーライドし、子製品グループを持たないユニットにのみ使用されます。

## その他すべての製品グループ

**[!UICONTROL Condition/Value]:** （既存の製品グループの場合は読み取り専用）ターゲットにする製品分析コード。 新製品グループの場合、製品のターゲットとなるディメンションと、選択した情報カテゴリの選定属性（ブランド別のターゲット設定の場合は「Acme」、条件でターゲット設定の場合は「新規」など）を入力します。

特定の商品ディメンション（「すべての商品」ではない）の商品グループを作成したら、検索、ソーシャルおよびCommerceは、「その他すべて」の商品グループを自動的に作成します。

使用可能な製品ディメンションのリストについては、「」を参照してください[買い物キャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」と入力します。 ディメンションのリストは、キャンペーンのに基づいて制限される場合があります [!UICONTROL Inventory Filter] の設定値。

**[!UICONTROL Excluded]:** （新しい製品グループの場合はオプション、既存の製品グループの場合は読み取り専用）一致する製品の広告の入札を除外します。

**[!UICONTROL Bid]:** （製品グループを含む場合のみ）広告クリックの支払いに最も高いクリック単価（CPC）。 この値は、子製品グループを持たないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

このテンプレートは、上位レベルのテンプレートをオーバーライドし、子製品グループを持たないユニットにのみ使用されます。

>[!MORELIKETHIS]
>
>* [ショッピング製品グループについて](product-group-about.md)
>* [ショッピング商品グループの管理](product-group-manage.md)
>* [買い物キャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [実装方法 [!DNL Microsoft Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
