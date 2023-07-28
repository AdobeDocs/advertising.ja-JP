---
title: '''[!DNL Google Ads] 製品グループの設定'
description: 次の設定を参照してください： [!DNL Google Ads] 買い物製品グループ。
exl-id: 3bf33d78-0ad5-43c7-970a-2f2d2e591802
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Google Ads] 製品グループの設定

## 「すべての製品」製品グループ

**[!UICONTROL Condition]:** （読み取り専用）すべての製品

**[!UICONTROL Bid]:** （製品グループのみを含む）最大クリック単価 (CPC)。広告クリックに対して支払われる金額の上限です。 この値は、子製品グループのない単位に対してのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

このテンプレートは、上位レベルのテンプレートを上書きし、子製品グループのない単位に対してのみ使用されます。

## その他のすべての製品グループ

**[!UICONTROL Condition/Value]:** （既存の製品グループの場合は読み取り専用）ターゲットにする製品ディメンション。 新しい製品グループの場合、製品をターゲットにするディメンションと、選択した情報カテゴリの資格属性（ブランドでターゲット設定する場合は「Acme」、条件でターゲット設定する場合は「新規」など）を入力します。

特定の製品ディメンション（「すべての製品」ではなく）の製品グループを作成すると、検索、ソーシャル、コマースは「その他すべて」の製品グループを自動的に作成します。

使用可能な製品ディメンションのリストについては、[買い物キャンペーンの製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; ディメンションのリストは、キャンペーンの [!UICONTROL Inventory Filter] 設定。

**[!UICONTROL Excluded]:** （新しい製品グループの場合はオプション、既存の製品グループの場合は読み取り専用）一致する製品の広告の入札を除外します。

**[!UICONTROL Bid]:** （製品グループのみを含む）最大クリック単価 (CPC)。広告クリックに対して支払われる金額の上限です。 この値は、子製品グループのない単位に対してのみ使用され、広告グループレベルの値の代わりに使用されます。

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

このテンプレートは、上位レベルのテンプレートを上書きし、子製品グループのない単位に対してのみ使用されます。

>[!MORELIKETHIS]
>
>* [買い物製品グループについて](product-group-about.md)
>* [買い物製品グループの管理](product-group-manage.md)
>* [買い物キャンペーンの製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [実装方法 [!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
