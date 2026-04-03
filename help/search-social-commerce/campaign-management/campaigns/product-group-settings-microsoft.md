---
title: '[!DNL Microsoft Advertising]製品グループの設定'
description: ' [!DNL Microsoft Advertising] 買い物商品グループの設定を参照します。'
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/xbYc0Xe-FsgGq-jqZdzZ4Rj877BL6NCxb4utaEMmCdY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 270
ht-degree: 0%

---

# [!DNL Microsoft Advertising]製品グループの設定

## 「すべての製品」製品グループ

**[!UICONTROL Condition]:** （読み取り専用）すべての製品

**[!UICONTROL Bid]:** （含まれる製品グループのみ）広告クリックに対する支払い額が最も高いクリック単価（CPC）です。 この値は、子製品グループのないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

このテンプレートは、より高いレベルでテンプレートを上書きし、子製品グループのないユニットにのみ使用されます。

## その他すべての製品グループ

**[!UICONTROL Condition/Value]:** （既存の製品グループの読み取り専用） ターゲットにする製品ディメンション。 新しい製品グループの場合、製品のターゲットとなるディメンションと、選択した情報カテゴリの適格属性を入力します（ブランド別のターゲット設定の場合は「Acme」、条件別のターゲット設定の場合は「New」など）。

特定の商品ディメンション（つまり「すべての商品」ではなく）の商品グループを作成すると、Search, Social, &amp; Commerceは、「その他」の商品グループを自動的に作成します。

使用可能な製品ディメンションのリストについては、「[&#x200B; ショッピングキャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)」を参照してください。 ディメンションのリストは、キャンペーンの[!UICONTROL Inventory Filter]設定に基づいて制限される場合があります。

**[!UICONTROL Excluded]:** （新製品グループの場合はオプション、既存製品グループの場合は読み取り専用）一致する製品の広告の入札を除外します。

**[!UICONTROL Bid]:** （含まれる製品グループのみ）広告クリックに対する支払い額が最も高いクリック単価（CPC）です。 この値は、子製品グループのないユニットにのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

このテンプレートは、より高いレベルでテンプレートを上書きし、子製品グループのないユニットにのみ使用されます。

>[!MORELIKETHIS]
>
>* [&#x200B; ショッピング商品グループについて](product-group-about.md)
>* [&#x200B; ショッピング商品グループの管理](product-group-manage.md)
>* [&#x200B; ショッピングキャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [&#x200B; ショッピング キャンペーン  [!DNL Microsoft Advertising] を実装](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
